# Giffer

This is a proof of concept for an API for adding text to gif images.  Think of it as a mix between giphy and meme generator.

#### Technology stack
- Python 2.7
- Flask w/ Flask-API for a pretty front end
- moviepy

## Dependencies
- Python
- Pip
- Virtualenv (pip install virtualenv)

## Installation
```shell
git clone https://github.com/m3brown/giffer
cd giffer
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

## Using the app
- After running `python app.py` you should be able to reach the site at localhost:5000
- Create a gif by submitting a POST with JSON data.  At the least, you'll need `text` along with one of `gif` or `search`
  - text: the text to put on the gif
  - gif: URL of the gif image to use
  - search: the search phrase to query from giphy
  
For example:
```json
{"text": "time for work", "gif": "http://25.media.tumblr.com/tumblr_m810e8Cbd41ql4mgjo1_500.gif"}
```
```json
{"text": "hey guys", "search": "elf wave"}
```
