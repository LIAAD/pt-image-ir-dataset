# pt-image-ir-dataset

A Dataset for Image Information Retrieval in European Portuguese.

## Data

The data is sourced from the [Portuguese Presidency](https://www.presidencia.pt/) website. It contains 4,678 articles, 42,333 images and 80 queries related to the Portuguese Presidency. Over 5000 images were annotated by three annotators.

The dataset is structured into four distinct files, available in the `data` directory:

- `articles.tsv`: Contains the articles collected from the Portuguese Presidency website. Each article has a url, title, content, data and a list of images.
- `images.tsv`: Contains the images related to the above-referred articles. Each image has only a url.
- `queries.tsv`: Contains the queries created by the authors of the dataset.
- `qrels.txt`: Contains the relevance judgments for the queries. It follows the TREC format, where each line contains a query id, a zero, an image id and a relevance score (0 or 1). The relevance score is 1 if the image is relevant to the query, and 0 otherwise.

## Annotation Methodology

The dataset annotated was done manually by three annotators. The annotators were given a set of guidelines to follow in order to determine the relevance of an image to a query. The platform used to annotate the dataset was made by the authors of the dataset.

## Annotator Guidelines

The goal of this annotation task is to determine whether an image is relevant(1) or non-relevant(0) to a given query. Relevance is defined by the relationship between the query, the image, and the context provided by the article title.

### Definitions

- **Relevant (1)** - The image directly supports, illustrates or is related to the query. It should provide meaningful context or information that aligns with the query's intent.
- **Non-relevant (0)** - The image does not support or relate to the query in a meaningful way. It may be unrelated, misleading, or provide no additional context to the query.

### Guidelines

1. **Understanding the query**: Read the query carefully. Identify the key terms and concepts. Consider the intent behind the query. What information is the user seeking?
2. **Evaluating the image**: Assess the content of the image. Does it depict something that is related to the query? Look for visual elements (People, objects, actions, places...) that can be linked to the query.
3. **Context from the article title**: Read the article title provided since it may help clarify the context of the image. It helps in situations where the query might depict a specific event, person or object that is mentioned in the title.
4. **Common scenarios**:
    - **Direct match**: if the image clearly depicts the subject, place, action or object mentioned in the query, it is relevant.
    - **Indirect match**: if the image depicts something that could be related to the query but not in an obvious way, consider the context provided by the article title. If the image is related to the article title and could be relevant to the query, it is relevant.
    - **Unrelated content**: If the image shows something completely different from the query and does not provide any context or information related to the query, it is non-relevant.
    - **Ambiguous cases**: If in doubt even after using the article title as context, choose the image as non-relevant. The subject of the image should be clearly shown in the image, for instance, if the image is blurry or too small to identify the subject, it is non-relevant. For people, the face should be clearly visible and identifiable, when the subject is to the side or not clearly visible, it is non-relevant.
5. **Avoiding biases**: Try to be objective and avoid personal biases. Focus on the content of the image and its relationship to the query. Do not let personal opinions or feelings about the subject matter influence your decision.
6. **Unknown terminology**: If you encounter a term or concept in the query or article title that you do not know, you can search for it online to understand its meaning. This can help you better assess the relevance of the image.

### How does the annotation process work?

1. In the interface, you will see a query, the article title for the image, and the image itself.
2. Read the query and the article title carefully.
3. Evaluate the image based on the guidelines provided above.
4. Select the appropriate label (1 for relevant, 0 for non-relevant) based on your assessment. You can use the buttons on the interface or the keys on your keyboard "R" for relevant and "I" for non-relevant.
5. After selecting the label, the next image will show up automatically. (Keep in mind that the query and article title can change, so be sure to read them carefully each time.)

>Note: If you made a mistake you can undo by clicking the "Undo" button or using the keyboard shortcut "Z". The progress is saved automatically and you can leave at any time. There is also a progress bar to track how many images you have annotated for the current query.

## Citing

If you use pt-image-ir-dataset in your research, please cite the following work:

Duarte, R., Campos, R., Proença, H. & Branco, A. (2025). pt-image-ir-dataset: A Quality Dataset to Support Image IR in Portuguese. Zenodo.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15566573.svg)](https://doi.org/10.5281/zenodo.15566573)

## License

This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).
