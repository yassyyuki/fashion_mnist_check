# Fashion-MNSIT Check

## Summary

Sample codes to train some model with TensorFlow (Keras), to export the trained model, and to import the model to TensorFlow.js.

## Usage

You need TensorFlow and TensorFlow.js. If you do not have them yet, install them as follows.

```sh
python3 -m venv tf  
source tf/bin/activate
python3 -m pip install --upgrade pip
python3 -m pip install tensorflow tensorflowjs
```

### Train a model

Train a model and save the trained model.

```sh
$ python3 train.py
(snip)

Test accuracy: 0.8709999918937683

Predictions for zero input
[0.08157011 0.00318779 0.02768737 0.05093732 0.00741246 0.71254516
 0.07637644 0.02599602 0.01260033 0.00168701]

Model was saved.
```

You will have the following files.

* model.data-00000-of-00001
* model.index

### Export the trained model

Load the trained model and export it for TensorFlow.js.

```sh
$ python3 export.py
(snip)

Predictions for zero input
[0.08157011 0.00318779 0.02768737 0.05093732 0.00741246 0.71254516
 0.07637644 0.02599602 0.01260033 0.00168701]

Model was exported.
```

You can verify that the model was loaded correctly by checking that you get the same output for the zero input.

Then you will have the following directory which contains the exported model for TensorFlow.js.

```txt
model
├── group1-shard1of1.bin
└── model.json
```
