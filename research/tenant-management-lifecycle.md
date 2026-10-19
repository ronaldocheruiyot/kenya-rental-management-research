# Tenant and Management Lifecycle Documentation

**Purpose**: Map every step in the tenant journey and management workflow to identify automation opportunities and system requirements

---

## Overview

The rental property lifecycle can be divided into three major phases:
1. **Pre-Tenancy**: Enquiry to lease signing
2. **Active Tenancy**: Move-in to notice of termination
3. **Post-Tenancy**: Notice given to final settlement

Each phase involves multiple steps, creates specific records, and requires coordination between landlord/manager, tenant, and sometimes third parties (banks, utilities, tribunals).

---

## PHASE 1: PRE-TENANCY (Enquiry to Lease Signing)

### Step 1.1: Property Listing & Marketing

**Who**: Landlord/Property Manager  
**Action**:
- List vacant unit with details: location, size, rent, deposit, amenities
- Upload photos and property description
- Set availability date
- Define tenant requirements (income level, references, etc.)

**Records Created**:
- Property listing (unit ID, rent, availability date)
- Marketing materials (photos, descriptions)

**System Features**:
- Property/unit management module
- Vacancy tracking
- Photo/document storage
- Listing generation for websites/social media

**What Can Go Wrong**:
- Inaccurate property description leads to unsuitable enquiries
- Photos don't match reality, causing tenant disappointment at viewing
- Rent listed doesn't match what landlord actually charges

**Automation Opportunity**: 
- Auto-generate listings from property database
- Track listing performance (views, enquiries)
- Sync availability across multiple platforms

---

### Step 1.2: Tenant Enquiry

**Who**: Prospective Tenant  
**Action**:
- Contact landlord/manager via phone, email, WhatsApp, or in person
- Ask about property details, viewing availability
- Provide basic information (name, contact, move-in date)

**Records Created**:
- Enquiry record (name, contact, date, property of interest, source)
- Communication log

**System Features**:
- Enquiry capture form (web, SMS, WhatsApp integration)
- Lead management system
- Automated responses with property details
- Viewing scheduler

**What Can Go Wrong**:
- Enquiries not captured or followed up
- Double-booking viewings
- Losing contact with interested tenant

**Automation Opportunity**:
- Auto-respond with property details and viewing times
- SMS/email confirmation of viewing appointment
- Reminder sent day before viewing

---

### Step 1.3: Property Viewing

**Who**: Landlord/Manager + Prospective Tenant  
**Action**:
- Schedule viewing appointment
- Conduct property tour
- Explain terms (rent, deposit, rules)
- Answer tenant questions
- Assess tenant suitability

**Records Created**:
- Viewing record (date, time, attendees, outcome)
- Initial tenant assessment notes

**System Features**:
- Viewing calendar with booking
- Mobile app for caretaker/agent to record viewing outcome
- Photo evidence of property condition at viewing date

**What Can Go Wrong**:
- Property not ready for viewing (dirty, occupied)
- No-show by tenant or agent
- Tenant interested but manager forgets to follow up

**Automation Opportunity**:
- Calendar reminders to both parties
- No-show tracking (if tenant repeatedly doesn't show, deprioritize)
- Follow-up automated 24 hours after viewing: "Are you interested?"

---

### Step 1.4: Tenant Application & Vetting

**Who**: Prospective Tenant submits; Landlord/Manager reviews  
**Action (Tenant)**:
- Complete application form
- Provide: ID/passport copy, employment letter or business registration, payslips (last 3 months), bank statement, previous landlord reference
- Pay application fee (if applicable, typically KSh 500-1,000)

**Action (Landlord/Manager)**:
- Review application completeness
- Verify employment (call employer)
- Contact previous landlord for reference
- Check credit history (if using credit bureau)
- Assess income vs. rent ratio (typically rent should not exceed 1/3 of income)
- Run background check (optional: check for court cases, criminal record via eCitizen)
- Approve or reject application

**Records Created**:
- Tenant application (all submitted documents)
- Verification records (employment confirmed, reference notes, credit report)
- Approval/rejection decision with reasons

**Data Protection Note**: 
- This creates extensive personal data subject to Data Protection Act
- Must obtain consent for processing, storage, third-party verification
- Rejected applications: retain 6 months then delete/anonymize (not 6 years; that's for actual tenancies)

**System Features**:
- Online application form with document upload
- Vetting checklist and status tracking
- Integration with credit bureaus (e.g., Metropol, CRB Africa)
- Reference contact log
- Decision workflow (approve/reject + reason + notify tenant)

**What Can Go Wrong**:
- Incomplete applications waste time
- Landlord accepts risky tenant (no verification) leading to future arrears
- Verification takes too long, good tenant goes elsewhere
- Discrimination in tenant selection (illegal; must document objective criteria)

**Automation Opportunity**:
- Auto-check application completeness before submission allowed
- Email/SMS verification requests to employer and previous landlord
- Credit bureau API integration for instant report
- Automated approval for tenants meeting criteria (e.g., income 3x rent, good credit, positive reference)
- Auto-notify tenant of decision within 24-48 hours

**Typical Timeline**: 2-5 days from application to decision

---

### Step 1.5: Lease Agreement Preparation

**Who**: Landlord/Manager  
**Action**:
- Select appropriate agreement template (controlled residential, commercial, etc.)
- Fill in specifics: parties' names, ID numbers, property address, rent, deposit, dates, payment method
- Customize special clauses if needed
- Review for legal compliance (Cap 296, Cap 301, Data Protection Act)
- Send draft to tenant for review

**Records Created**:
- Draft lease agreement
- Tenant review acknowledgment

**System Features**:
- Agreement template library (by property type, legal framework)
- Auto-fill from tenant application and property database
- Legal compliance checker (e.g., flag if advance rent >2 months on Cap 296 tenancy)
- Electronic signature integration
- Version control (if agreement amended)

**What Can Go Wrong**:
- Wrong template used (e.g., uncontrolled template for controlled tenancy)
- Non-compliant clauses (e.g., waiver of statutory rights in Cap 301 tenancy)
- Incorrect details (wrong rent amount, wrong unit number)
- Tenant doesn't understand terms but signs anyway

**Automation Opportunity**:
- Template auto-selected based on property type and legal classification
- All fields auto-populated from database
- Plain-language summary generated alongside legal agreement
- Tenant can review online and request clarifications before signing

**Typical Timeline**: 1-2 days to prepare and send to tenant

---

### Step 1.6: Deposit & First Rent Payment

**Who**: Tenant pays; Landlord receives  
**Action (Tenant)**:
- Pay security deposit (1-3 months' rent depending on property type)
- Pay first month's rent (or pro-rata if moving mid-month)
- Obtain receipt for both payments

**Action (Landlord/Manager)**:
- Receive and confirm payment (M-Pesa, bank transfer, or rarely cash)
- Issue official receipts (numbered, dated, sequenced for KRA compliance)
- Allocate payment: separate deposit (held in trust) from rent (income)

**Records Created**:
- Payment records (date, amount, method, reference number)
- Receipt copies
- Deposit held record (separate accounting from rent)

**System Features**:
- M-Pesa STK Push for instant collection
- Bank account reconciliation
- Automated receipt generation and SMS/email delivery
- Deposit liability tracking (deposit is owed back to tenant, not income)
- KRA-compliant receipt numbering

**What Can Go Wrong**:
- Payment made but not confirmed (M-Pesa sometimes delays)
- Receipt not issued (tenant has no proof of payment)
- Deposit and rent not separated in accounting (tax compliance issue)
- Overpayment or underpayment not caught

**Automation Opportunity**:
- M-Pesa API auto-confirms payment within seconds
- Receipt auto-generated and sent via SMS
- Payment shortfall flagged before lease signing
- Deposit held in separate ledger automatically

**Typical Timeline**: Same day or within 24 hours of lease signing

---

### Step 1.7: Lease Signing

**Who**: Landlord/Manager + Tenant (+ Witness if required)  
**Action**:
- Both parties meet to sign agreement
- Read through key clauses together (rent, deposit, notice period, termination, repairs)
- Tenant asks final questions
- Sign and date agreement (usually 2 copies: 1 for landlord, 1 for tenant)
- Witness signs (optional but common practice)
- Exchange copies

**Records Created**:
- Fully executed lease agreement (signed by both parties)
- Witness attestation

**System Features**:
- Electronic signature (e.g., DocuSign, local e-signature platform)
- PDF generation of final signed agreement
- Automatic storage in tenant file
- Counter-signature tracking (if signed at different times)

**What Can Go Wrong**:
- One party signs, other doesn't (incomplete agreement)
- Tenant signs without reading (later disputes over terms)
- No witness (weakens evidence if dispute arises)
- One party doesn't receive their copy

**Automation Opportunity**:
- E-signature with timestamp and IP log
- Both parties must initial every page electronically
- Auto-send final copy to both parties via email
- Store in encrypted cloud with access for both parties anytime

**Typical Timeline**: Same day as payment confirmation

---

### Step 1.8: Move-In Inspection

**Who**: Landlord/Manager + Tenant (+ Caretaker if present)  
**Action**:
- Walk through property together before tenant moves belongings
- Document condition of every room, fixture, appliance
- Take photos/video of property condition
- Note any existing damage, wear, defects (landlord cannot later claim tenant caused pre-existing damage)
- Test all appliances (if furnished)
- Record meter readings (electricity, water if metered)
- Both parties sign inspection report acknowledging condition

**Records Created**:
- Move-in inspection report (detailed, room-by-room)
- Photos/video (timestamped)
- Meter readings (start of tenancy)

**System Features**:
- Mobile inspection app with checklist
- Photo/video upload directly to tenant file
- Pre-populated checklist by property type (e.g., furnished apartment has appliance checks)
- E-signature on inspection report
- Meter reading capture

**What Can Go Wrong**:
- No inspection done (biggest mistake! Makes deposit disputes nearly impossible to resolve)
- Inspection done but not documented in writing
- Photos taken but not shared with tenant
- Tenant moves in before inspection (can't prove pre-existing damage)

**Automation Opportunity**:
- Inspection app guides through every room/fixture
- Photo upload required before completing inspection
- Tenant receives copy immediately via email/SMS
- Meter readings auto-logged as baseline for future billing

**Typical Timeline**: Same day as lease signing or day before move-in

**CRITICAL SUCCESS FACTOR**: This step prevents 80%+ of deposit refund disputes. System must make it impossible to skip.

---

## PHASE 2: ACTIVE TENANCY (Move-In to Notice Given)

### Step 2.1: Tenant Move-In

**Who**: Tenant  
**Action**:
- Receive keys and access cards/fobs
- Move belongings into unit
- Set up utilities (if not included)
- Register with caretaker/security (if applicable)

**Records Created**:
- Key handover log (number of keys issued, date)
- Tenant contact details confirmed
- Emergency contact recorded

**System Features**:
- Key register (tracking which keys issued to which tenant)
- Tenant portal access setup (username, password)
- Welcome email/SMS with important info (caretaker contact, garbage days, rules)

**What Can Go Wrong**:
- Tenant given wrong keys or not enough keys
- Security/caretaker not informed tenant moved in
- Utilities not set up, tenant has no water/electricity

**Automation Opportunity**:
- Auto-generate welcome pack (PDF with property rules, contacts, payment info)
- Tenant portal login credentials auto-sent
- Alert caretaker/security "New tenant in Unit X as of [date]"

---

### Step 2.2: Monthly Rent Invoicing

**Who**: Landlord/Manager generates; Tenant receives  
**Action (Landlord/Manager)**:
- Generate invoice for rent + any recurring charges (service charge, utilities if flat rate)
- Calculate any penalties from previous month (if rent was late)
- Send invoice 3-5 days before due date via SMS, email, tenant portal
- Include: amount due, due date, payment methods, late penalty terms

**Action (Tenant)**:
- Receive invoice
- Make payment by due date via M-Pesa, bank transfer, or cash

**Records Created**:
- Invoice (date generated, due date, amount, charges breakdown)
- Invoice delivery confirmation

**System Features**:
- Automated invoice generation based on tenancy terms
- Multi-channel delivery (SMS, email, push notification, portal)
- Payment link embedded in invoice (M-Pesa STK push, bank details)
- Invoice history accessible to tenant anytime

**What Can Go Wrong**:
- Invoice not sent or sent too late (tenant didn't know payment due)
- Incorrect amount on invoice (e.g., doesn't include service charge)
- Tenant receives invoice but ignores it
- Payment methods not clearly stated

**Automation Opportunity**:
- Invoices auto-generated on specified day each month (e.g., 3 days before due date)
- Recurring charges auto-included based on tenancy record
- Tenant can set up autopay (standing order or M-Pesa standing instruction)
- SMS reminder 1 day before due date

**Typical Timeline**: Invoice sent 3-5 days before rent due date (most common due date: 1st or 5th of month)

---

### Step 2.3: Rent Payment & Reconciliation

**Who**: Tenant pays; Landlord/Manager receives and allocates  
**Action (Tenant)**:
- Make payment via M-Pesa (most common for residential), bank transfer (commercial), or cash (rare, discouraged)
- Obtain confirmation (M-Pesa message, bank receipt)
- Expect receipt from landlord

**Action (Landlord/Manager)**:
- Receive payment notification
- Match payment to invoice and tenant
- Allocate payment (if partial, allocate to oldest debt first)
- Update tenant ledger
- Issue official receipt
- If full payment: mark invoice paid
- If partial payment: mark partially paid, outstanding balance carried forward
- If late payment: calculate penalty based on agreement terms

**Records Created**:
- Payment record (date received, amount, method, reference, payer details)
- Receipt (numbered, KRA-compliant)
- Tenant ledger entry (running balance)
- Late payment penalty record (if applicable)

**System Features**:
- M-Pesa API integration (payments auto-posted within seconds)
- Bank account reconciliation (import statements, match to tenants)
- Automated receipt generation and delivery (SMS, email)
- Payment allocation logic (apply to oldest invoice first, or split per agreement)
- Ledger auto-updates
- Penalty auto-calculation if payment late

**What Can Go Wrong**:
- Payment received but not matched to correct tenant (especially with M-Pesa if tenant uses different name)
- Partial payment not properly recorded (tenant thinks they paid full, landlord disagrees)
- Receipt not issued (tenant has no proof)
- Late penalty miscalculated
- Payment sits unreconciled for days/weeks (tenant thinks paid, landlord thinks unpaid)

**Automation Opportunity** (HIGHEST VALUE):
- M-Pesa integration: payment received → auto-matched to tenant → receipt sent → ledger updated → invoice marked paid (ALL INSTANT)
- Bank reconciliation: import statement → flag matching payments → suggest allocation → one-click confirm
- Unmatched payments flagged for manual review
- Tenant gets SMS receipt within 30 seconds of payment

**Typical Timeline**: Same day (instant with M-Pesa integration)

---

### Step 2.4: Arrears Management

**Who**: Landlord/Manager (proactive); Tenant (reactive)  
**Action (Landlord/Manager)**:
- Monitor rent payments daily
- Identify late/non-payments within 1-2 days of due date
- Send reminders escalating in tone:
  - Day 1 late: Friendly reminder (may be oversight)
  - Day 3-5 late: Firmer reminder + late penalty notice
  - Day 10-14 late: Warning letter + intent to escalate
  - Day 30+ late: Formal notice under tenancy agreement and Cap 296/301 (prelim to termination/tribunal)
- Attempt phone contact
- Understand reason for non-payment (financial hardship, dispute, oversight)
- Negotiate payment plan if appropriate
- Document all communication

**Action (Tenant)**:
- Respond to reminders
- Explain reason for delay if applicable
- Arrange payment or request payment plan

**Records Created**:
- Arrears aging report (all tenants with outstanding balances)
- Reminder messages sent (SMS, email log)
- Call log (if phone contact made)
- Payment plan agreement (if negotiated)
- Formal notices (if escalated)

**System Features**:
- Arrears dashboard (all late-paying tenants, days overdue, amount)
- Automated reminder workflows (escalating messages)
- SMS/email templates for each stage
- Call log integrated with tenant record
- Payment plan module (installment schedule, track compliance)
- Alert landlord if tenant reaches critical arrears level (e.g., 30 days = grounds for termination)

**What Can Go Wrong**:
- No arrears tracking = landlord realizes too late (tenant owes 3+ months)
- Inconsistent follow-up (some tenants reminded, others not)
- Overly aggressive collection tactics (illegal harassment)
- Accepting late payment repeatedly without consequences (tenant learns it's okay to pay late)
- Not documenting attempts to collect (weakens tribunal case)

**Automation Opportunity**:
- Auto-detect late payment on day 1
- Send first reminder automatically (SMS: "Hi [Name], friendly reminder your rent of KSh [X] was due on [date]. Please pay today to avoid late fee of KSh [Y] tomorrow.")
- Escalating reminders auto-sent at day 3, 7, 14, 30
- Landlord dashboard shows all arrears, color-coded by severity
- One-click call logging
- Payment plan generator with installment schedule

**Legal Considerations**:
- Cap 296 (controlled residential): Landlord can only terminate after proper notice and tribunal approval; cannot forcibly evict
- Cap 301 (commercial): Similar protections; Business Premises Tribunal procedures required
- Distress for Rent Act: Landlord may levy distress (seize goods) but only via court process; illegal to do so without order
- Harassment: Landlord cannot cut utilities, change locks, or threaten tenant illegally (criminal offense)

**Typical Timeline**: 
- Gentle phase: Days 1-14
- Serious phase: Days 15-30
- Legal phase: Day 30+ (formal notice, tribunal filing)

---

### Step 2.5: Maintenance Requests & Repairs

**Who**: Tenant requests; Landlord/Manager responds  
**Action (Tenant)**:
- Notice defect or damage (e.g., leaking pipe, broken lock, electrical fault)
- Report to landlord/manager via phone, SMS, WhatsApp, portal, or in person
- Describe issue and urgency

**Action (Landlord/Manager)**:
- Receive request
- Assess urgency (emergency = same day; non-emergency = within 7-14 days)
- Determine responsibility (landlord or tenant per agreement)
- Arrange repair:
  - If landlord's responsibility: schedule contractor/artisan, notify tenant of visit
  - If tenant's responsibility: inform tenant they must arrange and pay
  - If emergency (e.g., burst pipe flooding unit): immediate response regardless of time
- Conduct repair
- Confirm with tenant that issue resolved
- Document cost (for landlord's records or to bill tenant if their fault)

**Records Created**:
- Maintenance request (date, description, urgency, reported by)
- Responsibility determination (landlord or tenant)
- Work order (assigned to contractor, scheduled date)
- Completion confirmation
- Cost record (receipt, invoice)
- Photos (before/after if significant work)

**System Features**:
- Tenant portal: submit maintenance request with photo
- Request tracking (status: received → assessed → scheduled → in progress → completed)
- Contractor dispatch (assign work order to preferred vendor)
- Tenant notification (SMS: "Plumber will visit on [date] at [time]")
- SLA tracking (was repair done within agreed time?)
- Cost categorization (type of repair, property, cost)
- Tenant satisfaction rating (after completion)

**What Can Go Wrong**:
- Request not logged (tenant calls, manager forgets)
- Slow response (tenant waits weeks for urgent repair)
- Dispute over responsibility (landlord says tenant caused damage; tenant disagrees)
- Repair done poorly or incomplete
- Tenant not home when contractor arrives (wasted trip)
- Cost dispute (tenant says they shouldn't pay; landlord disagrees)

**Automation Opportunity**:
- Tenant submits request via app (with photo proving issue)
- System auto-tags as emergency/non-emergency based on keywords (flood, fire, electricity = emergency)
- Auto-assign to landlord or tenant responsibility based on issue type
- Auto-schedule with contractor and send appointment SMS to tenant
- Auto-follow-up: "Was this issue resolved?" 24 hours after completion
- Cost auto-logged against property maintenance budget

**Typical Timeline**:
- Emergency: Same day (within hours)
- Urgent (e.g., no hot water, toilet not flushing): 1-3 days
- Non-urgent (e.g., cabinet door loose): 7-14 days

**Legal Obligation**:
- Landlord must maintain structural integrity (walls, roof, plumbing, wiring) under most tenancy agreements and general law
- Failure to do timely repairs may entitle tenant to withhold rent or terminate lease (depending on severity)

---

### Step 2.6: Utility Billing (if Landlord Handles)

**Who**: Landlord/Manager calculates and bills; Tenant pays  
**Action (Landlord/Manager)**:
- Read meters monthly (electricity, water) on specified date
- Calculate consumption: (current reading - previous reading) × rate
- Add to tenant invoice as separate line item
- Some properties: landlord pays utility provider, then bills tenant (mark-up sometimes applied)

**Action (Tenant)**:
- Review utility charge on invoice
- Pay along with rent

**Records Created**:
- Meter readings (date, reading, unit, photo of meter if disputed)
- Consumption calculation
- Utility charge per tenant

**System Features**:
- Meter reading entry (mobile app: caretaker enters reading on-site)
- Photo capture of meter reading (evidence)
- Auto-calculate consumption
- Flag unusual consumption (e.g., 10x normal = possible leak or meter error)
- Utility billing on same invoice as rent
- Meter reading history graph (tenant can see their usage trend)

**What Can Go Wrong**:
- Meter not read monthly (estimated bills often inaccurate)
- Reading error (typo: 1234 entered as 12340)
- Meter faulty (shows much higher than actual usage)
- Shared meter (multiple units on one meter = dispute over allocation)
- Tenant disputes charge (no proof of reading)

**Automation Opportunity**:
- Caretaker app with meter reading checklist (must visit every unit monthly)
- Photo required for every reading (proves actual reading)
- System flags unusual consumption for landlord to investigate
- Tenant can see meter reading history anytime (transparency)
- If prepaid electricity: no billing needed; tenant buys tokens directly

**Typical Timeline**: Readings taken last 3 days of month; charges on next month's invoice

**Trend**: Prepaid electricity meters eliminate billing disputes and non-payment risk; increasingly common in Kenya.

---

### Step 2.7: Rent Increases (Annual or Periodic)

**Who**: Landlord initiates; Tenant receives notice  
**Action (Landlord/Manager)**:
- Determine new rent amount (per escalation clause in agreement, or market rate for uncontrolled tenancies)
- Prepare written notice of increase
- Serve notice to tenant (hand delivery, email, registered post, SMS) with required advance notice:
  - Cap 296 controlled: Specific procedures and tribunal approval required
  - Cap 301 commercial: Per agreement, typically 30-90 days' notice
  - Uncontrolled residential: Per agreement, typically 60-90 days' notice
- Document service of notice

**Action (Tenant)**:
- Receive notice
- Decide: accept increase, negotiate, or give notice to vacate
- If disputes increase (controlled tenancy): can challenge at tribunal

**Records Created**:
- Rent increase notice (dated, served, new amount, effective date)
- Proof of service
- Tenant response (acceptance or notice to vacate)
- Updated tenancy record with new rent amount

**System Features**:
- Rent review calendar (flags leases due for review based on annual anniversary)
- Increase calculator (suggests increase per agreement formula, e.g., 5% or CPI)
- Notice generator and delivery tracking
- Escalation workflow if tenant disputes
- Tenant response tracking
- Auto-update rent amount in system after notice period expires

**What Can Go Wrong**:
- Increase not legally permitted (Cap 296 controlled without tribunal approval)
- Notice too short (violates agreement or statute)
- No written notice (tenant claims they never knew)
- Excessive increase (tenant vacates, unit sits vacant)

**Automation Opportunity**:
- System flags leases due for review 120 days before anniversary
- Suggests increase amount based on agreement terms
- Auto-generates compliant notice
- Tracks delivery and tenant response
- Updates rent automatically after notice period if tenant doesn't object

**Typical Timeline**: Notice given 60-90 days before effective date; increase takes effect on next rent due date after notice period

---

### Step 2.8: Lease Renewal

**Who**: Either party initiates; both agree  
**Action (Landlord/Manager)**:
- Track lease expiry date (60-90 days before)
- Decide: offer renewal, end tenancy, or let it auto-renew (if month-to-month)
- If offering renewal: prepare new lease or renewal addendum
- May include rent increase at this point

**Action (Tenant)**:
- Decide: renew, negotiate terms, or give notice to vacate
- Sign renewal if agreeable

**Records Created**:
- Renewal offer/intent
- New lease agreement or renewal addendum
- Updated lease dates in system

**System Features**:
- Lease expiry calendar with alerts 90/60/30 days before
- Renewal workflow (offer → tenant decision → new agreement)
- Integration with lease signing process
- Historical lease version tracking

**What Can Go Wrong**:
- Lease expires, no renewal discussed (uncertainty for both parties)
- Tenant assumes auto-renewal; landlord assumes they're leaving (miscommunication)
- New agreement not signed (tenant becomes holdover tenant with unclear status)

**Automation Opportunity**:
- Auto-alert landlord 90 days before expiry: "Lease for Tenant X expires on [date]. Offer renewal?"
- Send renewal offer via tenant portal
- Tenant accepts online → e-signature flow starts
- If no response by 30 days before expiry: escalate to manager

**Typical Timeline**: Discuss renewal 60-90 days before expiry; finalize 30 days before expiry

---

### Step 2.9: Tenant Communication & Notices

**Who**: Both parties (ongoing throughout tenancy)  
**Action**:
- General notices (e.g., building maintenance, water shutoff, rent due reminders)
- Complaints (noise, parking, rule violations)
- Requests (permission to sublet, bring pet, alter premises)
- Policy changes (new house rules, gate access hours)

**Records Created**:
- Communication log (all emails, SMS, letters, WhatsApp messages)
- Complaint records
- Permission requests and approvals/denials

**System Features**:
- Messaging center (both parties can send/receive messages; all logged)
- Broadcast messaging (landlord to all tenants, e.g., "Water off tomorrow 9 AM - 12 PM")
- Read receipts
- Archive of all communication (searchable)

**What Can Go Wrong**:
- Verbal agreements not documented (he-said-she-said disputes)
- Important notice not received (tenant claims they didn't know)
- No record of complaints (can't prove pattern of issues)

**Automation Opportunity**:
- All communication via portal/SMS/email (auto-logged)
- Tenant must acknowledge receipt of important notices
- Search communication history anytime
- Templates for common notices (water shutoff, rent reminder, etc.)

---

## PHASE 3: POST-TENANCY (Notice to Final Settlement)

### Step 3.1: Notice of Termination

**Who**: Either party gives notice  
**Action (Tenant)** (if tenant initiates):
- Decide to vacate (new job, buying house, moving cities, dissatisfaction, etc.)
- Prepare written notice per agreement terms (1-3 months' notice typical)
- Serve notice to landlord (email, hand delivery, registered post)
- State intended move-out date (must be at least notice period away)

**Action (Landlord/Manager)** (if landlord initiates):
- Determine grounds for termination (end of lease, arrears, breach, need property for own use)
- Check legal requirements:
  - Cap 296 controlled residential: Limited grounds; tribunal procedures required
  - Cap 301 commercial: Controlled tenancies have statutory protections
  - Uncontrolled: Per agreement terms, but must be reasonable
- Prepare notice in required format (prescribed forms for Cap 296/301)
- Serve notice with required advance time
- Document service

**Records Created**:
- Termination notice (date given, date to vacate, reason, signature)
- Proof of service (delivery confirmation, registered post receipt)
- Updated tenancy status (notice period active)

**System Features**:
- Notice generator (templates for tenant-initiated and landlord-initiated)
- Legal compliance checker (ensures correct grounds, format, notice period)
- Delivery tracking
- Countdown calendar (days until move-out)
- Alert property manager: "Unit [X] will be vacant on [date]; prepare for new listing"

**What Can Go Wrong**:
- Notice too short (violates agreement; invalid notice)
- No written notice (tenant verbally says they're leaving but doesn't put in writing)
- Notice served improperly (e.g., SMS for Cap 301 tenancy requiring written notice)
- Landlord terminates controlled tenancy without legal grounds or tribunal approval (tenant can challenge)
- Tenant leaves without notice (abandons property; owes rent for notice period)

**Automation Opportunity**:
- Tenant can submit notice via portal (auto-calculates move-out date based on required notice period)
- Landlord receives alert immediately
- System blocks invalid notices (e.g., "You must give 60 days' notice; your requested move-out date is only 30 days away")
- Countdown to move-out date visible to both parties
- Triggers pre-move-out workflow (inspection scheduling, deposit calculation)

**Legal Requirements**:
- Notice must be in writing (verbal notice generally not binding)
- Cap 296/301 tenancies have specific notice formats and procedures
- Tenant must pay rent for entire notice period even if vacates early (unless landlord finds replacement tenant)

**Typical Timeline**: Notice given 30-90 days before intended move-out (depends on agreement)

---

### Step 3.2: Pre-Move-Out Arrangements

**Who**: Landlord/Manager + Tenant  
**Action**:
- Schedule move-out inspection date (typically same day as tenant vacates)
- Provide tenant with move-out checklist (what must be done before inspection):
  - All rent paid current
  - All utilities paid current
  - Property cleaned (floors, walls, bathroom, kitchen)
  - All personal belongings removed
  - Keys and access cards ready to return
  - Repair any tenant-caused damage (or it will be deducted from deposit)
- Arrange utility disconnection or transfer (if in tenant's name)
- Final meter readings scheduled

**Records Created**:
- Move-out checklist (shared with tenant)
- Inspection appointment

**System Features**:
- Automated move-out checklist sent to tenant
- Inspection scheduler
- Pre-move-out reminders (7 days before, 3 days before, 1 day before)

**What Can Go Wrong**:
- Tenant doesn't clean property (deposit deduction or dispute)
- Utilities not settled (tenant leaves owing electricity/water)
- No inspection scheduled (tenant drops keys and leaves; landlord can't do joint inspection)

**Automation Opportunity**:
- System auto-sends move-out checklist when notice received
- Tenant can book inspection time via portal
- Reminders auto-sent
- Final bills (utilities) auto-generated

---

### Step 3.3: Move-Out Inspection

**Who**: Landlord/Manager + Tenant (+ Caretaker/Witness)  
**Action**:
- Both parties walk through property on move-out date
- Compare current condition to move-in inspection report
- Identify any damage beyond fair wear and tear
- Take photos/video of current condition
- Document deficiencies (e.g., broken window, holes in wall, missing appliances, extreme dirt)
- Estimate repair costs for tenant-caused damage
- Take final meter readings (electricity, water)
- Tenant returns all keys and access cards
- Both parties sign move-out inspection report
- Landlord provides preliminary deposit refund calculation (deposit minus deductions if any)

**Records Created**:
- Move-out inspection report (detailed, room-by-room, compared to move-in)
- Photos/video (timestamped)
- Final meter readings
- Key return log (all keys accounted for)
- Preliminary deposit deduction worksheet

**System Features**:
- Mobile inspection app (side-by-side comparison with move-in inspection)
- Photo upload (before/after comparison)
- Damage assessment with cost estimation (database of typical repair costs)
- Key return tracking
- E-signature on move-out report
- Instant preview of deposit refund (calculated automatically based on deductions)

**What Can Go Wrong** (MOST CRITICAL STEP):
- No joint inspection (tenant and landlord not present together)
- Inspection done but not documented
- Disagreement over damage (tenant says it was pre-existing; landlord says tenant caused it) → **move-in photos are proof**
- Tenant refuses to sign inspection report
- Keys not all returned (landlord must change locks, charges tenant)

**Automation Opportunity**:
- Inspection must be completed before tenant's portal access disabled (enforces compliance)
- Side-by-side photo comparison (move-in vs. move-out)
- Damage photos auto-tagged with cost estimate from repair cost database
- Tenant sees preliminary deduction calculation in real-time
- Both parties e-sign report on-site (no delays)
- If disagreement: flag for dispute resolution

**CRITICAL SUCCESS FACTOR**: Joint inspection with photos and signed report prevents 95%+ of deposit refund litigation.

---

### Step 3.4: Final Accounting & Settlement

**Who**: Landlord/Manager calculates; Tenant reviews  
**Action (Landlord/Manager)**:
- Calculate final amounts:
  - **Owed to tenant**: Security deposit held
  - **Owed by tenant**: 
    - Unpaid rent (including pro-rata for final month if applicable)
    - Unpaid utilities (electricity, water final bills)
    - Damage repairs (per move-out inspection)
    - Cleaning costs (if property left excessively dirty)
    - Lost keys/access cards replacement
    - Any other charges per agreement
  - **Net amount**: Deposit minus all deductions = refund to tenant (or tenant owes balance)
- Prepare itemized settlement statement
- Send to tenant for review
- Address any tenant disputes over deductions
- If agreement: process refund (or collect balance if tenant owes)

**Action (Tenant)**:
- Review settlement statement
- Challenge any unfair deductions (with evidence)
- Agree to final amount
- Receive refund (or pay balance)

**Records Created**:
- Final settlement statement (itemized: deposit, deductions, refund/balance)
- Supporting documents (repair invoices, utility bills, cleaning receipt)
- Tenant acknowledgment of settlement
- Refund payment record

**System Features**:
- Auto-calculate settlement from tenancy ledger + inspection deductions
- Itemized statement generator (PDF)
- Tenant can view and approve via portal
- Dispute workflow (tenant flags item; landlord responds with evidence)
- Refund payment integration (M-Pesa or bank transfer; auto-sent when approved)
- Final statement archive (both parties can download anytime)

**What Can Go Wrong**:
- Deductions not itemized (tenant disputes "unfair deduction")
- No supporting evidence for deductions (e.g., landlord claims KSh 10,000 painting cost but no invoice)
- Refund delayed beyond agreement terms (30-60 days typical)
- Landlord deducts for fair wear and tear (illegal per Kenyan court rulings)
- Tenant disputes settlement but landlord ignores → tribunal/court case

**Automation Opportunity** (HIGH VALUE):
- Settlement auto-calculated immediately after move-out inspection
- Every deduction linked to supporting document (photo, invoice)
- Tenant can approve settlement online
- Refund auto-processed within 24 hours of approval (vs. 30-60 days manual)
- Disputed items flagged for manager review
- Compliance tracker: "Settlement must be sent within 14 days per agreement"

**Typical Timeline**: 
- Settlement statement sent: 7-14 days after move-out
- Tenant review: 3-7 days
- Refund processed: 30-60 days after move-out (per most agreements)

**Best Practice**: Process refund as quickly as possible (7-14 days); good landlord reputation spreads

---

### Step 3.5: Deposit Refund (or Balance Collection)

**Who**: Landlord/Manager pays (or tenant pays if owes balance)  
**Action (Landlord/Manager)** (if refund owed):
- Transfer net refund amount to tenant via M-Pesa or bank transfer
- Issue final receipt
- Close tenant ledger
- Archive tenancy records (retain for 6 years per data protection and tax requirements)

**Action (Tenant)** (if balance owed):
- Pay outstanding balance
- Obtain clearance letter

**Records Created**:
- Refund payment record
- Final receipt/clearance letter
- Tenancy closure record

**System Features**:
- One-click refund payment (M-Pesa STK push or bank transfer)
- Auto-generate final receipt and email to tenant
- Tenancy status: "Closed" with closure date
- Data retention scheduler (archive after 6 years)

**What Can Go Wrong**:
- Refund not paid within agreed timeline (breach of agreement)
- Wrong amount refunded (calculation error)
- Tenant doesn't receive refund (payment sent to wrong number/account)
- Landlord tries to keep deposit without justification (tenant goes to tribunal)

**Automation Opportunity**:
- Refund payment directly from system (instant M-Pesa or same-day bank transfer)
- Tenant receives SMS: "Your deposit refund of KSh [X] has been sent to [number]. Transaction [ref]"
- Auto-close tenancy record
- If balance owed by tenant: auto-send payment request with 7-day deadline

---

### Step 3.6: Post-Tenancy Obligations

**Who**: Landlord/Manager  
**Action**:
- If damages identified: arrange repairs before re-listing unit
- Conduct property refresh (painting, deep cleaning) if needed
- Update unit status to "Vacant" in system
- Prepare for new tenant marketing
- Retain all tenancy records securely for required period (6 years for legal claims; tax records 5 years)
- Anonymize/delete personal data after retention period (Data Protection Act requirement)

**Records Created**:
- Post-tenancy repair log
- Unit vacancy record

**System Features**:
- Vacancy tracker (unit available from [date])
- Work order for post-tenancy repairs
- Automated data retention and deletion (after 6 years, tenant personal data auto-anonymized)

**What Can Go Wrong**:
- Repairs delayed; unit sits vacant losing revenue
- Records lost or deleted too early (needed for dispute/audit)
- Personal data retained beyond legal requirement (data protection violation)

**Automation Opportunity**:
- When tenancy closed, unit auto-marked "Vacant - Preparing" until repairs done
- Once ready: auto-change to "Vacant - Available" and trigger listing workflow
- Data retention clock starts on tenancy closure date
- After 6 years: system prompts "Anonymize Tenant X data? Retention period expired."

---

## Cross-Cutting Workflows

### Dispute Resolution

**Triggers**: Any disagreement (deposit, repairs, rent increase, termination)  
**Process**:
1. Internal resolution attempt (direct communication between parties)
2. If unresolved: Mediation (neutral third party, voluntary)
3. If still unresolved: Tribunal or Court
   - Rent Restriction Tribunal (Cap 296 residential)
   - Business Premises Rent Tribunal (Cap 301 commercial)
   - Small Claims Court (amounts under KSh 1 million)
   - Magistrate/High Court (larger claims, complex issues)

**System Support**:
- Dispute log (issue, date raised, resolution attempts)
- Evidence export (all relevant records, communications, photos, payments)
- Tribunal filing assistance (forms, required documents)
- Hearing date tracker

---

### Compliance Reporting

**KRA (Kenya Revenue Authority)**:
- Monthly rental income return (due 20th of following month)
- Annual income tax return
- Withholding tax if landlord is non-resident

**Data Protection Commissioner**:
- Data controller registration (one-time + annual renewal)
- Data breach reporting (within 72 hours of discovery)
- Data subject access requests (respond within 21 days)

**System Support**:
- KRA report generator (monthly rental income by property)
- eTIMS invoice integration (for VAT-registered landlords)
- Data breach alert workflow
- Data subject request tracker

---

## Automation Priority Matrix

### Highest Impact (Automate First)

1. **M-Pesa payment reconciliation** (eliminates 90% of manual payment matching)
2. **Automated invoicing** (reduces admin time 80%)
3. **Move-in/move-out inspections with photos** (prevents deposit disputes)
4. **Arrears tracking and reminder workflows** (improves collection rates 20-30%)
5. **Lease expiry alerts** (prevents lease lapses, enables proactive renewals)

### High Impact (Automate Soon)

6. **Maintenance request tracking** (improves tenant satisfaction, reduces response time)
7. **Automated receipts** (KRA compliance, reduces admin time)
8. **Settlement calculation** (speeds deposit refunds from 45 days to 7 days)
9. **Communication logging** (prevents disputes, improves accountability)
10. **Tenant application and vetting workflow** (reduces time-to-lease from 7 days to 2 days)

### Medium Impact (Nice to Have)

11. **Utility meter reading and billing**
12. **Property marketing and listing syndication**
13. **Rent escalation calculator and notice generator**
14. **Key tracking and handover log**
15. **Document e-signature integration**

---

## Workflow Metrics & KPIs

### For Landlord/Manager

- **Vacancy rate** (% of units vacant at any time)
- **Time-to-lease** (days from vacancy to new tenant move-in)
- **Rent collection rate** (% of rent collected on time)
- **Arrears rate** (% of rent overdue >30 days)
- **Average arrears age** (days overdue for outstanding rent)
- **Maintenance response time** (hours from request to resolution)
- **Tenant retention rate** (% of tenants who renew)
- **Deposit dispute rate** (% of tenancies ending in deposit disputes)
- **Eviction rate** (% of tenancies ending in tribunal/court eviction)

### For Tenants

- **Payment success rate** (% of on-time rent payments)
- **Maintenance satisfaction** (rating of repair responsiveness)
- **Communication responsiveness** (landlord reply time to tenant messages)
- **Deposit refund time** (days from move-out to refund received)

### For System

- **Payment automation rate** (% of payments auto-reconciled vs. manual)
- **Invoice delivery rate** (% of invoices successfully delivered)
- **Inspection completion rate** (% of move-ins/move-outs with documented inspection)
- **Data retention compliance** (% of records properly archived/anonymized)

---

## Conclusion

The tenant and management lifecycle involves dozens of steps, hundreds of records, and multiple parties. **The greatest value of a rental management system is in automation, transparency, and dispute prevention.**

### Key Success Factors:

1. **Never skip joint inspections** (move-in and move-out with photos)
2. **Document everything** (payments, communications, notices, repairs)
3. **Automate routine tasks** (invoicing, receipts, reminders)
4. **Real-time payment reconciliation** (M-Pesa integration is game-changing)
5. **Transparency** (tenant and landlord see the same information)

### Next Steps:

- **Develop system architecture** based on this lifecycle
- **Design database schema** to capture all records identified
- **Build automation workflows** starting with highest-impact items
- **Test with real users** (landlords and tenants) at each phase
- **Iterate** based on feedback and Kenyan market realities

---

**Document Prepared**: October 2026  
**Purpose**: Guide system design and development for Kenya rental management platform  
**Next Deliverable**: Excel dataset with sample data
