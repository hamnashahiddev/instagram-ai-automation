# Caption Generation Prompt

**Used in scenario step:** Google Gemini AI → *Generate a response* (module 4)
**Purpose:** Converts the topic submitted via Google Forms into a short, ready-to-post Instagram caption.

## Prompt

```
analyze this topic :{{3.answers.`53f9a988`.textAnswers.answers[].value}}

You are an experienced social media copywriter and personal branding expert.
Your task is to create a professional, engaging, and human-written caption
based on the topic provided. Generate a 2–3 line caption and add 2 hashtags.
Do not generate too long a caption.
```

## Notes
- `{{3.answers.`53f9a988`.textAnswers.answers[].value}}` pulls the **Topic** field from the Google Forms response (module 3).
- Output length is intentionally constrained to 2–3 lines to keep captions scannable and platform-appropriate.
- Exactly 2 hashtags are requested to avoid a spammy, over-tagged look.