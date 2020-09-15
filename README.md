# Text-classifier-with-ensemble-method
Recognize hate speech on twitter via ensembling.

Data includes more than 18k tweets labeled as appropriate (OK) or not (NG). @USER and {{URL}} replace user names and urls in the tweets. The goal is to design a text classifier able to recognize hate speech as accurately as possible.
The dataset is very unbalanced, so it is firstly oversampled. Then, it is split in training and test set to evaluate the performance. In order to make data digestible for our classifier, it is applied a bag-of-words and the stopping words are deleted (as well as @USER and {{URL}}). Several different (to minimize the correlated error) classifiers are combined in an ensemble with soft voting. The ensemble is trained on the training set and evaluated on the test set with F1 macro score because of the unbalanced data. The performance for each individual classifier is also reported. The ensemble method gets a slight performance boost over the already high performance of classifiers alone.
