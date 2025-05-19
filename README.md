---
license: mit
task_categories:
- question-answering
language:
- en
pretty_name: RAGuard
size_categories:
- 10K<n<100K
---

# Dataset Card for RAGuard


## Dataset Details

```RAGuard``` is a fact-checking dataset designed to evaluate the robustness of RAG systems against misleading retrievals.
It consists of 2,648 political claims made by U.S. presidential candidates (2000–2024), each labeled as either *true* or *false*, and a knowledge base comprising 16,331 documents. Each claim is linked to a set
of associated documents, categorized as *supporting*, *misleading*, or *unrelated*

### Dataset Description

```claims.csv``` contains the following fields for each claim, scraped from [PolitiFact](https://www.politifact.com/).

1. Claim ID
2. Claim: Full text of the claim
3. Verdict: Binary fact-checking verdict, *True* or *False*
4. Document IDs: List IDs of documents corresponding to this claim
5. Document Labels: List of labels for the associated documents, either *supporting*, *misleading*, or *unrelated*

```documents.csv``` contains the following fields for each document in our knowledge base, scraped from [Reddit](https://www.reddit.com/).

1. Document ID
2. Title: Reddit post title
3. Full Text: Content of the document
4. Claim ID: ID of the corresponding claim
5. Document Label: Label for the document's label to the claim, either *supporting*, *misleading*, or *unrelated*
6. Link: URL to the original document

### Dataset Source and Usage

- See Section 2.4 of our paper for supported tasks

# Disclaimer

This dataset has been compiled from publicly available sources on the Internet. It may contain discussions on sensitive political topics, including viewpoints that some individuals may find controversial or offensive. The inclusion of any content does not imply endorsement of any views expressed. Users are advised to exercise discretion and ensure compliance with applicable ethical guidelines and legal frameworks when using this dataset.
