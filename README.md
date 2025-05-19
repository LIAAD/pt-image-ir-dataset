# pt-image-ir-dataset

A Dataset for Image Information Retrieval in European Portuguese.

## Data

The data is sources from the [Portuguese Presidency](https://www.presidencia.pt/) website. It contains 4678 articles, 42333 images and 80 queries related to the Portuguese Presidency. Over 5000 images were annotated by three annotators.

The dataset is divided into four files present in the `data` folder:

- `articles.tsv`: Contains the articles related to the Portuguese Presidency. Each article has a url, title, content, data and a list of images.
- `images.tsv`: Contains the images related to the articles. Each image has only a url.
- `queries.tsv`: Contains the queries created by the authors of the dataset.
- `qrels.txt`: Contains the relevance judgments for the queries. It follows the TREC format, where each line contains a query id, a zero, an image id and a relevance score (0 or 1). The relevance score is 1 if the image is relevant to the query, and 0 otherwise.

## Annotation Methodology

The dataset annotated was done manually by three annotators. The annotators were given a set of rules to follow in order to determine the relevance of an image to a query. The rules are in `rules.md` file. The platform used to annotate the dataset was made by the authors of the dataset.

## License

This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).
