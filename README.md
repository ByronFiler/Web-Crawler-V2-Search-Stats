# Web-Crawler-V2-Search-Stats
My web crawler remade in 2018, with a few new additional features.

# Information
In 2016 I made a basic web crawler, found <a href="https://github.com/ByronFiler/Web-Crawler"> here </a>, I now remade this to be more efficent and have a few more features, listed below with some more information.

# Features
- Map All Connected Pages from any source page.
- Basic search feature for a keyword, enter a keyword and will show all relevant page(s) that have been found and cached.
- Smart page caching, stores all readable words from a html page and saves them in a text file, the link is then stored in the file name and base58 encoded so that URLs can always be saved.
- Quick Statistics, option to in the background quite simply view statistics, such as time used, data used (estimated) and links processed.
- Constant saving so if it exits at anytime it will be able to be quickly restarted.

# Prequisites

### Beautiful Soup
`pip3 install BeautifulSoup4`

### Base58
`pip3 install Base58`

### Glob 
`pip3 install glob`


# Files & Directories Explination
### /json/
Stores JSON Files.

### /cache/
Cached html files after they have been downloaded, used for searching, the file names are base58 encoded for the full urls.

### links.json

#### Example Format
`{
    "processed": {
        "0": "http://filler.com/"
    },
    "todo": {
        "0": "http://www.bbc.co.uk/news"
    }
}`

Saves all links that have been done so they won't be done again, and the queue of links to be processed.

### links.json

#### Example Format
`{
    "data": 0,
    "processed": 0,
    "time": 0
}`

Saves all data related permanent statistics.

# Future Plans
- Directory Tree Mapping, possibly with matplotlib
- Graphing Resource Usage
- Links Found
- Stats on interconnected links
- Improving the search by listing off more options
