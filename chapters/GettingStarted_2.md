# Milestone 2: Building your application on Rackspace

After you've signed up and spoken with our Launch Team, you'll be ready to jump in and start building your application. Here are a few resources that might be helpful:

## Control panel  

* [Cloud Control Panel][1] - This is your control panel to manage your cloud infrastructure.
* [Use Role Based Access Control][2] (RBAC) to allow the correct stakeholder access to only the services he or she needs to access.

## Get a head start with Cloud Orchestration

If you are building an application from scratch, you might want to try [Cloud Orchestration][3]. The stacks offered in Cloud Orchestration can help you get your application up and running much faster than building from scratch. Orchestration stacks range from single server setups (LAMP Stack) to complex, mulit-server, configurations (for example a [multi-server WordPress stack.)][4]  


## Migration assistance

If your application is already live at another provider, we can potentially offer some limited [help migrating from another hosting provider to Rackspace][5]. We also work with some professional services partners who can provide additional help. Contact your Launch Manager or Account Team for more information.

For those of you who want to take a DIY approach to migrating to Rackspace, we have the following guides available:

* [Migrating a Linux server][6].
* [Migrating a Windows server][7]
.
## Modularize your application

We strongly recommend creating a modular application - it's one of the [5 Pillars of Cloudiness][8]. Modularizing your application can eliminate a single point of failure, and allow for significantly faster scaling if necessary. Here are a few tips for making a modular application.

* [Decouple your database from your web/app servers][9] by using a Cloud Database or a separate cloud server running your database. Additionally, look to [Object Rocket for hosted MongoDB or Redis][10].
* Build at least two web/app servers for [redundancy][11] and uptime.
* Place a Cloud Load Balancer in front of your web/app servers for [horizontal][12] [scalability][13].
* Use a [messaging queue][14] for asynchronous processes.

## Sending email from your application

If your application sends any email messages - think "Welcome!" emails, password resets, or weekly digests - then you'll need to configure your application to do that. We have a few tips for best results:

* To avoid blacklists, relay your mail through [MailGun][15] rather than sending directly from your cloud servers.
* Use [Rackspace Cloud Office][16] for employee mailboxes and collaboration, if needed. (IMAP, Exchange, Google Apps for Work, and Office 365 are available).

## Security

[Security is a partnership][17]. To be effective, security needs to happen at every level. Make sure to take the time to secure your application at every level.

### Account level

* Setup [role-based access control][18] for your team Use strong passwords and security questions/answers for each team member Infrastructure level Keep software and security patches up to date
* [Configure 2-factor authentication][19]

### Server level

* [Practice basic server security][20]  
* Lock down your firewalls manually or with a service such as [Dome9][21] or [CloudPassage][22]

### Application level

* Secure user authentication manually or with a tool like [Stormpath][23]
* Secure application communication with [SSL][24]
* Use strong passwords and rotate them often ([here's a fun example][25])
* Keep up to date with security patches
* Filter out malicious traffic to your sites with tools like [CloudFlare][26] or [Incapsula][27]


## Backups & Monitoring

Just as important as beginning or migrating your app to Rackspace is protecting that app with a solid backup and monitoring plan.  

### Backups
Backups are important if you need to restore your site should a server fail for any reason. There are many ways to backup your site and content. We recommend using a combination of [server images][28], file-level [differential backups][29], and [configuration management][30] to achieve a robust, comprehensive [backup strategy][31].

We recommend that you use [Cloud Backup][32] on the following directories:

#### Linux

* Web/App servers: Verify/configure backup jobs for your Web/App servers /home /root /etc /var/www.
* Database servers: Verify/configure Database backups (frequent backups and long retention are recommended):
  * /home
  * /root
  * /etc
  * /var/lib/mysqlbackup (For servers with a mySQL database. Managed Operations customers automatically dump the db to this location. Managed Infrastructure customers can configure the same backup using [Holland][33].)

#### Windows

* Verify/configure backup jobs for your Web/App servers C:\inetpub.
* Verify/configure Database backups (the location you are dumping your database files) frequent backups and long retention are recommended.

#### Backing up block storage

Block storage is a great way to increase the amount of storage space your application can use. You can include block storage in a Cloud Backup job; you can also save the volumes as image snapshots. If you're using Cloud Block Storage, please check and double check that backed up everything, and that you have configured to resume in the event of a reboot.

* Verify/configure backup of any Cloud Block Storage volumes.
* Verify that your attached [Cloud Block Storage volumes reconnect after reboot][34].

### Monitoring  

Monitoring can alert you if your site becomes non-responsive.  Customers with our Managed Operations service level can choose to atuomatically alert Rackspace Support when monitoring notices anything amiss.

* URL Check: [Add a Cloud Monitoring check][35] for your site's URL to ensure your site is responding.
* New Relic: Sign up for a free New Relic account at http://newrelic.com/rackspace Install New Relic's server and application monitoring agents on your cloud servers.

### Next steps

The next 3 milestones can vary greatly from customer to customer. Some customers go straight from opening an account to business as usual in immediate succession. Others have additional demands - high traffic events, or new feature launches, for example - that expand and prolong these milestones. In the next three chapters we will outline the process of [switching public traffic to Rackspace][36], [scaling for high traffic events][37], and [resuming steady state operations][38].


[1]: http://www.rackspace.com/knowledge_center/article/introducing-the-rackspace-cloud-control-panel
[2]: http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac
[3]: http://www.rackspace.com/blog/cloud-orchestration-automating-deployments-of-full-stack-configurations/
[4]: http://www.rackspace.com/knowledge_center/article/deploy-wordpress-packages-by-using-rackspace-cloud-orchestration
[5]: https://www.rackspace.com/migration
[6]: http://www.rackspace.com/knowledge_center/article/prepare-to-migrate-a-linux-server
[7]: http://www.rackspace.com/knowledge_center/article/prepare-to-migrate-a-windows-server
[8]: https://community.rackspace.com/products/f/54/t/4496
[9]: http://www.rackspace.com/blog/fundamentals-of-cloud-architecture-the-seed-config-video/
[10]: http://objectrocket.com/
[11]: http://www.rackspace.com/knowledge_center/article/protection-against-and-recovery-from-host-server-down-hsd-issue
[12]: http://www.rackspace.com/blog/pillars-of-cloudiness-no-3-scaling-horizontally/
[13]: http://www.rackspace.com/blog/examining-horizontal-scaling-google-hangout-recap/
[14]: https://developer.rackspace.com/blog/using-message-queues-in-cloud-applications/
[15]: http://www.rackspace.com/knowledge_center/article/configuring-mailgun-for-your-website
[16]: https://www.rackspace.com/email-hosting
[17]: http://www.rackspace.com/security/
[18]: http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac
[19]: http://www.rackspace.com/knowledge_center/article/multi-factor-authentication-from-the-cloud-control-panel
[20]: http://www.rackspace.com/knowledge_center/article/basic-cloud-server-security
[21]: http://www.dome9.com/
[22]: https://www.cloudpassage.com/
[23]: https://stormpath.com/
[24]: https://community.rackspace.com/products/f/18/t/55
[25]: https://xkcd.com/936/
[26]: https://www.cloudflare.com/
[27]: https://www.incapsula.com/
[28]: http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image
[29]: http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-create-a-backup-0
[30]: https://developer.rackspace.com/blog/devops-automation-series-images-vs-config-management/
[31]: http://www.rackspace.com/blog/backup-strategies-for-cloud-web-apps-google-hangout-recap/
[32]: http://www.rackspace.com/cloud/backup
[33]: https://community.rackspace.com/products/f/54/t/1638
[34]: https://community.rackspace.com/products/f/54/t/4319
[35]: http://www.rackspace.com/knowledge_center/article/creating-a-monitoring-check-using-the-cloud-control-panel
[36]: chapters/GettingStarted_1.md
[37]: chapters/GettingStarted_1.md
[38]: chapters/GettingStarted_1.md
