# Deploy-A-Large-Language-Model-Locally

The Llama2 7B large language model (LLM) is deployed here. In order to use the model locally (on a PC or other resource-limited devices) a slim (compressed) version of the model is obtained. This slim version is created by quantization, a process that reduces the memory size needed for the LLM’s weights. For example, quantization is achieved by turning floating-point numbers into integers. Integers require less space to be stored and thus reduce the size of the model. However, quantization also reduces the model precision.

The chosen quantized model here is 7b.Q4_K_M.gguf available for download from: https://huggingface.co/TheBloke/Llama-2-7B-GGUF . It has a medium size of 4.08 GB, it demands maximal RAM of 6.58 GB, and it has a balanced quality (i.e., balanced trade-off between size and precision). It is recommended for use in the Hugging Face page of available quantized models. The GGUF (appears in the quantized model name) stands for GPT-Generated Unified Format. It is a new format introduced by the llama.cpp team on August 21st 2023. It is a replacement for GGML and offers some advantages over GGML e.g., a better tokenization. Q4_K_M is the type of quantization, with further details being out of the scoop of this work.

The model is run using Python and the Ctransformers library from Longchain. 

Example of generating a response to a prompt:

![img1](https://github.com/Morikky/Deploy-A-Large-Language-Model-Locally/blob/main/plots/test.png)


One can see the responce is cut articulated  reduced precision of the response due to the quantization. 


