# Driver

The Driver entity is a comprehensive master data table in the Transportation Management System (TMS) that manages complete driver profiles for transportation operations.
It contains extensive driver information including:

- personal details (names, birth date, employment date)
- contact information (phone numbers, email, emergency contacts)
- professional qualifications (license details, categories, expiration dates), compliance certifications (medical cards, ADR for dangerous goods), - operational settings (carrier association, default vehicle assignment, fuel card, scheduler preferences).

The entity supports mobile integration through Proof of Delivery (PoD) app credentials and includes photo management capabilities with camera integration. It features a comprehensive card page with organized sections for all driver data, a list page for browsing and selection, and a dedicated picture management page part.

The Driver entity serves as the central repository for driver-related information, enabling effective driver assignment, scheduling, compliance tracking, and operational management within the TMS while ensuring regulatory compliance and supporting mobile workforce operations.

This directory allows you to store information not only about your own drivers but also to register drivers from third-party carriers if needed.

## Field description

- **No.** :  Unique identifier for the driver in TMS
- **Name** :  Short name or label for the driver, shown on TMS documents
- **Full Name** : Driver's complete name for official references in TMS
- **First Name** : Driver's given name for detailed TMS identification
- **Last Name** : Driver's family name used for TMS records or official documents
- **Middle Name** : Additional name if needed for complete driver identification

Personal Information:

- **Birth Date** : Driver's date of birth, often required for HR or compliance
- **Employment Date** :  When the driver started working for the organization

Carrier Association:

- **Carrier No.** :  Which carrier the driver is associated with for TMS tasks.
- **Carrier Name** : Name of the carrier linked to this driver (auto-populated)

Vehicle Assignment:

- **Default Vehicle No.** : Vehicle number the driver typically operates in TMS. This field can be filled in so that when a driver is selected in the Delivery Order, the vehicle is automatically selected.
- **Default Vehicle Name** : Name or label for the driver's main vehicle resource (auto-populated)

Contact Information:

- **Phone No.** : Driver's primary phone contact for scheduling or emergencies
- **Phone No. 2** :  Alternative phone contact if the driver has another line
- **E-Mail** : Driver's email address for official communication

License Information:

- **License No.** : Driver's official license ID used for compliance checks
- **License Categories** : Driver's permitted vehicle categories (e.g., A, B, C) for TMS routes
- **License Start Date** : When the driver's license validity begins
- **License Exp. Date** : When the driver's license expires and needs renewal
- **License State** : Which state or region issued the driver's license

Operational Status:

- **Blocked** : Indicates whether this driver cannot be assigned to new shipments

Medical Compliance:

- **Medical Card Number** : Driver's medical card ID if required by law
- **Medical Card Expiration** : When the driver's medical card becomes invalid

Dangerous Goods Certification:

- **ADR No.** : ADR certificate number if the driver handles dangerous goods
- **ADR Expiration Date** : When the ADR certificate is no longer valid for dangerous cargo

Emergency Information:

- **Emergency Contact** : Whom to contact for emergencies involving this driver

Fuel Management:

- **Fuel Card No.** : Assigned fuel card number for this driver if relevant

Proof-of Delivery (POD) Mobile App Integration:

- **PoD User E-mail** : Driver's email used to log in to the Proof of Delivery application. This field links an organization’s user, who may not necessarily have access to Business Central, with a driver’s card. As a result, when the user logs into the mobile Power App (Proof-Of-Delivery), they will only see Delivery Orders assigned to that specific driver.
- **PoD User Full Name** : Name displayed for the driver's PoD user account in TMS

Visual Identification:

- **Picture** : Stored photograph for driver identification within TMS. Foto in FactBox.

Scheduling Management:

- **Scheduler Sort Order** : Numeric priority for this driver in the TMS scheduler view
- **Block for Scheduling** : Indicates if this driver is restricted from scheduling due to maintenance or downtime

Audit Trail:

- **Last Modified Date Time** : When this driver record was last updated for traceability
- **Last Modified Date Time (UTC)** : Timestamp of the latest update in Coordinated Universal Time
- **Last Modified UserID** : User who performed the most recent modification to this record
