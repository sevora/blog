---
title: "AWS is Actually Amazing!"
---

I've been out for a while but I've always been learning. For this post I have a particular
topic in mind. Let's talk about deployment solutions.

As a beginner, I used services that made it very easy to deploy my Express backend, and then another service to get the React frontend out there. Pretty much services like Heroku, Vercel, and Render. These things are cool and easy to setup. So easy in fact you just have to link your Github account and choose the repository you want to deploy.

But one of their downsides is cost. As in the amount you pay for their service. Heroku had a free-tier and it was decent. Also the fact that the application spins down when not in usage was a downside as it takes a longer time to load up once more on the next visit.

Enter AWS or Amazon Web Services. It's way more complex to get started with and use and you'll probably have to learn a lot of things before you deploy something properly. One of the reasons why I can appreciate now is because I finished a Networking Course and a Cloud Computing Course which really filled in the gaps of knowledge and experience in using something like AWS.

## The Cara App Disaster (Vercel)
[Here's a link](https://www.reddit.com/r/nextjs/comments/1da4yzf/cara_grow_from_40k_to_650k_user_and_get_96k_wk/) to a costing disaster. Having heard of this story where an app that had a sudden growth in the number of users and their bill from Vercel reached $96,000 a week was alarming.

People kept pointing out how there's more cost-effective solutions and even just using AWS on its own was a good idea. I remember someone saying that they could have just hired engineers who could set up the infrastructure in AWS and it would be way way way cheaper than what they have now.

I guess this is one of my motivations for learning AWS.

## Plug-and-Play vs Do-It-Yourself
Heroku, and similar services, do offer a lot of control and then they handle everything else. The controls there are more tailored for someone who only cares about running their application. You don't have to worry about networking much.

Meanwhile, AWS is basically turning literal hardware components into digital components or services that do the same thing but on-demand. It's like you can get routers but digitally and you hook them up on your own. For example, you have to properly configure your own VPC (Virtual Private Cloud) as mostly a prerequisite.

Then you have to properly connect these components and resources too. You get an EC2 (a virtual machine) but you can think of it as getting a computer where you could run things like you do in your local environment. Then you would want to connect it to a load balancer, maybe an Application Load Balancer (ALB). Then also, it may be a good idea to connect that ALB to a Cloudfront distribution. Don't forget to get a domain from Route53 and configure your DNS properly so it points to the aforementioned Cloudfront distribution.

If you're able to successfully set all that up, then you have a reliable and relatively secure web server running already on the cloud. The cost? It's basically up to the demand but honestly it's going to cost less than using services like Vercel, Heroku, and Render.

For me, it was a thrill learning something new and being able to properly set up an infrastructure in AWS. 

## But it's not all easy
You do have to be careful with AWS and you pretty much have to be mindful and in the headspace especially when configuring things. Everything has a cost. You're basically the person balancing the costs and performance that you need. I could only immerse myself fully because I had time to finish a Networking Course and a Cloud Computing Course which are basically important before you dive in any service like AWS.