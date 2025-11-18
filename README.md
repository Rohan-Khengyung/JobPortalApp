# Job Portal Web Application

This Job Portal is a dynamic online platform developed with ASP.NET MVC, serving as a central hub for job seekers and employers. It is designed to make the job search and hiring process more efficient and effective for both parties.

## Key Features

- **User Roles:** The application supports two primary user roles, "Job Seekers" and "Employers," each with distinct features and capabilities.

- **Job Listings:** Job seekers can browse and search through a comprehensive list of job vacancies posted by various employers. The listings can be filtered by categories, locations, and other criteria.

- **Application Process:** Job seekers can seamlessly apply for jobs by submitting their resumes and cover letters, while employers can review applications, contact applicants, and schedule interviews.

- **User Profiles:** Both job seekers and employers can create and manage detailed profiles, including personal information, work experience, and educational backgrounds.

- **Secure Authentication:** The application implements user registration and authentication to ensure data and account security.

- **Responsive Design:** The web application is designed to be responsive, ensuring a seamless experience on various devices, including desktops, tablets, and smartphones.

## Project Goals
- Simplify and improve the job hunting and recruitment workflow.
- Offer an intuitive and easy-to-use interface.
- Foster better communication and connections between candidates and companies.
- Provide a reliable and secure environment for all job-related activities.


## Restoring the Database from a .bak File

This project uses a SQL Server database, and to get started, you'll need to restore the database from a .bak (backup) file. Follow these steps:

1. **Obtain the .bak File:**
   - Ensure you have a copy of the .bak file for this database. If you don't have it, please contact the administrator or owner of the database.

2. **Launch SQL Server Management Studio (SSMS):**
   - Open SQL Server Management Studio, a graphical tool for managing SQL Server databases. If you don't have SSMS installed, you can download it from [Microsoft's website](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms).

3. **Connect to SQL Server:**
   - Open SSMS and connect to your SQL Server instance where you want to restore the database. Ensure you have the necessary permissions to perform this operation.

4. **Restore the Database:**
   - In SSMS, in the Object Explorer, right-click on "Databases."
   - Choose "Restore Database."

5. **Specify Source and Destination:**
   - In the "General" section, select "Device" as the source.
   - Click the "..." button to browse for the .bak file.
   - Select your .bak backup file.
   - In the "To database" field, specify the name of the database you want to create or overwrite with the backup data.

6. **Restore Options (Optional):**
   - You can configure various options such as overwriting existing database files, specifying a new location for database files, or enabling options like "Overwrite the existing database." Adjust these options based on your requirements.

7. **Review and Confirm:**
   - Review the settings on the "General" page and make sure they are configured as desired.

8. **Initiate the Restore:**
   - Click the "OK" button to start the database restore process. The progress will be displayed.

9. **Confirmation:**
   - Once the process is complete, you should see a success message. The restored database is now available for use.

Please ensure that you have the necessary permissions to restore databases, and be cautious when restoring databases as it can overwrite existing data. Make sure to back up any data you want to preserve before performing the restore operation.

For command-line users, you can also use `sqlcmd` to restore the database. Here's an example command:

```bash
sqlcmd -S ServerName -U Username -P Password -Q "RESTORE DATABASE [YourDatabaseName] FROM DISK = 'C:\Path\To\YourDatabase.bak' WITH REPLACE;"
