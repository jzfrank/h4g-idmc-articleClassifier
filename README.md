# Article Classifcation Design

Given an article or its url (then scrape its content). We are to 

1. Fileter out non-relevant article -> if it is disaster or violence

2. Tag documents based on themes -> is it a disaster or violence? If yes, which type? 


To solve this, we could consider three approaches: 

1. Bag of words: using a list of keywords to filter out / classification 
2. Use transformers / pretrained models 
3. Train model based on "Figures-Helix-H4G-IDMC.xlsx". (train from scratch / transfer learning)



## Transformers: 
### Disaster 
classfies if a twitter has disaster 

https://huggingface.co/sacculifer/dimbat_disaster_distilbert?text=IndiaToday+-+Over+400%2C000+people+in+nearly+1%2C000+villages+evacuated+in+6+border+districts+in+Punjab


Identifies which type of disaster it is (10 types: disease, earthquake, flood, hurricane & tornado, wildfire, industrial accident, societal crime, transportation accident, meteor crash, haze)

https://huggingface.co/sacculifer/dimbat_disaster_type_distilbert?text=Flood+-+October+-+Dangkao+District+-+74+families+displaced

### Violence / Conflict 

Not really useful pretrained models are found. 

https://github.com/zubu007/ResNet-LSTM-model-for-Violence-Detection 

Or just use bagOfWord: ["evacuate", "displaced", "flee"]


## Other resources 

For dealing with multiple languages:
- Detecting which language it is: https://huggingface.co/papluca/xlm-roberta-base-language-detection?text=Guten+nacht
- Translate e.g. From French to English: https://huggingface.co/Helsinki-NLP/opus-mt-fr-en?text=Mon+nom+est+Wolfgang+et+je+vis+%C3%A0+Berlin 
