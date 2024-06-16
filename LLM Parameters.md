Parameters are like **adjustable components** or dials for the model. The number of parameters and their quality can significantly affect an [[LLMs|LLM's]] performance

**Types of Parameters**
* [[Embedding Model|Embedding Parameters]] - Map tokens into *high-dimensional vectors*, encoding their *semantic and contextual meaning
* **Transformer Layers Parameters** - Parameters such as _weights_ and _biases_ present in an LLM's *transformer layers*. They "transform" the input data and *capture intricate patterns* and meanings in them
* _Attention Mechanism Parameters_ - These parameters dictate the importance of parts of different tokens by assigning different weights. Transformers with attention mechanisms work by selectively zooming in on the most relevant parts of an input sentence while setting aside the ones that are not
* _Feed-forward Network Parameters_ - These parameters in transformer layers enable non-linear transformation of data -> helping form complex relationships between tokens
* _Normalization Parameters_ - These parameters help with normalization and stability of the model's training process. They also improve the generalization performance of the model
* _Output Layer Parameters_ - Final layer parameters responsible for producing predictions 

<font style="color:lightgreen">Pros</font>
* Increased complexity and power
* Increased performance and generalization of context

<font style="color:red">Cons</font>
* Increased memory usage
* Increased storage space
* Increased consumption of system resources and power

Parameter counts of various LLMs out there

| Model Name                | Number of Parameters |
| ------------------------- | -------------------- |
| GPT 3.5                   | 20B (?)              |
| GPT 4                     | 1.76T                |
| [[Meta Llama 3\|LLaMa 3]] | 8B / 70B             |
| Claude 3 Opus             | 137B                 |
| Claude 3 Sonnet           |                      |
| Gemini Pro                |                      |


### References
1. https://medium.com/@greg.broadhead/a-brief-guide-to-llm-numbers-parameter-count-vs-training-size-894a81c9258
2. https://ai.meta.com/blog/meta-llama-3/