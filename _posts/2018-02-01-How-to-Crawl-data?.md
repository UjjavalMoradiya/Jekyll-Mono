---
layout: post
title: How to S̶c̶r̶a̶p̶  Crawl data?
author: Ujjaval Moradiya
---

>  If you can see the data in your browser, you can crawl that data EASILY.

Are you in need of a data? Worried about blocking or don't know how to crawl, you are at a right place. Here I will talk about how to crawl a data?, the techniques you need to avaoid or you need to follow.

## Scrapping Ways
-----

**Make a Thumb rule** : Scrapping must not look like 'a bot is collecting a data'. **Bot must 	behave like a human is interacting with website**.

### So how will you teach your bot to behave like a human? 
This is about login based scrapping.

1. While typing credentials, you must need to maintain your typing speed. It **must look like** human is typing. What we are avoiding in scrapping is, we are just pasting userid and password. Don't do this.

2. If human is interacting a site, it follows some pattern. Ex, to buy a proudct, user goes to menu, selects category, then sub category and clicks on product **where as** a bot directly executes product url. Users are also doing this but only sometimes. So this is a good way to identify a bot. Don't follow this. Follow the same steps that users are following.

3. For login based crawling, don't rotate your ips, cause human, in normal scenarios, access website from one location only. Human can not travel from one location to another location in seconds. So rotating proxies/ips will not help here. Use static ips.

4. Websites displays information, why? Because they want to give information. 

	* So what the problem they have with the scrapping? Why they are putting captchas, security questions or email code or OTPs? **Only one reason, resource utilization.**

		And because of that, normal-actual user can not get resources. And that is why they want to restrict scrapping and bots.
		**So don't make your bot so loudy that can down source site.**

		* If source site is down, wait for sometime.
		
		* If source site is not giving information, find a reason, there must be some reason, 	identify that and go ahead.
		
		* Track the information you are getting, **don't try same url again and again**. 
		Want to scrap 1000 products data, track which are collected and which are remain, so anything happens you can start from what is left.

5. Human scrolls a page at some time interval. Bot never scrolls a page (identification of a bot), it executes url and collects source code.
	
	Human clicks on the page index buttons (pagination), bots executes url only. If bot clicks on the pagination buttons, it always click on the same X-Y axis, but when human click on the button, X-Y axis will always different.

This are the things that you need to keep in mind while making a bot, this are the indirect things. But there are also direct things that can identify a bot. Here that are,

1. Do not ignore http-headers. Read here about [http headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers). Every request which are coming from browser has headers. Websites can define certain headers and if that are specified than thay will serve the data. 

	* The most important header is 'user-agent'. From this, server can identify from which browser requests are coming.

	* Depending upon the request, headers varies. This also depends upon server configuration. So before making a request, get headers information first.

	* While working with proxy, proxy server also adds some headers. With that headers, server can identify that requests are coming from proxy and they can disallow you from accessing data.

2. When you are crawling login based websites, rotating ips can direclty identify that there is something wrong.

----------------------------------------------------------------
This is about how to crawl a data. 

But how to handle captcha, email code or OTP. Keep checking for details.