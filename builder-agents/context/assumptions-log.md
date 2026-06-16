# Assumptions Log

*This document tracks the assumptions baked into Pawprint's design. Each assumption should be named explicitly so it can be challenged, tested, and updated as we learn. An assumption that turns out to be wrong should not be deleted — it should be marked and the correction recorded.*

*Format: assumption → why we're making it → what would need to be true → risk if wrong*

---

## Signal Detection

**A1. Customers reveal lifecycle signals naturally in support chats**
- Why we're assuming this: Elizabeth's transcript is the model case — she mentioned "first puppy, first pet ever" organically during a delivery inquiry
- What needs to be true: Customers are comfortable sharing personal context during support interactions, even when it's not directly relevant to their issue
- Risk if wrong: Signal detection has no input to work from; the entire trigger mechanism fails

**A2. The support chat transcript contains enough signal to identify the lifecycle event with confidence**
- Why we're assuming this: One sentence from Elizabeth was sufficient. The signal was unambiguous.
- What needs to be true: Lifecycle signals, when present, are explicit enough that an AI agent can identify them reliably without high false-positive rates
- Risk if wrong: The Signal Detector agent triggers incorrectly (wrong event identified) or misses events entirely

**A3. Post-chat processing is sufficient — real-time detection is not required for MVP**
- Why we're assuming this: The email doesn't need to arrive during the chat; arriving within 24-48 hours of the conversation is timely enough to feel relevant
- What needs to be true: Customers remain in the lifecycle moment for at least a few days after the signal is detected
- Risk if wrong: The moment passes too quickly; by the time the email arrives, it feels late

---

## Customer Behavior

**A4. Elizabeth will open a triggered email within 24-48 hours of the support chat**
- Why we're assuming this: She's in an active, engaged state as a new puppy owner; her inbox attention is high; a relevant subject line will land
- What needs to be true: The email arrives while she's still in week-one mode and the subject line signals relevance clearly
- Risk if wrong: Open rate is low; the email doesn't reach her when it matters

**A5. Elizabeth will find an email — not an in-app notification or SMS — the right channel for this content**
- Why we're assuming this: Email is appropriate for longer-form, curated content packages; SMS is too brief; in-app assumes she's already in the retailer's app
- What needs to be true: Elizabeth checks email regularly and associates it with this type of content
- Risk if wrong: Email is the wrong channel; the content doesn't reach her where she actually pays attention

**A6. Elizabeth will not feel that the email is intrusive or that her support chat was "mined" for personal data**
- Why we're assuming this: The email will feel helpful, not surveillance-driven, because its content is genuinely useful and the timing feels natural
- What needs to be true: The email tone and content are warm and useful enough that the trigger mechanism is invisible
- Risk if wrong: Elizabeth feels uncomfortable that the retailer used something she said in passing; trust is damaged rather than built

---

## Content & Personalization

**A7. A combination of blog content, product recommendations, and sponsored results is the right email composition**
- Why we're assuming this: These three asset types cover the three things Elizabeth needs: information, products to buy, and curated third-party signals
- What needs to be true: The combination doesn't feel incoherent or like a dumping ground; the email has a clear through-line
- Risk if wrong: The email feels like a marketing grab bag rather than a curated care package

**A8. Breed-specific content (golden retriever) meaningfully increases relevance for Elizabeth**
- Why we're assuming this: Breed is a strong identity signal for dog owners; content that speaks to her specific breed will feel more personal than generic puppy content
- What needs to be true: We have (or can generate) breed-specific content that is genuinely useful, not just cosmetically personalized ("great news for golden retriever owners!")
- Risk if wrong: Breed-specific content is thin and the personalization feels forced

---

## Technical

**A9. The retailer has a content library and product catalog that is rich enough to curate from**
- Why we're assuming this: We are building a mock content library and product catalog as part of the MVP data layer
- What needs to be true: The mock data is realistic enough to simulate a genuine curation decision by the agent
- Risk if wrong: The agent has nothing meaningful to choose from; output looks templated regardless of the signal

**A10. A single email per lifecycle event is the right delivery model for MVP**
- Why we're assuming this: Simplicity; one email proves the concept without introducing sequencing, timing, and suppression logic
- What needs to be true: One well-crafted email is enough to validate that the content is relevant and the customer would engage
- Risk if wrong: One email undersells the potential; a series of emails over the first week might be the more natural product shape

---

*Last updated: 2026-06-14*
*Add new assumptions as they surface. Flag assumptions that have been tested or invalidated.*
