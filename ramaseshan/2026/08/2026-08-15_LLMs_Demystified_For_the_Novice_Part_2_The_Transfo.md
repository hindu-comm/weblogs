+++
title = "LLMs Demystified For the"
full_title = "LLMs Demystified For the Novice The Transformer & LLM Architecture"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/llms-demystified-for-the-novice-part"
date = "2026-08-15"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/llms-demystified-for-the-novice-part).

LLMs Demystified For the Novice (Part 2) : The Transformer & LLM Architecture 

# LLMs Demystified For the Novice (Part 2) : The Transformer & LLM Architecture

### In this series of two articles, I explain how LLMs work so that even a curious high school kid who has only a basic knowledge of mathematics can understand and appreciate how they work.

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Aug 15, 2026



25



7



5

Share

This is the second part in a series of two articles written to demystify LLMs for a beginner who is not of the STEM background. Last article, we discussed about neural networks as function fitters, and about the fundamental concepts of tokenisation and embeddings. To read the previous article in this series, click below.

[](https://ramaseshanchandrasekaran.substack.com/p/how-llms-work-for-dummies-part-1)

![LLMs Demystified For the Novice (Part 1) : The Geometry of Language](https://substackcdn.com/image/fetch/$s_!ajyK!,w_140,h_140,c_fill,f_auto,q_auto:good,fl_progressive:steep,g_auto/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe043ef17-815b-4846-b56c-e4a92613ee1c_330x486.png)

#### LLMs Demystified For the Novice (Part 1) : The Geometry of Language

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

Aug 11

[](https://ramaseshanchandrasekaran.substack.com/p/how-llms-work-for-dummies-part-1)

Read full story

**CONVENTIONS FOLLOWED IN THE ARTICLE** :

As usual, all new technical terms are highlighted in **bolded yellow** when first introduced in the article. These are the cool words that you can throw around when you meet LLM engineers at parties !

**New Convention** : We saw in the last article in detail that tokens are the fundemental building blocks of a linguistic text as handled by computers and not words. But, in this article, I use the the terms “word” and “token” interchangeably wherein when I actually mean only “token” even if I use “word”. The reason is because the term “token” sounds too abstract and does not make an instant connection in your heads unless you are a computer engineer. Hence, to make it easy to resonate with for non-CS folks, I have made this decision. So, remember that hereafter in this article, when I say “word” hereafter, I mean “token” which are parts of words.

The stuff in these grey boxes summarise the important points of a section.

> The content present here inside these orange margins gives more
> details on a topic and can be safely skipped on a first reading. But,
> they do convey valuable and fascinating information if you do choose
> to engage with them

Taking off from the previous article, we will now see here in detail about the Transformer which is the engine that powers all LLM models. Normally, all traditional books on Machine Learning or Artificial Intelligence make it very complicated by having lot of jargon and focusing to discuss everything including minute details at one go. But, if we look at all of it at once and analyse what are the important things happening in a Transformer, we see in the big picture frame that what is happening there are just some important mathematical operations. In this article, we will be focusing only on that zoomed out panoramic view of what happens inside the Transformer.

------------------------------------------------------------------------

# Stochastic Parroting : How LLMs Model Language :



Before we proceed further onto the details of an LLM, there are a few important generic concepts that need to be set straight. Think about how we humans produce language. Let us say that someone asks you to speak on a topic in which you are knowledgeable about. You would frame a vague idea of what to say, then think of keywords to put here and there, then decide what content to say after what, and then finetune and add words as you speak.

[](https://substackcdn.com/image/fetch/$s_!UTjN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7cb6787-110b-4000-926c-5cb97a854edb_2208x1952.png)

![](https://substackcdn.com/image/fetch/$s_!UTjN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff7cb6787-110b-4000-926c-5cb97a854edb_2208x1952.png)





But, this is not how an LLM generates a linguistic content. When you ask it write a whatsapp message and give it a prompt like “`Write a whatsapp message to my friend Akshay inviting him for my house warming ceremony next Friday`”. An LLM actually thinks statistically word by word. It asks : “Given this string “`Write a whatsapp message to my friend Akshay inviting him for my house warming ceremony next Friday`”, ***what is the most probable next token***?”. It passes this string inside and decides that the most probable next words are “`Hi`” (40%) , “`Hello`” (30%), “`Hey`” (20%), “`Dear`” (10%). Then, it now chooses a string to generate based on this probability distribution, which means that it chooses any of these four words with the chance given by their probabilities. Let us say it decides that the next word to this prompted input is “`Hi`”. It now appends this to the prompt and now asks “Given this string “`Write a whatsapp message to my friend Akshay inviting him for my house warming ceremony next Friday : Hi `”, ***what is the most probable next token***?”. It now passes this bigger string inside that also includes its earlier output word and decides that the most probable next words are “`Akshay`” (40%) , “`friend`” (30%), “`buddy`” (10%), “`bestie`” (10%), “`homie`” (10%). Then, it now chooses a string to generate based on this probability distribution, which means that it chooses any of these five words with the chance given by their probabilities. Let us say it decides that the next word to this prompted input is “`Akshay`”. It now appends this to the prompt and now asks “Given this string “`Write a whatsapp message to my friend Akshay inviting him for my house warming ceremony next Friday : Hi Akshay`”, ***what is the most probable next token***?”. With this it keeps choosing words one at a time and uses it own previously generated words as input to decide the probability distribution of the next word. Eventually, the string builds up one word at a time and you would have after few iterations, something like : “`Write a whatsapp message to my friend Akshay inviting him for my house warming ceremony next Friday : Hi Akshay`, `I am having a house-warming ceremony in my newly constructed home next Friday. I would like you to attend it and …`” .

[](https://substackcdn.com/image/fetch/$s_!iAag!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ae34347-bb75-40e9-9c38-b5400fa52120_1536x1024.png)

![](https://substackcdn.com/image/fetch/$s_!iAag!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0ae34347-bb75-40e9-9c38-b5400fa52120_1536x1024.png)





So, an LLM generates linguistic output word by word (or token by token, if you want to be more accurate). It asks :

Given the sequence of words {w₁, w₂, …, w_(n)} so far, what is the probability distribution for the next word w_(n+1))?

Based on that, it makes a decision and chooses the next word w_(n+1) and now it uses it as the input data to ask :

Given the sequence of words {w₁ , w₂ , … , w_(n) , w_(n+1)} so far, what is the probability distribution for the next word w_(n+2)? This continues until it decides to stop.

When a system uses its own generated previous outputs for the current input, tech folks like to give a fancy name for that. It is called **auto-regression**. So, you will say engineers saying that LLMs are auto-regressive and now you know what they mean by that.

This autoregressive mechanism highlights a profound divergence between human cognition and artificial intelligence. When humans speak, our words are anchored in sensory experiences, intentional goals, and a pre-verbal mental model of the world. We hold an idea in mind first, then select words to convey it, not necessarily in order, and we know the overall content and some of the future words we are most probably going to say already in our minds before we start speaking. An LLM, by contrast, operates in reverse: it constructs a response blindly, one token at a time, guided entirely by the statistical probability of what word ought to follow, given the sequence of words generated till now. This fundamental difference sits at the very heart of the debate over whether LLMs possess true intelligence. Skeptics argue that all an LLM does is merely executing a hyper-sophisticated statistically guided string completion task based on the patterns it picked up from the massive training set. This is called by tech folks as “**stochastic parroting**“, thus merely predicting statistical continuations. It hence lacks intentionality, factual grounding, and genuine comprehension. Yet, proponents point to emergent phenomena: to predict the next word with near-flawless accuracy across trillions of contexts, the model must implicitly discover and encode the underlying rules of logic, grammar, and world knowledge within its high-dimensional vector space. Whether this statistical mimicry constitutes genuine reasoning or merely an extraordinary illusion of thought remains one of the defining scientific and philosophical questions of modern AI.

# Motivating Transformers : Context Dependent Embeddings



Last article, we saw about embeddings of words (tokens). A single point in an embedding space cannot capture the fullest range of meanings that a word takes in various contexts. The embeddings that we saw in the last article are called **static embeddings** because each word (token) gets one fixed vector (one fixed set of numbers) in a d-dimensional space. While algorithms that learn static embeddings like **Word2Vec** marked a monumental leap forward by transforming flat token IDs into a rich geometric space, they do however carry a fundamental limitation: **a token’s vector is forever frozen in place**. Consider the following sentences employing the word `"bank"`.

*“*`I sat by the river bank.`*”* (meaning : shore)  
“`I deposit money in the bank.`” ( meaning : financial institution)  
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
*“*`After Sarah explained what happened, my mother was convinced that she did not do anything wrong.`*”* (she = Sarah)

We see that pronouns like “she”, “he”, and “it” lack any meaning by their own and their exact meaning is informed only when they are seen in the context of their sentences along with other words. It does not make any sense to give any sort of stable embedding position to pronouns like “`she`" before seeing them used in a sentence.

In a static embedding space, a word is assigned the coordinates of a single fixed point, forced to average out all its potential usages into a single compromise vector. Real language, however, is fluid; the precise nuance, tone, and semantic sense of a word shifts continuously depending on its exact surrounding words where it is seen in. To capture these fluid shades of meaning, we need a mechanism that does not merely look up a pre-computed, frozen vector, but actively updates embeddings of words on the fly based on other words in the sentence, dynamically recomputing a token’s coordinates in the embedding space based on the entire sentence it sits in. This idea was what set the stage for one of the greatest breakthroughs in modern artificial intelligence that came in 2017 : **The Transformer**. In this article, we will unpack how a Transformer works from scratch, demystifying its inner mechanics without getting lost in impenetrable jargon. But, before we do so, it is good to get the big picture of how LLMs treat language and a big picture idea of what a transformer does and how it is used in an LLM.

------------------------------------------------------------------------

# General Architecture of a Transformer Based LLM



So far, we have seen how an LLM converts a raw input linguistic texts into a series of token IDs using a tokeniser. It then converts each token ID into the coordinates of a vector in the embedding space. Then, after the processing, it generates an output point in the embedding space and then converts it into a probability distribution for the next token from which it samples to choose a particular token as the output.

Input Token(s) → Token IDs → Input Vectors in the Embedding Space → … processing of vectors in the embedding space …… → Output Vector (*for generating the next word*) in the Embedding Space → Output Probability distribution over tokens → Sampling the Output Token

The diagram below summarises this process. The part on the right where we go from a vector in the embedding space (violet colour) to a vector in the vocabulary space (through a matrix Q) which is then normalised to give a probability distribution for the next word is called the **LM (Language Modeling) Head** in the architecure of LLMs.

[](https://substackcdn.com/image/fetch/$s_!ujq5!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd95856eb-7516-46f2-801a-7d4a0fc163f9_1348x684.png)

![](https://substackcdn.com/image/fetch/$s_!ujq5!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd95856eb-7516-46f2-801a-7d4a0fc163f9_1348x684.png)





In this section, we see what happens inside that yellow region. How the input vectors corresponding to input words are transformed to produce the one output vector in the embedding space which will generate a probability distribution for sampling what the next token is. The yellow part is called the **Transformer** block and we will now see the first important thing that happens inside the Transformer block.

Look at the picture below. Let the incoming prompt words have static embeddings w₁, w₂, .., w_(n) shown below. They all go through multiple layers of transformers. The first transformer gets in the static embeddings and returns a context-sensitive embeddings of these same words. The second transformer takes in the output of the first transformer as its input and returns more accurate context-sensitive embeddings of these words. This is then improved upon by the third transformer and finally we have that the last transformer M gives the final very accurate context-sensitive embeddings of these words which we call as c₁, c₂, .. and c_(n). Then, a matrix (the Q matrix which we saw in the last article and revised in the beginning of this section) converts the context sensitive embedding of the final word c_(n) to produce a vector in the vocabulary space which is then normalised to generate a probability distribution for the next word w_(n+1).

[](https://substackcdn.com/image/fetch/$s_!icRc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82167307-5a1e-43f3-b730-2b6e55ea8ccf_1284x1008.png)

![](https://substackcdn.com/image/fetch/$s_!icRc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F82167307-5a1e-43f3-b730-2b6e55ea8ccf_1284x1008.png)





You might ask some questions related to the number of transformer layers in cascade that are used. Why not just one? Turns out that one transformer layer is not enough. We will see why at the end of the next section when we learn what processes go on inside a single Transformer layer. Adding more layers increases the accuracy of the performance of the LLM. But, how many transformer layers are needed in an LLM? Earlier models used a few dozen layers but these days the numbers go in the range of a few hundred. One can of course keep on increasing this but it will create more weights to train and hence requires more intensive training time, and also takes up more computation time and hence we have to stop somewhere.

------------------------------------------------------------------------

# What Happens Inside Each Transformer : A Networking Event



In this section, we will get a high-level picture of what happens inside a transformer. It is a sequence of a lot of mathematical operations but in this article, I focus on the big picture for the most part and have not given explicit equations. At the end of the article, for those who are mathematically sophisticated, I have given all the equations together at once and connect them to whatever I will describe here now.

We saw earlier why the embedding of a word must depend on the context of the other words around it. But we also know that, in pinning down the exact meaning of a word in a sentence, not every surrounding word contributes equally to that meaning. Some words matter enormously to the meaning of a given word; others barely matter at all. Consider the following sentence again.

“`I deposit money in the bank`” *=\> ?*

The LLM is supposed to predict the next token. The following are some possibilites for the next token.

“`I deposit money in the bank.`” (full stop)  
“`I deposit money in the bank weekly`”   
“`I deposit money in the bank every`”

For predicting these next tokens with great accuracy, we have to now calculate the contextual embeddings for every word. From the context of what we have so far “`I deposit money in the bank`”, we already know that the meaning that the word “`bank`” takes is more certain and hence we have to change the point associated with this word “`bank`” in the embedding space to reflect that. We need context sensitive embeddings because the exact meanings of words changes in the context of a sentence.

Let us assume we have already done this so far for the words “`I`”, “`deposit`”, “`money`”, “`in`”, and “`the`”. We now have to compute the contextual embedding for the word “`bank`”. Let us see how an LLM does it. The component that does this job is called a **Transformer** and true to its name, it transforms positions of points associated with words in the embedding spsace. In determining the exact meaning of the word “`bank`” in the above sentence (whether it is a river-bank kind of bank or a financial institution or a vehicular manoeuvre), given whatever has come before, we see that the highlighted words only contribute in freezing the meaning and the degree of highlight signifies the degree of influence.

[](https://substackcdn.com/image/fetch/$s_!sDxH!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9b8eeea-ed12-45ef-a2a1-cadf98f458ad_1134x628.png)

![](https://substackcdn.com/image/fetch/$s_!sDxH!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff9b8eeea-ed12-45ef-a2a1-cadf98f458ad_1134x628.png)





We see that in determining the exact embedding of the word “`bank`” in the above sentence, the words like “`I`” and “`the`” are not at all important and should never be weighed in. The word “`in`” coming before “`bank`” is important and it freezes the meaning of the word “`bank`” to a noun of place but still it could be either a shore or a financial institution. The words “`deposited`” and “`money`” are the real heavyweights in influencing the exact meaning of the word “`bank`” and hence they should have a huge role in influencing the embedding coordinates of the word “`bank`” in the context of the rest of the sentence.

Consider “`I deposit money in the bank`” of six words (six tokens as well, assume that no words split up here). Assume that we have already found the contextual embedding of all the words in the sentence except the last one “`bank`”. The LLM has to decide that the word “`bank`” in this context refers to a financial institution and hence its embedding should move closer to those of other financial words.

Now, in order to imagine how the transformer finds the contextual embedding of the last word “`bank`” given those of all other words : Imagine the word “`bank`” as a person who is a guest going to a networking event that is happening in the embedding space !! In this networking event, the word “`bank`” has an already allotted seat (coordinates of the static embedding) but depending on which other words it gets along with (words closer to its contextual meaning), it wants to switch seats so that it can sit closer to the words that clarify its identity the most.

This is just a metaphor to have in mind in order to understand the big picture of what is happening. Imagine there is a party going on in the embedding space and the members “`I`”, “`deposit`”, “`money`”, “`in`”, and “`the`” have already been seated in their context appropriate seats given by their coordinates. Now, the new guy “`bank`” walks in and it already has a pre-alloted seat. But, in the context of the other people in the party (like “`I`”, “`deposit`”, “`money`”, “`in`”, and “`the`”), we would want “`bank`” to update and move to a seat closer to other words like “`deposit`”, and “`money`”. To facilitate this interaction process and the settling down of the word “`bank`” at the appropriate point in the embedding space, imagine this as a social networking situation with a sequence of protocols to be followed.

## Act 1 : The Social Phase



In this first phase, the word “`bank`”moves around and interacts with other words through these steps.

### Act 1 : Part 1 : Matching Queries and Keys



The word “`bank`” holds up an advertisement card called “**Query**” card that enlists what it is looking for from the other words in the party. It would read something like :

------------------------------------------------------------------------

**QUERY** Card for the word `BANK` : (ADVERTISEMENT)

I am a word with multiple possible meanings like river shore, money institution, or driving manoeuvre. I am looking for prepositions of place, financial verbs or action words that can help clarify my identity so that I can shift to a seat closer to where I belong !

------------------------------------------------------------------------

While the “`bank`” does this, every other word word member sitting in their seat also issue their resume cards (to give to the word “`bank`”) in the party which contains all the information that they have so that the new member “`bank`” can decide if he belongs near them. Let us call these resume cards carried by all the other five words so far by the name “**Key**” card and let us denote the key card of a word by the symbol. For each word, it would look something like :

------------------------------------------------------------------------

**KEY** Card for the word `DEPOSIT` : (RESUME)

I am a verb involving financial transactions and stored assets!

------------------------------------------------------------------------

Let us now see how the KEY cards for other words would look like.

------------------------------------------------------------------------

**KEY** Card for the word `MONEY` (RESUME)

I am a noun representing financial currency !

------------------------------------------------------------------------

Even small words can have powerful resumes to make in their bussiness cards.

------------------------------------------------------------------------

**KEY** Card for the word `THE` (RESUME)

I am a definite article who can make a noun specific.

------------------------------------------------------------------------

Note that the word “bank” also gives key to itself as well which tells how important its current seat is to itself (This may sound weird but yeah bear with this as I cannot think of a more simpler yet more accurate analogy!).

------------------------------------------------------------------------

**KEY** Card for the word `BANK` (RESUME)

I am a word that means a financial institution or a shore or a manoeuvre.

------------------------------------------------------------------------

Now, given that the incoming guest word “`bank`” has a **Query card** which contains the advertisement of what it seeks, and all the other words have their **Key** **cards** which contain what they have, the transformer algorithm compares and sees how much of a match does the word “bank” have with another word in the sentence so far.

With this, the compatability between the advertisement issued by the word “`bank`” and all the resume of all other words is computed based on comparing their **Query** and **Key** cards by seeing if what “`bank`” needs is intersecting strongly with another word as to what it has. With this, a sequence of weights are generated which tell how much the word “bank” is compatible with each word in the party so far.

[](https://substackcdn.com/image/fetch/$s_!LMDX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F045f9c58-1f36-4eeb-9d98-6c75cd654308_1536x1024.png)

![](https://substackcdn.com/image/fetch/$s_!LMDX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F045f9c58-1f36-4eeb-9d98-6c75cd654308_1536x1024.png)





### Act 1 : Part 2 : Collecting the Values



After this matching between queries and keys, the other words also show another third card that they have which contains the actual information about what they can contribute for the incoming word if they are weighed favourably with it. Let us call the name of this bussiness card as **Value** card. The value card of a word like “`deposit`” contains something like :

------------------------------------------------------------------------

VALUE Card for the word `DEPOSIT`

If I turn out to be relevant to you, here is the information I can contribute to your understanding : financial transaction

------------------------------------------------------------------------

Now, the word “`bank`” sees all the contributions (**Value**) by the other words in their Value cards, then looks at the weights computed with all of them (in the previous part), and then calculates the weighted sum of the combined advice given by each word from their **Value** cards.

[](https://substackcdn.com/image/fetch/$s_!ONyh!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a0f829e-f6e0-4d63-becf-26f0d30d8485_1536x1024.png)

![](https://substackcdn.com/image/fetch/$s_!ONyh!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a0f829e-f6e0-4d63-becf-26f0d30d8485_1536x1024.png)





> **Mathematical Note** : The Query/Value “cards” are written as if they
> contain legible English phrases (like “looking for prepositions of
> place” or “financial transaction”). In reality, these are just
> numerical vectors with coordinates (nothing that clean or labeled ever
> gets literally read out and it is only numbers and math that happen
> inside an LLM till the LM Head). I have described the contents for
> these query, key, and value vectors in words for explaining it for a
> lay audience. Matrices convert the embedding vectors into coordinates
> for the query, key, and the value vectors. The mathematical operation
> that is exactly happening when deciding the degree of compatibility
> between the query vector and the value vector is the **dot product**
> or the **inner product** followed by a normalisation. The dot product
> between the query and value vectors are normalised to give
> compatability and weightage to combine value vectors.

## Act 2 : The Private Room



So far, our networking-event metaphor has explained how the word “`bank`” gathers information from the other words in the sentence . Gathering context at a networking party is only half the battle. Once you finish talking to everyone, you need time to process what you just heard and think for yourself to decide finally where exactly to sit.

Imagine, therefore, that after the networking round, “`bank`” at the party temporarily retires to a small private thinking room. Inside this room, “`bank`” isn’t talking to any other words. It sits down privately to digest the aggregated information it has gathered after updating itself based on social interactions. So, “`bank`” now privately processes this newly gathered information. It has talked to each word separately and got cues but now it is able to feel the weight of all the surrounding words together which gives it the big picture that it would have never gotten just by talking to each of them one by one in the social event.

### Act 2 : Part 1 : Don’t Lose Yourself



Note : Suppose “`bank`” receives a huge amount of contextual information from “`deposit`” and “`money`”. We don’t want the representation simply to become some average of “`deposit`” and “`money`”. The “`bank`” is still a bank and has its unique identity. In technical terms, the Transformer uses what is called a **residual connection**. Instead of wiping out **bank's** original coordinates and replacing them with the average of its neighbors, it simply adds the new contextual advice to its existing identity:

To put in more detail : There is the weighted sum of all the coordinate information which the other guests think “`bank`” should move to. The transformer then adds that information to “`bank`”’s existing representation. That is, **“**`bank`**” does not abandon its old seat and blindly occupies a seat in the middle of a weighted sum of seats dictated by everyone else. Instead, it keeps its existing identity and adds to it, the contextual advice it has just received.**

Conceptually : old **“**`bank`**” +** contextual update **→** new **“**`bank`**”**

### Act 2 : Part 2 : The Combined Decision



The word “`bank`” should modify finally decide where to go and settle down based on what it has gathered so far from others. This is nothing but a mathematical function (final private deicision to decide where to move from where one is). It is a function because it takes a bunch of numerical coordinates of the information gathered and decides where to settle down finally which is also given by a bunch of numerical coordinates. A neural network can learn any function, as we saw in the previous article. In the actual Transformer, this special neural network that performs this private processing is called a **feed-forward neural network**, or sometimes simply an **MLP**. Thus, there is a useful broad distinction to remember: **attention is the social part of the Transformer, where words exchange information with other words; the feed-forward network is the private part, where each word processes the aggregate information it has acquired from everywhere.** This private processing is referred to in the tech world as being **nonlinear**. It isn't just taking an average; it's performing complex reasoning. It allows the model to synthesize combinations of clues. The combined presence of *"*`deposit`*"* and *"*`money`*"* triggers a more specific understanding that neither word could have evoked on its own.

The presence of a financial-transaction clue together with a money clue may be treated differently from either clue appearing alone. Different combinations and patterns in the gathered information can therefore produce different internal responses. This is the intuitive importance of **nonlinearity**. Nonlinearity means that private thinking is not restricted to merely mixing the information already obtained in different proportions. The network can learn transformations in which **particular combinations of features matter in their own right**.

> **Only for mathematically little mature folks** : If “`bank`” merely
> kept on repeatedly taking simple weighted mixtures of information from
> interacting separately with the words “`deposit`”, “`money`”, “`in`”,
> and the other words, the system would ultimately be limited to just
> increasingly elaborate forms of mixing and rearranging geometric
> information. Repetitions of weighed mixing simply give other weighted
> mixings with different weights. The nonlinear processing stage allows
> something richer to happen: the Transformer can learn complicated
> conditional transformations of the information it has collected. In
> our metaphor, “`bank`” does not merely count the opinions of everyone
> it met and average them together. It can **digest their combined
> implications**. The clues “`deposit`”, “`money`”, “`in`”, and “`the`”
> taken together can activate patterns inside the network that would not
> be captured simply by interacting and weighing each value
> independently. The private thinking room therefore transforms the
> information gathered by attention into a richer internal
> representation that can be useful for subsequent reasoning and
> prediction.

Once again, the **Transformer** does not simply discard what came before. The newly processed information is added back to the representation that entered the private thinking stage. Residual connections therefore reccur throughout the Transformer like pathways preserving continuity: every stage is allowed to contribute something new without being forced to reconstruct everything useful from scratch.

We should be careful not to push the metaphor too literally. Everything described above is performed through transformations of long lists of numbers whose behaviour has been learned during training. Nevertheless, the social metaphor captures the division of labour rather well: **attention (the social phase) gathers context from interacting separately with other tokens and weighing their values ; the feed-forward network processes that entire context within each token.** This metaphor will be useful to organise and explain the mathematics. The Transformer therefore repeatedly follows a beautifully simple rhythm:

**The Transformer Rhythm:**

1.  Talk to others (**Multi-Head Attention**)

2.  Keep what you have & add what you learned **(Residual Connection)**

3.  Think privately and digest after seeing everything together
    **(Feed-Forward Network)**

4.  Again, keep what you have & add your new insights **(Residual
    Connection)**

## Act 3 : Seeing Multiple Angles



There is another major simplification in the story we have told so far. We imagined “`bank`” carrying one Query card and comparing it with one Key card belonging to each of the other words. Real Transformers do something much richer. They conduct **several versions of this networking exercise simultaneously**.

Imagine that our networking event contains several parallel conversation rooms. In every room, the same guests : “`I`”, “`deposit`”, “`money`”, “`in`”, “`the`”, and “`bank`” : are present, but the Query, Key, and Value cards used in one room are different from those used in another. Consequently, “`bank`” might discover a very strong relationship with “`money`” in one room, a different relationship with “`money`” in another, and perhaps some grammatical or positional relationship with another word in yet another room. Each room therefore provides a different opportunity for the network to discover newer relationships between the same set of words. Imagine parallel room floors at the party where for example, Room 1 might focus on grammatical structure (linking prepositions to nouns), Room 2 might focus on semantic meaning (linking *bank* to *money*), and Room 3 might track pronoun reference.

Each of these parallel networking rooms is called an **attention head**. Because several such heads operate simultaneously, the mechanism in technical parlance is called **multi-head attention**. Instead of forcing two words to interact in just one way, multi-head attention lets the model evaluate word relationships across multiple perspectives at the same time. Afterwards, the findings from all rooms are merged back into the token's vector.

The essential idea is only that the Transformer is not forced to judge the relationship between two words in just **one single way**. It can examine their relationship through several independently learned perspectives at once (different types grammatical and semantical interactions)

After these parallel networking conversations have taken place, their results are brought back together, in a process called **concatenation**. Thus, “`bank`” does not emerge carrying only the result of one conversation. It receives the combined information produced by all the attention heads. This combined information then becomes part of its updated representation before it proceeds through the rest of the Transformer block for residual connection and feed-forward neural network.

------------------------------------------------------------------------

# Scaling Up



### The Whole Drama Happens Again: Stacking Transformer Blocks



We have now described something close to **one Transformer block**. The words enter with their current representations. Through multi-head attention, they selectively gather information from other words. Residual connections preserve what they already knew while adding this contextual information. Each word then enters its private feed-forward processing stage, where the gathered information is transformed nonlinearly, and another residual connection again preserves and enriches An LLM doesn’t stop after a single round of networking and private thinking. Modern models stack dozens of these Transformer units on top of each other. Think of it as taking an elevator up through a skyscraper. Imagine that the networking event has many floors. After completing the conversations and private reflection on the first floor, all the guests take an elevator to the second floor. Crucially, they do not arrive on the second floor as exactly the same people who entered the first. Their representations have changed.

After the first round performed on all words till now, the word “`bank`” has already absorbed contextual information from other words like “`deposit`”, “`money`”, “`in`”, and the other words. The word “`deposit`”has likewise acquired information from the words available to it before. Every token therefore begins the next round carrying a more updated contextual representation than it possessed before. Tokens enter with raw representations. They network, think, and emerge with basic contextual updates. Tokens now print new Query, Key, and Value cards using their updated representations now. They network again, finding higher-level relationships. The model is thus able to processes abstract concepts, nuances, and broad reasoning structures built on top of the lower floors’ insights.

And now something remarkable happens: **new Query, Key, and Value cards are produced from these already updated representations**, and the networking process starts again. Consequently, the second Transformer block is not merely repeating the identical calculation performed by the first just for fun. It is examining relationships between representations that have themselves already been contextualised by an earlier round of interaction. So, the Query, Key, and Value cards that they print in the second level would be more sophisticated than what they did in the first level. After the second level, they are transformed again. They then enter a third level, then a fourth, and so on through the many stacked Transformer blocks making up the LLM.

This repeated process allows increasingly complicated information to be built from simpler relationships. An early block might discover useful local relationships; later blocks receive representations in which those relationships have already been incorporated and can therefore build further patterns upon them to discover more global relationships. **Each successive Transformer block operates upon representations enriched by all the blocks before it.**

Let me give an example to illustrate this. Consider what happens if we take the following complex sentence : *“*`The old architect who designed a palace for the king suddenly retired.`*”*

When the word “`retired`*”* enters the networking event on the level 1 (the first transformer), it broadcasts an advertisement in its quert card : *"Looking for a human who can retire."* Looking back across the room, it immediately spots **two** valid human nouns that can serve as its subjects : the “`architect`” and the “`king`”. Both can grow old and both can retire. We know by our human linguistic intuition that it is the architect that is retired and not the king. But, the first transformer matches “`retired`*”* to both “`architect`” and “`king`” (mathematically, the dot products and the resulting weights for “`retired`” with “`architect`” and “`king`” are both high). But in the second level (second transformer), the representation of the word “`king`” is updated considering its interaction with the word “`for`” because the preposition “`for`” needs an object noun for which the word “`king`” matches with. In this second level, the representation of the word “retired” now interacts with the updated representations of the words “`king`” and “`architect`”. It is now able to realise that the word “`king`” has strong similarity with that of also the word “`for`” through its updated contextual representation and hence now, it knows that it is more likely to match with “`architect`” as its subject (rather than “king” which now is seen to have a strong correlation with “`for`”), as is reflected in the updated representation. Now, and only now in this second round of interactions happening in the second transformer, can the word `"retired"` confidently shake hands with the word `"architect"` while ignoring and moving away from “`king`”. The journey up the levels across the cascade of dozens of Transformers thus represents a transition from **identifying relations between pairs of words** to **understanding the global situation and context**.

In the first transformer, words figure out what kind of words they are and bundle with whatever can be their descriptive neighbors possible. In the middle levels, the model is able to do sophisticated things which have to do with determinng long-range relationships (like untangling nested clauses and assigning structural roles). In the top levels across the final batch of transformers, full awareness of the entire story emerges, enabling an accurate, context-rich next-word prediction.

### Parallel Networking



Our story about “`bank`” created one final deliberate illusion. For simplicity, we pretended that “`I`”, “`deposit`”, “`money`”, “`in`”, and “`the`” had already obtained their contextual embeddings and were sitting patiently in their seats when the newcomer “`bank`” entered the party. That was useful for understanding attention, but it is not quite how the computation actually proceeds.

During a Transformer layer, **all the word positions are processed in parallel**. *“*`Money`*”* asks about its neighbors at the exact same millisecond that *“*`bank`*”* asks about its neighbors. The “`bank`” asks which available words matter to it, but at the same time “`money`” is asking which words matter to “`money`”; “`deposit`” is asking which words matter to “`deposit`”; and so forth. It is as though every person at the networking event simultaneously holds up a Query card while simultaneously displaying Key and Value cards to everyone who is permitted to see them. The Transformer can therefore calculate an enormous collection of relationships between words at the same time rather than moving laboriously through the sentence one word after another. But, there is just one constraint here.

## Constraints



### Causality



However, when predicting text left-to-right, words are not allowed to look into the future. When processing the word *“*`money`*”*, the model uses what is called as a **causal attention mask** : a one-way privacy screen that lets the word to interact with only words that occur before it in the sentence (what has already been written by the time the given word was written), but blocks them from peeking ahead at words yet to come. There is therefore an important terminology point. Because, no word can depend on the word following it to update its context in the same iteration.

A word is not allowed to cheat by obtaining information from words that occur **in its future**. In our sentence, when processing “`money`”, the model may use information from “`I`”, “`deposit`”, and “`money`” itself, but it cannot peek ahead at “`in`”, “`the`”, or “`bank`”. When processing “`bank`”, all the preceding words are available because they have already occurred in the text. This restriction is implemented by what is called a **causal attention mask**. In our party metaphor, everyone may network simultaneously, but there are one-way privacy screens: **each guest may look backward at the guests who have already appeared in the sentence, but cannot look forward at guests from the future.** Otherwise the LLM would be learning to predict words while secretly being allowed to see the answers.

### Position Embedding



There is one final ingredient that our networking event needs. Imagine that all the words entered the room wearing name tags but carried no information about where they occurred in the sentence. Then the party would contain the right guests, but crucial information about their arrangement would be missing. Language depends not merely upon **which words are present**, but upon **where they occur and how they are ordered**. “`Dog bites man`” and “`Man bites dog`” contain the same three words but certainly do not mean the same thing. The succession of words matter in a sentence (what comes before and what comes after) but also the exact position of words also matters (which comes first and which comes third). Otherwise, as we saw, the sentences *"*`Dog bites man`*"* and *"*`Man bites dog`*"* would look identical to the model. To prevent this, every token enters the party carrying a **positional tag** attached to its name badge. Modifications are performed to it depending on what position it is with respect to a running input of words. This ensures the attention calculations account for distance and word order, not just word identities. There are different kinds of positional based modifications possible depending on the exact mathematical operation performed and we will not go into much detail into it here. This is called in technical parlance by the term “**position embedding**”.

Thus, we see that since the Transformer therefore needs information about position as well as word identity, we should have that every guest enters the networking event carrying not merely a name badge saying “`bank`”, “`money`”, or “`deposit`”, but also some information indicating **where that guest appeared in the sequence**. As said, modern LLMs have different mathematical ways of representing positional information, and we need not enter those details yet. What matters for our metaphor is that the Transformer is never dealing merely with a bag of words floating timelessly around a room. Its computations have access to information about the structure of the sequence, allowing relationships to depend upon order and distance as well as upon the identities of the tokens themselves.

And after the initial position based update and many such rounds of transformer levels, the representation of “`bank`” is no longer merely the context-free representation with which the word entered the model. It has become a deeply contextual representation of **this particular occurrence of** “`bank`”**, in this particular sentence, surrounded by these particular words**. That richly contextualised representation is what the later stages of the LLM can ultimately use to help decide what token should come next. We should therefore not imagine an LLM as containing hundreds of completely separate “Transformers.” Rather, the **Transformer is the overall architecture**, and its central body contains many stacked **Transformer blocks**, each repeatedly updating the context sensitive representations by variations of the networking-and-private-processing cycle we have just described.

To summarise what happens in the entire sequence, we have the important technical terms in the various steps summarised :

**Attention**:  
Which other words should “`bank`” listen to?

**Query/Key**:  
How does it decide how much to listen to some word?

**Value**:  
What information does it take from them?

**Residual**:  
How does it learn from them without losing itself?

**MLP**:  
What does it do with everything it has learned?

**Multi-head Attention:**  
Why have only one sets of weights in just one conversation? Divide and Conquer.

**Stacking**:  
Why do all this only once? After everyone has updated their positions after considering multiple weights across multiple dimensions, learning and processing from all of each other, why not let them interact and make them repeat this entire process again?

**Causal masking:**  
How can everyone interact in parallel without cheating by looking what words comes after it ?

**Position**:  
How does anyone know where everyone stands in the sentence?

To summarise : *A Transformer alternates between two kinds of computation: communication and computation. Attention lets tokens communicate with other tokens; the feed-forward network lets each token compute privately on what it has learned. Stack this communicate–compute cycle many times, and increasingly rich contextual representations emerge.*

------------------------------------------------------------------------

# Training : Fill-In-The-Blanks



As seen in the previous article, how are the various weights and matrices in all the transformers, and also the P and Q matrices, decided? The approach is the same as that of training for static emdeddings described in the previous articles. Initially, all these paramaters are chosen randomly. Take a large training corpus of linguistic data and choose some successive words w₁, w₂, .. , w_(n). Try to predict the probability distribution for the next word w_(n+1) (imagining a single blank after the given words). From the training corpus, one already knows the probability distribution for the next word w_(n+1). By seeing the mismatch between the predicted and actual answers in probabilities, all parameters of the LLM are updated in a manner so as to improve the accuracy in prediction for the known cases from the training data. One then as usual hopes that this sufficient training is enough for it to learn and predict the next word for the random input prompt not encountered in the training data.

------------------------------------------------------------------------

# The Gory Math Behind LLM : For the Brave



If you are bold enough to see the mathy equations behind the LLM in all its full gore, then this last section is for you. Even if you are not a mathematics person, you can just see them (no harm in seeing something right??!!). I have breaken everything down in terms of the metaphor that we have now used so far. The equations and notations are taken from this wonderful paper which can be accessed by clicking [here](https://www.crc.business-school.ed.ac.uk/sites/crc/files/2026-02/Mathematics_of_LLMs_2026.pdf).

[](https://substackcdn.com/image/fetch/$s_!vAzi!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd21fd13-32ed-4569-8428-ab21e9f6b556_1368x1100.png)

![](https://substackcdn.com/image/fetch/$s_!vAzi!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdd21fd13-32ed-4569-8428-ab21e9f6b556_1368x1100.png)





------------------------------------------------------------------------

I intend to write a lot more articles on LLMs for various other applications. In this article, we have focused only on generative LLMs. There are lot more applications like machine translation and classification about which I intend to write about in the future. There are also more complex topics like multimodal LLMs, embeddings of contexts, etc about which also I intend to write about in future. But, I hope this series of two articles have given you the big picture and demystified the inaccessibility of probing into LLMs.

------------------------------------------------------------------------

#### Subscribe to Rama’s Substack

By Rama Seshan Chandrasekaran · Launched a year ago

My personal Substack

Subscribe

By subscribing, you agree to Substack's [Terms of Use](https://substack.com/tos), and acknowledge its [Information Collection Notice](https://substack.com/ccpa#personal-data-collected) and [Privacy Policy](https://substack.com/privacy).

[](https://substack.com/profile/8005438-ashok-viswanadha)

![Ashok Viswanadha's avatar](https://substackcdn.com/image/fetch/$s_!Taxq!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F653e1cdb-a6bc-4605-8527-bad6b59b34ce_400x400.png)

[](https://substack.com/profile/12628538-ankit-pandey)

![Ankit Pandey's avatar](https://substackcdn.com/image/fetch/$s_!o5PL!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc519df11-a023-4966-aa09-c6089d47bf01_96x96.jpeg)

[](https://substack.com/profile/5275863-henadologia)

![Henadologia's avatar](https://substackcdn.com/image/fetch/$s_!bWI0!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcd0c4051-66cc-4559-9953-1ff90f9e2503_710x710.jpeg)

[](https://substack.com/profile/284920280-ravinder-reddy)

![Ravinder Reddy's avatar](https://substackcdn.com/image/fetch/$s_!2Tvm!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77da9531-28fb-41f8-b757-599e5b73f4c6_1202x1204.png)

[](https://substack.com/profile/159472567-vaitheeswaran-lm)

![Vaitheeswaran L.M's avatar](https://substackcdn.com/image/fetch/$s_!3r0z!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F558d7e99-519b-4271-a911-e1a09727a0f2_96x96.png)

25 Likes∙

[5 Restacks](https://substack.com/note/p-210785774/restacks?utm_source=substack&utm_content=facepile-restacks)



25



7



5

Share
