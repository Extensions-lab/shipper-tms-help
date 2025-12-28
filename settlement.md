# Settlement Process

## Overview

The Settlement process in the Transportation Management System (TMS) is a comprehensive financial management feature that handles the complete lifecycle of Forwarding Order finances. It serves as the central hub for managing income, costs, billing, and financial reconciliation for transportation services.

Settlement is a comprehensive financial review and closure process that ensures all monetary aspects of a transportation order are accounted for, from the initial calculation of charges to the final payment and invoicing, ensuring transparency and financial integrity.

## What is Settlement?

Settlement in TMS is the process of **determining, recording, and reconciling all financial aspects** : of a forwarding order. It encompasses:

- **Income Calculation** : Identifying and calculating all charges to be billed to customers. This involves determining the total amount that will be billed to the client for the transportation services provided, including freight charges, fuel surcharges, and any other additional services rendered during the transportation process.
- **Cost Management** : Tracking and allocating all expenses incurred during transportation. This includes accounting for all expenses incurred by the company in providing these services, such as payments made to third-party service providers, carriers, fuel costs, and any other operational expenses linked to this forwarding order.
- **Financial Reconciliation** : Ensuring accurate recording of all monetary transactions. The settlement process ensures that all income and expenses are accurately recorded, reconciled, and the net amount (profit or loss) is determined. This step is crucial for financial reporting, budgeting, and financial management within the company.
- **Document Generation** : Creating invoices, credit memos, and purchase documents. As part of the settlement, invoices are generated for clients based on the determined charges, and payments are processed for any third-party services utilized during the transportation process.
- **Profit Analysis** : Calculating net profit or loss for each Forwarding Order.

## Key Components

### 1. Settlement Lines

Each settlement consists of multiple settlement lines, where each line represents either:

- **Income** : Services provided to customers (positive amounts)
- **Cost** : Expenses paid to vendors/suppliers (negative amounts)

#### Settlement Line Structure

- **Type** : Income or Cost
- **Code** : [Service](services.md) or [Charge](charges.md) code from master data
- **Description** : Human-readable description
- **Quantity** : Number of units (services)
- **Unit of Measure** : How the service/charge is measured
- **Price** : Unit price
- **Amount** : Total line amount
- **Currency** : Transaction currency
- **Customer/Vendor** : Associated business partner
- **Amount (ACY)** : Will be calculated automatically

### 2. Master Data Integration

#### Services (Income) Lines. Services define what you charge customers for

- **Code** : Unique service identifier
- **Description** : Service description
- **Unit of Measure** : How the service is billed
- **Invoice Line Type** : Maps to Business Central entities (G/L Account, Item, Resource, etc.)
- **Invoice Line No.** : Specific Business Central record

#### Charges (Cost) Lines. Charges define what you pay suppliers for

- **Code** : Unique charge identifier
- **Description** : Charge description
- **Unit of Measure** : How the charge is measured
- **Purchase Line Type** : Maps to Business Central purchase entities
- **Purchase Line No.** : Specific Business Central record
- **Default Vendor** : Default supplier for this charge

## Settlement Process Workflow

### Initial Setup

1. **Create Forwarding Order Type** : Forwarding order template
2. **Define Services** : Configure what services will be provided [details](services.md)
3. **Set Up Charges** : Define expected costs and suppliers [details](charges.md)

### Settlement Line Creation

#### Manual Entry

- Add settlement lines directly in the settlement subform
- Select appropriate Service or Charge codes
- Enter quantities, prices, and amounts
- Specify customer/vendor information

#### Automated Calculation

- **Distance-based** : Automatically calculate quantities based on transportation distance
- **Weight-based** : Calculate quantities based on cargo weight
- **Price List Integration** : Apply predefined pricing rules

### Cost Allocation

Link settlement cost lines to actual purchase documents:

- **Purchase Invoice Lines** : Allocate costs from purchase invoices
- **Posted Purchase Invoice Lines** : Link to already posted purchase invoices
- **Purchase Credit Memo Lines** : Handle cost corrections and refunds

### Document Generation

#### Sales Documents (Income)

- **Create Invoice** : Generate sales invoices for customers
- **Create Credit Memo** : Handle customer refunds and corrections
- **Add to Sales Invoice** : Add settlement lines to existing sales documents
- **Sync Income Lines** : Synchronize settlement changes with sales documents

#### Purchase Documents (Cost)

- **Create Purchase Invoice** : Generate purchase invoices for suppliers. The function is used when we issue a purchase invoice to ourselves on behalf of the carrier — i.e., the carrier is unable to issue the invoice, so we do it for them.
Normally, the carrier sends us an invoice, for example as a PDF, and we enter it into Business Central as a Purchase Invoice, then upload it to the Settlement of the corresponding Forwarding Order. In this case, however, the process is different: we create a Cost line in the Settlement and then generate a purchase invoice from there.
- **Link Purchase Lines** : Connect settlement lines to purchase documents

### Financial Reconciliation

- **Currency Conversion** : Handle multi-currency transactions
- **Exchange Rate Management** : Apply appropriate exchange rates
- **Amount Calculations** : Automatic calculation of totals and subtotals
- **Profit Analysis** : Calculate profit margins per order

## Key Features

### Multi-Currency Support

- Support for multiple currencies per settlement
- Automatic currency conversion using exchange rates to local currency and additional report currency (ACY)
- Additional reporting currency support

### Status Management

- Settlement availability controlled by order status [details](statuses.md)
- Different permissions for income vs. cost lines
- Status-based workflow enforcement

### Price List Integration

- Apply predefined pricing rules
- Automatic price calculation based on customer agreements
- Price list line tracking and management

### Document Linking

- Link settlement lines to actual Business Central documents (sales invoices and purchase invoices)
- Track document posting status
- Maintain audit trail of financial transactions

### Automated Calculations

- Distance-based quantity calculations
- Weight-based quantity calculations
- Automatic amount calculations
- Currency factor applications

## User Interface

### Forwarding Order Settlement section

The main interface for managing settlement lines includes

- **Type** : Income or Cost selection
- **Code** : Service/Charge code lookup
- **Description** : Line description
- **Quantity** : Number of units
- **Unit of Measure** : Measurement unit
- **Price** : Unit price
- **Currency Code** : Transaction currency
- **Amount** : Total line amount
- **Amount (LCY)** : Local currency amount
- **Account Name** : Customer/Vendor name
- **Document Type** : Linked document type
- **Document No.** : Linked document number

### Actions and Functions of the settlement subpage

- **Invoice Line > Credit Memo Line** : Add credit memo line in freight settlement based on the current income line information.
- **Calculate** : Recalculate quantities and amounts. Calculate service distance and weight quantities. Include all freight order charges to forwarding order

Invoicing. Functions for managing the process of billing customers for transportation services:

- **Create Invoice** : Generate customer invoices. Create a sales invoice for the customer. This function generates a sales invoice for the client specified in the Ordering Party, in the currency set by the order''s Currency Code field. All Income lines from the Settlement will be copied to the invoice, and if there is a currency difference, amounts will be recalculated to the invoice''s currency. The type of sales document line is determined by the TMS Service to BC items mapping settings.  The forwarding order must have a status that allows creates invoices. If a menu item is disabled, the action is not allowed for the current document status. Verify or change the order status or consult an administrator.
- **Create Credit Memo** : Generate customer credit memos. Create a sales credit memo for the customer. This function creates a credit note for the client specified in the Ordering Party, in the currency set by the order''s Currency Code field. All Income lines from the Settlement with a negative quantity will be copied to the invoice, and if there is a currency difference, amounts will be recalculated to the invoice''s currency. The type of sales document line is determined by the TMS Service to BC items mapping settings. The forwarding order must have a status that allows creates invoices. If a menu item is disabled, the action is not allowed for the current document status. Verify or change the order status or consult an administrator.
- **Add To Sales Invoice** : Add selected income lines to the another opened sales document (order or invoice).
- **Sync Income Lines** : This synchronization function transfers changes made in Income-type Settlement lines to the corresponding sales document lines (for example, sales invoices). Any new lines created in the Settlement will be automatically added to the sales document, ensuring that all Income-related adjustments are accurately reflected in the sales records. If a menu item is disabled, the action is not allowed for the current document status. Verify or change the order status or consult an administrator.
- **Create Purchase Invoice** : Generate supplier invoices. Create a purchase invoice. This function creates a purchase invoice for the vendor specified in the "Customer/Vendor Name" field. All Cost lines from the Settlement with a positive amount and the same vendor will be copied to the purchase invoice, and if there is a currency difference, amounts will be recalculated to the invoice''s currency. The type of purchase document line is determined by the mapping settings of the TMS Costs directory to BC items.  The forwarding order must have a status that allows creates invoices. If a menu item is disabled, the action is not allowed for the current document status. Verify or change the order status or consult an administrator.

Charge allocation. Functions for allocating transportation-related costs to this order:

- **Purchase Invoice Line** : This function allocates costs to the specified transportation. It links the selected settlement line of type Cost with an existing purchase invoice line, transferring values (quantity, amount, currency code) from the purchase invoice to the settlement line. The "Customer/Vendor Name" field must be filled to search for the purchase document.
- **Posted Purchase Invoice Line** : This function allocates costs to the specified transportation. It links the selected settlement line of type Cost with an existing posted purchase invoice line, transferring values (quantity, amount, currency code) from the posted purchase invoice to the settlement line. The "Customer/Vendor Name" field must be filled to search for the purchase document.
- **Purchase Credit-Memo Line** : This function allows for accounting corrections related to transportation costs. It links the selected settlement line of type Cost with an existing purchase credit note line, transferring values (quantity, amount, currency code) from the credit note to the settlement line. The "Customer/Vendor Name" field must be filled to search for the purchase document.
- **Delete Allocation** : Delete the charge allocation links to purchase documents.

Prices:

- **Get Prices** : Add new settlement income lines based on price list.
- **Show Price List** : Shows the current price list.

### Summary Information

- **Total Income (LCY)** : Sum of all income lines
- **Total Cost (LCY)** : Sum of all cost lines
- **Total Profit (LCY)** : Income minus costs

## Common Scenarios

### Standard Transportation Order

1. Create forwarding order
2. Add income lines for services provided
3. Add cost lines for expenses incurred
4. Generate customer invoice
5. Create purchase invoices for suppliers
6. Reconcile final amounts

### Multi-Stage Transportation

1. Set up transportation stages
2. Calculate distance-based services
3. Allocate costs per stage
4. Generate stage-specific invoices
5. Track profitability per stage

### International Shipment

1. Configure multi-currency settings
2. Set appropriate exchange rates
3. Handle currency conversions
4. Generate documents in relevant currencies
5. Reconcile currency differences

### Cost Allocation from Purchase Documents

1. Receive purchase invoices
2. Link invoice lines to settlement cost lines
3. Allocate costs to appropriate orders
4. Track cost allocation status
5. Generate supplier payments

## Troubleshooting

### Common Issues

1. **Settlement Disabled** : Check order status profile [details](statuses.md) or permissions
2. **Currency Errors** : Verify exchange rate settings
3. **Document Linking Issues** : Check document posting status
4. **Calculation Errors** : Verify quantity and price entries
5. **Permission Denied** : Confirm user access rights

### Solutions

1. **Status Management** : Update order status if needed
2. **Currency Setup** : Configure exchange rates properly
3. **Document Status** : Ensure documents are properly posted
4. **Data Validation** : Check all required fields
5. **User Permissions** : Grant appropriate access rights
