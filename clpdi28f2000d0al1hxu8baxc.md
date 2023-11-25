---
title: "Its been a while"
datePublished: Sat Nov 25 2023 03:36:42 GMT+0000 (Coordinated Universal Time)
cuid: clpdi28f2000d0al1hxu8baxc
slug: its-been-a-while
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1700883372559/608a3ccb-0d23-4c79-9256-bb911585aced.jpeg
tags: game-development, unreal-engine, nestjs, indiedev, devblog, game-dev

---

Hi again, yes I know it has been a *lloooonnnggg* time since you have heard anything from me regarding the project, and I do apologize. I promise I have not abandoned the project, in fact, I have quite the update. Before I get into that I want to start by sharing some news....

### **I will be live-streaming the development of Project24 starting in December!**

The goal with the live streams is to offer a more in-depth look at the development of the project along with the ability to have more of a Q&A style interaction and bring you into my thought process as I make decisions about the game in the moment. With the push into live-streaming, I will move blog posts to a monthly format, and they will highlight a specific aspect of the development from the previous month.

I will broadcast on various platforms. You can find links to all of the social media channels at the bottom of this post. Be sure to follow and subscribe for updates on when broadcasts go live. **One additional note is that I have pushed back the Early Access window a tad from Summer 2024 to Fall - Winter 2024.** This is mainly due to seeing the amount of foundational work still needed to be done and to give more time to ensure a solid player experience for Early Access.

With that out of the way, just what have I been working on for the last several months? It can be broken down into 3 main categories:

* DevOps and Production Infrastructure
    
* Finalizing a Development Stack
    
* Planning
    

Let us break each of these down:

### Finalizing a Development Stack

So when we announced our project back in February I had a good chunk of the stack already chosen:

* [Unreal Engine 5](https://docs.unrealengine.com/5.3/en-US/) for the game engine
    
* [Railway](https://railway.app?referralCode=mGgvS) for the API hosting
    
* [Perforce](https://www.perforce.com/products/helix-core) for version control
    
* [TeamCity Server](https://www.jetbrains.com/teamcity/) for CI/CD. I went with the self-hosted option.
    
* [NestJS](https://nestjs.com/) for the API framework
    

The next steps were finalizing any connections and making sure everything was set up properly. To start I rolled out [UnrealGameSync](https://docs.unrealengine.com/5.3/en-US/unreal-game-sync-ugs-for-unreal-engine/) a Perforce tool included with the Unreal Engine source code that streamlines working with Perforce and Unreal Engine. I also set up a [UnrealGameSync metadata server](https://docs.unrealengine.com/4.26/en-US/ProductionPipelines/DeployingTheEngine/UnrealGameSync/Reference/#settingupthemetadataservice) to integrate the build notifications from the TeamCity builds. Finally, I created a [YouTrack](https://www.jetbrains.com/youtrack/) project to track tasks and the overall development progress.

With these pieces in place, it allowed me to move on to the next phase...

### DevOps and Production Infrastructure

I already mentioned TeamCity and UnrealGameSync as critical pieces of the DevOps pipeline for this project. I created a couple of build configurations to handle two key parts of the project: Building the Game and Building the Editor.

The optimal way to set up UGS (UnrealGameSync) is to set up your Perforce depot to include the game source code and engine source code. UGS will monitor for changes to any code or files and tag Perforce change lists appropriately. If a code change is detected you will need to recompile the game and engine binaries. Now this sounds tedious as ANY code change will require this but that's where TeamCity and a feature of UGS called ["Precompiled Binaries"](https://docs.unrealengine.com/4.26/en-US/ProductionPipelines/DeployingTheEngine/UnrealGameSync/Reference/#precompiledbinaries) comes into play. By building and submitting binaries to another depot via Perforce you can keep the most up-to-date Editor in step for you and your team. By simply hitting a toggle in UGS anytime you sync to a change list the correct version of the Editor will be pulled down and you're off to the races.

I also added a deployment to a Steam beta channel as part of the game build process. This will allow me to test the game regularly in a production environment as if I were a player.

By adding a trigger in TeamCity changes for the editor and game code can be validated right away keeping in the spirit of continuous integration and continuous deployment; CI/CD for short. For the final piece of the infrastructure, I settled on [BugSplat](https://www.bugsplat.com/index.html) for monitoring crashes and bugs. For more about DevOps you can read a great blog post about it [here](https://www.atlassian.com/devops).

With these items set up, I was finally ready to jump in and start planning.

### Planning

First on the agenda for planning was creating a [publicly visible roadmap](https://miro.com/app/board/uXjVMBSURHg=/?share_link_id=830770131456) via Miro. This will allow everyone to follow along with tasks, or goals of the game at a 1000ft view. Second was creating a [game design document](https://docs.google.com/document/d/12MidM4HsYCXUKhTb_uvqaM3fLQ2-DMa26AGvxnSd-Mk/view), which will act as the "bible" for the game and make sharing and talking about the game a lot easier.

### What's Next?

So what now? One of my last goals for the year is to create a "debug gameplay" menu. One key aspect of the games foundation is the communication between the UI, Player, and API so the goal with the debug gameplay menu is to be able to simulate the entire gameplay loop as if I were playing by utilizing a UI, and seeing the proper state of the game displayed by the UI. So over the next week few weeks, I will be working on that to close out the year.

Thank you for stopping by and I hope to see you in the livestream chat. Till next time.

Cheers,

Simon

[@](https://bsky.app/profile/zhymon.bsky.social)[zhymon.bsky.social](http://zhymon.bsky.social) [@](https://mastodon.online/@Zhymon)[Zhymon@mastodon.online](mailto:Zhymon@mastodon.online)

*SWARM social links as promised...*

* [Instagram](https://www.instagram.com/agentsofswarm)
    
* [Twitter](https://twitter.com/agentsofswarm)
    
* [Kick](https://kick.com/agentsofswarm)
    
* [YouTube](https://www.youtube.com/channel/UCnGVwVYfDjTOWRQjnfJEkQA)
    
* [TikTok](https://www.tiktok.com/@agentsofswarm)
    
* [LinkedIn](https://www.linkedin.com/company/agents-of-swarm)
    
* [Threads](https://threads.net/agentsofswarm)