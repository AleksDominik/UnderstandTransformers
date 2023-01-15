# Understang Transformers

This worked is an personal annotated tutorial from official tensorflow site to help me (and some of you) understand the transformer inner mechanism. 
<br>https://www.tensorflow.org/text/tutorials/transformer

<br> the official Stanford course on NLP css224n helped me understand the theoritical part of the implementation. I also used the lecture slide
<br> the slides https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1214/slides/cs224n-2021-lecture09-transformers.pdf. 
<br> the video.  https://www.youtube.com/watch?v=ptuGllU5SQQ&list=PLoROMvodv4rOSH4v6133s9LFPRHjEmbmJ&index=14. 

This implementation and I guess lot of deep learning implementation use Einstein Notation. 
<br> This blog helped me https://rockt.github.io/2018/04/30/einsum#fn.10 
<br>This matrix operation mechanism is used in a specific layer  https://www.tensorflow.org/api_docs/python/tf/keras/layers/EinsumDense (the layer that implement the einsum). To quickly describe it, it use the Einstein Notation to define a internal kernel matrix aiming to transform the input matrix with the possibility to set the output shape. That give you projection( increase dimension) and contraction (decrease dimension) possibilities.

I volontary didn't cover the masking process because I think it pretty obvious and mainly because the biggest challenge remain in the computation mechanism. From projection to attention score computation through the equation creation logic. My little section aims to give you a deeper understanding of transformers.
