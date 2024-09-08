# Appointment Management System

The Appointment Management System is a web application developed using ASP .NET Core MVC, aimed at streamlining the scheduling and management of appointments.

## Key Features

- **User Authentication:** Secure login and account creation for administrators and customers, with password recovery functionality.
- **Appointment Management:** Schedule, modify, and delete appointments, with automatic removal of expired appointments and archiving of past appointments.
- **User Roles:** Administrators have full system access, while customers have restricted access tailored to their appointment-related needs.
- **Automated SMS Notifications:** Real-time updates for appointment activities, with logs maintained in a text file for tracking purposes.
- **System Administration:** CRUD functionality for user and appointment management, including the ability to create additional administrator accounts. 

## Technologies Used

- ASP .NET Core MVC
- Relational Database Management
- Automated SMS Notification Integration

## Usage

1. Clone the repository to your local machine.
2. Ensure ASP .NET Core MVC is installed.
3. Set up the database according to the provided schema.
4. Run the application and navigate to the appropriate URLs for admin or customer functionalities.

## Assumptions Made

- Application runs off of local system time (this impacts the auto-deletion of expired appointments).
- SMS is sent to a text file `SmsLog.txt` in the project directory.

## Start-up guide

Upon downloading the application, you will need to run two commands within the Package Manager Console:

- `update-database -Context AccountDbContext`
- `update-database -Context AppointmentDbContext`

After doing this, the application should open without issue. There are some initial accounts seeded into the database upon initialization.

**Admin account**
- Email: admin@admin.com
- Password: Secure@1

**User accounts**
1. - Email: test@test.com
   - Password: Secure@2
