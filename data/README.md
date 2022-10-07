---
tags:
- hate-speech
- counterspeech
- irt
- arxiv:2009.10277
annotations_creators:
- crowdsourced
language:
- en
license: [cc-by-4.0]
multilinguality:
- monolingual
pretty_name: measuring-hate-speech
source_datasets:
- original
task_categories:
- text-classification
- text-regression
task_ids:
- hate-speech
- counterspeech
- sentiment-classification
---

## Dataset Description

- **Homepage:** http://hatespeech.berkeley.edu
- **Paper:** https://arxiv.org/abs/2009.10277

# Dataset card for _Measuring Hate Speech_

This is a public release of the dataset described in Kennedy et al. (2020), consisting of 39,565 comments annotated by 7,912 annotators, for 135,556 combined rows. The primary outcome variable is the "hate speech score" but the 10 constituent labels (sentiment, (dis)respect, insult, humiliation, inferior status, violence, dehumanization, genocide, attack/defense, hate speech benchmark) can also be treated as outcomes.  Includes 8 target identity groups (race/ethnicity, religion, national origin/citizenship, gender, sexual orientation, age, disability, political ideology) and 42 identity subgroups.

This dataset card is a work in progress and will be improved over time.

## Key dataset columns

 * hate_speech_score - continuous hate speech measure, where higher = more hateful and lower = less hateful
 * text - lightly processed text of a social media post
 * comment\_id - unique ID for each comment
 * annotator\_id - unique ID for each annotator
 * sentiment - ordinal label that is combined into the continuous score
 * respect - ordinal label that is combined into the continuous score
 * insult - ordinal label that is combined into the continuous score
 * humiliate - ordinal label that is combined into the continuous score
 * status - ordinal label that is combined into the continuous score
 * dehumanize - ordinal label that is combined into the continuous score
 * violence - ordinal label that is combined into the continuous score
 * genocide - ordinal label that is combined into the continuous score
 * attack\_defend - ordinal label that is combined into the continuous score
 * hatespeech - ordinal label that is combined into the continuous score
 * annotator_severity - annotator's estimated survey interpretation bias

## Code to download

The dataset can be downloaded using the following python code:

```python
import datasets 
dataset = datasets.load_dataset('ucberkeley-dlab/measuring-hate-speech', 'binary')   
df = dataset['train'].to_pandas()
df.describe()
```

## Citation

```
@article{kennedy2020constructing,
  title={Constructing interval variables via faceted Rasch measurement and multitask deep learning: a hate speech application},
  author={Kennedy, Chris J and Bacon, Geoff and Sahn, Alexander and von Vacano, Claudia},
  journal={arXiv preprint arXiv:2009.10277},
  year={2020}
}
```

## Contributions

Dataset curated by [@ck37](https://github.com/ck37), [@pssachdeva](https://github.com/pssachdeva), et al.

## References

Kennedy, C. J., Bacon, G., Sahn, A., & von Vacano, C. (2020). [Constructing interval variables via faceted Rasch measurement and multitask deep learning: a hate speech application](https://arxiv.org/abs/2009.10277). arXiv preprint arXiv:2009.10277.
