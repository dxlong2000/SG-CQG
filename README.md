# Modeling What-to-ask and How-to-ask for Answer-unaware Conversational Question Generation (ACL 2023)

Code and data for the ACL 2023 paper: https://aclanthology.org/2023.acl-long.603.pdf

*Note: All the pre-trained models can be found [here](https://drive.google.com/drive/folders/1zsboereNjLl55XI7TZ9EDtwNX9ffEzHQ?usp=sharing).*

## 1. About the Two Notebooks
- Notebook ```SG_CQG_Graph_Construction.ipynb``` contains the class ```Semantic_Graph_Constructor``` which constructs our proposed semantic graph integrating **coreference, co-occurence, name entities** information, given a context. To create a semantic graph from a context, one can create an instance of the above class and call the ```build_linking_graph``` function to get the triples. See the example in the notebook. 

- Notebook ```SG_CQG_Generate_Conversations.ipynb``` contains the class ```Generate_Conversation_from_Graph``` aiming to generate a conversation, given a semantic graph and a context. It is achievable by calling 1 function. One can see the notebooks for the sample calls.

## 2. Pre-requisites Softwares
Please check the two notebooks for different setups.

## 3. Reference
Any question, please email directly to **Do Xuan Long** via email: *xuanlong.do@u.nus.edu*.

If you have found the codes helpful, please consider to cite the paper:

```
@inproceedings{do-etal-2023-modeling,
    title = "Modeling What-to-ask and How-to-ask for Answer-unaware Conversational Question Generation",
    author = "Do, Xuan Long  and
      Zou, Bowei  and
      Joty, Shafiq  and
      Tai, Tran  and
      Pan, Liangming  and
      Chen, Nancy  and
      Aw, Ai Ti",
    booktitle = "Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.acl-long.603",
    pages = "10785--10803",
    abstract = "Conversational Question Generation (CQG) is a critical task for machines to assist humans in fulfilling their information needs through conversations. The task is generally cast into two different settings: answer-aware and answer-unaware. While the former facilitates the models by exposing the expected answer, the latter is more realistic and receiving growing attentions recently. What-to-ask and how-to-ask are the two main challenges in the answer-unaware setting. To address the first challenge, existing methods mainly select sequential sentences in context as the rationales. We argue that the conversation generated using such naive heuristics may not be natural enough as in reality, the interlocutors often talk about the relevant contents that are not necessarily sequential in context. Additionally, previous methods decide the type of question to be generated (boolean/span-based) implicitly. Modeling the question type explicitly is crucial as the answer, which hints the models to generate a boolean or span-based question, is unavailable. To this end, we present SG-CQG, a two-stage CQG framework. For the what-to-ask stage, a sentence is selected as the rationale from a semantic graph that we construct, and extract the answer span from it. For the how-to-ask stage, a classifier determines the target answer type of the question via two explicit control signals before generating and filtering. In addition, we propose Conv-Distinct, a novel evaluation metric for CQG, to evaluate the diversity of the generated conversation from a context. Compared with the existing answer-unaware CQG models, the proposed SG-CQG achieves state-of-the-art performance.",
}
```

