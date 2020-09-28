# Crowdsourced English Temporal Dependency Tree (TDT) Corpus

The Crowdsourced English Temporal Dependency Tree (TDT) Corpus is a collection of English news articles annotated with time expressions, events, and temporal relations. Temporal relations in this corpus are represented as a dependency tree structure for each article. Detailed descriptions about Temporal Dependency Tree structures can be found in [our paper](https://arxiv.org/pdf/1808.07599.pdf).

This corpus is built upon the [Timebank corpus](http://www.timeml.org/timebank/timebank.html). The temporal dependency tree annotations are collected through crowdsourcing. Details on our crowdsourcing approach can be found in [our paper](https://www.aclweb.org/anthology/S19-1019.pdf).

## Corpus Statistics


|  | # Docs | # Time Expressions | # Events | # Temporal Relations |
| :---: | :---: | :---: | :---: | :---: |
| **News Articles** | 183 | 1,414 | 2,691 | 4,105 |


## Corpus Format

```*.tdt``` files are the **t**emporal **d**ependency **t**rees for the Timebank news articles. Each line in a ```*.tdt``` file represents one child-parent pair. Each line has 9 fields, separated by tabs:

```
filename    cSnt    cStart  cEnd    cLabel  pSnt    pStart  pEnd    trLabel
```
- filename: the file ID
- cSnt: the sentence ID of the child
- cStart: the start word ID of the child
- cEnd: the end word ID of the child
- cLabel: the *time expression* or *event* label of the child
- pSnt: the sentence ID of the parent
- pStart: the start word ID of the parent
- pEnd: the end word ID of the parent
- trLabel: the temporal relation label between this child-parent pair

Please note: We use `-1 -1  -1` in the place of `pSnt   pStart  pEnd`, when the parent is the *ROOT* of the dependency tree.

### To use this corpus, please cite:

- Yuchen Zhang and Nianwen Xue. 2019. [Acquiring Structured Temporal Representation via Crowdsourcing: A Feasibility Study](https://www.aclweb.org/anthology/S19-1019.pdf). In Proceedings of the Eighth Joint Conference on Lexical and Computational Semantics (*SEM-2019), Minneapolis, U.S.

```
@inproceedings{zhang2019acquiring,
  title={Acquiring structured temporal representation via crowdsourcing: A feasibility study},
  author={Zhang, Yuchen and Xue, Nianwen},
  booktitle={Proceedings of the Eighth Joint Conference on Lexical and Computational Semantics (* SEM 2019)},
  pages={178--185},
  year={2019}
}
```
