Instructor: Dr. Dragomir Radev
# Lecture 1 - Introduction
What is natural language processing (NLP)? It is a study of how to make machine understand and generate natural language - by natural language we don't mean language by animals, but humans.
It is an inter disciplinary area of study - Linguistics, Theorectical Computer Science, Mathematics, Statistics, Artificial Intellignece, Psychology, Databases, etc.

Applications: Web Search, Natural Language Assistants, Translations Systems.

Goals:
Is NLP hard and why? The rules from one language are in general not applicable to other language.

Key Problems; The methods to address them and the limitations of these methods

Language and Communication: This primarily involves two persons. The speaker and The listener.
The speaker - (i) Intent (goals, shared knowledge), (ii)Generation (tactical), and, (iii) Synthesis (text, or speech)
The listener - (i) Perception, (ii) Interpretation (Syntactic, semantic, Pragmatics), and (iii) Incorporation (Understanding)
Both the speaker and the listener should share common grounding (Context). For examples, a person in a bar could point out at a object saying, "I want this" - which would be clear to the listener.

Pipeline of NLP involves: 
```
                                        Language --(U)nderstanding--> Machine --(G)eneration--> Language.
```
Based on the requirement, sometimes we need only the first part, where we want the machine to understand the language, while the other time we want the machine to respond back in form of language as well.


# Lecture 2 - Examples of Text
There are different types of text available and each of them provide different set of challenges. For examples, a news articles may consists of different parts such as current event, background event, speculations, property, and, prenominal reference to previous sentences.

There can be different genres of text: Blogs, emails, press release, chats, debates, medical records, research articles, literary texts, etc, and of different lengths.
Poetry can be more different to understand.

# Lecture 3 - Funny Sentences
There can be also sentences that can be interpreted in different ways maybe sometimes in unintended way.
(Mostly because used phrase can have multiple interpretations)
- Lexical ambiguity 
- Structure ambiguity
- Scope ambiguity
- Others

# Lecture 4 - Administration of course
 Major topics
 - Linguistics, mathematicsla, computational background
 - morphology, syntax, semantics, discourse, pragmatics
 - Core NLP: parsing, pos, text generation
 - Applications: text classification, machine translation, information extraction.
  
 Goals:
 - basic principles and theoretical issues
 - techniques to develop practical robust systems
 - Open research problems
 
 Books:
 Speech and Languagge Processing - Jurafsky
 Foundation of Language Processing - Chris manning
 Natural Language Understanding - James Allen
 
 Alphabet Soup:
 NLP, CL, IR, SP, HLT, NLE, ML
 
 
# Lecture 5: Why is NLP Hard?
- There can be different interpretation like straight-forward interpretation , metaphorical interpretation.
- Common Sense Reasoning - word order, two sentence may look  very similar becuase of many subtle interactions.
- syntax and semantics.
- Word Ambiguity - due to meaning, part of speech, pronunciation (address, number)
- language ambiguity - noun noun phrase (XY)Z or X(YZ)

* NACLO Problems Challenges

Type of Ambihguity
-Morphological eg. impossible, important
-Phonetic eg. Joe's finger got number
-Part of Speech eg. Joe won the first round.
-Syntactic eg. Call Joe a taxi.
-Prepositional (Pp) attachment eg. Joe ate pizza with a fork / with meatballs / with Samantha / with pleasure.
-Sense eg. Joe took the bar exam.
-Modaltiy eg. Joe may win a lottery
-Subjectivity eg. Joe believes that stocks will rise.
-Cc (Coordinating conjuction) eg. Joe like ripe apples and pears.
-Negation eg. Joe like his pizza with no cheese and tomatoes.
-Referential eg. Joe yelled at Mike. He had broken the bike.
-Reflexive eg. John bought him a present
-Ellipsis and parallelism eg. Joe gives Mike a beer and Jeremy a glass of wine.
-Metonymy eg. Boston called and left a message for Joe.

Other source of difficulties 
-Non-standard, slang, and novel words
-Inconsistencies
-Typoes and gramattical errors
-Parsing problems
-Complex sentences
-Conterfactual sentences
-Humor and Sarcasm
-Implicature/inference/world knowledge
-Semantics vs Pragmatics (How sentences are used for certain goals)

Synonyms and Paraphrases
eg. climbed, gained, rose

# Lecture 6: Background
More of Linguistics Knowledge
a) Constituents: unit of synatax of sentences e.g. __Children__ eat pizza. __They__ eat pizza. (Note: repalceable subject or sometimes no subjects e.g. Eat pizza!)
b) Collocations: synonyms are not always interchangable. Big vs Large sister.

How do we get these knowledge into system?
- Manual rules
- Knowledge corpora

c) Phonetics and phonology - study of sounds
d) Morphology - study of word components
e) Syntax - study of sentences and phrase structure
f) Lexical semantics - study of meaning of words
g) Compositional semantics - how to combine words
h) Pragmatics - how to accomplish goals
i) Discourse conventions - how to deal with larger unit of utterances
j) Different level of languages

Computer Knowledge
a) Finite state automata - to encode sequences of words
b) Transducer - combined with (a) to perform some phonological or morpphological analysis
c) Push-Down automata - to process more sophesticated grammar
d) Grammars - reglular grammer, context-free grammer, context-sensitive grammer
e) Complexity
f) Algorithms  - DP 

Mathematics - Proabablity, Statistical models, Hypothesis Testing, Linear Algebra, Optimization, Numerical Methods

Computational tools- Language models, Estimation methods, Context-free grammars (for trees), Hidden Markov Models (for sequence), Conditional Random Fields (CRF), Generative and Discriminative models, Maximum entropy models

Statistical tools
- Vector space representation for Wsd, Nosiy channel for MT, Graph based random walk methods for sentiment analysis

Artificial Intelligence
- Logic (First order logic, Predictive Calculus), Agent (Speech Acts), Planning, Constraint satisfaction, Machine learning


# Lecture 7: Linguistics
how is nlp is related to linguistics?
Linguistics is study of language, and is related to aspeccts such as sounds , syntactic, change over time.
example: IPA Chart (sound systems reference) for consonants and verbs.

* Language are usually relted to each other; cognates e.g. night (english), nuit (frencch), nacht (dutch) and are derived from Proto-Indo European language.
finnish, hungarian, arabic, etc are non indo european languages.

* language family ; language diversity Ethnologue(7358 languages)

* change of language over time ; grimms law:
voiceless stops -> voiceless fricative
voiced stops -> voiceless stop, and so on.

See: NACLO Problem
See: Beowulf Poem (Old English)

Diversity of Languages:
- Articles not present in russian language
- cases e.g. In latin, order of word in determined by cases Puer puellam vexat
- sound systems e.g. glottal stop uh-oh
- social status (e.g. japenese otousan, chichi)
- kinships (warlpiri kinship challenge)

Language Universal
two types: unconditional and conditional
all have verbs and nouns; consonants and nouns;

In declarative sentences with nominal subject and object, the dominant order is always one in which the subject precedes the object.
If inflecions exists then derivation exists eg. sleep to sleeps, drink to drinkable

See: WALS (World Atlas of Language Structure), Ethnologue, Endangered languages


# Lecture 8: Text Similarity
Important application of linguistics and statistics to NLP and help in many different applications.

Express same concepts in many different ways
- "the plane leaves at 12 pm" "the flight depart at noon"
- cat documents asked for IR tasks, so kitten documents also to be considered
- fruit dessert asked, "peach tart" or "apple cobbler" should also be considered
- Dulles and Dallas - ambiguity in speech recognition system

Human judgement of similarity
tiger vs tiger 10
tiger vs cat 7.35

variance was pretty high, although it agreed on overall judgement

Automatic similarity computation (Mikolov 2013)
words similar to "france" - spain, belguim (countries near france geographically)

Types of similarity:

- morphological similarity e.g. respect respectful
- splelling similarity e.g. theater theatre
- synonymy eg. talktive chatty
- homophony eg. raise raze rays
- semantic similarity
- sentence similarity
- document similarity
- cross lingual similarity

