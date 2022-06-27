# ResearchProjectRelationExtraction

The seed dataset in contained inside the "rawdata" folder. Labelled datasets for both NER and relation extraction tasks are inside the labelledData folder.

The "unsupervised_methods" displays the unsupervised methods developed at the beginning of the project to extract labelled data from raw texts. The "unsupervised_relationExploration" notebook make use of these methods and also displays the number of manually labeled relations.

The NER folder contains all files related to Named-entity-recognition tasks. Two pre-processing notebooks were implemented. The one called "merged" differs from the other in that it combined product and market entities (often embiguous). Fine-tuning of Bert for token classification is implemented under the NERmodels notebook and was run on Google Collab. It also contains hyperparameter fine-tuning but unfortunately does not display optimum parameters.

Unfortunately, I could not implement the code from "Matching-the-Blanks" paper. I did fine-tune bert on my dataset and extract the embeddings from the last hidden layer for the entity special tokens. "rel_preprocessing" contains the code for pre-processing the data. More over, fine_tune_maskedModel.ipynb notebook implements the fine tuning on Google Collab.

"relation_classification" notebook implements a k-nearest-neighbor classifier and draws the baseline for new relation retrieval.

Finally, predict_relations_pipeline.ipynb implements the whole pipeline (NER+classification) to predict new relations.
