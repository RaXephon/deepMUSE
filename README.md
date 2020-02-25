
<!-- ![deepMUSE](https://cloud.githubusercontent.com/assets/9053987/16575656/901989da-424f-11e6-9f54-6a04199e69f5.png) -->
# deepMUSE

### Using Keras & Theano for deep learning driven music generation

I built **deepMUSE** over the weekend after checking out a [similar project](https://github.com/jisungk/deepjazz). It uses Keras & Theano, two deep learning libraries, to generate music. Specifically, it builds a two-layer [LSTM](http://deeplearning.net/tutorial/lstm.html), learning from the given MIDI file.

### Dependencies

* [Keras](http://keras.io/#installation)
* [Theano](http://deeplearning.net/software/theano/install.html#bleeding-edge-install-instructions)
* [music21](http://web.mit.edu/music21/doc/installing/index.html)

### Instructions

Run on CPU with command:  
```
python generator.py [num_epochs]
```

Run on GPU with command [Supported Only for NVIDIA cards (CUDA backend)]:  
```
THEANO_FLAGS=mode=FAST_RUN, device=gpu, floatX=float32 python generator.py [num_epochs]
```

Note: `preprocess.py` must be modified to work with other MIDI files (the relevant "melody" MIDI part needs to be selected). The ability to handle this natively is a planned feature.

### Author

[Shashwat Kapoor](raxephon.github.io)  
University of Maryland, College Park  
shashkap (at) umd.edu

### Citations

This project is mostly based on Ji-Sung Kim's [deepjazz](https://github.com/jisungk/deepjazz). Public examples from the [Keras documentation](https://github.com/fchollet/keras) were also referenced.

### Code License, Media Copyright

Code is licensed under the Apache License 2.0
