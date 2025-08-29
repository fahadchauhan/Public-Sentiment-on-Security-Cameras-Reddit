# Public Sentiment on Security Cameras – Reddit

This repository presents a detailed analysis of public sentiment toward surveillance cameras, based on discussions from Reddit. The dataset spans 2010–2020 and includes posts from five subreddits: **AskEurope, AskReddit, privacy, security, and technology**. The analysis leverages natural language processing techniques for aspect-based sentiment analysis and trend discovery.

This work serves as a follow-up to our earlier study on Suomi24 (Finland’s largest online forum, 2000–2020), enabling cross-platform comparison of surveillance discourse.

---

## Data Processing Workflow

1. **Data Acquisition**

   * Reddit submissions and comments were collected for the years 2010–2020 using targeted surveillance-related keywords (e.g., *CCTV surveillance, security camera, public camera privacy*).
   * Data covers five subreddits: *AskEurope, AskReddit, privacy, security, technology*.

2. **Data Filtering**

   * Discussions were filtered to retain only those relevant to surveillance technologies.
   * Thread titles and body text were combined for context preservation in submissions.

3. **Data Cleaning**

   * Removal of special characters, HTML entities, and extraneous symbols.
   * Expansion of contractions (e.g., *can’t → cannot*).
   * Lowercasing and normalization of text.
   * Manual review of a sample (\~20%) to check data quality.

4. **Preprocessing**

   * Stopword removal.
   * Lemmatization of words.
   * Preservation of contextual cues for sarcasm, slang, and informal speech (particularly common on Reddit).

---

## Analysis and Visualization

The repository includes Jupyter notebooks for key analysis steps:

* **Trends**: Yearly and monthly patterns in surveillance-related discussions.
* **Heatmaps**: Visualization of activity intensity across time.
* **Keyword Frequencies**: Tracking the prominence of specific terms.
* **Hypothesis Assignment**: Mapping posts to predefined hypotheses (H0–H7).
* **Sentiment Analysis**: Using SentiStrength to classify sentiments as positive, negative, or neutral.
* **Aspect Trends**: Visualization of sentiment evolution for each hypothesis.

---

## Hypothesis Framework and Sentiment Analysis

We tested the same set of hypotheses (H0–H7) as in the Suomi24 study to allow cross-platform comparability:

* H0: Personal encounters with cameras influence perceptions.
* H1: Sentiment varies by camera placement.
* H2: Technical shortcomings drive dissatisfaction.
* H3: Cameras are seen as enhancing security.
* H4: Camera density shapes public opinion.
* H5: Surveillance in public spaces triggers privacy concerns.
* H6: Cameras contribute to crime reduction and deterrence.
* H7: Trust depends on transparency and accountability.

**Embeddings**: Posts and hypotheses were embedded using Snowflake Arctic embeddings, with assignment via cosine similarity. Ambiguous cases were refined using Empath emotion embeddings.

**Sentiment Analysis**: Classified with **SentiStrength**, optimized for short, informal social media texts.
