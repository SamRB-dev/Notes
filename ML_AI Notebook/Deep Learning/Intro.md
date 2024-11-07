Opencv, Machine learning, deep learning (prefer pytorch), object detection ( yolov3, yolov4, yoloR, yolov7), object segmentation (prefer detectron2 and mxnet) objrct tracking (prefer fastmot and deepsort), Pose estimation, OCR, Face detection and recognition, Dockerization, Triton inference server (basically tensorrt optimization). Do this in order. I did in this order, as a result, I am a 22M student and working for the AI company full time (started working as intern for 2 months, then part time for a year, now full time for nearly six months) and I still have one year to graduate.

[Start Here](https://machinelearningmastery.com/what-is-deep-learning/)
**Deep learning** is an approach to machine learning characterized by deep stacks of computations. This depth of computation is what has enabled deep learning models to disentangle the kinds of complex and hierarchical patterns found in the most challenging real-world datasets.

# The Linear Unit[¶](https://www.kaggle.com/code/ryanholbrook/a-single-neuron#The-Linear-Unit)

So let's begin with the fundamental component of a neural network: the individual neuron. As a diagram, a **neuron** (or **unit**) with one input looks like:
![[mfOlDR6.png]]
The input is `x`. Its connection to the neuron has a **weight** which is `w`. Whenever a value flows through a connection, you multiply the value by the connection's weight. For the input `x`, what reaches the neuron is `w * x`. A neural network "learns" by modifying its weights.

The `b` is a special kind of weight we call the **bias**. The bias doesn't have any input data associated with it; instead, we put a `1` in the diagram so that the value that reaches the neuron is just `b` (since `1 * b = b`). The bias enables the neuron to modify the output independently of its inputs.

The `y` is the value the neuron ultimately outputs. To get the output, the neuron sums up all the values it receives through its connections. This neuron's activation is `y = w * x + b`, or as a formula y=wx+b

.