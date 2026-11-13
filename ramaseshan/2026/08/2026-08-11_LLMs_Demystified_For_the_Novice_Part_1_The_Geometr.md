+++
title = "LLMs Demystified For the"
full_title = "LLMs Demystified For the Novice The Geometry of Language"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/how-llms-work-for-dummies-part-1"
date = "2026-08-11"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/how-llms-work-for-dummies-part-1).

LLMs Demystified For the Novice (Part 1) : The Geometry of Language

# LLMs Demystified For the Novice (Part 1) : The Geometry of Language

### In this series of two articles, I explain how LLMs work so that even a curious high school kid who has only a basic knowledge of mathematics can understand and appreciate how they work.

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Aug 11, 2026



108



7



15

Share

[](https://substackcdn.com/image/fetch/$s_!ajyK!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe043ef17-815b-4846-b56c-e4a92613ee1c_330x486.png)

![](https://substackcdn.com/image/fetch/$s_!ajyK!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe043ef17-815b-4846-b56c-e4a92613ee1c_330x486.png)





Are you a person who has never been exposed to mathematics after school but fascinated by LLM tools like ChatGPT, Claude, Gemini, etc.. and want to demystify yourself regarding how they work? Do you want to dive somewhat deeply and be conversant with the latest research in this area and learn the fancy terms they use without getting bogged down by the complexity of the mathematics involved? Then, this article is perfect for you. Get ready for an engaging read regarding the mechanics and principles using which LLMs work without getting entangled amidst complex equations and code. Just a few things worth noting.

**CONVENTIONS FOLLOWED IN THE ARTICLE** :

All new technical terms are highlighted in **bolded yellow** when first introduced in the article. These are the cool words that you can throw around when you meet LLM engineers at parties !

The stuff in these grey boxes summarise the important points of a section.

> The content present here inside these orange margins gives more
> details on a topic and can be safely skipped on a first reading. But,
> they do convey valuable and fascinating information if you do choose
> to engage with them !

------------------------------------------------------------------------

# Drawing Graphs & Learning Functions : Neural Networks as Function-Learners



Do you remember those days in your school physics lab where you would collect data for two related variables, plot them as a bunch points in a graph sheet, and use your intuitive judgement to draw a curve that best describes the relationship between those two variables? Let us assume we want to understand how a cup of boiled water cools down with time. So, we have a stopwatch that records time and a thermometer that records the temperature of water. Let us say we record the temperature of water at some instants of time and plot them into a graph sheet below with “time” in the x-axis and the “temperature” of the water in the y-axis. A typical scatter plot of the data would look like as follows when I collect the time-temperature data for ten instants of time.

[](https://substackcdn.com/image/fetch/$s_!8iLX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc6cb4b7-6544-4ed0-b274-2d4f58463f37_1422x536.png)

![](https://substackcdn.com/image/fetch/$s_!8iLX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdc6cb4b7-6544-4ed0-b274-2d4f58463f37_1422x536.png)





Now, you know from intuition that for the remaining instants of time not recorded, the relation between temperature and time would be something like this.

[](https://substackcdn.com/image/fetch/$s_!7GBR!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae92f8dd-6e2b-4ea0-8da1-97ab07316941_1412x650.png)

![](https://substackcdn.com/image/fetch/$s_!7GBR!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fae92f8dd-6e2b-4ea0-8da1-97ab07316941_1412x650.png)





With this judgement, if someone asks you what is the temperature of water at any instant of time that is not recorded as a data point, you know that this curve would give a very reliable estimate for you to look up and say. This process of fitting a curve is called by so many fancy names in the computer science and the mathematics community like **interpolation**, **curve-fitting**, **regression**, **function-approximation from data**, etc.

**Function** : A fancy word that denotes a fixed relationship between sets of numerical variables (e.g. the fixed relation between temperature and time in the cooling curve of a cup of hot water). If the letter “y” denotes the dependent variable that depends on an independent variable which is denoted by the letter “x”, and the function which describes the relation between them is denoted by the letter “f”, then this is normally denoted by the equation

$`y = f(x)`$

That is why the name function-learning or function-approximation. As neat it was for this simple scenario, things can get complicated soon in typical real life scenarios that can prevent intuitive visualisation from helping us. In our example, there was just one independent variable which is time and just one dependent variable which is temperature of water that depends on the independent variable which is the time elapsed. So, you can take a graph sheet and intuitively fit a curve for prediction. But, for complex problems, there can be hundreds of dependent variables that depend on hundreds of independent variables. For example, let us say that you want to predict the expected rental income and sale price of a building in a particular city quarter given the following details.

[](https://substackcdn.com/image/fetch/$s_!AdIZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b3b8b86-c953-4afd-ad57-ef099927f4d6_1342x404.png)

![](https://substackcdn.com/image/fetch/$s_!AdIZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3b3b8b86-c953-4afd-ad57-ef099927f4d6_1342x404.png)





Here, we see that there are eight independent variables and two dependent variables. Let us assume that you have transaction (buying-selling interactions) data of these variables for a few hundreds of buildings. Using these data for other buildings, you want to predict the sale price and rental income of your house, whose details you know and which you plan to sell. Here, graphing cannot help as you need ten axes to keep track of all the variables. You wish there was some oracle who could have access to a high dimensional graph space with ten axes, and who could plot these hundreds of data as points in that space, and somehow intuitively interpolate and build a smooth relationship using which he can predict the expected sale price and expected rental income given the eight building variables that is not a part of the recorded data. There exists such an oracle and it is called a **neural network**. For beginner purposes, treat a neural network as a black box that learns functions from data. It does interpolation through millions of data through hundreds of variables as easily as you did the interpolation in a two-dimensional graph sheet, to figure out the cooling curve of water.

**Neural Network** : At its core, a neural network is simply an extraordinarily powerful curve-fitter. Whether it is estimating house prices using eight variables, or predicting the underlying trick is the same: **learning patterns from numerical data**. If anyone uses a neural network, it is for learning relationships between a fixed set of numerical variables from data.

------------------------------------------------------------------------

# Language Learning as Function Learning



If neural networks are just glorified curve-fitters that connect across numerical dots and pick up general relationships from them, they might not sound very cool or powerful to begin with. So why are they taking over the world? The secret isn’t just in the machine : it’s the human creativity involved in using these neural networks. That is where the domain expertise comes in. You might want to solve a very practical problem and you might have lot of data that are of relevance in solving the problem. But, for using a neural network, you need to convert your niche problem into a function learning problem and your raw data into data for the function that you want to learn. Once you do this, there are readymade software tools that can train a neural network to handle the rest.

[](https://substackcdn.com/image/fetch/$s_!Fzo8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01f9f5aa-d639-409f-b2d4-bdd483c7e566_1024x597.jpeg)

![](https://substackcdn.com/image/fetch/$s_!Fzo8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01f9f5aa-d639-409f-b2d4-bdd483c7e566_1024x597.jpeg)





The diagram maps out how real-world challenges are translated into a mathematical structure that a neural network can process. At the top, you start with a practical real-world problem which is typically seeking an answer to a particular question, given a set of previous observations or case studies. A domain expert bridges the gap by reframing this problem into a function-learning task. This involves reformulating the questions as independent numerical input variables and the answers as dependent numerical output variables. This converts the raw data into a structured numerical dataset of independent and dependent variables that a neural network can then learn from and make predictions. In the bottom execution pipeline, any new question is first converted into these independent numerical variables, passed through the neural network’s learned relationship function, which outputs the corresponding dependent variables, which is then translated back into a clear, real-world answer.

To use machine learning effectively for any real-world scenario, your primary goal is to translate the problem into a task of function learning from data. Neural networks do not understand human context, physical objects, or qualitative concepts directly; they only compute mathematical relationships between numerical inputs and outputs. Therefore, domain expertise is required to abstract a real-world system into a set of measurable inputs and desired outputs. Once you reframe the question as *“Find the function relationship that best predicts the output numbers given the input number given their data,”* you can harness standard neural network tools to discover that mapping automatically from historical data.

Consider the challenge of medical diagnosis of diabetes based on a patient consultation. At first glance, this might seem like involving clinical reasoning rather than a mathematical function. However, by applying domain expertise, a medical team can convert this process into a function-learning format. To convert this problem, the expert redefines the patient’s condition as a set of independent numerical variables: This can include the following numbers like his age, height, weight, fasting blood sugar level gathered from a lab test, and other qualitative symptoms (like fatigue or thirst) as binary inputs (number 1 for present, number 0 for absent). The target output which is the dependent variable is defined numerically as a score between 0 and 1 where 0 indicates absence of diabetes and 1 indicates presence of diabetes and any number in between denoting the chance that the patient has diabetes. By converting thousands of historical patient files into this structured format, the neural network can fit a high-dimensional function across all the relevant variables as it studies the previous diagnostic data. When a new patient arrives, their symptoms are converted into this numerical format, evaluated by the learned function, and translated back into a machine diagnosis.

[](https://substackcdn.com/image/fetch/$s_!5Qpq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d9c33e9-cfaf-49c4-bcb8-143045646e00_1024x597.jpeg)

![](https://substackcdn.com/image/fetch/$s_!5Qpq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4d9c33e9-cfaf-49c4-bcb8-143045646e00_1024x597.jpeg)





If a neural network is all about learning relationships between numerical variables (function learning from data), then if we are to use neural networks to learn and manipulate in a human language, then we have to convert the problem of language learning into a function learning problem.

If a neural network is nothing more than a system for learning relationships between numerical variables based on their numerical data, how can it master human conversation? The trick lies in reformulation. Before an AI can learn, write, or reason in human language, we have to refashion the entire concept of language into a mathematical function and the linguistic data that we have into the data for these numerical functions so that a neural network can deal with it.

The entire magic of LLMs hinges on this single question : **How do I convert the complex mess of words and their grammatical relationships in a language to numbers and functions that relate numbers?**

The question of how to convert words and relationships in a language to a bunch of numbers and numerical relationships is a tough question to be answered and that is what will occupy us for the entire remainder of this article. We will build up the answer to this question step by step. The entire architecture that is popular these days and converts a language learning problem into a function learning problem which powers all the LLMs out there is called a **transformer**.

[](https://substackcdn.com/image/fetch/$s_!Inh-!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bac4616-4756-4d81-b3c1-7567d70a30d1_1024x559.jpeg)

![](https://substackcdn.com/image/fetch/$s_!Inh-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bac4616-4756-4d81-b3c1-7567d70a30d1_1024x559.jpeg)





So, how do I convert words to numbers and grammar to numerical relations? Let us get started.

------------------------------------------------------------------------

# Tokens and Tokenisation



What is the smallest unit of a language that contains meaning? Letters are the smallest units of a language but by themselves letters do not mean anything. At a first guess, maybe words are the smallest units of a language that contain meaning. Every dictionary of a language contains a list of words. Shall we take then words from a dictionary as building blocks of a language? Turns out it is a good starting guess but the best answer is a little more sophisticated than that. Also, there is another problem if we treat words as the basic unit of language. There are simply too many of them. The Oxford dictionary of English contains almost 600,000 words and the actual word count may run to millions if we include archaic words, technical words, slangs, etc. This is not a manageable chunk of data to store, search, and study with in any easy manner. Also, consider the following sets of words given below.

SET 1 :   
realise, realises, realised, realising, realisation  
salute, salutes, saluted, saluting, salutation  
liberate, liberates, liberated, liberating, liberation  
  
SET 2 :   
girl, girls, girl’s, girls’  
boy, boys, boy’s, boys’  
person, persons, person’s, persons’

SET 3 :   
tall, taller, tallest, tallness  
small, smaller, smallest, smallness  
smart, smarter, smartest, smartness  

You see that instead of treating each of the word above as separate entities is not efficient as we see that they are all related. Also, all of these words can be split up into constituents that contribute grammatical meanings. So, now consider this updated list.

realis, salut, liber   
-e, -es, -ed, -ing, -ation  
girl, boy, person.   
-s, -’s, -s’  
tall, small, smart, great   
-er, -est, -ness

Here, we see that we have split out the recurring suffixes as separate entities denoted by a hyphen. These suffixes have meanings by themselves. For example, the suffix -er conveys that an adjective is in its comparative form, the suffix -est conveys that an adjective is in its superlative form, the suffix -ation conveys the abstract noun associated with an action, the suffix -’s conveys singular possession, and so on. It is both economical to split a word into its root, prefixes, and suffixes, and also the right thing to do. For example, let us say that there are a 10,000 words in the English language that take a prefix **re-** (write → rewrite, grouping → regrouping). Then, if we include all the **re-** prefixed forms of these words separately again, then we will have 10,000 x 2 = 20,000 words to store and manipulate. But if we consider the prefix re- as a separate prefix, then we only have to store this one prefix **re-** and the 10,000 words which gives us a total of just 10,000 + 1 = 10,001 words. So, the number of words drastically reduces if we split them into roots, prefixes, and suffixes. Also, these prefixes and suffixes carry meaning as well and they convey grammatical information. Sometimes, a word cannot be split further and has to be treated as a single unit of meaning (e.g. “**to**”). In other cases when a word can be split into smaller units of meaning (prefix, suffix, root), then we consider such smaller units as the basic building block of language (e.g. “**redeveloping**” = “**re**” “**develop**” “**ing**”). We also consider punctuation marks and even spaces as legit building blocks of language because they also carry a lot of meaning, given that we split up words.

The two sentences “**Eat, mom**” (meaning : you are asking your mother to eat) and “**Eat mom**” (meaning : you are asking someone to eat a mother) have drastically different meanings because of the presence or absence of the comma punctuation. The two sentences “**He has a blue tooth**” and “**He has a bluetooth**” once more have drastically different meanings because of the presence or absence of the space punctuation.

The smallest such unit of a word (word, root, prefix, suffix, space, punctuation) that conveys meaning (concrete or grammatical) that is considered as the basic unit of a language for an LLM is called a **token**.

> Study this section inside the red margin only if you are interested in
> applications involving other languages. Otherwise, you can skip this
> on a first reading.
>
> In the linguistics community, the smallest unit of a word that conveys
> meaning is called a **morpheme**. Ideally, we want the list of tokens
> used by an LLM to coincide with the list of morphemes in the language.
> But they are not exactly the same, and tokens typically contain a
> little more things than morphemes. To understand why, wait until the
> next red box section where we encounter the Byte-Pair Encoding
> Algorithm. But, in this section, I will explain about morphemes in a
> little more detail which can be skipped on a first reading.
>
> The study of how languages vary in their morphology, i.e., how words
> break up into their parts, is called **morphological typology**. While
> morphologies of languages can differ along many dimensions, two
> dimensions are particularly relevant for computational tokenisation.
> Again, you may choose to skip this if you want to focus just on
> English as the rest of the article does.
>
> **Dimension 1 :** The first dimension is the number of morphemes per
> word. In some languages like Vietnamese and Chinese, each word on
> average has just over one morpheme. That is, words are so small that
> they have only one morpheme that cannot be split any further. We call
> languages at this end of the scale as **isolating languages**.
> Alternatively, in languages like Finnish, a single word may have so
> many morphemes, which sometimes may correspond to a whole phrase in
> English and in some other languages, a whole sentence (e.g. the Inuit
> language spoken in Greenland). We call languages toward this end of
> the scale as **synthetic languages**, (like Finnish) and the very end
> of the scale **polysynthetic languages** (like the Inuit language).
>
> Let me give an example. The single Finnish word `Taloissammekin`
> translates into English as “`Even in our houses`*”.* A single Finnish
> word packs a lot of information that takes four English words to
> convey because it splits into five morphemes as follows with their
> meaning given in brackets following them. `Taloissammekin` *=* `talo`
> (house) + -`it`- (plural) + -`ssa`- (in) + -`mme`- (our)+ -`kin`
> (also/even). Such languages that tend to many morphemes into a single
> word are what are called synthetic languages. On the other hand, a
> language like Chinese has exactly one morpheme per word and even
> grammatical information that are typically conveyed by suffixes or
> prefixes in Indo-European languages are conveyed in Chinese by
> separate words.
>
> **Dimension 2 :** The second dimension is the degree to which
> morphemes are easily segmentable. In languages like Turkish and Tamil,
> the morphemes have relatively clean boundaries and are easily
> segmentable with each morpheme conveying exactly one unit of
> grammatical information. Such languages are called **agglutinative
> languages**. Whereas in languages like Russian and Sanskrit, morphemes
> tend to run into each other and a single morpheme can convey multiple
> units of grammatical information. Such languages are called **fusional
> languages**. Consider a Tamil word `Māṇavarkaḷukkāka` which transltes
> to “`for the sake of the students`”. The morpheme breakdown is as
> follows. `Māṇavarkaḷukkāka = Māṇavar` (student) + -`kaḷ`- (plural) +
> `ukk`\[u\] (for) + -`āka` (the sake of). Every piece of this word is
> easily separable and conveys exactly one grammatical information. So,
> it is an agglutinative language. But consider a Sanskrit word like
> `Gacchāmaḥ` which translates into English as “`We go`” and splits as
> `Gacchāmaḥ =` `Gacch` (go) + -`āmaḥ` (present tense, first person,
> singular, indicative). The single suffix -`āmaḥ` cannot be chopped
> into smaller pieces for "first person", "plural", or "present tense"
> or “indicative mood”. Thus, Sanskrit is a fusional language.
>
> [](https://substackcdn.com/image/fetch/$s_!vdNX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94d6b70f-bb50-433e-bf86-7144af04363a_1238x418.png)
>
> ![](https://substackcdn.com/image/fetch/$s_!vdNX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F94d6b70f-bb50-433e-bf86-7144af04363a_1238x418.png)
>
> 
>
> 

Considering tokens as the basic units of meaning in a language is both **economical** (*the number of tokens is much lower than the number of words*) and also **conceptually appropriate** (*tokens are indeed the smallest units of a linguistic utterance that carries meaning*). The process of chopping a raw linguistic corpus into these smart, bite-sized pieces is called **tokenisation.** Considering tokens as the basic building blocks shrinks a dictionary of millions of words down to a manageable vocabulary of around 50,000 to 250,000 tokens.

The very first step when you feed text into an LLM is **tokenisation**, where a program called the **tokeniser** breaks your raw text into its constituent tokens. The tokeniser then looks up each token in its **vocabulary list** (a master directory that consists of numbered entries of tokens) and replaces it with an integer representing its exact position in that vocabulary list. For example, if the sentence that you feed into the LLM prompt has the word `"cat"`, and that token is entry `#3758` in the vocabulary list, the tokeniser simply swaps the string `"cat"` with the number `3758`. Thus, it converts a sentence into a bunch of \#— numbers that denote the IDs of each of the token in the sentence. If you input the sentence *"*`The cat sat.`*"* as a prompt into the LLM, the tokeniser breaks it into four tokens and look up their corresponding IDs in the dictionary which might come out something like : \#464 *"*`The`*"*, \#3758 *"* `cat`*"*, \#3372 *"* `sat`*", ʼʼ*\#13 “`.`”. The prompt is thus converted into the simple numerical sequence `464, 3758, 3372, 13` before being sent to the neural network.

Similarly, when an LLM generates a response, the underlying neural network (which only processes numbers) outputs a sequence of token IDs. In the final step, the de-tokeniser looks up these numbers in the same directory once again and converts them back into human-readable words, punctuation, and spaces. For example, if the neural network in the LLM at the last stage outputs a sequence of token IDs that are `[9288, 318, 4148, 13]`, the program once more looks up each ID in the master directory and finds the token corresponding to them which might come out as \#9288 *"*`Mom`*"*, \#318 *"* `is`*"* (with space), \#4148 *"*` ready`*"* (with space), and \#13 “`.`”, and finally stitches them together to output the final text: *"*`Mom is ready`*.".* The process of converting a bunch of token IDs into a human readable string is called **detokenisation**.

[](https://substackcdn.com/image/fetch/$s_!6pb2!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe93c6466-8c51-4662-8dfa-ed9894358eac_1024x559.jpeg)

![](https://substackcdn.com/image/fetch/$s_!6pb2!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe93c6466-8c51-4662-8dfa-ed9894358eac_1024x559.jpeg)





[](https://substackcdn.com/image/fetch/$s_!9FA7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F916c5d32-36b6-4419-b3fa-8bb57d254bdc_1390x582.png)

![](https://substackcdn.com/image/fetch/$s_!9FA7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F916c5d32-36b6-4419-b3fa-8bb57d254bdc_1390x582.png)





Now that we know about tokenisation and vocabulary list, the following two questions pop up in mind.

1.  **How is this vocabulary list of tokens created in the first
    place?**

2.  **When given a prompt, how does the tokeniser decide exactly where
    to break words into tokens?**

The answers to both of these questions lie in a single algorithm that is widely used in LLMs which is called as **Byte Pair Encoding**.

**A Quick Note for the Reader:** If you are happy to treat tokenisation and vocabulary lists as readymade tools working behind the scenes, feel free to skip ahead. But if you are curious about the inner mechanics of how modern AI constructs its vocabulary and splits up words into tokens, read on! You can of course come back again and read this later!

> **Byte Pair Encoding (BPE) :** This is the most widely used scheme to
> both create a vocabulary list as well as do tokenisation. The first
> task is done by a program called a trainer and the second part is done
> by a program called the encoder.
>
> **Trainer** : How do we create a list of all tokens of the English
> language other than manually of course? We have lots of recorded
> digital textual corpus in the English language on the internet. How do
> we exploit this? The trainer works based on a simple intuition. The
> group of letters that constitute tokens occur much more often than
> expected by chance. For example, take the following three letter
> sequence “`dis-`” that is a popular prefix in the English language
> that conveys the grammatical meaning of opposite (e.g. orient →
> disorient). In a large textual corpus, this sequence of characters
> “`dis`” occurs much more often than any random bunch of three letters
> that do not have any meaning (for example : `rsx`). Similarly, a three
> letter single morpheme word like “`sit`” occurs much more frequently
> in a large running corpus of English text than any random meaningless
> bunch of three letters. The trainer in the BPE exploits this to build
> a list of tokens.
>
> First start with the list of all letters as the initial seed of the
> token list. Now, inspect the entire corpus and find which 2-token
> sequence occurs most frequently in the corpus. Since the initial list
> of tokens are just the letters, this will just be the same as
> identifying the most frequently occurring two-letter sequence in the
> corpus. Then add this most frequently occurring two letter pair into
> the list of tokens. Then, merge this two letter pair and consider it
> as a single entry and put it inside the token list. Now, repeat the
> same search again and find which two-token pair occurs the most
> frequently (now not just the letters but also the two-letter sequence
> counts as a token). Add this most frequently occurring two-token
> sequence into the token list. Keep repeating. We have to repeat this a
> lot of times to capture all morphemes of English. If we repeat this
> enough times, we will capture all the morphemes of the English
> language which tend to occur most frequently. But if we repeat this
> process too many times, then we will include all big words and
> combinations of morphemes as well as entries in our growing token
> list. Eventually, we will include all possible words in the corpus
> into the token list if we keep doing this into its fullest conclusion.
>
> There is a sweet spot to stop this process when the token list has
> expanded to just the correct size to only have the most frequently
> occurring smallest units of letters which mostly capture the morphemes
> and nothing else (no other larger units) bigger than them. The only
> additional thing to mention is that this process is usually run only
> inside words. That is, the algorithm does not merge letters across
> word boundaries to count the frequencies. While counts come from a
> corpus, merges are only allowed within the strings.
>
> **Encoder** : Once the vocabulary list (list of tokens) and the
> prioritised list of merge rules are established, splitting new text
> into tokens is straightforward. The Encoder takes raw input text,
> splits it into individual characters, and then applies the exact merge
> rules in the order they were learned during training. By applying
> these prioritised merges, the Encoder automatically combines character
> sequences into the largest learned sub-words available in its
> vocabulary.
>
> **WORKED EXAMPLE : TRAINER**
>
> As an example, consider the following toy corpus of words :   
> `low low low low low `  
> `lower lower `  
> `newest newest newest newest newest newest`  
> `widest widest widest `
>
> **Starting Base Tokens:** `{d, e, i, l, n, o, r, s, t, w, </w>}` (11
> unique characters that include the word boundary).
>
> **Iteration 1 (Discovering** `es`**)** : The Trainer scans all
> adjacent pairs of characters in the corpus and counts their
> frequencies. Some of them that occur more than once are given below.
>
> - `l + o `: 5 (in *low*) + 2 (in *lower*) = 7
>
> - `o + w `: 5 (in *low*) + 2 (in *lower*) = 7
>
> - `e + s `: 6 (in *newest*) + 3 (in *widest*) = **9** → **Highest
>   Frequency!**
>
> - `s + t `: 6 (in *newest*) + 3 (in *widest*) = 9
>
> - `e + r `: 2 (in *lower*) = 2
>
> **Action:** Merge `e` and `s` into new token `es`.
>
> **Vocabulary:** Adds `es` to the vocabulary (12 tokens total).
>
> **Corpus State:**
>
> - `l o w </w>` : 5
>
> - `l o w e r </w>` : 2
>
> - `n e w es t </w>` : 6
>
> - `w i d es t </w>` : 3
>
> **Iteration 2 (Discovering** `est`**)** : Scan adjacent pairs again
> (now counting `es` as a single unit) and find the most frequently
> occurring token pair. Important among them are given below,
>
> - `l + o `: 7
>
> - `o + w `: 7
>
> - `es + t `: 6 (in *newest*) + 3 (in *widest*) = **9** → **Highest
>   Frequency!**
>
> **Action:** Merge `es` and `t` into new token `est`.
>
> **Vocabulary:** Adds `est` (13 tokens total).
>
> **Corpus State:**
>
> - `l o w </w>` : 5
>
> - `l o w e r </w>` : 2
>
> - `n e w est </w>` : 6
>
> - `w i d est </w>` : 3
>
> **Iteration 3 (Discovering** `lo`**) :**
>
> Scan adjacent pairs again merging letters in the token list and count
> their frequencies :
>
> - `l + o `: 5 (in *low*) + 2 (in *lower*) = **7** → **Highest
>   Frequency!**
>
> - `o + w `: 7
>
> - `w + est `: 6 (in *newest*) = 6
>
> **Action:** Merge `l` and `o` into new token `lo`.
>
> **Vocabulary:** Adds `lo` (14 tokens total).
>
> **Corpus State:**
>
> - `lo w </w>` : 5
>
> - `lo w e r </w>` : 2
>
> - `n e w est </w>` : 6
>
> - `w i d est </w>` : 3
>
> **Iteration 4 (Discovering** `low`**) :**
>
> Scan adjacent pairs again:
>
> - `lo + w`: 5 (in *low*) + 2 (in *lower*) = **7** → **Highest
>   Frequency!**
>
> **Action:** Merge `lo` and `w` into new token `low`.
>
> **Vocabulary:** Adds `low` (15 tokens total).
>
> **Corpus State:**
>
> - `low </w>` : 5
>
> - `low e r </w>` : 2
>
> - `n e w est </w>` : 6
>
> - `w i d est </w>` : 3
>
> **Iteration 5 (Discovering** `er`**) :**
>
> Scan adjacent pairs again:
>
> - `e + r`: 2 (in *lower*) = **2** → **Highest Frequency remaining!**
>
> **Action:** Merge `e` and `r` into new token `er`.
>
> **Vocabulary:** Adds `er` (16 tokens total).
>
> **Corpus State:**
>
> - `low </w>` : 5
>
> - `low er </w>` : 2
>
> - `n e w est </w>` : 6
>
> - `w i d est </w>` : 3
>
> **Iteration 6 (Discovering** `wi`**) :**
>
> Checking remaining adjacent pairs across the corpus:
>
> - `n + e` (1 time in *newest*)
>
> - `e + w` (1 time in *newest*)
>
> - `w + i` (1 time in *widest*) → **Selected** *(Tied frequencies can
>   be picked in alphabetical or scan order)*
>
> **Action:** Merge `w` and `i` into `wi`.
>
> **Vocabulary:** Adds `wi` (17 tokens total).
>
> **Corpus State:** `wi d est </w>` (in *widest*)
>
> **Iteration 7 (Discovering** `wid`**) :**
>
> Checking remaining adjacent pairs:
>
> - `wi + d` (1 time in *widest*) → **Highest remaining frequency!**
>
> **Action:** Merge `wi` and `d` into `wid`.
>
> **Vocabulary:** Adds `wid` (18 tokens total).
>
> **Corpus State:** `wid est </w>` (in *widest*)
>
> **Iterations 8 & 9 (Discovering** `ne` **&** `new`**) :**
>
> Similarly, processing `"newest"` takes two more merges (`n + e` →
> `ne`, then `ne + w` → `new`) to form the root token `new`.
>
> The True Natural Stopping Point
>
> Now, look at the vocabulary state after **Iteration 9**:
>
> Vocabulary: {base characters}+{es,est,lo,low,er,wi,wid,ne,new}
>
> This is the **true sweet spot** for this toy corpus to stop. Any more
> iterations, it will continue to generate larger tokens the size of
> entire words.
>
> WORKED EXAMPLE : ENCODER  
> Now with the vocabulary {base characters}+{es, est, lo, low, er, wi,
> wid, ne, new}, suppose a user inputs the prompt containing the word
> `"lowest"`. Note that this model has never seen this exact word during
> training as our training data did not contain the word “`lowest`” but
> only “`widest`” and “`lower`”. But it can split the new word “lowest”
> into the tokens “`low`” and “`est`” since it has picked them up from
> the other words in the training vocabulary corpus. Here is how the
> Encoder processes it:
>
> **Step 0: Initial Character Split**
>
> The Encoder breaks the input string into individual base characters:
>
> Current State: \[”l”,”o”,”w”,”e”,”s”,”t”\]
>
> **Step 1: Apply Rule 1 (**`e` **+** `s` **→** `es`**)**
>
> The Encoder scans the current sequence from left to right for adjacent
> pairs matching `e` and `s`. It finds `e` and `s` at positions 4 and 5
> and merges them:
>
> Current State: \[”l”,”o”,”w”,”es”,”t”\]
>
> **Step 2: Apply Rule 2 (**`es` **+** `t` **→** `est`**)**
>
> The Encoder scans for adjacent pairs matching `es` and `t`. It finds
> `es` and `t` at the end of the word and merges them:
>
> Current State: \[”l”,”o”,”w”,”est”\]
>
> **Step 3: Apply Rule 3 (**`l` **+** `o` **→** `lo`**)**
>
> The Encoder scans for adjacent pairs matching `l` and `o`. It finds
> them at the beginning of the word and merges them:
>
> Current State: \[”lo”,”w”,”est”\]
>
> **Step 4: Apply Rule 4 (**`lo` **+** `w` **→** `low`**)**
>
> The Encoder scans for adjacent pairs matching `lo` and `w`. It finds
> them and merges them:
>
> Current State: \[`low, est`\]
>
> **Steps 5 through 9: Scanning Remaining Rules**
>
> The Encoder scans the remaining rules (**Rule 5** through **Rule 9**):
>
> - **Rule 5 (**`er`**):** No `e` + `r` pair present in
>   `["low", "est"]`. *(Skip)*
>
> - **Rule 6 (**`wi`**):** No `w` + `i` pair present. *(Skip)*
>
> - **Rule 7 (**`wid`**):** No `wi` + `d` pair present. *(Skip)*
>
> - **Rule 8 (**`ne`**):** No `n` + `e` pair present. *(Skip)*
>
> - **Rule 9 (**`new`**):** No `ne` + `w` pair present. *(Skip)*
>
> **Final Tokenised Output :**
>
> No more merge rules apply. The Encoder finishes and converts the
> sequence into its final sub-word tokens:
>
> Final Tokens: \[`low`, `est`\]
>
> **Key Takeaways for the Reader**
>
> 1.  **Deterministic Order:** The Encoder doesn’t make subjective
>     guesses or search for the “biggest word first.” It simply iterates
>     through the learned merge rules in their exact historical priority
>     order.
>
> 2.  **Generalisation in Action:** Even though `"lowest"` was absent
>     from the training set, BPE successfully mapped the unfamiliar word
>     onto two highly reusable sub-word tokens: the root `"low"`
>     (learned from `low` and `lower`) and the suffix `"est"` (learned
>     from `newest` and `widest`).

------------------------------------------------------------------------

# The Geometry of Words : Vector Embeddings



### From Token IDs to Geometric Embeddings



Having converted a linguistic text into a series of tokens with IDs, what next? It turns out token IDs are not great numbers to play with. Whatever way you arrange these tokens and assign IDs to them serially, these IDs are not physically meaningful in any sense. Let us give some examples. We know that words/tokens like “`cat`”, “`dog`”, “`reindeer`”, “`cow`” and “`bison`” are more similar to each other (they are all words for animals). In a vocabulary list, these words will be assigned random numbers and far apart from each other whether we follow a frequency based ordering or alphabetic ordering. Also words/tokens like “`sit`”, “`seat`”, “`sat`”, “`chair`” are more similar to each other semantically (they are all words related to the action of sitting). But their token IDs do not convey this relationship. Even if we rearrange the tokens such a way that similar words get nearby token IDs, this still cannot capture the full range of semantic relationships. Let us give some examples to illustrate this.

- For example, the words “`early`” and “`late`” are semantic opposites
  yet share similar contexts (they are used to describe the same kind of
  stuff that have to do with timing) and also have the same grammatical
  roles (adjectives). Should their IDs be right next to each other
  because they share context and grammatical role, or should we put them
  far apart in the token list because they mean opposite things?

- Consider the words/tokens “`cat`”, “`parrot`”, and “`tiger`”. The
  words/tokens “`cat`” and “`parrot`” are dissimilar because one is an
  animal and another is a bird. But they are both pets and are similar
  to each other in that respect. But the words/tokens “`cat`” and
  “`tiger`” are also more similar to each other because they are both
  feline animals but they are dissimilar because one is a domestic pet
  and another is wild. How does assigning numerical IDs to each of these
  words capture these multi-faceted relationships that these
  words/tokens have with each other (the same word pair being similar in
  one aspect but different in another aspects)? Human language also
  contain more complex relationships.

- For example, we know that the word/token “`king`” is related to the
  word/token “`queen`” in the same way the word/token “`man`” is related
  to the word/token “`woman`”. This complex multi-directional
  relationship cannot be encoded by assigning them numbers in any serial
  arrangement. We have to convert these token IDs into a meaningful
  geometric representations that faithfully represent their semantic
  relationships.

- Consider the four words “`water`”, “`oxygen`”, “`H_2O`”, and “`O_2`”.
  The pair of words “`water`” and “`H_2O`” and also the pairs “`oxygen`”
  and “`O_2`” are similar in meaning in the sense that they refer to the
  same entities. But, when it comes to context, we see that the pair
  “`water`” and “`oxygen`” occur in similar contexts involving everyday
  non-scientific genres whereas in a technical context one expects to
  see the pair “`H_2O`” and “`O_2`”. Even though “`water`” and “`H_2O`”
  are semantically synonyms, they occur in different contexts. For
  example, one would be very surprised to see the word “`H_2O`” in a
  hiking manual or a newspaper or a flight safety instructions kit but
  when it comes to technical contexts and complex chemical equations,
  one would not expect to see “`water`”. So, we see that words can be
  similar in the semantic dimension but still dissimilar in contextual
  dimension. So, we have a tension here between semantic similarity and
  genre similarity.

A flat list of serial numbers cannot capture multi-faceted contextual, grammatical, and semantic relationships between tokens. We must convert token IDs into a **meaningful geometric representation ;** assign them positions in a geometric space where the many distances and directions in that space faithfully reflect all their complex relationships.

The process of converting a list of tokens of a language into a meaningful geometric representation that faithfully encodes all of their complex semantic and contextual relations through the distances and directions available in that geometric space is called **embedding**. The linguistic field that studies such embeddings and their meanings is called **vector semantics**.

[](https://substackcdn.com/image/fetch/$s_!7hRX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8afaf22c-1e31-4b48-aad9-9b1b56d0dcd9_1024x559.jpeg)

![](https://substackcdn.com/image/fetch/$s_!7hRX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8afaf22c-1e31-4b48-aad9-9b1b56d0dcd9_1024x559.jpeg)





Let us see how a multi-dimensional embedding helps us by using an example that we already encountered.

[](https://substackcdn.com/image/fetch/$s_!CEZ8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f0c7fd2-33e0-4fa9-8e82-e477955dc0a6_1384x918.png)

![](https://substackcdn.com/image/fetch/$s_!CEZ8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f0c7fd2-33e0-4fa9-8e82-e477955dc0a6_1384x918.png)





The following shows a geometric placement of a group of animals based on a two-dimensional grid where the horizontal axis represents the petting level of the animal whereas the vertical axis represents the felinity of the animal. Consider “`cat`” and “`tiger`” here. They are horizontally far apart and on the opposite ends of the spectrum because the horizontal axis represents pet-ness and clearly cat is a popular pet animal whereas a tiger is a wild and ferocious animal. But since they are both feline, they share the same vertical position and project to the same point on the vertical axis. On the other hand, consider “`cat`” and “`dog`” here. They are vertically far apart and on the opposite ends of the spectrum because the vertical axis represents feline nature and clearly cat is a feline animal whereas a dog is not. But since they are both pet animals, they share the same horizontal position and project to the same point on the horizontal axis.

Thus, we have seen that, **if we assign two numbers (called coordinates in geometry) for each animal in this representation in a two-dimensional planar space, then we can more faithfully capture the two-dimensional relationships between animals based on their two independent characteristics** (pet vs wild & feline vs non-feline). If we have a third axes and assign three coordinates , we can capture more one more feature (for example, size : small vs large, food : herbivore vs carnivore). While humans cannot visually imagine a space beyond three dimensions, a computer handles N-dimensional space (a space with N-axis) with ease; to a machine, a high-dimensional space simply means keeping track of an array of N coordinates. A two dimensional space is equivalent to keeping track of two numbers and a three dimensional space is equivalent to keeping track of three numbers (thanks to high-school coordinate geometry). **A human being cannot imagine spaces with dimensions four or higher, but a computer has no problem going beyond three-dimensional spaces because all it sees is keeping track of more numbers (or coordinates). And a computer finds it as easy to keep track of a thousand numbers (1000-D space) as easily as it can keep track of three numbers (3-D space).** So, we can have some axes or directions representing animals, some for actions related to movement and so on. The process of converting a token number to a bunch of coordinates in a N-dimensional space (a space that needs N coordinates or numbers to keep track of) is called **embedding**. This dimension N should be large enough to contain enough perpendicular axes to convey all possible distinct relations between all words in a language. But how large exactly should this dimension of the space N be in order to achieve this for a human language? Is a hundred dimensions with a hundred perpendicular axes enough? Or do we need to go to a thousand? Or a million? Or a billion? (Even computers give up at this much high numbers). Turns out, the answer is really positive and this is what is the subject of the following sub-section.

### The Indian King, Chess & Exponential Growth



Typically, the dimensions of embeddings in LLMs run from around five hundred to a few thousand (on average : a thousand) so that every word is represented by a thousand numbers (coordinates) on average. You might think that our language has at least tens of thousand of concepts and categories even upto a million, but instead of using a million coordinates in a million dimensions, how can a thousand numbers and thousand dimensions be enough? This is a very deep thing to understand. Turns out that in an N-dimensional space with just N-coordinates, we can have at maximum, only N perpendicular directions to serve as axes. So far, this is obvious - a two-dimensional space with two coordinates can have a maximum of only two perpendicular directions ; a three-dimensional place with three coordinates can have a maximum of only three mutually perpendicular directions ; hence we expect that a N-dimensional place with N coordinates can have a maximum of only N perpendicular directions. So, the maximum number of mutually “exactly”perpendicular directions in a N-dimensional space is equal to N itself and hence grows proportionally to N.

But turns out that if we are okay with only approximately perpendicular axes, then the number of approximately mutually perpendicular axes is no longer proportional to the dimension N but is proportional to the exponential of the dimension of that space which grows much faster than N ! Turns out that when the dimension N is large, the maximum number of “approximately” mutually perpendicular directions P in a N-dimensional space is given by

> $`P = K\mspace{631mu} 2^{\epsilon N}`$

where K is a proportionality constant and the fancy Greek letter ϵ is related to the amount of error in the perpendicularity that you are willing to tolerate (mathematicians will frown at this vague equation ; if you are more mathematically sophisticated, refer to another article that I have written specifically on this result and the link to that article follows shortly). This means that **adding just a few extra dimensions doubles the number of approximately perpendicular directions available** !! Doubling is what people call as an exponential growth and it is incredibly faster than a proportional growth ! There is an Indian folk tale about the invention of chess that illustrates the power of exponential growth that goes as follows. The king was so delighted by the invention of the chess game that he offered the inventor any reward he wanted. The inventor of the game who was a humble sage, said: *“Oh king, I am a simple man. I only ask for rice. Place one grain of rice on the first square of the chessboard. Then, place two grains on the second square, four on the third, eight on the fourth, and so on. Just keep doubling the number of grains for each of the 64 squares.”* The king laughed, thinking the sage was a fool for asking for such a meagre reward. He ordered his treasurer to pay the man immediately.

**The Trap:**

- **Square 1:** 1 grain. (2^0)

- **Square 2:** 2 grains. (2^1)

- **Square 3:** 4 grains. (2^2)

- **Square 10:** 512 grains (a small handful). (2^9)

At this point, the king was still smiling. But then they passed the halfway mark of the board.

- **Square 32:** ~ (approximately) 2 billion grains (2^31 - about a
  large field’s harvest)

- **Square 64:** 10 quintillion grains….

This isn’t a sack of rice. This is a mountain of rice larger than Mount Everest. It is more rice than has been produced in the entire history of the human race. The king went bankrupt not because he was poor, but because he didn’t understand **exponential growth**. Exponential growth starts slow and looks harmless. But once it hits the “knee point,” it shoots up vertically, becoming effectively infinite.

[](https://substackcdn.com/image/fetch/$s_!MtU6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04c32919-1253-41d6-81a1-e3f537d0c63c_960x640.jpeg)

![The Legend Of Rice And Chess: Exponential Growth - Pragati Rice](https://substackcdn.com/image/fetch/$s_!MtU6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F04c32919-1253-41d6-81a1-e3f537d0c63c_960x640.jpeg "The Legend Of Rice And Chess: Exponential Growth - Pragati Rice")





Now, how does this relate to our math problem about vectors and orthogonality? In this story, the squares of the chessboard represent the dimension (N) of our space. The **number of rice grains** represents the number of approximately orthogonal vectors we can fit in that space. Like our minister asked for a rice grains that grow to the power of 2 with each square position, I told you the result that the maximum number of approximately perpendicular directions available in a space increases proportionally with some power of two (refer to the equation again below).

$`P = K\mspace{631mu} 2^{\epsilon N}`$

This means that the number of approximately perpendicular directions available in a space doubles every few fixed increase in dimensions! So, this is the same chess game tale happening in practice. In **low dimensions** (the first few squares)**,** when we are in 1D, 2D, or 3D space (like the first few squares of the chessboard), the “room” available for orthogonal vectors is tiny. In 2D Space, you can only have **2** perpendicular vectors (X and Y). In 3D Space**,** you can only have **3** (X, Y, Z). It feels crowded. If you try to add a 4th vector, it ***must*** **overlap** with the others. There is no “space” left. But, in high dimensions **(**the second half of the Chessboard**),** as we increase N (the dimension), we are moving to the later squares of the chessboard. Just like the rice grains doubled with every square, the exponential bound that we derived (for the number of orthogonal vectors that can be accommodated) proved that the number of approximately perpendicular vectors P that we can fit without grows exponentially with N. So, at N=100, we aren’t just adding room for a few more vectors. We are suddenly in a universe where we can fit millions of mutually perpendicular directions. At N=1000, we have passed the “Mount Everest” point. The space is now so vastly, mind-bogglingly huge that you could pick billions of directions that are approximately perpendicular to each other. In computer science, this phenomenon of the staggering power of exponential growth is called “**the curse of dimensionality**”. If the computational effort exponentially grows with the dimension of the data, then the problem effectively becomes unsolvable beyond a point because eventually the exponential effort is going to kill you. But, in this case, what is normally a “curse” of exponential growth (when it comes to the growth of computing time or space) becomes a “boon” here for accommodating approximately orthogonal vectors in a space. If you are building a garage or a storehouse or a library (or a database), in 3D space, you only have directionally 3 distinct axes of shelves (X, Y, Z). But, in a 1,000-dimensional space, you have trillions of approximately orthogonal shelves. You can give every single narrow genre of book (or data point) its own private shelf (orthogonal direction).

Just as the king underestimated the rice because he couldn’t visualise the explosion of numbers on the 64th square, we underestimate high-dimensional space. We think adding a few more dimensions just adds ‘few more axes’ like adding a line on a graph. In reality, adding a dimension doubles the ‘volume’ of the universe. In 10,000 dimensions, space is so incredibly vast that everything is far away from everything else, and ‘collisions’ (where two different ideas get confused) become mathematically rare and this leaves space for a staggering number of approximately independent perpendicular directions to work with. So, thanks to the exponential growth result, **just a thousand dimensions can give millions of approximately perpendicular directions which can capture all the semantic dimensions of distinctions possible in a language**.

There is no way we can intuitively visualise this phenomenon as our mind cannot imagine any space with a dimension bigger than three but that is the sorcery of mathematics that it gives us tools to probe and derive information about ideas and constructs like multi-dimensional spaces that are otherwise impossible to imagine !

If you are mathematically mature and can handle college level mathematics, refer to the article below where I derive the result in all its precision and prove that the number of approximately perpendicular directions available in a space grows exponentially with its dimension. The result is called as the **Johnson-Lindenstrauss Lemma** in the mathematics community.

[](https://ramaseshanchandrasekaran.substack.com/p/an-indian-king-high-dimensional-garages)

![An Indian King, The Boon of High Dimensional Garages & Natural Language Processing](https://substackcdn.com/image/fetch/$s_!cKJl!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd3286831-7c73-474a-9c73-380e8b835125_1498x1068.jpeg)

#### An Indian King, The Boon of High Dimensional Garages & Natural Language Processing

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

December 24, 2025

[](https://ramaseshanchandrasekaran.substack.com/p/an-indian-king-high-dimensional-garages)

Read full story

### How Computers Learn Semantic Relations



Okay, embeddings are great. But, how are they done? If you think engineers are patient enough to manually sit, design the directions, and assign a bunch of thousand coordinates to every token, then it would take forever. The number of dimensions N of the space to use is pre-decided. But, what coordinates to assign to each word in that space is learnt by a neural network. In this sub-section, let me describe a popular method to learn embeddings and as usual, I will treat a neural network as a black box that learns function from data. Before that, one needs to know how do computers learn the different shades of “meanings” of words so that it can assign appropriate coordinates to them? How does a computer learn that some words refer to pet animals and some words refer to feline animals? We humans learn relationships between various words by observing the relationships between the objects in the world that they mean. We learn that words like “`cat`”, “`tiger`”, “`leopard`”, “`lion`”, “`jaguar`” share a similarity in their feline nature because we actually see the animals that these words refer to and actually observe that these animals share some properties in common. But, a computer does not have that luxury and cannot “see” the objects referred to by the words. How does it then decode the semantic meanings encoded in a word? The answer is succinctly captured in the quote by the British linguist **John Rupert Firth** who said in 1957 that “*You shall know a word by the company it keeps*”. A computer does not learn that a feline animal is one that looks like a cat (it cannot look at anything) but by the fact that they can be replaced for one another in some contexts. Consider the following sentences :

`__ has a sharp and retractable claw.`

`__ is carnivorous and has 30 teeth.`

`__ has a lithe and muscular frame with a highly flexible spine joined by muscles`

`__ walks on toes with soft paw pads and has five toes on forefeet and four on hind feet.`

`__ has a tongue that is covered in rough, horn-like papillae used for rasping meat from bone and grooming. `

`__ has large eyes with an exceptional night vision and broad binocular fields.`

`__ has outer ears driven by multiple muscles that swivel 180 degrees to precisely locate high-frequency sounds.`

`__ has highly sensitive vibrissae on the muzzle, cheeks, and above eyes to detect minute air currents and spatial dimensions.`

`__ is equipped with an organ in the roof of the mouth to analyse scents and pheromones.`

In all of these sentences and other related ones, you can substitute for the first word any from the list of feline animals {“`cat`”, “`tiger`”, “`leopard`”, “`lion`”, “`jaguar`”}, and they all will be valid sentences. As the LLM model is trained with lots of textual corpuses from zoology involving writings about various animals, it learns that there are sentences like those shown above in the training corpus where the words for all the animals in the list {“`cat`”, “`tiger`”, “`leopard`”, “`lion`”, “`jaguar`”} can come. So, it learns that in some groups of sentences (involving discussions on zoology), these words {“`cat`”, “`tiger`”, “`leopard`”, “`lion`”, “`jaguar`”} are replaceable with each other. So, it figures out that the words {“`cat`”, “`tiger`”, “`leopard`”, “`lion`”, “`jaguar`”} are similar in some context not because they refer to feline animals but because they are replaceable in certain sentence contexts. So, an LLM learns relations between words not based on their meanings but based on their patterns of co-occurrence with other words.

The computer doesn't know what a feline animal “looks” like; it simply figures out that because words like **"cat"**, **"tiger"**, and **"leopard"** are repeatedly interchangeable across a certain group of thousands of sentences encountered in zoological corpuses on which it is trained, hence they must share a close geometric relationship in some dimension(s). An LLM learns the nuances of semantic relationships between words not from real-world sensory meaning, but from their **statistical patterns of co-occurrence**.

### How Neural Networks Learn Embeddings : From Fill in the Blanks to Function Learning



We saw the general philosophy of how computers in general pick up the semantic relationships between words. Now, let us come to the exact problem. **How does a neural network discover which coordinates to assign to every word (token) in the embedding space?** As always in machine learning, we must frame this embedding problem as a **function learning problem**. We have to convert this problem of embedding into a function learning problem and we have to transform the immense linguistic training data to data for the function. In this subsection, we will learn about a pair of models that have been used and are still used in many NLP applications and go by the name **Word2Vec**. Although they have been replaced by more sophisticated models and transformers, it is useful to get an introduction to this simpler model before we go on to discuss more complicated methods because components used in these simpler and relatively unsophisticated and outdated models recur in the currently used transformer models. Before that, or the first step, the tokens are represented as very large dimensional vectors as follows.

Let the total size of the vocabulary be V. Consider a V-dimensional space with V coordinates (x_1, x_2, x_3, ….. , x_V). Notice that typically V is huge and runs into about a 100,000. Now, represent a token with number \#K by the coordinate (0, 0, 0, 0, … , 1, 0, 0, …., 0) where only the K^th coordinate x_k is 1 and the rest of all the coordinates are zero. Such a V-dimensional vector with 1 at the position \#k and 0 everywhere else is called the **One-Hot Vector** corresponding to the token number \#k.

[](https://substackcdn.com/image/fetch/$s_!6go4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b2fe3ed-b91a-4e4f-a444-627995617a50_952x404.png)

![](https://substackcdn.com/image/fetch/$s_!6go4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7b2fe3ed-b91a-4e4f-a444-627995617a50_952x404.png)





This means that each token is represented by an axis in the very large V-dimensional space. This One-Hot Vector is just a rewriting of the token number as a large vector with 1 in the position corresponding to its index and 0 at all other positions. Note that this kind of One-Hot Vector representation is useless on its own because of two reasons.

1.  **Unmanageable Size:** V is far too large with lots of 0s for
    searching, manipulation and computation.

2.  **Lack of Geometry:** In this representation, every single token
    vector is strictly perpendicular (orthogonal) to every other vector.
    The vector for `"cat"` is just as far from `"dog"` as it is from
    `"airplane"`, encoding zero semantic similarity. Remember that we
    want similar words to be close in directions encoding that
    similarity - remember the diagram below).

[](https://substackcdn.com/image/fetch/$s_!CEZ8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f0c7fd2-33e0-4fa9-8e82-e477955dc0a6_1384x918.png)

![](https://substackcdn.com/image/fetch/$s_!CEZ8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2f0c7fd2-33e0-4fa9-8e82-e477955dc0a6_1384x918.png)





Because the V-dimensional space One-Hot representation is too large and uninformative, we want to map our tokens down into a much smaller d-dimensional embedding space (where d is in the range of hundreds or thousands). To do this, we set up two mathematical functions (for those more technically strong, these are actually matrix transformations P and Q) that convert vectors back and forth between these spaces. So, we want mathematical functions P and Q that take us back and forth between this large V-dimensional space (where tokens are represented by just one 1 and lots of zeroes) and the much smaller d-dimensional embedding space. Let P be the function that takes us from this larger V-dimensional representation to the smaller d-dimensional embedded coordinate. Let Q be the function that takes us from the small d-dimensional embedding representation to the large V-dimensional representation where the token number is easily identifiable. To add more details :

- **Function P (The Encoder / Embedding Lookup):** Takes the sparse
  V-dimensional One-Hot vector of a token with lots of 0s and projects
  it down into a d-dimensional coordinate (z1,z2,…,zd) inside the
  bottleneck embedding space of much smaller dimensions that also
  captures all the semantic relations between words as geometric
  relations.

- **Function Q (The Decoder / Output Projection):** Takes a
  d-dimensional vector from the embedding space and projects it back up
  into the V-dimensional space, translating coordinates back into
  vocabulary-level numbers.

The following illustrate the P and Q (in more technical language, P and Q are matrices that transform vectors between the two spaces).

[](https://substackcdn.com/image/fetch/$s_!xspC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bffb946-e509-4a93-8e66-be3f806acdfe_1352x642.png)

![](https://substackcdn.com/image/fetch/$s_!xspC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9bffb946-e509-4a93-8e66-be3f806acdfe_1352x642.png)





So, we see that we have to be able to convert back and forth between token indices (represented by V-dimensional vectors with 1 at the token number and 0 everywhere else) and the embedding space of d-dimensions. So, how do we use the data of the linguistic corpus to figure out what are the correct functions P and Q? Here is where a slight tweak comes in.

At the core of Word2Vec is a fill-in the blanks problem. Depending on the type of fill in the blanks problem, there are two types of Word2Vec for learning embeddings. Let me start with one model called the **Continuous Bag of Words (CBOW) Model**. Consider the following fill-in-the blanks example.

`The Nobel prize in __ this year was awarded for research in superconductivity.`

Everyone knows that given the context of the entire sentence, the only appropriate word that can fill the blank above is the word “`physics`”. But, note that this fill in the blanks tells us something. It tells us that the word “physics” is related to words like “`Nobel`” and “`superconductivity`”. So, we know that the correct answer to this fill-in-the-blanks question is only the word “`physics`”. Let the word “`physics`” in our vocabulary be at position \#563. Then, this correct answer can be represented by the One-Hot Vector corresponding to 1 at the \#563th position and zero everywhere else.

[](https://substackcdn.com/image/fetch/$s_!pycX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9a5166b-6d8e-4822-982a-501c0fae7a43_1246x698.png)

![](https://substackcdn.com/image/fetch/$s_!pycX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9a5166b-6d8e-4822-982a-501c0fae7a43_1246x698.png)





But, for other fill-in-the-blanks questions, the answer need not be that straightforward. Consider the following fill-in-the blanks example.

`The __ hunts deer.`

Here, there is no single correct answer but there are a range of correct answers possible. Theoretically, any carnivorous animal that lives in the forest can serve as the example. Let us hypothetically say that our vocabulary is limited and the only tokens in our vocabulary that correspond to carnivorous animals are the words “`lion`”, “`tiger`”, and “`leopard`”. Let us say that the token numbers for these words are as follows : “`lion`” \#14, “`tiger`” \#217, and “`leopard`” \#1345. Let us say that in the training corpora which we train the neural network with has this type of sentences so that the word “`lion`” occurs in this sentence 35% of the time, the word “`tiger`” occurs in this type of sentences 35% of the time, and the word “`leopard`” occurs in this sentence type the remaining 30% of the time. What we learn here is that the words “`lion`”, “`tiger`”, and “`leopard`” tend to co-occur in contexts involving the words “`hunts`” and “`deer`”. So, the correct answer to this question would not be any on the One-Hot Vectors corresponding to any one of these three words but a probabilistic vector with coordinates.

[](https://substackcdn.com/image/fetch/$s_!eJ63!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25a9e80e-9db6-4705-82c3-55f37fe707a7_1222x1040.png)

![](https://substackcdn.com/image/fetch/$s_!eJ63!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25a9e80e-9db6-4705-82c3-55f37fe707a7_1222x1040.png)





So, from the given linguistic corpus that contain millions of phrases and sentences, one can frame many such fill-in-the-blank questions. One knows the answer to these questions already from the corpus by determining the probability with which a given word fills in the blank by studying the pattern of words in the training corpus that fill in such blanks. Viola, now using this fill-in-the-blanks approach, we have now enabled the data for learning P and Q to be created. How? Look at the diagram below.

[](https://substackcdn.com/image/fetch/$s_!wNyq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbad57b55-362f-445e-a680-ef86874597de_1254x880.png)

![](https://substackcdn.com/image/fetch/$s_!wNyq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbad57b55-362f-445e-a680-ef86874597de_1254x880.png)





Consider all the fill in the blanks type questions of the form X \_\_ X X where the second word out of four words is missing . This fill-in-the-blanks question can be reformulated as a function evaluation problem now.

**Fill-In-The-Blanks** : w1 \_\_\_ w3 w4 (fill in for w2)

**Fill in the Blanks as a Function Evaluation Problem :**

y = f(x)  

**What numbers go inside as input “x”** : The three One-Hot vectors corresponding to the words w1, w3, and w4, with zeros everywhere except their right positions.   

**What numbers come out as output “y”** : A vector whose k^th entry is a number that is equal to the probability of the k^th word in the vocabulary to be the answer w_2 that fills in the blanks.   

**What are the data which are collections of (x_i , y_i) for many known cases** : Known answers to known Fill-In-The-Blanks questions generated from the corpus data.

**Training** & **Feedback** :

- Take off a four word portion from the content in the vast training
  corpus. E.g. “`… The lion hunts the deer…`”

- Form a fill in the blanks question based on it.   
  E.g. “`… The ___ hunts the deer…`”

- The answer now needs to be chosen for the blank. The general idea is
  to look for words lying in the middle of these context words in the
  embedded space. One choose the answer by first picking up the point in
  the embedding space that is central to the three given words as the
  answer (say the centre of the triangle joining these three words -
  this is what is called **centre prediction** in the figure above).
  Mathematically, it is done by averaging all the coordinates of the
  three words.   
  E.g. It looks in the embedding space and picks the centre of the
  triangle enclosing the words “`the`”, “`hunts`” and “`deer`” .

- Convert this centre point to a list of words with probabilities by
  sending it through the Q matrix and normalising for probabilities.  
  E.g. let us say that the most probable word corresponding to this
  central point of “`the`”, “`hunts`” and “`deer`” on this initial
  random embedding gives “`box`” (90%), “`green`” (10%) as the most
  probable word. So it answers “`The box hunts deer`” (90% chance) and
  “`The green hunts deer`” (10% chance).

- Compare the guessed answer to the correct answer based on seeing the
  corpus.  
  E.g.   
  **Guessed answer** : “`box`” (90%) , “`green`” (10%)

  **Correct answer** : “`lion`” (35%) , “`tiger`” (35%), “`leopard`”
  (30%) (from searching the corpus)

- Correct the embeddings (P and Q matrices) based on this feedback
  received on comparison so that words like “`lion`, “`tiger`” and
  “`leopard`” move closer to towards the centre of the words “`the`”,
  “`hunt`” , and “`deer`”, etc so that the correct answers to the
  fill-in-the-blanks moves closer to their context words.

- So, now with this example, words that co-occur move towards each
  other. Repeat this for billions of Fill-In-The-Blanks questions
  generated from the corpus. By doing this feedback based adjustment
  billions of times, it comes to become that words related to each other
  in a given context come closer together along the dimensions that get
  chosen for encoding that context, thus converging on the correct
  embedding.

This algorithm above is illustrated below.

[](https://substackcdn.com/image/fetch/$s_!iGCs!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F419953d6-ef30-49ae-a775-dcf16eeba300_1422x1114.png)

![](https://substackcdn.com/image/fetch/$s_!iGCs!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F419953d6-ef30-49ae-a775-dcf16eeba300_1422x1114.png)





So, since Fill-In-The-Blanks is now a function learning problem, the neural network in the computer has to learn the correct P and Q functions so that it sends words to their correct embeddings so that the correct embedding relation can allow it to predict the correct probabilistic vectors for the Fill-In-The Blanks for unknown cases by using the answers from known cases during training with the given linguistic corpus.

Through this self-supervised mechanism, the neural network transforms raw text into geometry. What began as a rigid, uninformative list of flat token numbers is mapped into a continuous embedding space, one where :

- the distance between points reflects shared context

- directional vectors encode contexts and relations

- similar concepts naturally gravitate toward the same neighbourhoods.

By framing the problem of meaning as a problem of fill-in-the blanks, models like Word2Vec demonstrate that we do not need to manually teach a machine human semantics. Given enough text and an embedding space, the geometry of language emerges all on its own. **In the process of learning to answer all the fill-in-the-blanks questions from a corpus training data correctly (which is reformulated as a function learning problem), the neural network adjusts its P and Q such that it chooses the most appropriate embeddings for all tokens, to give correct answers to the fill-in-the-blanks questions that it has been trained on with the corpus.**

**This fill-in-the-blanks question-answer is nothing but a function learning problem since given a bunch of One-Hot Vectors of a bunch of words given** (which are a bunch of numbers)**, the answer generated is a probability score of words that can fill the blank** (which are also a bunch of numbers)**.**

> **Note** : Based on the type of Fill-In-The-Blanks question used for
> feedback and training purposes, the type of algorithm differs. In our
> case, we used the format “w1 \_\_ w3 w4” , four word segments with
> blanks in the second word. This is called **CBOW** (**Continuous Bag
> of Words) algorithm**. The number of words before and after the blanks
> can vary. Here, we have taken a case with one word before the blank
> and one word after the blank. There is another version called the
> **Skip Gram algorithm** which takes one word as the input and tries to
> predict a fixed number of words before and after it as the output. For
> example, a Skip Gram model might take the same sentence “The lion
> hunts deer” , take the word “lion” as the centre word and try to
> predict one word before and two words after it. Hence the
> Fill-In-The-Blanks is of the type “\_\_ `lion` \_\_ \_\_” with answers
> like “`The lion hunts deer`” or “`The lion is king`” and so on with
> the probabilities for each blank.

------------------------------------------------------------------------

# Building the Case for Transformers



The idea of embeddings for words is really wonderful and revolutionary indeed. It is only through embeddings that we can capture multiple semantic relations between words. But, the embedding that we have seen so far is not enough. A single point in an embedding space for a given word, cannot capture the fullest range of meanings that a word takes in various contexts. The embeddings that we saw till now in this article which assign a single set of coordinates for every word are called **static embeddings** because each word (token) gets one fixed vector (one fixed set of numbers) in a d-dimensional space. While algorithms that learn static embeddings like **Word2Vec** marked a monumental leap forward by transforming flat token IDs into a rich geometric space, they do however carry a fundamental limitation: **a token’s vector is forever frozen in place**. Consider the following sentences employing the word `"bank"`.

*“*`I sat by the river bank.`*”* (meaning : shore)  
`I deposited money in the bank.`*”* ( meaning : financial institution)  
“`The cars bank on the hill road.`” (meaning : manoeuvre)

In a static lookup table, a word like `"bank"` receives the exact same set of coordinates no matter whatever sentence it appears in. Even for words with very unambiguous, fixed meanings, subtler shades of context, register, and sentiment alter their functional role in a sentence. Consider the word `"fire"` that is used in the following two sentences :

*“*`The warm fire kept us comfortable.`*”* (pleasant context)   
*“*`The building is on fire!`*”* (distress context).

Consider the following word “`great`” in the following two sentences.

“`The movie was great.`”   
“`The movie was great, said no one ever.`”

Here, the meaning of the word “`great`” when employed in the second sentence, changes to its exact opposite because of the following clause and the sarcastic context it implies. Some words even change their part of speech depending on the sentence.

“`The parcel got delivered on time.`”  
“`Can you parcel this for me?`”

Here, the same word “`parcel`” is used as a noun in the first sentence while as a verb in the second sentence. Also, there are some words in the language whose meanings are inherently ambiguous and hollow when seen alone and whose actual meanings are very heavily dependent upon other words in the sentence. Consider the following sentences :

*“*`My mother said that she was tired.`*”* (she = my mother)   
*“*`After Sarah explained, what had happened, my mother was convinced that she did not do anything wrong.`*”* (she = Sarah)

We see that pronouns like “she”, “he”, and “it” lack any meaning by their own and their exact meaning is informed only when they are seen in the context of their sentences along with other words. It does not make any sense to give any sort of stable embedding position to pronouns like “`she`“ before seeing them used in a sentence.

In a static embedding space, a word is assigned the coordinates of a single fixed point, forced to average out all its potential usages into a single compromise vector. Real language, however, is fluid; the precise nuance, tone, and semantic sense of a word shifts continuously depending on its exact surrounding words where it is seen in. To capture these fluid shades of meaning, we need a mechanism that does not merely look up a pre-computed, frozen vector, but actively updates embeddings of words on the fly based on other words in the sentence, dynamically recomputing a token’s coordinates in the embedding space based on the entire sentence it sits in. This idea was what set the stage for one of the greatest breakthroughs in modern artificial intelligence that came in 2017 : **The Transformer**.

By introducing a technique called **Self-Attention**, Transformers allow every token in a sentence to dynamically communicate with every other token simultaneously. Instead of pulling a static vector from a lookup table, a Transformer calculates a context-infused vector for a token on the fly; thereby letting the embedding coordinates for the token `"bank"` bend toward geography or finance or manoeuvre (depending on the context of the surrounding words) and allowing the embedding coordinates for the token `"fire"` to change depending on whether it is pleasant or bad. It is this revolutionary capability of turning static geometry into dynamic, context-aware geometry, that unlocked true language comprehension and directly powers modern LLMs like GPT-4, Claude, and Gemini.

------------------------------------------------------------------------

# Summary



How do machines made of silicon come to understand human language? To a computer, words like *"bank"*, *"river"*, or *"reindeer"* hold no inherent meaning; they are merely arbitrary strings of text. Before a neural network can reason, translate, or generate stories, it must first convert raw, unstructured words into a format it can perform math on: numbers. But simply assigning a serial ID to every word in the dictionary turns out to be a mathematical dead end. Language is not a flat, one-dimensional list of unconnected words ; it is a rich, interconnected web of meanings, contexts, analogies, and subtle shades of emotion. To bridge this gap, modern artificial intelligence relies on a profound paradigm shift: **transforming words into points on a multi-dimensional geometric space**. In this article, we saw how Large Language Models break down raw text into sub-word tokens, why flat numbers fail to capture semantic relationships, and how neural networks automatically build high-dimensional vector spaces, discovering the hidden geometry of human thought. In our next article in this series, we will unpack the inner mechanics of the Transformer and discover how self-attention brings static embeddings to life!   

The link for the second article in the series to continue from here is given below,

[](https://ramaseshanchandrasekaran.substack.com/p/llms-demystified-for-the-novice-part)

![LLMs Demystified For the Novice (Part 2) : The Transformer & LLM Architecture ](https://substackcdn.com/image/fetch/$s_!UTjN!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7cb6787-110b-4000-926c-5cb97a854edb_2208x1952.png)

#### LLMs Demystified For the Novice (Part 2) : The Transformer & LLM Architecture

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

Aug 15

[](https://ramaseshanchandrasekaran.substack.com/p/llms-demystified-for-the-novice-part)

Read full story

------------------------------------------------------------------------

#### Subscribe to Rama’s Substack

By Rama Seshan Chandrasekaran · Launched a year ago

My personal Substack

Subscribe

By subscribing, you agree to Substack's [Terms of Use](https://substack.com/tos), and acknowledge its [Information Collection Notice](https://substack.com/ccpa#personal-data-collected) and [Privacy Policy](https://substack.com/privacy).

[](https://substack.com/profile/395018655-akinapelli-harshith)

![Akinapelli Harshith's avatar](https://substackcdn.com/image/fetch/$s_!GqKY!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc0e7cac2-d936-42ac-92b4-d008a273ad8b_96x96.jpeg)

[](https://substack.com/profile/370439108-wizard-of-oz)

![Wizard of Oz's avatar](https://substackcdn.com/image/fetch/$s_!9XIW!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc1842e22-d7b3-400f-a71d-43a531a7cc6d_144x144.png)

[](https://substack.com/profile/360871361-tusar-kar)

![Tuṣār Kar's avatar](https://substackcdn.com/image/fetch/$s_!TI95!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fefff33b6-31c6-4a95-8dc4-5678984e18d5_4080x3060.jpeg)

[](https://substack.com/profile/284920280-ravinder-reddy)

![Ravinder Reddy's avatar](https://substackcdn.com/image/fetch/$s_!2Tvm!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77da9531-28fb-41f8-b757-599e5b73f4c6_1202x1204.png)

[](https://substack.com/profile/20902319-sreekar-saha)

![Sreekar Saha's avatar](https://substackcdn.com/image/fetch/$s_!5zg6!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0b9c68f-f127-4622-bb0c-dd6ff98493f0_3456x4608.jpeg)

108 Likes∙

[15 Restacks](https://substack.com/note/p-210606488/restacks?utm_source=substack&utm_content=facepile-restacks)



108



7



15

Share
