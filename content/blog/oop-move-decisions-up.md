---
title: "OOP - Control vs Implementation"
date: 2020-04-10T12:14:34+06:00
image: "https://res.cloudinary.com/aalbero/image/upload/v1597260175/raspberry-pi_zfsn48.svg"
description: "Move decisions up to control and responsibilities down"
author: "Alvaro Albero"
type: "post"
---
[See original post in my LinkedIn](https://www.linkedin.com/posts/alvaro-albero-gran-416554128_oop-cleancode-activity-6656555977778835456-QJsf)

One of my classes at GW this semester is Object Oriented Design, I'm studying today for the exam (even though is open book because we are having remote classes) and I came across the following sentence "move decisions up to control and responsibilities down as far as possible".

I had seen this in some controller classes or SQL stored procedures in a legacy system I worked with, where everything was in the same file, sometimes extending to thousands of lines. But also in a smaller project.

I remembered a conversation I had with Sean McBride during our distributed systems chord project. At some point during the implementation of the algorithm we had some errors and we were debugging the program. Then I mentioned, "how can we fix this if I cannot even see the algorithm in all these lines". All the code necessary to handle errors, gRPC calls, etc. hid the code that was implementing the algorithm of the paper and it was hard to follow.

Moving control decisions up and responsibilities down would help in both cases. Keep the control class as minimal as possible, extract code to other functions or classes, you just want control flow, not implementation. You would be able to have a readable class, that gives you a clear high-level idea of what's going on.

