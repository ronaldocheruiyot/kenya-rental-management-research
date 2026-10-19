# Rental Management Dataset - User Guide

## Overview

This dataset represents a complete, realistic rental management system data structure for Kenya. It includes **9 interlinked tables** with sample data covering 3 properties, 15 units, 12 tenants, and 6 months of operational history (May - October 2026).

## Files Included

All files are in CSV format (comma-separated values) for universal compatibility:

1. `properties.csv` - Properties owned/managed
2. `units.csv` - Individual rental units within properties
3. `tenants.csv` - Tenant master records
4. `staff.csv` - Property management staff
5. `tenancies.csv` - Lease agreements linking tenants to units
6. `charges.csv` - All charges (rent, deposits, utilities, penalties)
7. `payments.csv` - All payments received
8. `meter_readings.csv` - Electricity and water meter readings
9. `events.csv` - Significant events (move-ins, move-outs, repairs, notices)

## How to Use in Excel

### Option 1: Import All Files into One Workbook

1. Open Microsoft Excel or Google Sheets
2. Create a new workbook
3. For each CSV file:
   - Click **Data** > **Get Data** > **From File** > **From Text/CSV** (Excel)
   - OR **File** > **Import** > **Upload** (Google Sheets)
   - Select the CSV file
   - Choose **Load to** > **Existing worksheet** > Specify sheet name
4. You'll have one workbook with 9 sheets, each representing a table

### Option 2: Open CSV Files Individually

- Each CSV can be opened directly in Excel
- Save as `.xlsx` if you want Excel format

## Data Relationships (How Tables Connect)

```
PROPERTIES (property_id)
    ↓
UNITS (unit_id, property_id)
    ↓
TENANCIES (tenancy_id, unit_id, tenant_id)
    ↓ ↓
TENANTS (tenant_id)    CHARGES (charge_id, tenancy_id)
                           ↓
                       PAYMENTS (payment_id, charge_id)

METER_READINGS (reading_id, unit_id)
EVENTS (event_id, property_id, unit_id, tenant_id, tenancy_id)
STAFF (staff_id)
```

### Key Relationships:

- **Properties contain Units** (one-to-many)
  - Link: `units.property_id` = `properties.property_id`
  
- **Tenancies link Tenants to Units** (many-to-many through tenancies)
  - Link: `tenancies.tenant_id` = `tenants.tenant_id`
  - Link: `tenancies.unit_id` = `units.unit_id`
  
- **Charges belong to Tenancies** (one-to-many)
  - Link: `charges.tenancy_id` = `tenancies.tenancy_id`
  
- **Payments settle Charges** (one-to-many)
  - Link: `payments.charge_id` = `charges.charge_id`
  
- **Meter Readings are per Unit** (one-to-many)
  - Link: `meter_readings.unit_id` = `units.unit_id`
  
- **Events reference Properties, Units, Tenants, Tenancies** (many-to-one)
  - Link: `events.property_id` = `properties.property_id`
  - Link: `events.unit_id` = `units.unit_id`
  - Link: `events.tenant_id` = `tenants.tenant_id`
  - Link: `events.tenancy_id` = `tenancies.tenancy_id`

## Using the Dataset

### Example Queries You Can Answer:

1. **Which units are currently vacant?**
   - Filter `units.csv` where `current_status = "Vacant"`

2. **How much rent was collected in October 2026?**
   - Filter `payments.csv` where `payment_date` is in October 2026
   - Sum `amount_paid` where `payment_type = "Rent"`

3. **Which tenants are in arrears?**
   - Sum `charges.amount` per tenancy
   - Sum `payments.amount_paid` per tenancy
   - Compare: if charges > payments, tenant owes balance

4. **What's the average rent per bedroom in Property P001?**
   - Filter `units.csv` where `property_id = "P001"`
   - Average `monthly_rent` grouped by `bedrooms`

5. **How many maintenance requests were logged in September?**
   - Filter `events.csv` where `event_type = "Maintenance Request"` and `event_date` in September 2026

### Creating Useful Reports in Excel:

#### Rent Roll Report
1. Use `units.csv` as base table
2. VLOOKUP to get property name from `properties.csv`
3. VLOOKUP to get tenant name from `tenants.csv` (via `tenancies.csv`)
4. Show: Property, Unit, Tenant, Monthly Rent, Status

#### Arrears Report
1. Use `tenancies.csv` as base
2. SUMIF charges by tenancy_id
3. SUMIF payments by charge_id (linked to tenancy)
4. Calculate: Total Owed - Total Paid = Balance

#### Occupancy Report
1. Count total units from `units.csv`
2. Count occupied units (where `current_status = "Occupied"`)
3. Calculate occupancy rate: Occupied / Total × 100%

## Sample Data Summary

### Properties (3 total)
- **P001**: Maplewood Apartments - Kilimani, Nairobi (10 units, mid-range residential)
- **P002**: Westgate Business Center - Westlands, Nairobi (4 units, commercial offices)
- **P003**: Bamburi Beach Residences - Bamburi, Mombasa (1 unit included as sample)

### Units (15 total)
- 10 residential apartments (bedsitters, 1BR, 2BR)
- 4 commercial offices
- 1 coastal residential

### Tenants (12 active + 1 departed)
- Mix of individuals and companies
- Various income levels and occupations
- Representative of Kenyan urban rental market

### Tenancies (13 total: 10 active, 2 ended, 1 pending)
- Start dates from January - September 2026
- Different lease types (monthly, 1-year, 2-year)
- Mix of controlled and uncontrolled tenancies

### Charges (78 records)
- Rent charges (monthly recurring)
- Deposits (one-time)
- Service charges
- Utilities
- Late payment penalties
- Maintenance charges

### Payments (65 records)
- M-Pesa (majority)
- Bank transfers
- Some partial payments
- Some late payments
- All properly receipted

### Meter Readings (60 records)
- Electricity readings (monthly)
- Water readings (monthly)
- May - October 2026 period

### Events (42 records)
- Move-ins (10)
- Move-outs (2)
- Maintenance requests (15)
- Late payment warnings (8)
- Rent increases (2)
- Other events (5)

## Quality Features of This Dataset

1. **Realistic IDs**: Property IDs (P001, P002), Unit IDs (U001-U015), etc.
2. **Proper Dates**: All dates in ISO format (YYYY-MM-DD) for easy sorting
3. **Complete Linkages**: Every foreign key has a matching primary key
4. **No Orphan Records**: All child records have valid parent records
5. **Balanced Payments**: Charge amounts approximately match payment totals (some arrears intentionally included)
6. **Kenyan Context**: M-Pesa payments, KRA PINs, Kenya phone numbers, Nairobi/Mombasa locations
7. **Real Scenarios**: Late payments, maintenance issues, move-outs, deposit refunds

## Common Data Quality Issues (Intentionally Avoided)

✅ **This dataset does NOT have these problems:**
- Duplicate records
- Mismatched IDs (broken links)
- Negative amounts
- Future dates where not logical
- Missing required fields
- Inconsistent naming (e.g., "Nairobi" vs. "nairobi")

## Extending the Dataset

You can add more data following the same patterns:

1. **Add a new property**: Add row to `properties.csv`, then add units in `units.csv`
2. **Add a new tenant**: Add row to `tenants.csv`, then create tenancy in `tenancies.csv`
3. **Record a payment**: Add row to `payments.csv` with `charge_id` from existing charge
4. **Log an event**: Add row to `events.csv` with relevant IDs

## Converting to Database

If you want to migrate this to a database (MySQL, PostgreSQL, SQLite):

1. Each CSV file becomes a database table
2. Column names become field names
3. ID columns become primary keys
4. Foreign key columns get proper constraints
5. Add indexes on frequently queried fields (tenant_id, property_id, payment_date, etc.)

### Suggested SQL Schema:
```sql
CREATE TABLE properties (
    property_id VARCHAR(10) PRIMARY KEY,
    property_name VARCHAR(200),
    property_type VARCHAR(50),
    -- ... other fields
);

CREATE TABLE units (
    unit_id VARCHAR(10) PRIMARY KEY,
    property_id VARCHAR(10) REFERENCES properties(property_id),
    -- ... other fields
);

-- ... and so on for each table
```

## Data Protection Compliance Note

This dataset contains sample personal data (names, ID numbers, phone numbers, addresses). In a production system:

1. **Obtain consent** from tenants before collecting data
2. **Encrypt sensitive fields** (ID numbers, bank accounts)
3. **Retain only as long as necessary** (6 years post-tenancy for legal purposes)
4. **Anonymize after retention period** (replace names with "Tenant #123", null out ID numbers)
5. **Access control**: Only authorized staff can view personal data
6. **Audit logs**: Track who accessed which tenant records and when

---

**Dataset Created**: October 2026  
**Purpose**: Seed data for rental management system development and testing  
**Geographic Scope**: Kenya (Nairobi and Mombasa)  
**Time Period**: January - October 2026 (10 months)

**Ready to use in Excel, Google Sheets, or database import!**
