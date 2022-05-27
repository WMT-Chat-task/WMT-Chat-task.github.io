---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Welcome to the WMT 2022 Chat Shared Task!
  Translating conversational text, in particular customer support chats, is an important and challenging application task for machine translation technology. This type of content has so far not been extensively explored in prior MT research, largely due to the lack of publicly available data sets. Prior related work has mostly focused on movie subtitles and European Parliament speeches.
  In contrast to the translation of the news stories, software manuals, biomedical text, etc. in which the text is carefully authored and well formated, chat conversations are less planned, more informal, and often ungrammatical.
  Further, such conversations are usually characterized by shorter and simpler sentences and contain more pronouns.
  In effect, the task of translating chat conversations can be regarded as a two-in-one task, modelling both dialogue and translation at the same time.
  Machine translation systems trained for chat conversations are expected to deal with the task's inherent challenges and characteristics, such as (among others):

- The importance of using extended context for translating the segments and modelling dialogue. E.g. Agreement and anaphora resolution requiring inter-sentential modelling:
      `I had a flight with AirLiberty for next Saturday from Lisbon to Abu Dhabi. Could you please change it to next Monday?`

- Robustness to noisy input. Chat text is usually noisier, containing misspelled words, wrong casings, incomplete sentences, etc.,
- Consistent and coherent translation throughout the entire conversation, and
- Modeling of all the speakers and language directions involved in the conversation, where each can be regarded as a different sub-domain (depending on the task).
  
The primary goal of this Chat shared task is to encourage participants to train and test models specific for bilingual chat conversations in a corpus composed of original bilingual costumer support conversations.
  
  This year we expanded the language pairs to en⇔de, en⇔fr, and en⇔pt_br.

  We encourage participants to use the **bilingual** context in the translation models submissions.
  
  Have questions or suggestions? Feel free to [Contact Us](mailto:wmt.metrics@gmail.com)!

## Chat Task Important Dates

|  | Date |
| ----------- | :-----------: |
| Validation set ready to download | TBA |
| Test set ready to download | TBA |
| Submission deadline for Chat task | 23-28th July, 2022 |
| Paper submission deadline to WMT | 7th September, 2022 |
| WMT Notification of acceptance | 9th October, 2022 |
| WMT Camera-ready deadline | 16th October, 2022 |
| Conference | 7th - 8th December, 2022 |

## Goals

The goals of chat translation shared task are to provide the common ground for:

- Studying the applicability of machine translation systems for translating conversational text;
- Investigating the impact of context in a conversation's translation;
- Studying the feasibility of an all-in-one multi-lingual system;

## Task Description

A critical challenge faced by international companies today is delivering customer support in several different languages. One solution to this challenge is centralizing support with English speaking agents and having a translation layer in the middle to translate from the customer's language into the agent's (English) and vice versa.

Although this year's task is not focused on dealing with noisy input nor measuring the model's robustness to such noise, the original data contains different types of noise including typos, wrong capitalization, among others; and while not required, the participants might want to take this aspect into consideration when developing their models.

## Data

The data used in this edition of the shared task is part of a unique corpus called MAIA corpus that is composed with genuin bilingual costumer support conversations.
### Subtracks:

1. [Zero-shot](./subtasks/zero-shot/): In this subtask participants have to develop machine translation systems without access to any in-domain training data.
2. [Low-resource](./subtasks/low-resource/): In this subtask participants have to develop machine translation systems with access to bilingual conversations without reference translations.

### Datasets

TBA


### Test Sets (Evaluation Data)

TBA


## Submission Format

TBA

## Evaluation
Similarly to the previous edition, the Systems' performance will be evaluated both automatically and manualy.
But, this year we will use [COMET](https://unbabel.github.io/COMET/html/index.html) as the automatic metric and MQM for the human evluation.
The official rankings will be based on the MQM scores at the document level, accounting for both directions.
The COMET scores, measured on the document level will be used as the secondary metric.


## Paper Describing Your MT Systems
Participants are invited to submit a short paper (4 to 6 pages) to WMT describing their MT system. Information on how to submit is available [here](https://www.statmt.org/wmt22/index.html").
Please note that the shared task submission description papers are non-archival, and it is not mandatory to submit a paper if you do not want to.





## Organization:

- Ana C. Farinha, Unbabel
- M. Amin Farajian, Unbabel
- Patrick Fernandes, Google and CMU and Instituto Superior Técnico
- José Souza, Unbabel
- João Alves, Unbabel
- António Lopes, Unbabel
- Helena Moniz, INESC-ID and Unbabel 
- André Martins, Unbabel and Instituto Superior Técnico

## Sponsors

<style>
	.column {
	  float: left;
	  padding: 20px;
	}
	
</style>
<div style="position: relative; width: 700px; height: 100px; min-height: 200px">    
    <div style="position: relative; bottom: 0px;">
	   <div class="column">
	     <img src="/public/css/unbabel.png" height=100px width=auto>
	   </div>
	</div>


