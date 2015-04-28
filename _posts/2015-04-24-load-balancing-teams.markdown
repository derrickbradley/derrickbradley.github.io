---
layout: post
title:  "Load Balancing Teams"
date:   2015-04-24 9:00:00
categories: [Resources, Ways of Organizing]
---

A while back Undercurrent introduced a resourcing policy to maintain a consistent amount of slack on our client delivery teams. We consented to cap our utilization at 2 cycles (cycles are 4 weeklong sprints) fewer than we currently have Members to deliver. This means that a small number of people (3-4) have 50% of their time available for at least 4 weeks at a time to help other client teams deliver their work. We call this being ‘on slack.’ The idea is that this helps keep our allocated teams from running too hot and gives Members the flexibility to explore other parts of the business they’re passionate about (culture, operations, growth, software, and so forth).

It’s hard to say whether or not this has been working all that well. There are times when I see someone jump in to help plan a workshop or create a few slides for another team, but it’s probably not because of this policy, it’s someone (not necessarily on slack) deciding to be helpful and interested in the work for a brief moment. Most of the time, though, Members on slack will up their utilization on existing work, leaning in harder than they should, while Members on active projects continue to run hotter than they have to. Both make the impact of the policy null.

This is a process problem, not a people problem. We don’t have any easy way for Members on slack to jump on and off of projects easily, nor do we have a tight feedback loop for client teams to signal that they need the help. To ask for help today teams will use Slack (either group or direct message) and offer a prompt like “Who can help me write this SOW?” or they’ll raise it as an action item during their weekly standup and assign someone to resolve it “Derrick to find extra resources to facilitate workshop.” These aren’t bad, but they offer no data on what kind of impact slack is having on our business model and they don’t signal how well slack capacity is being utilized. Members on slack could be bombarded with incoming requests or be receiving none at all because client teams are guessing at whether or not they’re busy. It’s push when it should be pull. 

It occurred to me that one experiment to run against this challenge is to look at how networks distribute traffic amongst web servers and introduce a system that performs like a load balancer for our business. The idea is straightforward: when the demand on any UC Team is too high, distribute tasks to Members on slack and record all activity in an accessible online platform without disrupting anyone’s existing workflow.

> Load balancing is a core networking solution responsible for distributing incoming traffic among servers hosting the same application content. By balancing application requests across multiple servers, a load balancer prevents any application server from becoming a single point of failure, thus improving overall application availability and responsiveness. For example, when one application server becomes unavailable, the load balancer simply directs all new application requests to other available servers in the pool.

To put this idea into practice I’ve decided to use a tool called Trello. Almost every team at Undercurrent already uses it to manage their projects, which makes it a great place to start. 

The first thing we need is a new Trello board that will capture all of the jobs to be done by Members on slack (our load balancer). The way an allocated team adds a card to this board is simply by adding a “Slack” label to any card on their existing Trello boards. [Zapier](https://zapier.com), a piece of elegant task automation software, then makes a copy of that card and adds it a Jobs to Be Done list in the load balancing board. Once there, Members on slack can add themselves to any card they're interested in working on, execute on it, and move the card into the Done list once completed.

There’s nothing more to it than that for now. It’s lean and flexible, two attributes that make for quick uptake around Undercurrent. I’m excited to give this a go and see what kind of use we get out of it. 

For anyone who's interested this is the [Zap](https://zapier.com) that makes this whole thing work.

![Step 1](http://i.imgur.com/q5NDy8hl.png)

![Step 2](http://i.imgur.com/OIPEeBYl.png)

![Step 3](http://i.imgur.com/qJzNpMKl.png)

![Step 4](http://i.imgur.com/i6kvCxhl.png)

![Step 5](http://i.imgur.com/KdH8uUKl.png)


[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
