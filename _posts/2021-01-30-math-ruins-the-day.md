---
layout: post
title:  "Math Ruins the Day"
date:   2021-01-30 12:00:00 -0700
permalink: /math-ruins-the-day/
categories: blog
tags: probability, dating, multi-armed bandit, thinking in bets, building, math 
author: Michael Zhao
---
### Math ruins the day, again
Let's say you just graduated college, you're in your mid-20s, and looking for a soulmate. Working in a big city, you're meeting new people, going on dates, and starting (and sometimes ending) relationships. Some dates go well, but others don't. During one of the better dates, in between conversation and laughs, your mind suddenly drifts: "When should I stop dating and take the leap? When should I decide to stop and marry?" After some brief pondering, you chuckle. "There's no way it's possible to have an exact answer to this," you think to yourself. "Relationships are subjective and diverse; there can't possibly be a scientifically optimal way to decide."

"Actually, if you're planning on dating between 20 and 32, the optimal age to take the leap is 24.5. In this case, when you find someone better than anyone you've met after 24.5 years old, marry them," your date, who coincidentally has a PhD in Statistics from UCLA, says. It turns out, you were thinking out loud. Without waiting for a response, she continues: "If you go on 100 dates with 100 different people, it's difficult to know which of the 100 people you should choose to marry. If you pick someone randomly, the probability they're your perfect match is just one percent. However, you apply the Optimal Stopping Problem's 37% rule, after meeting about 37% of your potential dating pool, you have enough information to understand the type of person you like, and at that point you can make the leap."

After about a minute, you're still speechless, so your date frowns, shrugs, stands up, and cartwheels out of the room. Once the initial shock subsides, and you finally begin to process what your date said. You wonder if you should start doing something with this information.

In probability theory, the optimal stopping problem is part of a process called the "multi-armed bandit" - it's a problem where, given a fixed set of resources, you find the optimal way to maximize expected gain. The reason it's called a "multi-armed bandit" is because you can imagine a gambler with a limited amount of cash at a row of slot machines ("one armed bandits") , trying to figure out which machines to exploit. If you reframe the problem, each slot machine = a decision, and pulling the slot machine's arm = deciding.

Starting out, you are unsure of which machines will pay well. Initially, you expend resources to collect data to note which machines are paying more than others. Once you have enough information, you can be more selective and play on machines that you have determined to pay well. After the gambling session, you collect your winnings and leave.

Informally, the multi-armed bandit problem can be rephrased as the "explore vs. exploit" tradeoff. Our lives are determined by the decisions we make, so it's hard to not see this problem everywhere: choosing where to go for lunch, applying to certain jobs, deciding your life partner, etc. We apply this explore/exploit framework to understand why certain people do certain things: for example, explore/exploit explains why young people tend to try new things, whereas older people stick with familiar activities.

While the explore/exploit tradeoff is a relatively good starting point for understanding and applying decision making, I want to bring up some issues that I've had with the framework and nuances that I've applied to make the framework more useful.

### Feedback of Effort
The first issue with the multiarmed bandit problem is that it views decisions as binary: you either choose to pull the slot machine arm or you don't. In reality, the level of "force" you apply to the decision matters - you can decide to do something and dive in wholeheartedly or you can poke your feet in the water and wade around first. Therefore, the decisions' expected value can shift depending on how hard you pull the lever: your effort becomes factor. In addition, pulling a lever more times can compound the expected value.

For example, you can't just look at the decision of "starting a relationship" as a simple lever pull with an associated expected value. Relationships are built initially through energy, and grown through repetition. The more you pull the lever of "building the relationship", the more valuable the relationship becomes. While the initial value might be small, as meaning is built through time and repetition, the decision to pull the lever over and over becomes more valuable. Therefore, there is value in having the agency and willpower to continuously pull certain levers. Kevin Simler in his blog ["Melting Asphalt"](https://meltingasphalt.com/religion-politics-and-self-suppression/) has a great quote about "time sacrifice" as a way to develop strong bonds:

>"Sacrifices don't just help foster group solidarity; they're also a powerful force for pair bonding. In fact, knowing that a particular good was sacrificed for you alone makes that sacrifice all the more meaningful.

>Many courtship rituals involve the sharing or sacrifice of time, money, food, energy, and other goods. What's an engagement ring if not the perfect sacrifice, the distillation of valuable resources (money) into a completely functionless token. An "engagement car" just wouldn't have the same romance to it.

>Even friendship is often cemented with sacrifice. Sharing secrets and intimate details, for example, makes you vulnerable but engenders trust. In my own life, one of the things that helps me feel closer to someone is wasting time together. My childhood and teenage friends are dear to me in part because we've sacrificed countless hours to each other. As an adult I simply don't have as much time to give, making it harder to develop deep friendships."

This is where reality deviates from economics: certain choices combined with continuous repetition becomes the opposite of diminishing returns.

### Learning from others
The normal multiarmed bandit problem assumes that you're the only one on the casino floor and that you have to make decisions solely based on the feedback of previous decisions. In reality, if you plan on doing something, chances are, someone has done that thing before and will have advice. There are many ways to do this: reading, asking, calling, observing, etc. When you're given advice, hazy paths will become clearer, and you can save time and energy by avoiding potential pitfalls.

For example, if you want to be a guitar player and play popular songs, you don't immediately try to play songs by ear. Rather, you begin by searching on YouTube: "How to play ‘Stop This Train’ by John Mayer", and work through a few videos, which helps avoid wasted time on trying methods that have dead ends.

While learning from others isn't as powerful as learning through trial and error, it's efficient and useful if you're faced with many different decisions. Learning from others narrows the scope of the decisions and allows you to focus on those that are more promising.

### More optionality isn't better
Something that I've noticed about me and my colleagues is that we apply the language and logic of financial concepts to our lives. ["Troubled by Optionality"](https://www.thecrimson.com/article/2017/5/25/desai-commencement-ed/) an article by Mihir Desai, describes it better than I can:

>"I’ve lost count of the number of students who, when describing their career goals, talk about their desire to “maximize optionality.” They’re referring to financial instruments known as options that confer the right to do something rather than an obligation to do something. For this reason, options have a “Heads I win, tails I don’t lose” character—what those in finance lovingly describe as a “nonlinear payoff structure.” When you hold an option and the world moves with you, you enjoy the benefits; when the world moves against you, you are shielded from the bad outcome since you are not obligated to do anything. Optionality is the state of enjoying possibilities without being on the hook to do anything. (...)

>This emphasis on creating optionality can backfire in surprising ways. Instead of enabling young people to take on risks and make choices, acquiring options becomes habitual. You can never create enough option value—and the longer you spend acquiring options, the harder it is to stop.

>The Yale undergraduate goes to work at McKinsey for two years, then comes to Harvard Business School, then graduates and goes to work Goldman Sachs and leaves after several years to work at Blackstone. Optionality abounds!

>This individual has merely acquired stamps of approval and has acquired safety net upon safety net. These safety nets don’t end up enabling big risk-taking—individuals just become habitual acquirers of safety nets. The comfort of a high-paying job at a prestigious firm surrounded by smart people is simply too much to give up. When that happens, the dreams that those options were meant to enable slowly recede into the background. For a few, those destinations are in fact their dreams come true—but for every one of those, there are ten entrepreneurs, artists, and restaurateurs that get trapped in those institutions."

Just like how spreading your bets across the casino floor is safe option, a bias towards maximizing optionality and riskless gain is the safe route to take. Yet, the cost for maximum optionality is giving up on your potential to be extraordinary on things you deem to be important. This is another issue with the framework - seeing every decision as bets can make you biased against risk. Risk exposure is necessary to achieve deeper goals.

### Stop thinking in bets
In spite of the the mounds of statistical evidence that can make you lean towards certain "optimal" behaviors, I believe thinking probabilistically is useful to a point. In situations that require fast-paced decisions, like crises or literal gambling, it makes sense to have a heuristic to help decide quickly. For longer term games, like relationship-building and skill-learning, it's better to have a "building" mentality. Sure, maybe theoretically it's optimal to eventually reject the first 37% of people you date, but in reality that's sociopathic behavior. During the more meaningful portions of your life, you shouldn't live as an algorithm, deciding on future decisions by using historical data as inputs. Rather, beautiful things can be built if you give them both time and energy.

![image](/assets/images/dice.jpg)

