# GreenTech Inventory Management

## Client Requirements

### Inventory Management
- Ability to add new equipment to the inventory.
- Track the current status of each piece of equipment (Available, In Use, Maintenance, Retired).
- Generate a report of all equipment with their status.

### User Roles
- **Admin:** Can add, update, and delete equipment.
- **User:** Can only view the equipment and its status.

### Notifications
- Send an email notification to the Admin when equipment status changes to "Maintenance" or "Retired".

## Features and Functionalities

1. **Inventory Management:**
   - Ability to add new equipment.
   - Track and update the status of each piece of equipment.
   - Generate reports of all equipment with their current status.

2. **User Roles:**
   - **Admin:** 
     - Add new equipment.
     - Update equipment details.
     - Delete equipment.
   - **User:**
     - View equipment details and status.

3. **Notifications:**
   - Send email notifications to the Admin when the equipment status changes to "Maintenance" or "Retired."

## User Stories

1. **Admin Adding New Equipment:**
   - As an Admin, I want to be able to add new equipment to the inventory so that I can keep track of all equipment details and their statuses.

2. **User Viewing Equipment Status:**
   - As a User, I want to view the list of all equipment and their statuses so that I can know the current availability and condition of the equipment.

3. **Admin Receiving Notifications:**
   - As an Admin, I want to receive email notifications when equipment status changes to "Maintenance" or "Retired" so that I can take appropriate actions.

## Workflow Diagram

### Adding New Equipment and Status Change Notification

```plaintext
                     +---------------+
                     |  Admin Login  |
                     +-------+-------+
                             |
                             v
                     +---------------+
                     |  Add Equipment|
                     +-------+-------+
                             |
                             v
                     +---------------+
                     | Equipment Added|
                     +-------+-------+
                             |
                             v
                     +---------------+
                     |  Update Status|
                     +-------+-------+
                             |
             +---------------+---------------+
             |               |               |
             v               v               v
   +------------------+ +----------------+ +---------------+
   |Status: Available | |Status: In Use  | |Status: Retired|
   +------------------+ +----------------+ +---------------+
   |                      |                   |
   v                      v                   v
   +---------------+ +----------------+ +---------------+
   |   No Action   | |   No Action    | | Send Email to |
   |               | |                | |     Admin     |
   +---------------+ +----------------+ +---------------+
                                                |
                                                v
                                    +--------------------+
                                    | Email Notification |
                                    +--------------------+
