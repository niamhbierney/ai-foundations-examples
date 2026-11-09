# AI Foundations: Four Practical Examples

A short evidence log exploring tokenisation, context windows, temperature, and hallucinations.

> **Evidence note:** This page separates verified examples from demonstrations and items still awaiting a measurement. It does not present an unperformed test as a real observation.

## 1. Tokenisation — measurement pending

**Test sentence**

> Artificial intelligence uses patterns in data to generate responses, but it does not always understand facts.

**How to verify:** Paste the sentence into the [OpenAI Tokenizer](https://platform.openai.com/tokenizer), select the relevant model/encoding if prompted, and record the displayed token count here.

**Result:** _Awaiting tokenizer measurement._

**What it shows:** A language model processes text as tokens, which can be whole words, parts of words, punctuation, or other text units. Token count is not necessarily the same as word count.

Source: [OpenAI Help Center — What are tokens and how to count them?](https://help.openai.com/en/articles/4936856-what-are-tokens-and-how-to-count-them)

## 2. Context window — reproducible test, personal example pending

**Test:** Start a long conversation with an AI assistant. Add a specific instruction or fact near the beginning. Continue with enough unrelated material to approach or exceed the model's available context. Then ask the assistant to recall the original detail.

**Expected observation:** If the original detail is no longer available in the model's active context, the assistant may omit it, misremember it, or ask for it again. This is a context limitation, not necessarily a failure to understand the original sentence.

**Evidence status:** This is a reproducible test procedure, not a claim that a particular overflow event has already been observed in this project. Add a dated transcript or screenshot after running it.

**What it shows:** A context window limits how much input and conversation history a model can use at one time. Long conversations may require older material to be left out or summarised.

Further reading: [OpenAI — Model context and token limits](https://platform.openai.com/docs/models)

## 3. Temperature — qualitative comparison

**Same task:** “Suggest a name for a small creative coding club for children.”

**Straightforward response:** “Code Club”

**More playful response:** “Pixel Pioneers”

**What it shows:** Generative models can produce different plausible outputs for the same task. Temperature is a sampling setting that can influence how varied or predictable outputs are.

**Important limitation:** This is an illustration of different response styles, not a controlled experiment in which the model's temperature parameter was directly changed. To test temperature properly, use the same model and prompt, change only the temperature setting, and compare several outputs at each setting.

Further reading: [OpenAI API — Text generation and sampling parameters](https://platform.openai.com/docs/guides/text-generation)

## 4. Hallucination — Google Bard and the James Webb Space Telescope

In a February 2023 promotional demonstration, Google Bard answered a question about discoveries from the James Webb Space Telescope (JWST). It claimed that JWST had taken the first pictures of a planet outside our solar system. That attribution was wrong: the European Southern Observatory's Very Large Telescope captured the first confirmed direct image of an exoplanet in 2004. JWST did later capture its own direct image of an exoplanet in 2022.

**What gave the error away?**

1. **Factual contradiction:** the claim that JWST took the first-ever image conflicts with the earlier 2004 observation.
2. **Specific but incorrect attribution:** the answer named a telescope and a scientific achievement, making the statement sound authoritative.
3. **Confident presentation:** the claim was delivered as a fact rather than flagged as uncertain or checked.

**What it shows:** A fluent, confident answer can still contain a false factual claim. Important claims should be checked against reliable primary sources.

Sources:
- [Reuters / Euronews — Google AI chatbot Bard gives wrong answer in promotional video](https://www.euronews.com/next/2023/02/08/google-ai-chatbot-bard-gives-wrong-answer-in-promotional-video)
- [European Southern Observatory — First direct image of an exoplanet](https://www.eso.org/public/news/eso_multiple_planets/)
- [NASA — Webb captures its first image of an exoplanet](https://science.nasa.gov/missions/webb/webb-captures-its-first-image-of-an-exoplanet/)

---

## Reflection

These examples highlight four different parts of working with generative AI:

- **Tokens** are the units the model processes.
- **Context** limits how much information can be considered at once.
- **Temperature** can influence variation in generated responses.
- **Hallucinations** remind us to verify factual claims, especially specific dates, names, and attributions.

## Evidence to add before calling this complete

- [ ] Record the exact token count from the OpenAI Tokenizer for the test sentence above.
- [ ] Run the context-window test and add a genuine dated example (transcript excerpt or screenshot).
- [ ] If conducting a temperature experiment, record the model, prompt, temperature settings, and outputs so the comparison is reproducible.
