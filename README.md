# Bias-in-LLMs
Demo for AWS Live Streaming on Responsible AI
> This demo was built by [@kyrillospan](https://github.com/kyrillospan).

This code uses Amazon SageMakerAI to run prompts to different Large Language Models (LLMs) linked to it via Amazon Bedrock.
The purpose of this demo is to show how different models reply to the same prompt and do a qualitative evaluation of how bias the outputs are.
Further prompts ask the models to evaluate the bias on their outputs and reiterate on the replies eliminating possible bias found.

## How to use this code?
In your Amazon account, enable the models you wish to use on Amazon Bedrock. We used the models listed below. From the list, only Dall-E 3 is **not** accessible through Bedrock and requires an API key.

Then, create a notebook on SageMaker AI , we are using an `ml.t2.medium` instance. You are now ready to copy and paste the code given in this repository to run the application.

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
