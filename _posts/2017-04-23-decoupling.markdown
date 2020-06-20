---
title: Decoupling isn't just for developers
layout: post
---

A while ago I read this article: [Complexity and Strategy](https://hackernoon.com/complexity-and-strategy-325cd7f59a92)

I highly recommend reading it. It's much better than any of my blog posts.<!--more-->

One sentence that still lingers in my mind two months later is this one:

<div class="blockquote">
<em>Features interact — intentionally — and that makes the cost of implementing the N+1 feature closer to N than 1.</em>
</div>

In every organisation I've been a part of it goes this way: At first adding new features is fast and easy but as the codebase grows, it gets exponentially harder and slower.

I've always ascribed this to technical debt, but that never felt quite right. The codebases weren't that bad, yet adding new features still kept getting harder.

Now it all makes sense. New features usually interact with existing features, so the more existing features there are that need to be interacted with, the harder it is to add a new feature.

*****

I saw a good example of this in Slack just now. I write most of my blog posts, including this one, while on vacation. When I left work I used Slack's new "status" feature to set my status to one of the defaults: "Vacationing".

I was suprised to find that setting my status in this way did not affect my notification settings in any way. I kept getting notifications from my workmates until I used a separate feature to "Snooze Notifications".

The status feature is completely decoupled from the notification settings functionality. They do not interact in any way.

While I was initially suprised that setting my status to "Vacationing" did not change my notification settings, can you imagine the confusion if it had? Even if it was well communicated in the UI, it would leave me confused about how different statuses affected my notifications. What if I set my status to "At Lunch", would I expect that to also mute notifications? What if I ignored the default statuses and created a custom status of "On Holiday"?

Decoupled features are generally easier for users to understand than features that interact with one another in complex ways.

To understand why Slack did this, it helps to understand the context: The notifications functionality is already very complex. Check out this diagram of how Slack decides whether to send a notification:

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">When Hacker News commenters say &quot;I could build that app in a weekend!&quot; I think of this chart of how Slack decides to send a notification. <a href="https://t.co/LopicAyzkL">pic.twitter.com/LopicAyzkL</a></p>&mdash; Matt Haughey (@mathowie) <a href="https://twitter.com/mathowie/status/837735473745289218">March 3, 2017</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Slack already have a lot of features that interact with notification settings in a complex way, if they had designed statuses to interact with notification settings as well it would have vastly increased the cost of adding this new feature.

Adding features in a decoupled way like Slack did with Statuses avoids interactions between features which reduces overall complexity in the system and makes it easier to add new functionality.

*****

Good developers are always trying to decouple things, to minify the ways in which different pieces of code interact with each other. It's one of the main selling points of the current hot trend: microservices.

Decoupling can't be purely the concern of developers though. Software architecture and product design are inescapably linked. If the product design specifies that features interact with each other, then to a certain extent the developers' hands are tied.

This doesn't mean product designers need to understand software architecture, microservices and decoupling. Nor does it mean that we should elevate technical concerns over user experience.

It means we need to be conscious of the ways features interact with one another. To understand that interactions between features add complexity to the product and that complexity is expensive.

Complex interactions between features can make it harder for users to understand how the product works, and are guaranteed to slow down development of new features.

With that in mind, let us go forth and make trade-offs.
