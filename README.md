# versatile-graph-learning-approaches

A comparisons of existing methods.

| Method                                  | Task Definition                                      | Taxonomy of feature engineering | Descriptions                                            | LLMs                        | Taxonomy of graph learning models | Descriptions                                                 | LLMs           | Deployment and Response                                      |
| --------------------------------------- | ---------------------------------------------------- | ------------------------------- | ------------------------------------------------------- | --------------------------- | --------------------------------- | ------------------------------------------------------------ | -------------- | ------------------------------------------------------------ |
| Graphtext~\cite{zhao2023graphtext}      | -                                                    | $\mathcal{G}^T$                 | The features and node labels of k-hop subgraphs         | -                           | Predictor                         | predicting labels of centric node                            | ChatGPT/GPT-4  | Using predictions as response                                |
| NLGraph~\cite{wang2023can}              | Formulating graph reasoning tasks with human experts | $\mathcal{G}^T$                 | Describing the graphs, nodes, edges and learning tasks. | -                           | Predictor                         | Predicting the statistics of graphs.                         | GPT-3.5 / GPT4 | Using predictions as response                                |
| GPT4Graph~\cite{guo2023gpt4graph}       | -                                                    | $\mathcal{G}^T$                 | self-prompting to describe the graphs.                  | InstructGPT-3               | Predictor                         | Predicting the statistics and Semantic labels of graphs.     | InstructGPT-3  | Using predictions as response                                |
| TLG~\cite{fatemi2023talk}               | Formulating graph reasoning tasks with human experts | $\mathcal{G}^T$                 | Describing the graphs, nodes, edges and learning tasks. | -                           | Predictor                         | Predicting the statistics of graphs.                         | PaLM 62B       | Using predictions as response                                |
| OFA~\cite{liu2023one}                   | -                                                    | $\mathcal{G}^{ST}$              | Explanations on $\mathcal{V}^T$ and $\mathcal{E}^T$     | ChatGPT                     | GLA-centric                       | co-trained LLMs and R-GCNs                                   | Sentence-bert  | -                                                            |
| \cite{chen2023exploring}                | -                                                    | $\mathcal{G}^{ST}$              | generating and encoding text information                | Open-source LLMs            | Predictor                         | ?                                                            | ?              | -                                                            |
| TAPE~\cite{he2023explanations}          | -                                                    | $\mathcal{G}^{ST}$              | Explanations on $\mathcal{V}^T$ Predictions, encoding   | GPT3.5, fine-tuning Deberta | -                                 | Training RevGAT with enriched features                       | -              | -                                                            |
| GRAD~\cite{mavromatis2023train}         | -                                                    | $\mathcal{G}^{ST}$              | Using the raw texts in graphs                           | -                           | Alignment-based                   | co-trained GNN teacher and LLM student                       | BERT           | -                                                            |
| GraphGPT~\cite{tang2023graphgpt}        | -                                                    | $\mathcal{G}^{ST}$              | Using the raw texts in graphs                           | -                           | Alignment-based                   | Applying contrastive alignment objective on the predictions of pre-trained GNNs and LLMs | Bert           | -                                                            |
| GraphPrompt~\cite{liu2023graphprompt}   | -                                                    | $\mathcal{G}^S$                 | Sampling and unifying data and tasks                    | -                           | GFMs                              | Pre-trains and prompted on downstream tasks                  | -              | -                                                            |
| All in One~\cite{sun2022gppt}           | Unified with graph-level tasks                       | $\mathcal{G}^S$                 | Constructing prompt graphs                              | -                           | GFMs                              | Pre-trained with multi-task meta-learning and prompted on downstream tasks | -              | -                                                            |
| Instruction2GL~\cite{wei2023unleashing} | Formulating tasks with ChatGPT-3.5                   | $\mathcal{G}^S$                 | Load and Split data based on user instructions          | ChatGPT-3.5                 | LLM-assisted                      | Configuring AutoML and                                       | ChatGPT-3.5    | Configuring codes and generating response with ChatGPT and the agents |
| GPT4GNAS~\cite{wang2023graph}           | -                                                    | $\mathcal{G}^S$                 | -                                                       | -                           | LLM-assisted                      | Selecting and evaluating GNNs on AutoML with LLMs.           | GPT-4          | -                                                            |





##### GRAPHTEXT: GRAPH REASONING IN TEXT SPACE   [[PDF](https://arxiv.org/abs/2310.01089)]

```
Jianan Zhao, Le Zhuo, Yikang Shen, Meng Qu, Kai Liu, Michael Bronstein, Zhaocheng Zhu, Jian Tang
```
Taxonomy

```
Task definition: -
Feature Engineering: 
	Taxonomy: Constructing $G^T$
	Descriptions: Sampling k-hop ego subgraphs, and then desceibe the labels and features of these nodes.
	LLMs: - 
Graph learning model:
	Taxonomy: Predict the labels based on the subgraph text directly.
```



