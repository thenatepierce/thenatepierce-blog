---
title: "Fixing my EDHRec URL Logic"
date: "2025-06-10"
---

I had the chance to chip more away at the project today, so I focused on the EDHRec URL logic.  

[https://github.com/thenatepierce/cs50final/commit/395d165185b97c644eb53cb91e50c02acdf6953f](https://github.com/thenatepierce/cs50final/commit/395d165185b97c644eb53cb91e50c02acdf6953f)

What I've settled on for the time being is:
  1.  Where the cardname is formatted as "dash-separated-strings", I created a list of these strings delimited by "-".
  2.  I then created a while loop that checks if the r.status_code == 403.
  3.  Each iteration of the loop, it builds an EDHrec link URL, starting with the first string in the card name, until it hits a valid URL, which breaks the while loop

It feels a bit brute-forcey, but it's the best solution I can think of for the time being.  If I stumble across something more elegant, I might swap that out.  I will also need to set up some logic to prevent an infinite loop.

While doing some testing for that, I realized another flaw in my code such that if Scryfall returns a two-faced card and both sides have the same color, then I get an index out of range error as it only has a single color identity.  [https://scryfall.com/card/mid/109/jerren-corrupted-bishop-ormendahl-the-corrupter?back](https://scryfall.com/card/mid/109/jerren-corrupted-bishop-ormendahl-the-corrupter?back) for example.  I think this further supports the try/except logic needed for all fields I'm pulling.

To Do list:

- [ ] Add Comments
- [x] Validate Commanders
- [ ] Build try/except functionalitiy for all fields
- [x] Create edhrec url while loop
- [ ] Make edhrec while loop infinite-loop proof
- [ ] Create commander_info classes that the function calls

Stay tuned for more!
