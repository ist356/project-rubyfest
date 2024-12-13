# About My Project

Student Name:  Shane Rubenstein
Student Email:  srrubens@syr.edu

### What it does
The goal of this project is to scrape different political articles from right before the election from CBS and FOX to see how their language differs, and then see if I could develop a model that accurately categorizes articles as being from one site or the other.

### How you run my project
This project is mostly static at this point, as the only data that can be collected is from articles written before the election.

Make sure to install requirements.txt before running code

The three files with functions are cache_saves.py, get_site.py, and playwright_get_site.py. I would suggest running those first. 

Next, you should run get_sites.py, create_sites_df.py, data_manipulation.py, and ml_attempts.py (ml_attempts.py is not required for the finished product) in that order.

Finally, run st_analysis.py with streamlit to see the finished product

### Other things you need to know
I want to first point out that this was initially a passion project while also being time sensitive, meaning that for some code, especially in get_site.py, it either isn't perfect or uses a different scraping package than learned in class. playwright_get_site.py has some similar functions to get_site.py but is correct and also uses playwright instead of beutiful soup.

The main difficulty, as you may expect, was the web scraping. Every time I would run through the code I would have some minor issue or I would scrape something I didn't want. This required me to really think out of the box, especially when it came to removing specific links within articles and also image captions. There was a moment where I accidentally ran the code to bring new links into the cache after the election happened which I didn't want. I then needed to add a new part of the algorithm for both reading FOX and CBS articles that would ensure that the article was not written after the election date and time.

I also decided to implement a small amount of machine learning even though this wasn't something we learned in class. I thought it would be an interesting way to finish the project, especially showing which words are most influential in determining what site an article was written by.