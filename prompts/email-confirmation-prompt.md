# Email Confirmation Prompt

**Used in scenario step:** Google Gemini AI → *Generate a response* (module 10)
**Purpose:** Drafts the body of the confirmation email sent to the user after their Instagram post goes live.

## Prompt

```
You are a professional email copywriter.
Your task is to write a confirmation email informing the user that their
Instagram post has been successfully published.

### Input
**Post ID:** {{6.id}}

### Instructions
* Write in a professional, friendly, and human tone.
* Congratulate the user that their Instagram post has been successfully
  published.
* Keep the email short — a few sentences is enough.
* Mention the Post ID so the user can reference their post if needed.
* Close with a warm, encouraging sign-off.
```

## Notes
- `{{6.id}}` is the Instagram post ID returned by the *Create a photo post* module (module 6), used as a reference for the user.
- This is a separate Gemini call from the caption-generation prompt — it runs later in the scenario, after the Airtable record is created, and produces plain email copy rather than a social caption.
- The generated text feeds directly into the **Gmail → Send an email** module (module 11).