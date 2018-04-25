# Disciplined Trading - Settings for ProfitTrailer 2 and PTMagic
[NOT RELEASED YET -- HOLD YOUR HORSES WE'RE ALMOST READY!](https://github.com/stevenshizzleh/gen3-pt-settings/releases)

This is a pre-release group of settings for ProfitTrailer (PT) 2 and PTMagic (PTM) 1.6. These settings are pre-release for a few reasons:

1. A number of indicators that this team wanted to use are not working correctly in PT or they are not properly documented. Because of this, the indicators that would yield best results cannot be used.

2. This is a learning process. We'll see pair characteristics that demand we change the way we trade them (e.g., downtrends, uptrends, volatility, volume, pump & dumps, etc.). As we become more familiar with the new indicators and some of the great charting tools out there, we'll continue to improve the settings.

## Thought Process Behind Settings
1. **Optimal Entry.** The settings employ a combination of technical inicators to both purchase pairs and dollar cost average (DCA) at the optimal entry point. No more buying at a peak, and no more buying in the midst of a downtrend unless there are signs of intermediate stability.

2. **Optimal Exit.** We'll be using indicators such as RSI to help determine when it is time to sell a pair. Keep this in mind when you see the low sell_value. A sell_value may be 0.8%, but PT will not begin to trail the pair until it receives a confirmation from a secondary indicator that confirms it's time to exit. This means profit can be 0.8% or it can be something like 4.9% depending on the pair, small pumps, and the adjustments we continue to make to these settings as we learn more.

3. **DCA with depth.** DCA depth continues to be deper than traditional approaches from the PT community. This results in you being able to deploy more of your capital to other trading pairs in order to maintain a high quantity and velocity of trading. It wouldn't make sense to DCA rapidly for what started as a small committment to a small gain (that's trading on emotion). Think of it this way: if you dropped $5 into a drain along the sidewalk, would you rapidly invest hundreds of dollars to get that $5 out? Nope!

4. **Patience.** Allowing the bot to work its way out of a DCA will require patience. Experience shows that many pairs will sell after only 1 or 2 DCA levels. This might take 1 or 2 weeks. Don't focus on one poor performer. Maintain a holistic and disciplined view of your trading and continue to take into consideration daily gains and montly projections.

# Getting Started
1. Review the details of the Single Market Settings (SMS) in the below section. Then, review your single market settings and make changes where appropriate.

2. Review the PAIRS.properties and make changes in the first section. If you don't, results will be unpredictable. The settings need to be tuned to your risk preferences, market (BTC/ETH/USDT), and balance.

3. Be advised there's an issue with the PT 2.0 possible buy log that may prevent pairs from being displayed. Recommend you use PT Tracker as an alternative if you have PT Pro.

# Single Market Settings
## All Stop
Triggered by the sudden drop in price of a pair. The pair will go into sell only mode (SOM) for 30 days or until you turn off the All Stop setting in PTM. If a pair is held when this triggers, the bot will sell for a very minimal profit and DCA disabled.

## Recent Dump
Triggered when the 1-day value of a pair has dropped by 10% or more. Unless PT was activated at just the wrong time, you should not be holding a pair in this position because pump protection should have kicked in at the start of the pump. 

If a pair is held when this triggers, the bot will sell for a very minimal profit and DCA disabled.

## Pump Protection
Triggered when the 1 hour value of a pair is higher than normal. The pair will go into SOM for 16 hours or when a pullback ocurrs compared to the value of the pair 12 hours ago. If a pair is held when this triggers, profit is increased marginally, trailing profit is increased significantly.

## Extreme Uptrend
Not sure if we'll keep this but at this time we have it in here out of caution. We'll be doing more analysis on extreme uptrends to analyze the risk and determine if it is tradable. Oftentimes, extreme uptrends are not tradable because it's hard to get them to trigger and if we can get them to trigger, it's not at the right time. Awaiting updates to PT to resolve indicator issues then we'll revisit this SMS. It'll either become tradable or will get merged with Uptrend. We'll also need to analyze if this ocurrs as a result of a pump, or naturally. This may require additional work to the Pump Protection SMS.

Triggered when the 1-day value of a pair is higher than normal. If a pair is held when this triggers, profit is increased marginally, trailing profit is increased significantly.

## Untradable Downtrend
At this time, we're being more careful than not. Imagine you're on a jet-ski off the coast of a local beach. There are little waves, the water is choppy, it throws you around a little. Sometimes you get thrown into the air just a pinch -- this is lots of fun. Now imagine that you're on a jet-ski and about to drive yourself off a 1/4 mile tall waterfall. During the fall, there are no bumps and hence there's no fun as all you're doing is falling pretty quickly.

We'll continue to study how to trade in a steep downtrend, but for now it's best to stay away from it. If the value is going down, then your investment is going to go down.

Triggered when the 1-day or 2-day value of a pair is too steep to trade, based on research on a number of pairs in decline. If a pair is held when this triggers, the pair will go into SOM. Sell values and trailing profit will not change from the baseline.

## Downtrend
Triggered when the 3-day or 5-day value of a pair reflects a consistent downtrend. The bot will attempt to trade during pauses in downtrend. Slightly higher trailing buy than normal and slightly lower sell value than normal due to the constraints imposed on the width of the bollinger bands by the BBWIDTH indicator. DCA levels are deeper.

## Uptrend
Triggered when the 3-day or 5-day value of a pair reflects a consistent uptrend. The bot will attempt to trade on the volatility of the pair. Slightly lower trailing buy than normal and slightly higher sell value than normal due to the constraints imposed on the width of the bollinger bands by the BBWIDTH indicator. DCA levels are shallower.

## Baseline (PAIRS and DCA defaults)
The default settings in PAIRS.properties and DCA.properties.

# PTMagic Global Settings
The pre-release settings will not use global market settings. Dispite what the majority of pairs are doing, some pairs will do the exact opposite. In those cases, we'll rely on the buy and sell setting to guide us to the path of profit.

# FAQ
**Q:** Will this work with BTC?

**A:** Yes. You will need to update the below settings:
    
    --PAIRS.properties--
    market = BTC
    max_trading_pairs = [your value here, see next question]
    DEFAULT_min_buy_volume = [your value here, recommend 780]
    
    --settings.analyzer.json--
    Change the ignored markets for market trends

**Q:** What should I set ALL_max_trading_pairs to?

**A:** You'll need to determine what your max trading pairs is based on your comfort levels, balance, DCA levels, and risk acceptance. As of this FAQ, I have 0.90 ETH. I can comfortably trade up to 14 pairs at a time. Your max trading pairs will be based on (1) your assumption of how many pairs will enter the various DCA levels (2) the **depth** of the DCA levels (3) ALL_max_cost_percentage. The true limiting factor on the number of pairs you run is your DCA setup. The current DCA setup is deep and  allows for a large number of pairs to be traded as the likelihood of DCA3 and DCA4 is less likely. Please take a look at my a helper spreadhseet I made availabe on [GoogleDocs](https://docs.google.com/spreadsheets/d/17quWIFAAK0xfsUXyBz1mU9wjAGUrUHBFm3_MhSaOnTg/edit?usp=sharing).

**Q:** Why do you use DEFAULT_initial_cost_percentage instead of DEFAULT_initial_cost?

**A:** To make sure you're compounding! Longer explanation: if you use percentage, then each time you buy it will take into account previous gains/losses. If you're making gains, subsequent buys will be larger and will in theory return greater net gains.

**Q:** I've had a pair in the pairs log for X number of days, what's up with this?

**A:** You'll have that. Allow the DCA levels to do their thing and allow the market to do what it does. Keep in mind the depth of DCAs means all of your capital won't be tied up in just one or two pairs.

**Q:** How much will I make?

**A:** I do not know the answer to that question. Our goal is to deliver a consistent 1% per day. We will not rest until we've reached that goal.

**Q:** Can I make a donation?

**A:** Nope! The best way you can donate is to share your feedback, ask questions, and share these settings if they help you. The developers of PTMagic do not charge for the application and will we. It used to be just me working on these settings, but now we've got a team of people dedicated to creating the best settings we can get out there. The team is comprised of a software engineer, a professional trader, and a number of dedicated users/testers who continuously analyze the settings to make sure this is the best settings for ProfitTrailer on the internet. As long as we continue to have people with dedication like theirs, that'll be payment enough!
**_"A rising tide lifts all boats."_**

**Q:** What will the sales look like?

**A:** Like this:

I don't know yet but we'll find out and then I'll put a cool picture here.
