# RepoDataset

Repository metadata as dataset

## Setup the Environment

The development was done using Jupyter extension in [Visual Studio Code](https://code.visualstudio.com/), so it may work diirectly with "pure" Jupyter, but probably there are packages missing to run with Jupyter Labs.

To set the environment inside [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) (probably the same for any Linux):

```
mgarcia@arda:~/Work$ git clone https://github.com/kaust-library/RepoDataset.git
mgarcia@arda:~/Work/RepoDataset$ python -m venv venv
mgarcia@arda:~/Work/RepoDataset$ . venv/bin/activate
mgarcia@arda:~/Work/RepoDataset$ pip install -r requirements.txt
# 
# Unzip the sample data file
mgarcia@arda:~/Work/RepoDataset$ cd data
mgarcia@arda:~/Work/RepoDataset/data$ unzip kaust_repo.zip
Archive:  kaust_repo.zip
  inflating: kaust_repo.csv
mgarcia@arda:~/Work/RepoDataset/data$
```

## Usage

Using the jupyter notebook to explore the Insitutionl Repository metadata dataset.

We provide three examples to explore the dataset:

* `repodataset.ipynb`: Publication types, and top publishers.
* `gettext.ipynb`: Download the text version of the PDF, or save the URLs to a text that can be downloaded with commands like `wget` or `curl.`
* `vosviwer.ipynb`: Export certain fields to [Vosviewer](https://www.vosviewer.com/), like _abstract_ or _authors_. There is an option to plot the map using all fields, but it takes several minutes to create the plot. 

## Data

We provide a sample of the data in the `data` directory, that is for a simple tests. Once the tests are done, one can use the full dataset available on the repository website:

```
https://repository.kaust.edu.sa/bitstream/handle/10754/691066/KAUST_Affiliated_Research_Basic_Metadata.csv
```

The VOSviewer notebook expects to find the full CSV file in the `data` directory. One can download directly using the URL above.