# KBKAIST_Chatbot
KBKAIST chatbot from ParlAI

This repository is slightly modified version of ParlAI chitchat example.

See https://github.com/facebookresearch/ParlAI


1) clone this project in server

2) python setup.py develop (make sure python version is newer than 3.5)

3) copy data 
from brain21:/data3/kenkim/ParlAI/data/OpenSubtitles/{train.txt, valid.txt, test.txt}
to new_server:/path/to/ParlAI/data/OpenSubtitles/{train.txt, valid.txt, test.txt}
  
4) Train example

python examples/train_model.py -m seq2seq -t opensubtitles -mf data/OpenSubtitles/model_512 -hs 512 -bs 64  --gpu 0 -lr 0.001

python examples/train_model.py -m seq2seq -t opensubtitles -mf data/OpenSubtitles/model_2048 -hs 2048 -bs 64 --gpu 1 -lr 0.001

5) Interactive example

 python examples/interactive.py -t opensubtitles -m seq2seq -mf data/OpenSubtitles/model_512 --dict-file data/OpenSubtitles/model_512.dict -hs 512 --gpu 0



