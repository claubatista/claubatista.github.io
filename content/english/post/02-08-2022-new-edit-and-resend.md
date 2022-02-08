---
author: Clau Batista
title: New HTTP Edit & Resend Panel
date: 2022-02-08
description:
tags: [outreachy, internship, devtools, firefox]
series:
  - series-outreachy
---

hello everyone 🤙🏼

As I said on my [previous blog post](https://claubatista.github.io/post/01-31-2022-edit-and-resend/), in this one I’ll present more details about my Outreachy project.

To recap, I’m an Outreachy intern at Mozilla working on the Network monitor on the Devtools team. The main goal of my project is to write a new Edit and Resend panel on the Netmonitor based on the current one, with an update interface. The Edit and Resend panel is a tool for sending custom HTTP requests directly through the Netmonitor interface.

I just finished implementing most of the features and updates that were planned, and now I’m going into a new phase of the project where I’ll focus more on testing.

## What is new?

### Opening the panel

Just like the current panel, the new panel can be opened by right-clicking  on any request on the Network panel and selecting  the “Edit and Resend” option.

![edit-and-resend.gif](/images/02-08-2022-edit-and-resend.gif)

Notice that the new panel is now on the left side, we made this change so that users could inspect a request on the right panel and still have the edit and resend panel open.

There is also a new way to open the panel through toolbar

![toolbar.gif](/images/02-08-2022-toolbar.gif)

When the panel is open using this method, it is empty. This is useful for the case when a user wants to send a new request not based on any of the listed ones.

### Using the panel

One of the most different areas on the new panel is the headers section. The current panel provides only a textarea for editing headers, where each header is separated by a new line and the name and value are separated by a colon. On the new panel, each header has its own line and the name and value are in different input areas. When a user wants to add a new header, they can do so by using the fields on the last line of the header section and clicking enter. There are minor validations at this point to disallow headers with empty names and values.

![headers.gif](/images/02-08-2022-headers.gif)

Once a header is added, it can be deleted from the list simply by hovering on it and clicking on the “x” sign that shows up. The headers name and value can also be edited. Only headers which are added by the browser cannot be deleted or edited and show up as disabled on the list. Finally, there is also a checkbox next to each header to disable/enable it without deleting.

![headers-disabel.gif](/images/02-08-2022-headers-disable.gif)

The URL query parameters section looks very similar to the headers one, however it is not as feature intensive. In order to edit, delete or add query params changes need to be made directly on the URL field, these changes are then mirrored on the query parameters section.

![params.gif](/images/02-08-2022-query-params.gif)

The only thing that can be done through the query parameter section directly is to check or uncheck a given query param.

![params-disable.gif](/images/02-08-2022-query-params-disable.gif)

Some other updates that are worth calling out are:
1. the clear button, which was added right next to the send button and is an easy way to clear the whole form;
2. the input areas for the URL and Headers auto grow in height as you type;
3. and whenever a new request is made successfully it is automatically selected and the panel on the right side of the Netmonitor is opened for the user to check out details on the new request.

### What are the next steps?

I still have a little over a month before the internship period ends.

My goals from now on are to work on testing and improving the interface and its accessibility.

I’m very happy to work on this project and have the opportunity to contribute to the Firefox Devtools. None of the changes  that I describe here would have been possible without all the help that I got from my mentors: bomsy and Honza.

I hope you have also liked the new changes.