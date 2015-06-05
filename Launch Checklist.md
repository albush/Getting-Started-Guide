Title: Getting started with Rackspace - a timeline of your experience as a Rackspace Cloud Customer
Author: Bill Hertzing and Justin Kase; Edited by Alan Bush
Date: Friday 2015-06-05

# Launch Checklist

We recently asked our [Cloud Launch Team](http://www.rackspace.com/blog/an-insiders-look-at-the-cloud-launch-team/) to provide us with a checklist of all of the most pertinent information that they try to convey to their customers. We've aggregated their suggestions here, into one comprehensive list. We've broken the list down into various sections, and grouped content together where appropriate. Additionally, we have linked out to other Community and Knowledge Center content for additional information and context.

## Account activation tips

* Ensure your primary contact's email address is valid. This is where all ticket updates and communications will be sent
* Whitelist 'rackspace.com' and 'rackspacecloud.com' to ensure delivery to your mailbox
* Understand the [different account roles](https://community.rackspace.com/general/f/34/t/59).
* [Add your technical contact(s)](http://www.rackspace.com/knowledge_center/article/managing-role-based-access-control-rbac) to the account so that they can work with our support team when needed
* Make sure their contact information is correct
* Suggestion: [Setup a distribution list](https://community.rackspace.com/general/f/34/t/56) 'rackspace@yourdomain.com' for instance so all communication  is delivered to the correct team members


### Modularize your application

* [Decouple your database from your web/app servers](http://www.rackspace.com/blog/fundamentals-of-cloud-architecture-the-seed-config-video/) by using a Cloud Database or a separate cloud server running your database. Additionally, look to Object Rocket for hosted MongoDB or Redis
* Build at least two web/app servers for [redundancy](http://www.rackspace.com/knowledge_center/article/protection-against-and-recovery-from-host-server-down-hsd-issue) and uptime
* Place a Cloud Load Balancer in front of your web/app servers for [horizontal](http://www.rackspace.com/blog/pillars-of-cloudiness-no-3-scaling-horizontally/) [scalability](http://www.rackspace.com/blog/examining-horizontal-scaling-google-hangout-recap/)
* Use a [messaging queue](https://developer.rackspace.com/blog/using-message-queues-in-cloud-applications/) for asynchronous processes

## Sending email from your application

* To avoid blacklists, relay your mail through [MailGun](http://www.rackspace.com/knowledge_center/article/configuring-mailgun-for-your-website) rather than sending directly from your cloud servers
* Use [Rackspace Cloud Office](https://www.rackspace.com/email-hosting) for employee mailboxes and colloboration, if needed. (IMAP, Exchange, Google Apps for Work, and Office 365 are available)

## Backups

(This is important if you need to restore your site should a server fail for any reason.) Remember that using [server images](https://community.rackspace.com/products/f/25/t/135) is [not a complete backup strategy.](https://developer.rackspace.com/blog/devops-automation-series-images-vs-config-management/) [More on backup strategies](http://www.rackspace.com/blog/backup-strategies-for-cloud-web-apps-google-hangout-recap/)

We recommend that you use [Cloud Backup](http://www.rackspace.com/cloud/backup) on the following directories:

### Linux

* Web/App servers: Verify/configure backup jobs for your Web/App servers /home /root /etc /var/www
* Database servers: Verify/configure Database backups (frequent backups and long retention are recommended)
  * /home
  * /root
  * /etc
  * /var/lib/mysqlbackup (For servers with a mySQL database. Managed Operations customers automatically dump the db to this location. Managed Infrastructure customers can configure the same backup using [Holland](https://community.rackspace.com/products/f/54/t/1638).)

### Windows

* Verify/configure backup jobs for your Web/App servers C:\inetpub
* Verify/configure Database backups (the location you are dumping your database files) frequent backups and long retention are recommended

### Block Storage

* Verify/configure backup of any Cloud Block Storage volumes
* Verify that your attached Cloud Block Storage volumes reconnect after reboot
* [Verify that your services start back up after reboot](https://community.rackspace.com/products/f/54/t/4319)


### Monitoring  

Monitoring can alert you if your site becomes non-responsive.  Customers with our Managed Operations service level can choose to atuomatically alert Rackspace Support when monitoring notices anything amiss.

* URL Check: [Add a Cloud Monitoring check](http://www.rackspace.com/knowledge_center/article/creating-a-monitoring-check-using-the-cloud-control-panel) for your site's URL to ensure your site is responding
* New Relic: Sign up for a free New Relic account at http://newrelic.com/rackspace Install New Relic's server and application monitoring agents on your cloud servers


## Security

Security needs to happen at every level. Make sure to take the time to secure

### Account level

* Setup [role-based access control](http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac) for your team Use strong passwords and security questions/answers for each team member Infrastructure level Keep software and security patches up to date
* [Configure 2-factor authentication](http://www.rackspace.com/knowledge_center/article/multi-factor-authentication-from-the-cloud-control-panel)

### Server level

* [Practice basic server security](http://www.rackspace.com/knowledge_center/article/basic-cloud-server-security)  
* Lock down your firewalls manually or with a service such as [Dome9](http://www.dome9.com/) or [CloudPassage](https://www.cloudpassage.com/)

### Application level

* Secure user authentication manually or with a tool like [Stormpath](https://stormpath.com/)
* Secure application communication with [SSL](https://community.rackspace.com/products/f/18/t/55)
* Use strong passwords and rotate them often ([here's a fun example](https://xkcd.com/936/))
* Keep up to date with security patches
* Filter out malicious traffic to your sites with tools like [CloudFlare](https://www.cloudflare.com/) or [Incapsula](https://www.incapsula.com/)

## Load Testing

* Run a baseline [load test](http://www.rackspace.com/blog/load-testing-your-site-with-load-impact-google-hangout-recap/) using [Load Impact](https://loadimpact.com/), [Loader.io](http://loader.io/), [Apica LoadTest,](https://www.apicasystem.com/) or another load testing service
* Examine your test results and make appropriate changes to your configuration (adjust Apache MaxClients etc.)
* Run an additional load test after tuning your configuration to get an idea of how much traffic your site/app can handle

## Optimizing

* Serve static files from the [Rackspace CDN](http://www.rackspace.com/cloud/cdn-content-delivery-network) to [improve performance and load speeds](https://youtu.be/XVH7uVHBiE8)
* Introduce one or more caching layers within your configuration
* Use a third party tool such as CloudFlare or Incapsula to cache and optimize your web content at the DNS level

## How to configure Rackspace DNS for Rackspace Cloud

1. In your [MyCloud control panel](https://mycloud.rackspace.com), add your domain and [copy your existing records](http://www.rackspace.com/knowledge_center/article/creating-dns-records-for-cloud-servers-with-the-control-panel)
3. Ensure your domain's A record is pointing to your cloud load balancer
4. Move your site to Rackspace
5. At your domain registrar, update your nameservers to 'dns1.stabletransit.com' & 'dns2.stabletransit.com' - **Once this step completes (5 minutes to 48 hours depending on DNS host) anyone visiting your domain will be directed to the server(s) at Rackspace. Make sure to do this step last, when you are ready to send traffic to Rackspace.**

## Billing

* Cloud servers are billed at an hourly rate until they are deleted from the account
* The hourly rates for cloud servers include both infrastructure and support fees
* Managed Infrastructure accounts have a $50 minimum support fee
* Managed Operations: SysOps accounts have a $500 minimum support fee
* Your monthly invoices will be available via your MyCloud Control panel (for security, we will not email you a copy of your invoice)
* You can view an estimation of your current charges in the Current Usage page of the MyCloud control panel (Account > Usage Overview)
