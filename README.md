# ED-mod


# INTRODUCTION
Entity description-enhanced temporal knowledge graph
reasoning(ED-mod)
The first is the extractor module, followed by the processing
of the textual information, and finally the execution of our experiments.


# COMPILE

1.extract and process

# WikiExtractor
[WikiExtractor.py](http://medialab.di.unipi.it/wiki/Wikipedia_Extractor) is a Python script that extracts and cleans text from a [Wikipedia database dump](https://dumps.wikimedia.org/).
The tool is written in Python and requires Python 3 but no additional library.
**Warning**: problems have been reported on Windows due to poor support for `StringIO` in the Python implementation on Windows.
#Usage
#Wikiextractor
The script is invoked with a Wikipedia dump file as an argument:

    python -m wikiextractor.WikiExtractor <Wikipedia dump file> [--templates <extracted template file>]

The option `--templates` extracts the templates to a local file, which can be reloaded to reduce the time to perform extraction.

2. execution of our experiment
	g++ Train_ED_mod.cpp -o Train_ED_mod -O2 -lpthread
	g++ Test_CBOW.cpp -o Test_CBOW -O2 -lpthread
	g++ Test_BiLSTM.cpp -o Test_BiLSTM -O2 -lpthread

# NOTE
From the original entity description to the accurate description of the entity, the Transformer model is used. For the training of the Transformer model, we use the abstract extraction dataset as training and testing data. Specifically, we use the Turing NLG model as the basis to generate our accurate entity descriptions.


# DATA
The ICEWS dataset is the data published by "ICEWS Coded Event Data" in 2015, you can visit https://doi.org/10.7910/DVN/28075 for details.
The GDELT dataset is “GDELT: Global data on events, location,
and tone.” published in 2013. You can visit http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.686.6605 for details.
Wikipedia Corpus downloads directly from the Wikipedia database, and then uses our extractor to process the raw data to obtain a clean dataset as entity descriptions.
enwiki.txt and experimentdata.zip. store the data we need to use.
