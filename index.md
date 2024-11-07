
# JOKER
<p align="center">
  <img src="joker.png" width="120" height="142">
</p>

{% include navbar.md %}

<br>
  <h1 align="center">CLEF 2024 JOKER Track:</h1>
  <h2 align="center">Automatic Humour Analysis</h2> 

## Abstract

Over the last years, the JOKER Track has created an active community of researchers in NLP and IR working together on non-literal use of language in text—which is still challenging for both AI models and humans as it requires understanding implicit cultural references or double meanings. Its benchmarks on humorous text analysis, retrieval, and translation have become standard references. We propose significant changes in the track’s setup and tasks. The CLEF 2025 JOKER track will contain the following 3+1 tasks: 

- **Task 1 (Humor-aware Information Retrieval):** retrieve short humorous texts for a query. 
- **Task 2 (Wordplay Translation):** translate puns from English to French. 
- **Task 3 (Funny Names):** detect and translate pun names. 
- **Task 4 (Controlled Creativity):** identify and avoid hallucination.
  The JOKER lab aims to bring together linguists and computer scientists to create reusable test collections to foster work on automatic humor analysis. To encourage research in humor-aware information retrieval, JOKER 2024 introduced a new task that focuses on retrieving short humorous texts from a document collection. 

The intended use case is to search for a joke on a specific topic. This can be useful for:
- Humor researchers in the humanities,
- Second-language learners as a learning aid,
- Professional comedians as a writing aid,
- Translators who might need to adapt certain jokes to other cultures.

## 1. Title, Description, and Relevance

We propose to retain the now well-established title: **CLEF 2025 JOKER Track: Automatic Humor Analysis**.

State-of-the-art AI, NLP, and IR models are still not able to handle humor or other non-literal aspects of text naturally (Ermakova et al., 2023a). Specifically, tasks like wordplay detection or analysis, which can involve the surface structure or orthography of a word or its pronunciation, present significant challenges.

These tasks rely on word surface aspects that are not captured in the deep semantic embeddings of modern AI models. Current pre-training models, which are based on next-word prediction objectives, also fail to account for these non-literal language features.

## 2. Use Case

Humor is one of the most important aspects of social interaction. Despite significant advances in AI and NLP, understanding humor remains a challenge, as it often involves grasping implicit cultural references and/or double meanings. 

The goal of the JOKER lab is to bring together linguists and computer scientists to create reusable test collections that foster work on automatic humor analysis.

To encourage research in humor-aware information retrieval, JOKER 2024 introduced a new task aimed at retrieving short humorous texts from a document collection. 

The intended use case is to search for a joke on a specific topic. This can be useful for:
- Humor researchers in the humanities,
- Second-language learners as a learning aid,
- Professional comedians as a writing aid,
- Translators who need to adapt jokes for different cultures.
### 3.1 Task 1: Humor-aware Information Retrieval

The goal of this task is to retrieve short humorous texts from a document collection based on a given query. The retrieved texts must meet two criteria: they should be relevant to the query and involve wordplay. A typical use case would be searching for a joke on a specific topic – for example, a query for "math" would aim to find math-related jokes, while a query for "Tom" would seek jokes about someone named Tom.

The data for this task is an extension of the dataset used in JOKER 2023’s wordplay detection task in English, annotated for humor. This has been expanded with data from Task 3 (Translation) (Ermakova et al., 2023d, 2024c). We grouped the humorous texts into topic-based clusters and created queries accordingly. Additionally, we included a significant amount of topically relevant, non-humorous texts by extracting passages from Wikipedia and generating text using Meta’s Llama-2 (7B) models. Due to the number of queries, a large fraction of the corpus is non-relevant content.

For evaluation, we use standard information retrieval metrics: MRR, Precision, and NDCG at early ranks, and MAP for overall retrieval effectiveness. We evaluate both humor relevance and topical relevance.

### 3.2 Task 2: Wordplay Translation

This task involves translating English puns into French, aiming to preserve both the form and meaning of the original wordplay as much as possible. This is a challenge for both modern machine translation (MT) models and professional human translators, making it an interesting task for professionals and students alike. This allows us to involve many translation students and professionals, contributing to the creation of a large, high-quality corpus.

The training data for Task 2 consists of 1,405 English wordplays with 5,838 professional French translations. The test data includes 4,501 English wordplays. This task builds on previous years of the JOKER track (Ermakova et al., 2024c), and we have already collected over 1,000 new translations, often with multiple references, for use in 2025.

We will provide a range of standard MT evaluation metrics, such as BLEU, METEOR, COMET, and BERTScore. Additionally, trained experts will manually evaluate system translations based on criteria like lexical field preservation, sense preservation, wordplay form preservation, style shift, humor shift, and errors in syntax or word choice. Runs will be ranked by the number of successful translations that preserve both the form and sense of the original wordplay.


## How to Cite
If you extend or use this work, please cite the [paper](https://link.springer.com/chapter/10.1007/978-3-031-13643-6_27) where it was introduced:

> Liana Ermakova, Anne-Gwenn Bosser, Tristan Miller, Tremaine Thomas-Young, Victor Manuel Palma Preciado, Grigori Sidorov, and Adam Jatowt. *[CLEF 2024 JOKER lab: Automatic humour analysis.](https://link.springer.com/content/pdf/10.1007/978-3-031-56072-9_5.pdf)* In Nazli Goharian, Nicola Tonellotto, Yulan He, Aldo Lipani, Graham McDonald, Craig Macdonald, and Iadh Ounis, editors, _[Advances in Information Retrieval: 46th European Conference on Information Retrieval, ECIR 2024, Glasgow, UK, March 24–28, Proceedings, Part VI](https://link.springer.com/book/10.1007/978-3-031-56072-9)_, volume 14613 of Lecture Notes in Computer Science (ISSN 0302-9743), pages 36–43, Cham, March 2024. Springer. ISBN 978-3-031-56072-9. DOI: [10.1007/978-3-031-56072-9_5](https://dx.doi.org/10.1007/978-3-031-56072-9_5).


<p>
<em>This project has received a government grant managed by the National Research Agency under the program "Investissements d'avenir" integrated into France 2030, with the Reference ANR-19-GURE-0001.</em>
</p>
<p>
<em>JOKER is supported by The Human Science Institute in Brittany (MSHB)</em>
</p>
<div align="center">
  <a href="https://www.mshb.fr"><img src="img/mshb.jpg" height="120"></a>
  <a href="https://sea-eu.org/?lang=fr"><img src="img/sea-eu.png" height="120"></a>
  <a href="https://www.gouvernement.fr/le-programme-d-investissements-d-avenir"><img src="img/Logotype France 2030.jpg" height="120"></a>
</div>
<br />
<div align="center">
  <a href="https://clef2022.clef-initiative.eu/index.php"><img src="img/clef2024.png" height="90"></a> 
</div>
