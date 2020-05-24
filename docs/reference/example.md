---
templateKey: "model-page"
title: example()
exampleimgsrc: ../assets/ref-yolo.png
tags:
  - reference

description: >-
  RNN and [LSTMs](https://colah.github.io/posts/2015-08-Understanding-LSTMs/) (Long Short Term Memory networks) are a type of Neural Network architecture useful for working with sequential data (like characters in text or the musical notes of a song) where the order of the that sequence matters. This class allows you run a model pre-trained on a body of text to generate new text.

  <br/>
  <br/>

  You can train your own models [using this tutorial](/docs/training-lstm) or use [this set of pre trained models](https://github.com/ml5js/ml5-data-and-training/tree/master/models/lstm).

examples:
  - title: the title of the demo
    github: https://github.com/ml5js/ml5-library/blob/development/examples/p5js/ImageClassification/ImageClassification_Video/sketch.js
    demo: https://yining1023.github.io/fast_style_transfer_in_ML5/
    code: >-
      const video = document.getElementById("video");

      // Create a YOLO method
      const yolo = ml5.YOLO(video, modelLoaded);

      // When the model is loaded
      function modelLoaded() {
        console.log("Model Loaded!");
      }

      // Detect objects in the video element
      yolo.detect(function(err, results) {
        console.log(results); // Will output bounding boxes of detected objects
      });

  - title: the title of the demo
    github: https://github.com/ml5js/ml5-library/blob/development/examples/p5js/ImageClassification/ImageClassification_Video/sketch.js
    demo: https://yining1023.github.io/fast_style_transfer_in_ML5/
    code: >-
      const video = document.getElementById("video");

      // Create a YOLO method
      const yolo = ml5.YOLO(video, modelLoaded);

      // When the model is loaded
      function modelLoaded() {
        console.log("Model Loaded!");
      }

      // Detect objects in the video element
      yolo.detect(function(err, results) {
        console.log(results); // Will output bounding boxes of detected objects
      });

tutorials:
  - tutorial: '<div class="iframe__container iframe__container--video"><iframe src="https://www.youtube.com/embed/vYgIKn7iDH8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>'
  - tutorial: '<div class="iframe__container iframe__container--video"><iframe src="https://www.youtube.com/embed/vYgIKn7iDH8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>'

training: >
  ## heading 2


  [this is a link](https://www.wenqi.li)


  This is some text
---

## Syntax ( A subject should use H2 )

> ( A blue block use blockquote )
>
> ### ml5.charRNN(**model**, **?callback**) ( A syntax highlight use H5, which is green )
>
> Generates content a stateless manner, based on some initial text (known as a "seed"). Returns a string.
>
> - `model`, **model** (props use strong or inline block inside a list item, which is purple): The pre-trained charRNN model.
> - **callback** — Optional. A callback to be called once the model has loaded. If no callback is provided, it will return a promise that will be resolved once the model has loaded.

Tags in the front matter can be formatted as such:

```
tags:
 - image
 - text
 - helpers
 - sound
```

## Properties

### .ready

Boolean value that specifies if the model has loaded.

### .state

The current state of the model.

### .model

The pre-trained charRNN model.

### .vocabSize

The vocabulary size (or total number of possible characters).

## Methods

> ### .generate(**options**, **?callback**)
>
> Generates content in a stateless manner, based on some initial text (known as a "seed"). Returns a string.
>
> - **options** - An object specifying the input parameters of seed, length and temperature. Default length is 20, temperature is 0.5 and seed is a random character from the model. The object should look like this:
>
> ```javascript
> {
>    seed: 'The meaning of pizza is'
>    length: 20,
>    temperature: 0.5
> }
> ```
>
> - **callback** - Optional. A function to be called when the model has generated content. If no callback is provided, it will return a promise that will be resolved once the model has generated new content.

> ### .feed(**seed**, **?callback**)
>
> Feed a string of characters to the model state.
>
> - **seed** - A string to feed the charRNN model state.
> - **callback** - Optional. A function to be called when the model finished adding the seed. If no callback is provided, it will return a promise that will be resolved once seed has been fed.

> ### .predict(**temperature**, **?callback**)
>
> Feed a string of characters to the model state.
>
> - **predict** - Predict the next character based on the model's current state.
> - **callback** - Optional. A function to be called when the model finished adding the seed. If no callback is provided, it will return a promise that will be resolved once the prediction has been generated.

> ### .reset()
>
> Reset the model state

## Source

[/src/charRNN/](https://github.com/ml5js/ml5-library/tree/master/src/charRNN)
