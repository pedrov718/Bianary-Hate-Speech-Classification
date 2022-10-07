# Hate Speech/Profanity Detection Project

### The Problem:

![alt text](https://github.com/pedrov718/Bianary-Hate-Speech-Classification/blob/main/figures/hate_speech_no_stops_word_bubble.png)


Social media has become a vital part of our modern society, from political elections to fashion and education,
social media like Twitter, Reddit, Instagram, and Meta have truly become all-encompassing. However for many of the great benefits that social media
provides there are some terrible consequences. Cyberbullying, racism/hate speech, and profanity run rampant.
Social media has become like the wild wild west, with law-less entities wantonly posting content without concern or
care for others.

### The Data:

Using a dataset collected by UC Berkley researcher I was able to get a human labled dataset with 135553 text samples, each labled as hate speech or not hatespeech. More information about the dataset and methods to how to download it can be found here: https://huggingface.co/datasets/ucberkeley-dlab/measuring-hate-speech

![10_most_frequnet_words_withstops](https://user-images.githubusercontent.com/82776178/194624370-c27c1171-6d0a-4146-8922-04e8d6253a4a.png)

![alt text](https://github.com/pedrov718/Bianary-Hate-Speech-Classification/blob/2ac81607cdcffda21c9dd36c9f40aa63f179e0b9/figures/10_most_frequnet_words_nostops.png)

![percent_hate](https://user-images.githubusercontent.com/82776178/194624408-6aa3ef46-db8b-4f5f-b312-04dd8303c7ea.png)

### The Solution:
#### Keep safe spaces safe!

As much as we would like to prevent the future of George Orwell's big brother from ever becoming reality we must accept
the fact that freedom of speech/expression can lead to dark places. Thus, technologies must be created to limit
hate speech, cyberbullying, and harassment in spaces where it does not belong. Training a machine
learning algorithm I was able to detect the presence of hate speech and profanity in tweets containing text.
Leveraging the power of Natural Langauge Processing (NLP) I was able to train a model to detect hate speech with an
accuracy of 87.65%. But accuracy score was not the metric that I was most concerned with. I wanted to limit hatespeech in places where it didnt belong, thus I wanted to catch as much hate speech as posssible. So by hyperparamter tuning my model with recall in mind I was able to get a recall score of 88.59%. 

![Hate speech classification LinearSVM Slide](https://user-images.githubusercontent.com/82776178/194624074-e66b3dde-44e1-4dc4-bcfb-1b55e5814961.png)

Some of my most important features for my model were the following words: 

![top20_feature_importance_bargraph](https://user-images.githubusercontent.com/82776178/194624429-0743c1a6-152c-4541-b083-2fa78f697278.png)

![top20_feature_importance](https://user-images.githubusercontent.com/82776178/194624166-f2159849-72fa-4967-af20-ef2a6e1d01cf.png)

For more information you can view my presentation here: https://docs.google.com/presentation/d/16TsQ3jTNRKx3UbBn3JQ7t2YNRoeXbVfK08hsS6EBVuQ/edit?usp=sharing

### The implementation:

Monitor social medias/online forums and censor hate speech and profanity in real-time. Adjust custom thresholds
depending on your use case. For example, allowing profanity to exist in adult oriented content and limiting 
it altogether in spaces primarily used by children. 

### Future Work

Create a Reddit/twitch bot that can censor hate speech in real-time. Replace hate-speech/ profanity with an
auto-generated summary of the text (to convey meaning without negative sentiment)


