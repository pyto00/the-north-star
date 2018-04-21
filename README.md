# 3rd Generation Profit Trailer Settings for ProfitTrailer 2+
[SETTINGS ARE NOT AVAILABLE YET...THIS IS A PLACEHOLDER :)](https://github.com/stevenshizzleh/gen3-pt-settings/releases)
## Thought Process Behind Settings
1. **Optimal Entry.** The settings employ a combination of technical inicators to both purchase pairs and dollar cost average (DCA) at the optimal entry point. No more buying at a peak, and no more buying in the midst of a downtrend.

2. **DCA with depth.** DCA depth continues to be deper than traditional approaches from the PT community. This results in you being able to deploy more of your capital to other trading pairs in order to maintain a high quantity and velocity of trading. The baseline profit for these settings is 1.75% and 1.75% of your balance per pair. It wouldn't make sense to DCA rapidly for what started as a small committment to a small gain.

3. **Patience.** Allowing the bot to work its way out of a DCA will require patience. Experience shows that many pairs will DCA after 1 DCA level. This can take 1 or 2 weeks. Don't focus on one poor performer. Maintain a holistic and disciplined view of your trading and continue to take into consideration daily gains and montly projections. You'll be fine!


## PTMagic Global Settings
Settings are in development

### Too close for missiles
Switching to guns.

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
