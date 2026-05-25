+++
title = "The computing genius of"
full_title = "The computing genius of Pāṇini An introduction"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/the-computing-genius-of-panini-an"
date = "2025-10-28"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/the-computing-genius-of-panini-an).

The computing genius of Pāṇini : An introduction

# The computing genius of Pāṇini : An introduction

### In this article, I introduce the reader to the depth and genius of the Pāṇinian grammatical tradition of ancient India and relate it to modern developments in programming and formal language theory.

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Oct 28, 2025

11

4

3

Share

This article is a surface level panoramic introduction to **Pāṇinian** grammar of the Sanskrit language, as presented in his treatise **Aṣṭādhyāyi**. In trying to characterise the grammar of the Sanskrit language spoken in his day, Pāṇini Maharṣi manufactures legitimate and only legitimate words of the Sanskrit language, by designing a set of 4000 rules in a highly compressed language of the sūtra that operates on the sounds, verb roots, prefixes and suffixes, to generate all the words of Sanskrit language.

[](https://substackcdn.com/image/fetch/$s_!erMI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42c24017-8fd4-4e02-a4f1-5fc0b94eb6d6_1200x630.webp)

![Dimensions of Pāṇinian Grammar Explored, Part 4 - The Light-Before-Heavy Principle](https://substackcdn.com/image/fetch/$s_!erMI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42c24017-8fd4-4e02-a4f1-5fc0b94eb6d6_1200x630.webp "Dimensions of Pāṇinian Grammar Explored, Part 4 - The Light-Before-Heavy Principle")

In this process, **Pāṇini** uses techniques from modern computing (especially the theory of formal languages that are used in analysis and compiler design for programming languages) and anticipates them even though it would be 2500 years from his time when the first actual computer would be invented. Techniques like optimal ordering of data, information compression, metalanguage, metarules, use of non-terminal symbols, light before heavy are all used in this masterpiece.

To study the Aṣṭādhyāyi, it is essential to know the Sanskrit language, as that is the language for which the grammar is designed. However in this series, my aim is to introduce how Pāṇini uses these techniques in his treatise for people who don’t have any knowledge of the Sanskrit language, or formal language theory in computer science.

Language was an important concern in ancient Indian philosophy, especially for the Āstika schools, as they believed that the efficacy of the Vedic rituals directly depended on the sounds of the chanted mantras. They wanted to justify how this efficacy is brought about, and in the process, they had to analyze how the sounds of a language relate to meaning and ultimately reality itself. By the end of this series, you will have a deep appreciation of the importance, depth and scope of Aṣtādhyāyi and the Indian views on language.

# **A Fruit Market**

Let’s imagine that you are in a fruit market, wanting to buy a bunch of fruits. You see a list of fruits that is available there as follows:

- Mango

- Apple

- Orange

- Pineapple

- Strawberry

- Jackfruit

- Guava

- Pomegranate

- Litchi

- Lemon

- Blueberry

Luckily, let’s say that the fruits that you want to buy are:

- Pineapple

- Strawberry

- Jackfruit

- Guava

- Pomegranate

Now, you see that the fruits that you want are all together consecutively in the list - the list is shown here again with the fruits you want in bold.

- Mango

- Apple

- Orange

- **Pineapple**

- **Strawberry**

- **Jackfruit**

- **Guava**

- **Pomegranate**

- Litchi

- Lemon

- Blueberry

One way of saying what you want from the vendor is to name the fruits that you want sequentially. But now you realize that the list is displayed and the vendor can see it clearly. So, instead of saying I want “pineapple, strawberry, jackfruit, guava and pomegranate”, you can save some time and her short term memory by saying that In that list displayed, I want the fruits “**from** pineapple **to** \*pomegranate”. This not only saves little time but the vendor can also get relieved of her short term memory - she can just remember the initial fruit (pineapple) and the final fruit (pomegranate) in the list and she can use the list as reference and pack all the fruits in between.

So what? - you might ask. But imagine instead of some dozen fruits, you are a computer scientist and are dealing with an array (a fancy name for list in computer programming) with 10,000 entries. And you want to pick up a hundred of them for doing some operation. And it happens that those hundred elements fall in a nice order and are one by one in the array by luck. Then, as a computer programmer, obviously you would code in such a way that you ask the computer to pick up using the “**from** here **to** here” style rather than saying all the numbers of all the entries. In this case, this would save immense computing power.

Now, suppose that in the same fruit shop, next time you want the following:

- Mango

- Orange

- Guava

- Lemon

These fruits are shown bolded in the entire list below:

- **Mango**

- Apple

- **Orange**

- Pineapple

- Strawberry

- Jackfruit

- **Guava**

- Pomegranate

- Litchi

- **Lemon**

- Blueberry

Note that this time you are not so lucky. You can’t simply say to the vendor that you want fruits from mango to lemon. It will include so many unnecessary fruits that you do not want. The poor vendor has to remember your requirements individually, and pick up and hand it over to you. You can extrapolate this scenario to the computer programming example.

Now suppose the list of fruits in the shop was reordered as follows:

NEW LIST:

- Apple

- Pineapple

- Strawberry

- Jackfruit

- Pomegranate

- Guava

- Mango

- Orange

- Lemon

- Litchi

- Blueberry

Now let’s consider both of your orders:

Order first time: Pineapple, Strawberry, Jackfruit, Guava, Pomegranate.

Order second time: Mango, Orange, Guava, Lemon.

Now, with this new list, you can make both the orders in the initial-final way because both of the list of fruits fall sequentially one below the other in the list. Let me bold the fruits in both the orders in the new list. It is shown below:

NEW LIST:

- Apple

- **Pineapple**

- **Strawberry**

- **Jackfruit**

- **Pomegranate**

- **Guava**

- **Mango**

- **Orange**

- **Lemon**

- Litchi

- Blueberry

Now you can make both orders as follows in this new list:

Previous order - From Pineapple to Guava in the new list.

Present order - From guava to lemon in the new list.

> **So, you see how the appropriate ordering of entries in a list
> matters a lot. If the fruit shop owner is clever, he will perform a
> statistical analysis and collect the most frequently ordered sets of
> fruits and rearrange the list of fruits in such a way that as many
> frequently ordered sets of fruits can be done so by the initial-final
> way. A computer programmer analogously will write a code to reorder
> the elements of an array such that as many frequently called upon
> entries can be called in the initial-final way to save his future
> programming time.**

# **When Words Do Double Role Playing : Grammaticalisation**

What is the meaning of the English word have?

- I **have** this book.

- They **have** a beautiful voice.

- I **have** two children.

- Our group of restaurants **have** bulk orders on Sundays.

We see that the meaning of the word “have” in the above sentences is something concrete and means possession or association. Even dictionaries tell only this meaning. Check any dictionary. But consider these sentences.

- I **have** ***written*** this book.

- I **have** ***finished*** my homework.

- They **have** ***stolen*** my car.

In these sentences above too, the word “have” occurs. But they don’t convey any meaning of possession there - right? When I say “They have stolen my car” , I am not implying that they own the car - the sentence itself says it is clearly my car! So, what is happening to the word have in these usages?

A native English speaker wouldn’t even be aware of this and still continue to use the language appropriately from his instincts. But an adult learner who learns English would go crazy confused seeing these pairs of sentences - he would be clueless.

Since you have studied (or were forced to study) grammar at school, you realize that the word “**have”** in a sentence like “*They have stolen my car*” does not have its literal meaning to possess. Instead, it combines with the following verb “stolen” and conveys an abstract idea - the idea of a present perfect tense - an action that has been completed very recently from the present. So, the word “have” here loses its literal meaning and instead conveys an abstract grammatical information with the succeeding verb. It informs us that the verb following it is of a present perfect tense - an action that has just been recently completed (i.e. the car has just been stolen by them).

If you had paid even more attention to your high school grammar class, you would recall that the word “have” is now acting as an **auxiliary verb**. An auxiliary verb is a word that was originally a verb (Eg. I have this book) but has lost its literal meaning and is now acting in communion with another verb to convey an abstract grammatical information about the verb that follows it (Eg. They have stolen the car).

English has other auxiliaries too. Take the word “do” and the sentence “I **do** this everyday”. Here, the word “do” is a normal verb that signifies action. But in a sentence like “I **do** ***read*** books everyday” - the word “do” has lost its literal meaning and has now combined with another verb (e.g. “read”) to convey an emphatic meaning for the verb that follows. The difference between the sentences “I read books everyday” and “I **do** read books everyday” is that the latter sentence is more emphatic.

Consider the word “will” that can be used as a noun with concrete meaning as in a sentence like “Where there is a **will**, there is a way”. Here, “will” is a normal noun that means desire or intent. But in the sentence “I **will** ***read*** that book”, the word “will” has lost its literal concrete meaning, has combined with the verb that follows it, and conveys an abstract grammatical information which is that the verb is in the future tense.

Such a phenomena in which a word loses its concrete meaning (referring to a thing or an action) and instead is hijacked to convey an abstract grammatical information (like tense / emphasis) is called in linguistics as **grammaticalization**. You might think that this grammaticalization exists only in English, but it abounds in all languages - just that we are not trained to explicitly recognise this phenomenon, and we do so only when we try to learn another language as an adult logically.

Let me give some examples from Hindi.

Consider the following verb root रह (rah). This has a concrete meaning which is to remain, to stay. Consider the following sentences where it is used in this concrete sense.

मैं अपने घर में **रहता हूँ** (mein apne ghar men rahtā hūn)  
(Meaning: I **stay/remain** in my house)

आपका छात्रावास में **रहना** अत्यवश्यक है (āpkā chātrāvās men rahnā atyavashyak hai)  
(Meaning: You **staying** in the hostel is very important)

But this verb does indeed get hijacked and loses its concrete meaning in sentences like

मैं हिंदी सीख **रहा** हूँ (main hindī sīkh **rahā** hūn).

If you literally translate this sentence into English, it would be “*I remained learnt Hindi*” which is absurd. Instead if you are a native Hindi speaker, you know that this sentence above instinctively means “*I am learning Hindi*”. In other words, the verb root रह (rah) has lost its concrete meaning and now conveys the grammatical information of continuous tense (an action that is in the process).

The difference between मैं हिंदी सीखता हूँ and मैं हिंदी सीख **रहा** हूँ is that मैं हिंदी सीखता हूँ means “*I learn Hindi*” while मैं हिंदी सीख **रहा** हूँ means “*I am learning Hindi*” (in the process). So, the root रह has lost its original meaning of stay/remain and is now hijacked by the language to convey the grammatical information of the continuous tense.

Another verb that famously gets hijacked is the verb root जा. As a concrete verb, it means to go as in sentences like -

मैं हर दिन विद्यालय **जाता** हूँ (mein har din vidyālay jātā hūn)  
(Meaning: I **go** to school everyday)

But this verb gets hijacked a lot of time to convey the grammatical meaning of passive voice. Examples:

शतरंज लड़कों द्वारा खेला **जाता** है (shatranj laṛkōn dvārā khēlā **jātā** hai)  
(Meaning: Chess is played by the boys)

Here, the word **jātā** has completely lost any meaning of going. It simply conveys the grammatical information of passive voice. The difference between लड़के शतरंज खेलते हैं *(the boys play chess)* and शतरंज लड़कों द्वारा खेला **जाता** है (*chess is played by the boys*) is that the latter sentence with **जाता** transforms the sentence from active voice to passive voice. There is no connotation of any motion or going in the latter sentence. Auxiliary verbs abound in Hindi - much more than in English. As an exercise, try to recognise more.

So, now you are used to a word meaning two different things - a concrete meaning in one situation and an abstract grammatical meaning in another situation. As a native speaker of a language, your neurons are wired by exposure in childhood to seamlessly tell in sub-second time, what meaning is intended, given the syntax. When I learnt Hindi, during the initial stages, these double meanings of the verbs rah and jā confused me a lot until I picked up a grammar book.

# **Pāṇini’s Sandhi Problem : Optimal Ordering & Metalanguage**

You might ask, What do all these have to do with Pāṇinian grammar and Sanskrit? Well, Pāṇini had to write a grammar for the Saṃskṛta language of his day and place (he was based in ***Śalātura***, close to modern day Lahore in Pakistan). Many people have written many grammar books for their languages, but Pāṇini’s work is not a grammar book like that of Wren & Martin. His is actually a code - kind of like a computer program. He wanted to design a machine that would take as its input - his verb roots, prefixes and suffixes - and based on his rules - combine them and create legitimate words of the Saṃskṛta language. In other words, he wanted to automatize and imagine word formation in Sanskrit as a factory process. The raw materials that he gives to the factory are verb roots, prefixes and suffixes. The factory process control algorithm he uses are the sūtras of his work called the Aṣṭhādhyāyī. If it was a computer, the algorithm could be stored in a ROM. But Pāṇini’s code was supposed to be stored in the minds of people and transmitted orally across generations - it was to be stored in actual memories of the people. But you know human memory is limited and tends to forget, and hence he needed to write a code for his algorithm (in sūtra format) in a highly compressed language so that it could be memorized in a brain in reasonable time. So, he had to do severe information compression for his algorithms while coding them down as sūtras. This is where the fruit market example and contextual based hijacking of words comes into play.

Pāṇini was facing the same problem as a fruit vendor. There is a phenomenon called **sandhi** in Sanskrit wherein final sounds of a word change so as to accommodate well with the beginning sound of the word that follows it. For example, no language in this world tolerates two vowels coming together at word boundaries - they avoid it by some or the other means.

Example: **a book** (OK in English) but **an egg** (not OK in English). Why? Because there is a succession of two vowels a-e in the phrase **a egg**! English avoids this vowel-vowel hiatus by inserting a consonant in between - it chooses N - and hence we have **an egg**! So, the addition of N to change a to an is actually a sandhi in English. Both aanand an are exactly the same as far as meaning is concerned - indefinite articles. Just that “an” is a sandhi adjusted form of “a” to avoid a vowel-vowel hiatus when the word following the article also begins with a vowel. Sanskrit speakers were very conscious of these sound changes happening at boundaries since their language flourished in a mostly oral culture and hence minutely noted these changes. Sanskrit however follows a different strategy to avoid a vowel-vowel hiatus. When the vowel that ends the first word is इ/उ/ऋ/ऌ (i/u/ṛ/ḷ), then instead of inserting a consonant, the initial vowel itself converts into its appropriate semi-vowel consonant य्/व्/र्/ल् (y/v/r/l). These transformations are:

- इ =\> य् (i=\>y)

- उ =\> व् (u=\>v)

- ऋ =\> र् (ṛ=\>r)

- ऌ =\> ल् (ḷ=\>l)

Examples:

- प्रति + उषा = प्रत्युषा (prat***i*** + uṣā = prat***y***uṣā)

- सु + आगतम् = स्वागतम् (s***u*** + āgatam = s***v***āgatam)

- मातृ + अंशः = मात्रंशः (māt***ṛ*** + aṃśaḥ = māt**r**aṃśaḥ)

So Pāṇini wanted to actually say that

> If an (इ/उ/ ऋ/ऌ i/u/ṛ/ḷ) is followed by any other vowel, then replace
> (इ/उ/ ऋ/ऌ i/u/ṛ/ḷ) by (य्/व्/र्/ल् y/v/r/l)” respectively.

Pāṇini could not afford to say this in so many words - he was not writing a book but rather composing orally transmittable texts. He had 4000 sutras (lines of code) and he wanted each line to be as compressed and brief as possible. So to compress them, Pāṇini uses two strategies:

1.  Creating an efficiently arranged list of sounds to call upon the
    list of sounds that he wants to call on easily using the
    initial-final way (reminds you of the fruit basket problem?!)

2.  Hijacking the normal meaning of small grammatical case endings in
    the Sanskrit language and using them to convey algorithmic
    transformations of sounds (sounds like the grammaticalisation
    problem?!!)

Note that Pāṇini not only had to call the group of sounds like (i,u,ṛ,ḷ) and (y,v,r,l) but also dozens of other groups of sounds for other sandhis and other purposes as well. So this is exactly the fruit vendor problem and what he did was exactly what we had said there also - create a well ordered list so that the required groups of sounds to be called, fall consecutively and hence can be summoned by just saying the initial and final sound (with the implicit understanding that sounds in between are also included).

Pāṇini did arrange the sounds of Saṃskṛta in such a list, and it is called the **Śivasūtras** because he believed that these sounds originated from the drum of Lord Shiva. The list is:

- अ इ उ **ण्** \| a i u **ṇ**

- ऋ ऌ **क्** \| ṛ ḷ **k**

- ए ओ **ङ्** \| e o **ṅ**

- ऐ औ **च्** \| ai au **c**

- ह य व र **ट्** \| ha ya va ra **ṭ**

- ल **ण्** \| la **ṇ**

- ञ म ङ ण न **म्** \| ña ma ṅa ṇa na **m**

- झ भ **ञ्** \| jha bha **ñ**

- घ ढ ध **ष्** \| gha ḍha dha **ṣ**

- ज ब ग ड द **श्** \| ja ba ga ḍa da **ś**

- ख फ छ ठ थ च ट त **व्** \| kha pha cha ṭha tha ca ṭa ta **v**

- क प **य्** \| ka pa **y**

- श ष स **र्** \| śa ṣa sa **r**

- ह **ल्** \| ha **l**

This is the list that Pāṇini created and credited to Lord Śiva. There is only one difference between this and the fruit list. The last sound in each line (shown bolded) which are pure consonant sounds (with no inherent vowel attached) together are called mute letters and are not a part of the list and hence excluded in any enumeration. Only letters with the inherent vowel an are part of the list (black letters). Why would Pāṇini add these mute bolded letters anyway? Wait till the next section. Pāṇini is a genius. Everything he does has amazing foresight and reason behind it.

How efficient is this ordering of letters in the Śivasūtras for the groups of sounds that Pāṇini wants to refer to? For the collection of letters he wants to refer to, this ordering is the most optimal, as per the analysis done by the mathematician Wiebke Petersen in his paper [here.](https://link.springer.com/article/10.1007/s10849-004-2117-7)

[](https://substackcdn.com/image/fetch/$s_!g4mf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdf89b726-6c17-4a16-bb7b-66b5c284482e_1080x1463.jpeg)

![Image](https://substackcdn.com/image/fetch/$s_!g4mf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fdf89b726-6c17-4a16-bb7b-66b5c284482e_1080x1463.jpeg "Image")

Now, seeing this list, for the Sandhi rule we saw earlier, recalling it:

If an (इ/उ/ ऋ/ऌ i/u/ṛ/ḷ) is followed by any other vowel, then replace (इ/उ/ऋ/ऌ i/u/ṛ/ḷ) by (य्/व्/र्/ल् y/v/r/l) respectively.

Now, hence we need to call three sets of sounds for this Sandhi rule:

1.  First set - the four vowels **(इ/उ/ऋ/ऌ i/u/ṛ/ḷ)** that precede

2.  Second set - the set of all vowels that can follow

3.  Third set - the four consonants **(य्/व्/र्/ल् y/v/r/l)** that are going
    to replace the vowels in 1.

Seeing the **Śivasūtra** list above, the three sets can be called as:

1.  **इक् ik** (set of all sounds in the list from **इ** to **क्**
    excluding the bold letters)

2.  **अच् ac** (set of all sounds in the list from **अ** to \**च् \**
    excluding the bold letters)

3.  **यण् yaṇ** (set of all sounds in the list from **य** to **ण्**
    excluding the bold letters)

If you collect the sounds as directed above from the list (Śivasūtras), you will end up with the exact set of sounds that you want for the rule in the same order! So, the rule can now be compressed somewhat as:

> When an **इक् ik** letter is followed by an **अच् ac** letter, replace
> the **इक् ik** letter by its corresponding **यण् yaṇ** letter

But Pāṇini is not happy with this level of compression - he wants to further compress the conditional statements and the replacement rule also. For that, we need to take a slightly congruent detour of the grammatical case endings of Sanskrit nouns and adjectives.

The words **जागत् jagat** and **मरुत् marut** in Sanskrit mean “world” and “wind” respectively. In the normal Saṃskṛta language, the following endings change the meaning as follows:

- **जागत् \| jagat** = the world

- **जगतः \| jagataḥ** = **of** the world

- **जगति \| jagati** = **in/on/at** the world  

- **मरुत् \| marut** = the wind

- **मरुतः \| marutaḥ** = **of** the wind

- **मरुति \| maruti** = **in/on/at** the wind

So, we see that in normal language, for words ending in consonant, the ending **aḥ** conveys the meaning of “**of”** and the ending “**i”** conveys a sense of location as conveyed by a preposition like **in/on/at**. But these prepositions are the meanings of the ending in the unhiijacked Sanskrit language in normal usage! Oh my god - what Pāṇini does now would be unbelievable! He will now hijack these case endings and use it for his special operations in the sūtras!

What Pāṇini does here is this. He indirectly declares something like:

“Grammarians, forget what the endings **aḥ, i** mean in our normal Sanskrit language. As far as my sūtras are concerned, they will stand for these operations:”

1.  **aḥ =\>** this will stand for the group of sounds that precede and
    need to be replaced.

2.  **i =\>** this will stand for the group of sounds that follow.

3.  no ending =\> this will stand for the group of sounds that replace
    the first set of sounds.

> Pāṇini hijacks the normal Sanskrit language (at least some part of
> it - the grammatical case endings) for his coding purposes - in
> computer jargon - this is called **metalanguage!** Pāṇini is
> essentially creating a metalanguage out of a natural language
> (Sanskrit) for his coding purpose!!!!

Isn’t this genius!

In case of auxiliary verbs, a word gets hijacked within the natural language itself to convey certain other abstract grammatical purposes - Pāṇini now hijacks some case endings of the language - strips them of their normal meaning - and encodes them with a new instructional meaning as far as the context of his sutras are concerned!! This is the essence of what a metalanguage is.

So, in this elegant meta-language and the well-ordered list of sounds in the Śivasūtras, this rule can be summarized elegantly as:

> Final rule in its fully compressed form : इकः यण् अचि \| ik***aḥ*** yaṇ
> ac***i***

- Literal meaning of the Sutra: Of IK, in AC, yan (does not make any
  sense)

- Actual meaning when interpreted in the meta-language of the sutra:
  Whenever an “ik” sound is followed by an “ac” sound, replace the “ik”
  sound by its corresponding “yaṇ” sound

So we see how an elaborate set of Sandhi rules has been so efficiently compressed to a very small statement “ikaḥ yaṇ aci” using optimally ordered lists and meta-language. This meta-language will be useful throughout the language because Sanskrit is a left-changing language predominantly - that is when two sounds meet, mostly it is the first sound that gets replaced while the second sound stays put. So, this meta language of **aḥ** denoting both the first sound and the sound that needs to be replaced is useful across all operations concerning the language.

Now, we will see what those bolded/underlined letters are doing in the Śivasūtras and also more sophisticated metalanguage. Gradually, we will see other concepts.

# Shopping in a bookstore

We went to a fruit shop to demonstrate the concept of optimal ordering. This time, we will consider shopping in a bookstore to demonstrate another mathematical al problem. We will see that managing a bookstore efficiently requires more than optimal ordering. Imagine that you are the owner of a bookstore that sells a particular genre of books - say literature. Imagine that your bookstore is a bunch of linear arrangements of books in just one direction - left to right. For some reason, your shop has a lot of length but only a small width - so you can afford only a single large shelf that goes from left to right. This may be weird, but it will be most helpful when you later connect it to computer science (arrays) and Pāṇinian grammar. To be more precise, imagine all of the books that you want to sell are arranged in an array - one after the other, from left to right, as shown below.

> Book 1 - Book 2 - Book 3 - Book 4 - Book 5 - and so on.

For an efficient shopping experience for your customers, you do realize that there should be an efficient ordering of the books involved - as in the fruit shop case. But the problem is that books carry more information than a fruit. There are so many criteria that one can use to efficiently order the books. Some of them are enumerated below.

1.  One can arrange the books in alphabetical order of their authors.
    This will enable people who are shopping for books of specific
    authors to find what they want easily.

2.  One can arrange the books starting with the most recent releases, to
    the book that is released the oldest. This can enable people who are
    exploring for new releases and selecting on the spot very much. This
    will also enable people who are exploring select vintage books.

3.  One can arrange the books in terms of increasing price. This can
    enable people who are shopping randomly and are open to any book but
    come with specific budget constraints.

4.  One can arrange books by genre: fiction, fantasy, classic,
    self-help, etc. This is also another useful idea. Within a given
    genre, another criteria from the above options can be used to order
    the books within that genre.

We see that number 4 is the most efficient way; but that still leaves a question, how to order the books within a given genre? Should we follow 1, 2, or 3? Whatever we do, we realize that we can choose only one and cannot make everyone happy. Within a given genre, if we arrange by the alphabetical order of the author’s name, then people who shop for specific author’s books will be very happy to search, but people shopping by other criteria like recentness and budget constraints will be sad.

What do we do then? We could adopt this solution: We can do the arrangement via author’s name; but to satisfy the budget customers, and customers who have the recentness of the books they shop for in their mind, we can attach a tag from every book that has the price info and the month and year of release. For example, we can attach a big tag from every book that displays something like:

## **02-2023, Rs 435**

This can easily convey that the book was released in Feb 2023 and costs Rs 435/-. A budget customer can keep looking at these tags for the price, instead of taking out each book and looking inside for the price. So he can take out and explore only those books within his price range. This will save some time for him (although not as ideal as the option number 3).

Now, there is an important thing. This tag is useful only until you select the book. This is only to facilitate shopping and selection. The information in the tag is not a part of the book. Once you purchase the book, you will throw it away (like you throw away the tags in your clothes once you purchase them - the tags are not a part of a cloth and are there only to facilitate the shopping experience). **So notice that the tag is not a part of the book.**

## **A Little Computer Science**

I myself am not a computer programmer - do not worry if you also are not one. I will just give a barebones introduction to an extremely simple computational problem in the area of formal language theory, in an easily understandable manner so that one can appreciate what Pāṇini did, which will come up in the next section. Let’s say, someone states that you should display on your screen the following list of strings (a string is a collection of letters that need not have any meaning in any language):

AC  
AACC  
AAACCC  
AAAACCCC  
AAAAACCCCC  
upto 10,000 iterations.

You might ask initially, what is the point of this exercise? I have chosen a very simple problem to convey a point here, even though it might not seem that practically relevant. Obviously I have to generate 10,000 strings of this type, made of equal numbers of the letters A,C in equal numbers. One way to do this is to type these strings one-by-one manually onto the screen. But come on, you will realize that is inefficient, straightaway. Now, let me write an algorithm for a computer to follow:

> Step 1: Start with S
>
> From i=1 to i=10,000
>
> Step 2: Rewrite S =\> ASC “i times”
>
> After doing so for each “i”,
>
> Step 3: Rewrite S = B
>
> Step 4: Erase B
>
> Step 5: Send the final string to screen

So, we see that this code can generate the required list of strings we want. For example, taking i=4, we have ‘Rewrite S = ASC’

This gives us the following derivation:  
S =\> ASC =\> AASCC =\> AAASCCC =\> AAAASCCCC (4th time, i=4)

Then, we have:   
AAAASCCCC = AAAABCCCC (Step 3: Replace S by B) = AAAACCCC (Step 4: Erase B)

So, we see that this set of instructions, when blindly repeated 10,000 times (counted by “i”), can generate all the strings that we want on the screen.

But look what has happened here! Here, the strings that I have to generate have only the letters A and C! But for coding and manufacturing them, I have used extra symbols in bold - **S** and **B**. These letters were used only as intermediaries for keeping track in the iterative process and they disappear in the final stage when the word is produced. So you realize that to generate a set of strings from an alphabet set computationally, one finds the need to use extra symbols apart from the alphabet for book-keeping purposes. Here, the extra letter S was used as a kind of counter to keep producing repeatedly more sets of A and C that we want (through the iteration with the variable “i”). The letter B was used as an intermediary to erase the S to produce the final string that is bereft of any letters other than A and C.

Now, the letters S, B - they are used just as intermediaries, facilitate the iterative generation of words, and disappear in the final stage. This must remind you of the tags in the bookstore that are not a part of the book, are there only to facilitate the shopping experience, and are removed after the book is selected and purchased! In the area of computer science called “Formal Language Theory” - which deals with algorithmic generation of a given set of words over an alphabet - there is a technical name to these two kinds of letters.

> The letters that are a part of the words of the final intended
> language that is to be generated are called **terminal symbols**. The
> set of all such terminal symbols is called the **terminal alphabet**.
>
> The letters that are not a part of the words of the final intended
> language but are used by the algorithm to just act as intermediaries
> to facilitate the generation of the final word and disappear in the
> final stage when a word is created are called **non-terminal
> symbols**. The set of all such non-terminal symbols is called the
> **non-terminal alphabet**.

In this definition, the tag in the book is a non-terminal!

Now, what Pāṇini did is essentially this. He was concerned not with generating a bunch of simple strings of only two letters. His aim was to generate all Saṃskṛta words algorithmically! His problem was not as simple as generating AC, AACC, AAACCC etc. It was basically to generate all the words of a complicated natural language based on the sacred Vedas! He wanted to design an algorithm so that there was a way to derive any Saṃskṛta word through his algorithm, so that people could check whether what they uttered was a legitimate Saṃskṛta word or not.

Remember at the time of Pāṇini, the Vedic language was already becoming archaic and difficult to understand because Vedic Sanskrit had changed and evolved a lot into the various Prakrits (Prākṛt-s). So, at Pāṇini’s time, the language of ordinary discourse and the native tongue of everyone was one of the Prakrits with Sanskrit, being reserved only for intellectual discourse by the people who preserved the Veda. Now, for a person whose native language is a Prakrit, and with Sanskrit being learnt later and used only in formal communication, there is a high chance that he might mix the two up and make mistakes in his Sanskrit pronunciation. This is where Pāṇini enters the scene - he thought ‘what if’ in future - two people are pronouncing the same word in a Sanskrit differently, how will they resolve which one of their pronunciation is correct, and hence which one of their words is a legitimate Saṃskṛta word? So, it is in this scenario that he presents his grammar. Through his sūtras, Pāṇini says:

> A word is a legitimate Sanskrit word if and only if it can be derived
> from the repeated and correct application of some subset of my sūtras.

In other words, he is giving us an algorithm (a generation process, like we saw for the language consisting of the words ‘AC, AACC, AAACCC’) but for the natural language of Sanskrit consisting of all Sanskrit words! Pāṇini’s sūtras are the transformation steps like seen in the simple A&C language like “ Rewrite S = ASC” or “Rewrite S = B” or “Erase B”. For that, he uses tag letters as intermediary non-terminal symbols that help to perform the required operations for word formation but disappear in the final stage and do not contribute to the pronunciation of the final words themselves.

This technique of using tags or non-terminals or auxiliary symbols was rediscovered in Europe only in the last century.

Pāṇini used the method of auxiliary symbols (non-terminal symbols), in which new affixes are designated to mark syntactic categories and the control of grammatical derivations. This technique, rediscovered by the logician **Emil Post**, became a standard method in the design of computer programming languages.

**Noam Chomsky**, the person who laid most of the foundations of modern linguistic theory and formal language theory, also acknowledges Pāṇini as his antecedent. At a speech he delivered in Kolkata in 2001, he said, “*The first generative grammar in the modern sense was Pāṇini’s grammar*”.

*The idea of describing the structure of language with rewriting rules can be traced back to at least the work of Pāṇini, who used it in his description of Sanskrit word structure – hence, some suggest to rename **Backus-Naur Form** (BNF) to **Pāṇini–Backus Form**.*

# **Sanskrit : Roots, Ablaut, and the Vedic Accent**

To understand what Pāṇini did exactly, we must have a rough idea of the Sanskrit language - after all, that is the language for which he is designing a formal grammar, right? You do not need to remember all the language specific information that I tell below, but only the overall gist of what is happening.

### Roots

For that, let us look at some Saṃskṛta words with their meanings:

करोति = he/she/it does  
सरति = he/she/it flows  
चलति = he/she/it moves or walks  
एति = he/she/it goes  
बोधति = he/she/it awakens

Now, we see intuitively that the ति part in every verb that is listed above is a suffix, or a grammatical ending, as it repeats in all verbs that are in 3rd person, singular, present tense. It turns out that this ति is an ending for a verb which conveys that the verb is:

1.  Present tense

2.  Indicative mood (conveying a factual statement)

3.  Active Voice

4.  The subject of the verb is third person and singular

Let us change one of these grammatical aspects and we will see the endings change.

Example: Consider the word चलति which is a present indicative active 3rd person singular form of the verb. Let’s see how the endings change when any of these details above change:

चलति = he/she/it moves (present, indicative, active, 3rd person, singular)  
अचलत् = he/she/it moved (past, indicative, active, 3rd person, singular)  
चलतु = he/she/it should move (present, command, active, 3rd person, singular)  
चल्यते = he/she/it is moved (present, indicative, passive, 3rd person, singular)  
चलसि = you (singular) move (present, indicative, active, 2nd person, singular)  
चलन्ति = they move (present, indicative, active, 3rd person, plural)

So we see that the core part of the verb, which conveys the meaning of moving, is the part “चल्”. We see that as this part is the barest minimum part which conveys walking - all other endings that come after it (called suffixes) or before it (called prefixes) convey grammatical information like tense, mood, voice, person and number of the subject.

### Ablaut

Now, let us take some more words for comparison.

[](https://substackcdn.com/image/fetch/$s_!rQzC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d75498b-8814-43e8-ac2c-7049e059ee33_1374x552.heic)

![](https://substackcdn.com/image/fetch/$s_!rQzC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1d75498b-8814-43e8-ac2c-7049e059ee33_1374x552.heic)

So, we see something happening here that would be very familiar if you are a speaker of an Indo-Aryan language (e.g. खुलना vs खोलना), but not that much if you are a speaker of a Dravidian language. What happens here is that the vowel inside the main part of various words conveying the same core meaning changes as it goes through various forms. The exact vowel changes are enumerated below:

- चल् vs चाल् (cal vs cāl)

- विष् vs वेष् vs वैष् (viṣ vs veṣ vs vaiṣ)

- बुध् vs बोध् vs बौध् (budh vs bodh vs baudh)

- कृ vs कर् vs कार् (kṛ vs kar vs kār)

The vowel changes inside the main root cover three varieties and they are:

[](https://substackcdn.com/image/fetch/$s_!iy8v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0a11613-ea3e-43ad-bbd0-0393e95802cc_1306x722.heic)

![](https://substackcdn.com/image/fetch/$s_!iy8v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd0a11613-ea3e-43ad-bbd0-0393e95802cc_1306x722.heic)

So, we see that the main part of all the words with the same core meaning remains the same except for a three-part variation in vowel. The first variety (अ, इ, उ, ऋ, ऌ) is called **low grade** by English grammarians because the gap between the lower and upper part of the mouth is the lowest in this variety. Sanskrit grammarians consider this the default form of the vowel and never named it. The second variety of vowels (अ/आ, ए, ओ, अर्, अल्) is called the **medium grade** by English grammarians and **guṇa** by Sanskrit grammarians. The third group of vowels (आ, ऐ, औ, आर्, आल्) is called **high grade** by English grammarians because the gap between the lower and upper portions of the mouth is the highest in this grade; and is called **vṛddhi** by Saṃskṛta grammarians which also carries the same meaning.

If you think this is too strange for you to handle, you have it in English and Hindi too. For example, consider the words

- sing, sang, sung, song (core meaning: singing)

- give, gave (core meaning: giving)

- man, men (core meaning: manliness)

- drink, drank, drunk (core meaning: drinking)

- food, feed, fed (core meaning: eating)

So you see that English uses vowel changes inside the main part of the root to convey things like tense, number, and nominal derivation - just that you knew it all along, but didn’t know that you knew it!

The variation between low and medium grade for इ and उ vowels still survives in the modern Indo-Aryan languages; although the vṛddhi derivation has ceased to be productive in the modern languages, except in learnt Tatsāma borrowings from Saṃskṛta. Examples in Hindi are:

- खुलना vs खोलना (उ vs ओ)

- भेजना vs भिजवाना (इ vs ए)

In fact, some form of vowel alternation inside a single syllable main part survives, in some form or the other, in all Indo-European languages; and remains one of the key features in characterizing the relatedness of the languages of that family. This is known in technical Indo-European linguistics by the term **ablaut**.

If the main part varies in its vowel, by three possible ways, in various related derivations, how can we list them in a dictionary that contains the main parts alone? This is where Pāṇini makes a choice - he looks at all possible words derived from a common theme, and then chooses to take the main part with the lowest vowel grade that it occurs in, and then put it in his dictionary of main parts. The main part with the lowest grade that Pāṇini chooses to enter into his list is called by English grammarians as root and by Sanskrit grammarians as धातु (dhātu).

So, the root is that main part of all related words in Sanskrit, in the lowest possible vowel grade in which it is found among all possible words coming from it. In most cases, this happens to be the vowel in low grade; but in some cases this can be the medium grade too, and in rare cases the root can be listed in the root list in high grade also. The list of roots is called as dhātupāṭha. To see the list of all the roots of the Sanskrit language (Pāṇini), visit [this page](https://ashtadhyayi.com/dhatu) (the roots are in bold, and the remaining are technical details about the root).

### Vedic pitch accent

In this sub-section, we will talk about a very important feature of vowels in the Vedic language that had been completely lost in the spoken classical language, which is accentuation of vowels. In the Vedic language, all vowels in all words could be articulated in 3 ways depending on the pitch in which they were uttered. Based on that, they are classified as

1.  udātta उदात्त raised (high pitch)

2.  anudātta अनुदात्त “ (low pitch)

3.  svarita स्वरित sounded (high & then low = falling pitch)

This type of accent system is similar to the pitch-accent system of modern-day Japanese, but has completely disappeared from Classical Sanskrit and its daughter Indo-Aryan languages after the Vedic era. Although the Vedic mantras were transmitted by the priests with correct accent, it was lost in the later post-Vedic stage of spoken Sanskrit and Prakrits. The exact manner of articulating these three accents may be best mastered by listening to Vedic chantings done by professionally trained Vedic priests. But what is important here is how Pāṇini uses these pitch accents for other purposes - in his input data, he equips the vowels with accents, to convey more information in it, and use them as tags again!

# Non-Terminals in Pāṇinian Grammar (इत् letters)

Pāṇini has lots of inputs going in to his algorithms - some of them are:

1.  Śivasūtras (arrangement of sounds of the language)

2.  List of roots धातुपाठः

3.  List of suffixes प्रत्ययाः

4.  List of prefixes उपसर्गाः

5.  List of augments

He creates Sanskrit words by combining roots with prefixes and suffixes, and by applying certain transformations on them that are enumerated by the sūtras.

Now in arranging these roots and suffixes, we run into the same problem as the bookstore. There are many ways to arrange the roots and suffixes and prefixes, as they have many characteristics and undergo many transformations for many kinds of situations. So, not all of those can be conveyed through mere ordering of them (like not all kinds of shoppers will be satisfied given an arrangement of books in a bookstore with a given criterion). So, like tags, Pāṇini needs to equip them with tags so that they convey more information about the root or suffix. The tags which we have called in computer science as non-terminals are referred to as इत् letters by the gramamtical tradition.

Remember what we did in the computer science problem, where we had to generate a language with alphabets A and C? We used non-terminals whose letters are not A and C but something else - B and S. This is a rational choice - otherwise we will confuse the non-terminals and the terminals. This is a good coding strategy. But unfortunately, Pāṇini did not have that luxury as he was living in an oral culture. He could not afford to use novel sounds for those tag-like non-terminal letters. Whatever sounds are found in his Sanskrit and Prakrit language, he could use only those for his non-terminal symbols too! So, he places these non-terminals carefully at some place and tells us in the sūtras, where he has these non-terminals exactly so that hearers do not mistake it as a part of the root or a suffix! The set of instructions he gives are encoded in the sūtras 1.3.2 - 1.3.9.

For brevity’s sake, I shall state only some of the important sūtras regarding this and I shall not state the original Saṃskṛta sūtra of Pāṇini; because not all of you may be familiar with Saṃskṛta, and also lot of meta-language and contextual issues have to be broken down. So, I shall state only what the sūtras convey in plain English after their decoding.

> 1.3.2 In any input data, a nasal-vowel (अनुनासिकः) is a non-terminal
> (इत्) letter (except those qualified by 1.3.4).  
> 1.3.3 A final consonant in any input data is a non-terminal (इत्)
> letter (except those qualified by 1.3.4).

So, here we see that the final consonant of any input data (Śivasūtras, roots, prefixes, suffixes, etc) is non-terminal; and has to be remembered but omitted, for linguistic purposes. Also, a vowel in the input data is a non-terminal if it is a nasal vowel. But the rule has some exceptions (as stated in bold) and these exceptions are what are spelled out in the sūtra 1.3.4. But I shall not go through this here in this introductory level article.

> 1.3.5 An initial syllable that is either of ञि, टु, डु in any input data
> is a non-terminal (इत्) letter

In this sūtra, we are told that in any input data, if the initial starting syllable is one of the three - ञि/टु/डु - then that syllable is again not a part of the data, it is only a tag that has some information about the data.

> 1.3.6 An initial ष् consonant at the beginning of a suffix only (प्रत्यय)
> is a non-terminal (इत्) letter

In this sūtra, we are told that only in suffixes (प्रत्ययs), the letter ष् - when it occurs initially in the suffix - is not a part of the suffix, and is just a tag non-terminal.

> 1.3.7 An initial consonant that is either of च्, छ्, ज्, झ्, ञ्, ट्, ठ्, ड्,
> ढ्, ण् at the beginning of a suffix only (प्रत्यय) is a non-terminal (इत्)
> letter

In this sūtra also, we are told that only in the case of suffixes, if the initial letter is among च्, छ्, ज्, झ्, ञ्, ट्, ठ्, ड्, ढ्, ण् - then it ceases to be a part of the suffix, and is a tag non-terminal letter.

Now, an important question may arise. Why did not Pāṇini make this rule as a part of the previous rule itself? Why state for initial ष् of the suffix alone separately in 1.3.6 and for the other initials of suffixes in 1.3.7? The answer again has to wait until a future section - in Pāṇinian grammar, there exist what are called as meta-rules, where in a rule can be overridden by another rule depending on the parameters of the rule. So, it turns out that this 1.3.7 can be overridden under circumstances (i.e. not all initial च्, छ्, ज्, झ्, ञ्, ट्, ठ्, ड्, ढ्, ण् of suffixes are non-terminals - sometimes they are a part of the suffix itself). This overriding will be described in another rule; but 1.3.6 is unconditionally true, and holds universally for all suffixes. Due to the difference in nature of these two rules, they are separately enunciated.

> 1.3.8 An initial consonant that is either of ल्, श्, क्, ख्, ग्, घ्, ङ् at
> the beginning of a suffix that are not taddhita (non तद्धित-प्रत्ययs) is
> a non-terminal (इत्) letter

Now, we see that this rule applies not to all suffixes, but to a special class of suffixes that are not of a particular type. What is a taddhita suffix? These are the suffixes that are not attached to verb roots but to other derived parts of speech - like noun stem or adjective stem.

For example in English, the suffix “tion” acts on a verb root and converts it into a noun.   
Eg. “deplete” (verb) = “depletion”.

But the suffix “ic” acts on not verbs but nouns to convert them into adjectives.   
Eg. “atom” (noun) = “atomic” .

The suffix “ness” acts on adjectives and converts them into nouns.  
Eg. “great” (adjective) = “greatness”.

So, in the language of Pāṇini grammar, the suffixes “ic” and “ness” are the taddhita suffixes in English as they act on stuff that are not verbs (nouns and adjectives) whereas the suffix “tion” is a non-taddhita suffix as it acts on a verb.

So, the sūtra 1.3.8 says that for suffixes that act only on verbs, an initial ल्, श्, क्, ख्, ग्, घ्, ङ् is a non-terminal.

You might ask, what do these tag letters convey? They convey quite a lot of information. Seeing the exact इत् letter and the nature of the data (whether it is a root or a suffix or so on), one can convey so much additional information. Some of them are given below.

# **Uses of non-terminal इत् symbols**

### Use 1 : Deciding what suffixes a root or a nominal stem can take

There are a lot of suffixes in English taken by lots of words. For example, take the suffix “ion” in English that converts a verb ending in a silent “e” into an abstract noun.

- dilute = dilution

- substitute = substitution

- deplete = depletion

But not all verb roots in English that end in “e” can take this “ion”. As examples, see below.

take = ~~taktion~~  
make = ~~maktion~~  
measure = ~~measurtion~~  
(these are not real English words)

We see that there is no regular rule that determines what kind of verb roots take this “ion” suffix. So we need to equip the roots with tags that convey this information of whether they can take the suffix “ion”. Consider another example of how English verbs form their past tenses.

**First way (regular) way:**   
Most English verbs form their past tense by attaching a “d/ed” suffix to the verb root. These are called regular verbs.  
Examples: call-called, show-showed, maintain-maintained, manage-managed, help-helped.

Now, there are also lots of other verbs that form their past tense by a vowel change inside the root as it was mentioned previously. They can be arranged into groups based on what vowel comes about in the past tense inside the root.

**Second class - Drink:**  
These verbs form their past tense like drink-drank.   
Examples: sing-sang, drink-drank, shrink-shrank, sink-sank, ring-rang, sit-sat, eat-ate.

**Third class - Drive:**  
These verbs form their past tense like drive-drove.  
Examples: ride-rode, dive-dove, strive-strove, freeze-froze, win-won.

**Fourth class - Grind:**  
These verbs form their past tense like grind-ground.   
Examples: wind-wound.

**Fifth class - Sleep:**  
These verbs for their past tense like sleep-slept.  
Examples: keep-kept, weep-wept, sweep-swept, creep-crept.

**Sixth class - Blow:**  
These verbs for their past tense like blow-blew.  
Examples: throw-threw, fly-flew, grow-grew.

**Seventh class - Cut:**  
These verbs for their past tense like cut-cut (no change).  
Examples: put-put, hit-hit

**Eighth class - Take:**  
These verbs for their past tense like take-took.  
Examples: shake-shook.

**Ninth class - Fight:**  
These verbs for their past tense like fight-fought.  
Examples: seek-sought, bring-brought, think-thought, buy-bought, teach-taught.

**Tenth class - Catch:**  
These verbs for their past tense like catch-caught.  
  
**The irregular ones:**  
For some verbs, the past tense is completely unrelated to the present tense and comes from an entirely different root and has to be painstakingly memorised separately.  
Examples: go-went, make-made, is-was, do-did

So, we see English verbs are divided into some ten classes and some irregulars based on how they form their past tense from the present tense. And there is no predictable rule for this. For example, the words “call” and “fall” look almost similar in form but belong to different classes (“called” vs “fell”). The words “sit” and “hit” also look almost similar in form and again belong to different classes (“sat” vs “hit”). So, this class information again has to be conveyed by either arranging them in an order according to class, or attaching tags to them. For the past tense, if we arrange the verbs according to class, we cannot repeat the same for the classes of forming some other tense like the past participle. So, even if we manage to convey the past tense class information by arrangement and optimal order of the roots, the method by which the past participle is formed has to be conveyed by other means like using a tag, because these classes do not overlap.

So, the non-terminals can convey the information of which roots can take which kinds of suffixes.

Now how does this work in Sanskrit? Let us see an example. If you recollect the verb examples in the previous section, you might have recalled the verb suffix ति that conveyed that the verb is third person, singular, present tense, indicative mood and active voice.

Eg. Root पठ् (to read) = पठति (he/she/it reads)

Turns out not all roots take this ति suffix. Some other roots prefer to take another set of suffixes and in this other set, the same third person singular, present tense, indicative mood, active voice is conveyed by a suffix ते.

Eg. Root युध् (to fight) = युध्यते (he/she/it fights)

Some other roots can take both of those suffixes.

Eg. Root पच् (to cook, to get ripe) = पचति/पचते (he/she/it cooks)

The first set of suffixes with ति as 3rd person, singular, present, indicative, active are called parasmaipada suffixes and the second set of suffixes with ते as 3rd person, singular, present, indicative, active are called ātmanepada suffixes. Roots that can take only parasmaipada suffixes are called naturally parasmaipada roots. Roots that can take only ātmanepada suffixes are called naturally ātmanepada roots. Roots that can take both are called ubhayapada roots (Sanskrit: ubhaya = both).

Now, why do roots take two kinds of suffixes to mean the same thing? From comparative linguistics with other Indo-European languages, it turns out that at an earlier stage of the language, all roots could take both parasmaipada and ātmanepada suffixes and this conveyed a distinction in meaning. This distinction is still preserved in Sanskrit roots that are ubhayapada (can take both kinds of suffixes). Take the root पच् that we saw above that can take both parasmaipada and ātmanepada suffixes. The distinction was that the parasmaipada conveyed that the verb was done for someone else other than the subject and the ātmanepada conveyed that the verb was done for the subject itself.

Example:  
Root पच् = parasmaiapada पचति = he cooks for himself  
Root पच् = ātmanepada पचते = he cooks for someone else

So, this was the original distinction between parasmaipada and ātmanepada suffixes. This distinction is still conserved in ubhayapada roots that can take both kinds of suffixes. But as the language evolved, some verbs were only used in the parasmaipada form and some others only in the ātmanepada form that the alternative was totally forgotten and hence only one set of suffixes survived in usage for those roots by the time the language was recorded down. That is for instance, an ātmanepada root like युध् would have originally had both a parasmaipada युध्यति (he fights for someone else) and an an ātmanepada युध्यते (he fights for himself) but the ātmanepada form युध्यते eventually having been used more frequently, eclipsed the parasmaipada form such that it was forgotten. So, now the verb root युध् in classical Saṃskṛta takes only the ātmanepada form युध्यते. For this root, we have proof explicitly. The root युध् had both parasmaipada and form in the Vedic language and only in classical language, its parasmaipada usage has vanished.

Anyways how does Pāṇini convey which root is which? He does this through the non-terminal tag letters again! The rule is as follows:

- If a root has a non-terminal consonant ङ् or it has a non-terminal
  nasal vowel with the anudātta accent, then it takes only the
  ātmanepada suffixes!

- If a root has a non-terminal consonant ञ् or it has a non-terminal
  nasal vowel with the svarita accent, then it optionally takes
  ātmanepada suffixes! (i.e. it is an ubhayapada root)

- All other roots that do not satisfy either of these two conditions can
  take only parasmaipada suffixes!

Examples of roots (inside the brackets is the bare root without the non-terminals):

- Root डुपचँष् (पच्) with svarita अँ = ubhayapada

- Root शिञ् (शि) has ञ् non-terminal = ubhayapada

- Root युधँ (युध्) with anudātta अँ = only ātmanepada

- Root गाङ् (गा) with ङ् non-terminal = only ātmanepada

- Root भू (भू) with no non-terminals = only parasmaipada

### Use 2 : Deciding what suffixes cause what change in roots

Next, we will see what the non-terminals on suffixes can do. They can say quite a lot of information like:

To what, the suffix must attach itself to - for example: The suffix “er” in English (play = player) can attach itself only to verbs, while the suffix “ic” in English (atom = atomic) can attach itself only to nouns, while the suffix “ness” can attach itself only to adjectives (ugly = ugliness). The non terminals on roots can convey information as to what kinds of changes they cause to the roots or stems that they attach themselves to. For example, the suffix “er” in English doubles the final hard consonant of a verb root if the root ends in a consonant (eg. put = putter, sit = sitter, rap = rapper).

Similarly, we have counterparts in Sanskrit too. Take for example, some roots and their associated verbal nouns.

Sanskrit has several suffixes that demand that the vowel inside the root stays in medium grade (guṇa) so that by default, it is the vowel grade assume for suffixes that attach to verbs directly and give rise to nouns or adjectives.

Example: Root कृ (meaning: to do)  
The guṇa of the vowel ऋ is अर्.  
  
Some nouns and adjective suffixes when attached to these root to form nouns derived from this root require that the vowel in the अर् form. Examples :

- करण = the act of doing (कर् + अण)

- करणीय / कर्तव्य = that which is to be done (कर् + तव्य / अणीय)

- कर्तृ = doer (कर् + तृ)

- कर्तुम् = for doing (कर् + तुम्)

But the past participle (done) always mostly has its vowel in the low grade which is

- कृत = done (कृ + त)

How can this be conveyed? Again, Pāṇini conveys this using non-terminals. In his list of suffixes, he stores this त suffix as क्त (kta) with the first क् being a non-terminal. This initial क् is not a part of the suffix but tells us that the vowel inside the root should not be in the normal guṇa grade as expected for many other suffixes but should be in the low grade!

# Programming for dummies like me

If you are a computer scientist and programming is your day job, you can safely skip this and the next section. I am not a computer scientist either - I am so bad at coding. But what I am going to say is more about problem solving than it is about the exact coding. Hence, it is okay if you do not understand all the exact details in your head. Read through this section where I introduce in as simple terms as possible, the various concepts of object oriented programming and its uses. In the next section, I will connect all these concepts to Pāṇinian grammar and how he brilliantly uses them in his Aṣṭādhyāyī.

Let us consider a very simple problem - to check whether a given positive integer is even or odd. This is how a program for that will look like in the C++ programming language - don’t be scared if you did not study computer science (I also did not), but just watch it and I will explain it step by step.

    include <iostream>
    using namespace std;
    int main() {
    int n;
    cout << “Enter an integer: “;
    cin >> n;
    if ( n % 2 == 0)
    cout << n << “ is even.”;
    else
    cout >> m >> “ is odd.”;
    }

Now, let me explain this program. The first two lines are routine stuff that need to be typed for every program. The core part starts with the main block. Let us focus between the int main `{ }` thing.

    int n;

The symbol “int” here is an abbreviation for integer and the line “int n;” defines that a variable named “n” is an integer. This is the number that the user is going to enter and have it checked for even or odd. So this line defines the name and nature of the data that the user is going to enter - which is an integer named “n”. So, this line in the code is not doing anything but only defining things that are going to be involved in the task that is going to be solved by an algorithm. The line:

    cout << “Enter an integer: “; 

is an output that comes from the computer to the user. The computer here is being asked or programmed to give an output that prompts the user to enter an integer. Upon seeing this message, the user will enter the positive integer. Now, coming to the next line.

    cin >> n;

After the user has entered the positive integer, this line in the code is instructing the computer to take the data he entered as the positive integer “n” that he wants to be checked as even or odd. Now, coming to the core task. Look at the following lines

    if ( n % 2 == 0)
    cout << n << “ is even.”;
    else
    cout << n << “ is odd.”;

Here, the symbol “%” is the remainder operator - i.e. “a%b” is the remainder obtained by dividing “a” by “b”. So, **n%2** will give the remainder that is obtained when the integer **n** is divided by 2. Now when any integer is divided by 2, it is either 0 or 1. The line above tells us that if the remainder obtained in the operation **n%2** is 0, then output to the user that the number **n** is even. Or else, output and prompt the user that the number “n” is odd. This is a very simple problem. We all know that a number is even if and only if the remainder obtained after dividing it by 2 is zero and odd otherwise. But there are technical names for certain things that are seen in this code.

### **Reserved keyword**

The abbreviation **int** that stands for a positive integer is called a keyword in a computer program. This abbreviation cannot be used to name any other variable and is reserved and defined by the programming language system itself - you cannot name any other entity in your program by these abbreviations like **int** that are already reserved by the programming language (in this case C++) for something else.

### **Standard function**

The symbol **%** is also reserved by the system for a specific purpose - from what I have told you, it is the remainder operation. Such standard operations that are defined already in the programming languages are called standard functions. The **%** operator takes two positive integers, divides the first one by the second and outputs the reminder of the result obtained. Again, this remainder function with its symbol **%** is already reserved by the system. The system already knows everything that this **%** operator does. It knows

1.  What it takes in as its input - in this case, two positive integers

2.  What it does to the input - in this case, compute the remainder of
    the first divided by second

3.  What it returns or gives back - in this case, return the remainder
    obtained

Now, let us execute the same task in a slightly different way - using the concept of user-defined functions.

### User-defined functions

Read the code below. Here, in the main part of the code, I have called upon a strange operation that I have created on my own - it is called **evenoddcheck**. It takes an integer, divides it by 2 and returns the remainder. Using this I rewrite the code as follows:

    include <iostream>
    using namespace std;
    int evenoddcheck(int n);
    int main() {
    int n;
    cout << “Enter an integer: “;
    cin >> n;
    if(evenoddcheck(n)==0)
    cout << n << “ is even.”;
    else
    cout << n << “ is odd.”;
    }

But how will the computer know what this strange operation **evenoddcheck** stands for? It turns out that after the program, I need to type what the function does and define it completely. That definition follows outside of the main bracket **int main** `{....}` and is given below.

    int evenoddcheck(int n) {
    int result;
    if(n%2==0)
    result=0;
    else
    result=1;
    return result;
    }

Here, let me explain the function definition step by step. The first line of the code is

    int evenoddcheck(int n) { ... }

Here, the part **evenoddcheck** is the name I assign to the function. In the bracket that has **(int n)**, I tell that this function has to take an integer named **n** as the input. In the first word **int**, I tell that the output of the function is also another integer - in this case, the remainder obtained when the integer \*\*n \*\*is divided by 2. The rest part inside is the standard computation of the remainder.

Now what difference is achieved? By rewriting the remainder by 2 computations separately. The thing is that I can use this function readily whenever I want in the main program instead of typing it all again. It may not mean much for simple operations as in here but a lot for more complex operations. I can define all the complicated operations that I am going to use separately and my main program will be clean and call readily just what I want.

## **Object Oriented Programming for Dummies Like Me**

In this section, I will take a little step further and introduce object oriented programming concepts. Again, this can be safely skipped for whom it is a day job. In this section, I am going to introduce a few more concepts that may sound sophisticated but are in essence simple to understand. They are the following - **class**, **object and inheritance**.

### **Class & Object**

The standard types of data that computers are trained to manipulate are routine objects like integers or strings or arrays. When we deal with more complicated data types, one needs to come up with the notion of a class. A class is simply a blueprint for a combination of a novel data type and a set of instructions one is interested in. For example, I can define the class for driving a car named CAR_CONTROLS with the following attributes - fuel, speed that also has some operations associated with it - accelerating and driving. All these characterize a car control system (there are lots of others too but for now, let us stick to only these). For example,

    class CAR_CONTROLS {
    float fuel_level
    float speed
    float driving(float accelerator) {...}
    float braking(float brake_position) {...}
    }

Here, the class CAR_CONTROLS has two data associated with it - fuel_level and speed. And we have two operations - driving and braking that take as their inputs, accelerator and brake position and modify the speed accordingly in the `{...}`section. So, this is what the concept of a class is - a template for a combination of a data set and instructions.

Now, this class is a template for creating so many actual cars having some values for these numbers specified. A specific car may have a fuel_level of 0.5 in liters. An object is an instance of a class.

### **Inheritance**

A very important concept in object oriented programming is the notion of inheritance. Consider two classes - the class HUMAN and the class STUDENT. We see that all students are humans and hence we would like the class STUDENT to inherit the data and instructions in the class HUMAN. This phenomenon is called inheritance. Of course the class STUDENT could contain more specific information like name of the school that is not present in the generic class HUMAN but we all agree that it should logically get the properties of the class HUMAN. This inheritance saves lots of programming time and space since one need not keep on mentioning the repeating set of features in all the inherited classes from a given parent class.

Consider the even more generic class ANIMAL. And now the class HUMAN which is an inherited class from ANIMAL. Now consider the instruction MOVEMENT. In the generic class ANIMAL, the instruction MOVEMENT would be something like: position four limbs vertically upright and touching the ground and then actuate to move. But we know that humans, while being an inherited class from ANIMAL do the movement differently - we walk erect with just two of our backlimbs (called legs) positioned vertically and touching the ground and we reserve our forelimbs (called hands) for novel tasks like tool making and grasping. So, consider the scenario:

    class ANIMAL {
    movement {..walk using four limbs..}
    }

For other classes of animals like DOG, CAT, etc this function “movement” using four limbs can be inherited directly. But it cannot be done so for humans. So, for the class HUMAN, we must have

    class HUMAN: ANIMAL {
    movement {..walk using two back limbs..}
    }

Now, let us say that I create an object from the class HUMAN and call the function “movement”. What should be implemented? It turns out that instructions in the inherited class overrides the instructions in the parent classes. This phenomenon is called function overriding in object oriented programming. Its formal definition is given below.

### **Function Overriding**

Function overriding is a concept in object-oriented programming which allows a function within an inherited class to override a function in its base class. This is very important and saves lots of programming time - if you have a general instruction that is applicable by default but some special set of instruction to override it for special cases, then function overriding ensures that by simply rewriting the function for the special case, the special instruction is implemented for the special case and the general instruction is ignored. The following picture summarises inheritance and overriding.

[](https://substackcdn.com/image/fetch/$s_!DT2h!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d6aa4b8-19bc-454a-90f9-7c1d328519ce_790x498.heic)

![](https://substackcdn.com/image/fetch/$s_!DT2h!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d6aa4b8-19bc-454a-90f9-7c1d328519ce_790x498.heic)

### **Multiple inheritance**

How about a class that inherits from two or more base classes? After all, biologically, a child inherits from two parents. This phenomenon is called multiple inheritance. For example, the class INDIAN_BOY needs to inherit both from the class INDIAN and the class BOY. But what if there are two instructions of the same name but doing different things in the two parent classes? If both the parent classes contain different implementations of a function named X, then when the subclass inherits it, from what parent class will it implement X? If the inherited class has another instruction for X, then it turns out that by overriding, it overrides both of the instructions of X in the parent classes. Otherwise, there should be an explicit redefinition of X in the inherited class that tells us from which parent class, the function X is inherited in the inherited class. A picture illustrating it is given below.

[](https://substackcdn.com/image/fetch/$s_!elEy!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7cc5368f-623d-4c98-a5d8-662234370681_940x492.heic)

![](https://substackcdn.com/image/fetch/$s_!elEy!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7cc5368f-623d-4c98-a5d8-662234370681_940x492.heic)

# **The Programming Genius of Pāṇini**

You might ask again what the above things have to do with Sanskrit grammar? In this section, let us see it. In Sanskrit, to form the present tense of most verbs, one adds an extra अ before the personal endings. I give some examples:

1.  Root पठ् (to read) =\> पठ् + **अ** = पठ =\> पठ + ति =\> पठति
    (he/she/it reads)

2.  Root पत् (to fall) =\> पत् + **अ** = पत =\> पत + ति =\> पतति
    (he/she/it falls)

3.  Root लिख् (to write) =\> लिख् + **अ** = लिख =\> लिख + ति =\> लिखति
    (he/she/it writes)

4.  Root रक्ष् (to guard) =\> रक्ष् + **अ** = रक्ष =\> रक्ष + ति =\> रक्षति
    (he/she/it guards)

This is the case with most of the verbs. About 80% of the verb roots get an extra अ vowel before the personal endings are attached in the present and some other related tenses. But there are some classes of verbs that refuse to adhere to this rule or do something weird. Some examples are:

1.  Root हन् (to kill) =\> हन् + ति =\> हन्ति (he/she/it kills)

2.  Root अस् (to be) =\> अस् + ति =\> अस्ति (he/she/it is)

So, we again have a general rule applicable to all verb roots but a special exception for only some small class of roots. Does this remind you of inheritance? Note that there are many other rules in action as well and the picture is more complicated - I am simplifying it and am taking only one aspect to demonstrate in a simple fashion.

Pāṇini as usual solves this by using inheritance. He defines a class of ROOTS in general and divides them into ten subclasses - CLASS_1 , CLASS_2, CLASS_3, …CLASS_10. He generally gives an instruction to add the extra vowel अ to all roots by giving it in the parent class ROOTS but redefines that instruction in certain irregular classes and overrides them in the irregular classes. This is a general rule in Pāṇinian grammar:

> **Whenever there are two rules competing to be applied on the same
> object, with one rule for a generic case (applicability in a larger
> domain) and the other for a particular case (applicability in a
> smaller domain), the smaller domain is viewed as an inheritance of the
> larger domain since it it is a part of it and hence the rule for the
> smaller domain overrides the rule for the larger domain.**

Let us now see an example of the multiple inheritance case. Consider the three sets of Sandhi rules below.

1.  इ/उ/ऋ/ऌ + vowel = य्/व् /र् /ल् + vowel (We already saw this in a
    previous section as इकः यण् अचि)

2.  अ + vowel = guna (medium grade of the vowel)

3.  Vowel + Vowel (same pair) = Long Vowel

I give various examples of the three rules:

1.  प्रति + उषा = प्रत्युषा, सु + आगतम् = स्वागतम्, मातृ + अंशः = मात्रांशः

2.  राज + इन्द्रः = राजेद्रः, मह + उत्सवः = महोत्सवः, सप्त + ऋषिः = सप्तर्षिः

3.  ब्रह्म + अस्त्रम् = ब्रह्मास्त्रम्, योगि + इन्द्रः = योगीन्दरः, गुरु + उत्तमः =
    गुरूत्तमः

We see that rule 3 conflicts with rules 1 and 2. In the examples of rule 3, ब्रह्म + अस्त्रम् where in sandhi, an अ+अ is encountered, I can also apply rule 2 because it falls under the domain of अ+ any vowel . In the same rule 3 example of योगि + इन्द्रः where in sandhi, an इ+इ is encountered, I can also apply Rule 1 because it falls under the domain of इ + any vowel. So, how does Pāṇini ensure that it is only Rule 3 that applies in all those examples and not rules 1 and 2. The concept of overriding for the case of multiple inheritance comes into play. Consider the possible pairs of vowels visualised below. The like vowel combinations come at the diagonal of the table.

[](https://substackcdn.com/image/fetch/$s_!vFEe!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01338e58-37ba-43d8-b59f-c9695445e791_1276x360.heic)

![](https://substackcdn.com/image/fetch/$s_!vFEe!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01338e58-37ba-43d8-b59f-c9695445e791_1276x360.heic)

Now, the information of whether the combination is under the applicability of rule 1 (इ,उ,ऋ+vowel) or rule 2 (अ+vowel) or rule 3 (like vowels) is also given.

[](https://substackcdn.com/image/fetch/$s_!RR_t!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4abdc902-1428-438e-93e0-18fed042687f_1284x362.heic)

![](https://substackcdn.com/image/fetch/$s_!RR_t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4abdc902-1428-438e-93e0-18fed042687f_1284x362.heic)

One sees that the domain of Rule 3 is contained in the combinations of the domains of rules 1 and 2. combined. This is visualised below.

[](https://substackcdn.com/image/fetch/$s_!x_LB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bb6a785-b6fd-4266-9586-b2457e74471c_940x492.heic)

![](https://substackcdn.com/image/fetch/$s_!x_LB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4bb6a785-b6fd-4266-9586-b2457e74471c_940x492.heic)

So, Pāṇini does not have to qualify anything more - the overriding principle that he assumes and states, automatically overrides applications of rules 1 and 2 whenever rule 3 also can be applied. So, rules 1 and 2 will be applied only when rule 3 cannot be applied. This is because the rules 1 and 2 are more general than rule 3 which is more specific and always an instruction for a specific class is followed whenever it clashes with an instruction from a generic case.

# **Recursion and Production of More Objects**

We saw that classes are templates for objects which contain information about data and instructions (functions). And we saw that functions like evenoddcheck act on data and give out new data (take two numbers and return remainder). But wait, can a function throw out new objects, thus adding to a database? This is possible in object oriented programming - one can have functions inside classes (that act inside all the objects of those classes) and one can arrange these functions to return new objects of the existing classes with its own new functions. I do not want to write a code again for this but the idea should be clear.

Pāṇini does this too - he utillises important aspects of Sanskrit language. Let us take one simple application - the desideratives or सनाद्यन्तः. Consider the following two sentences in English:

1.  I **read** books.

2.  I **want to read** books.

In the first sentence, the verb is factual - the reading is a matter of fact. Whereas in the second sentence, the verbal part “want to read” is not factual - it merely conveys desire or intention. English conveys this desire by using the verb “want” and then putting a “to” in front of the verb that is desired. But Saṃskṛta modifies the verb itself to achieve this meaning. This mood of desire or intention is called the desiderative mood in grammar. See in Saṃskṛta.

1.  सः पुस्तकानि **पठति** (He reads books)

2.  सः पुस्तकानि **पिपठिषति** (He wants to read books)

So, we see that the verb transforms internally from **पठति** to **पिपठिषति.** What is happening are two crucial steps.

1.  Reduplication of the first consonant of the initial consonant part
    of the root with some vowel - i.e. पठ् =\> (the initial consonant प्
    in पठ् reduplicates with इ) पि + पठ् = पिपठ्

2.  Then, an additional स् /इष् is added to the reduplicated root - पिपठ् +
    इष् = पिपठिष्

Then, as usual we add the usual thematic vowel अ and the personal ending ति to get the final verb.

1.  पिपठिष् + अ + ति = पिपठिषति

How Pāṇini thinks of this process is that to convey desire, one manufactures a new root पिपठिष् from the ordinary verb पठ् through reduplication and addition of इष्. These roots are called secondary roots that convey desiderative grade (desire).

Pāṇini uses a special function that acts on all roots to create new roots. If we consider roots as objects like he did, then what he is doing is coming up with a function that takes in a root and gives out another root. The technical name that he gives for this function in his grammar is सन्. When the suffix सन् is added to a root, it triggers appropriate reduplication and additions to give up another root related to it and conveying the meaning of desire.

To translate from the language of object oriented programming to Pāṇinian grammatical terms,

[](https://substackcdn.com/image/fetch/$s_!ONI7!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe437007-9d69-4beb-a805-424342371369_1312x852.heic)

![](https://substackcdn.com/image/fetch/$s_!ONI7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbe437007-9d69-4beb-a805-424342371369_1312x852.heic)

Thus, we have seen how Pāṇini anticipates modern object oriented programming techniques through his masterpiece.

# Heads: Initial or Final?

In this final section of this article, let us end on a lighter and a slightly less technical topic. Try reading the following two sentences.

1.  *The view that beating a third-rate Serbian military that for the
    third time in a decade is brutally targeting civilians is hardly
    worth the effort is not based on a lack of understanding of what is
    occurring on the ground.*

2.  *It’s not a lack of understanding of what is occurring on the ground
    that creates the view that it’s hardly worth the effort to beat a
    third-rate Serbian military that is brutally targeting civilians for
    the third time in a decade*

Both the above sentences mean exactly the same and are equivalent completely in terms of vocabulary. What differs is just ordering of the information - what detail comes after what? Yet, did you find the first sentence more difficult to comprehend and the second one easier to comprehend even though you realised at the end that both convey exactly the same thing? If yes, you have understood an important phenomena - ordering of information affects our comprehension. Let us now analyse a little deeper - why is the second sentence easier on the mind than the first. For that we need to start with gentler examples and some technical language needed to describe some linguistic concepts.

### The first pairs of concepts are - **HEAD** and the **MODIFIER.   Noun & Adjective**

Let me explain what they mean by an example. Consider the phrase “***this beautiful house***”.

In the phrase “***this beautiful house***“ , the main thing that is being talked about is “***house***“ and the demonstrative pronoun “***this***“ and the adjective “***beautiful***“ are modifiers. You realise that the main thing that is being described in this phrase is the house. The word “beautiful” just adds additional information that the house is of a particular kind - nice to look at. The word “this” simply conveys that you are not talking about any random house but a particular house that is relevant to your context and is situated nearby.

So we have: “***this beautiful house”***  
Head: house  
Modifiers: this, beautiful

Now, in English, we have by its syntactical convention that the modifiers (adjectives, articles) come first and then the head comes finally at last. Such languages where the head comes last and its modifiers come first are called logically as head-final languages (rarely, scholarly jargon does make sense!). But this is not the case in all languages and need not be. In principle, the head and its modifiers could have come in any order.

Take Spanish, for example.   
Phrase: ***“esta casa hermosa”*** (esta=this, casa=house, hermosa=beautiful)  
Literal Translation: “***this house beautiful”***

In Spanish, first comes the demonstrative pronoun (this) , then the head (house) and its other modifiers (beautiful). So in this case, Spanish is a head-intermediate language because the head comes in between a set of modifiers - neither first nor last.

Let us consider Basque, a language spoken in France. There, this same phrase is given below.  
Phrase: “***etxe eder hau***” (hau=this, eder=beautiful, etxe=house)  
Literal word-by-word Translation: ***“house beautiful the”***

So, we see that in Basque, the head comes first and is then followed by its modifiers.   
  
Exercise: In all the languages that you know of, translate this phrase and see where the heads and the modifiers came. In Indian languages, the phrase will come like English only.

### **Reported Speech**

The concepts of head and modifiers are also important in other scenarios.

Consider the following sentence: “***He said that the water was hot***”.

We can split the sentence as follows:

***He said*** = the main sentence \[HEAD\]

***that*** = marker of reported speech

***the water was hot*** = details of what was reported \[MODIFIER\]

So here we see that the main sentence is “he said”. The part “the water was hot” is simply a description or a detail about what was said. In other words, the reporting sentence (“he said”) is the HEAD and the reported sentence (“the water was hot”) is its MODIFIER. In this case, English prefers a head-initial approach. But let me translate this sentence in few other languages:

Consider Hindi:  
Sentence: “***उन्होंने कहा कि पानी गर्म था***”  
Literal word-by-word Translation: ***He said that water hot was***   
Syntax: HEAD-MODIFIER

Consider Sanskrit:  
Sentence: ***सः अवदत् जलम् उष्नम् आसीत् इति*** {PREFERED}  
(OR) ***जलम् उष्नम् आसीत् इति सः अवदत्*** {ALSO USED}  
Literal word-by-word Translation: ***He said water hot was that*** (OR) ***water hot was that he said***  
Syntax: HEAD-MODIFIER (OR) MODIFIER-HEAD

Consider Tamil:

Sentence: ***தண்ணீர் சூடாக இருந்தது என்று அவர் கூறினார்*** {PREFERED}  
(OR) ***அவர் கூறினார் தண்ணீர் சூடாக இருந்தது என்று*** {RARELY USED}***  *** Transliteration: ***taṇṇīr sūḍāga irundadu enḍru avar kūrinār*** {PREFERED}***  *** (OR)***avar kūrinār taṇṇīr sūḍāga irundadu enḍru*** {RARELY USED}***  *** Literal word-by-word translation: ***Water hot was that he said*** (OR) ***He said water hot was that  *** Syntax: MODIFIER-HEAD {PREFERRED} / HEAD-MODIFIER

We see that both English and Hindi allow only a head initial construction for reported speech. The head should come first and then only the modifier - what was reported. But Tamil and Sanskrit allow both head-initial and head-final construction. But the head-final construction is preferred in both Tamil and Sanskrit and the head-initial construction for reported speech is used less often.

### **Possessive Case**

Next, let us go to possessives. Consider the English phrases below.

Phrases: ***Rama’s book*** (OR) ***book of Rama***  
Syntax: ***MODIFIER-HEAD*** (OR) ***HEAD-MODIFIER***

In expressing a possessive like in the phrase “***Rama’s book***”, the main thing being talked about is the book. **“Rama’s”** is just a modifier that conveys the additional information that the book being talked about is owned by or associated with Rama. In the apostrophe construction “***Rama’s book***”, we have a head-final construction whereas in the OF construction like in the phrase “***book of Rama***”, we have a head-initial construction. So we see that in case of possession, English allows both a head-initial and a head-final construction. But Indian languages in this case, allow only a head-final construction in this possession scenario.

Examples:   
Hindi = ***रामा का पुस्तक***  
Sanskrit = ***रामस्य पुस्तकम् / राम-पुस्तकम्***  
Tamil = ***ராமனுடைய புத்தகம் (rāmaṇuḍaiya puttagam)  *** Literal Translation in all the above examples: ***Rama \[ \] book*** (MODIFIER - HEAD)

### **Subject - Verb - Object**

Consider an ordinary English phrase “***Rama killed Ravana***”. In this sentence, the main person being talked about is Rama. In English grammar, you would have learnt that “***Rama***” is the subject of this sentence. Everything else in the sentence - “***killed Ravana***” - describes what the subject “***Rama***” is doing and if you still remember your school English grammar, you would have been taught that the things that describe the subject are called predicates. Now, if you want to recast it in our terms, the subject is the HEAD as he is the entity being described. The predicate describing the modifier is the MODIFIER. In English, the subject of a sentence always comes first and only then the predicate. So, in case of a subject-predicate scenario, English is a purely head-initial language. Now let’s go deeper into the predicate “***killed Ravana***”. Here, the main thing is the action that is being done - “***killed***”. The object of the verb “***Ravana***” is simply an additional information that conveys who was being killed. So, within the predicate - the verb is the HEAD and the object of the verb is the MODIFIER. And we know that in English, the object always has to come after the verb. So, within the predicate too, English strictly follows a head-initial construction.

In short, in the sentence: ***Rama kills Ravana  *** SUBJECT: ***Rama*** =\> HEAD  
PREDICATE: ***killed Ravana*** =\> MODIFIER (answers the question: Rama did what?)  
  
WITHIN THE PREDICATE:  
VERB: ***killed*** =\> HEAD  
OBJECT: ***Ravana*** =\> MODIFIER (answers the question: Who/What got killed?)

So, English strictly follows a head-initial construction when organising a simple SUBJECT-VERB-OBJECT sentence.

Now, this need not always be the case always. Consider Biblical Hebrew. If I translate this same sentence into Biblical Hebrew, it is:  
  
Hebrew sentence: ***Harag Rama et-Ravana  *** Literal Translation: ***Killed Rama \[object marker\]-Ravana  ***
  
Here, we see that the subject of the verb “Rama” neither comes first nor last in the sentence - it sits in between the initial verb and the object. So, it is head-intermediate with respect to subject and predicate. Within the predicate, the verb comes first (killed) and then the object (Ravana). So, in the predicate, Biblical Hebrew is a head-initial language. It is the same with Classical Arabic. \[Note: Modern Hebrew and Modern Standard Arabic follow the same English order of SUB-VERB-OBJ\].

How about a full head-final construction? Subject comes last after the predicate. The verb comes after the object in the predicate - so OBJ VERB SUB - exactly the reverse of English. So the sentence “Rama killed Ravana” would come out in such a language as “Ravana killed Rama”. Such languages are rare but they do exist - examples of this are a few Native American languages: Hixkaryana and Urarina.

How about Indian languages? Indian languages have flexible word order and the order of the subject, verb and the object can be changed due to the case endings. But the normal word order is that of SUB OBJ VERB. So, the English sentence “***Rama killed Ravana***” normally comes out as “***Rama Ravana killed***” in all Indian languages. Here, the subject “***Rama***” first and then only the predicate. So it is head-initial with respect to subject and predicate. But within the predicate, the HEAD verb comes later after the MODIFIER which is its object. So, Indian languages are head-final within the predicate.

### **Relative Clauses**

Consider the following sentence: ***Rama, who gave me the book, is here***.***  *** Let us now concentrate on the phrase “***Rama who gave me the book**”.* Here, the main person being talked about is “Rama”. So, this is the HEAD. Now, the part “***who gave me the book***” is just additional information that describes “***Rama***”- it is called a relative clause in grammar. In this case, a relative clause acts as the MODIFIER. Now, as usual, here, the MODIFIER (relative clause) follows the HEAD (main clause). So, this is once again a head-initial construction. In English, only a head initial construction is allowed for relative clauses.

This is the same in Hindi as well. For example,  
Hindi sentence: राम जिन्होंने मुझे किताब दी थी वह यहाँ है  
Literal word-by-word translation: Rama who to-me book gave he here is

But Dravidian languages like Tamil only allow a head-final construction where the relative clause comes first and the independent clause comes later. For example,

Tamil sentence: ***புத்தகத்தை எனக்குக் கொடுத்த ராமர் இங்கே இருக்கிறார்***  
Transliteration: ***puttagattai enakkuk koḍutta rāmar ingē irukkirār  *** Literal word-by-word translation: ***Book having-given Rama here is***

What about Sanskrit? It turns out Sanskrit, also like Dravidian languages, mostly follow the head-final construction although rarely it allows a head-initial construction for relative clauses.

Sanskrit sentence: ***यः मम पुस्तकं दत्तवान् रामः अत्र अस्ति  *** Literal word-by-word translation: ***Who to-me book gave Rama here is***

Let us summarise all the information in a table:

[](https://substackcdn.com/image/fetch/$s_!OwEA!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb58925eb-49b9-441a-b515-c7f365cb7bcb_1286x512.heic)

![](https://substackcdn.com/image/fetch/$s_!OwEA!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb58925eb-49b9-441a-b515-c7f365cb7bcb_1286x512.heic)

Comparing the entries of this table, we find that Sanskrit=Tamil and Hindi is in between English and Sanskrit. Like this, we can compare on so many aspects, whether a language is head-initial or head-final. In doing so, we arrive at the same results (verify this with the 6 parameters in the table above):

- European languages prefer more head-initial constructions whereas
  modern Indian languages have more head-final constructions.

- Among the Indian languages, the Dravidian languages and Sanskrit are
  almost always head-final but the modern Indo-Aryan languages (that are
  directly descended from Sanskrit) have developed quite a bit of
  head-initial tendencies (like in reported speech, relative clauses).
  Actually, Sanskrit and Dravidian are almost identical in this regard
  even if belonging to different languages families!

# Where should the head be?

Now which is a better way of communicating - telling the head first and then its modifiers (head initial)? - or telling the head last after describing it completely using the modifiers (head final)? What are the advantages and disadvantages of a head-initial versus head-final communication at least for a noun-adjective case? Think about it for a minute yourself before reading further.

Turns out head-initial constructions where the main matter HEAD comes first and then the MODIFIER, are easier on the mind to understand. Consider the simple phrase that we started with - “the beautiful house” - a head final construction. Syntactically it is not an efficient way to understand and parse because when you hear the words ***the*** and ***beautiful***, there is a brief moment of tension wherein you dunno what the heck is being talked about. This tension is released only after the head word “***house***” is obtained. The moment you understand that it is a “house”, you have to go back for a few milliseconds, and connect the descriptions “the” and “beautiful” to the house to get a complete mental picture of a beautiful house. So, in a head-final construction, you cannot gradually build up your understanding. Initially all the information that you get are about the modifiers that are hanging in the air. But the moment you get the HEAD, you have to go back and connect the MODIFIERs to the HEAD and you get the complete picture. So, in head-final constructions, understanding is not gradually built up but it is built all of a sudden after the HEAD is obtained finally and then by remembering the MODIFIERs and relating them to the HEAD. So, in a head-final construction, the modifiers that come initially are hanging in the air, waiting for the main HEAD to come. But imagine a head-final construction in a language like Basque where the first information that we get is the word “house” that is the HEAD. Now, immediately we can create a mental picture and understanding of a house. Then as the modifier words “the” and “beautiful” enter your head, you gradually refine your mental picture and understanding of the house (HEAD). So, in a head-initial construction, understanding is built gradually without any accumulation or suspense. So they are easier on the head for comprehension. Head-final constructions resemble a magic trick. This is because they keep the reader or the listener in suspense by only revealing at the end of the sentence what it is that’s being discussed about! So, head-final constructions are difficult to comprehend but have an advantage in vivid storytelling by enabling the story-writer to keep the reader in suspense and only revealing finally to the reader what has happened.

So, we see that head-final constructions are heavier on the head but are good for vivid storytelling but head-initial constructions while being light on the head are not good for suspensive narration. Let us now witness this by reading a typical sentence in Tamil, Sanskrit, Hindi and English and see how the head positioning in relative clauses, affects comprehension.

Consider the following sentence in English:

***This article, which I, a student of Sanskrit in Chennai, have written about Panini, who was a genius who lived in ancient India, seems to be getting off to a slow start.***

In this English sentence, everytime more information is added about something, it comes after that something. So, information is gradually built up. But in Tamil, the word order will be almost reverse of that of English because the small small extra bits come first and finally only, the main noun. I now give the above sentence in Tamil in both Tamil and Roman transliteration and a literal word-by-word translation.

TAMIL SENTENCE:

***பண்டைய இந்தியாவில் வாழ்ந்த மேதையான பாணினியைப் பற்றி சென்னையில் சமஸ்கிருத மாணவனாகிய நான் எழுதிய இந்தக் கட்டுரை மெதுவாகத் தொடங்குவதாகத் தெரிகிறது.***

***Paṇṭaiya intiyāvil vāḻnta mētaiyāṉa pāṇiṉiyaip paṟṟi ceṉṉaiyil camaskiruta māṇavaṉākiya nāṉ eḻutiya intak kaṭṭurai metuvākat toṭaṅkuvatākat terikiṟatu.***

WORD-BY-WORD TRANSLATION OF THE TAMIL SENTENCE:

***Ancient in-India lived genius Panini about in-Chennai Sanskrit student I have-written this article slowly starting looks-like-it.***

TRANSLATION:

***This article, which I, a student of Sanskrit in Chennai, have written about Panini, who was a genius who lived in ancient India, seems to be getting off to a slow start.***

Except for the predicate, the relative clauses in the subject for Tamil are exactly reversed as that of English.

ENGLISH ORDER OF SUBJECT: ***This article, which I, a student of Sanskrit in Chennai, have written about Panini, who was a genius who lived in ancient India***

TAMIL ORDER OF SUBJECT: ***Ancient in-India lived genius Panini about in-Chennai Sanskrit student I have-written this article slowly starting looks-like-it.***

Let us now see this sentence in Sanskrit!  
  
SANSKRIT SENTENCE:

प्राचीन-भारते उषितवतः प्रतिभाशालिनः पाणिनेः विषये मया चेन्नैनगर-संस्कृत-छात्रेण लिखितः अयं लेखः मन्दप्रारम्भं कुर्वन् इव दृश्यते।

WORD-BY-WORD TRANSLATION OF THE SANSKRIT SENTENCE:

***in-Ancient-India lived genius Panini about by-me Chennai-Sanskrit-student written this article slowly starting looks-like-it.***

Note how exactly the Tamil word order almost mirrors the Sanskrit one. But Hindi deviates considerably and is close to English.

HINDI SENTENCE: ***यह लेख, जो मैं, चेन्नई में संस्कृत का एक छात्र, ने पाणिनि के बारे में लिखा है, जो प्राचीन भारत में रहने वाले एक प्रतिभाशाली व्यक्ति थे, धीमी गति से शुरू हो रहा है।***

WORD-BY-WORD TRANSLATION OF THE HINDI SENTENCE: ***This article, which I, Chennai in Sanskrit ‘s a student, Panini ‘s about wrote, who ancient India in living a genius person was, slow state with start has***

So, Hindi follows the English more closely than Sanskrit for relative clause syntax and in general for head and modifier ordering!

Now, let us go back to the two sentences presented in the beginning of this article.

> *The view that beating a third-rate Serbian military that for the
> third time in a decade is brutally targeting civilians is hardly worth
> the effort is not based on a lack of understanding of what is
> occurring on the ground.*
>
> *It’s not a lack of understanding of what is occurring on the ground
> that creates the view that it’s hardly worth the effort to beat a
> third-rate Serbian military that is brutally targeting civilians for
> the third time in a decade*

The reason why the first sentence is difficult to comprehend whereas the second sentence is easy is because the first involves a large number of nested head-final constructions.

One of the reasons why Sanskrit literature is difficult to translate is excessive usage of head finals especially through compound words to create vivid effects. For example,  
SANSKRIT PHRASE:***अज्ञाप-रोग-पीडित-धनिकः***  
LITERAL TRANSLATION: Unknown-disease-stricken-richman.  
ACTUAL TRANSLATION : A rich man, struck by an unknown disease

On reading the first word, you don’t get anything. What is unknown here? On reading the second word, you think the phrase is about an unknown disease. But upon seeing the next word, you realise that it talks about pain and suffering and only the last word breaks the suspense that it is about a rich man. Now that you know that the subject is a rich man, you go backwards and figure out that the rich man is suffering due to an unknown disease. But the head-initial English construction “The man stricken by an unknown disease” sounds straightforward and plain. First, you have a solid idea that the subject is a man. Then you know that he is suffering. Then, you get that he is suffering from an unknown disease (a rare instance where head final construction is followed in English where the noun comes later after the adjective that modifies it).

This principle in linguistics where head-initial constructions are easier for cognition is called the “**light-before-heavy**” principle. This is because, in a head-final construction, you are holding a heavy MODIFIER together for a long time at once, waiting for the single HEAD (lighter one) to finally come. But in a head-initial construction, you are introduced to the short HEAD first itself and gradually build up the load of its modifiers.

# Panini and Light-Before-Heavy

This light-before-heavy principle is also important in mere listing of items. For example, why do we say “bread and butter” not not “butter and bread”? Look at the following lists,

- bread and butter (not: butter and bread!)

- Tom, Dick and Harry (not: Harry, Dick and Tom!)

- light and darkness (not: darkness and light)

- Tit for Tat (not: tat for tit)

There are many rules governing the ordering of the constituents in a list. Such lists are common in Sanskrit too and are called by the name of **dvandva samāsa**. It turns out that in such listings too, the light before heavy rule applies. Items with lower number of syllables appear first!! That is why it is “bread” (one syllabled word) and then butter (two syllabled word)! Words with lesser number of syllables (light) come before ones with higher number of syllables (heavy). What if two words are of equal syllable numbers? Then refer this paper to decide. You will then get why we say “***Hari-hara***” and not “***Hara-Hari***”! This principle of light-before-heavy was discovered by none other than Panini himself. To quote eminent language psychologist **Steven Pinker** from his book “***The Sense of Style***”: ( I highly recommend all books by Steven Pinker - my most favourite author in linguistics)

*“Human comprehension demands topic before comment and given before new…The Scottish prayer asks the Lord to deliver us from “ghoulies and ghosties and long-leggedy beasties and things that go bump in the night”—not from “things that go bump in the night and long-leggedy beasties and ghoulies and ghosties.” The order fits with our cognitive processes: it’s taxing to work on a big heavy phrase (things that go bump in the night) while you are holding in memory an incomplete bigger phrase it’s part of (in this case, the four-part coordination embracing things, beasties, ghoulies, and ghosties). A big heavy phrase is easier to handle if it comes at the end, when your work assembling the overarching phrase is done and nothing else is on your mind. (It’s another version of the advice to prefer right-branching trees over left-branching and centre-embedded ones.) Light-before-heavy is one of the oldest principles in linguistics, having been discovered in the fourth century BCE by the Sanskrit grammarian Pāṇini It often guides the intuitions of writers when they have to choose an order for items in a list, as in life, liberty, and the pursuit of happiness; The Wild, The Innocent, and The E Street Shuffle; and Faster than a speeding bullet! More powerful than a locomotive! Able to leap tall buildings in a single bound! Topic, then comment. Given, then new”.*

In fact, in linguistics, this is called Panini’s law. <https://en.wiktionary.org/wiki/Panini%27s_law>

Panini mentions this in Astadhyayi [2.2.34](https://ashtadhyayi.com/sutraani/2/2/34) - अल्पाच्तरम् . S.K.Vasu’s commentary reads *“In a द्वन्द्व compound, that word-form which has fewer vowels, is to be placed first. Thus प्लक्ष +न्यग्रोध = प्लक्षन्यग्रोधौ ; (not न्यग्रोधप्लक्षौ)”*!!

I sincerely hope that you have enjoyed this article and got a spark. What I have provided is just a small drop in the ocean of Paninian grammar and I urge you to explore this vast treasure trove of knowledge.

11

4

3

Share
