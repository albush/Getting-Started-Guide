

# Milestone 5:  Steady State

At milestone 5, we've reached the point where the customer is completely up and running on Rackspace. For many customers, this milestone occurs immediately after going live. For others, it's after one or more high traffic events. For others still, continually fluctuating traffic *is* steady state. Whenever this milestone occurs for you, there are some additional actions we recommend taking to make sure everything runs smoothly for you for as long as you are at Rackspace.

## Scaling back after a high traffic event

If you've just completed a high traffic event - congratulations! Hopefully everything went well. Likely you'll not need to continue on with the expanded infrastructure you've built for to accommodate the enhanced traffic; if you do, then you've just had a very successful event. If you've followed our [guides for scaling up](https://community.rackspace.com/products/f/54/t/1009), you can follow them in reverse to scale back down. We recommend staggering the scale down, so that you don't scale your app too low to handle your traffic. Begin by draining connections from one of the servers behind your load balancer at a time. When all connections are gone, you can remove that node, and delete the server. Test to see that your traffic is keeping up, and repeat until your architecture meets traffic demand.

If you run into any issues, don't hesitate to contact support.

## Steady state maintenance

After the relative chaos of migrating, launching, and a possible high traffic event, the steady state is a great time to do a bit of maintenance to make sure your projects are set up for success going forward. Your Launch Manager team can walk you through these items we've included below.

### Account and contact management  

Help us stay in touch when you need support by keeping your contacts up to date. We won't use them to send marketing email, we'll just use them to contact the right people to get you the support you need.


### Benchmarking

Benchmarking early allows you to understand how your site grows over time. Single high traffic events will drive rapid capacity changes, and organic growth will drive a more slow and steady capacity change. Take some time to establish a baseline from which you can continue to monitor and plan capacity moving forward.

### Fire Drills

All of the planing in the world is just a hunch unless you test it. Take some time to plan and execute a "Fire Drill" to see just how well you can react to a disruption to your application.  Whether it's an emergency reboot, or a host machine failure, any cloud application is susceptible to  

<!-- Hide this in the print version <iframe src="http://www.slideshare.net/AndrewDrewCox/slideshelf" width="760px" height="570px" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:none;" allowfullscreen webkitallowfullscreen mozallowfullscreen></iframe> -->
