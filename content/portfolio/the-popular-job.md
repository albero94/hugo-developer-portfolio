+++
categories = ["web-dev"]
coders = []
date = 2020-08-10T23:00:00Z
description = "A job search portal for working holiday visas in Australia"
github = [""]
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

[ThePouparJob](https://thepopularjob.com)

This web application was developed by me after having multiple conversations with two friends, one of them living in Australia, and thinking it could be a good business opportunity. Many working holiday visa holders use the common job portals such as LinkedIn, Indeed, Seek to look for jobs. We thought that having a portal that focuses on working holiday visas as well as providing them with useful information would be very valuable.

We started having constant meetings to develop the idea, study our rivals, thinking how we could monetize the portal, etc. We also created social media platforms to start marketing the company. With COVID still very active in 2020, we have postponed the "official launch" of the service, as working holiday visas has been suspended. This will also give me time to keep working on the application as it is not ready yet.

Right now the GitHub repo is private, but if you are interested I could show you pieces of the code.

## Application Architecture
The main application is divided into two parts right now. One part is crawling jobs from the main job portals (Indeed, Seek, Jora...) and other backpacker jobs websites we found. The other part, is the MVC website you see when you navigate to the [URL](https://thepopularjob.com). Both of these projects connect to the same PostgreSQL database hosted in an Ubuntu VM in Digital Ocean. ThePopularJob project is also hosted in Digital Ocean and secured through HTTPS. I also created a JobsLibrary project to hold the common classes between the other two.

There is also a WordPress website that we call the [Blog](http://blog.thepopularjob.com/), where we are including general information about working holiday visas. We decided to do this part in WordPress so that the other non-technical team members can also participate in the development of the site and add valuable information.

### Jobs Library

### Web Crawler

### ThePopularJob


