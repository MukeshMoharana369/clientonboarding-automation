# Client Onboarding Automation (Manual Payment)

## What this is

This project is a **simple onboarding automation** for coaches and consultants who **confirm payments manually** (UPI, bank transfer, cash, etc.).

It solves one specific problem:

> Making sure onboarding starts consistently **after** payment is confirmed.

No more. No less.

---

## The problem it addresses

In many coaching businesses:
- Payment is confirmed manually
- Onboarding is also handled manually
- Things get delayed, forgotten, or done inconsistently

This creates friction **before coaching even begins**.

This automation removes that friction without taking control away from the coach.

---

## How it works (plain English)

1. A client pays using any manual method  
2. The coach verifies the payment  
3. The coach updates the client’s status to `CLIENT` in Google Sheets  
4. The automation starts immediately  
5. Onboarding content is prepared  
6. The client receives a clear welcome and next steps  
7. The coach gets confirmation  
8. The automation stops  

That’s the entire lifecycle.

---

## What triggers the automation

The workflow listens to **one signal only**:
Status = CLIENT


This value is set manually by the coach.

Everything else is ignored.

---

## Role of AI in this project

AI is used **only for preparation**.

It is responsible for:
- Drafting a welcome message
- Preparing onboarding steps
- Generating intake questions
- Creating a short internal summary for the coach

AI does **not**:
- Coach the client
- Give advice
- Make decisions
- Modify programs

All AI behavior follows a coach-written SOP.

---

## Why Google Sheets is used

Google Sheets acts as a **simple control panel**.

It was chosen because:
- Coaches already use it
- No training is required
- It works with any payment method
- It keeps human responsibility clear

This project intentionally avoids fragile payment integrations.

---

## What this is NOT

This project is not:
- A payment system
- An AI coaching tool
- A CRM replacement
- A long-running automation
- A “smart” system

It is a **reliable system**.

---

## Workflow summary

- Google Sheets trigger (row updated)
- Status check (`CLIENT`)
- Data normalization and validation
- SOP fetch
- AI preparation
- Client onboarding email
- Coach notification
- Stop

No loops.  
No reminders.  
No background processes.

