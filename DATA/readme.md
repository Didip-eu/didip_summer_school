# Dataset Overview: `mom_1000_sample.tsv`

This dataset is a sample of 1000 entries from a larger collection of historical texts, potentially charters. It provides a rich resource for various Natural Language Processing (NLP) tasks, particularly in the context of historical text analysis and teaching. This sample includes machine-translated abstracts in English, adding another dimension for NLP exploration.

## Dataset Structure

The dataset is stored in a tab-separated values (TSV) file named `mom_1000_sample.tsv`. Each row represents a single text entry, and the columns provide metadata and content information:

| Column Name                   | Description                                                               | Data Type |
| :---------------------------- | :------------------------------------------------------------------------ | :------- |
| `atom_id`                     | Unique identifier for each text entry (e.g., "AT-StiAG/GoettweigOSB/1402_IV_13"	)                                    | Object   |
| `place`                       | Location associated with the text entry (if available, e.g., "Rom")                    | Object   |
| `year`                        | Year the text entry was created (e.g., "1402")                                           | Int64    |
| `lang`                        | Language of the text ('lat' for Latin, 'de' for German)                    | Object   |
| `text`                        | Full text content (e.g., | Bonifatius episcopus, servus servorum dei, ad futuram rei memoriam. | Sincere devocionis affectus, ...)                                                           | Object   |
| `abstract`                    | Abstract or summary of the text (in original language)                    | Object   |
| `abstract_lang`               | Language of the abstract ('de' for German, 'lat' for Latin)               | Object   |
| `translated_abstract_opus`    | Machine-translated version of the abstract with Opus (in English)                 | Object   |

* There are marginal missing values in the dataset.
* The datatypes are suitable for the respective columns.
* The languages of the texts are either Latin (`lat`) or German (`de`), and the abstracts are predominantly in German (`de`).
* The years range from 816 to 1752, representing a broad historical time frame.
* The dataset includes a new column `translated_abstract_opus` with English translations of the abstracts.

## Applications

1.  **Topic Modeling:**
    *   Explore topic modeling techniques across three languages (Latin, German, and English).
    *   Compare topics extracted from original texts, original language abstracts, and translated abstracts.
    *   Analyze potential shifts in topics introduced by machine translation.

2.  **Named Entity Recognition (NER):**
    *   Evaluate and compare NER performance on original language texts and translated abstracts.
    *   Investigate how translation affects entity recognition and extraction.

3.  **Stylometry/Text Reuse:**
    *   Assess how machine translation impacts stylometric features and authorship attribution.
    *   Explore cross-lingual text reuse detection using both original and translated texts.

4.  **Large Language Models (LLMs):**
    *   Fine-tune LLMs on this multilingual dataset for tasks like text generation, translation, and summarization.
    *   Evaluate and improve machine translation models using the available translations.

5.  **Machine Translation Evaluation:**
    *   Use the dataset to assess the quality of the provided machine translations.
    *   Develop metrics to evaluate translation accuracy and fluency in a historical context.
