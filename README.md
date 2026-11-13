# ARCA

### Your sustainability data. Backed by evidence.

**ARCA is an evidence-based sustainability reporting platform in development for small and medium-sized manufacturers.**

It aims to help manufacturers turn existing business documents—starting with electricity bills—into structured, traceable carbon data that can support sustainability reporting and customer information requests.

---

## The problem

Small and medium-sized manufacturers increasingly encounter requests from customers, suppliers and business partners for environmental and sustainability information.

However, the underlying information is often scattered across:
- Electricity and utility bills
- Operational records
- Supplier documents
- Spreadsheets
- Internal administrative files

Collecting, interpreting and validating this information can be time-consuming, especially for businesses without dedicated sustainability teams.

ARCA is being built to make this process more structured, transparent and manageable.

## The solution

ARCA focuses on turning existing business records into documented sustainability evidence.

The initial product focuses on **purchased electricity and Scope 2 emissions using the location-based method**.

The intended workflow:

1. **Upload** – Submit an electricity bill in PDF format.
2. **Extract** – Identify relevant information such as electricity consumption, billing period and supplier.
3. **Review** – Allow a user to inspect and correct extracted information.
4. **Calculate** – Apply a documented emission factor to confirmed electricity consumption.
5. **Trace** – Maintain links between source documents, confirmed values, emission factors and calculations.
6. **Report** – Generate a structured sustainability report with supporting evidence.

The objective is simple: make reported figures easier to understand, review and substantiate.

## Initial focus: Scope 2 reporting

ARCA's first use case is electricity-related Scope 2 reporting for German manufacturing SMEs.

The initial calculation follows the basic relationship:

**Electricity consumption × applicable emission factor = estimated emissions**

For example:

`kWh × kg CO₂e/kWh = kg CO₂e`

The calculation engine is designed to use deterministic arithmetic rather than allowing a generative AI model to determine reported emissions.

Emission factors must be traceable to their source, geographical scope, reporting year, units and methodology.

ARCA's initial focus is location-based accounting. Market-based accounting and other emissions categories are outside the initial MVP scope.

## Evidence-first approach

A sustainability figure should not exist without a clear explanation of where it came from.

ARCA is designed around an evidence trail connecting:

- Original source documents
- Extracted information
- Human-reviewed and confirmed values
- Emission factor references
- Calculation results
- Generated reports

This approach is intended to improve transparency, reviewability and confidence in reported information.

## Technology

The application is being developed using:

| Layer | Technology |
|---|---|
| Frontend | React, TypeScript, Vite |
| UI | Tailwind CSS, Radix UI |
| Backend | Python, FastAPI |
| Database | Supabase / PostgreSQL |
| Authentication | Supabase Auth |
| Document processing | PyMuPDF |
| Calculations | Python Decimal arithmetic |
| PDF reporting | ReportLab |

The architecture separates document extraction, user confirmation, calculation logic and report generation.

AI-assisted document processing may support information extraction, but numerical emissions calculations are intended to remain deterministic and independently traceable.

## Development status

**Status: MVP under active development.**

The current development work includes:

- React and TypeScript application
- FastAPI backend foundation
- Supabase database integration structure
- PDF text extraction
- Scope 2 calculation service
- Document verification API integration
- Evidence ledger service
- PDF report generation

The frontend build and initial calculation tests have been executed successfully.

The following work remains before ARCA can be considered ready for real customer use:

- Complete and secure authentication and authorization
- Verify company-level data isolation
- Validate German electricity bill extraction against real document formats
- Independently validate emission factor references and methodology
- Test the complete upload-to-report workflow
- Deploy and validate the application in a production environment

**ARCA is not yet a production-ready sustainability reporting or regulatory compliance platform.**

## Product direction

The initial MVP is deliberately narrow.

The development roadmap is:

- [x] Establish the frontend application structure
- [x] Establish the FastAPI backend foundation
- [x] Implement the initial deterministic Scope 2 calculation service
- [x] Implement initial PDF text extraction
- [x] Establish the evidence ledger and report generation services
- [ ] Complete secure authentication and company-level authorization
- [ ] Improve German electricity bill extraction and validation
- [ ] Complete end-to-end workflow testing
- [ ] Deploy the first usable MVP
- [ ] Validate the workflow with manufacturing businesses

Future expansion will depend on user feedback and validated business requirements.

## Who ARCA is for

ARCA is initially being developed for:

- Small and medium-sized manufacturers
- Industrial suppliers
- Businesses responding to customer sustainability requests
- Companies seeking a more organized approach to electricity-related emissions data

The initial market focus is Germany.

## Project principles

**Evidence over assumptions.** Reported figures should have traceable supporting information.

**Human review matters.** Extracted information should be inspectable and correctable before confirmation.

**Deterministic calculations.** Emissions calculations should be reproducible and transparent.

**Practical before complex.** Start with a useful workflow before expanding into a broad sustainability platform.

---

## Project information

**Product:** ARCA  
**Focus:** Evidence-based sustainability reporting  
**Initial market:** German manufacturing SMEs  
**Initial workflow:** Electricity documents to location-based Scope 2 reporting  
**Development stage:** MVP development

More information, product updates and a hosted application link will be published here as the project progresses.

---

*ARCA — Your sustainability data. Backed by evidence.*
