---
description: >-
  These are just guidelines, not rules. Consider the invisible power asymmetries
  (junior v senior, male v female, experience v new etc.) often present during a
  social dynamic such as programming.
---

# Code Reviews

### Effective reviewing

#### As a reviewer

Do your best to help the author get their work into trunk. Your job is to assume competence and not just point out changes and modifications and criticisms, your job is to try your best to accept their code into mainline, i.e.; make progress.

* If you like an abstraction, a nitty-gritty or a change, point it out and make them feel like you appreciate their work. 
* Try to summarize your review with a high-level overview of your thoughts in closing. Mention what you have reviewed, what you skimmed over and what next steps we could take to try to get it merged. 
* If you’ve been put up to review, don’t just skim through and accept, have a healthy conversation.

Avoid unnecessarily terse and assertive questioning. If stuff is unclear, ask the author to explain. Provide information on why you found it difficult to understand and if possible, provide an alternate solution and your current understanding of the piece.

**Avoid**

* Why is this done this way? 
* What is this? 
* What does this do? 
* This doesn’t make any sense.

**Instead**

* I didn’t quite understand X. I think doing it as A might be a lot simpler for these reasons: r1, r2. 
* This looks like it’s X. Do you actually need it? Since we don’t use it anywhere. 
* I couldn’t parse this. Could we unpack this a bit and pull out semantic methods for readability? 
* This can be better done as Y.

The idea is not just to have flowery language. The idea is to create an environment where civil discourse can be had and power-asymmetries can be reduced.

* Clearly mention that your comment is a nitpick or a style change or an aesthetic suggestion. I like to prefix my messages with: `[NITPICK]`, `[STYLE]`, `[AESTHETIC]` respectively. 
* This goes without saying, don’t use aggressive/harsh language. Be very mindful of your tone and angle.
* Do not make the review personal. Talk about the code.
  * Prefer: _There’s an issue with **this** code_ over _There’s an issue with **your** code._ 
* Be mindful of not treating certain closer teammates with positivity and others with not so much. 
* If your review is cut short due to time or lack of bandwidth. Call that out explicitly so that the author isn’t left hanging wondering on what order of depth they should consider your review.

#### **As an author**

Respond to your review in a timely fashion to allow for new cycles. Use something like [Trailer](http://ptsochantaris.github.io/trailer) to keep a track of notifications. Don’t just accept the feedback and change your code. Work through the trade-offs and explain advantages of your approach wherever possible. In times of conflict, apply [this](https://google.github.io/eng-practices/review/reviewer/standard.html#conflicts).

Consider using a template like this to describe your PR. Specifically Because and This addresses. Make good use of images and gifs wherever possible. Add implementation notes \(or comments\) so that the reviewer doesn’t have to check in with you about non-obvious design decisions. Wherever possible, link to the issue or card or story on the top of your description.

### References

* [https://conventionalcomments.org](https://conventionalcomments.org/)
* [http://ptsochantaris.github.io/trailer](http://ptsochantaris.github.io/trailer/)
* [https://google.github.io/eng-practices/review](https://google.github.io/eng-practices/review)

