# Amazon Bedrock Model Invocation

This repository contains examples and scripts to invoke models using Amazon Bedrock. It includes configurations for different models like `meta.llama3-1-70b-instruct-v1:0` and `anthropic.claude-v2`.

## Prerequisites

- AWS Account with appropriate permissions
- AWS CLI configured with your credentials
- Python 3.x installed
- Boto3 library installed

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/bedrock-model-invocation.git
    cd Amazon_bedrock
    ```

2. Install the required Python packages:
    ```sh
    pip install boto3
    ```

## Usage

### Invoking the Llama 3.1 70B Instruct Model

The following script demonstrates how to invoke the `meta.llama3-1-70b-instruct-v1:0` model.

```python
import boto3
import json

prompt_data = """
Act as Shakespeare and write a poem on machine learning.
"""

bedrock = boto3.client(service_name="bedrock-runtime")
payload = {
    "prompt": "INST " + prompt_data + " [/INST]",
    "max_gen_len": 512,
    "temperature": 0.5,
    "top_p": 0.9
}
body = json.dumps(payload)
model_id = "meta.llama3-1-70b-instruct-v1:0"

try:
    response = bedrock.invoke_model(
        body=body,
        modelId=model_id,
        accept="application/json",
        contentType="application/json"
    )

    response_body = json.loads(response.get("body").read())
    response_text = response_body['generation']
    print(response_text)
except Exception as e:
    print(f"An error occurred: {e}")
