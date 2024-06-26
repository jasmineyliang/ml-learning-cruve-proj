# ml-learning-cruve-proj


### Anatomy of functions
1. The time points are generated by the function `generate_data` that returns both the time points and groundtruth distances corresponding to those time points. 
2. The function `test_NN` training a neural network using the data generated above, and use the same neural network to predict on the same time points used in training. 
3. The function `learning_curve` is what you are expected to implement. It shall make two plots. One is groundtruth used in training with respect to time points. The other is the predictions with respect to time points. Both the training data and the groundtruth should have the same length. 

### Speficiations for the function `learning_curve` 

Please folow the specifications carefully, such as using the right colors. Otherwise, the auotgrader will give you zero. 

1. The function takes three arguements, 
   * `N`, of type `int`, is the number of data points, 
   * `max_iter`, also of type `int`, is the number of iterations to train the neural network
   * `filename`, of type `str`, is where the visualization is saved. 
2. The function returns a hash digest of the `filename`. It is for you to self-check the correctness of your implementation. The TA will also use this value to grade your submission. 
   * If you execute on DeepNote, for `learning_curve(500, 300, "test.png")` , the return hash shall be `4b2737555fbaabffba658659a7cd53ed`. If you get the same number, then you are correct. 
   * For execution on Google Colab, upgrade the version of matplotlib using `!pip install matplotlib==3.6.0`, restart the runtime/kernel, and after `import matplotlib`, reset the rcParams using `matplotlib.rcParams.update(matplotlib.rcParamsDefault)`, you should be able to get the same hash `4b2737555fbaabffba658659a7cd53ed`.
3. `learning_curve` shall first call `generate_data` to generate `N` data points (two parts, times `Ts` and heights `Hs`), then pass the data points to `test_NN` function to obtain the predictions and the score, the latter of which is not needed. 
4. Finally, you visualize the ground truth and the prediction using `matplotlib.pyplot.plot` as shown in one cell in `1_intro.ipynb`. 
5. It shall plot two [lines](https://en.wikipedia.org/wiki/Line_chart) in two distinctive colors. For the groundtruth, use BLUE (color code `tab:blue`), and for the prediction, use ORANGE (color code `tab:orange`). Regarding how to change colors in line plots, see the demo in `1_intro.ipynb`. 
6. For every plot setting else, leave to default settings. 
7. Use 4-space indentations. No tabs.


Dr.forrestbao MLClass
