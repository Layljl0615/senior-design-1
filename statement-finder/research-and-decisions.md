# Research and Decisions


## Relevant Research

#### Language Notes and Definitions
- Statement: A sentence that can reasonably be classified as either true or false.
- Opinion: A statement of personal belief or value.
    - Note: Opinions can be framed as statements or exclamations.
- Types of non-statements include: questions, commands, and greetings (such as "Good morning!")

#### Natural Language Processing Notes
- Cleaning Text: Turn text into a filtered list of words in preparation for vectorization.
    - Removing Punctuation: Not required, but can remove some duplicate entries from the vector and lower the overall size of the vector.
    - Tokenization: The process of splitting a character sequence into smaller pieces. In this context, it is the process of breaking a sentence into a list of words.
    - Removing Stop Words: Stop words are commonly used words (such as "a", "and", "but" and many others) with less importance to the overall meaning of a sentence. Removing them filters a sentence down to only the most important words.
    - Stemming: Method of trimming words to their base form. 
    - Lemmatization: Method of trimming words to their base form.
        - Note: While stemming and lemmatizing perform the same basic function, the lemmatizer does a better job at preserving the context of the root word. For example, a stemmer will transform both "meaning" and "meanness" to "mean" whereas a lemmatizer will transform them to "meaning" and "mean", respectively.

- Vectorizing Text: Turn list of cleaned text into a vector where each row represents a specific message and each column represents a specific word (or n-gram).
    - Count Vectorization: Each cell within the vector represents the count of the associated word withing the associated message.
    - N-gram Vectorization: Columns represent n-grams (all groups of n consecutive words from the text) rather than words.
    - Inverse Document Frequency Weighting: Similar to Count Vectorization, except rather than each cell showing the count of the word in the message, it shows the proportion of that word to the overall message.

- Machine Learning Models:
    - Random Forest: Learning model that forms many decision trees as a forest. Prevents model from overfitting to the training set.
    - Gradient Boosting: Learning model that forms decision trees that build off each other. 

- Evaluating Models:
    - Grid Search: Method of finding the best parameters to use for a learning model. GridSearchCV from Python's sklearn.model_selection module is the one used in the development of the tool.


## Decisions
- For the purposes of this tool, opinions will be classified as non-statements.
    - Opinions cannot be judged as objectively true or false, so they shall be filtered out during the statement-finding process to simplify the fact-checking process later.
- For the initial prototype of the statement-finder tool, a Random Forest Classifier is used for the machine learning model.
    - In initial tests, the Random Forest model appeared to perform better than the Gradient Boosting model.
- In the text cleaning process, the program uses a lemmatizer rather than a stemmer.
    - The lemmatizer finds the root words more accurately, which was deemed necessary for the tool.
