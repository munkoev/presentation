## **Machine Learning JS**

### **AI and ML in today's life**

Artificial intelligence and machine learning is now considered to be one of the biggest innovations.
Just a couple of decades ML used to be a concept from science fiction, but now it’s becoming a daily reality.

One day, computers will not only replace manual labor, but also mental labor.
This process is already happening, here are some examples:

- AlphaGo wins best Go players.
Back then it was impossible for computers to overcome human's experience and intuition because of huge number of turns available.
But AlplhaGo was specifically trained to play Go, not by simply analyzing the moves of the very best players,
but by learning how to play the game better from practicing against itself millions of times.

- Digital maps already performs function of road police.
In Russia Yandex navigator can recommend the fastest route for you based on traffic jams, construction work or accidents between you and your destination
It determines how slow traffic is in real time and can combine that data with incidents reported by users to build a picture of the traffic at any given moment

- Moreover, ML will eventually replace human drivers.
No need for road police anymore. ML allows self-driving cars to instantaneously adapt to changing road conditions,
while at the same time learning from new road situations.
ns with computers, thereby enhancing many of our natural abilities.

- ML now is a must in the entertainment industry,
Netflix, Spotify, ...any entertaining platform or website.
They use ML not only for recommendation but also to eliminate buffering and low-quality playback.

- ML can already write texts and produce media.
GPT-3 producing texts, numerous image filters can replicate famous artists, courthouses already should issue procedures to handle deep-fake videos, and so on.

There are plenty of other examples in every aspect of our life.

### **ML, Python and JS**

Yes, Python is not the only option for programming machine learning applications. Browsers can also perform machine learning
using WebGL for matrix-alike operations.
JavaScript can't yet beat Python's rich libraries, but there can be some reasons to use JavaScript in machine learning.

- Client-side machine learning
  - Python machine learning relies on client-server architectures as Python not supported by default on many user devices.
So, you have to send your private data to servers which is sometimes not preferable, for instance due to privacy issues. 

  - JavaScript, on the other hand, is natively supported by all modern mobile and desktop browsers.
This means JavaScript machine learning applications are guaranteed to run on most desktop and mobile devices.

  - Moreover, users might want to be able to run their machine learning models even when they don’t have an internet connection
or have a poor one, when it's faster to use JS ML rather than send data to Python server.

  - Client-side machine learning also saves server's capacity.

- Combining server-side and client-side learning
  - One of the main challenges of machine learning is training the models.
This is especially true for deep learning, where learning requires expensive backpropagation computations over several epochs.
While you can train deep learning models on user devices, it could take weeks or months if the neural network is large.
  
  - Fortunately, machine learning libraries written in different languages are highly compatible.
For instance, if you train your deep learning model with TensorFlow or Keras for Python,
you can save it in one of several language-independent formats such as JSON or HDF5.
You can then send the saved model to the user’s device and load it with JavaScript deep learning library,
which can also be easily integrated with mobile applications.

- Better accessibility to sensors
Browser has direct access to web-cameras, GPS, accelerometer etc
  
### **tensorflow.js**

There are already several JavaScript machine learning libraries, such as ML5.js, Synaptic, and Brain.js.
Another example is TensorFlow.js, the JavaScript version of Google’s famous TensorFlow machine learning and deep learning library.
This is an open-source library which everyone can use to define, train, and run machine learning models entirely in the browser,
using Javascript and a high-level layers API.

TensorFlow.js automatically supports WebGL, and will accelerate your code behind the scenes when a GPU is available.
Users may also open your webpage from a mobile device, in which case your model can take advantage of sensor data,
say from a gyroscope or accelerometer. Finally, all data stays on the client,
making TensorFlow.js useful for low-latency inference, as well as for privacy preserving applications.

- tensorflow.js examples

  - LipSync by Youtube is a web application that checks how good user sings along. The systems recognizes motion of lips and face during singing
    and matches it with target. The model was trained with TensorFlow.js.

  - emojiscavengerhunt by Google. emoji scavenger hunt — a new AI experiment created by Google that shows how the company’s machine learning tools can be used to make fun little games.
    In this case, you have to use your phone’s camera to find objects that match emoji within a time limit. Each one you find increases your time.

  - Performance RNN, a neural network designed to model polyphonic music with expressive timing and dynamics.
    this isn’t a performance of an existing piece; the model is also choosing the notes to play, “composing” a performance directly.
    The performances generated by the model lack the overall coherence that one might expect from a piano composition;
    in musical jargon, it might sound like the model is “noodling”— playing without a long-term structure.
    However, to our ears, the local characteristics of the performance (i.e. the phrasing within a one or two second time window) are quite expressive.

Let's take a look on how we can setup a simple example from Google codelabs.

The steps in training a machine learning model include:

Formulate your task:

Is it a regression problem or a classification one?
Can this be done with supervised learning or unsupervised learning?
What is the shape of the input data? What should the output data look like?
Prepare your data:

Clean your data and manually inspect it for patterns when possible
Shuffle your data before using it for training
Normalize your data into a reasonable range for the neural network. Usually 0-1 or -1-1 are good ranges for numerical data.
Convert your data into tensors
Build and run your model:

Define your model using tf.sequential or tf.model then add layers to it using tf.layers.*
Choose an optimizer ( adam is usually a good one), and parameters like batch size and number of epochs.
Choose an appropriate loss function for your problem, and an accuracy metric to help your evaluate progress. meanSquaredError is a common loss function for regression problems.
Monitor training to see whether the loss is going down
Evaluate your model

Choose an evaluation metric for your model that you can monitor while training. Once it's trained, try making some test predictions to get a sense of prediction quality.
