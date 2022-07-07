---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# Welcome to the WMT 2022 Chat Shared Task!

## Updates

### July 7th, 2022

``❗`` Baselines scores on devsets are now available in the section **Baseline Scores on DevSets** below and scripts to reproduce them can be found [here](https://github.com/WMT-Chat-task/data-and-baselines). 


### June 30th, 2022

``❗`` Please also register to the chat-shared-task [google-group](https://groups.google.com/g/wmt-chat-task) in order to be able to receive immediate updates announcements and ask us questions! 

``❗`` Baselines' scores on devsets will be available soon! 

``❗`` List of additional permited training data are updated in the Datasets section.

<br />

## Overview

<p class="message">  
  Translating conversational text, in particular customer support chats, is an important and challenging application for machine translation technology. This type of content has so far not been extensively explored in prior MT research, largely due to the lack of publicly available data sets. Prior related work has mostly focused on movie subtitles and European Parliament speeches.<br />

  In contrast to the translation of the news stories, software manuals, biomedical text, etc. in which the text is carefully authored and well formated, chat conversations are less planned, more informal, and often ungrammatical.
  Further, such conversations are usually characterized by shorter and simpler sentences and contain more pronouns.<br />
  In effect, the task of translating chat conversations can be regarded as a two-in-one task, modelling both dialogue and translation at the same time.<br />
</p>

Machine translation systems trained for chat conversations are expected to deal with the task's inherent challenges and characteristics, such as (among others):
- The importance of using extended context for translating the segments and modelling dialogue. E.g. Agreement and anaphora resolution requiring inter-sentential modelling:
  - `I had a flight with AirLiberty for next Saturday from Lisbon to Abu Dhabi. Could you please change it to next Monday?`
- Robustness to noisy input. Chat text is usually noisier, containing misspelled words, wrong casings, incomplete sentences, etc.,
- Consistent and coherent translation throughout the entire conversation, and
- Modeling of all the speakers and language directions involved in the conversation, where each can be regarded as a different sub-domain (depending on the task).

The primary goal of this Chat shared task is to encourage participants to train and test models specific for bilingual chat conversations in a corpus composed of original bilingual costumer support conversations.

This year we expanded the language pairs to en⇔de, en⇔fr, and en⇔pt_br.

We encourage participants to use the **bilingual context** in the translation models submissions.<br />

Have questions or suggestions? Feel free to <a href="mailto:wmt.chat.task@gmail.com">Contact Us</a>!

## Chat Task Important Dates
<style scoped>
table {
  font-size: 14px;
}
</style>

|  | Date |
| ----------- | :-----------: |
| Validation set ready to download | ~~15th~~ 22nd June |
| Test set ready to download | 23rd July, 2022 |
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

## Data

The data used in this shared task is part of a unique corpus called MAIA corpus that is composed with genuin bilingual costumer support conversations.
One of the main challenges of this domain is the lack of real bilingual training data available.
In order to make this shared task as close as possible to the real-world settings, this year, we release only the dev and test sets. So, please note that there will be no training data for this edition and the participants are expected to use only the dev sets (bilingual and monolingual) to train and fine-tune their MT systems.

Please note, that all the data released for the WMT22 Chat Translation task is under the license of [CC-BY-NC-4.0](https://creativecommons.org/licenses/by-nc/4.0)
 and can be freely used for research purposes only. Please note that, as the license states, no commercial uses are permitted for this corpus. We just ask that you cite the WMT22 Chat Translation Task overview paper. Any other use is not permitted unless previous written authorization is given by Unbabel.

### Tracks:

1. **Zero-shot**: In this task participants have to develop machine translation systems without access to any in-domain training data.
2. **Low-resource**: In this task participants have to develop machine translation systems with access to bilingual conversations without reference translations.
   

## Datasets

The Dev sets (both bilingual and monolingual) of all the language pairs are available in the [github](https://github.com/chat-task/wmt-chat-task/tree/main/data) repository.
The files contain the bilingual conversations by a customer and an agent in their original language.
Here is an example of such a conversation:


| **source_language** | **mt_language** | **source_segment**                                                                                                                                                       | **pe_segment**                                                                                                                                                                                           | translation_direction |
|-----------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| fr              | en          | Bonjour je ne peut pas utiliser mes jetons accumuler pour acheter un livre audio                                                                                         | Hello, I can't use the tokens I accumulated to buy an audio book.                                                                                                                                 | customer              |
| en              | fr          | Thank you for contacting #PRS_ORG#, it was my pleasure to assist you today.                                                                                              | Merci d'avoir contacté #PRS_ORG#, ce fut un plaisir de vous aider aujourd'hui.                                                                                                                    | agent                 |
| en              | fr          | I hope you have an excellent day.                                                                                                                                        | J'espère que vous passez une excellente journée.                                                                                                                                                  | agent                 |
| en              | fr          | Please allow me a moment to verify the account.                                                                                                                          | Veuillez m'accorder un moment pour vérifier le compte.                                                                                                                                            | agent                 |
| en              | fr          | I am sorry that you are experiencing this issue, I will do my best to assist you.                                                                                        | Je suis désolé que vous rencontriez ce problème, je ferai de mon mieux pour vous aider.                                                                                                           | agent                 |
| en              | fr          | What is the error message or problem you are getting when trying to use your audio book credits?                                                                         | Quel est le message d'erreur ou le problème que vous rencontrez lorsque vous essayez d'utiliser vos crédits de livres audio ?                                                                     | agent                 |
| fr              | en          | Je ne peu pas effectuer l achat je peu juste le faire avec #PRS_ORG# ou par carte                                                                                        | I am unable to make the purchase, I can only do it with #PRS_ORG# or by card.                                                                                                                     | customer              |
| en              | fr          | Are your credit s from an #PRS_ORG# subscription?                                                                                                                        | Vos crédits proviennent-ils d'un abonnement #PRS_ORG# ?                                                                                                                                           | agent                 |
| fr              | en          | Oui                                                                                                                                                                      | Yes.                                                                                                                                                                                              | customer              |
| en              | fr          | I understand, at the moment we no longer work with #PRS_ORG#, they are not partnered with us anymore, probably that is the error, please let me confirm this information | Je comprends, pour le moment nous ne travaillons plus avec #PRS_ORG#, ils ne sont plus en partenariat avec nous, c'est probablement la raison de l'erreur, laissez-moi confirmer ces informations | agent                 |
| fr              | en          | Mais ça me met que j ai 13 jetons à utiliser                                                                                                                             | But it shows that I have 13 tokens.                                                                                                                                                               | customer              |
| en              | fr          | I am confirming the information with my team, thanks for your patience                                                                                                   | Je confirme les informations avec mon équipe, merci pour votre patience                                                                                                                           | agent                 |

<br /><br />
As you can see, the source sentences (i.e. *source_segment*) are in the original language of the speaker, i.e. French in the case of *customer* and English in the case of *agent*. And the translations (i.e. *pe_segment*).
Moreover, since the data is anonymised, we have the entities replaced by the following special tokens:

| **Token**         | **Description**                          |
|-------------------|------------------------------------------|
| #NAME#            | Person’s names                           |
| #PRS_ORG#         | Products and Services, and Organizations |
| #ADDRESS#         | Address                                  |
| #EMAIL#           | E-mail address                           |
| #IP#              | IP Address                               |
| #PASSWORD#        | Password                                 |
| #PHONENUMBER#     | Phone number                             |
| #CREDITCARD#      | Credit card number                       |
| #URL#             | URL Address                              |
| #IBAN#            | IBAN number                              |
| #NUMBER#          | Any number (all digits)                  |
| #ALPHANUMERIC_ID# | Any alphanumeric ID                      |

<br />

<span style="color:red">**Note**</span> that for training and validation purposes you can use the training data of the general task (including the data of the previous editions), the data of the other tracks (eg. biomedical) if you find them useful for this task, and the other corpora (either parallel or monolingual) that are publicly available for the research purposes, like most of the corpora available on OPUS, as well as the data of the previous edition of the Chat Translation Task.

<br />

## Baseline Scores on DevSets

We provide two different baselines: one without any context and another with context (using the two previous iterations for the corresponding direction).

### Baseline without context:

| Direction | Lang  | BLEU  | chrF  | COMET  | TER   |
|-----------|-------|-------|-------|--------|-------|
| agent     | de    | 35.24 | 57.17 | 0.4168 | 55.70 |
| agent     | fr    | 54.14 | 69.47 | 0.7984 | 37.95 |
| agent     | pt_br | 50.38 | 68.84 | 0.8645 | 40.99 |
| customer  | de    | 45.98 | 60.81 | 0.5426 | 51.21 |
| customer  | fr    | 46.51 | 62.29 | 0.6382 | 50.12 |
| customer  | pt_br | 44.71 | 59.95 | 0.5851 | 53.78 |

### Baseline with context:

| Direction | Lang  | BLEU  | chrF  | COMET  | TER   |
|-----------|-------|-------|-------|--------|-------|
| agent     | de    | 33.89 | 55.96 | 0.3811 | 57.30 |
| agent     | fr    | 53.58 | 68.81 | 0.7978 | 41.50 |
| agent     | pt_br | 49.94 | 67.95 | 0.9029 | 40.89 |
| customer  | de    | 47.11 | 62.06 | 0.6163 | 46.94 |
| customer  | fr    | 48.05 | 63.61 | 0.6834 | 47.78 |
| customer  | pt_br | 47.24 | 62.31 | 0.6437 | 47.91 |

Scripts to reproduce scores are available [here](https://github.com/WMT-Chat-task/data-and-baselines).

<br />

## Test Sets (Evaluation Data)

Test Sets will be available on the 23rd of July.

### Submission Format

TBA

## Evaluation
Similarly to the previous edition, the Systems' performance will be evaluated both automatically and manualy.
But, this year we will use [COMET](https://unbabel.github.io/COMET/html/index.html) as the automatic metric and MQM for the human evluation. <br />
The official rankings will be based on the MQM scores at the document level, accounting for both directions.
The COMET scores, measured on the document level will be used as the secondary metric.


## Paper Describing Your MT Systems
Participants are invited to submit a short paper (4 to 6 pages) to WMT describing their MT system. Information on how to submit is available [here](https://www.statmt.org/wmt22).<br />
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


