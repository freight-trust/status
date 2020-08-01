---
title: Besu Node Upgrade

draft: false

# Full date: 2020-08-10 17:26:09
date: 2020-08-10

# Status: "resolved" | "in_progress" | "scheduled"
status: "scheduled"

# This message will be taken out of the flow of events
# and displayed at top of page or below the header
# as long as its status is marked as in_progress
# pinned: (empty) | top | belowheader
pinned: 

# Duration for "scheduled" issues: Raw text, ie 5mn, 1h, 1 hour,..
duration: 5mn

# Max severity: will be displayed when issue is resolved, in the past events section
# Max_severity: ok | disrupted | down | monitoring | maintenance
max_severity: down

# Current severity: used for current issue display
# current_severity: ok | disrupted | down | monitoring | maintenance
current_severity: down

# Full date: 2020-03-29 17:26:09
resolved_on:

# Affected components, must use exact names defined in site config
affected:
  - Site

# If set and the status is in_progress, this feed will be embedded
# in the event display. Leave empty for no Twitter feed.
# Possible URL formats:
# See:  https://help.twitter.com/en/using-twitter/embed-twitter-feed
#
# - Profile: Display public Tweets from any user on Twitter:
#    https://twitter.com/freighttrust
#  
# - Likes: Show all Tweets a specific user has marked as likes.
#    https://twitter.com/freighttrustnet/likes
#
# - List: Show Tweets from public Lists that you own and/or subscribe to.
#    https://twitter.com/freighttrustnet/lists/national-parks
# 
# - Collection: Show Tweets from a curated collection.
#    https://twitter.com/freighttrustnet/timelines/539487832448843776
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

## Do not change
section: issue

# Short code available in content to display current date
# in a short format. For instance for issue updates.

# {{< track "2020-08-12 15:31:06" >}}
# {{< track "" >}}

## Enter below issue description and subsequent updates if any
---

We need to perform some software updates on our main website server. These updates require restarting the machine which implies some downtime.
\
This maintenance should not last more than a few minutes or cause any other perturbation.
\
Sorry about the trouble!
\
