# TOPOTIDE-Topoisomerase-Targeted-Inhibitor-Design-Engine-for-Anticancer-Drug-Discovery-
Human topoisomerase IIα (hTopoIIα) is a key regulator of DNA topology and an established anticancer target. Its overexpression in multiple cancers necessitates the discovery of novel and safer inhibitors.
The framework integrates generative artificial intelligence (GAI), recurrent neural networks (RNNs), long short-term memory (LSTM), transfer learning, reinforcement learning, molecular-property analysis, molecular-generation evaluation, molecular docking, molecular dynamics simulations, and ADMET prediction.

**Project Obejctive**
**Dataset Curation ** - A curated dataset of experimentally validated hTopoIIα inhibitors was assembled to capture relevant chemical space and guide model fine-tuning toward biologically meaningful scaffolds.

# Training Parameters

| Section    | Parameter           | Description                           | Value/Comment                   
| Model      | Number of layers    | Number of stacked LSTM layers         | 7                             
             | Hidden units        | Number of hidden units per LSTM layer | 128                            
            
| Training   | Epochs              | Number of training epochs             |80                              
             | Learning rate       | Optimizer learning rate               | 0.001                          
             | Batch size          | Number of molecules per batch         | 1024                            
| Generation | Temperature         | Sampling temperature                  | 0.8                            
             | Number of molecules | Number of generated structures        | 3000                            

 Fine-Tuning

Fine-tuning requires a pretrained LSTM model and the corresponding target-specific molecular dataset.

# SMILES Generation

Following fine-tuning, the TOPOTIDE model is used to generate new molecular structures represented as SMILES strings.

Molecular generation is performed sequentially, with the model predicting one molecular character/token at a time.

Temperature-controlled sampling is used to control the stochasticity of the generation process.

A lower temperature produces more conservative sampling, whereas increasing the temperature increases sampling variability and exploration of molecular sequence space.

The generated molecules are subsequently subjected to chemical validation and molecular evaluation.

# Reinforcement Learning

Reinforcement learning is incorporated to guide molecular generation according to predefined molecular objectives.

The reinforcement-learning stage can assign rewards to desirable molecular characteristics and penalties to undesirable structures.


# Repository Structure

TOPOTIDE/
│
├── Environment/
│   └── environment.yml
│
├── Preprocessing/
│   └── data_preprocessing.py
│
├── Model/
│   └── model_development.py
│
├── Fine-tuning/
│   └── fine-tuning.py
│
├── Smiles Generation/
│   └── SMILES_generation.py
│
├── Reinforcement-learning/
│
├── Molecular-properties/
│
├── Evaluation/
│
├── Benchmarking/
│   ├── VAE/
│   ├── MolGPT/
│   ├── MoLFormer/
│   └── Transformer/
│
├── Docking/
│
├── Molecular-Dynamics/
│
├── ADMET/
│
├── requirements.txt
│
└── README.md

