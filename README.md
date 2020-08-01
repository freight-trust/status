
<!-- COPYRIGHT 2020 - FREIGHTTRUST AND CLEARING CORPORATION
        ALL RIGHTS RESERVED 
    -->
<!-- FREIGHT TRUST HEADER AREA DEFAULTS  -->
<!-- FREIGHT TRUST BANNER IMAGE -->
<p   align="center">

<img   src="https://raw.githubusercontent.com/freight-trust/branding/master/images/optimized_github_repo_card.png">
</p>
<br>
<!-- FREIGHT TRUST BANNER IMAGE -->
<!-- Badges Start -->
<p   align="center">
<img   alt="Twitter Follow"   src="https://img.shields.io/twitter/follow/freighttrustnet?label=%40FreightTrustNet&style=social">
 <a   href="https://t.me/freighttrust">
 <img   alt="Join Freight Trust's Public Telegram"   src="https://img.shields.io/badge/telegram-%40freighttrust-blue">
 </a>
<img src="https://hackmd.io/NCz6pCrUTyuI2cksLNHShQ/badge" href="https://hackmd.io/NCz6pCrUTyuI2cksLNHShQ/badge">
</p>
<!-- Badges End -->
<!-- FREIGHT TRUST HEADER AREA DEFAULTS END -->


## Issue file naming

The issue file should be created with the following convention:

````
2019-04-10-title-of-issue.md
````   

- should start with a date in the `YYYY-MM-DD` format
- then a title with no spaces
- with a `.md` extension

> The start page of a ClearStatus status page displays all present and past events. However each event also has an individual URL that you can share. Click on an issue header to reach that page.

## Issue file content and template.

Issue files use the [markdown](https://daringfireball.net/projects/markdown/syntax) language, which is basically just text and images with little in terms of formatting and is what [Hugo](https://gohugo.io) normally uses.

The first section of the file is used however to tell ClearStatus about the, well, status of the event happening and you should use it to convey your message to visitors.

Once you have written the current event description, use the `Commit changes` button in Github/GitLab to save the content. This will trigger an update of your status page after a few seconds.

When the issue status changes, for instance when it's resolved or some more information is available, come back to this page, modify the event file and use `Commit changes` again to update your status page.

Here is a sample issue file, you can use it as a template:


````

---
title: Connectivity issue

draft: false

# Full date: 2019-03-29 17:26:09
date: 2019-03-30 20:03:00

# Status: "resolved" | "in_progress" | "scheduled"
status: "resolved"

# This message will be taken out of the flow of events
# and displayed at top of page or below the header
# as long as its status is marked as in_progress
# pinned: (empty) | top | belowheader
pinned: 

# Duration for "scheduled" issues: Raw text, ie 5mn, 1h, 1 hour,..
duration:

# Max severity: will be displayed when issue is resolved, in the past events section
# Max_severity: ok | disrupted | down | monitoring | maintenance
max_severity: down

# Current severity: used for current issue display
# current_severity: ok | disrupted | down | monitoring | maintenance
current_severity: ok

# Full date: 2019-03-29 17:26:09
resolved_on: 2019-03-30 20:45:19

# Affected components, must use exact names defined in site config
affected:
  - Site
  - Helpdesk

# If set and the status is in_progress, this feed will be embedded
# in the event display. Leave empty for no Twitter feed.
# Possible URL formats:
# See:  https://help.twitter.com/en/using-twitter/embed-twitter-feed
#
# - Profile: Display public Tweets from any user on Twitter:
#    https://twitter.com/weeblrpress
#  
# - Likes: Show all Tweets a specific user has marked as likes.
#    https://twitter.com/TwitterDev/likes
#
# - List: Show Tweets from public Lists that you own and/or subscribe to.
#    https://twitter.com/TwitterDev/lists/national-parks
# 
# - Collection: Show Tweets from a curated collection.
#    https://twitter.com/WeeblrPress/timelines/1118432874733219840
#
# - Moment: Show Tweets from a public moment.
#    https://twitter.com/i/moments/625792726546558977
#
twitterFeed:

# Enable Disqus commenting on this page. This will only works if 
# you added your Disqus identifier in the global config.yml file
# under the disqusShortname option.
# enabledDisqus: true | false
enableComments: true

# Do not change
section: issue

# Short code available in content to display current date
# in a short format. For instance for issue updates.

# {{< track "2019-03-26 15:31:06" >}}
# {{< track "" >}}

## Enter below issue description and subsequent updates if any
---

Both our website and customer support area cannot be reached at the moment. We are investigating the matter.
\
**Issue identified:** Our hosting company has informed us of a failure in the datacenter network equipment. They are working on it and expect a quick resolution.  {{< track "2019-03-30 20:08:19" >}}
\
**Monitoring:** The equipment in question has been replaced and website and support site can be reached. We are monitoring the servers for the next few minutes to be sure all is OK. {{< track "2019-03-30 20:31:19" >}}
\
**Resolved:** Both servers are operating normally, issue is solved. Really sorry about the trouble!
\

````

Here is a breakdown of options available:

- `title`: a short and explicit title for the event happening such as "Helpdesk not available" or "Site under maintenance" 
- `date`: the date and time at which the event started - or will start in the case of scheduled events 
- `status`: 3 options: `resolved`, `in_progress` or `scheduled`. 

`in_progress` events are listed at the top of your status page, with a red header

`resolved` events are listed at the bottom of the page, with a neutral colored header

`scheduled` events are listed just below the list of components (systems) on your page with a lighlty colored header.

- `pinned`: if you set this to `top` or `belowheader` and set its status to `in_progress`, the event will be taken out of the regular display and will show at the very top of each page or just below the header, respectively. This is meant to display an important message in a prominent manner to all visitors such as a security warning. Once the status is reset to anything else but `in_progress`, the event will not be displayed anywhere anymore.

Pinned items also have a simplified layout

- `duration` is only used for **scheduled** event. Use that field to tell visitors how long that scheduled event is supposed to last. It's free text, can be "about 5 mn", "1 hour" or "1h"

- `max_severity` and `current_severity` are used to display an event importance and severity. Both can be: `ok`, `disrupted`, `down`, `monitoring` or `maintenance`

`current_severity` is used when an event is `in_progress`. `max_severity` will be used when the event is resolved to indicate what the worst state of operation was.

Typically, while an event is in progress, you will first set `current_severity` to `down`. Then as you make progress towards resolution you can change the state to `disrupted` or `monitoring` after you think the problem is solved but you are monitoring to be sure it does not come back. 

Once the problem is fully solved, you can set its `status` option to `resolved`. That's when we'll use the `max_severity` as it is important to remember the system was down, even though the last severity level displayed may have been `disrupted` or `monitoring` only.

- `resolved_on`: an optional date and time. Required when an event has been marked as `resolved` in its `status` field.

- `affected`: a list of components that are affected by the event. Add one component per line and use exactly the same name you used on your configuration file.

- `twitterFeed`: an optional Twitter feed or collections. 

- `enableComments`: another excellent way to communicate directly with your users. Clearstatus can include commenting on each issue individual page. You can enable/disable commenting per issue. The only pre-requisite is to set your [Disqus shortname](https://disqus.com) under the `disqusShortname` option in the global configuration file. You will of course need to set up a Disqus account for your status page to make this work.

> We advise to use a dedicated shortname for your status page, separate from any other Disqus shortname you may be using on your other websites.

- `body`: the body is the free text area located after the `---` line (do not touch or remove this line by the way). It is just plain text you can write to describe it. You can add to, remove from or update that text to your liking using markdown for nicer formatting. 
 
## Credits

This project is loosely inspired by [CState](https://github.com/cstate/cstate) and started out both out of different requirements and the desire to work with Hugo, Netlify, Go templates and such.


_(version 2.0.0)_
