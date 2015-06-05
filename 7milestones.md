Title: Getting started with Rackspace - a timeline of your experience as a Rackspace Cloud Customer
Author: Bill Hertzing and Justin Kase; Edited by Alan Bush
Date: Friday 2015-06-05

# 7 Customer Milestones <!-- A timeline of your experience as a Rackspace Cloud Customer -->

This article is part of a series of articles from our [Cloud Launch Team](http://www.rackspace.com/blog/an-insiders-look-at-the-cloud-launch-team/) - the team of cloud usability experts who help our newest customers. We have asked the Launch Team to share some of their findings with a greater audience. This article outlines the seven customer milestones they see for their customers. The timeline begins at account signup, and follows for the first 60 days, after which customers work with our main support channels.

We have linked out to other Community and Knowledge Center content for additional information and context.

# Milestone 1: Sign-up

## New account created

The very first step in your customer journey is creating a cloud account with Rackspace. We try to contact everyone of our new customers, personally, to welcome them to Rackspace, and provide immediate assistance to those that need it, so make sure that the contact information you provide is accurate. We also recommend that you take the time to speak with one of our Launch Managers to discuss your plans, and work with them to meet your goals.

## Initial call with a launch manager (strongly recommended)

We invite you to join a call with one of our Launch Managers. They are available to all of our customers for the first 60 days after your account is created, free of charge. During an initial call, the Launch Managers will work with you to discover the following (among other things):

* Service Strategy: learn about your business, support expectations, end user experience
* Demand Management: learn about your traffic patterns of business, website activity, hosting priorities
* Financial Management: learn about your new vs. existing projects, hosting budget, compliance requirements, budget planning
* Supplier Management: how was your previous hosting experience? Why did you choose Rackspace?  Do you need to migrate anything to Rackspace?
* Service Level Management: discuss implementation activities, downtime tolerance, go live date
* Capacity Management: load balancers, horizontal computing, modularity
* Continuity Management: load testing, GET v. POST testing, HA v. continuous operation
* Security Testing: network access, user access, cryptographic controls, patching, etc.
* Availability Management: monitoring, backups

*We've put much of the above together as a checklist, based on the most important conversations the Launch Managers want to have with each customer.*  <!-- Needs a link, once they're published. -->

# Milestone 2: Building your application

After you've signed up and spoken with our Launch Team, you'll be ready to jump in and start building your application. Here are a few resources that might be helpful:

## Control Panel <!-- do we have a recording of a CP Walkthrough? Should we? -->

* [Cloud Control Panel](http://www.rackspace.com/knowledge_center/article/introducing-the-rackspace-cloud-control-panel) - This is your control panel to manage your cloud infrastructure.
* [Use Role Based Access Control](http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac) (RBAC)


## Migration Team (Cloud Movers or Website Movers)

We can offer some limited [help migrating from another hosting provider to Rackspace](https://www.rackspace.com/migration). We also work with some professional services partners who can provide additional help. Contact your Launch Manager or Account Team for more information.  

For those of you who want to take a DIY approach to migrating to Rackspace, we have the following guides available:

* [Migrating a Linux server](http://www.rackspace.com/knowledge_center/article/prepare-to-migrate-a-linux-server)
* [Migrating a Windows server](http://www.rackspace.com/knowledge_center/article/prepare-to-migrate-a-windows-server)

# Milestone 3:  Launch on Rackspace


## Pre-launch

* Lower TTLs
* Change local host file

## Launch Day

* Determine exactly what will be switched (backup current DNS configuration)
* Base line check (capture "as is" configuration to measure/capture real time progress)
* Making the change

## Post Launch

* Verify all systems are still in production

# Milestone 4:  Customer Event

This is the time when the customer will reveal their new site to the world.

For some customers this might be their launch date as it occurs when they point their DNS.  For others it might be when an event is airing, press release or some other kind of announcement.

The customer might ask for an administrator or Launch Manger to be present in case various systems start to buckle. It's also important to note that the customer's developer should also be present during this time.

## Be aware of possible issues that can occur during high traffic events & solutions to remedy

* Oversaturation of traffic to Web01 from other web servers
* Resource exhaustion & contention
* Reboot check

## Create awareness of event in advance

* Document time, POCs, config summary, tactical plans, proactive configuration of backups & domain monitoring, and pre-work by adding cloud load balancers & databases.

# Milestone 5:  Steady State

After all the tuning from the customer's event has been completed, the system should reach a steady state where no additional changes need to be made.

This is where the system is working as expected and orders are coming in.

Monitoring should continue looking for when the traffic requests will taper off. It's at this point that maintenance windows should start to be planned. Cloud Databases will need to be downsized and nodes in the cloud load balancer can start to be drained.

Also at this time, postmortem data should be collected while still fresh.

* Capture date stamps
* logs copied
* noted requests
* calculations for credits (if necessary)

Additionally, things that went well should be noted so they can be repeated again.

# Milestone 6: First Invoice

At 30 Days the customer will receive their first cloud invoice. It's important to follow-up with the customer to see if there are any questions about the invoice.

## Example issues might be:

* Bandwidth charges & Support costs
* Ensure customer understands $50 for MI and $500 for MO is just a minimum and not a flat fee
* Discuss storage fees where applicable

## Proactive Initiatives

* 30 days is a good time to run a Discovery Report


# Milestone 7: Graduation Date

With the customer's Graduation Date (at day 60) they move from Team D0 to their long term support team, the following needs to take place:

## Conduct warm handoff

* For MO customers go to team D3-4
* For MI customers go to team D4-2

## Monitoring Review

Make sure there are URL checks for all the customer's primary domains. This is important should the customer's site go offline, support will be notified

## Complete full Backups Review

* Web servers, DB servers, CBS,etc.
* Ensure customer understands costs & risks of not having backups

## Golden Image

* Golden image is a manual image of a server. When a server is deleted, all automated backups and content associated with that server is also deleted. Only manual images are kept
