---
title: "Robinhood's Infinite Leverage"
date: 2019-11-09T15:09:48+01:00
exturl: https://www.bloomberg.com/news/articles/2019-11-05/robinhood-has-a-glitch-that-gives-traders-infinite-leverage
categories: [weekly]
tags: [trading,robinhood,leverage,margin]
draft: false
---

Imagine you could borrow an unlimited amount of money. You need USD &#36;2000 collateral, but otherwise everything goes - no questions asked. Want to borrow &#36;10k? Fine. &#36;100k? No problems. A cool million? Absolutely, with pleasure.

This week's article is exactly about this situation: [Robinhood's Infinite Leverage](https://www.bloomberg.com/news/articles/2019-11-05/robinhood-has-a-glitch-that-gives-traders-infinite-leverage).

<!--more-->

How much would you borrow? What would you do with the money?

Here's one idea:

- borrow USD &#36;50 000;
- buy AAPL covered put options;
- get to a ~&#36;7 000 unrealized profit (yay 🎉); but then also
- hold on and lose &#36;50 000 for a total of (&#36;100 000) realized return.

Somebody [actually did this](https://www.reddit.com/r/wallstreetbets/comments/dp6x5c/one_more_for_old_times_sake_because_if_i_dont/). Very cool. And by very cool, I mean *holy shit, why would you do this*.

There is [a YouTube video](https://www.youtube.com/watch?v=A-tNkuYV4_Q#t=39s) of the events unfolding a short time later. Take a look at the portfolio value change between 0:41 and 0:42.

Internet being what it is, some people saw this video and thought to themselves, [*I want this, except riskier*](https://www.reddit.com/r/wallstreetbets/comments/drt5tr/guh_of_fame_2019/).

## How Did the Infinite Borrowing Work?

Here are three things you need to know:

- Robinhood offers a 2:1 margin. If you have &#36;100 in cash, Robinhood will lend you &#36;100, so you can buy a total of &#36;200 of stuff;
- same if you have non-cash assets available. If you have &#36;100 in Apple stock, Robinhood will float you &#36;100 to buy some stuff;
- if you sell a call option, the premium will be added to your cash balance, but the stocks will not be excluded from your non-cash asset balance.

It might not be immediately obvious what's happening here, so here's a step by step example:

- initial state: **CASH:&#36;100** **AMD:&#36;0** **MARGIN:&#36;100**;
- buy AMD stock: **CASH:&#36;0** **AMD:&#36;200** **MARGIN:&#36;0**;
- sell AMD stock for let's say 90% (strike price + premium). Robinhood and reality part ways here:
  - real life: **CASH:&#36;80** **AMD:&#36;0** **MARGIN:&#36;80** (*You have lost money!* The strike price is &#36;2 and the options are sure to be exercised);
  - Robinhood, though, thinks your portfolio value just went up: **CASH:&#36;80** **AMD:&#36;200** **MARGIN:&#36;280**;
- now you can buy some AMD for &#36;360 (cash on hand + margin that Robinhood extends based on your imaginary portfolio value as collateral);

Notice (but don't let it stop you, I guess) that at *every iteration you are actually losing money*.

Repeat the process until you reach your Personal Risk Tolerance™, and then plow everything into 358 AAPL covered puts, and hope for the best.

There was a fixed amount lost on the AMD contracts, and the ultimate upside/downside was dependent on AAPL movement. Because these were covered puts, the upside was limited, but the maximum downside was unlimited 🚀 (except instead of the moon, this rocket is burrowing into the ground).

## This Explanation is Boring

Here is an admittedly better and [more hilarious explanation](https://www.reddit.com/r/wallstreetbets/comments/dqg6xx/infinite_leverage_explained/). This one uses less *finance terms*, and more *Reddit finance terms* such as "line of white lightning", and "cat lady".

## The Fallout

I suppose it ends in therapy for the people who lost 5 to 6 figures on this. For Robinhood, this ends with [increased regulatory scrutiny](
https://www.bloomberg.com/news/articles/2019-11-07/robinhood-back-in-washington-s-crosshairs-after-leverage-glitch).
