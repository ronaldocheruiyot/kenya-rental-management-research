# Quick Start Guide - Kenya Rental Management Research

Welcome! This repository contains comprehensive research for building a rental management system for the Kenyan market. Here's how to get started with the three main deliverables.

---

## 📋 What You Have

### ✅ Deliverable 1: Tenancy Agreements Research
**Location**: `/research/tenancy-agreements-analysis.md`

**What's inside**:
- 10 real tenancy agreement examples from Kenya
- Residential: Low-cost (bedsitters KSh 8,000-12,000), Mid-range (1-2BR KSh 20,000-45,000), Premium (2-3BR KSh 65,000+)
- Commercial: Offices, retail shops, warehouses
- Student housing, co-living, serviced apartments, affordable housing
- Detailed analysis of rent, deposits, payment terms, utilities, repairs, termination clauses

**Legal framework covered**:
- Rent Restriction Act (Cap 296) - Controlled residential
- Landlord and Tenant Act (Cap 301) - Commercial
- Data Protection Act 2019 - Tenant data handling
- Distress for Rent Act, Land Act 2012

**How to use it**:
1. Read Executive Summary (page 1-2) for overview
2. Review specific agreement types matching your target market
3. Study Comparative Analysis section for cross-property insights
4. Use System Design Implications section to guide your development

---

### ✅ Deliverable 2: Excel Dataset
**Location**: `/data/` folder

**9 CSV files** representing a complete rental management system:
- `properties.csv` - 3 properties (Nairobi residential, commercial, Mombasa residential)
- `units.csv` - 15 units (bedsitters, 1BR, 2BR apartments, offices)
- `tenants.csv` - 13 tenants (individuals and companies)
- `staff.csv` - 4 staff members (managers, caretaker, accountant)
- `tenancies.csv` - 13 tenancy agreements (active, ended, various terms)
- `charges.csv` - 79 charges (deposits, rent, service charges, penalties)
- `payments.csv` - 65 payments (M-Pesa, bank transfers, various dates)
- `meter_readings.csv` - 60 readings (electricity & water, May-Oct 2026)
- `events.csv` - 42 events (move-ins, maintenance, late payments, inspections)

**How to use it**:

**Option A: Open in Excel/Google Sheets**
1. Open Excel or Google Sheets
2. Import each CSV file as a separate sheet
3. Create a new workbook with 9 sheets named after each file
4. See `/data/README-DATASET.md` for detailed import instructions

**Option B: Use as Database Seed Data**
1. Each CSV becomes a database table
2. Column names are your field names
3. ID columns become primary keys
4. See the README for SQL schema suggestions

**What you can do with it**:
- Calculate total rent collected per month
- Identify tenants in arrears
- Track occupancy rates
- Analyze utility consumption patterns
- See maintenance request trends
- Practice Excel formulas (VLOOKUP, SUMIF, PivotTables)
- Migrate to a database for system development
- Use as test data for your application

**Sample Queries**:
```
Q: Which units are vacant?
A: Filter units.csv where current_status = "Vacant" → U007, U014

Q: How much rent was collected in October 2026?
A: Filter payments.csv where payment_date starts with 2026-10 → Sum amount_paid

Q: Which tenants are behind on rent?
A: Compare total charges vs. total payments per tenancy_id
```

---

### ✅ Deliverable 3: Tenant Management Lifecycle
**Location**: `/research/tenant-management-lifecycle.md`

**What's inside**:
- Complete lifecycle from first enquiry to final deposit refund
- 3 phases broken into 20+ detailed steps
- **Phase 1: Pre-Tenancy** (Enquiry → Lease Signing → Move-In)
- **Phase 2: Active Tenancy** (Invoicing → Payments → Maintenance → Renewals)
- **Phase 3: Post-Tenancy** (Notice → Move-Out → Settlement → Refund)

**For each step, you get**:
- Who is involved
- Actions taken
- Records created
- System features needed
- What can go wrong
- Automation opportunities
- Typical timelines

**Key sections**:
- **Automation Priority Matrix**: What to automate first (M-Pesa integration = highest ROI)
- **Workflow Metrics & KPIs**: How to measure success
- **Legal Considerations**: Compliance requirements at each stage
- **Dispute Prevention**: How to avoid common conflicts

**How to use it**:
1. Read the Overview to understand the 3 phases
2. Study each step in detail as you design that feature
3. Use automation opportunities to prioritize development
4. Reference legal considerations for compliance
5. Build system features based on "System Features" listed for each step

**Example workflow design**:
```
Step 2.2: Monthly Rent Invoicing
↓
System features needed:
- Auto-generate invoices 3 days before due date
- Send via SMS/email/portal
- Include payment link (M-Pesa STK push)
- Track delivery confirmation
↓
Step 2.3: Rent Payment & Reconciliation
↓
Automation opportunity (highest value):
- M-Pesa API integration
- Auto-match payment to invoice
- Send receipt via SMS within 30 seconds
- Update ledger automatically
```

---

## 🎯 How to Use These Deliverables Together

### Week 1: Understanding the Domain
1. Read the **Tenancy Agreements Analysis** to understand what landlords and tenants agree on
2. Open the **Excel Dataset** and explore the relationships between tables
3. Skim the **Lifecycle Documentation** to see the big picture workflow

### Week 2: Deep Dive into Data
1. Import all CSV files into Excel
2. Practice creating reports:
   - Rent roll (property → units → tenants → rent amounts)
   - Arrears report (charges - payments by tenant)
   - Occupancy report (occupied units / total units)
3. Try VLOOKUP formulas to link data across sheets
4. Create a PivotTable to summarize rent by property

### Week 3: Workflow Design
1. Pick one phase from the Lifecycle doc (e.g., Active Tenancy)
2. Map out each step on a whiteboard or flowchart tool
3. Identify which steps you'll automate vs. manual
4. Design your first feature (e.g., automated invoicing)

### Week 4: System Architecture
1. Use the dataset structure as your database schema
2. Sketch your database tables based on the CSV files
3. Define relationships (foreign keys)
4. Plan your APIs (e.g., POST /payments, GET /tenancies/:id)

### Then: Build!
- Start with highest-impact automation (M-Pesa payment reconciliation)
- Build features following the lifecycle sequence
- Test with the sample data in the dataset
- Iterate based on user feedback

---

## 🔍 Quick Navigation

**Want to understand...**
- **Legal requirements?** → Read `/research/tenancy-agreements-analysis.md` section "Legal Framework Overview"
- **Data structure?** → Open `/data/README-DATASET.md` and see the relationship diagrams
- **Payment workflow?** → Read `/research/tenant-management-lifecycle.md` Steps 2.2-2.4
- **Deposit refund process?** → Read lifecycle Steps 3.3-3.5
- **What to build first?** → See lifecycle "Automation Priority Matrix"

**Want to analyze...**
- **Current occupancy?** → Filter `units.csv` by `current_status`
- **Payment trends?** → Open `payments.csv` and group by `payment_date` month
- **Maintenance issues?** → Filter `events.csv` where `event_type = "Maintenance Request"`
- **Arrears situations?** → Compare totals in `charges.csv` vs. `payments.csv` per `tenancy_id`

---

## 💡 Pro Tips

1. **Start with the lifecycle doc** - It's the blueprint for your system workflow
2. **The dataset is your test data** - Import it into your database once you build it
3. **Read case law in the agreements doc** - Real Kenyan court cases show what disputes look like
4. **M-Pesa integration is critical** - 80%+ of residential rent is paid via M-Pesa in Kenya
5. **Joint inspections prevent 95% of deposit disputes** - Make this feature mandatory in your system
6. **Data Protection Act compliance is not optional** - Budget for encryption, consent tracking, retention policies

---

## 📞 Next Steps

You now have everything you need to:
1. ✅ Understand Kenyan tenancy agreements (10 real examples)
2. ✅ See what data a rental system needs (9 linked tables)
3. ✅ Know every workflow step from enquiry to deposit refund (20+ steps mapped)

**Recommended Action Plan**:
1. Review all three deliverables (allocate 1 week)
2. Discuss findings with your team
3. Design your system architecture
4. Prioritize features (use automation priority matrix)
5. Start development (begin with M-Pesa integration + invoicing)

---

**Questions?** Review the detailed notes in each deliverable document.

**Ready to build?** Start with `/research/tenant-management-lifecycle.md` and pick your first workflow to implement.

Good luck building an excellent rental management system for Kenya! 🚀🇰🇪
