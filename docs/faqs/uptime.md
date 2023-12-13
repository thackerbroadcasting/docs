---
title: How do we Guarantee our Uptime?
icon: simple/upptime
---

!!! note "TL;DR"
    Load Balancing, Backups, and Preventative Measures

Our business — like many others today — relies on cloud-based architecture to provide our services at the lowest possible price with the best possible experience. We use Digital Ocean to power our operations.

A consequence of using these cloud-based business is that when your favorite websites go down, we probably will to. Which is why we have several backup systems in place. There is a secondary and tertiary Digital Ocean instance, copied into Azure as a failsafe. We mirror our main Digital Ocean instance (San Fransisco) across the continent for our secondary (Toronto), and the third is mirrored completely off of the North American continent (London). Azure, as our failsafe, mirrors our Digital Ocean environment but stays in a dormant state until it is needed (yes, there are three copies that are separated from their parent: Wyoming, Texas, and Sweden).

## How Does This Work?
In the event of a disaster at one of these data centers, our system will automatically spin up the duplicated instance, starting with the one that is next in line. So for example, let’s say our San Fransisco instance goes down due to an earthquake in the area. Our instance will immediately switch over to the Toronto or London instance, whichever responds first. You may experience your audio stream cutting off suddenly as the change happens. Don’t worry though, this takes about five seconds to complete. Then, your music will continue as if nothing happened. We’ll take care of the rest. And don’t worry, the same URLs will work regardless of if your connecting to our Digital Ocean instances or our Azure environment.

## Major Catastrophe
Okay, let’s investigate something a little further. Let’s say Digital Ocean suffers a cyber attack of some sort that takes out their entire infrastructure. Not to worry, the system will automatically swap over to an Azure instance, whichever responds first.

Now, should absolute disaster strike and neither Digital Ocean nor Azure respond, we’ll start your instance in our datacenter. That way, you will always have something playing.

## Do you switch back?
Of course! We prefer to use our San Fransisco instance, so once the issues are resolved, we will manually switch your service back. We chose to switch it back manually because we can plan those, so we’ll treat it just like a maintenance window. For example, if an event happens at 10am MST that takes out our San Fransisco instance, no matter how quickly they can bring it back online (even if it’s a couple minutes), we will wait until the maintenance window you have expressed to swap you back.

Over the last two years, we’ve been able to guarantee an uptime for our main website and our broadcasting portal of 99.4%! And that was using our local resources! This does not include a DNS issue that sometimes affected z96mix.com in March/April 2023, and an issue that took out our ISP for a couple hours back in June 2022. We always want you to be able to listen and manage your music, so we take our infrastructure and backup measures very seriously.
