# BasicWebApp

Prerequisites:
Visual Studio Community 2015
SQL Server 2016 Service Developer
Microsoft SQL Server Management Studio

(Steps 7-8 may not be needed, but installing Entity Framework likes to be a bit strange sometimes)

1. Open SQL Server Management Studio and connect to either (localdb)\V11.0 or (localdb)\MSSQLLocalDB.
2. Create a new database.
3. Open Visual Studio 2015 running as administrator and open and build the solution.
4. Connect to new database in the server explorer window. Connect to the same server used in step 1 and choose the database created in step 2.
5. Copy the connection string in the properties window of the new connection.
6. Replace the connection string in Web.Config with the one copied.
7. Open the Package manager window and type:
    Uninstall-Package EntityFramework -Force
8. Restart visual studio when prompted, then in the package manager console again type:
    Install-Package EntityFramework
9. Once that is complete type:
Update-Database

The database should be accessible from SQL Server Management Studio.

The application was developed using a local IIS instance.