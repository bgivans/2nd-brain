# GIVANS GLOBAL — STANDARD LEADS TABLE SQL
# Run this in every new client Supabase project

## Step 1: Create Table
CREATE TABLE public.leads (
  id uuid DEFAULT gen_random_uuid() PRIMARY KEY,
  created_at timestamptz DEFAULT now(),
  contact_name text NOT NULL,
  contact_email text NOT NULL,
  contact_phone text,
  best_contact_method text NOT NULL,
  primary_selection text,
  project_description text,
  service_location text,
  budget_range text,
  timeline text,
  decision_maker text,
  how_they_found_us text,
  source text DEFAULT 'website',
  status text DEFAULT 'new',
  internal_notes text,
  follow_up_date date
);

## Step 2: Enable RLS
ALTER TABLE public.leads ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Anyone can submit a lead"
  ON public.leads FOR INSERT TO anon
  WITH CHECK (true);

CREATE POLICY "Authenticated users can view leads"
  ON public.leads FOR SELECT TO authenticated
  USING (true);

CREATE POLICY "Authenticated users can update leads"
  ON public.leads FOR UPDATE TO authenticated
  USING (true) WITH CHECK (true);

## Step 3: updated_at trigger
CREATE OR REPLACE FUNCTION public.handle_updated_at()
RETURNS trigger AS $$
BEGIN
  NEW.updated_at = now();
  RETURN NEW;
END;
$$ LANGUAGE plpgsql;

## Step 4: Email notification trigger
CREATE OR REPLACE FUNCTION public.notify_new_lead()
RETURNS trigger AS $$
BEGIN
  PERFORM net.http_post(
    url := current_setting('app.edge_function_url'),
    headers := json_build_object(
      'Content-Type', 'application/json',
      'Authorization', 'Bearer ' || 
      current_setting('app.anon_key')
    )::jsonb,
    body := row_to_json(new)::text::jsonb
  );
  RETURN NEW;
END;
$$ LANGUAGE plpgsql SECURITY DEFINER;

CREATE TRIGGER on_new_lead_submitted
  AFTER INSERT ON public.leads
  FOR EACH ROW EXECUTE PROCEDURE public.notify_new_lead();

## Supabase Secrets to add per project
# RESEND_API_KEY = [from resend.com]
# CLIENT_EMAIL = [business owner email]
# CLIENT_NAME = [owner name]
# BUSINESS_NAME = [business name]
# FROM_EMAIL = [verified sender on resend]
