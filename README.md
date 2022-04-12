# Datasets for the Creative-Summ 2022 Workshop
This repository contains the datasets for the shared task of the Automatic Summarization for Creative Writing (Creative-Summ) workshop at COLING 2022.

More information can be found at https://creativesumm.github.io/sharedtask.

## Shared Task Overview
The CreativeSumm 2022 shared task is divided into four sub-tasks, namely:

- summarization of chapters from novels
- summarization of movie scripts
- summarization of primetime television transcripts
- summarization of daytime, “soap opera” transcripts

The training data for each sub-task comes from existing, well-established datasets (see below), but **for the movie and television sub-tasks we will provide new, unseen test inputs for evaluation**.


## Corpora

### Novel Chapters/BookSum (Ladhak et al., 2020; Kryściński et al., 2021)
This dataset pairs chapters of novels released as part of Project Gutenberg with corresponding summaries. For this shared task, we provide the novel chapters
[here](https://github.com/fladhak/creative-summ-data/tree/main/booksum). We unfortunately cannot provide the summaries, as the study guide websites are copyrighted. Each novel chapter in the provided data, however, does have a link to the page where the summary text may be found.

Please see the associated papers Ladhak et al. (2020) and Kryściński et al. (2021) papers for more information on how they collected the summaries.

Notes:
- **For the novel chapter summarization task, please do not use the test splits (of either NovelChapter or BookSum) for either training or development.**
- **Note that the provided links and alignments in this repo have excluded test set books -- ensure you do the same!**
- **We will use the test set of BookSum as part of the final evaluation. We may or may not provide new, unseen test inputs for the final evaluation as well.**

### Scriptbase (Gorinski & Lapata, 2015)
This dataset pairs movie transcripts with their corresponding Wikipedia summaries. The data may be downloaded from [here](https://github.com/EdinburghNLP/scriptbase/tree/master/scriptbase_alpha). See the main [repository](https://github.com/EdinburghNLP/scriptbase) for additional information.

**TODO**: I assume we'll use `script.txt` as the input. Do we want the target to be `processed/wikiplot.txt` (plain text synopsis from Wikipedia) or the `processed/summaries` (the shorter, trailer-style IMDB blurbs)?

Notes:
- **You may use any part of this dataset for training, since we will be providing new inputs for evaluation.**
- **We recommend training on the training+validation sets, and using the test set for validation.**

### SummScreen, Forever Dreaming (Chen et al., 2022)
This dataset pairs TV transcripts from primetime shows with their corresponding Wikipedia summaries. We will use version of this data associated with the [SCROLLS Benchmark](https://www.scrolls-benchmark.com/) (Shaham et al., 2022), and you may download the data [there](https://www.scrolls-benchmark.com/tasks).

Notes:
- **You may use any part of this dataset for training, since we will be providing new inputs for evaluation.**
- **We recommend training on the training+validation sets, and using the test set for validation.**

### SummScreen, TV Megasite (Chen et al., 2022)
This dataset pairs soap opera transcripts with summaries written by TV Megasite contributors. We have preprocessed the data so that it is in the same format as the Forever Dreaming data (i.e., it follows SCROLLS conventions), and it may be downloaded [here](summscreen_tms.zip).

Notes:
- **You may use any part of this dataset for training, since we will be providing new inputs for evaluation.**
- **We recommend training on the training+validation sets, and using the test set for validation.**

## References
Mingda Chen, Zewei Chu, Sam Wiseman, Kevin Gimpel. 2022. [SummScreen: A Dataset for Abstractive Screenplay Summarization](https://aclanthology.org/N15-1113/). In ACL.

Philip John Gorinski, Mirella Lapata. 2015. [Movie Script Summarization as Graph-based Scene Extraction](https://aclanthology.org/N15-1113/). In NAACL.

Wojciech Kryściński, Nazneen Rajani, Divyansh Agarwal, Caiming Xiong, Dragomir Radev. 2021. [BookSum: A Collection of Datasets for Long-form Narrative Summarization](https://arxiv.org/pdf/2105.08209.pdf).

Faisal Ladhak, Bryan Li, Yaser Al-Onaizan, Kathlen McKeown. 2020. [Exploring Content Selection in Summarization of Novel Chapters](https://aclanthology.org/2020.acl-main.453/). In ACL.
