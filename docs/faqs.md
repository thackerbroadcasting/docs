---
hide:
    - navigation
---
# FAQs

## Can I have a local instance?
??? abstract "Yes and no"

    We try to provide you with the easiest possible solution to managing your tunes, which requires an internet connection. We will evaluate each individual request for an offline instance and reply to each based on circumstances. However, if you are approved an offline installation, a contract will be written that waives our liability for unauthorized access, system updates, system disruptions, and music management. If there are questions, please reach out to [contact@thackerbroadcasting.com](mailto:contact@thackerbroadcasting.com) or submit a ticket.


## Can I request to be hosted in a different data center?
??? abstract "No"

    At this time, no. We’ll put you in our San Fransisco instance by default. At this time, there isn’t a way to scatter clients around data centers. We will, however, put a relay server in the data center closest to you and connect you to that to help minimize the delay and reduce buffering.

    Keep in mind, this is subject to change in the future. We understand that while our customers remain close to home for the time being, expansion is inevitable. The current working structure is that clients will be placed in one of the closest data centers possible and will operate there until the client either moves or expands.

## How do I get my Music?
??? abstract "The Power of Magic!"

    Upon confirming a contract with you (or your business), Thacker Broadcasting will submit for a music license on your behalf to fit your needs. Once we have received that license, we will save that in our business documentation and will send you a copy of it for your records. This will happen every year you have a contract with us. After receiving the license, two things will happen: First, we will load up a profile for you on our web-based music system and a profile in our ticketing system with the email you provided (you’ll receive an email with this happens as you’ll have to change the password for both). Once that profile is created, we’ll tailor the music to what you have told us and begin playing. Secondly, we will send a technician to your business to set up a custom-made device that will “listen” to the web-based stream coming from your profile. This device is preloaded with software that, when turned on, will automatically load your music stream and begin to play it. This happens every time the device is turned on so if something goes wrong, your best bet is to unplug that device and plug it back in, which the technician will show you how to do.

## How do we guarantee our uptime?

??? abstract "Load Balancing, Backups, and Proactive Measures"
    Our business — like many others today — relies on cloud-based architecture to provide our services at the lowest possible price with the best possible experience. We use Digital Ocean to power our operations.

    A consequence of using these cloud-based business is that when your favorite websites go down, we probably will to. Which is why we have several backup systems in place. There is a secondary and tertiary Digital Ocean instance, copied into Azure as a failsafe. We mirror our main Digital Ocean instance (San Fransisco) across the continent for our secondary (Toronto), and the third is mirrored completely off of the North American continent (London). Azure, as our failsafe, mirrors our Digital Ocean environment but stays in a dormant state until it is needed (yes, there are three copies that are separated from their parent: Wyoming, Texas, and Sweden).

    !!! tip "How does this work?"

        In the event of a disaster at one of these data centers, our system will automatically spin up the duplicated instance, starting with the one that is next in line. So for example, let’s say our San Fransisco instance goes down due to an earthquake in the area. Our instance will immediately switch over to the Toronto or London instance, whichever responds first. You may experience your audio stream cutting off suddenly as the change happens. Don’t worry though, this takes about five seconds to complete. Then, your music will continue as if nothing happened. We’ll take care of the rest. And don’t worry, the same URLs will work regardless of if your connecting to our Digital Ocean instances or our Azure environment.

    !!! danger "Major Catastrophe"

        Okay, let’s investigate something a little further. Let’s say Digital Ocean suffers a cyber attack of some sort that takes out their entire infrastructure. Not to worry, the system will automatically swap over to an Azure instance, whichever responds first.

        Now, should absolute disaster strike and neither Digital Ocean nor Azure respond, we’ll start your instance in our datacenter. That way, you will always have something playing.

    !!! example "Do you switch back?"

        Of course! We prefer to use our San Fransisco instance, so once the issues are resolved, we will manually switch your service back. We chose to switch it back manually because we can plan those, so we’ll treat it just like a maintenance window. For example, if an event happens at 10am MST that takes out our San Fransisco instance, no matter how quickly they can bring it back online (even if it’s a couple minutes), we will wait until the maintenance window you have expressed to swap you back.

        Over the last two years, we’ve been able to guarantee an uptime for our main website and our broadcasting portal of 99.4%! And that was using our local resources! This does not include a DNS issue that sometimes affected z96mix.com in March/April 2023, and an issue that took out our ISP for a couple hours back in June 2022. We always want you to be able to listen and manage your music, so we take our infrastructure and backup measures very seriously.

## What are the security measures used to protect me and my music?
??? abstract "To keep it short..."
    There are a variety of measures we take to protect your customer data and the music you enjoy.

    - There is physical security of the device itself. Protected by a password, physical locks, disabling USB ports, and disabling wireless connectivity helps prevent your device from being found and accessed, both physically and wirelessly.
    - When the device is installed on your network, we will segregate it from the rest of your network. What this simply means is that it will be locked in its own little network area, unable to talk to any of your local devices. That way, local customers won’t be able to accidentally (or even purposefully) find and try to take control of the device.
    - Your device will talk directly to a proxy service. This will help prevent your business’ public IP address from being spilled or broadcast to the internet. We utilize Cloudflare which is very fast and secure. In addition, all of our websites use the latest encryption to ensure that your data is transported safely and securely. Cloudflare helps us ensure that your data is protected while helping your music be delivered as fast as possible.
    - We only use cloud providers that support the industries latest security measures. This helps prevent unauthorized access should a security breach happen.
    - The servers we use are physically protected by our cloud providers. Digitally, they are protected by SHA-256 encryption keys that are physically separated from any of our publicly accessible content. These keys are stored on a server that will never touch the internet. Any updates we have to do on this server must be done in an offline fashion