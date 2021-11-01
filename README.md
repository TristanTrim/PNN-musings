# PNN-musings

With advances in gpu, it has become possible to train neural nets with increasingly impressive applications, but are gpu the best hardware to be training NN's on, or is it possible to build hardware better tailored to training neural nets?

There are two broad approaches I imagine:
 - Continuing to represent the NN digitally, but changing the way the calculations are done
 - Representing the NN as an analog circuit, this is Physical Neural Net (PNN)

## Initial model

My initial interest involves a circuit with an array of digital potentiometers, each representing the weight between a neuron in one layer, and the neurons in the next layer. In this way, the net's weights would be controlled digitally, but would be evaluated at the speed it takes charge to propagate through the potentiometers, which afaik should be much faster than corrisponding digital calculations.

I'm also interested in designing a way to do back propagation training in novel ways in the circuitry, which would require the controlling computer be able to read, as well as write to the neuron weights, otherwise the back propagation would need to pass through the digital computer, which is potentially a bottleneck. Of course at this point this is very fuzzy conceptualization.

## Questions & concerns

### How parallel can you train a NN?

It could be that the amount of parallelization that can be done in training NNs makes gpu a superior method and makes this kind of PNN research unimportant. I need to do more research to be sure.

### Series digital calculations?

It may be better to build a circuit that has many digital calculations in series, where the output of one digital calculation is pushed directly into a calculation in the next layer, rather than into a buffer. Maybe this is how gpu's are doing things now? I should read some more.

### How much interference is there in an analog circuit of this kind?

The digital potentiometers would be varying by quite small amounts of resistance. Potentially the voltage differences would be too small, and interference too great to effectively use the PNN. Maybe this could be solved by using a different transistor technology and/or higher voltage.

## Prior research

I'll describe other PNNs here, as I read about them.
