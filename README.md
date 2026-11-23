# HomeFix Uganda: E-Commerce Prototype (MGT3151)

Two-sided marketplace connecting property owners with verified technicians.
Prototype only. Fictitious data and sandbox payments. No real money, PINs, OTPs or personal data.

## Run locally (no install, no build)
1. Download or clone this repository.
2. Open `index.html` in Chrome, Edge or Firefox (double-click).
   Optional local server: `python3 -m http.server 8000` then open http://localhost:8000
Requirements: any modern browser. Internet is only used to load Google Fonts (the app works without it).

## Demo accounts (password for all: `Demo@123`)
| Role | Email |
|---|---|
| Customer | customer@homefix.demo |
| Technician | tech@homefix.demo |
| Admin | admin@homefix.demo |

## Website pages
Home, Find a technician, technician profiles, How it works, Pricing, For technicians, About, Help centre (FAQ), Contact, Terms, Privacy, Create account (customer or technician), Sign in, Forgot password, My account.
Signed-in areas: customer (jobs, properties, booking, payment), technician dashboard, admin (verification, disputes, audit log).

## Workflow (E-Commerce MVP)
Cities: Kampala, Wakiso, Mukono.
Discover/search > select technician > 6-step booking > technician quotation > customer approval >
job tracking and chat > sandbox mobile-money payment > receipt and 90-day warranty > review / warranty claim.
Admin verifies technicians, resolves warranty disputes and reads the audit log.

## Controls built in
- Account registration with validation; passwords stored as salted SHA-256 hashes (prototype, in browser)
- Role-based route guards (customer / technician / admin) with "Access denied" page
- Input validation on login, booking, quotation, payment, review, claim and chat forms
- Sandbox payment: never asks for PIN, OTP or card; includes a simulated failure path
- Audit log of key actions (login, booking, quote, payment, review, claim, verification, denied access)
- Data kept in browser localStorage only; "Reset demo data" button in the footer
- Accessibility: semantic HTML, labelled inputs, visible focus, keyboard navigation, AA contrast

## Test cases
Suggested cases TC1 to TC8: 5 positive (login, filter, booking, quote and approval, payment with receipt and warranty), 2 validation (bad login, invalid phone or past date), 1 access control (customer opening #admin).
Record expected result, actual result, screenshot and status in the report.

## Files
- `index.html`: the whole app (HTML, CSS, JavaScript, mock data in the `seed()` function)

## Limitations
No backend, real authentication, real payments, real ID verification or notifications. These are simulated.

## AI-use declaration
Generative AI (Claude) was used to help generate the prototype code. Declare this in the report appendix.
