---
title: "CS50 Final Update - Back to Class(es)"
date: "2025-06-11"
---

Made some big updates today!

[https://github.com/thenatepierce/cs50final/commit/c302ceb0e99c5748aaaabeadbf6b306ef5b14e44](https://github.com/thenatepierce/cs50final/commit/c302ceb0e99c5748aaaabeadbf6b306ef5b14e44)

First of all, I added logic to my EDHRec while loop such that if the number of loops (aka strings in the card name) becomes larger than the max_loop (total length of the card name in strings),  then the loop will stop and fill in placeholder data for EDH rec.

Secondly, I did double duty of creating classes for both the Scryfall and EDHrec output formatting and included try/except logic for each field.  On one hand, this should reduce the amount of code in the functions themselves, but the classes are pretty lengthy.  I'm not 100% sure this is best practices, but I can see the logic behind this method.  Having the try/excepts for each field will also help protect the program run in the cases where Scryfall/EDHrec have an expected field missing, which I think is an overall benefit (though it added a lot of length to the code.)  Overall pretty happy on the progress I made today, I think I am close to done with writing new code for the program itself, it will just be going back and making fixes/cleanup.

Todo:

- [ ] Add Comments
- [ ] Build testing
- [ ] Create Requirements
- [ ] Create Readme
- [x] Validate Commanders
- [x] Build try/except functionalitiy for all fields
- [x] Create edhrec url while loop
- [x] Make edhrec while loop infinite-loop proof
- [x] Create commander_info classes that the function calls
- [ ] Code Review

Stay tuned for more!