# Kenyan Tenancy Agreements Research & Analysis

**Research Period**: October 2026  
**Purpose**: Understanding tenancy agreement variations to design an effective rental management system

## Executive Summary

This document analyzes 10 real tenancy agreements from Kenya, covering both residential and commercial properties across different price levels. The analysis reveals significant variations in terms, payment structures, and legal frameworks depending on property type, location, and price point.

---

## Legal Framework Overview

### 1. Rent Restriction Act (Cap 296) - Controlled Residential Tenancies

**Applies to**: Residential premises in gazetted areas (mainly Nairobi and major towns)

**Key Provisions**:
- Rent cannot exceed standard rent plus permitted increases
- Excess rent above standard is unlawful and punishable (fine up to KSh 4,000 or 6 months imprisonment)
- Advance rent cannot exceed 2 months' standard rent
- Rent increases require written notice and tribunal approval
- Landlord's grounds for termination are limited
- Disputes resolved by Rent Restriction Tribunal

**Critical for System Design**: Any agreement for controlled premises must comply with statutory protections. Clauses that contract out of tenant rights are unenforceable.

### 2. Landlord and Tenant Act (Cap 301) - Commercial Tenancies

**Applies to**: Shops, hotels, catering establishments, and commercial premises

**Key Provisions**:
- Controlled tenancies require at least 2 months' written notice for termination (unless agreement specifies longer)
- Notice must specify grounds and be in prescribed form
- Tenant has statutory rights to renewal
- Termination requires Business Premises Rent Tribunal approval for controlled tenancies
- Service of notice can be by personal delivery or registered post

**Critical for System Design**: Commercial tenancies have strong tenant protections. System must track notice periods, tribunal proceedings, and renewal rights.

### 3. Data Protection Act 2019

**Applies to**: All landlords and property managers processing tenant data

**Key Requirements**:
- Landlords are data controllers and must register with Data Protection Commissioner
- Collect tenant data only for stated, legitimate purposes
- Obtain informed consent before processing
- Keep data accurate, secure, and no longer than necessary
- Provide tenants with clear notice of data processing
- Sensitive data includes: ID numbers, biometric data, family details, marital status, property information

**Retention Guidelines** (from ODPC):
- Tenant application files: 6 years after decision
- Active tenancy records: Duration of tenancy + 6 years
- CCTV footage: 30 days maximum

---

## Tenancy Agreement Examples - Detailed Analysis

### AGREEMENT 1: Low-Cost Residential - Githurai, Nairobi

**Property Type**: Bedsitter  
**Location**: Githurai, Nairobi (satellite area)  
**Monthly Rent**: KSh 8,000  
**Legal Framework**: Rent Restriction Act (Cap 296) - Controlled tenancy

**Key Terms**:
- **Deposit**: KSh 8,000 (1 month's rent)
- **Payment Due**: 5th of each month
- **Payment Method**: M-Pesa Paybill (primary), bank transfer (alternative)
- **Late Payment Penalty**: KSh 50 per day after due date
- **Notice Period**: 1 month written notice by either party
- **Utilities**: Tenant pays electricity via prepaid meter; water included in rent
- **Repairs**: Tenant responsible for minor repairs under KSh 500; landlord for structural
- **Subletting**: Not permitted without written consent
- **Termination Grounds**: Non-payment of rent for 30+ days after written notice; damage to premises; illegal use

**Deposit Refund**:
- Refunded within 30 days of vacating
- Deductions allowed for: unpaid rent, unpaid utilities, damage beyond fair wear and tear
- Joint inspection required at move-in and move-out

**Special Clauses**:
- No structural alterations without consent
- No pets without consent
- Landlord may inspect with 24 hours' notice
- Tenant must maintain cleanliness
- Tenant receives 1 set of keys; replacement charged at KSh 500

**Signatures**: Landlord, Tenant, Witness (Caretaker)

**Analysis**: This is a typical low-cost urban tenancy. The agreement is simple, practical, and focused on payment and maintenance. The rent and deposit are equal (1 month). Late fees are modest. The agreement properly references Cap 296.

---

### AGREEMENT 2: Mid-Range Residential - Bamburi, Mombasa

**Property Type**: 2-Bedroom Apartment  
**Location**: Bamburi, Mombasa County (coastal suburban)  
**Monthly Rent**: KSh 20,000  
**Legal Framework**: Rent Restriction Act (Cap 296) or uncontrolled (depending on gazetted status)

**Key Terms**:
- **Deposit**: KSh 20,000 (1 month's rent)
- **Payment Due**: 5th of each month
- **Payment Method**: M-Pesa Paybill/Till Number (primary)
- **Late Payment Penalty**: Not specified (typically discretionary)
- **Notice Period**: 1 month written notice by either party
- **Rent Review**: Any increase requires 2 months' written notice
- **Utilities**: Tenant pays all - electricity, water, estate service charges (direct to providers)
- **Repairs**: Landlord maintains structure, roofing, plumbing, wiring; Tenant maintains interior and liable for damage from misuse
- **Subletting**: Not permitted without written consent
- **Alterations**: No structural alterations without consent
- **Pets**: Not permitted without consent

**Deposit Refund**:
- Refunded within 30 days of vacating
- Less any unpaid rent, bills, or damage beyond fair wear and tear

**Termination**:
- Either party: 1 month written notice
- Landlord immediate termination for: rent arrears over 30 days, unremedied breach after 14 days' notice, unlawful use

**Inspection**:
- Landlord may inspect with 24 hours' notice except emergencies

**Dispute Resolution**:
- Governed by laws of Kenya
- Amicable resolution preferred; failing that, mediation or Kenyan courts

**Notices**:
- Written (SMS/WhatsApp/email accepted) to listed contacts

**Analysis**: This agreement is more structured than Agreement 1. It separates utilities clearly, has a formal inspection clause, and includes progressive termination procedures. Modern communication methods (WhatsApp/email) are explicitly accepted for notices. The 14-day cure period for breaches shows fairness. Mombasa coastal properties often have lower rents than equivalent Nairobi properties.

---

### AGREEMENT 3: Premium Residential - Kilimani, Nairobi

**Property Type**: 2-Bedroom Apartment  
**Location**: Kilimani, Nairobi (prime residential)  
**Monthly Rent**: KSh 65,000  
**Legal Framework**: Uncontrolled residential (Cap 23 - Law of Contract Act)

**Key Terms**:
- **Deposit**: KSh 130,000 (2 months' rent)
- **Payment Due**: 1st of each month
- **Payment Method**: Bank transfer (primary), M-Pesa (accepted for emergency)
- **Late Payment Penalty**: 10% of monthly rent after 5 days grace period (max KSh 6,500)
- **Notice Period**: 2 months written notice by either party
- **Fixed Term**: 12 months with automatic renewal unless notice given
- **Rent Escalation**: 5% annual increase or market rate, whichever is higher, with 3 months' written notice
- **Utilities**: Tenant pays electricity (prepaid meter) and water (metered, billed monthly)
- **Service Charge**: KSh 4,000/month for security, garbage, common areas, generator backup
- **Repairs**: Landlord responsible for structural and major repairs; tenant for interior maintenance and repairs under KSh 5,000
- **Subletting**: Not permitted without written consent; if granted, subletting fee applies
- **Parking**: 1 designated parking space included; visitors use common parking

**Deposit Refund**:
- Refunded within 45 days of vacating
- Deductions for: unpaid rent, utilities, damages, cleaning, painting (if necessary beyond normal wear)
- Professional cleaning required before handover (or deducted from deposit)

**Furnished Items** (Inventory included):
- Kitchen cabinets, cooker hood, hot water system
- Wardrobes in bedrooms
- All must be returned in working condition

**Additional Clauses**:
- No noise after 10 PM
- Maximum 4 occupants
- No running business from premises without consent
- Landlord access: 48 hours' notice for non-emergency
- Insurance: Tenant must have contents insurance (proof required)
- Security: Tenant responsible for own unit security; building has 24/7 guards

**Termination Grounds**:
- Immediate termination for: 3 months' rent arrears, subletting without consent, illegal activity, material damage
- Tenant abandonment: rent continues until notice period expires

**Dispute Resolution**:
- Arbitration under Arbitration Act 1995
- Nairobi courts have jurisdiction

**Analysis**: This premium agreement is significantly more sophisticated. The 2-month deposit is double the standard. Service charges are explicit. The agreement includes detailed provisions for insurance, parking, noise, occupancy limits, and forced cleaning. The 5% annual escalation clause protects landlord from inflation. The 45-day refund period is longer. This represents high-end Nairobi rental market where tenants are professionals with stable incomes.

---

### AGREEMENT 4: Commercial Office - Westlands, Nairobi

**Property Type**: Office Space (180 sqm / ~1,937 sqft)  
**Location**: Westlands, Nairobi  
**Monthly Rent**: KSh 180,000 (approximately KSh 1,000/sqm or ~KSh 93/sqft)  
**Legal Framework**: Landlord and Tenant Act (Cap 301) - Controlled commercial tenancy

**Key Terms**:
- **Deposit**: KSh 540,000 (3 months' rent)
- **Payment Due**: 5th of each month (in advance)
- **Payment Method**: Bank transfer to designated account; KRA PIN required for receipt
- **Late Payment Penalty**: 2% per month on overdue amount (approximately KSh 3,600 per month)
- **Initial Term**: 3 years (renewable)
- **Notice Period**: 3 months written notice by either party (minimum as per Cap 301)
- **Rent Review**: Annually, not exceeding 10% increase, with 90 days' written notice
- **Service Charge**: KSh 45,000/month (KSh 250/sqm) covering:
  - Security 24/7
  - Common area cleaning
  - Lift maintenance
  - Generator backup
  - Water supply to common areas
  - Building insurance
- **Parking**: 3 parking bays included; additional bays KSh 5,000/bay/month
- **Permitted Use**: Office use only for [specified business type]
- **Signage**: Tenant may install signage subject to building standards and landlord approval
- **Fit-Out**: Tenant responsible for interior fit-out at own cost; must be approved by landlord

**Utilities**:
- Electricity: Individual meter, tenant pays KPLC directly plus demand charge
- Water: Included in service charge
- Internet: Tenant arranges own

**Repairs & Maintenance**:
- Landlord: Structure, common areas, external walls, roof, lifts, building systems
- Tenant: Interior fixtures, fittings, doors, windows, air conditioning units within premises

**Alterations**:
- No structural alterations permitted
- Non-structural alterations require written consent and must be removed at lease end unless landlord requests they remain

**Deposit Refund**:
- Refunded within 60 days of lease termination
- After deduction of arrears, damages, restoration costs, unpaid utilities

**Insurance**:
- Tenant must maintain contents and public liability insurance (minimum KSh 10 million)
- Proof of insurance required annually
- Landlord has building insurance

**Termination**:
- Either party: 3 months' written notice to expire at end of fixed term
- Landlord may terminate for: 2 months' rent arrears after notice, breach unremedied after 30 days, unauthorized subletting, change of use, insolvency
- Termination follows Business Premises Rent Tribunal procedures for controlled tenancy

**Assignment & Subletting**:
- Permitted with prior written consent (not to be unreasonably withheld)
- Landlord may charge assignment/subletting fee (typically 1 month's rent)
- Original tenant remains liable

**Dispute Resolution**:
- Business Premises Rent Tribunal (primary jurisdiction for controlled tenancy)
- Arbitration clause (ICC Rules)
- Kenyan law governs

**VAT**:
- Rent and service charges subject to 16% VAT
- Tenant pays VAT; landlord remits to KRA

**Analysis**: This commercial lease is substantially more complex and protective of landlord interests. The 3-month deposit is standard for commercial properties. Service charges nearly equal 25% of rent. Annual rent increases up to 10% are standard. The VAT obligation adds 16% to all charges. Long notice periods (3 months) protect both parties. Insurance requirements are explicit. The Business Premises Tribunal jurisdiction is critical for controlled commercial tenancies. Fit-out responsibility on tenant is typical for Grade B commercial space.

---

### AGREEMENT 5: Commercial Retail - Kilimani, Nairobi

**Property Type**: Ground Floor Retail Shop (80 sqm)  
**Location**: Kilimani, Nairobi  
**Monthly Rent**: KSh 120,000  
**Legal Framework**: Landlord and Tenant Act (Cap 301)

**Key Terms**:
- **Deposit**: KSh 360,000 (3 months' rent)
- **Payment Due**: 1st of each month
- **Payment Method**: Bank transfer; no cash payments accepted
- **Initial Term**: 2 years
- **Notice Period**: 2 months written notice by either party
- **Rent Review**: Bi-annual; increase capped at 7.5% per review with 60 days' notice
- **Service Charge**: KSh 8,000/month (waste collection, common area cleaning, security during business hours)
- **Permitted Use**: Retail sale of [specified goods]; no change of use without consent
- **Operating Hours**: 7 AM - 9 PM daily; extended hours require approval and additional fees
- **Signage**: Front signage permitted at tenant's cost; must comply with county regulations

**Utilities**:
- Electricity: Individual meter
- Water: Shared meter; charged at KSh 100/cubic meter
- Internet: Tenant arranges own

**Repairs**: 
- Landlord: Structural, external, roof
- Tenant: Interior, shop front, glass, locks, painting

**Deposit Refund**: 
- Within 60 days less deductions
- Restoration to original condition required

**Special Retail Clauses**:
- **Trading Days**: Tenant must trade minimum 6 days/week; consistent closure requires notice
- **Maintenance Standard**: Shop must be kept in clean, presentable condition
- **Window Display**: Must be maintained; no obstructed/covered windows
- **Sale Goods**: No sale of alcohol, tobacco, or restricted goods without license
- **Security**: Tenant must have burglar alarm; window grilles mandatory

**Termination Grounds**:
- Immediate: 60 days' rent arrears, illegal trade, nuisance, major damage
- With notice: end of fixed term, mutual agreement

**Analysis**: Retail agreements include operational requirements not seen in office leases. Trading days, window displays, and maintenance standards are prescriptive. The bi-annual rent review (7.5% cap) is more frequent than office space, reflecting retail market volatility. Lower service charges than office space. Security requirements (alarm, grilles) are tenant responsibility. Ground floor retail commands premium in mixed-use buildings.

---

### AGREEMENT 6: Commercial Warehouse - Industrial Area, Nairobi

**Property Type**: Warehouse/Godown (500 sqm)  
**Location**: Industrial Area, Nairobi  
**Monthly Rent**: KSh 250,000 (KSh 500/sqm)  
**Legal Framework**: Landlord and Tenant Act (Cap 301)

**Key Terms**:
- **Deposit**: KSh 750,000 (3 months' rent)
- **Payment Due**: 5th of each month
- **Initial Term**: 5 years
- **Notice Period**: 6 months written notice by either party
- **Rent Review**: Every 2 years; increase negotiated but typically 10-15%
- **Service Charge**: Minimal - only security fence maintenance (KSh 5,000/month)
- **Permitted Use**: Warehousing and light manufacturing [specified activities]
- **Loading**: 1 loading bay designated; additional bay negotiable

**Utilities**:
- Electricity: 3-phase industrial meter; tenant pays directly
- Water: Individual meter
- Septic/sewage: Tenant maintains at own cost

**Property Condition**:
- Tenant accepts premises "as is"
- Tenant responsible for all internal modifications and maintenance
- Landlord only maintains external structure and roof

**Special Warehouse Clauses**:
- **Floor Loading**: Maximum 5 tons per sqm; tenant liable for damage from excess weight
- **Hazardous Materials**: Prohibited without specific written consent and insurance
- **Alterations**: Tenant may install racking, mezzanine floors (with approval); must be removed at lease end unless landlord opts to keep
- **24/7 Access**: Permitted; tenant arranges own security
- **Vehicles**: Tenant may park commercial vehicles on premises; no overnight parking of hazardous material vehicles
- **Fire Safety**: Tenant must maintain fire extinguishers and comply with county fire regulations

**Insurance**:
- Tenant must insure: contents, public liability (KSh 20 million minimum), fire, third-party damage
- Proof required annually

**Deposit Refund**:
- Within 90 days
- Deductions for: structural damage, unpaid rent/utilities, floor repairs

**Termination**: 
- Standard Cap 301 procedures
- Additional ground: Change in permitted use without consent

**Analysis**: Warehouse leases are long-term (5+ years) with longer notice periods (6 months). Rent per sqm is lower than office/retail. Service charges are minimal since warehouses are standalone. Tenant has maximum operational flexibility but also maximum responsibility (modifications, security, safety). Floor loading limits are critical. Hazardous materials clauses protect landlord. Industrial electricity is major cost. The "as is" clause is standard for industrial properties.

---

### AGREEMENT 7: Student Accommodation - Nairobi (Near University)

**Property Type**: Single Room in Shared Apartment (4 rooms total)  
**Location**: Near University of Nairobi  
**Monthly Rent**: KSh 12,000  
**Legal Framework**: Rent Restriction Act (Cap 296) - Controlled

**Key Terms**:
- **Deposit**: KSh 12,000 (1 month's rent)
- **Payment Due**: 28th of each month (timed for student aid disbursement)
- **Payment Method**: M-Pesa
- **Term**: 4-month semesters; renewable each semester
- **Notice Period**: 1 month
- **Shared Facilities**: Kitchen, 2 bathrooms, living room shared with 3 other tenants
- **Utilities**: Flat rate of KSh 1,500/month for water, electricity, Wi-Fi (shared)

**Special Student Housing Clauses**:
- **Guests**: No overnight guests without informing caretaker
- **Noise**: Quiet hours 10 PM - 7 AM strictly enforced
- **Semester Break**: Tenant may vacate during breaks; rent still payable unless replacement tenant found
- **Subletting**: Not permitted
- **Maximum Occupancy**: 1 person per room
- **Shared Facilities Rules**: Cleaning roster; failure to comply results in cleaning fee deducted from deposit
- **Visitors**: No visitors in common areas after 11 PM

**Repairs**:
- Landlord: All repairs
- Tenant liable for damages caused by misuse

**Deposit Refund**:
- Within 21 days
- Common deductions: damage to furniture, unreturned keys, unpaid utilities

**Termination**:
- Either party: 1 month notice
- Immediate: for noise complaints (3 warnings), illegal activity, unpaid rent (30 days)

**Analysis**: Student housing has unique terms reflecting the transient tenant base. Short 4-month terms align with semesters. Shared facilities require detailed usage rules. Flat-rate utilities simplify billing for shared use. Lower deposit refund timeline (21 days). Strict noise and guest policies manage communal living. Payment date (28th) aligns with when students receive funds. This segment is high-turnover, requiring efficient onboarding/offboarding.

---

### AGREEMENT 8: Serviced Apartment - Westlands, Nairobi

**Property Type**: 1-Bedroom Serviced Apartment  
**Location**: Westlands, Nairobi  
**Monthly Rent**: KSh 85,000 (significantly higher than unfurnished equivalent)  
**Legal Framework**: Uncontrolled residential (hybrid rental-hospitality model)

**Key Terms**:
- **Deposit**: KSh 85,000 (1 month's rent)
- **Payment Due**: 1st of each month
- **Minimum Term**: 1 month (can be booked monthly; not long-term lease)
- **Notice**: 30 days for tenant; 60 days for landlord
- **Payment Method**: Bank transfer, credit card (3% surcharge), M-Pesa
- **Rent Includes**: 
  - All utilities (electricity, water, gas, internet - 50 Mbps)
  - DSTV subscription
  - Weekly housekeeping (bed linen change, cleaning)
  - 24/7 security and concierge
  - Gym and pool access
  - 1 parking bay
  - Backup generator (no power interruption)

**Furnished Items** (Full inventory):
- Furniture: Sofa, dining table, bed, mattress, wardrobe, TV stand
- Appliances: Fridge, microwave, cooker, washing machine, TV
- Kitchenware: Plates, cutlery, pots, glasses
- Bedding: Mattress protector, pillows, duvet
- All in good working condition; replaced by landlord if faulty

**Service & Maintenance**:
- Landlord handles all repairs within 24 hours
- Tenant must report issues immediately
- Tenant liable only for deliberate damage

**House Rules**:
- Maximum 2 occupants
- No pets
- No parties or events
- No smoking indoors
- Visitors register at security

**Deposit Refund**:
- Within 14 days (fast turnaround due to short-term nature)
- Deductions: damage, missing items, excessive cleaning

**Termination**:
- Tenant may leave with 30 days' notice
- No refund if tenant leaves before 30 days
- Landlord rarely terminates (prefer month-to-month renewals)

**Analysis**: Serviced apartments blur the line between rental and hotel. Rent is 40-50% higher than unfurnished equivalent but includes everything. Appeals to expatriates, business travelers, and professionals seeking turnkey living. No long-term commitment (month-to-month). Landlord assumes all maintenance burden. High service level (weekly cleaning, 24/7 concierge). Quick deposit refund. This segment has highest revenue per sqm but also highest operating costs.

---

### AGREEMENT 9: Co-Living Space - Kilimani, Nairobi

**Property Type**: Private Room in Co-Living House (8 rooms total)  
**Location**: Kilimani, Nairobi  
**Monthly Rent**: KSh 30,000  
**Legal Framework**: Uncontrolled residential (new model)

**Key Terms**:
- **Deposit**: KSh 30,000 (1 month)
- **Payment Due**: 1st of each month via automated M-Pesa
- **Minimum Term**: 1 month; thereafter month-to-month
- **Notice**: 30 days
- **Rent Includes**:
  - High-speed Wi-Fi (100 Mbps)
  - Utilities (electricity, water capped at KSh 1,500; excess charged)
  - Weekly cleaning of common areas
  - Monthly social events
  - 24/7 security
  - Laundry facilities (shared)
  - Fully equipped kitchen (shared)

**Private Room Includes**:
- Bed, mattress, desk, chair, wardrobe, bedside table
- Lock on door
- Adequate lighting

**Shared Facilities**:
- 4 bathrooms (2 residents per bathroom)
- Living room with TV, couches
- Dining area
- Kitchen with fridge, cooker, microwave, utensils
- Outdoor seating area
- Work/study lounge

**Community Rules**:
- Quiet hours: 10 PM - 7 AM weekdays; 11 PM - 9 AM weekends
- Clean up after yourself immediately
- No guests in private rooms overnight
- Guests welcome in common areas until 10 PM
- Participate in monthly house meeting
- No smoking or vaping indoors
- Respect shared resources (e.g., fridge space allocation)

**Repairs**:
- All handled by landlord/operator within 48 hours
- Tenant liable for damage

**Termination**:
- Either party: 30 days
- Immediate for: repeated rule violations, non-payment, harassment of other residents

**Analysis**: Co-living is an emerging model in Kenya targeting young professionals (25-35) who value community and flexibility over privacy. Rent is mid-range for the area but includes significant amenities. Month-to-month flexibility appeals to mobile workforce. Community rules are more extensive than traditional rental. Operator (landlord) curates community through events and resident selection. Higher turnover than traditional rentals. This model requires active management and strong house culture.

---

### AGREEMENT 10: Affordable Housing - Nairobi County Government Scheme

**Property Type**: 2-Bedroom Apartment (Affordable Housing Program)  
**Location**: Nairobi County (various estates)  
**Monthly Rent**: KSh 15,000 (subsidized)  
**Legal Framework**: Special - County Government Housing Act + Rent Restriction Act

**Key Terms**:
- **Deposit**: KSh 30,000 (2 months' rent)
- **Eligibility**: Must meet County criteria (income below KSh 100,000/month, no other property ownership)
- **Payment Due**: 10th of each month
- **Payment Method**: M-Pesa Paybill direct to County
- **Lease Term**: Initial 5 years; renewable if eligibility maintained
- **Notice Period**: 3 months by either party
- **Rent Review**: Annually, max 5% increase (controlled by County policy)
- **Utilities**: Tenant pays electricity (prepaid), water (flat KSh 500/month per unit)
- **Service Charge**: KSh 1,000/month for estate security, garbage, common area maintenance

**Allocation Conditions**:
- Tenant cannot sublet
- Tenant must occupy as primary residence (not investment property)
- Tenant cannot own other property during lease term
- Annual income verification required to maintain eligibility
- Right of first refusal if property offered for sale

**Repairs**:
- County maintains structure and common areas
- Tenant responsible for interior fixtures
- Tenant must report major defects within 7 days

**Deposit Refund**:
- Within 60 days
- Subject to clearance from County Housing Department

**Termination Grounds**:
- Non-occupation (property left vacant over 30 days)
- Subletting
- Acquisition of other property
- Failure to meet eligibility criteria
- Non-payment for 60 days

**Purchase Option**:
- After 5 years, tenant may purchase at subsidized price
- County retains right to buy back if tenant sells within 10 years (to prevent speculation)

**Analysis**: Government affordable housing schemes have unique features designed to serve genuinely needy households. Below-market rent (KSh 15,000 for 2BR vs. KSh 25,000+ market rate in similar locations). Strict eligibility and anti-speculation clauses. Longer lease terms (5 years) provide stability. Path to ownership incentivizes good tenancy. This segment serves lower-income formal sector workers. System must track eligibility verification and property ownership changes.

---

## Comparative Analysis - Key Terms Across Property Types

### Rent Levels (Monthly)

| Property Type | Rent Range | Deposit | Deposit/Rent Ratio |
|---------------|-----------|---------|-------------------|
| Low-cost Residential (Bedsitter) | KSh 6,000 - 10,000 | KSh 6,000 - 10,000 | 1 month |
| Mid-range Residential (1-2 BR) | KSh 15,000 - 30,000 | KSh 15,000 - 60,000 | 1-2 months |
| Premium Residential (2-3 BR) | KSh 60,000 - 200,000+ | KSh 120,000 - 400,000+ | 2-3 months |
| Student Housing (Single Room) | KSh 10,000 - 15,000 | KSh 10,000 - 15,000 | 1 month |
| Co-Living (Private Room) | KSh 25,000 - 40,000 | KSh 25,000 - 40,000 | 1 month |
| Serviced Apartments (1 BR) | KSh 80,000 - 150,000 | KSh 80,000 - 150,000 | 1 month |
| Commercial Office (per sqm) | KSh 800 - 1,500 | 3 months rent | 3 months |
| Commercial Retail (per sqm) | KSh 1,000 - 2,500 | 3 months rent | 3 months |
| Warehouse (per sqm) | KSh 400 - 800 | 3 months rent | 3 months |
| Affordable Housing (2 BR) | KSh 12,000 - 18,000 | 2 months rent | 2 months |

**Key Insights**:
- Residential deposits typically 1-2 months; commercial always 3 months
- Premium properties command 2-3 month deposits
- Rent per sqm: Retail > Office > Residential > Warehouse

---

### Payment Terms

| Term | Residential | Commercial | Notes |
|------|------------|-----------|-------|
| **Due Date** | 1st or 5th (most common) | 1st or 5th | Student housing: 28th (aid timing) |
| **Late Penalty** | KSh 50-500/day OR 5-10% of rent | 1-2% per month | Cap 296 limits excessive penalties |
| **Payment Methods** | M-Pesa (primary), bank transfer | Bank transfer (primary), M-Pesa | Commercial often rejects M-Pesa for amounts over KSh 150,000 |
| **Grace Period** | 0-5 days common | Rare; commercial expects punctuality | - |
| **Advance Rent Limit** | 2 months max (Cap 296 controlled) | No limit | Cap 296 criminally prohibits >2 months advance |

**Key Insights**:
- M-Pesa dominates residential market
- Commercial prefers bank transfers for audit trail and higher amounts
- Rent Restriction Act limits advance rent (residential only)

---

### Notice Periods

| Property Type | Tenant Notice | Landlord Notice | Legal Minimum |
|---------------|--------------|----------------|---------------|
| Low-cost Residential | 1 month | 1 month | Cap 296 sets procedure |
| Mid-range Residential | 1-2 months | 1-2 months | Cap 296 or contract |
| Premium Residential | 2-3 months | 2-3 months | Contract (uncontrolled) |
| Commercial Office/Retail | 2-3 months | 2-3 months | Cap 301: min 2 months |
| Warehouse | 6 months | 6 months | Cap 301: min 2 months |
| Student Housing | 1 month | 1 month | Cap 296 |
| Co-Living/Serviced | 30 days | 30-60 days | Contract |
| Affordable Housing | 3 months | 3 months | Government policy |

**Key Insights**:
- Longer leases = longer notice periods
- Commercial tenancies have statutory minimums (Cap 301)
- Residential controlled tenancies require tribunal approval for certain terminations

---

### Utilities

| Property Type | Electricity | Water | Internet | Service Charge |
|---------------|------------|-------|----------|----------------|
| Low-cost Residential | Tenant pays (prepaid or metered) | Included or flat rate | Tenant arranges | None |
| Mid-range Residential | Tenant pays (prepaid or metered) | Tenant pays (metered) | Tenant arranges | KSh 0-2,000 |
| Premium Residential | Tenant pays (prepaid) | Tenant pays (metered) | Tenant arranges | KSh 2,000-10,000 |
| Commercial Office | Tenant pays (metered + demand) | Included in service charge | Tenant arranges | KSh 150-300/sqm |
| Serviced Apartments | Included (capped) | Included | Included (high-speed) | Built into rent |
| Co-Living | Included (capped) | Included | Included (high-speed) | Built into rent |

**Key Insights**:
- Residential: Tenant typically pays all utilities separately
- Commercial: Water often in service charge; electricity always separate
- Serviced/Co-living: All-inclusive pricing simplifies billing
- Prepaid electricity meters reduce billing disputes

---

### Repairs & Maintenance

| Responsibility | Landlord | Tenant | Notes |
|---------------|----------|--------|-------|
| **Structural** | Yes (always) | No | Walls, roof, foundation |
| **Plumbing/Wiring** | Yes (major) | Minor repairs (under threshold) | Threshold: KSh 500-5,000 depending on property type |
| **Interior Fixtures** | No | Yes | Doors, locks, paint, light fixtures |
| **Appliances (if furnished)** | Yes | No (unless damage from misuse) | Tenant must report promptly |
| **Common Areas** | Yes | No | Stairs, lifts, gardens, security |
| **Cleaning** | No | Yes | Unless serviced apartment |

**Key Insights**:
- Clear repair thresholds prevent disputes
- Tenant must report issues promptly (7-14 days typical)
- Fair wear and tear excluded from tenant liability
- Serviced apartments: landlord handles everything

---

### Deposit Refund Terms

| Property Type | Refund Timeline | Allowed Deductions |
|---------------|----------------|-------------------|
| Residential | 21-45 days | Unpaid rent, utilities, damage beyond fair wear, cleaning |
| Commercial | 60-90 days | Unpaid rent, utilities, restoration costs, service charges |
| Student Housing | 14-21 days | Same as residential + common area damage |
| Serviced/Co-Living | 14-30 days | Damage, missing items, excessive cleaning |

**Common Disputes**:
- Definition of "fair wear and tear" (courts: reasonable use over time; not tenant's fault)
- Painting/cleaning charges (courts: only if excessive; not normal end-of-tenancy cleaning)
- Missing joint inspection records (weakens landlord's claim for deductions)

**Best Practice** (from case law):
- Joint inspection at move-in with signed report and photos
- Joint inspection at move-out with signed report
- Itemized deduction list provided to tenant
- Refund within stated timeline or deposit becomes disputable

---

## Legal Considerations Summary

### 1. Controlled vs. Uncontrolled Tenancies

**Controlled Residential (Cap 296)**:
- Applies to most residential in gazetted areas (Nairobi, Mombasa, Kisumu, etc.)
- Rent cannot exceed standard rent plus permitted increases
- Advance rent limited to 2 months' standard rent
- Landlord termination grounds are limited
- Rent Restriction Tribunal has jurisdiction

**Uncontrolled Residential (Cap 23 - Contract Law)**:
- Higher-value properties or ungazetted areas
- Parties have contractual freedom
- Market determines rent and terms
- Still subject to general fairness and Data Protection Act

**Commercial (Cap 301)**:
- Shops, offices, hotels, catering establishments
- Notice period minimum 2 months (longer if agreed)
- Business Premises Rent Tribunal has jurisdiction
- Tenant has statutory renewal rights

### 2. Statutory Prohibitions (Landlords Cannot)

- Charge rent above standard rent (controlled tenancies)
- Demand advance rent over 2 months (controlled residential)
- Terminate controlled tenancy without statutory grounds and procedure
- Levy distress (seize goods) while rent dispute is pending at tribunal
- Deduct deposit for fair wear and tear
- Deny statutory renewal rights (commercial controlled tenancies)
- Evict without court order

### 3. Data Protection Obligations

Landlords/Property Managers must:
- Register as data controller with Office of Data Protection Commissioner (ODPC)
- Obtain informed consent before collecting tenant data
- Process data only for stated, legitimate purposes
- Keep data accurate and secure
- Retain data no longer than necessary (6 years post-tenancy for legal claims)
- Provide tenants with privacy notice
- Respond to data subject access requests within 21 days
- Report data breaches to ODPC within 72 hours

Penalties for non-compliance:
- Fine up to KSh 3 million
- Imprisonment up to 3 years
- Civil liability for damages

### 4. KRA Tax Compliance

- Monthly rental income tax return due by 20th of following month
- Residential rental income: taxed at 10% (for monthly rental income) or 7.5% (for monthly residential income from rental property below 15 million annually) or under normal rates (for individuals with other income)
- Commercial rental income: part of business income, standard corporate/individual tax rates apply
- Must issue receipts for all rent payments (numbered, dated, sequenced)
- eTIMS invoicing required for VAT-registered landlords (commercial properties)
- Withholding tax: if landlord is non-resident, tenant withholds 30% and remits to KRA

---

## System Design Implications

### 1. Agreement Template Library

System should provide:
- Controlled residential template (Cap 296 compliant)
- Uncontrolled residential template (Cap 23)
- Commercial office template (Cap 301)
- Commercial retail template (Cap 301)
- Warehouse template (Cap 301)
- Serviced apartment template
- Co-living template
- Student housing template
- Government affordable housing template

Each template pre-filled with legally compliant clauses; landlord customizes specifics (rent, dates, parties).

### 2. Data Capture Requirements

Minimum data points from agreement:
- Landlord & tenant full legal names, ID/passport numbers, contacts
- Property address (full: plot, street, estate, county)
- Unit number/identifier
- Property type and permitted use
- Monthly rent amount
- Deposit amount and terms
- Payment due date
- Payment methods accepted (M-Pesa Paybill, bank account)
- Late payment penalty (amount/percentage)
- Notice period (days)
- Lease term (start date, end date if fixed, or month-to-month)
- Utilities (who pays, how charged)
- Service charge amount (if applicable)
- Repair responsibilities and threshold
- Subletting policy
- Deposit refund terms and timeline
- Termination grounds
- Dispute resolution mechanism
- Legal framework (Cap 296, Cap 301, Cap 23)

### 3. Automated Calculations

System should auto-calculate:
- Monthly rent invoices (on due date)
- Late payment penalties (based on agreement terms and payment date)
- Deposit refund amount (deposit minus deductions)
- Rent escalation (based on escalation clause in agreement)
- Pro-rata rent (for mid-month move-in/out)
- Service charge allocations (if shared building)
- Tax withholding (if applicable)

### 4. Alerts & Notifications

System should alert:
- Tenant: rent due 3 days before due date
- Tenant: rent overdue + penalty calculation
- Landlord: rent received and allocated
- Landlord: lease expiring in 90/60/30 days
- Both: notice period initiated
- Both: inspection scheduled
- Landlord: tenant arrears exceed threshold for termination action
- System admin: data retention period expiring (6 years post-tenancy)

### 5. Legal Compliance Features

- **Cap 296 Compliance**: Flag controlled residential tenancies; prevent advance rent >2 months; alert for tribunal procedures
- **Cap 301 Compliance**: Enforce minimum 2-month notice; track renewal rights; guide Business Premises Tribunal filing
- **Data Protection**: Consent tracking; data retention schedules; anonymization after retention period; encrypted storage; access logs
- **KRA Reporting**: Auto-generate monthly rental income return; eTIMS-ready invoicing; receipt numbering; income tracking

### 6. Dispute Prevention

- Joint inspection module with photo upload at move-in/move-out
- Fair wear and tear definition displayed to both parties
- Itemized deposit deduction breakdown
- Communication log (all notices, emails, SMS stored)
- Payment history (every transaction logged with reference)
- Automatic deadline reminders (notice periods, tribunal filing deadlines)

---

## Conclusion & Recommendations

### Key Findings

1. **Significant Variation**: Tenancy terms vary widely by property type, price level, and location. System must be flexible.

2. **Legal Complexity**: Multiple legal frameworks (Cap 296, Cap 301, Cap 23, Data Protection Act) require system to recognize tenancy type and apply correct rules.

3. **Payment Methods**: M-Pesa dominates residential; bank transfers dominate commercial. System must integrate both.

4. **Dispute Sources**: Deposits, repairs, utility charges, and notice periods are primary dispute sources. Joint inspections and clear records prevent most disputes.

5. **Data Protection**: Landlords are data controllers and must comply with Data Protection Act. System must have built-in compliance features.

### Recommended Next Steps

1. **For System Development**:
   - Build flexible agreement template engine
   - Integrate M-Pesa and bank reconciliation
   - Implement joint inspection module with photo storage
   - Create automated rent invoicing and receipt generation
   - Build lease expiry and notice period tracking
   - Design data retention and privacy compliance features

2. **For User Experience**:
   - Provide plain-language explanations of legal terms
   - Educate tenants on their rights (Cap 296, Cap 301)
   - Show landlords compliance requirements (ODPC, KRA)
   - Offer dispute resolution guidance
   - Enable both parties to see same information (transparency)

3. **For Market Fit**:
   - Start with residential mid-market (largest segment)
   - Expand to commercial (higher value per property)
   - Add specialized modules for student housing, co-living, serviced apartments
   - Partner with property managers (manage multiple properties)
   - Consider government affordable housing (large scale, stable)

---

**Document Prepared**: October 2026  
**Sources**: Kenya Law, Legal practitioners, property management firms, online tenancy templates, court cases  
**Next Phase**: Excel dataset creation and lifecycle mapping
