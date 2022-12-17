# seq-inverter

A simple transformer based encoder-decoder architecture is trained to flip the input of binary values e.g. [0, 1, 1, 0, 0, 1] -> [1, 0, 0, 1, 1, 0] using torch.

## Why?
- The transformer encoder is easy to understand. Understanding the decoder requires more work due to masking/how training is done in parallel. I wanted to understand how the stuff works by bilding a simple toy problem myself

- Although it's not very useful to replace torch.fliplr/numpy.fliplr with this torch model :blush: in principle it could be done (at least for shorter sequences). The implications are very interesting: https://karpathy.medium.com/software-2-0-a64152b37c35

Interesting things to study:
- What is the longest possible sequence the transformer can learn to flip? 
- Include other values besides, 0 and 1.  
- How many training exampels are needed for the model to learn the task?
- Teach the transformer to do other tasks, such as summing two numbers

## Instructions

Create a virtual environment

```
python -m venv env
source env/bin/activate
```

Upgrade pip and install requirements:

```
pip install --upgrade pip setuptools wheel
pip install -r requirements.txt
```

Open the notebook and run the cells
