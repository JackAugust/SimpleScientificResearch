# SimpleScientificResearch
## This is for CS Postgraduates in China who want to :
- Identify popular research directions
- Determine the current status of a hot research topic
- Determine the high-quality papers corresponding to the research direction
- Select the appropriate high-quality journal/conference to complete the submission

## The Guidance Blogs
- [Result analysis](https://blog.csdn.net/jack_zj123/article/details/127048484)
- [Complete journal article crawling](https://blog.csdn.net/jack_zj123/article/details/127060560)
- [Complete conference paper crawling](https://blog.csdn.net/jack_zj123/article/details/127061539)

## Description
### Research direction
The current results are analyzed for the **blockchain**

### Timeframe
Journal until September 19, 2022, conference from 2006 to September 22, 2022

### Result
`TheFinallyResult.xlsx` is the crawling result based on the `blockchain`
You can get more in-depth information by `Ctrl+F` and `Enter` your words to search
You can `Click` on the title of interest to jump to `the corresponding page` to read the real paper content

## Instructions for use

### Environment dependent
#### Python 3.7
`pip install lxml`
```python
import requests
import re
from openpyxl import load_workbook
import json
from bs4 import BeautifulSoup
```
#### Excel 2009+

### Installation
#### Step 1
` run GetJourInfo.py`
#### Step 2 
` run AddJCR2JourInfo.py`
#### Step 3
If you want to get the   `blockchain` paper, just do :
` run GetAllPaperText-Plus.py`
else, you should to modify the `GetAllPaperText-Plus.py`:
##### 01 should be modified
```python
def BlockFind(kw, info):
    if re.findall(kw, info, re.I):
        return info
```
##### 02 Must be modified
```python
KW = "blockchain" ## you should to modify this to your resarch
```
##### 03 Save and run
` run GetAllPaperText-Plus.py`

#### Step 4
If you want to get the   `blockchain` paper , just do :
` run GetAllMeetPaper.py`
else, you should to modify the `GetAllMeetPaper.py`:
##### 01 should be modified
```python
def BlockFind(kw, info):
    if re.findall(kw, info, re.I):
        return info
```
##### 02 Must be modified
```python
KW = "blockchain" ## you should to modify this to your resarch
```
##### 03 Save and run
` run GetAllMeetPaper.py`

#### Step 5
You can get the infomation you want in the file : `JournalInfo.xlsx`
and follow the  `Result` part

## END