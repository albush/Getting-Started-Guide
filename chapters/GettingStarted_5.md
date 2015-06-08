
# Milestone 5:  Steady State

At milestone 5, we've reached the point where the customer is completely up and running on Rackspace. For many customers, this milestone occurs immediately after going live. For others, it's after one or more high traffic events. For others still, continually fluctuating traffic *is* steady state. Whenever this milestone occurs for you, there are some additional actions we recommend taking to make sure everything runs smoothly for you for as long as you are at Rackspace.

## Steady state maintenance

After the relative chaos of migrating, launching, and a possible high traffic event, the steady state is a great time to do a bit of maintenance to make sure your projects are set up for success going forward. Your Launch Manager team can walk you through these items we've included below.

### Account and contact management  

Help us stay in touch when you need support by keeping your contacts up to date. We won't use them to send marketing email, we'll just use them to contact the right people to get you the support you need.

* [Help us help you get the most out of your support interactions](https://community.rackspace.com/general/f/34/t/4677)
* [Give additional team members access](https://community.rackspace.com/products/f/54/t/4551)
* Give those additional team members the correct [roles](https://community.rackspace.com/general/f/34/t/59) and [access](https://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac)


### Benchmarking

Benchmarking early allows you to understand how your site grows over time. Single high traffic events will drive rapid capacity changes, and organic growth will drive a more slow and steady capacity change. Take some time to establish a baseline from which you can continue to monitor and plan capacity moving forward. Take a look at this discussion on [benchmarking best practices](https://youtu.be/zhi8E15_yEQ).

### Manage images and backups

Daily images probably aren't needed anymore. Daily images are great for hedging against rapid changes to your OS configuration, but once you've hit a steady state, daily images likely won't catch anything new, and are therefore a waste of space (and money). At this point we recommend creating one "golden" image, and keeping that for scaling and recovery.

Do you have the backups you need? If you had to build from scratch, using only your latest backup, how much data would you lose? Would that amount of data loss be acceptable? Do your backups cover everything you need to backup? Are you backing up too much, and wasting time, space, and money by doing so?  
These are tough questions that you have to ask yourself. We recommend taking the time to go over all of these questions so that you can best recover in the event of an issue.

Again, we recommend using a combination of [server images](http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image), file-level [differential backups](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-create-a-backup-0), and [configuration management](https://developer.rackspace.com/blog/devops-automation-series-images-vs-config-management/) to achieve a robust, comprehensive [backup strategy](http://www.rackspace.com/blog/backup-strategies-for-cloud-web-apps-google-hangout-recap/).

### Fire Drills

All of the planing in the world is just a hunch unless you test it. Take some time to plan and execute a "Fire Drill" to see just how well you can react to a disruption to your application.  Whether it's an emergency reboot, or a host machine failure, any cloud application is susceptible to disruption. Taking some time now to reduce the impact of a disruption can be extremely valuable months later if and when something out of the ordinary happens. Here are a few tips we have for planning and executing a fire drill.

* Modularize your application, so that no issue with a single component can result in total application failure.
* Use tools like [Chaos Monkey](https://github.com/Netflix/SimianArmy/wiki/Chaos-Monkey) to see what happens when a server goes offline.
* Write out your emergency plan. Know not just what needs to be done, but who is responsible for each step in getting the application back online.
* Practice. Actually hold a fire drill. Set up a duplicate testing enviornment and start breaking things. See how fast you can get back online.
* Make sure all essential services and storage are configured to come online after a [reboot](https://community.rackspace.com/products/f/54/t/4319).
* Know who to call at Rackspace. Know what you can fix, and when you need to call in Rackspace's support for additional help.

<!-- Hide this in the print version <iframe src="http://www.slideshare.net/AndrewDrewCox/slideshelf" width="760px" height="570px" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:none;" allowfullscreen webkitallowfullscreen mozallowfullscreen></iframe> -->
