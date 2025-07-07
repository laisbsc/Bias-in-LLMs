# Bias-in-LLMs
Demo for AWS Live Streaming on Responsible AI

> This demo was built in collaboration with [@kyrillospan](https://github.com/kyrillospan).

---
![img.png](media/img.png)

## Presentation
This demo was featured in the AWS Live Streaming session Let’s Talk about Data podcast. 
Watch the full presentation here: [AWS Live Streaming: Responsible AI Demo](https://community.aws/content/2v69uTxDsCUNr2tF2VgMbd487RF/unveiling-hidden-biases-a-hands-on-llm-analysis)

## Overview
This repository contains a demo that showcases how different Large Language Models (LLMs) respond to the same prompts, with a focus on evaluating and mitigating bias on their outputs. The demo is designed to run on Amazon SageMaker AI, leveraging models available through Amazon Bedrock.

The demo consists of two main parts: **text-to-text** and **text-to-image**. In the **text-to-text** part, different models are prompted with the same sentence and asked to complete it. Further prompts ask the models to evaluate the bias on their own outputs and reiterate on the replies eliminating possible bias. The **text-to-image** part involves requesting different models to generate images based on the same prompt.

This demo demonstrates how different models respond to identical prompts and provides a qualitative evaluation of bias in their outputs, along with mitigation strategies. While not intended as a comprehensive analysis of LLM bias, it serves as a starting point for understanding how models can exhibit varying biases when given the same prompt and offers approaches to address these issues.

## Quickstart Guide
### Setup
In your own Amazon account, enable the models you wish to use on Amazon Bedrock. [See the models used](#models-used) in this demo in the table below. From the list, only Dall-E 3 is **NOT** accessible through Bedrock and requires an API key.

### Run the code
Create a notebook on SageMaker AI. We are using an `ml.t2.medium` instance. Once this is done, you are now ready to copy and paste the code in this repository and run the application.
The real fun is to play with the prompts and see how different models respond to the same input. Try it out!

## Models used
For the text-to-text part of this demo, we used the following models:
| Model name | Model ID | Last version | Release date |
| --- | --- | --- | --- |
| Amazon Nova Lite | amazon.nova-lite-v1:0 | 1.0 | Dec 3rd 2024 |
| Meta LLama 3.3 | meta.llama3-3-70b-instruct-v1:0 | v1 | Dec 18th 2024 |
| Deep Seek R1 | deepseek.r1-v1:0 | v1 | Mar 3rd 2025 |

For the text-to-image part of this demo, we used the following models:
| Model name | Model ID | Last version | Release date |
| --- | --- | --- | --- |
| Amazon Nova Canvas | amazon.nova-canvas-v1:0 | 1.0 | Dec 3rd 2024 |
| Titan Image Generator G1 v2 | amazon.titan-image-generator-v2:0 | v2 | Aug 6th 2024 |
| Dall-E 3 | 'dall-e-3' | - | Oct 2023 |


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
