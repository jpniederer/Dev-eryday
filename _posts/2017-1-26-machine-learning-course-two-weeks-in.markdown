---
layout: post
title:  "Machine Learning Course Two Weeks In"
date: 2017-1-26 21:00:00 +0000
categories: Machine Learning
---
I've officially made it through the first two weeks of the [Machine Learning][ML] on Coursera. It's been a lot of fun so far and gets more interesting as I get deeper into it. In fact, as I write this, I'm watching some videos on regularization as part of the week three curriculum. Here are some brief notes covering the material from the first two weeks of the course.

Week One
--------
**What is Machine Learning:** The modern, formal definition, of Machine Learning is "A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E." This definition comes from [Tom Mitchell][tm], who is the chair of the Machine Learning department at Carnegie Mellon University.

There are two main types of Machine Learning, *supervised learning*, when we have data and know the results already, and *unsupervised learning*, when we don't know much at all and build up a structure from there. Furthermore, supervised learning and unsupervised learning are broken down even further into the types of problems they solve. Supervised learning solves regression and classification problems. Unsupervised learning is used to solve clustering and non-clusting problems.

**Model and Cost Function:** Machine learning problems are solved by building a model. For supervised learning, the process begins with a set of data known as the training set. The training set is provided to the learning algorithm which will return a predicted value based on our hypothesis. Regression problems take continuous values and classification problems take discrete values.

The accuracy of our hypothesis can be measured through the use of a [cost function][cf].

**Parameter Learning:** [Gradient Descent][gd] is an iterative algorithm that can be used to minimize the cost function. By selecting an appropriate learning rate and a reasonable number of iterations, the gradient descent should find the cost function's global minima. If a poor learning rate or insufficient number of iterations are ran, gradient descent can get stuck in a local minima and produce incorrect results.

**Linear Algebra Review:** This section of the course brought me back to high school. It was an optional review of matrices and vectors. It covered addition and multiplication of matrices. The review only covered very basic linear algebra, I recommend skipping it unless it's been a few years since seeing the material or it's your first time dealing with matrices.

Week Two
--------
**Linear Regression with Multiple Variables:** The [Normal Equation][ne] can be used as an alternative to gradient descent. The normal equation is calculation based and not an iterative process. Note that the normal equation is O(n^3) and will be slow when we have a large number of features. Gradient descent is only O(kn^2) so it is more efficient than using the normal equation. 

**Matlab/Octave Overview:** All programming assignments in the ML course are completed using Matlab or it's open source replacement, Octave. The course covered how to set up both languages in multiple environments. Both languages are very similar and offer a robust toolset for implementing machine learning algorithms. Through using Matlab/Octave, learners have a low barrier to entry as far as learning a new language. This allows learners to focus more on learning the machine learning techniques, rather than worrying about learning a more difficult programming language.

The course has a fantastic series of videos on getting started using both languages and even has some interactive [examples][oct]. 

[ML]: https://www.coursera.org/learn/machine-learning/
[tm]: https://en.wikipedia.org/wiki/Tom_M._Mitchell
[cf]: https://www.coursera.org/learn/machine-learning/supplement/nhzyF/cost-function
[gd]: https://www.coursera.org/learn/machine-learning/supplement/2GnUg/gradient-descent
[oct]: https://www.coursera.org/learn/machine-learning/supplement/INFAY/practice-octave
[ne]: https://www.coursera.org/learn/machine-learning/supplement/bjjZW/normal-equation