Title: Getting started with Rackspace - a timeline of your experience as a Rackspace Cloud Customer
Author: Bill Hertzing and Justin Kase; Edited by Alan Bush
Date: Friday 2015-06-05

*We recently asked our [Cloud Launch Team](http://www.rackspace.com/blog/an-insiders-look-at-the-cloud-launch-team/) to provide us with a checklist of all of the most pertinent information that they try to convey to their customers. This article represents just one of seven milestones identified by the Launch Team.*

# Milestone 3:  Launch on Rackspace

Moving your applications to Rackspace is the first step to launching your app at Rackpsace; "turning it on" is the next step. If your application is currently hosted elsewhere, you will need to point your DNS to Rackspace. Here are some steps we recommend for launching on Rackspace.

## Pre-launch

A little bit of planning goes a long way, so make sure you lower your TTLs and update your local hosts file.

* [Change local host file](http://www.rackspace.com/knowledge_center/article/how-do-i-modify-my-hosts-file) - In order to view your content exactly as it will be presented to your consumers, you will likely need to modify your local hosts file on your desktop. This will override global DNS,  which will allow you to visit your site as it appears live on Rackspace, prior to shifting DNS to Rackspace. Any existing customers will continue to the existing site.
* Lower TTLs - The TTL ([Time to Live](http://www.rackspace.com/knowledge_center/article/about-ttl-best-practices)) determines how long your DNS information is cached in each DNS host. A long TTL when you try to switch to Rackspace could potentially mean yourapplication's visitors would continue to be sent to your previous hosting provider. Lowering the TTL allows changes to be made more frequently. Lower the TTL ASAP, so that the DNS change will happen as fast as possible.

Now it's time to test, test, test. Does everything work as planned? What's different than your current host? Hopefully it's better, but if not, what needs to be changed? Test, iterate, and test some more until you're ready to launch.


## Launch Day

Once everything is tested, it's time for launch. The actual switch will vary based on your current DNS host, so check with them. Of course we encourage you to use Rackspace Cloud DNS (either as a primary or backup DNS provider), but you do not need to host your DNS with us.

* Determine exactly what will be switched and backup your current DNS configuration. Make sure you get all components.
* If you're switching all of your DNS hosting, make sure your email and other systems configurations have been moved.

### How to configure Rackspace DNS for Rackspace Cloud

1. In your [MyCloud control panel](https://mycloud.rackspace.com), add your domain and [copy your existing records](http://www.rackspace.com/knowledge_center/article/creating-dns-records-for-cloud-servers-with-the-control-panel)
3. Ensure your domain's A record is pointing to your cloud load balancer
4. Move your site to Rackspace
5. At your domain registrar, update your nameservers to 'dns1.stabletransit.com' & 'dns2.stabletransit.com' - **Once this step completes (5 minutes to 48 hours depending on DNS host) anyone visiting your domain will be directed to the server(s) at Rackspace. Make sure to do this step last, when you are ready to send traffic to Rackspace.**

## Post Launch

* Verify all systems are still in production
* Immediately contact Rackspace Support if anything is not working.