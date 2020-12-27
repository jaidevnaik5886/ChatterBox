# ChatterBox
Chat Bot using Machine Learning in python

# Prerequisites
I have used Google colab for this mini project.
Install chatterbot and chatterbot_corpus libraries
```
pip install chatterbot
```

```
pip install chatterbot_corpus
```

# Code
1. Add the below imports.
2. Create an instance of ChatBot.
3. Add some sample messages to the queries array

```
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
```

Now you need to train your chatbot. You can do it using ListTrainer and passing the list of string(queries in our case) to it.

```
 listTrainer = ListTrainer(chatBot)
 listTrainer.train(queries)
```

Once you run the above code, you can comment queries and listtrainers code and proceed with communication with your chat bot.
To communicate you can use get_response() function. Below is a sample code for the same.

```
print(chatBot.get_response("What is your name?"))
```

Further you can train your chat bot using ChatterBotCorpusTrainer 
```
// corpusTrainer = ChatterBotCorpusTrainer(chatBot)
// corpusTrainer.train('chatterbot.corpus.english')
```

Thank you ! Happy coding.


