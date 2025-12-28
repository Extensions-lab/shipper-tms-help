# Time Slots

## Overview

Time Slots in the TMS system provide a structured approach to scheduling transportation activities by defining specific time windows for loading and unloading operations. This functionality enables precise scheduling, resource optimization, and better coordination between shippers, carriers, and consignees.

The Time Slot functionality provides TMS users with powerful scheduling capabilities that enhance operational efficiency and customer satisfaction through precise time window management.

## Benefits

- Standardization: Consistent time window definitions across the organization
- Customer Service: Align deliveries with customer availability preferences
- Resource Planning: Optimize warehouse and transportation resource utilization
- Automation: Reduce manual scheduling errors through predefined time windows
- Flexibility: Support different scheduling patterns for different customer types or locations

## Settings

### Time Slot Profiles

Time Slot Profiles serve as templates that group related time slots together. Each profile contains:

- **Code**: Unique identifier for the profile
- **Description**: Brief description of the profile's purpose (e.g., "Morning Deliveries", "Weekend Pickups")
- **Slots**: Automatically calculated count of time slot lines within the profile

### Time Slot Profile Lines

These define the actual time windows within each profile:

- **No.**: Unique identifier within the profile
- **Description**: Description of the specific time slot
- **Time Start**: Beginning time of the slot
- **Time End**: Ending time of the slot

## Integration with TMS Operations

### Transport Request Scheduling

Time Slot Profiles are extensively used in Transport Requests for:

- **Load Time Slot Profile Code**: Defines available loading windows at pickup locations
- **Unload Time Slot Profile Code**: Defines available unloading windows at delivery locations

### Delivery Order Management

In Delivery Orders, time slots are used to:

- Schedule specific delivery times for each stop
- Provide assist edit functionality for selecting from predefined time windows
- Ensure deliveries align with customer availability

### Customer and Vendor Integration

Time Slot Profiles can be assigned to:

- **Customers**: "Time Slot Profile" sets the customer's working hours schedule during which deliveries can be made. Default delivery time preferences are set via the "Default Time Slot" field.
- **Vendors**: "Time Slot Profile" sets the supplier's working hours schedule during which deliveries for loading can be made. Default pickup time preferences are set via the "Default Time Slot" field.
- **Locations**: Default "Time Slot Profile" sets the warehouse's operating hours schedule.
- **Order/Ship-to Addresses**: Specific address-level scheduling preferences are set via "Time Slot Profile" and "Default Time Slot" fields.

## How to Use Time Slots

### 1. Setting Up Time Slot Profiles

- Navigate to Time Slot Profiles from the TMS Role Center
- Create a new profile with a descriptive code and description
- Add time slot lines defining specific time windows

### 2. Assign the Profile to Relevant Customers, Vendors, or Locations

### 3. Using Time Slots in Transport Requests

When creating a Transport Request:

- Select appropriate Load and Unload Time Slot Profile fields
- Use the assist edit button on date/time fields to select from available time slots
- The system will automatically populate the date/time based on the selected time slot

### 4. Delivery Scheduling

- In Delivery Orders, use the assist edit functionality on "Scheduled Date and Time" fields
- Select from available time slots based on the assigned Time Slot Profile

The system automatically calculates estimated arrival times considering transportation duration.

