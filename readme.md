# The North Star: Settings for ProfitTrailer 2
These settings are ProfitTrailer-only settings that exclusively trade high-performance pairs. They have surgical entry points with gentle low-risk exits. The settings feature responsibly tiered DCA levels that are applied only when the market tells us its time. 

The settings bring clarity and focus. In a sea of opinions, clichés, and lackluster settings, we ask you trust The North Star.

> Whenever you find yourself on the side of the majority, it is time to pause and reflect. - Mark Twain

# What are The North Star settings?
We went back to the basics. We asked ourselves the fundamental questions until we were able to craft the ways means to a profitable setup:

**What do we want to do?** We want to increase our Bitcoin (or Ethereum) position within the cryptocurrency space. We want the bot to buy at the right time and sell at the right time more often than not. We do not want our capital tied up in dollar cost averaging.

**Why are we having trouble with this?** Some pairs are on an uptrend, some are on a downtrend, and some aren't doing very much. With PTMagic, we are trying to account for every possible scenario. It's time to focus on doing one thing and doing it with excellence.

**What kind of pairs do we want to buy into most?** I think I can speak for all of us when I say that when we wish upon a star, we want to ride the up-trending pairs (pumps). We look back in hindsight and think, _"I wish I got in on that action!"_ We wish we could do it with little risk and we wish we could be more certain than ever that our bot is making the right choices on our behalf.

**We can't predict when a pair is going to pump. How can we get in on the action?** We need to characterize a pump. The more we looked at high-performance pairs, the more we saw repeating patterns. We captured the hallmark characteristics of an up-trending pair and came up with a buy strategy that we really think you're gonna like.

# FAQ
**Q:** I need help!

**A:** Visit our [Discord](https://discord.gg/34bxedy) channel.

**Q:** Will you be releasing PTMagic settings?

**A:** To be clear, the presence of PTMagic does not mean you will make more money. The results are only as good as the settings and at this time we've been able to accomplish our initial goal with ProfitTrailer 2. 

Our intent is to continue to improve this specific setting to increase profit and curtail risk. We feel if we can do this one thing extremely well, then it's going to represent a large majority of the overall solution. Saying the PT settings aren't good because there aren't any PTM settings is like saying a dining room table is crap because there isn't a napkin holder on it. This is not to say that PTM isn't a great tool, but it's not a necessity and we're trying to keep things managable and profitable. Eventually, we would like to get extremely good at trading other trends. So the vision is that one day we'll have The North Star as a Single Market Setting in PTMagic, alongside other refined settings.

**Q:** Wthout PTMagic, how can you protect against pumps?

**A:** When a pump occurs, the width of the Bollinger Bands will increase. If the pump is too great, the width of the bands will exceed that allowed by the BBWIDTH setting in the PAIRS.properties file. Bottom line here is that pump protection is built in. Now you might ask, "well what if it buys at the top of the pump?" It won't because (1) the buy value cannot be much higher than the top Bollinger Band, and (2) the STOCH must be low, representing a fall in value compared to previous price action.

**Q:** What should I set max_trading_pairs and DEFAULT_initial_cost_percentage to?

**A:** You'll need to determine what your max trading pairs is based on your comfort levels, balance, DCA levels, and risk acceptance. As we see more buys, sells, and inevitable bags, we'll be doing Post-Purchase Reviews to look for patterns and leading indicators that can help make these settings even safer. 

For the time being, I feel very comfortable in saying that it is more unlikely than ever that you will enter a level 4 DCA. Feel free to take a look at our planning spreadsheet available on [GoogleDocs](https://docs.google.com/spreadsheets/d/17quWIFAAK0xfsUXyBz1mU9wjAGUrUHBFm3_MhSaOnTg/edit?usp=sharing) or the settings [landing page](https://github.com/stevenshizzleh/the-north-star) to help you get started. Please proceed with caution and at your own risk. If you're nervous about the 4.25% on the spreadsheet, settle at 2.12%. If you consistently get about 0.5% profit per day or greater and don't have any bags, then crank it up a pinch to your liking.

**Q:** Why do you use DEFAULT_initial_cost_percentage instead of DEFAULT_initial_cost?

**A:** To make sure you're compounding. Longer explanation: if you use a percentage, then each time you buy it will take into account previous gains/losses. If you're making gains, subsequent buys will be larger and will in theory return greater net gains. If you do not use the percentage, your missing out on the compounding. 

Let's say you start of with $800, investments are based on a percentage of the balance, and you make 1% per day. At the end of 30 days, you will have $1068. On the other hand, if each day your investments are based on a static value, you will have $1032. At a 1.5% profit, this gap is even wider at $1232 and $1148, respectively.

**Q:** I've had a pair in the pairs log for X number of days, what's up with this?

**A:** You'll have that. Allow the DCA levels to do their thing and allow the market to do what it does. Keep in mind the depth and intelligence of the DCAs means all of your capital won't be tied up in just one or two pairs. Be patient - those bags will pop!

**Q:** How much will I make?

**A:** I do not know the answer to that question. Our goal is to deliver a consistent 1% per day and I think if we're not already doing it, we're pretty darn close.

**Q:** Can I make a donation?

**A:** This is a toughie for me. Mostly because I don't usually accept praise well ;) The best way you can donate is to share your feedback, ask questions, and share these settings. I do not feel comfortable advertising a Bitcoin or Ethereum address for donation. If you're definitely compelled to donate, feel free to contact me directly as I want to have the opportunity to thank you directly. At the same time, I do acknowledge that I have dedicated a lot of time to this project and at personal sacrifice. Others have put forth time and effort as well and I would be remiss if I didn't acknowledge their hard work. I could not have done this without them.

I want you to know that this work is profoundly important to me. I have ambition, I have dreams, and like most people I have debt. My "North Star" is telling me that if I can make this work, this may be able to change my life. If I can help just a few people out there get out of a tight spot in life or help a parent get a bicycle for their 6 year-old, then that's something that'll put a smile on my face.

**Q:** What will the sales look like?

**A:** Something like this:

![North Star Profits](https://i.imgur.com/mQWe0LK.png)
