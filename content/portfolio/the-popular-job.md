+++
categories = ["web-dev"]
coders = []
date = 2020-08-10T23:00:00Z
description = "A job search portal for working holiday visas in Australia"
github = ["https://github.com/albero94/aw-work-and-holiday"]
image = "https://res.cloudinary.com/aalbero/image/upload/v1597411391/logo_150x150_fn9jl3.jpg"
title = "The Popular Job"
type = "post"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260162/.net_core_pxrqly.png"
name = ".NET Core"
url = "https://dotnet.microsoft.com/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597260164/C_Sharp_logo_yagaj2.svg"
name = "C#"
url = "https://docs.microsoft.com/en-us/dotnet/csharp/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597411455/digital-ocean_eog0p0.png"
name = "Digital Ocean"
url = "https://www.digitalocean.com/"
[[tech]]
logo = "https://res.cloudinary.com/aalbero/image/upload/v1597329684/postgres_qpe92s.png"
name = "PostgreSQL"
url = "https://www.postgresql.org/"

+++
## Description

[ThePopularJob](https://thepopularjob.com)

This web application was developed by me after having multiple conversations with two friends, one of them living in Australia, and thinking it could be a good business opportunity. Many working holiday visa holders use the common job portals such as LinkedIn, Indeed, Seek to look for jobs. We thought that having a portal that focuses on working holiday visas as well as providing them with useful information would be very valuable.

We started having constant meetings to develop the idea, study our rivals, thinking how we could monetize the portal, etc. We also created social media platforms to start marketing the company. With the coronavirus still very active in 2020, we have postponed the "official launch" of the service, as working holiday visas has been suspended. This will also give me time to keep working on the application as it is not ready yet.

Right now the GitHub repo is private, but if you are interested I could show you pieces of the code.

## Application Structure
The main application is divided into two parts right now. One part is scraping jobs from the main job portals (Indeed, Seek, Jora...) and other backpacker jobs websites we found. The other part, is the MVC website you see when you navigate to the [URL](https://thepopularjob.com). Both of these projects connect to the same PostgreSQL database hosted in an Ubuntu VM in Digital Ocean. ThePopularJob project is also hosted in Digital Ocean and secured through HTTPS. I also created a JobsLibrary project to hold the common classes between the other two.

There is also a WordPress website that we call the [Blog](http://blog.thepopularjob.com/), where we are including general information about working holiday visas. We decided to do this part in WordPress so that the other non-technical team members can also participate in the development of the site and add valuable information.

### Jobs Library
Contains the common classes used for both the web application and the web scraper. It also contains the database repository classes and the migrations. 

There is a test project used for unit testing the methods of these classes.

### Web Scraper
This application is used to download jobs from different job portals. There is a base Scraper class that downloads the page of a given URL, if the page contains jobs it extracts the data, it iterates through the different pages of that job search and finally stores all the downloaded jobs in the database.

There are up to 7 classes that extend the base class to implement the details of extracting the job information of the page. I have done this using AngleSharp, a C# library to query the DOM as if you are using JavaScript.

I also created a ScraperFactory class that is used in the Startup class of the project. Depending on which job portal we want to download, the factory class will receive the name of the portal and create the corresponding scraper object. The Run mehtod is later called on this object and the right jobs are downloaded to the databse.

### ThePopularJob
The main application, built following the MVC pattern. It retrieves the jobs from the database and presents them to the users, you also have the ability to query these jobs. It can also handle user information, so users can create an account and login. I am on the process of creating a job posting form and job posting admin page so that companies that are registered are able to create new job postings.


