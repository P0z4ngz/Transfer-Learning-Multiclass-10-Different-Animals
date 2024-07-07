# Personal project exercise of Deep Learning CNN course

## Description
By following the practical of a course Deep Learning TensorFlow, I decided to write my own notebook in [Google Colab](https://colab.research.google.com/) introducing computer vision multiclass 10 different animals from custom sorted dataset. Original dataset from [Kaggle Animals-10](https://www.kaggle.com/datasets/alessiocorrado99/animals10).

## Content
The dataset consists of `1000` images from each class in **train**, `100` images from each class in **valid** & **test** set (spider, horse, butterfly, elephant, chicken, cow, squirrel, sheep, cat, and dog). I created 2 models with [**Functional API**](https://www.tensorflow.org/guide/keras/functional_api) for architecture flexibility combaine with base model from [`tf.keras.applications.EfficientNetB2`](https://www.tensorflow.org/api_docs/python/tf/keras/applications/EfficientNetB2). One with none trainable layers in `base model` and improvment model where I use **fine tuning** method in the `base model` to boost the performance if it's gain significant improvement in training set.

The notebook itself covers some methods:
1. Import dataset, [Get Here.](https://drive.google.com/file/d/1osRe49hLWFUkaKDWr25RlgAcPXaSLFDU/view?usp=sharing)
2. View some dataset(images)
3. Preprocessing images
   * Turn into tensors
   * Resize the shape (128x128)
   * Seperate into 32 bathes
   * Implementing data augmentation
   * Normalize tensors (if need it, depends on base model)
4. Build callbacks model
   * Checkpoint
   * Early Stopping
5. Build and run a model with **functional API**
   * Model architecture
   * Compile a model
   * Fit data into the model
6. Evaluate model performance
   * History learned model
   * Making prediction with test dataset
   * Check metrics performance (`confusion matrix` and `classification report`)
   * Save a model for future use
7. Re-create model architecture with **Fine Tuning** base model layers method and repeat compile and fit a model
8. Repeate the step **6** until satisfied
9. View prediction of a model to the test dataset randomly
10. Make a prediction with other pictures from public
11. Visualize dataset scores performance into dataframe and plot the [F1-score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html)

## Log
* 08 July 2024: Minor update in notebook.
* 07 July 2024: First attempt, completed notebook.
