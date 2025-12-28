# Check List

The Check List entity is a comprehensive task management and quality control system within the Transportation Management System that enables Logistics Service Providers (LSPs) to define, track, and monitor completion of standardized operational tasks associated with forwarding orders.

This system consists of configurable checklist templates that can be customized for different operational scenarios, ensuring consistent process execution and compliance with transportation procedures.

The Check List functionality operates through a two-tier structure: Check List Settings serves as the master configuration where administrators define reusable checklist templates with sequential task descriptions, while Check List Line represents the actual execution instance linked to specific forwarding orders.

Users can mark tasks as completed, add comments, and track completion status with automatic timestamping and user identification. The system provides multiple interface options including a full checklist page for comprehensive task management, a sub-page for quick status overview, and specialized pages for posted forwarding orders to maintain historical task completion records.

This ensures operational transparency, quality assurance, and audit trail maintenance throughout the transportation workflow, enabling organizations to standardize processes, reduce errors, and maintain consistent service delivery standards across all forwarding operations.

## Check List Setup Process

The check list setup is configured at the "Forwarding Order Type" level through the "Check List Settings" page, which can be accessed via:
Forwarding Order Type page → "Check List Setup" action. Each Forwarding Order Type can have its own checklist template.

Step 1: Template Configuration
In the "Check List Settings" page checklist items are defined with:

- Order (sequence number)
- Description (task description)

## How Check List Works

When creating a new forwarding order, checklist items are automatically created from the template
When a new Forwarding Order is created, the system automatically:

- Validates the "Forwarding Order Type"
- Creates checklist items from the template for created FWO.

Users mark items as done and add comments. Check List does not depend on the status system..

### Technical Details

The setup uses two main tables:

- **Check List Settings" table** : stores the check list template configuration for [Forwarding Order Type](forwardingordertype.md).
