---
title: "Setting up OverTheWire and WeChall scoreboard"
date: 2024-1210
---

---

**!! THIS IS A DRAFT ENTRY... !!**

---

I've recently been completing several [Wargames](https://en.wikipedia.org/wiki/Wargame_(hacking)) on [OverTheWire](https://overthewire.org/wargames/) as a bit of a a refresher on some foundational tools and techniques for exploiting vulnerable systems. 

Towards the end of the [Bandit wargame](https://overthewire.org/wargames/bandit/) (their beginner game) I learnt of a platform called [WeChall](https://www.wechall.net) which allows users to keep track of their progress on "challenge sites" (e.g. OverTheWire, pwn.college, Hack The Box etc) and then copmares your performance on a global leaderboard. Talk about providing competitive incentive!

Whilst there are some [instructions](https://overthewire.org/information/wechall.html) over on OverTheWire to get the two platforms configured, I found there were a couple of extra steps needed to get it to work in my instance - so documenting here in case it's helpful for others.

![OverTheWire profile on WeChall](/assets/images/overthewire-on-wechall.png)

## Step 1 - Register with WeChall
You'll need to [register for a WeCall account](https://www.wechall.net/register), if you haven't already got one.

Sign in and head over to your Account and then to the [WarBoxes](https://www.wechall.net/warboxes) page. Here, you're looking for **your current WarToken** which is in the format of something like `00000-00000-00000-00000-00000-00000`.

You'll need both your **WarToken and Username** from WeChall.

![Your WarToken on WeChall](/assets/images/warboxes.png)

## Step 2 - Configure .bashrc
Next, you'll need to configure your machine with the credentials so they can be passed to the WeChall agent on the OverTheWire boxes.

```
export WECHALLUSER="YOUR_WEHCALL_USERNAME"
export WECHALLTOKEN="YOUR_WECHALL_WARTOKEN"
```

e.g

```
export WECHALLUSER="fcxi8"
export WECHALLTOKEN="00000-00000-00000-00000-00000-00000"
```