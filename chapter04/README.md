# Practical MLOps - Chapter 4

Overview

## Description

## Demo

## Features

- feature:1
- feature:2

## Requirement

## Usage

### 1. Download ONYX model

- [RoBERTa](https://github.com/onnx/models/tree/main/text/machine_comprehension/roberta)

RoBERTa Use cases:
Transformer-based language model for text generation.

```shell
curl -sL https://github.com/onnx/models/raw/main/text/machine_comprehension/roberta/model/roberta-sequence-classification-9.tar.gz| tar xvf -
mv roberta-sequence-classification-9/roberta-sequence-classification-9.onnx .
rm -fr roberta-sequence-classification-9
```

### 2. Configure Python Environment

Python version: `3.8.18`

```shell
pyenv local 3.8.18
```

Create vietual environment

```shell
python -m venv .venv
```

Intall dependencies

```shell
pip install -r requirements.txt
```

### 3. Create Docker image

```shell
docker build -t shinyay/roberta-sequence-classification-9 .
```

Run the docker image

```shell
docker run --rm -it -p 5001:5001 shinyay/roberta-sequence-classification-9
```

### 4. Test the app

```shell
 curl -X POST  -H "Content-Type: application/json" \
      --data '["MLOps is critical for robustness"]' \
      http://0.0.0.0:5001/predict
```

## Installation

## References

- [Chapter 4. Continuous Delivery for Machine Learning Models](https://learning.oreilly.com/library/view/practical-mlops/9781098103002/ch04.html)

## Licence

Released under the [MIT license](https://gist.githubusercontent.com/shinyay/56e54ee4c0e22db8211e05e70a63247e/raw/34c6fdd50d54aa8e23560c296424aeb61599aa71/LICENSE)

## Author

- github: <https://github.com/shinyay>
- twitter: <https://twitter.com/yanashin18618>
- mastodon: <https://mastodon.social/@yanashin>
