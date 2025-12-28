# Attachment Control

The Attachment Control Page is a comprehensive monitoring and analysis tool within the Transportation Management System that provides centralized oversight of document attachments across forwarding orders and posted documents.

This sophisticated page displays a consolidated view of all transportation documents (both draft and posted) with detailed attachment statistics, allowing users to track and analyze document completeness and compliance. The page features a dynamic column structure that can display up to 15 customizable attachment categories, each configured through the Attachments Selection to filter specific document types or categories.

The system automatically populates attachment counts for each document, showing both total attachments and category-specific counts, with drill-down capabilities that open detailed attachment views filtered by selected categories.

Users can configure which attachment categories to monitor through the "Settings" action, which opens the "Attachments Selections" page where administrators can define category filters and captions for up to 15 different attachment types.

The page includes comprehensive document information such as ordering party names, document dates, status codes, posting dates, and order types, making it an essential tool for compliance monitoring, document management, and quality control in transportation operations.

## Attachment Category

The Attachment Category is a simple master data entity within the Transportation Management System that provides a classification system for organizing and categorizing attachments and documents used throughout the TMS.
This entity serves as a lookup table with a basic two-field structure consisting of a unique code identifier and a descriptive text field.
The Attachment Category enables users to systematically classify various types of transportation-related documents such as shipping manifests, customs forms, delivery receipts, insurance certificates, and other logistics paperwork.

The system provides a straightforward list page interface that allows administrators to define and manage these categories, making it easier for users to select appropriate categories when attaching documents to the Forwarding Orders.

By implementing a standardized categorization system, the TMS ensures consistent document organization and improves the ability to locate and manage transportation-related attachments efficiently.

Attachment Categories are used in the advanced status setup to define the types of documents that must be attached at a specific stage of processing a Forwarding Order [details](statuses.md).

## Note

LSP scenario settings
