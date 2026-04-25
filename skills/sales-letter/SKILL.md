---
name: sales-letter
description: Write a full direct response sales letter using proven frameworks, hooks, proof stacking, and close sequences.
---

# sales-letter-writer

## Trigger Description

Run this skill to write a new AI-generated sales letter using your CLF Prompt, Mad-Lib Template, and audience research. This is the execution step — writing, generating variations, and editing. Triggers on: "write my sales letter," "generate my letter," "use my CLF prompt," "run my mad lib," "edit my sales letter," "audit my copy," "10-question review," "emotional arc," "analyze my letter."

Do NOT use this skill to build the CLF prompt or research your audience. Run `sales-letter-reverse-engineer` to build the CLF Prompt and `audience-research` to complete the Input section before running this skill.

## Inputs Required

- Your completed CLF Legendary Letter Prompt (from `sales-letter-reverse-engineer` Step 5)
- Your Mad-Lib Template (from `sales-letter-reverse-engineer` Step 4)
- Your Question List (from `sales-letter-reverse-engineer` Step 4)
- Your product/service details, audience description, desired outcome, features, benefits, and offer (from `audience-research`)

---

## Process

### Step 1: Research Your Niche (Answer the Question List)

Before writing, answer the question list you generated in Step 4 of `sales-letter-reverse-engineer`. These questions define exactly what ChatGPT needs to write your letter.

You can answer the questions yourself (best results), record yourself talking through them and transcribe, or use the following prompt to get AI-generated answers as a starting point:

```
Hey ChatGPT, I need help answerin the below list of questions for my niche.

Topic = {Your Topic}

Audience = {Your Audience}

Outcome = {Your Audience Desire}

QUESTIONS =

{Insert the list of questions you created in Step 4}
```

Once answered, format your inputs like this example:

```
Topic = Ghostwriting

Product = Premium Ghostwriting Academy (PGA)

Target Audience = Burned out freelance writers or 9-5'ers

Outcome = Land your first high-ticket ($5,000) client

Features = Education, PGA's core curriculum is 8 modules approximately ~60 minutes each (text & video). Mentorship, get added to a private channel in our PGA Slack

Benefits = Our curriculum will show you exactly how to reposition yourself as a Premium Ghostwriter, create and launch an Educational Email Course for yourself, and then execute our "Free Consulting" cold outreach strategy to pitch, sell, and close Premium Ghostwriting clients.

About Me = My Name Is Nicolas Cole! Founder of Digital Press, the first ghostwriting agency for C-Level Executives & Silicon Valley Founders/Investors, called Digital Press (2016-2021). Scaled to $2M ARR & 24 full-time employees, writing on behalf of 300+ industry leaders (including Grammy-Winning musicians, Olympic athletes, NYT best-selling authors, and more). The author of The Art & Business of Ghostwriting & Co-Founder of Premium Ghostwriting Academy & Premium Ghostwriting Mastermind.
```

**Note:** More detail = better results. But don't feel like you have to answer every question exhaustively. Get the main ideas down: product, benefits, audience, who you are, the offer.

---

### Step 2: Build the CLF for Your Niche

Copy your completed answers from Step 1 into the CLF Legendary Letter Prompt — paste them into the `# Input` section where it says "User Input Goes Here."

This is your filled-in and completed Legendary Letter Prompt. Save it. You can also save the Input section separately so you can repurpose it for future CLF prompts on the same offer.

---

### Step 3: Run the CLF With ChatGPT

Open a new ChatGPT chat session.

Copy your full filled-in CLF Prompt (with inputs) and paste it into the chat. Hit enter.

ChatGPT will write the letter. The section headings will still be present in the output — you'll remove these in the editing step. Save the output to your working document.

---

### Step 4: Run the CLF With Claude and Gemini

Run the same filled-in prompt in Claude and Google's Gemini. Each LLM produces a different variation of the same structure.

- ChatGPT: 1 version
- Claude: 1 version
- Gemini: 3 versions (Gemini creates multiple drafts by default)

Total: 5 different versions to choose from.

Pick the one you enjoy reading and that best represents your product/service and target audience. Don't overthink it.

---

### Step 5: Run the "Mad Lib" Prompt

Run the Mad-Lib Template from `sales-letter-reverse-engineer` Step 4 using the prompt below. This creates one more version — a letter that follows the template structure more closely.

```
Given the below INPUT and TEMPLATE, please write a new text by filling the variables in the TEMPLATE using the INPUT context.

Your goal is to follow the TEMPLATE. But, you can make minor adaptations to the template for the context.

Avoid salesy words like "game-changer, unlock, discover, skyrocket, revolutionize, etc"

Avoid purple prose AT ALL COSTS

# INPUT =

User input goes here.

# TEMPLATE =

Sales Letter Template goes here.
```

Run this in each LLM to generate additional variations. You now have up to 10 versions to choose from.

---

### Step 6: Final Copy Edit Review (CLF #8)

Once you've selected your best version, run this in a **new chat window**. It audits the letter against Evaldo Albuquerque's 10 customer questions and checks the emotional accuracy.

```
I am going to give you a text and I want you to analyze it for me.

Act like a copywriter

Step 1: Give me a list of the fears, frustrations, goals, and aspirations Be succinct. Use 12 words or less for each point.

Step 2: Read the text and answer the following questions: Be succinct. Simple 1-2 sentences only.

- Question #1: "How is this different from everything else I've seen?"
- Question #2: "What's in it for me?"
- Question #3: "How do I know this is real?"
- Question #4: "What's holding me back?"
- Question #5: "Who/What is to blame?"
- Question #6: "Why now?"
- Question #7: "Why should I trust you?"
- Question #8: "How does it work?"
- Question #9: "How can I get started?"
- Question #10: "What do I have to lose?"

Give me the question and the answer. If a question is not answered by the text, please tell me so.

Let me know when you are ready for the text.
```

When ChatGPT prompts you for the text, paste in your selected letter. Review the results. If any question shows "not answered," edit the letter to address it and re-run the prompt.

See `references/10-customer-questions.md` for a full breakdown of what each question means and how to answer it.

---

### Step 7: Emotional Arc Analyzer (CLF #9)

Optional — run this in a new chat window to see the emotional journey your reader experiences. Helps you understand whether the persuasion arc is working.

```
Using NLP, I want you to analyze the text I provide.

Your goal is to present the emotional arc the reader experiences when reading the LTR.

List the emotions being triggered in the reader in the order they are raised.

Let me know when you are ready for the text?
```

Paste your letter when prompted. Review whether the arc moves correctly: skepticism → curiosity → problem recognition → hope → desire → action.

---

### Step 8: Emotional Arc Chart (CLF #10)

Optional — run in the same session as Step 7, after getting the emotion list:

```
Can you illustrate the emotional arc on a graph where the y axis is negative to positive emotions and the x axis is time?
```

This gives you a visual of the reader's emotional journey. A well-structured sales letter starts neutral-to-skeptical, dips into the problem, builds toward a solution, then peaks at the close.

---

### Final Step: Edit and Ship

- Read the letter out loud.
- Remove section headers from the AI output.
- Make any final edits based on the audit (Step 6).
- Ship it.

---

## Output Specification

The final output is 1 polished sales letter (~1,000 words) that:

- Answers all 10 of Evaldo Albuquerque's customer questions
- Follows the rhetorical structure of the legendary letter you modeled
- Is written in plain, direct language (no salesy words, no purple prose)
- Has section headings removed for final publication

Save your final version in your working document with the filled-in CLF Prompt and Mad-Lib Input so you can reuse both for future letters.

---

## Chaining

- **Receives from:** `sales-letter-reverse-engineer` — CLF Prompt, Mad-Lib Template, and Question List. `audience-research` — the research doc becomes the `INPUT =` section.
- **Passes to:** Nothing. This is the final step in the chain.
- **Standalone:** Yes — if you already have a CLF Prompt and inputs from prior work, run this to generate and edit the letter.
