## Introduction

This project "Finding the Octopus Alley" explores the concept of bellwether. A bellweter refers to a specific county or region that historically tends to vote for the eventual winner of a national election. In Taiwan, if a candidate wins in a so-called "Octopus Alley", people generally assume they will likely win the entire country. 

However, based on the data from the [2024 Taiwan presidential election](https://db.cec.gov.tw/ElecTable/Election/ElecTickets?dataType=tickets&typeId=ELC&subjectId=P0&legisId=00&themeId=4d83db17c1707e3defae5dc4d4e9c800&dataLevel=N&prvCode=00&cityCode=000&areaCode=00&deptCode=000&liCode=0000), this project aims to show that the "Octopus Alley" is a myth. This can be debunked by two major factors:

1. The population profiles change over time, and react differently to various types of elections; therefore, considering a single neighborhood like Tianyu (天玉里) to be a bellwether for every elections is irrational. 

2. Mainstream media constantly proclaims that the polling results from Tianyu are'highly predictive' of national election without providing an operational definition of the predictability or explaining it was calculated. 

To explore this phenomenon further, we used `pandas` and `SQLite` to create an election database. We also verified closeness of regional and national polling results using "cosine similarity". Finally, we presented the retults through a `Gradio` UI interface. 


## How to Reproduce

1. Install Miniconda.

2. Create the environment using environment.yml by running: `conda env create -f environment.yml`.

3. Place the 22 spreadsheet files from the "Presidential-A05-4-Candidate Vote Count Summary-By Polling Station" folder into the project's `data/` directory.

4. Activate the environment and run python `create_taiwan_presidential_election_2024_db.ipynb` to generate the taiwan_presidential_election_2024.db file in the `data/` directory.

5. Activate the environment and run python app.py, then navigate to http://127.0.0.1:7860 to view the final results.