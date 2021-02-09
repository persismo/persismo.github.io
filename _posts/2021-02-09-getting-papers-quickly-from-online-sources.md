---
layout: post
title: Getting papers quickly from online sources
bdate: February 9, 2021 12:00 AM
author: Harsha S. Bhat
math: false
tags:
  - papers
  - scihub
  - cnrs
hide: false
---
Suppose you come across a manuscript through Google Scholar or some other source and arrive at the webpage of the journal. For example, here is an article that I read recently. <https://epubs.siam.org/doi/abs/10.1137/20M1345153>. Clearly, clicking on the link to the PDF will not work. The fastest way to get to the PDF is using [bookmarklets](https://en.wikipedia.org/wiki/Bookmarklet). I have created the bookmarklets for INSU Bibliography thingammyjig and (wink wink) for Sci Hub.

Here is how to make it work.

- Use a browser of your choice and create a new bookmark.
- For the URL simply paste
  - ` javascript:location.hostname=location.hostname+'.insu.bib.cnrs.fr' ` for INSU
  - ` javascript:location.hostname=location.hostname+'.sci-hub.st' ` for SCIHUB
- Save the bookmark in a handy place. I put it on my bookmarks tab so that I can access it directly.

Et Voila. You are set to go. 

To use it, simply go the page containing the article, <https://epubs.siam.org/doi/abs/10.1137/20M1345153> and then click on one of the two bookmarklets you have created. 

For INSU you will be asked to log-in the first time you do it (use your JANUS identity) and then you don't have to login again as long as the browser is open. 

For SciHub you get the PDF directly :)

Enjoy reading papers.

