This repo is dedicated to machine learning benchmarks for various otaku domains (visual novel, manga, light novel, etc)

At the moment, it only has resources for neural machine translation (NMT) but in the future I plan to add OCR and maybe audio benchmarks too.

For NMT benchmarking, I use BLEU score, specifically, [SacreBLEU](https://github.com/mjpost/sacrebleu "SacreBLEU") implementation.

The original Japanese file is located in each domain folder which is named "japaneseOriginal.txt"

After you translate that using your model, here are the steps to benchmark your model or replicate the result:

**FOR BENCHMARKING:**

1st, install SacreBLEU (Python>=3.6 only):

`pip install sacrebleu`

2nd, clone this repo then navigate to the domain folder of your choice, like visual novel for example.

`cd '.\Visual Novel\' `

3rd, use the command line in that folder and run calculateBleu.py

`python3  calculateBleu.py NameOfHumanTranslationFile.txt NameOfYourModelTranslationFile.txt`

Example:

`python3 calculateBleu.py humanTranslation.txt SugoiTranslatorOfflineV20.txt`


