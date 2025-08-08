# Code:You Capstone Project

I chose to look at weather data for my capstone project. I did this because our summers have become hotter, we have had more and more tornadoes in our region, and lots more extreme weather. While I know the weather and our atmosphere is changing due to pollution and other factors, I wanted to look at exactly how much things are actually changing. I constantly feel like things are so much x or y compared to when I was a kid; but I always wonder if it's just because I'm seeing more details now than I was when I was younger. So I'm curious if things are actually that much different from what I remember as a kid. I picked Lexington, KY to look at, because it's fairly central to Kentucky, it's one of the larger cities, and there's more data available.

I hope to look at the data and see what trends we can spot plotting the data on some graphs!

## Installation

1. Clone or download this repository to your local machine

2. Create and activate a virtual environment:

   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate

   # Mac/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. Open the `data_analysis.ipynb` notebook to view and run the analysis

## Rebuild Database

If you want to rebuild the database, or choose not to download the database with this repo, please run the `data_cleaning.ipynb` file before opening `data_analysis.ipynb`

## Data

I was able to collect all of the data from NOAA. There is such a wealth of data available to us from the NOAA, it was a pleasant suprise to see just how far back the data went.

For this project, I downloaded a few datasets. The main two datasets start from the earliest point in time that the NOAA has to offer for Lexington: 1048! The data is pretty up to date, and so we were able to pull data all the way until late July of 2025. While this will be interesting to look at, having a partial year will probably skew some data. I separated this data into two sets: what I chose to call "current" (2000-2025) and "historical" (1948-1999). I handled the data this way so that I could easily keep them separated and potentially compare them side by side.

The next datasets I collected were daily values from 2000 to now. This data comes from multiple sources, with lots of missing data. The main goal for these sets was to collect the daily information: the max, min and average. So I cleaned up the data to drop any row that did not have any information in the MAX and MIN columns, and created an average using those two columns if the column was null.

- [NOAA](https://www.ncei.noaa.gov/access/search/index)

## Resources/Technologies Used

Pandas: Core technology used to handle the massive amounts of data from the csv files.
Jupyter Notebooks: One of the core technologies used; everything was written in a jupyter notebook to easily experiment with and display the process as I went through this project.
sqlite3: Used to create a simple database using the dataframe information.
Mathplotlib:
Seaborn:
