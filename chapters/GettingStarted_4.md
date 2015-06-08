

# Milestone 4:  High traffic event

For some customers, launching a site is only the first leg, not the finish line.For some customers, the goal is a major event with publicity of some sort driving traffic. This might be their launch date as it occurs when they point their DNS; For others it might occur days or weeks later, corresponding with an episode of [Shark Tank](http://www.rackspace.com/content/2015/04/20/surviving-the-shark-tank-effect-solving-for-high-traffic-events/), a press release or some other kind of announcement. Whenever your event happens, we want you to succeed. Here are a few tips and tricks we've collected.

<!-- Need to mention the 10x SLA -->

## Be aware of possible issues that can occur during high traffic events & solutions to remedy

* Over-saturation of traffic to Web01 from other web servers
* Resource exhaustion & contention
* Reboot check

## Create awareness of event in advance

* Document time, POCs, config summary, tactical plans, proactive configuration of backups & domain monitoring, and pre-work by adding cloud load balancers & databases.

## Scaling from 1 server to multiple servers

* Seed config
* Load balancer and multiple servers
* Scale DB/add replication

## Test, test, and test some more

We always recommend testing, but testing becomes more important as you scale up for a high traffic event. Below are our recommendations on load testing and optimizing before an event. Don't hesitate to reach out to Rackspace for additional recommendations while preparing for a high traffic event.

### Load Testing

* Run a baseline test [load test](http://www.rackspace.com/blog/load-testing-your-site-with-load-impact-google-hangout-recap/) using [Load Impact](https://loadimpact.com/), [Loader.io](http://loader.io/), [Apica LoadTest,](https://www.apicasystem.com/) or another load testing service - you should know how your application works under normal conditions so you can better estimate how additional traffic will impact the app.
* Examine your test results and make appropriate changes to your configuration (adjust Apache MaxClients etc.)
* Run an additional load test after tuning your configuration to get an idea of how much traffic your site/app can handle

## Optimizing

* Serve static files from the [Rackspace CDN](http://www.rackspace.com/cloud/cdn-content-delivery-network) to [improve performance and load speeds](https://youtu.be/XVH7uVHBiE8)
* Introduce one or more caching layers within your configuration
* Use a third party tool such as CloudFlare or Incapsula to cache and optimize your web content at the DNS level

## If anything goes wrong

The old saying is that the best offense is a good defense, so we highly recommend that you contact Rackspace early, as soon as you know about an upcoming event. This will allow us to work with you to develop a plan for addressing any issues that might come up. Let us know when the event is scheduled, who will be your primary point of contact, how to get in touch with that person, etc. The more we know ahead of time, the better. If anything does go wrong, call support immediately - we'll be much better able to address the issue if you're on the phone, than if we're trying to figure out who you are based on your angry tweet.

## Next steps

After the high traffic events are completed, it's time to scale back down for steady state traffic. We'll cover that, and more, in the next chapter.
