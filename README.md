This is an official repository for [ProvG-Searcher: A Graph Representation Learning Approach for Efficient Provenance Graph Search](https://arxiv.org/pdf/2309.03647.pdf).

The repository provides three main capabilities for using ProvG-Searcher:

1. **Calculating Sampling Stats:** It calculates the sampling statistics used during training.
2. **Training the Model:** It trains the model on Darpha datasets.
3. **Testing the Model:** It tests the models on Darpha datasets.

## Installation

You can set up the conda environment with all the requirements using the following command:

```bash
conda env create -f environment.yml
```

## Data

For Darpha datasets, ego graphs and node features can be obtained from [Drive](https://drive.google.com/drive/folders/1ltVVOl31qNhrmK9z8ii0r5u3ZQUCnImF?usp=sharing). Unzip the files and place them in the `data` and `node_feature` folders, respectively.

## Training

The model can be trained for each dataset as follows:

```bash
python -u run.py --dataset data/[dataset_name]/k_[number_of_neighborhood].pt --data_identifier [dataset_name] --model_path ckpt/[dataset_name]_model.pth
```

Here, `[dataset_name]` can be one of:

- ta1-theia-e3-official-6r
- fiveDirection
- cadets_data
- trace_data

and `[number_of_neighborhood]` can be 3 or 5.

## Testing

To test a model, set the testing arguments to True.

The model part of the code is forked from [neural-subgraph-learning-GNN repository](https://github.com/snap-stanford/neural-subgraph-learning-GNN).

# Interpret-ProvG-Searcher 可解释的溯源图搜索模型

