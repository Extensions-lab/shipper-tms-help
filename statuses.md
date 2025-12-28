# Statuses

The status system is a core tool for managing and controlling transportation processes. It defines the set of steps a transportation request goes through within a company—from initial request approval, document preparation, coordination, approval, profit calculation, to cost collection from third-party providers (such as carriers), and more. These are not statuses of the physical movement of goods, but rather statuses of the overall process—from request to final invoicing.

The list of statuses, along with the rules defining what actions are allowed or restricted at each stage for a specific type of Forwarding Order, is called a status profile.

A status profile is a structured set of statuses that a forwarding and transportation order goes through during its lifecycle within the business process. This profile determines which operations are permitted and what restrictions apply to the document in each specific status.

Such a configuration ensures systematic progress and control over the document's state within the workflow.

## How TMS uses the status system

The status system is utilized for document types such as Forwarding Orders and Freight Orders. Different types of documents may have diverse status structures, allowing for more flexible configuration of the document processing business process.

![Statuses Image](resources/statuses/pics/statuses1.png)

## Where to find

using main menu of the TMS

![Setup Image](resources/statuses/pics/statuses2.png)

using search

![Setup Image](resources/statuses/pics/statuses3.png)

## Main Fields

- Code. Unique identifier of the status profile that will be used in the Forwarding Order Types.
- Description. Name of the status profile.
- Action Control System. Displays whether the system for monitoring specific actions is activated at each status.
- Enhanced system for monitoring additional actions that the system can control for documents with a selected status.
- Color highlighting of the document in the list for documents having this status.

![Setup Image](resources/statuses/pics/statuses4.png)

- "Action Control System" parameter allows for the authorization or prohibition of actions that can be performed with documents having a selected status. This facilitates the organization of workflow and the orderly processing of documents, as well as synchronizing the efforts of individuals working simultaneously on the same document. Works only for Forwarding Orders.

![Setup Image](resources/statuses/pics/statuses5.png)

You can activate verification by setting a flag in the field of the corresponding column. Determine whether an order can be posted, whether an invoice can be issued, and whether copying or modifying a document with the given status is allowed.

### Action Control Description for Statuses

- **Change Order Type** : Specifies if the user can switch the order type at this status.
- **Shipper/Consignee Change** : Specifies if shipper or consignee details can be edited when the order is at this status.
- **Lines Change** : Specifies if lines (content of the Forwarding Order) can be added, removed, or modified at this status.
- **Date Planning** : Specifies if planning dates can be changed for an order at this status.
- **Rount Planning** : Specifies if the route (stages) can be adjusted at this status.
- **Delete Document** : Specifies if the order can be fully deleted at this status.
- **Logistic Units Build** : Specifies if logistic units can be built or assembled at this status.
- **Create Freight Order** : Specifies if a freight order can be created from the forwarding order at this status. This means that the system allows you to assign a performer (carrier) to the stages of a Forwarding Order—that is, the party who will actually carry out the transportation.
- **Invoicing** : Specifies if the order can be invoiced at this status.
- **Settlement Document Posted** : Specifies if all documents in the settlement must be posted at this status. Requires that all documents in the Settlement (customer invoices and invoices from carriers/service providers) are posted before the Forwarding Order can be moved to this status [details](settlement.md).
- **Settlement Posting Date Control** : Specifies if the settlement posting dates must be earlier than the forwarding order's posting date to move Forwarding Order at this status.
- **Post** : Specifies if the order can be posted at this status.
- **Copy** : Specifies if data can be copied from or to another order at this status.
- **Settlement** : Specifies if settlement lines can be added at this status [details](settlement.md).
- **Settlement Invoice Lines** : Specifies if invoice settlement lines can be created at this status.
- **Settlement Cost Lines** : Specifies if cost settlement lines can be created at this status.
- **Line Style** : Specifies the visual style used to display or highlight documents in Forwarding Order Lisp page at this status.
- **Extended Control** : Specifies if additional document controls or attachments are enforced at this status [details](attachmentcontrol.md).

![Setup Image](resources/statuses/pics/statuses6.png)

## Extended Control for Statuses

Extended Control for a status allows you to enhance the requirements for transitioning to that status. It enables the creation of a document control system (attachments) that must be present in the transportation process for the order to move to the selected status.

To activate this control, you can define the types of attachments that must be uploaded to the document—for example, before it can be posted. In other words, you set rules requiring that, at a certain status, specific documents (such as MAWB, Invoice, Delivery Note, etc.) must be attached in the system [details](attachmentcontrol.md).

## Additional

To ensure the action control system functions, it must be activated globally in the TMS Setup page.

![Setup Image](resources/statuses/pics/statuses7.png)

## Prerequisites

To change or create status profiles user must have TMS Admin or Super Permissions.
