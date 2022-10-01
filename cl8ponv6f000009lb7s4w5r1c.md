## "Krakens and GUIs and CLIs, Oh My!"

Saaaaalllutationssss! I'm Simon, a multi-disciplined developer focusing on frontend development, app development, and game development using tools like [Unreal Engine](https://unrealengine.com), [Next.js](https://nextjs.org/), [TailwindCSS](https://tailwindcss.com/), and [Capacitor](https://capacitorjs.com/). Today I want to share a few of my favorite tools in my tool kit around something I use daily: Git. 

If you are new to software development, I want to give you a quick TL;DR on Git: Git is a method of version control. In short, it allows you to keep copies of the various changes to your work. Make a mistake? Delete a file by accident? Lose your laptop? You can easily re-download the files or even "go back in time" to a previous state. I can't tell you how often Git has "saved my bacon." You can learn more about Git here.

For starters, let's review the software that I will be referencing in this article: 

### **GitHub & GitHub CLI**

If you are brand new to Git, the names "Git" and "GitHub" might be confusing. While both Git and GitHub utilize version control and make managing and sharing code easier, that is where their similarities end. Think of Git as a single computer and GitHub as a network of multiple interconnected computers, all with the same end goal but a wildly different role for how to get there.

GitHub is a great hosting provider with millions of repos and organizations that use it daily. I love it because it integrates with my favorite tools (more on that later) and, most notably, the developer experience. 

GitHub is free and has multiple tiers if you are inclined to pay for a plan. I have pretty much always used the free tier. The only time I have used a paid method for GitHub is for my job to take advantage of some team-focused tools.
The GitHub CLI is a great way to interact with GitHub and your repositories without ever leaving your workflow or IDE. I am a big fan and advocate of efficiency and deep work.

### **Gitkraken Client & Gitkraken CLI**


Okay, I have to confess something before I continue: I am a HUGE fan of GitKraken and have been a paying customer since 2016. Here are a few reasons why:
- If you're new to Git, the Gitkraken Client is a Git GUI. It simplifies your interactions with Git by giving you a visual interface to interact with rather than the Git CLI.
- It offers a generous free tier. If you use GitHub, the only drawback would be not allowing you to connect to private repos. I haven't found this to be an issue. I used the free tier for GitKraken long before I became a paying customer.
- I have tried MANY Git GUIs: SourceTree, the built-in Git GUI included with Git for Windows, GitHub Desktop, and more. Not a single one could match the feature set and performance of GitKraken.
- GitKraken GUI also includes a CLI, a recent feature that I found pretty helpful. It lets those who have only used Git CLI take advantage of GitKarkens GUI while keeping their everyday workflows intact. 
- Recent updates have focused on teams and are an excellent quality of life addition.

### **Visual Studio Code (VSCode) w/ GitLens**

- In my opinion, VSCode is THE IDE for development. Download it [here](https://code.visualstudio.com/).
- Think of GitLens as adding Git superpowers to VSCode. More on this later. 
- At the time of writing, GitLens only supports VSCode. 
- I use the free tier of GitLens and will showcase the free tier in this article. GitLens+ includes features such as a visual view of file history and worktress, with more features coming soon. More on GitLens+ [here](https://www.gitkraken.com/gitlens/plus-features).
- Fun Fact: GitLens was recently acquired by GitKraken so expect more unique features in the future. Download GitLens [here](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

**Quick Note:** for the remainder of this article, I will be using a GitKraken Client Pro plan, so to utilize some of the features, you will need a Pro plan or higher, and I am happy to report that not only do you get a  7-day trial of Pro with any new GitKraken Client account, Pro is only $4.95 a month paid annually. That's like, what two fewer Starbucks trips a month? You'll quickly learn it pays for itself with time saved and deep integrations for many Git hosting providers. To get started for free with GitKraken, click [here](https://www.gitkraken.com/invite/csheW1Ty). With that out of the way, let's get started: 

(To help you get the most out of this article, I've created a companion repo to go along with this article. You can find it [here](https://github.com/Swarm-Creative/krakens-guis-clis).)

**GitKraken Client & Gitkraken CLI **

Whether you're working locally in Git or connecting to a hosting provider GitKraken Client & CLI has a host of tools to improve the developer experience, here are just a few: 

**Deep integrations with many hosting providers**

![git-gk-providers.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664613910569/jaiyieMrD.png align="left")

As shown in the image above, GitKraken integrates with many Git hosting providers. 

![git-gk-panel-issues.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614013053/EQKIdkwax.png align="left")

All issues and any issues assigned to me are easily visible right inside the client.
This supports various issue trackers such as JIRA, GitHub, Gitlab, and Trello.

![git-gk-pr-view.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614023961/eT0qQ7OCl.png align="left")

One of my favorite features is viewing and creating a pull request right from the GitKraken Client. It just works.
You can do pretty much ANYTHING from this view that you could do on GitHub. Add comments, see status checks running, add reviewers, and even merge the PR, all right from here. Bonkers!  

**A clear and streamlined way to interact with Git**

![git-gk-cli-commit.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614056241/3IqclLFsd.png align="left")

From the side panel, you can see your WIP, changed files, staged files, write your commit message, and more. From a UX standpoint, having your changed files and your staged files stacked visually clearly indicates what you will commit. Noice!

**If you're a power user...**

GitKraken recently added a CLI view with great features such as autocomplete, including autocomplete common tools such as yarn, the ability to hide the graph view outright, and more. 

![git-gk-cli-panel.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614069647/KpWIR5DM3.png align="left")

![git-gk-cli-git.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614080695/vc0ch9pJE.png align="left")

![git-gk-cli-autocomplete.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614090698/BiNxwCGw7.png align="left")


**GitHub & GitHub CLI**

GitHub is my git hosting provider of choice for many reasons, but in essence, it comes down to two main factors; integrations and ease of use. GitHub integrates well with many of the tools I use daily: Vercel, VSCode, and of course, GitKraken. 
   Here is a view of some of the ways GitHub is a blast to use: 

Issues are an easy way to keep track of work or bugs that need to be fixed in software. You can assign a branch in your repo to an issue and have it close once you merge it into your main branch. The issue can be assigned to a teammate, given labels, and assigned to project milestones (there is a whole suite of tools within GitHub for managing your software projects; however, I won't be covering them in this article). 

![git-gh-issue-open.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614163444/-kfEYD0bG.png align="left")

![git-gh-pr-close.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614177083/89DDRC6bT.png align="left")

For power users, GitHub has a CLI available that allows access to nearly every bit of functionality you would find in their web UI. 

![git-gh-cli-issues.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614193901/ejzrHcwAr.png align="left")
                                              *view of issues in GitHub CLI*

![Screen Shot 2022-10-01 at 04.51.08.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614283579/O866yq6H2.png align="left")
                                              *view of PR's in GitHub CLI*

**GitLens**

GitLens allows you to see changes in your files right within VSCode, even down to individual lines of code. The two views I use the most are line blame, gutter view, and diff view. Line blame shows when a file was changed and by who, while the diff view shows all changes to a file side by side. The gutter view allows you to see colored bars in the gutter of VSCode, by clicking one of the bars, you can peek at a change inline. 


![git-lens-diff.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614404325/qN3GnK4lX.png align="left")
                                                       *GitLens diff view*

![git-lens-gutter-diff.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614412356/xbYGz9b7R.png align="left")
                                                      *GitLens gutter view*

![git-lens-blame.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1664614472330/640yf0CEJ.png align="left")
                                                       *GitLens line blame*

***So there you have it; some of the ways I use GitKraken, GitHub, and GitLens, a few of my favorite tools that I use every day. I would highly recommend you give them a try in your workflow. Have a tool you think I should check out? Let me know in the comments below. Thanks for reading!***