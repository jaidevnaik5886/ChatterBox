# ChatterBox
Chat Bot using Machine Learning in python


pip install chatterbot

pip install chatterbot_corpus

from chatterbot import ChatBot
from chatterbot.trainers import ListTrainer
from chatterbot.trainers import ChatterBotCorpusTrainer

chatBot = ChatBot(name='UM',
                  read_only=False,
                  logic_adapters= ['chatterbot.logic.MathematicalEvaluation','chatterbot.logic.BestMatch'])

 queries = ['Hi',
            'Hello',
           'How are you',
           'I m good, what about you?',
           'What is your name?',
           'United maharaja'
           ]

// listTrainer = ListTrainer(chatBot)
// listTrainer.train(queries)

// corpusTrainer = ChatterBotCorpusTrainer(chatBot)
// corpusTrainer.train('chatterbot.corpus.english')

print(chatBot.get_response("What is your name?"))
