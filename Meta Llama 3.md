* 8B and 70B params (pretrained and instruction-fine-tuned → [[LLMs]])
* **Architecture** - Decoder-only Transformer
* 128K tokens (8192 tokens sequence)
* GQA to improve inference efficiency
* Pretraining done with 15T tokens
* Compute Utilization of >400 TFLOPS/GPU (on 16k GPUs simultaneously)
#### Post-training
* Instruction fine-tuning
* SFT, PPO, DPO

#### Development
* torchtune (PyTorch library for LLM tuning)

https://ai.meta.com/blog/meta-llama-3/