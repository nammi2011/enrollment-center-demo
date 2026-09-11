# Customer Enrollment Center — Interactive Demo

A self-contained, static HTML demo of a **Customer Enrollment Center** concept for
SAP Service Cloud Version 2, illustrating a BTP-hosted extension UI for utility
customer program enrollment.

## Pages

| Page | Mode |
|---|---|
| `index.html` | Combined — Work Center / Move-In toggle |
| `workcenter.html` | Work Center only (identified customer with active contracts, persona switcher) |
| `movein.html` | Move-In embedded step only (pre-active context, deferred fulfillment) |

Live (GitHub Pages, once enabled): https://nammi2011.github.io/enrollment-center-demo/ ,
`/workcenter.html`, `/movein.html`

## What it shows

- Two access modes: standalone **Work Center** and **Move-In (embedded)** pre-active context
- **Seven customer personas** (combo CA-per-utility, credit/AMI-fault, combo single-CA medical, commercial+BESS, non-AMI, medical+AMI, prepay-active) selectable in Work Center mode
- **Per-utility device model**: device number, meter number, AMI/AMR type and connection status per service; DER equipment (EV charger, battery, generator) shown where present
- Program catalog from the legacy Enrollment Center scope: PTR, CPP, TOU, Peak Power Savers, Smart Thermostat, CSDD, eBill, DPP, Budget Billing, PrePay, CARE/FERA, Medical Alert, Commercial DR
- The four Enrollment Center panels: Participating Programs, Available (Eligible) Programs,
  Eligibility Messages (hard stop / warning severities), Program History
- Enrollment wizard with program-specific data capture, consent recording and idempotent submission
- Deferred fulfillment: move-in enrollments parked as *Enrollment Request* and auto-dispatched
  on the simulated contract-activation event; cancellation cascade on move-in cancel
- Supervisor override flow for warning-level eligibility failures
- De-enrollment with exit-rule validation
- A simulated Integration Monitor showing API calls and event traffic

## Notes

- **All data is fictitious.** No real customers, systems or APIs are involved;
  everything is simulated in the browser and resets on page reload.
- Single file, no dependencies: open `index.html` in any modern browser.
