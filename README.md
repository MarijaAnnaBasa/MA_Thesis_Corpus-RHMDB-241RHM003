# Introduction

The present repository concerns the corpus created for the empirical analysis of Master's Thesis 'Comparative Discourse Analysis of Russia-Ukraine War Coverage in Russian and Ukrainian Online Media Outlets' conducted within the RTU studies program RHMDB Digital Humanities. The research author is **Marija Anna Baša**; identity card number is **241RHM003**.
Thus, the repository regards the matter of both the analysed corpora and the Python code created, being noted for one to perform the analysis concerning themes and narratives, framing of events, and propaganda and ideology setting within the corpus of the selected articles, i.e., that of *Sputnik* and *The Kyiv Independent*.

## Contents

The repository created consists of nine files.

Two Excel format files that contain the titles, external links to the respective articles, as well as the date of publishing (if such information was able to acquire in the scraping process):

- Sputnik_FULL.xlsx
- Kyiv_Ind_FULL.xlsx

Six Python files where all of the needed code is present:

- scraped_sputnik.py (saves articles of *Sputnik* as CSV files in one folder along with their metadata)
- scraped_kyiv.py (saves articles of *The Kyiv Independent* as CSV files in one folder along with their metadata)
- corpus_volume.py (counts the number of files and tokens within them)
- themes_and_narratives.py (performs modelling of topics, sentiment analysis of the gathered articles, as well as representative analysis within the created corpora)
- framing_of_events_.py (creates frames based on keywords noted and addresses the matter of sentiment analysis for each of the frames, while also executing the KWIC function)
- propaganda_ideology_setting.py (frames keywords for both ideology and propaganda frames, while also creating heatmaps based on their presence within the analysed corpora)

Within the list of files visible above, they ought to be run in the same sequence as they are listed, i.e., with the scraped_sputnik.py being the first one run and propaganda_ideology_setting.py - the last one. The reasons for that are that, firstly, that would ensure a cohesive analysis of the dataset in question, as it begins with noting the more common parameters, e.g., the volume of the corpora, and later proceeds with more complex notions like, e.g., entity analysis and frame creation for propaganda and ideology examination, and, secondly, the code consistently utilized the same variables where one line run is dependent upon the previous one due to the variable encoding, i.e., running the code out of order may result in errors.


Lastly, one file concerns a list of all Python packages along with their versions and dependencies used within the scope of the analysis:

- requirements.txt

## Environment setup 


1. Creating the virtual environment:

   python3 -m venv venv

2. Activating it:

  source venv/bin/activate (for macOS/Linux users)
  venv\Scripts\activate (for Windows users)


3. Installing the needed packages:

   pip install -r requirements.txt

   
### Additional notes

All path within the code now concerns a Google Drive (Colab) environment, so if copied directly into another Colab environment or run locally, the path ought to be updated.
Some scripts, particularly the one concerning the scraping of the corpus, may take several minutes to finish running.

