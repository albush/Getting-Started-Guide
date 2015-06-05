*We recently asked our [Cloud Launch Team](http://www.rackspace.com/blog/an-insiders-look-at-the-cloud-launch-team/) to provide us with a checklist of all of the most pertinent information that they try to convey to their customers. This article represents just one of [seven milestones](getting_started_master_article.md) identified by the Launch Team.*

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
