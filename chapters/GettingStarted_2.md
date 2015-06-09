

# Milestone 2: Building your application on Rackspace

After you've signed up and spoken with our Launch Team, you'll be ready to jump in and start building your application. Here are a few resources that might be helpful:

## Control Panel  

* [Cloud Control Panel](http://www.rackspace.com/knowledge_center/article/introducing-the-rackspace-cloud-control-panel) - This is your control panel to manage your cloud infrastructure.
* [Use Role Based Access Control](http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac) (RBAC) to allow the correct stakeholder access to only the services he or she needs to access.


## Migration assistance

If your application is already live at another provider, we can potentially offer some limited [help migrating from another hosting provider to Rackspace](https://www.rackspace.com/migration). We also work with some professional services partners who can provide additional help. Contact your Launch Manager or Account Team for more information.

For those of you who want to take a DIY approach to migrating to Rackspace, we have the following guides available:

* [Migrating a Linux server](http://www.rackspace.com/knowledge_center/article/prepare-to-migrate-a-linux-server).
* [Migrating a Windows server](http://www.rackspace.com/knowledge_center/article/prepare-to-migrate-a-windows-server)
.
## Modularize your application

We strongly recommend creating a modular application - it's one of the [5 Pillars of Cloudiness](https://community.rackspace.com/products/f/54/t/4496). Modularizing your application can eliminate a single point of failure, and allow for significantly faster scaling if necessary. Here are a few tips for making a modular application.

* [Decouple your database from your web/app servers](http://www.rackspace.com/blog/fundamentals-of-cloud-architecture-the-seed-config-video/) by using a Cloud Database or a separate cloud server running your database. Additionally, look to [Object Rocket for hosted MongoDB or Redis](http://objectrocket.com/).
* Build at least two web/app servers for [redundancy](http://www.rackspace.com/knowledge_center/article/protection-against-and-recovery-from-host-server-down-hsd-issue) and uptime.
* Place a Cloud Load Balancer in front of your web/app servers for [horizontal](http://www.rackspace.com/blog/pillars-of-cloudiness-no-3-scaling-horizontally/) [scalability](http://www.rackspace.com/blog/examining-horizontal-scaling-google-hangout-recap/).
* Use a [messaging queue](https://developer.rackspace.com/blog/using-message-queues-in-cloud-applications/) for asynchronous processes.

## Sending email from your application

If your application sends any email messages - think "Welcome!" emails, password resets, or weekly digests - then you'll need to configure your application to do that. We have a few tips for best results:

* To avoid blacklists, relay your mail through [MailGun](http://www.rackspace.com/knowledge_center/article/configuring-mailgun-for-your-website) rather than sending directly from your cloud servers.
* Use [Rackspace Cloud Office](https://www.rackspace.com/email-hosting) for employee mailboxes and collaboration, if needed. (IMAP, Exchange, Google Apps for Work, and Office 365 are available).

## Security

[Security is a partnership](http://www.rackspace.com/security/). To be effective, security needs to happen at every level. Make sure to take the time to secure your application at every level.

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


## Backups & Monitoring

Just as important as beginning or migrating your app to Rackspace is protecting that app with a solid backup and monitoring plan.  

### Backups
Backups are important if you need to restore your site should a server fail for any reason. There are many ways to backup your site and content. We recommend using a combination of [server images](http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image), file-level [differential backups](http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-create-a-backup-0), and [configuration management](https://developer.rackspace.com/blog/devops-automation-series-images-vs-config-management/) to achieve a robust, comprehensive [backup strategy](http://www.rackspace.com/blog/backup-strategies-for-cloud-web-apps-google-hangout-recap/).

We recommend that you use [Cloud Backup](http://www.rackspace.com/cloud/backup) on the following directories:

#### Linux

* Web/App servers: Verify/configure backup jobs for your Web/App servers /home /root /etc /var/www.
* Database servers: Verify/configure Database backups (frequent backups and long retention are recommended):
  * /home
  * /root
  * /etc
  * /var/lib/mysqlbackup (For servers with a mySQL database. Managed Operations customers automatically dump the db to this location. Managed Infrastructure customers can configure the same backup using [Holland](https://community.rackspace.com/products/f/54/t/1638).)

#### Windows

* Verify/configure backup jobs for your Web/App servers C:\inetpub.
* Verify/configure Database backups (the location you are dumping your database files) frequent backups and long retention are recommended.

#### Backing up block storage

Block storage is a great way to increase the amount of storage space your application can use. Content in a storage volume can be included in Cloud Backup, and the volumes can also be saved as image snapshots. If you're using Cloud Block Storage, please check and double check that everything is backed up and configured to resume in the event of a reboot.

* Verify/configure backup of any Cloud Block Storage volumes.
* Verify that your attached [Cloud Block Storage volumes reconnect after reboot](https://community.rackspace.com/products/f/54/t/4319).

### Monitoring  

Monitoring can alert you if your site becomes non-responsive.  Customers with our Managed Operations service level can choose to atuomatically alert Rackspace Support when monitoring notices anything amiss.

* URL Check: [Add a Cloud Monitoring check](http://www.rackspace.com/knowledge_center/article/creating-a-monitoring-check-using-the-cloud-control-panel) for your site's URL to ensure your site is responding.
* New Relic: Sign up for a free New Relic account at http://newrelic.com/rackspace Install New Relic's server and application monitoring agents on your cloud servers.

## Next steps

The next 3 milestones can vary greatly from customer to customer. Some customers go straight from opening an account to business as usual in immediate succession. Others have additional demands - high traffic events, or new feature launches, for example - that expand and prolong these milestones. In the next three chapters we will outline the process of [switching public traffic to Rackspace](chapters/GettingStarted_1.md), [scaling for high traffic events](chapters/GettingStarted_1.md), and [resuming steady state operations](chapters/GettingStarted_1.md).
