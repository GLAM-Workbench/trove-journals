# Trove journals

Current version: [v1.0.0](https://github.com/GLAM-Workbench/trove-journals/releases/tag/v1.0.0)

Examples of working with data from Trove's Journals zone. For more information see the [Trove Journals](https://glam-workbench.net/trove-journals/) section of the GLAM Workbench.

## Harvesting metadata

* [Create a list of Trove's digitised journals](Create-digitised-journals-list.ipynb) – uses the Trove API to harvest metadata relating to periodicals available from Trove in digital form.

## Harvesting text

* [Get OCRd text from a digitised journal in Trove](Get-text-from-a-Trove-journal.ipynb) – shows how to extract issue data from a digitised journal and download OCRd text for each issue.
* [Download the OCRd text for ALL the digitised journals in Trove!](Download-text-for-all-digitised-journals.ipynb) – using the code and data from the previous two notebooks, you can download the OCRd text from every digitised journal.
* [Harvest parliament press releases from Trove](Harvest-parliament-press-releases.ipynb) – shows you how to harvest both metadata and full text from a search of the parliamentary press releases.
* [Create a database to search across each line of text in a series of volumes](index-each-line-in-series.ipynb) – index any series of publication where it would be useful to search by line.

## Harvesting images

* [Get covers (or any other pages) from a digitised journal in Trove](Get-page-images-from-a-Trove-journal.ipynb) – shows how to download all the cover images from a specified journal. With some minor modifications you could download any page, or range of pages.
* [Finding editorial cartoons in the Bulletin](Finding_editorial_cartoons_in_the_Bulletin.ipynb) – full page editorial cartoons were a consistent feature of The Bulletin for many decades, I wanted to try and assemble a collection of all the editorial cartoons, but how?

See the [GLAM Workbench for more details](https://glam-workbench.github.io/trove-journals/).


<!-- START RUN INFO -->


## Run these notebooks

There are a number of different ways to use these notebooks. Binder is quickest and easiest, but it doesn't save your data. I've listed the options below from easiest to most complicated (requiring more technical knowledge).

### Using Binder

[![Launch on Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GLAM-Workbench/trove-journals/master/?urlpath=lab/tree/index.ipynb)

Click on the button above to launch the notebooks in this repository using the [Binder](https://mybinder.org/) service (it might take a little while to load). This is a free service, but note that sessions will close if you stop using the notebooks, and no data will be saved. Make sure you download any changed notebooks or harvested data that you want to save.

See [Using Binder](https://glam-workbench.net/using-binder/) for more details.

### Using Reclaim Cloud

[![Launch on Reclaim Cloud](https://glam-workbench.github.io/images/launch-on-reclaim-cloud.svg)](https://app.my.reclaim.cloud/?manifest=https://raw.githubusercontent.com/GLAM-Workbench/trove-journals/master/reclaim-manifest.jps)

[Reclaim Cloud](https://reclaim.cloud/) is a paid hosting service, aimed particularly at supported digital scholarship in hte humanities. Unlike Binder, the environments you create on Reclaim Cloud will save your data – even if you switch them off! To run this repository on Reclaim Cloud for the first time:

* Create a [Reclaim Cloud](https://reclaim.cloud/) account and log in.
* Click on the button above to start the installation process.
* A dialogue box will ask you to set a password, this is used to limit access to your Jupyter installation.
* Sit back and wait for the installation to complete!
* Once the installation is finished click on the 'Open in Browser' button of your newly created environment (note that you might need to wait a few minutes before everything is ready).

See [Using Reclaim Cloud](https://glam-workbench.net/using-reclaim-cloud/) for more details.

### Using Docker

You can use Docker to run a pre-built computing environment on your own computer. It will set up everything you need to run the notebooks in this repository. This is free, but requires more technical knowledge – you'll have to install Docker on your computer, and be able to use the command line.

* Install [Docker Desktop](https://docs.docker.com/get-docker/).
* Create a new directory for this repository and open it from the command line.
* From the command line, run the following command:  
  ```
  docker run -p 8888:8888 --name trove-journals -v "$PWD":/home/jovyan/work quay.io/glamworkbench/trove-journals repo2docker-entrypoint jupyter lab --ip 0.0.0.0 --NotebookApp.token='' --LabApp.default_url='/lab/tree/index.ipynb'
  ```
* It will take a while to download and configure the Docker image. Once it's ready you'll see a message saying that Jupyter Notebook is running.
* Point your web browser to `http://127.0.0.1:8888`

See [Using Docker](https://glam-workbench.net/using-docker/) for more details.

### Setting up on your own computer

If you know your way around the command line and are comfortable installing software, you might want to set up your own computer to run these notebooks.

Assuming you have recent versions of Python and Git installed, the steps might be something like:

* Create a virtual environment, eg: `python -m venv trove-journals`
* Open the new directory" `cd trove-journals`
* Activate the environment `source bin/activate`
* Clone the repository: `git clone https://github.com/GLAM-Workbench/trove-journals.git notebooks`
* Open the new `notebooks` directory: `cd notebooks`
* Install the necessary Python packages: `pip install -r requirements.txt`
* Run Jupyter: `jupyter lab`

See [Getting started](https://glam-workbench.net/getting-started/#using-python-on-your-own-computer) for more details.

<!-- END RUN INFO -->

## Cite as

See the [GLAM Workbench](https://glam-workbench.net/trove-journals/#cite-as) or [Zenodo](https://doi.org/10.5281/zenodo.6622312) for up-to-date citation details.

----

This repository is part of the [GLAM Workbench](https://glam-workbench.github.io/).  
