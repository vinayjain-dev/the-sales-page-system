# Email templates (fill-in)

Plain text, from the seller, short lines, one link repeated two or three times, and the guarantee in the P.S. Fill in
every `{{PLACEHOLDER}}`. If a placeholder has no true answer, cut the line that needs it. Run every email through the
honesty gate in `SKILL.md` section 6 before you send it.

**Schedule**

| Sequence | Who gets it | When |
|---|---|---|
| 1. Fulfillment (welcome) | every buyer of the front-end product | immediately after purchase |
| 2. Upsell follow-up (5 emails) | buyers who did not take the upsell | one per day for 5 days |
| 3. Non-buyer (4 emails) | people who opted in but did not buy | one per day for 4 days |
| 4. Book-a-call (3 emails) | engaged buyers you can actually help one-to-one | spaced 2 to 3 days apart |

Use `{{FIRST_NAME}}` in the greeting if the sending tool supports it. If not, write "Hey there,".

---

## 1. Fulfillment (welcome email, sent instantly)

**Subject:** Welcome to {{PRODUCT_NAME}}

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here, and I'd like to welcome you to {{PRODUCT_NAME}}!

You're in!

FIRST THING YOU NEED TO DO
Download {{PRODUCT_NAME}} and create your account here:
{{ACCESS_LINK}}

SECOND THING YOU NEED TO DO
Join the {{COMMUNITY_OR_RESOURCE_NAME}}:
{{COMMUNITY_LINK}}

THIRD THING YOU NEED TO DO
Check out the one next step we recommend, when you're ready:
{{UPSELL_LINK}}

By the way, {{UPSELL_NAME}} comes with a {{GUARANTEE_DAYS}}-day guarantee.
If you're not happy for any reason, reply to this email and we'll refund you right away.

If you need any help, reach us at {{SUPPORT_EMAIL}}.

To your success,
{{SELLER_NAME}}
```

Remove the "THIRD THING" block if there is no upsell page yet. Keep the guarantee line only if the guarantee is real.

---

## 2. Upsell follow-up (5 emails to buyers who did not take the upsell)

### Email 1 (day 1): why I made it

**Subject:** Why I created {{UPSELL_NAME}}

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

I just wanted to check in and see how you're getting on with {{PRODUCT_NAME}}.

I want to tell you why I made {{UPSELL_NAME}}.

After I wrote {{PRODUCT_NAME}}, people kept asking for more.
Not more theory. More detail on how it all works, step by step.

I couldn't fit all of that in the first product. It would have made it too long to be useful.

So I built {{UPSELL_NAME}}. It's designed to {{ONE_LINE_PURPOSE}}.

You can see the details here:
{{UPSELL_LINK}}

By the way, {{UPSELL_NAME}} comes with a {{GUARANTEE_DAYS}}-day guarantee.
If it isn't right for you, just reply and we'll refund you.

To your success,
{{SELLER_NAME}}
```

### Email 2 (day 2): the questions everyone asks

**Subject:** {{UPSELL_NAME}}: your questions, answered

```
Hey {{FIRST_NAME}},

Lots of people have asked me the same questions about {{UPSELL_NAME}} before they buy.

So instead of replying one by one, here are the answers to the most common ones.

Question: {{COMMON_QUESTION_1}}?
Answer: {{HONEST_ANSWER_1}}

Question: {{COMMON_QUESTION_2}}?
Answer: {{HONEST_ANSWER_2}}

Question: {{COMMON_QUESTION_3}}?
Answer: {{HONEST_ANSWER_3}}

--------------------------------------

If that answers your questions, you can get {{UPSELL_NAME}} here:
{{UPSELL_LINK}}

By the way, it comes with a {{GUARANTEE_DAYS}}-day guarantee. If you're not happy for any reason, just let me know and we'll refund you.

{{SELLER_NAME}}

P.S. If I didn't answer your question, reply to this email and ask me anything.
```

### Email 3 (day 3): the two types of buyer

**Subject:** This is for one kind of person

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

After {{PRODUCT_NAME}} went out, a lot of people wrote back with the same kind of comment:
"This helped me {{BENEFIT_THEY_SAID}}."

At first I didn't see the pattern.
Then I saw it clearly.

There are two types of people who buy {{PRODUCT_NAME}}.

Type 1 is the do-it-yourself type.
They read it, work things out on their own, and get going. Some of them are better at it than others.

Type 2 reads it, sees how much is in it, and wants to get results fast, with as few mistakes as possible.

Type 2 is the person who picks up {{UPSELL_NAME}}.
It saves time and removes the guesswork.

If you're Type 1, keep going, and reply if I can help in any way.

If you're Type 2, here it is:
{{UPSELL_LINK}}

By the way, it comes with a {{GUARANTEE_DAYS}}-day guarantee.

Talk soon,
{{SELLER_NAME}}
```

### Email 4 (day 4): a result, with proof

Use this only with a real result the buyer or the seller actually got, with a real screenshot or quote. If you have
neither yet, skip this email and send Email 5 on day 4.

**Subject:** {{SPECIFIC_RESULT_IN_PLAIN_WORDS}}

```
Hey {{FIRST_NAME}},

It's only been a few days since you joined {{PRODUCT_NAME}}, so I know you're reading it or working through it.

Either way, I want to say: great job.

I also want to share something real. {{REAL_RESULT_AND_WHEN}}.

Here's the screenshot:
{{PROOF_IMAGE_OR_QUOTE}}

How did I get there? I followed what's in {{PRODUCT_NAME}}. Go through it, and do the next step.

If you want to move faster, {{UPSELL_NAME}} walks through everything step by step:
{{UPSELL_LINK}}

{{GUARANTEE_LINE}}

Talk soon,
{{SELLER_NAME}}
```

### Email 5 (day 5): the last check-in

**Subject:** Did you want {{UPSELL_NAME}}?

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

I just wanted to ask: did you want {{UPSELL_NAME}}?

You can get it here:
{{UPSELL_LINK}}

I don't want to keep bugging you about it, so I'll leave it with you.

Either way, reply if I can help you move forward.

Talk soon,
{{SELLER_NAME}}
```

---

## 3. Non-buyer (4 emails to people who opted in but did not buy)

These replace the common "problem with your order" template. The honest version is below. Do not send any message
that claims a payment failed, a launch was blocked, or spots are running out unless it is literally true.

### Email 1 (day 1): what happened, honestly

**Subject:** Did something go wrong?

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

You were looking at {{PRODUCT_NAME}}, and I wanted to check that nothing stopped you from getting it.

If the checkout did not work, or you had a question before you bought, reply and tell me.

Here's a bit of what {{PRODUCT_NAME}} covers:

- {{CONTENT_POINT_1}}
- {{CONTENT_POINT_2}}
- {{CONTENT_POINT_3}}
- {{CONTENT_POINT_4}}

You can get it here:
{{CHECKOUT_LINK}}

It comes with a {{GUARANTEE_DAYS}}-day guarantee. If it isn't for you, just reply and we'll refund you.

To your success,
{{SELLER_NAME}}
```

### Email 2 (day 2): the questions

**Subject:** {{PRODUCT_NAME}}: questions people ask

```
Hey {{FIRST_NAME}},

People ask me the same questions about {{PRODUCT_NAME}} again and again. So here are the answers.

Who is it for?
{{HONEST_ANSWER}}

What is it about?
{{HONEST_ANSWER}}

How long does it take?
{{HONEST_ANSWER}}

Do I need experience?
{{HONEST_ANSWER}}

If that answers your question, you can get it here:
{{CHECKOUT_LINK}}

{{SELLER_NAME}}

P.S. If I didn't answer your question, reply and ask me anything.
P.P.S. It comes with a {{GUARANTEE_DAYS}}-day guarantee, no questions asked.
```

### Email 3 (day 3): what you are missing

**Subject:** What you're missing

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

Here's the honest case for {{PRODUCT_NAME}}.

Right now, you're still dealing with {{PAIN_IN_THEIR_WORDS}}.

{{PRODUCT_NAME}} gives you {{RESULT_IN_THEIR_WORDS}}, with {{REAL_HOW}}.

It isn't magic. It takes {{REAL_TIME_OR_EFFORT}}. But it's the step that most people skip.

Here it is:
{{CHECKOUT_LINK}}

{{SELLER_NAME}}

P.S. {{GUARANTEE_LINE}}
```

### Email 4 (day 4): in or out

**Subject:** In or out?

```
{{SELLER_NAME}} here.

I want to ask you a straight question.

Are you in, or are you out?

A lot of people sit in the middle. They keep thinking about it, and nothing changes.

If you want {{RESULT_IN_THEIR_WORDS}}, go here and start today:
{{CHECKOUT_LINK}}

If you don't, that's fine too. Just let it go and make a clear decision.

See you on the other side,
{{SELLER_NAME}}

P.S. {{GUARANTEE_LINE}}
```

---

## 4. Book-a-call (3 emails, to engaged buyers you will personally help)

Only send these to people who have bought, opened, or engaged, and only offer a call you will actually take. The call is
free only if it is free. Do not state member counts unless the number is real and current.

### Email 1: the swap

**Subject:** Private invitation for {{PRODUCT_NAME}} buyers

```
Hey {{FIRST_NAME}},

I have a question. If you answer it honestly, it could change things for you.

What if you and I could trade places?

I take the parts of your work that drain you. You take the result.

You don't have to know how to {{SKILL_1}}.
You don't have to know how to {{SKILL_2}}.
You don't even have to learn {{SKILL_3}}.

That's the offer, in a way. You get {{RESULT_IN_THEIR_WORDS}}, and I help you build it, step by step.

If that's something you want, book a call here:
{{CALL_LINK}}

It's a {{LENGTH}}-minute call. We look at where you are, and I tell you honestly whether I can help.

To your success,
{{SELLER_NAME}}
```

### Email 2: the call, explained

**Subject:** A free {{LENGTH}}-minute call, for {{PRODUCT_NAME}} buyers

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

I'm offering a free {{LENGTH}}-minute call to people who have {{PRODUCT_NAME}}.

On the call, we look at where you are right now, what's stopping you, and what the next step is.

If I can help, I'll tell you how. If I can't, I'll tell you that too.

Book your call here:
{{CALL_LINK}}

It's free. There's no hard sell on the call.

To your success,
{{SELLER_NAME}}
```

### Email 3: why me

**Subject:** Why I'll look at your situation myself

```
Hey {{FIRST_NAME}},

{{SELLER_NAME}} here.

I'd like to look at your situation personally.

I started where you probably are. {{ONE_LINE_OWN_STORY_THAT_IS_TRUE}}.

So I know what it's like to {{PAIN}}.

If you want to talk it through, here's the link:
{{CALL_LINK}}

To your success,
{{SELLER_NAME}}
```

---

## Checks before sending any email

- [ ] Every number, date, and deadline is true and current.
- [ ] No "problem with your order", "payment failed", "launch blocked", or "spots left" line unless it is literally true.
- [ ] The guarantee line matches the real guarantee, word for word, on the sales page.
- [ ] One link appears two or three times, not ten.
- [ ] No em dashes, no en dashes.
- [ ] The P.S. restates the guarantee or the one reason to act.
