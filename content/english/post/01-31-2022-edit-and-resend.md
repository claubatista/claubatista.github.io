---
author: Clau Batista
title: HTTP Edit & Resend Panel
date: 2022-01-31
description: A introduction about my Outreachy internship
tags: [outreachy, internship, devtools, firefox]
series:
  - series-outreachy
---

hello everyone 🤙🏼

Today I will present my project to you.

The Firefox DevTools have an Edit & Resend Panel and the goal of my project is to create a new one, based on the old one but with new user interface and functionalities.

![Screenshot 2022-01-30 at 17.12.57.png](/images/01-31-2022-old-panel.png)

### Why create a new one?

We didn’t create one from scratch, we created the new one based on the old one. We used the same structure of the old one, but tried to simplify the code. The old one used Redux, and now we avoided using Redux as much as possible as not to put too much complexity into the code, and to make it easier to maintain in the future.

### What is it Edit & Resend?

The Edit and Resend is a panel through which the developer can send a synthetic HTTP network request. It is useful for building, testing and using REST APIs.

### How is the project going?

The project is going well. Now I’m finishing the interface changes. I have already done the first part of the project, which was to change the panel to the other side, to add all basic functionalities and put everything behind a pref.

On Feb 8th will the release of  Firefox 99. All my changes will be available there for testing behind a pref **“devtools.netmonitor.features.newEditAndResend”** and on Firefox Nightly by default. Before then, I will write a new blog detailing all the changes.

I’ll leave you with a small spoiler of the new panel before the UI changes:

![Screenshot 2022-01-30 at 17.50.27.png](/images/01-31-2022-new-panel.png)

See you next week, thanks for reading. 🙂