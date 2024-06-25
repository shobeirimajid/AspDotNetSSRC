# Displaying SSRS Reports in ASP.NET Core MVC Web Applications

Embed **SSRS** (SQL Server Reporting Services) report into **MVC Web App**.

**ReportViewer** is a server control and **server controls** were generally designed with **web forms**
 
Microsoft package **"Microsoft.Reporting.WebForm"** is a solution for utilizing the **ReportViewer** Control in a Web Forms.

Unfortunately, **ASP.NET MVC** does not support Web Forms, so ReportViewer control is not going to work there.

With absents of "Microsoft.Reporting.WebForm" in ASP.NET MVC, displaying SSRS reports in **ASP.NET MVC** Web App is a challenging topic for many developers. 

Microsoft has not release **SSRS viewer** for **ASP.NET MVC** yet. We hope, Microsoft support web forms for **ASP.NET MVC** and integrate **SSRS** report into **ASP.NET MVC** web app in the future.

# Solutions

  2. Two Co-Existing Web-Frameworks (web form project along with MVC project)
     Mixing **ASP.NET MVC** project with **ASP.NET Web Forms** project
     Web Forms project is for utilizing the **Report Viewer** control
      
  4. render an RDLC (Client Report Definition File) directly in a MVC project

     - https://weblogs.asp.net/rajbk/Contents/Item/Display/331

      Part-1
     - https://www.codemag.com/article/1009061
       
      Part-2
     - https://www.codemag.com/article/1011131/Incorporating-ASP.NET-MVC-and-SQL-Server-Reporting-Services-Part-2

     


# Community Packages

  1- https://github.com/alanjuden/MvcReportViewer (ASP.NET Core support)

  2- https://github.com/ilich/MvcReportViewer
    
This package does not work with asp.net core. 
It internally hosts the webform control and calls it’s render. 
As **webform controls** are not supported on **.netcore** this will not work.
To host type the SSRS control, you need a **.net framework 4.x** website.
The **asp .net core** site can use an **iframe** or **link to the SSRS** site.

It should be possible to update the MvcReportViewer to proxy a call to the SSRS site instead of hosting the actual control.

  3- [ReportViewerForMVC](https://github.com/chasoliveira/ReportViewerForMvc)

     https://www.nuget.org/packages/Chaso.ReportViewerForMvc/
     
     .NET Framework 4.6.1


# References

  - https://stackoverflow.com/questions/7691328/asp-net-mvc-ssrs-embeded-report
  - 

  - https://github.com/dotnet/aspnetcore/issues/1528

  - https://learn.microsoft.com/en-us/answers/questions/1365398/how-to-integrate-ssrs-in-asp-net-core-mvc

# .Net Reading List

https://www.codemag.com/magazine/allissues

https://marketplace.visualstudio.com/search?term=services&target=VS&category=All%20categories&vsVersion=&sortBy=Relevance


