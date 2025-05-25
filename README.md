# Aspect Detection and Classification in Historical Travel Literature  
*A study on Prompting Strategies and the Diachronic Influence of Language on Generative AI Performance*

**Authors**  
- Tess Dejaeghere ([ORCID](https://orcid.org/0000-0001-6330-4958)) – GhentCDH, Ghent University  
- Salvador Ros ([ORCID](https://orcid.org/0000-0002-8472-4457)) – CLARIAH-UNED, UNED  
- Julie Birkholz ([ORCID](https://orcid.org/0000-0003-1193-0847)) – GhentCDH, Ghent University  

## Overvie
This project explores how Generative AI models, particularly Large Language Models (LLMs), perform in the task of **aspect recognition and classification** in historical travel literature. It focuses on two main variables:

1. **Prompting Strategies** (zero-shot, few-shot, chain-of-thought)
2. **Diachronic Variation in Language**, analyzing texts from the 18th, 19th, and 20th centuries.

Our objective is to understand how different prompt designs and linguistic characteristics across time periods affect the performance of LLMs on information extraction tasks relevant to the Digital Humanities (DH).

## Research Questions

1. Which prompting strategies are most effective for aspect detection and classification?
2. Do LLMs perform better on more recent, standardized texts or equally well on older, historical texts?
3. Does model performance vary across different aspect categories?

## Methodology

- **Corpus**: Annotated English travel literature from the 18th to 20th centuries (Dejaeghere & Singh, 2024).
- **Entity categories**: PERSON, LOCATION, ORGANISATION, FAUNA, FLORA, BIOME, HUMAN_LANDFORM, NATURAL_LANDFORM, NATURAL_PHENOMENON, WEATHER, MYTH.
- **Models tested**: LLaMA 3.3 70B.
- **Prompting strategies**: Zero-shot, few-shot, and chain-of-thought.
- **Evaluation**: Precision, recall, F1 score using [Nervaluate](https://github.com/MantisAI/nervaluate).
- **Statistical tests**: Kruskal-Wallis, Mann-Whitney U. andDunn Test

## Key Findings

- Overall, statistical significance for prompting strategies is mainly observed for recall across several evaluation schemes. Most entity aspects—including Person, Organisation, Fauna, Flora, Biome, Natural Landform, Weather, and Myth—do not exhibit significant differences across prompt types, with the exception of Human Landform. Nevertheless, the findings using Mann-WhitnCey U & Dunn Tests sre robut and consistent.

1. One-shot prompting appears to help models recover more relevant entities
2. In structured tasks like NER, simple prompts can outperform more complex reasoning-based formats like chain-of-thought

Simpler may mean better—especially if exhaustiveness (recall) is the goal

- In the case of variation across centuries, clear global significance emerges, with all aspects showing statistically significant differences. Applying Mann-Whitney U and Dunn tests reveals that century exerts a distinct influence on each aspect, affecting them in different ways.
1. Models detect roughly the same number of relevant aspects across centuries (recall), but they are less accurate and consistent in earlier texts (precision/F1).
2. This suggests that historical language variation impacts precision more than recall.
3. Post hoc tests confirmed lower performance in 18th-century texts compared to 19th and 20th.

So for Diachronism: FIND INSPIRATION

## Dataset

The dataset is a curated corpus of multilingual non-fictional travelogues annotated for aspect-based sentiment analysis. It includes 12 detailed entity categories and achieves high annotation reliability (Fleiss’ kappa = 0.88). It is designed to support both NLP and literary-historical analysis.

## Reproducibility

All data, Jupyter Notebooks, and Python code used in this study will be released in accordance with **FAIR** and **Open Science** principles.

## References

- Dejaeghere, T. & Singh, P. (2024). *Exploring Aspect-Based Sentiment Analysis Methodologies for Literary-Historical Research Purposes*. [LREC-COLING 2024](https://lrec-coling-2024.org/conference-program/)
- OpenAI (2024), Anthropic (2023), Google (2024), Amazon (2023)
- Batista, D. (2019). [Nervaluate: NER Evaluation Considering Partial Match Scoring](https://github.com/MantisAI/nervaluate)

## Contact

- Tess Dejaeghere – tess.dejaeghere@ugent.be  
- Salvador Ros – sros@scc.uned.es  
- Julie Birkholz – julie.birkholz@ugent.be

