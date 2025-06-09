---
title: CS50 Final Project Update 6/9
date: 2025-06-09
---

I was able to get some work done on the project after my last post.

[https://github.com/thenatepierce/cs50final/commit/6aa49e004adfe0d3795061668f2f5ae70e246db8](https://github.com/thenatepierce/cs50final/commit/6aa49e004adfe0d3795061668f2f5ae70e246db8)

- I was betrayed a bit by Scryfall, as the is:commander search option will show both cards banned in the commmander format and "Legendary Enchantment - Backgrounds", which are not valid commanders in their own right.  I made a new function, validate_commander, to check to check for these two instances, and fetch a new random commander as needed without input from the user.

- I think the try/except loop is going to be necessary, as I forgot that some Planeswalkers can be commanders as well, and will not have a Power or Toughness

- I found that the commander naming from Scryfall does not line up 1:1 with EDHRech for the URLS, for example:
  
  https://scryfall.com/card/fin/58/jill-shivas-dominant-shiva-warden-of-ice
  
  https://edhrec.com/commanders/jill-shivas-dominant

  When using an invalid edhrec url, I get a 403 response code, so I built a while loop that checks for the 403 status code.  The hope in the future is that I can use the while loop to "trim" off the end of the url until I get a valid one.  I was tempted to just remove edhrec from the equation, but I think this practice will be good for me to have.

To Do list:

- [ ] Add Comments
- [x] Validate Commanders
- [ ] Build try/except functionalitiy for all fields
- [ ] Create edhrec url while loop
- [ ] Create commander_info classes that the function calls

Stay tuned for more!
