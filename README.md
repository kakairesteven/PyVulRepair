# PyVulRepair
PyVulRepair is a Large Language Model for Automatic Repair of Single Statement Security Vulnerabilities in Python Source Code.

Python Language is one of the top programming languages and has applications in many fields. This project is to build an APR tool to
repair single statement security vulnerabilities in Python Source Code.

## Experimental Setup
I leverage two deep learning Python libraries i.e <a href='https://github.com/huggingface/transformers'>Transformer</a> and <a href='https://ronan.collobert.com/pub/matos/2011_torch7_nipsw.pdf'>PyTorch</a> to build the PyVulRepair.

## Datasets
In my experiment, I use two datasets i.e <a href='https://github.com/JafarAkhondali/Morefixes'>MoreFixes</a> and <a href='https://github.com/cedricrupb/TSSB3M/blob/main/README.md'>STTB-3M</a> that contain
10,000 Python Single Statement security vulnerability bugs and 3 million Python Single
Statement bugs respectively.

## To Replicate this work
#### Environment Setup
Install requirements using;
`pip install -r requirements.txt`

