# 📚 Introduction

<img align="right" src="https://images.hamodia.com/hamod-uploads/2017/11/27160118/download.jpg" width="250">

<!--- ![calendar](https://print-a-calendar.com/printable-calendars/one-page-year-thumbnail.png) --->

This repository is to help all chess players utilize and work with [public chess profile data](http://ratings.fide.com/download_lists.phtml) provided by the `FIDE` organization (through December 2019). FIDE's website can be cumbersome to work with and has limited visuals about chess players. My hope is that this project helps users avoid the pain of using their website and provide interesting insights to the chess community.

The project is divided into 6 steps, which are outlined [here](https://github.com/AnujDahiya24/FIDE-Chess-Data#-lifecycle-of-data).

---

# 📈 Dashboard

To see ratings in real-time, I've created a dashboard to help chess players [here](https://anujdahiya24.shinyapps.io/apps/).

---

<img align="right" src = "https://cdn0.iconfinder.com/data/icons/Free-Icons-Shimmer-01-Creative-Freedom/256/folder.png" width="250">

# 🗺️ Where is the data?

The data is located in this [folder](https://github.com/AnujDahiya24/FIDE-Chess-Data/tree/master/Chess%20Scripts/Step%204%20-%20Cleaning/Cleaned%20csvs).

The folder contains over a hundred `.csv` files, from January 2001 to December 2019, that can be analyzed.

If you have suggestions on different data formats you'd like, please state them in [Issues](https://github.com/AnujDahiya24/FIDE/issues).

Other than that, feel free to use it as you see fit.


---


# 📊 Example data

An example of what the FIDE **Standard** Rating data looks like in December 2019: 

| ID_NUMBER | Name | Fed | Sex | Tit | WTit | OTit | FOA | Rating | Gms | K | Birthday | Flag |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 25121731 | A C J John | IND| M  |     |     |   |    | 1063 | 0  | 40 | 1987 | |
| 35077023 | A Chakravarthy | IND| M  |     |     |    |    | 1151 | 0  | 40 | 1986 | i  |
| 10207538 | A E M, Doshtagir | BAN| M  |     |     |    |    | 1840 | 0  | 40 | 1974 | i  |
| 10680810 | A hamed Ashraf, Abdallah  | EGY| M  |     |     |     |    | 1728 | 0  | 40 | 2001 |    |
| 5716365  | A Hamid, Harman | MAS| M  |     |     | NI            |    | 1325 | 0  | 40 | 1970 | i  |

---

# 🗄️ Metadata information

From the [FIDE Download Rating List page (old)](http://ratings.fide.com/download.phtml), we can understand each column a bit more:

<center>
 
| Column name | Meaning | Example |
| --- | :--- | --- |
| ID_NUMBER | a FIDE player's ID | 123456 |
| Name | a FIDE player's name | Carlsen, Magnus |
| Fed | a FIDE player's federation | USA |
| Sex | a FIDE player's sex | M, F |
| Tit | a FIDE player's title | GM, IM, FM, etc. |
| OTit | a FIDE player's other title(s)** | IA, FT, NI, etc.|
| FOA | a FIDE player's FOA*** titles | AGM, AIM, AFM, etc. |
| Rating | a FIDE player's rating | 2168 |
| Gms | # of games played in a month | 46 |
| K | a FIDE player's K-factor | 40 |
| Birthday | a FIDE player's birth year | 1993 |
| Flag | a FIDE player's level of activity | i, wi |

</center>

###### ** IA - International Arbiter,  FT - FIDE Trainer, NI - National Instructor
###### *** Fide Online Arena


---

# 🧬 Lifecycle of data

The lifecycle of the data is divided into 6 steps (below).

All 6 steps are done through R and Python.

You can click each step below for more information.

| <img src="http://shs-seniorproject.weebly.com/uploads/1/9/5/4/19541383/3steps-20140326042407248_orig.jpg" width="60"> | <img src="https://seohackercdn-seohacker.netdna-ssl.com/wp-content/uploads/2011/07/Link-Searching.jpg" width = "50"> |
| --- | --- |
|Step #1| [Download the data](https://github.com/AnujDahiya24/FIDE/tree/master/Chess%20Scripts/Step%201%20-%20Download)|
|Step #2| [Reformating the data](https://github.com/AnujDahiya24/FIDE/tree/master/Chess%20Scripts/Step%202%20-%20Reformat)|
|Step #3| [Scraping country data](https://github.com/AnujDahiya24/FIDE/tree/master/Chess%20Scripts/Step%203%20-%20FIDE%20Country%20Codes)|
|Step #4| [Cleaning the data](https://github.com/AnujDahiya24/FIDE-Chess-Data/tree/master/Chess%20Scripts/Step%204%20-%20Cleaning)|
|Step #5| [Visualizing the data](https://github.com/AnujDahiya24/FIDE-Chess-Data/tree/master/Chess%20Scripts/Step%205%20-%20Analysis)|
|Step #6| [Future Work](https://github.com/AnujDahiya24/FIDE-Chess-Data/tree/master/Chess%20Scripts/Step%206%20-%20Experimental%20work)|

---

# ♟️ Why did I do this?

I chose to work on this project because of several reasons:

- FIDE's publically available data is in an unorganized layout. There is no "download all datasets" button to acquire all of their data. FIDE also doesn't publically list data prior to February 2015 on the new download page when there is actually data going back as early as 2001. As a result, site visitors may find FIDE's website frustrating to work with and I wanted to help overcome their struggles.

- Chess players like to see visuals of themselves, friends, competitors, top players and players across various demographics. I wanted to provide these visuals.

- I wanted to improve my skills in 2 programming languages.

- I've always taken an interest in any data about chess that has not been extensively analyzed. My curiosity drives me.

---

# ✂️ Clone repo

You can clone this repo with the following:

```
$ git clone https://github.com/AnujDahiya24/FIDE-Chess-Data
```

---

# ❓ Questions?

Please post inquiries about the data in [Issues](https://github.com/AnujDahiya24/FIDE/issues).


1
-----------------------
# 📚 Introduction 

The first step has us downloading the profile player data (zipped text files) from [FIDE's website](http://ratings.fide.com/download_lists.phtml). Feel free to explore FIDE's [new] website. It seems as if data prior to 2015 is not being displayed anymore. Thankfully, all of the URLs still host the `.zip` files that we will download and are **not** broken.

If you want to: 

1. View the text files, see the `Data (all text files)` hyperlink below.
2. View the process of the data downloading, then see the `Tutorial` below
3. Run the script yourself, then you should download the `R-Markdown file` below and run it on your local machine.

# ⚡ Quick Links

- [Data (all text files)](https://github.com/AnujDahiya24/FIDE/tree/master/Chess%20Scripts/Step%201%20-%20Download/Downloaded%20files)
- [Tutorial](https://github.com/AnujDahiya24/FIDE/blob/master/Chess%20Scripts/Step%201%20-%20Download/Download%20Scripts/Download.pdf)
- [R-Markdown file](https://github.com/AnujDahiya24/FIDE/blob/master/Chess%20Scripts/Step%201%20-%20Download/Download%20Scripts/Download.Rmd)

# 🔄 Download the FIDE files

![Download](https://www.pngarts.com/files/2/Download-Button-Transparent-Background-PNG.png)

In order to download the player profile data, we will use something like the following snippet:

```
#R function that downloads FIDE data files and skips over non-existing URLs

download_function <- function(link, dest){
  if (!file.exists(dest)) {
    tryCatch({
      download.file(link, dest, method="auto", quiet = TRUE) 
    }, error=function(e){})
  }
} 

#Download all data files from URLs and direct them to a folder

mapply(download_function, url_vector, url_vect_destfile)
```

in order to download all files of interest and puts them into a destination folder. 

Please see the `Tutorial` and `R-Markdown` file for further reference.

# ⌚ Time Length

**Note:** The files may take some time to download depending on your internet connection speed.

# ❓ Questions?

Please post inquiries in [Issues](https://github.com/AnujDahiya24/FIDE/issues).


----------------------------
2

# 📚 Introduction

The second step has us modifying all of the text files from FIDE's website. In order to modify all of the files quickly, we will utilize parallel processing: It's a big time saver.

If you want to:

1. View the .csv files, see the `Data (all csv files)` hyperlink below.
2. View the process of the data downloading, then see the `Tutorial` below
3. Run the script yourself, then you should download the `R-Markdown file` below and run it on your local machine.

# ⚡ Quick Links

- [Data (all csv files)](https://github.com/AnujDahiya24/FIDE-Chess-Data/tree/master/Chess%20Scripts/Step%202%20-%20Reformat/Data%20csvs)
- [Tutorial](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%202%20-%20Reformat/Reformat%20Scripts/Reformat.pdf)
- [R-Markdown file](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%202%20-%20Reformat/Reformat%20Scripts/Reformat.Rmd)

# ⚠️ Issues

After downloading the files in Step 1, I wasn't able to import text files downloaded from [FIDE's data download page](http://ratings.fide.com/download_lists.phtml), into R. A typical `read.csv()` statement will not work because the data has no defined delimiter to parse columns on.  

For example, the earliest dataset on FIDE's website is from January 2001. Let's take a moment to look at the first few rows of the raw text file.

```
ID_NUMBER NAME                             TITLE COUNTRY JAN01 GAMES FLAG
 
 1701991  Aaberg, Anton                          SWE     2300    0   i   
 1401815  Aagaard, Jacob                   m     DEN     2374   18       
 1406248  Aage, Bjarke                           DEN     2063    0       
```

There are several issues with working with the data, but the most pressing one is that there is no clear delimiter to import the files on. A regular comma delimiter will not work because the text does not contain commas to separate the columns. Whitespace and tab delimiters won't work either.

One [github user](https://github.com/xdurana/fider/blob/master/R/zzz.R) has imported FIDE data via fixed widths. This works quite well for most, if not all of the data and I'll look into reading in the text files faster using this [stackoverflow post's](https://stackoverflow.com/questions/24715894/faster-way-to-read-fixed-width-files) benchmarking results.

When I first started working on this project, I didn't quite understand it required fixed-width functions such as `read_fwf()`. I was new to R and my main motivation was I wanted to learn R and Python in a creative setting.

There are several other issues with the rest of the text files (Text files run from January 2001 through December 2019). Just to name a few (shown with table visuals):

### Some have misspelled columns and ever-changing column names over time

```
ID NUMBER NAME                             TIT  Fed     JAN   GMs FLAG
 
 1701991  Aaberg, Anton                         SWE     2300    0   i       
 1401815  Aagaard, Jacob                   m    DEN     2374   18       
 1406248  Aage, Bjarke                          DEN     2063    0       
```  
- `ID NUMBER` is not `ID_NUMBER`, which is problematic for various programmatic reasons.
- `TIT` is different from `TITLE`
- `FED` is different from `Country`.
- `GMs` is different from `Games`
- `JAN` should be `JAN01`

### Some have their columns out of line or missing columns labels outright


```
ID_NUMBER   NAME                        TITLE   COUNTRYJAN01        FLAG
 
 1701991  Aaberg, Anton                          SWE     2300    0   i   
 1401815  Aagaard, Jacob                   m     DEN     2374   18       
 1406248  Aage, Bjarke                           DEN     2063    0       
```
- `NAME` is out of position
- `COUNTRY` and `JAN01` are one word instead of being separated into two
- `GAMES` is missing

### Some have blank & missing rows

```
ID_NUMBER NAME                             TITLE COUNTRY JAN01 GAMES FLAG
 
 1701991  Aaberg, Anton                          SWE     2300    0   i   

 1406248  Aage, Bjarke                           DEN     2063    0       
```
- The entire 2nd row is missing (Jacob Aagaard's information is missing).

### Some don’t even have column headers

```  
 1701991  Aaberg, Anton                          SWE     2300    0   i   
 1401815  Aagaard, Jacob                   m     DEN     2374   18       
 1406248  Aage, Bjarke                           DEN     2063    0       
```
- The column headers aren't even included in the data.

# 🧹 Reformat files

![](https://www.howtogeek.com/wp-content/uploads/blogs/files/2008/07/310.png)

As a result, our next step is to work through each file and transform them into a usable format. The approach I took was to insert delimiters at each index (based on the column line) where a space followed by a character occurred. For example, the data, after inserting `*` delimiters, would look something like this:

```
ID_NUMBER*NAME                            *TITLE*COUNTRY*JAN01*GAMES*FLAG
 
 1701991 *Aaberg, Anton                   *     *SWE    *2300 *  0  *i   
 1401815 *Aagaard, Jacob                  *m    *DEN    *2374 * 18  *    
 1406248 *Aage, Bjarke                    *     *DEN    *2063 *  0  *    
```
where we can clearly see `*` delmiters have been inserted at indexes where a whitespace occured and was one index before another character.

**Note:** Approximately ~14000 observations contain faulty Title and Flag/Activity information. These will be addressed in future iterations of the project.

The `multi_processing()` function below is the general wrapper that weaves everything together (importing, inserting delimiters, export reformatted data to `.csv` format.

```
#run All_files_fwrite() in parallel

multi_processing <- function(Year_num){
                    functions = ls(globalenv())
                    cl <- makeCluster(detectCores())
                    clusterExport(cl, functions)
                    registerDoParallel(cl)
                    foreach(i = Year_num,
                            .export = functions,
                            .packages = c("dplyr",
                                          "data.table",
                                          "Kmisc")) %dopar% {All_files_fwrite(i)}
                    stopCluster(cl)
                                      }
```
After this function is executed on every one of the `.txt` files, they will become usable `.csv` files.


# ⌚ Time Length

**Note:** The files (through December 2019) take some time to process and modify (5 minutes) on my computer, which runs on 8 cores.

# ❓ Questions?

Please post inquiries in [Issues](https://github.com/AnujDahiya24/FIDE/issues).

---------------------
3

# 📚 Introduction 

The thirds step has us scraping a table of FIDE Country Codes from this [URL](https://www.olimpbase.org/help/help41.html). This is a handy table to convert the `Country` column values over to more interpretable values in Step 4. In hindsight, I could have saved myself some time by looking at this [link](http://www.enpassant.dk/chess/palview/p3manual/p3flags.htm) within the URL I linked above.

If you want to: 

1. View the table, see the `Country Data` hyperlink below.
2. View/Run the program, see the scraping `Tutorial` below.

# ⚡ Quick Links

- [Country Data](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%203%20-%20FIDE%20Country%20Codes/Country%20Data/FIDE_codes.csv)
- [Tutorial](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%203%20-%20FIDE%20Country%20Codes/Country%20Scripts/FIDE%20country%20codes.ipynb)

# 🗺️ Country Table

![](https://geology.com/world/world-map-360.gif)

Python was used to scrape the table (BeautifulSoup is extremely useful). You can see what the truncated table looks like below.

| Code | Country |
|--- | ---|
| AFG | Afghanistan |
| ALB | Albania |
| ALG | Algeria |

# 🗄️ Metadata Information

| Code | 3 letter country code |
|--- | ---|
| Country | Country name |


# ⌚ Time Length

This takes less than half of a second to run.

# ❓ Questions?

Please post inquiries in [Issues](https://github.com/AnujDahiya24/FIDE/issues).

--------------------------------

4

# 📚 Introduction

If you want to: 

1. View the .csv files, see the `Cleaned csvs` hyperlink below.
2. View the process of the data downloading, then see the `Tutorial` below
3. Run the script yourself, then you should download the `R-Markdown file` below and run it on your local machine.

# ⚡ Quick Links

- [Cleaned csvs](https://github.com/AnujDahiya24/FIDE-Chess-Data/tree/master/Chess%20Scripts/Step%204%20-%20Cleaning/Cleaned%20csvs)
- [Tutorial](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%204%20-%20Cleaning/Cleaning%20scripts/Cleaning.pdf)
- [R-Markdown file](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%204%20-%20Cleaning/Cleaning%20scripts/Cleaning.Rmd)

---

# 🧹 Cleaning files

![](https://miro.medium.com/max/500/1*yWFQiGjlgHUVYeh4ELELyw.jpeg)


To clean the data, we will at some point need to modify each file's column names and values using something like the following in R:

```
#Iterate over each data.frame in list
for(i in 1:length(FIDE)){

#Rename columns in each dataset
  colnames(FIDE[[i]])[grepl("Name|NAME|name", colnames(FIDE[[i]]))] <- "Name"
  ...... more column editing ......
  ...... more column editing ......
  ...... more column editing ......
  colnames(FIDE[[i]])[grepl("OTit", colnames(FIDE[[i]]))] <- "Other_Titles"
  
 #Clean each data.frame
  FIDE[[i]] <- FIDE[[i]] %>%
               mutate(Date = as.POSIXct(names(FIDE)[i], format="%Y-%m-%d"),
                      Date_numeric = year(Date)+yday(Date)/366,
                      Rating = as.numeric(Rating),
                      Title= c(new, Title)[match(Title, c(old, Title))],
                      Country = c(codes$Country, Country)[match(Country, c(codes$Code, Country))],
                      Country = c(countries, Country)[match(Country, c(country_codes, Country))])%>%
                      filter(!Country %in% c("Fed", "Col"))%>%
                      select(-one_of("V1"))
                      
  #Write to new file
  fwrite(FIDE[[i]] , file = paste(dest, files[i], sep = ""), sep = "*")
  
}
```
I'll look to parallelize this for loop to save time moving forward. 

**Note::** The `Age_Birthday` needs a considerable amount of work. Many of the dates have differing formats, so I will need to write a function that will reformat the data.

# ⌚ Time Length

Note: The files take a few minutes to process the data and export it to the proper destination.

---

# ❓ Questions?

Please post inquiries about the data in [Issues](https://github.com/AnujDahiya24/FIDE/issues).

-----------------------
5
# 📚 Introduction

Welcome to the analytical portion of this repository. There are several topics explored here, but countless more to explore over time.

A few examples of visuals in the `Tutorial` file below are:

- Total player counts over time
- Total players gained/lost over time
- Rating stability graphs
- Total player gained/lost over time by country (Countries with extreme values)
- Total titled player counts over time
- Total titled player counts by country (Latest month)
- Strongest countries by age group
- Age vs Rating by title (Latest month)

If you want to:
1. View the process of the data visualization, then see the `Tutorial` below
2. Run the script yourself, then you should download the `R-Markdown file` below and run it on your local machine.

# ⚡ Quick Links

- [Tutorial](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%205%20-%20Analysis/Analysis%20%26%20Visuals/Analysis.pdf)
- [R-Markdown file](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%205%20-%20Analysis/Analysis%20%26%20Visuals/Analysis.Rmd)

---

# Visuals

Below is an experimental visualization I'm working on improving. It is **not** included in the Tutorial file: it is in the `Experiments` folder in `Step 6`.

#### FIDE player (Active) rating distribution of Males & Females over time.

![](https://github.com/AnujDahiya24/FIDE-Chess-Data/blob/master/Chess%20Scripts/Step%206%20-%20Experimental%20work/Experiments/Men_women_gif.gif)

I find this graph to be interesting because it shows a few strange trends:

- The graphs look like play-dough that has been slowly compressed over time.
- There were no players rated below 2200 in many of the early datasets provided by FIDE.
- Around 2014, both the male and female distributions looked fairly Gaussian in their shape
- Since 2014, FIDE's rating floor of 1000 has prevented players from naturally falling below the floor. I will look to explore the differences between the male and female distributions (both are heavily right-skewed, but the female distribution is even more so) moving forward. There's an interesting sociological phenomenon present here that has not been vocalized in public yet.

# ⌚ Time Length

Note: The `Analysis.pdf` file take several minutes to knit because of functions like `rbindlist()` that combine all of the datasets together.

---

# ❓ Questions?

Please post inquiries about the data in [Issues](https://github.com/AnujDahiya24/FIDE/issues).

--------------------------

mudei nome dos arquivos

rename APR01.csv 2001-APR.csv
rename APR02.csv 2002-APR.csv
rename APR03.csv 2003-APR.csv
rename APR04.csv 2004-APR.csv
rename APR05.csv 2005-APR.csv
rename APR06.csv 2006-APR.csv
rename APR07.csv 2007-APR.csv
rename APR08.csv 2008-APR.csv
rename APR09.csv 2009-APR.csv
rename APR13.csv 2013-APR.csv
rename APR14.csv 2014-APR.csv
rename APR15.csv 2015-APR.csv
rename APR16.csv 2016-APR.csv
rename APR17.csv 2017-APR.csv
rename APR18.csv 2018-APR.csv
rename APR19.csv 2019-APR.csv
rename AUG12.csv 2012-AUG.csv
rename AUG13.csv 2013-AUG.csv
rename AUG14.csv 2014-AUG.csv
rename AUG15.csv 2015-AUG.csv
rename AUG16.csv 2016-AUG.csv
rename AUG17.csv 2017-AUG.csv
rename AUG18.csv 2018-AUG.csv
rename AUG19.csv 2019-AUG.csv
rename DEC12.csv 2012-DEC.csv
rename DEC13.csv 2013-DEC.csv
rename DEC14.csv 2014-DEC.csv
rename DEC15.csv 2015-DEC.csv
rename DEC16.csv 2016-DEC.csv
rename DEC17.csv 2017-DEC.csv
rename DEC18.csv 2018-DEC.csv
rename DEC19.csv 2019-DEC.csv
rename FEB13.csv 2013-FEB.csv
rename FEB14.csv 2014-FEB.csv
rename FEB15.csv 2015-FEB.csv
rename FEB16.csv 2016-FEB.csv
rename FEB17.csv 2017-FEB.csv
rename FEB18.csv 2018-FEB.csv
rename FEB19.csv 2019-FEB.csv
rename JAN01.csv 2001-JAN.csv
rename JAN02.csv 2002-JAN.csv
rename JAN03.csv 2003-JAN.csv
rename JAN04.csv 2004-JAN.csv
rename JAN05.csv 2005-JAN.csv
rename JAN06.csv 2006-JAN.csv
rename JAN07.csv 2007-JAN.csv
rename JAN08.csv 2008-JAN.csv
rename JAN09.csv 2009-JAN.csv
rename JAN10.csv 2010-JAN.csv
rename JAN11.csv 2011-JAN.csv
rename JAN12.csv 2012-JAN.csv
rename JAN13.csv 2013-JAN.csv
rename JAN14.csv 2014-JAN.csv
rename JAN15.csv 2015-JAN.csv
rename JAN16.csv 2016-JAN.csv
rename JAN17.csv 2017-JAN.csv
rename JAN18.csv 2018-JAN.csv
rename JAN19.csv 2019-JAN.csv
rename JUL01.csv 2001-JUL.csv
rename JUL02.csv 2002-JUL.csv
rename JUL03.csv 2003-JUL.csv
rename JUL04.csv 2004-JUL.csv
rename JUL05.csv 2005-JUL.csv
rename JUL06.csv 2006-JUL.csv
rename JUL07.csv 2007-JUL.csv
rename JUL08.csv 2008-JUL.csv
rename JUL09.csv 2009-JUL.csv
rename JUL10.csv 2010-JUL.csv
rename JUL11.csv 2011-JUL.csv
rename JUL12.csv 2012-JUL.csv
rename JUL13.csv 2013-JUL.csv
rename JUL14.csv 2014-JUL.csv
rename JUL15.csv 2015-JUL.csv
rename JUL16.csv 2016-JUL.csv
rename JUL17.csv 2017-JUL.csv
rename JUL18.csv 2018-JUL.csv
rename JUL19.csv 2019-JUL.csv
rename JUN13.csv 2013-JUN.csv
rename JUN14.csv 2014-JUN.csv
rename JUN15.csv 2015-JUN.csv
rename JUN16.csv 2016-JUN.csv
rename JUN17.csv 2017-JUN.csv
rename JUN18.csv 2018-JUN.csv
rename JUN19.csv 2019-JUN.csv
rename MAR10.csv 2010-MAR.csv
rename MAR11.csv 2011-MAR.csv
rename MAR12.csv 2012-MAR.csv
rename MAR13.csv 2013-MAR.csv
rename MAR14.csv 2014-MAR.csv
rename MAR15.csv 2015-MAR.csv
rename MAR16.csv 2016-MAR.csv
rename MAR17.csv 2017-MAR.csv
rename MAR18.csv 2018-MAR.csv
rename MAR19.csv 2019-MAR.csv
rename MAY10.csv 2010-MAY.csv
rename MAY11.csv 2011-MAY.csv
rename MAY12.csv 2012-MAY.csv
rename MAY13.csv 2013-MAY.csv
rename MAY14.csv 2014-MAY.csv
rename MAY15.csv 2015-MAY.csv
rename MAY16.csv 2016-MAY.csv
rename MAY17.csv 2017-MAY.csv
rename MAY18.csv 2018-MAY.csv
rename MAY19.csv 2019-MAY.csv
rename NOV09.csv 2009-NOV.csv
rename NOV10.csv 2010-NOV.csv
rename NOV11.csv 2011-NOV.csv
rename NOV12.csv 2012-NOV.csv
rename NOV13.csv 2013-NOV.csv
rename NOV14.csv 2014-NOV.csv
rename NOV15.csv 2015-NOV.csv
rename NOV16.csv 2016-NOV.csv
rename NOV17.csv 2017-NOV.csv
rename NOV18.csv 2018-NOV.csv
rename NOV19.csv 2019-NOV.csv
rename OCT01.csv 2001-OCT.csv
rename OCT02.csv 2002-OCT.csv
rename OCT03.csv 2003-OCT.csv
rename OCT04.csv 2004-OCT.csv
rename OCT05.csv 2005-OCT.csv
rename OCT06.csv 2006-OCT.csv
rename OCT07.csv 2007-OCT.csv
rename OCT08.csv 2008-OCT.csv
rename OCT12.csv 2012-OCT.csv
rename OCT13.csv 2013-OCT.csv
rename OCT14.csv 2014-OCT.csv
rename OCT15.csv 2015-OCT.csv
rename OCT16.csv 2016-OCT.csv
rename OCT17.csv 2017-OCT.csv
rename OCT18.csv 2018-OCT.csv
rename OCT19.csv 2019-OCT.csv
rename SEP09.csv 2009-SEP.csv
rename SEP10.csv 2010-SEP.csv
rename SEP11.csv 2011-SEP.csv
rename SEP12.csv 2012-SEP.csv
rename SEP13.csv 2013-SEP.csv
rename SEP14.csv 2014-SEP.csv
rename SEP15.csv 2015-SEP.csv
rename SEP16.csv 2016-SEP.csv
rename SEP17.csv 2017-SEP.csv
rename SEP18.csv 2018-SEP.csv
rename SEP19.csv 2019-SEP.csv