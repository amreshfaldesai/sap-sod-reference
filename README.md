SAP Segregation of Duties (SoD) — Reference Guide

A free reference guide to common Segregation of Duties (SoD) conflict patterns in SAP ECC & S/4HANA — built from real-world SAP GRC and IT audit experience. 
Use this to spot high-risk access combinations before your next audit, security review, or GRC ruleset build.
If you work in SAP security, internal audit, IT governance, or GRC, this is meant to be a genuinely useful starting reference — not just a teaser.

What is SoD, briefly
Segregation of Duties is a control principle that prevents any single user from having conflicting access — for example, 
the ability to both create a vendor and approve a payment to that vendor. When these conflicts exist unchecked, 
they create fraud and error risk that auditors (internal, external, or SOX) will flag.

Sample Conflict Patterns

Real examples pulled from the full rulesets below — one high-risk conflict per module.

Finance (FI/CO)
  Risk	Conflicting Functions	T-Codes	Risk Level
    Fictitious Vendor + Invoice	Create/Maintain Vendor Master ↔ Post Vendor Invoice	FK01/XK01 ↔ FB60/MIRO	High
    Vendor Bank Details + Payment Run	Maintain Vendor Bank Details ↔ Process Payment Run	FK02/XK02 ↔ F110	High
    Posting Period Control + Journal Posting	Open/Close Posting Periods ↔ Post Journal Entries	OB52 ↔ FB01/F-02	High

Materials Management (MM)
  Risk	Conflicting Functions	T-Codes	Risk Level
    Fictitious Vendor + Purchase Order	Create/Maintain Vendor Master ↔ Create Purchase Order	XK01/FK01 ↔ ME21N	High
    PO Creation + PO Release/Approval	Create Purchase Order ↔ Release/Approve Purchase Order	ME21N ↔ ME28/ME29N	High
    Physical Inventory Count + Adjustment Posting	Enter/Count Physical Inventory ↔ Post Inventory Difference	MI04/MI05 ↔ MI07/MI10	High

Sales & Distribution (SD)
    Risk	Conflicting Functions	T-Codes	Risk Level
    Fictitious Customer + Sales Order	Create/Maintain Customer Master ↔ Create Sales Order	XD01/VD01 ↔ VA01	High
    Delivery Creation + Goods Issue Posting	Create Outbound Delivery ↔ Post Goods Issue	VL01N ↔ VL02N	High
    Sales Order Pricing Override + Billing	Manually Override Order Pricing ↔ Create Billing Document	VA02 ↔ VF01	High

Human Resources (HR/HCM)
    Risk	Conflicting Functions	T-Codes	Risk Level
    Fictitious Employee + Payroll Run	Create/Maintain Employee Master ↔ Execute Payroll Run	PA30/PA40 ↔ PC00_M99_CALC	High
    Employee Bank Details + Payroll Payment	Maintain Employee Bank Details ↔ Execute Payroll Payment Run	PA30 ↔ PC00_M99_CIPE	High
    Payroll Control Record + Payroll Run Execution	Lock/Unlock Payroll Period ↔ Execute Payroll Run	PA03 ↔ PC00_M99_CALC	High

These are samples. Each full ruleset also includes Medium/Low-risk rules, key authorization objects, business rationale, and a suggested mitigating control per rule — plus an Auth Object Glossary tab for quick reference.

Full SAP SoD Rulesets (Paid — ECC & S/4HANA)

Each ruleset is a ready-to-use Excel workbook with a full rule list, an "Applicable to Our Org?" tracking column, an Auth Object Glossary tab, and a Summary tab for reporting risk counts to management or auditors.

Module	Rules	Price	Link
FI/CO	30 pre-built risk rules	$129	amreshfaldesai.gumroad.com/l/sap-fico-sod-ruleset
MM	30 pre-built risk rules	$99	amreshfaldesai.gumroad.com/l/sap-mm-sod-ruleset
SD	30 pre-built risk rules	$99	amreshfaldesai.gumroad.com/l/sap-sd-sod-ruleset
HR/HCM	20 pre-built risk rules	$79	amreshfaldesai.gumroad.com/l/sap-hr-sod-ruleset

Free version (this repo's source guide): amreshfaldesai.gumroad.com/l/sap-sod

Note: these are reference starting points built from common, widely-documented SAP standard transaction codes and authorization objects. They are not a certification, legal advice, or a substitute for a formal SOX/internal audit opinion — validate and customize every rule against your own SAP system. Licensed for single-company internal use; not for resale or redistribution as your own template.

Also relevant: DPDPA Readiness (for teams with Indian users)
If your organization is a foreign SaaS or app company with users in India, you're in scope for India's Digital Personal Data Protection Act (DPDPA) — separate from GDPR/CCPA, with its own consent, notice, and grievance-redressal requirements.
DPDPA Readiness Checklist — a structured checklist to assess your current compliance gap. → amreshfaldesai.gumroad.com/l/dpdpa-readiness-checklist — $79

Other Compliance & Audit Resources
Broader IT audit and governance checklists, built on the same practical, control-level approach:

SAP BTP & Joule Governance Checklist (28 items — cost, access & AI agent controls) — $99
IT General Controls (ITGC) Audit Checklist (102 controls, 8 domains, COBIT-aligned) — $129
Vendor / Third-Party Risk Assessment Checklist (50 controls, full vendor lifecycle) — $119
Business Continuity / Disaster Recovery Plan Checklist (52 controls) — $109
Data Retention & Records Management Policy Checklist (50 controls) — $109

Full catalog: amreshfaldesai.gumroad.com

About

Built from 13+ years of hands-on SAP, ERP audit, and IT governance experience — 
including SAP GRC implementation, SoD ruleset design, and IT compliance leadership roles.
