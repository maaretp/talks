# Working through uncertainty: collaborative learning of AI

_Length: 40 min_
_Presented by: Aryadevi and Maaret_

Already before the age of AI, testing field was split in two: the test-case oriented view of verification and validation, and the exploratory view of learning through testing. The former is anchored to requirements, the latter is anchored to discovery. The former is about checking against a known target, the latter is about finding the target in the first place. The difference is grounded in uncertainty. 

In this talk, we share introduce you to five patterns of uncertainty we discovered from collaborative learning of AI, coming from the two worlds of testing. The five patterns of uncertainty we needed to work through are: 
- Change 1: The Specification Lives in Your Head and AI Guesses It
- Change 2: The Code Looks Right Even When It Is Wrong
- Change 3: You Cannot Verify What You Cannot See
- Change 4: Validation Used to Have a Finish Line - Now It Never Ends
- Change 5: You Are Now Simultaneously Too Close and Too Far

AI amplifies uncertainty that exploratory testing thrives in. Learning techniques from exploring help us on our journey on learning of AI. We share how we have adapted our thinking and practices to work through them. 

The frame of our learning has been vibe coding and testing with AI. None of the work starts with requirements. The work brings along task expansion of expecting to beyond our usual roles. 

Join us to learn about the insights we needed to name and discuss to fast-track your journey on a major change in testing. 

---


We have been learning together collaboratively and independently to do things in testing with AI:

- We vibe code applications that help us outsource data from our heads to the computer
- We test application with playwright agents
- We do AI-based quality audits of code and applications
- We create test artifacts with AI

In this talk, we distill our lessons into learnings the audience can take home. Our recipes and examples help you find yourself on the AI journey and give you options on how to grow. We ground our sharing on collaborative learning that brought the two of us together on AI learning, and bring you perspectives from individual as well as mutual learning journey.

What will learn:
- Architecture-aware mindset for testing with AI
- Importance of knowing what is good enough to be in control of AI
- Changing ideas of verification and validation: comparing intent and result 


----
'task expansion' - what does it require, or what your puzzled with when you work on areas you have never worked on before? 

unlimited ideas, agreeing what is right. We used to expect someone would tell us that. 


---

Change 1: The Specification Lives in Your Head  and AI Guesses It



Traditional world:

Spec was written down
Verification compared code to document
If spec said "date format DD/MM/YYYY" - tester checked that. Simple.
In vibe coding world:

You said "date picker" -AI built something
But did you mean past dates allowed? Future only? What timezone? Mobile friendly?
AI filled your silence with assumptions
You don't even know what assumptions were made until something breaks in production
The change: Verification used to be checking against a document. Now it is excavating assumptions you didn't know were made.

 

Change 2: The Code Looks Right Even When It Is Wrong

Traditional world:

Human-written bugs were often visible -wrong variable, missing condition, obvious logic gap
A code review or basic test caught them
The code looked wrong when it was wrong
In vibe coding world:

AI writes fluent, clean, well-structured code
It passes linting. It compiles. It runs.
But it might handle an edge case incorrectly -and the code looks so clean you never question it
You trust the cleanliness of the output instead of questioning its correctness
 

example in my context base:

You ask AI to build email confirmation. AI builds it perfectly : sends email, shows success message.

But what if the email sending fails silently? The user sees "email sent!" but receives nothing. The code is beautiful. The behavior is wrong. And it looked right the whole time.

The change: Verification used to be finding where code was obviously broken. Now it is finding where code is subtly wrong beneath a confident surface.

 

Change 3: You Cannot Verify What You Cannot See

Traditional world:

Tester could read the code, trace the logic, understand every step
Verification was possible because the system was transparent
You could follow the path from input to output
‘In vibe coding world:

If your website uses an AI feature -a chatbot, a recommendation, a content generator like you cannot see inside it
You give it an input. You get an output. The middle is a black box.
You can only verify at the edges , what goes in and what comes out
You cannot verify the reasoning, only the result
And here is the deeper problem : you might also not fully understand the non-AI code AI wrote for you. You vibe coded it. It works. But if it breaks in an unexpected way, can you trace exactly why?

The change: Verification used to assume full visibility into the system. Now it requires testing at the boundaries of things you cannot fully see.

 

Change 4: Validation Used to Have a Finish Line - Now It Never Ends

Traditional world:

Build → Test → Validate → Ship → Done
Validation was a phase. You completed it. You moved on.
The system you validated stayed the same after you validated it.
In vibe coding world:

You validated your website last month
But you are using an AI API -and the model behind it was quietly updated
Your website now behaves slightly differently - and you did not change a single line of code
Or you added one new feature with AI -and it subtly changed how another feature behaves
Validation has no finish line anymore.

Think about your booking website again. You validated it works for desktop users. Then you add an AI chatbot feature. The chatbot gives users advice. Now validation must include: is the advice good? Is it accurate? Is it appropriate? These are entirely new validation questions that did not exist before you added that one feature.

The change: Validation used to be a phase before shipping. Now it is a permanent habit after shipping.

 

Change 5: You Are Now Simultaneously Too Close and Too Far

This is the most personal change for solo vibe coders  and the most honest one to share in your speech.

Traditional world:

The person who built it did not test it
Fresh eyes caught what familiar eyes missed
Separation of roles created natural distance and objectivity
Your vibe coding world:

You built it, so you know what it is supposed to do which means you test what you expect, not what is really there
But you also partly do not understand it, because AI built parts you did not write line by line
You are simultaneously too familiar to test objectively and too unfamiliar to verify deeply
This is a completely new cognitive position that no traditional testing methodology prepared anyone for.

The change: V&V used to rely on role separation to create objectivity. Now solo vibe coders must manufacture their own objectivity — through personas, delay, AI assistance, and deliberate adversarial thinking.

has context menu
Replying to external participants.


