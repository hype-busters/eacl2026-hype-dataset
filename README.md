# Hype Dataset

We present our dataset for promotional language detection in biomedical funding proposals, introduced in our EACL2026 paper ["Hype or not? Formalizing Automatic Promotional Language Detection in Biomedical Research"](https://aclanthology.org/2026.eacl-long.328/).

This dataset contains 1200 sentences containing potential hype adjectives, where 917 sentences are deemed as Hype, and 353 Not Hype.
These sentences were extracted from NIH grant application corpus.

## Guidelines
Each sentence contains a hype adjective candidate which was annotated following the guidelines proposed in the paper.
Proposed guidelines can be found [here](https://kansaineil.github.io/hype-annotation-guidelines-eacl26/).

## Data

| Group        | Hype   | Not Hype | Total |
| :----------- | ------:| --------:| -----:|
| Novelty      | 392    | 145      | 537   | 
| Rigour       | 525    | 208      | 733   |
| Total        | 917    | 353      | 1270  |

For more statistics on the dataset, please refer to our paper.

For each sentence, we include:
- The potential hype adjective annotated.
- The binary decision: 1 for hype, 0 for not hype.
- Rationale decisions: A list containing rationales annotated. They can be any of the five described in our paper, i.e., hyperbolic, gratuitous, amplified, coordinated, and broader context)
- Privacy tag: 1 if sample was anonymized, 0 if it was not.

## Anonymization
Our goal is to analyze language as a legitimate object of scientific study, not criticizing individual authors for using or not using promotional language in their writing. Therefore, we manually inspected all the sentences in our dataset and replaced any individual identifiers, such as names and affiliations, with generic placeholders, e.g.: 

> As a result, Dr. A has an unparalleled view of laboratory based aging research at Institute B to enhance mentee research training and career development of junior investigators.

A total of 228 sentences were flagged with individual identifiers, representing around 18% of the dataset.

Results presented in our paper use the non-anonymized version of this dataset. While do not expect this process to significantly impact the overall results presented, the anonymized version is likely to lead to different performances for some models.

We reckon that there are better ways of anonymizing the data to produce more natural sentences. We will improve this process in further iterations of the dataset.

## Acknowledgements
This paper was supported by grant No. 25K00851 from the Japan Society for the Promotion of Science. Additionally, this paper is based on results obtained from project JPNP25006, commissioned by the New Energy and Industrial Technology Development Organization (NEDO).

## Cite us, please :)
If you use our guidelines to annotate more data or use our dataset, please cite our paper:

```
@inproceedings{batalo-etal-2026-hype,
    title = "Hype or not? Formalizing Automatic Promotional Language Detection in Biomedical Research",
    author = "Batalo, Bojan  and
      Shimomoto, Erica K.  and
      Satav, Dipesh  and
      Millar, Neil",
    editor = "Demberg, Vera  and
      Inui, Kentaro  and
      Marquez, Llu{\'i}s",
    booktitle = "Proceedings of the 19th Conference of the {E}uropean Chapter of the {A}ssociation for {C}omputational {L}inguistics (Volume 1: Long Papers)",
    month = mar,
    year = "2026",
    address = "Rabat, Morocco",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2026.eacl-long.328/",
    doi = "10.18653/v1/2026.eacl-long.328",
    pages = "6979--6992",
    ISBN = "979-8-89176-380-7",
    abstract = "In science, promotional language ({'}hype') is increasing and can undermine objective evaluation of evidence, impede research development, and erode trust in science. In this paper, we introduce the task of automatic detection of hype, which we define as hyperbolic or subjective language that authors use to glamorize, promote, embellish, or exaggerate aspects of their research. We propose formalized guidelines for identifying hype language and apply them to annotate a portion of the National Institutes of Health (NIH) grant application corpus. We then evaluate traditional text classifiers and language models on this task, comparing their performance with a human baseline. Our experiments show that formalizing annotation guidelines can help humans reliably annotate candidate hype adjectives and that using our annotated dataset to train machine learning models yields promising results. Our findings highlight the linguistic complexity of the task and the potential need for domain knowledge. While some linguistic works address hype detection, to the best of our knowledge, we are the first to approach it as a natural language processing task. Our annotation guidelines and dataset are available at https://github.com/hype-busters/eacl2026-hype-dataset."
}
```

## 
Proposal abstracts were obtained through the NIH RePORTER tool. All original abstracts are publicly available. We follow NIH standards and release our dataset under the same license (ODC Open Database License (ODbL) v1.0).
