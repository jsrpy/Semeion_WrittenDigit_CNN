# Semeion Hand Written Digit Classification
The semeion hand written digit is a dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/semeion+handwritten+digit).

It consists of 1593 handwritten digits from around 80 persons were scanned, stretched in a rectangular box 16x16 in a gray scale of 256 values.

Our task is to build a Convnet model to classify the digits.

## The source code and model
[semeion_cnn-A](semeion_cnn-A.ipynb) contains the source code.

It also outputs the [model](semeion_cnn.h5) and [model weighting](semeion_cnn_weight.h5) in h5 format.

You can load them using `model.load_weights` and reproduce the same result as mine.

## Results
We reached a 95.61% accurcay. It is believed that the bottleneck for CNN in this task is around 98%.

Surely there are rooms for improvements if we tune the architecture properly.

Particularly, the issue of random number when fitting the model causes us some troubles in getting better result.

If we do not set the random seed, we could occassionally get as high as ~97% accuracy, but then we are not able to reproduce
the result. 

If we set the random seed, we need to spend a huge amount of time trialing which one is the best one.

## References
1. Dua, D. and Karra Taniskidou, E. (2017). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.
2. M Buscema, MetaNet: The Theory of Independent Judges, in Substance Use & Misuse 33(2)1998, pp 439-461.
