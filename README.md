## Project: Incident Analysis Question-Answering System

## Description
This project implements a question-answering system for incident analysis using the HuggingFace Bert and Falcon models. The system is designed to answer questions about incidents based on the provided context. It uses both generative and extractive models to generate answers, and evaluates their performance based on F1 and Exact Match scores.

## Files
- `incident_analysis.ipynb`: This Jupyter notebook contains the main code for the project. It includes the implementation of the question-answering system, the evaluation of the models, and the analysis of the results.

## Implementation
The project is implemented in Python and makes use of several libraries including HuggingFace Transformers, Torch, Pandas, and Numpy. The code is organized into several sections:

1. **Library Imports**: Necessary libraries and modules are imported.

2. **Utility Functions**: A set of utility functions are defined for tasks such as normalizing answers, calculating F1 and Exact Match scores, loading datasets, and evaluating the models.

3. **Generative Model Experiment**: The generative model (Falcon) is loaded and used to generate answers to the questions. The answers are then evaluated and the results are analyzed.

4. **Extractive Model Experiment**: The extractive model (Bert) is loaded and used to extract answers from the context. The answers are then evaluated and the results are analyzed.

5. **Analysis and Conclusion**: The performances of the two models are compared and conclusions are drawn based on the results.

## Usage
To run the project, open the `incident_analysis.ipynb` notebook in a Jupyter environment. Ensure that all the necessary libraries are installed. Run the cells in order to execute the code.
You can have a look at the dataset used in the project [here](https://drive.google.com/drive/folders/12CBUYGICyc40DVGil6QmcKp8YAUNr_t9?usp=sharing).

## Results

1. **Tiiuae/falcon-7b-instruct (Modèle Génératif):**

* F1 Score : 35.96%
* EM Score : 170 sur 1130

2. **Bert-large-uncased-whole-word-masking-finetuned-squad (Modèle Extractif):**

* F1 Score : 58.64%
* EM Score : 533 sur 1130

From the preceding analysis, we can conclude that:

* The extractive model "bert-large-uncased-whole-word-masking-finetuned-squad" outperforms the generative model "tiiuae/falcon-7b-instruct" in terms of precision and relevance of answers within the question-answering task.

* The extractive nature of "bert-large-uncased-whole-word-masking-finetuned-squad" makes it more suitable for tasks where the exact answer must be found within a given context, as is often the case in question-answering systems.

* Despite its ability to generate new and unique answers, the generative model may lack precision and accuracy compared to an extractive model in this specific context.

In summary, for a question-answering application where accuracy and relevance of information are crucial, an extractive model like "bert-large-uncased-whole-word-masking-finetuned-squad" would likely be more appropriate than the generative model "tiiuae/falcon-7b-instruct".

## Future Work
- Integrate more advanced models and techniques for question-answering like RAG
- Explore other evaluation metrics as BUS for question-answering
- Use advanced tools to generate more accurate prompts for the models