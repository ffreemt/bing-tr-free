# bing-tr-free

Youdao translate for free -- local cache and throttling (averag 1.5 calls/s, first 1000 calls exempted). Let's hope it lasts.
### Limitation
Maximum of 50 characters per query -- you'll have to do some processing if you want to handle longer text.

### Installation

```pip install bing-tr-free```

or

* Install (pip or whatever) necessary requirements, e.g. ```
pip install requests fuzzywuzzy pytest jmespath coloredlogs``` or ```
pip install -r requirements.txt```
* Drop the file bing_tr.py in any folder in your PYTHONPATH (check with import sys; print(sys.path)
* or clone the repo (e.g., ```git clone https://github.com/ffreemt/bing-tr-free.git``` or download https://github.com/ffreemt/bing-tr-free/archive/master.zip and unzip) and change to the bing-tr-free folder and do a ```
python setup.py develop```

### Usage

```
from bing_tr import bing_tr
print(bing_tr('hello world'))  # ->'世界您好'
print(bing_tr('hello world', to_lang='de'))  # ->'Hallo Welt'
print(bing_tr('hello world', to_lang='fr'))  # ->'Salut tout le monde'
print(bing_tr('hello world', to_lang='ja'))  # ->'ハローワールド'
```

Consult the official website for language pairs supported.

### Acknowledgments

* Thanks to everyone whose code was used