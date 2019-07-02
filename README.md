# NLI_datasets: Datasets on inference

## Dataset format:

 premise | hypothesis| label
 "bla bla", "bla bla", "entailment"

 csv format

## FRACAS

 - paper: 
    @MISC{Fracas96,
        author = {{The Fracas Consortium} and
                  Robin Cooper and
                  Dick Crouch and
                  Jan Van Eijck and
                  Chris Fox and
                  Josef Van Genabith and
                  Jan Jaspars and
                  Hans Kamp and
                  David Milward and
                  Manfred Pinkal and
                  Massimo Poesio and
                  Steve Pulman and
                  Ted Briscoe and
                  Holger Maier and
                  Karsten Konrad},
        title = {Using the Framework},
        year = {1996}
    }
 - year: 1996
 - type: NLI dataset
 - adapted from https://nlp.stanford.edu/~wcmac/downloads/fracas.xml
     We took P1, ..Pn as premise
             H as hypothesis
             label = {'yes': "entailment",
                      'no': 'contradiction',
                      'undef': "neutral",
                       'unknown': "neutral"}
                       
     And we randomly split 80/20 for train/dev.
   
 - link: https://drive.google.com/open?id=13-gDw3lnxqnqYwXQUdH0bPsPPZXdD5n7


## RTE
 
 - paper:
     @inproceedings{wang-etal-2018-glue,
        title = "{GLUE}: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding",
        author = "Wang, Alex  and
          Singh, Amanpreet  and
          Michael, Julian  and
          Hill, Felix  and
          Levy, Omer  and
          Bowman, Samuel",
        booktitle = "Proceedings of the 2018 {EMNLP} Workshop {B}lackbox{NLP}: Analyzing and Interpreting Neural Networks for {NLP}",
        month = nov,
        year = "2018",
        address = "Brussels, Belgium",
        publisher = "Association for Computational Linguistics",
        url = "https://www.aclweb.org/anthology/W18-5446",
        pages = "353--355",
        abstract = "For natural language understanding (NLU) technology to be maximally useful, it must be able to process language in a way that is not exclusively tailored to a specific task, genre, or dataset.",
    }
 - year: 2006, 2007, 2009 -> (created from RTE1, RTE2, RTE3, RTE5)
 - type: RTE dataset
 - link: https://drive.google.com/open?id=1-7xH81M__XsKF7Uog5nemoNppabiKqZy

## COPA

 - paper: 
     @inproceedings{wang-etal-2019-superglue,
        title = "{SuperGLUE}: A Stickier Benchmark for General-Purpose Language
                 Understanding Systems",
                 author = "Wang, Alex  and
                 Singh, Amanpreet  and
                 Michael, Julian  and
                 Hill, Felix  and
                 Levy, Omer  and
                 Bowman, Samuel",
                 year = "2019",
                 url = "https://w4ngatang.github.io/static/papers/superglue.pdf"}
 - year: 21 March 2011 (constructed from http://people.ict.usc.edu/~gordon/copa.html)
 - type: RTE dataset
 - note: I have modified the original dataset as follows:
        original:

         premise                                |       choice1       |          choice2            |        label
         My body cast a shadow over the grass   |  The sun was rising |     The grass was cut       |          0

        transformed:

          premise                              |    hypothesis     |   label
          My body cast a shadow over the grass | The sun was rising| entailment
          My body cast a shadow over the grass | The grass was cut | not_entailment
 - link: https://drive.google.com/open?id=1UYXo9OQOnu51yjunHGBwSa6Jj_YFoCLR


## WNLI

 - paper: 
     @inproceedings{wang-etal-2018-glue,
        title = "{GLUE}: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding",
        author = "Wang, Alex  and
          Singh, Amanpreet  and
          Michael, Julian  and
          Hill, Felix  and
          Levy, Omer  and
          Bowman, Samuel",
        booktitle = "Proceedings of the 2018 {EMNLP} Workshop {B}lackbox{NLP}: Analyzing and Interpreting Neural Networks for {NLP}",
        month = nov,
        year = "2018",
        address = "Brussels, Belgium",
        publisher = "Association for Computational Linguistics",
        url = "https://www.aclweb.org/anthology/W18-5446",
        pages = "353--355",
        abstract = "For natural language understanding (NLU) technology to be maximally useful, it must be able to process language in a way that is not exclusively tailored to a specific task, genre, or dataset.",
    }
 - year: January 2012 -> (created from The Winograd Schema Challenge)
 - type: RTE dataset
 - link: https://drive.google.com/open?id=1R1aR18dC4ke1TUSzDl8Pwr4VviDgpX_q


## SICK

 - paper: 
    @inproceedings{Marelli2014,
      title={A SICK cure for the evaluation of compositional distributional semantic models},
      author={Marco Marelli and
              Stefano Menini and
              Marco Baroni and
              Luisa Bentivogli and
              Raffaella Bernardi and
              Roberto Zamparelli},
      booktitle={LREC},
      year={2014}
}
 - year: 2014
 - type: NLI dataset
 - I could not find the original dataset. Hence I used two Github repositories to get 10K examples:
   - https://github.com/text-machine-lab/MUTT
   - https://github.com/lukecq1231/sent_enc_nli_sick
 - link: https://drive.google.com/open?id=1rT4KC-uNInSVQmgolwvK0mGfBmeO5M-a 
 
## SNLI

 - paper: 
    @inproceedings{snli:emnlp2015,
        Author = {Bowman, Samuel R. and Angeli, Gabor and Potts, Christopher, and Manning, Christopher D.},
        Booktitle = {Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing (EMNLP)},
        Publisher = {Association for Computational Linguistics},
        Title = {A large annotated corpus for learning natural language inference},
        Year = {2015}}
 - year: 2015
 - type: NLI dataset
 - link: https://drive.google.com/open?id=1k1Mj0-vVdGuPkx3BaP_BGCUyRb-97Mx2
 

## Add-one RTE
 - paper: 
    @inproceedings{DBLP:conf/acl/PavlickC16,
      author    = {Ellie Pavlick and
                   Chris Callison{-}Burch},
      title     = {Most "babies" are "little" and most "problems" are "huge": Compositional
                   Entailment in Adjective-Nouns},
      booktitle = {Proceedings of the 54th Annual Meeting of the Association for Computational
                   Linguistics, {ACL} 2016, August 7-12, 2016, Berlin, Germany, Volume
                   1: Long Papers},
      year      = {2016},
      crossref  = {DBLP:conf/acl/2016-1},
      url       = {http://aclweb.org/anthology/P/P16/P16-1204.pdf},
      timestamp = {Mon, 15 Aug 2016 20:10:51 +0200},
      biburl    = {https://dblp.org/rec/bib/conf/acl/PavlickC16},
      bibsource = {dblp computer science bibliography, https://dblp.org}
    }
- year: 15 Aug 2016
- type: RTE dataset
- link: https://drive.google.com/open?id=14CLKNNUjzgGSDW-1kaKmr9VfGzgmtixL


## QNLI

 - paper: 
     @inproceedings{wang-etal-2018-glue,
        title = "{GLUE}: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding",
        author = "Wang, Alex  and
          Singh, Amanpreet  and
          Michael, Julian  and
          Hill, Felix  and
          Levy, Omer  and
          Bowman, Samuel",
        booktitle = "Proceedings of the 2018 {EMNLP} Workshop {B}lackbox{NLP}: Analyzing and Interpreting Neural Networks for {NLP}",
        month = nov,
        year = "2018",
        address = "Brussels, Belgium",
        publisher = "Association for Computational Linguistics",
        url = "https://www.aclweb.org/anthology/W18-5446",
        pages = "353--355",
        abstract = "For natural language understanding (NLU) technology to be maximally useful, it must be able to process language in a way that is not exclusively tailored to a specific task, genre, or dataset.",
    }
 - year: 11 october 2016 -> (created from The Standford Question Answering Dataset)
 - type: RTE dataset
 - link: https://drive.google.com/open?id=1_5BK3fWBzQouS8XtLGx57TFQhRlAjRTN


## MNLI

 - paper: 
     @InProceedings{williams2018broad,
      author    = {Williams, Adina and Nangia, Nikita and Bowman, Samuel R.},
      title     = {A Broad-Coverage Challenge Corpus for Sentence Understanding through Inference},
      booktitle = {Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies},
      year      = {2018},
      publisher = {Association for Computational Linguistics}}
 - year:  18 Apr 2017 
 - type: NLI dataset
 - link: https://drive.google.com/open?id=1zW3D9E6uVcKRvAEsS_inI31J4QO1J3po

## JOCI

 - paper: 
     @article{DBLP:journals/corr/ZhangRDD16,
      author    = {Sheng Zhang and
                   Rachel Rudinger and
                   Kevin Duh and
                   Benjamin Van Durme},
      title     = {Ordinal Common-sense Inference},
      journal   = {CoRR},
      volume    = {abs/1611.00601},
      year      = {2016},
      url       = {http://arxiv.org/abs/1611.00601},
      archivePrefix = {arXiv},
      eprint    = {1611.00601},
      timestamp = {Mon, 05 Nov 2018 11:12:21 +0100},
      biburl    = {https://dblp.org/rec/bib/journals/corr/ZhangRDD16},
      bibsource = {dblp computer science bibliography, https://dblp.org}
    }
 - year: 2 Jun 2017
 - modification: {0-1: contradiction,
                  2-4: neutral,
                  5:entailment}
   Could not find the original dataset. Only a part in http://decomp.io/data/
 - type: NLI dataset
 - link: https://drive.google.com/open?id=1F-y_J3QbgxKV5QnigvlQYw9XgxwFZzwk
 
## IIE
 
 - paper: 
    @inproceedings{white-etal-2017-inference,
        title = "Inference is Everything: Recasting Semantic Resources into a Unified Evaluation Framework",
        author = "White, Aaron Steven  and
          Rastogi, Pushpendre  and
          Duh, Kevin  and
          Van Durme, Benjamin",
        booktitle = "Proceedings of the Eighth International Joint Conference on Natural Language Processing (Volume 1: Long Papers)",
        month = nov,
        year = "2017",
        address = "Taipei, Taiwan",
        publisher = "Asian Federation of Natural Language Processing",
        url = "https://www.aclweb.org/anthology/I17-1100",
        pages = "996--1005",
        abstract = "We propose to unify a variety of existing semantic classification tasks, such as semantic role labeling, anaphora resolution, and paraphrase detection, under the heading of Recognizing Textual Entailment (RTE). We present a general strategy to automatically generate one or more sentential hypotheses based on an input sentence and pre-existing manual semantic annotations. The resulting suite of datasets enables us to probe a statistical RTE model{'}s performance on different aspects of semantics. We demonstrate the value of this approach by investigating the behavior of a popular neural network RTE model.",
    }
 - year:  27 NOV 2017 
 - type: RTE dataset
 - collect from: http://decomp.io/projects/diverse-natural-language-inference/
 - link: https://drive.google.com/open?id=1vYE0lAMf_G0iLKCV9oE31xxnxQPZbLTv

## MPE

  - paper: 
    @inproceedings{lai-etal-2017-natural,
        title = "Natural Language Inference from Multiple Premises",
        author = "Lai, Alice  and
          Bisk, Yonatan  and
          Hockenmaier, Julia",
        booktitle = "Proceedings of the Eighth International Joint Conference on Natural Language Processing (Volume 1: Long Papers)",
        month = nov,
        year = "2017",
        address = "Taipei, Taiwan",
        publisher = "Asian Federation of Natural Language Processing",
        url = "https://www.aclweb.org/anthology/I17-1011",
        pages = "100--109",
        abstract = "We define a novel textual entailment task that requires inference over multiplepremise sentences. We present a new dataset for this task that minimizestrivial lexical inferences, emphasizes knowledge of everyday events, andpresents a more challenging setting for textual entailment. We evaluate severalstrong neural baselines and analyze how the multiple premise task differs fromstandard textual entailment.",
    }
 - year:  27 NOV 2017 
 - type: NLI dataset
 - link: https://drive.google.com/open?id=1oH5YpPg1gkddrrV6TRA5tA7zxnVkjqiX
 
## Scitail

 - paper: 
        @inproceedings{scitail,
                Author = {Tushar Khot and Ashish Sabharwal and Peter Clark},
                Booktitle = {AAAI}
                Title = {SciTail: A Textual Entailment Dataset from Science Question Answering},
                Year = {2018}
                }
 - year: 27 Apr 2018
 - type: RTE dataset
 - alteration: I have changed the labels:
                 {"neutral": "not_entailment",
                 "entailment": "entailment"} 
 - link: https://drive.google.com/open?id=11VMy9l6RNBXfvgD9_GfMHHj8e95gokel 

## Commitment Bank

 - paper: 
     @inproceedings{wang-etal-2019-superglue,
        title = "{SuperGLUE}: A Stickier Benchmark for General-Purpose Language
                 Understanding Systems",
                 author = "Wang, Alex  and
                 Singh, Amanpreet  and
                 Michael, Julian  and
                 Hill, Felix  and
                 Levy, Omer  and
                 Bowman, Samuel",
                 year = "2019",
                 url = "https://w4ngatang.github.io/static/papers/superglue.pdf"}
 - year: 2019 (constructed from https://github.com/mcdm/CommitmentBank)
 - type: NLI dataset
 - link: https://drive.google.com/open?id=1wGq7tMT76CDfhPUYt9DJSvQRTL5fhp8r
 
 
 

