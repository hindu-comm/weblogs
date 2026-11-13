+++
title = "How Systems Sustain"
full_title = "How Systems Sustain Themselves The Principle of Bootstrapping in Programming"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/how-languages-teach-and-sustain-themselves"
date = "2026-10-02"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/how-languages-teach-and-sustain-themselves).

How Systems Sustain Themselves : The Principle of Bootstrapping in Programming 

# How Systems Sustain Themselves : The Principle of Bootstrapping in Programming

### In this article, I am going to write on a small topic that has excited me a lot in my exploration of computer science which is bootstrapping.

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Oct 02, 2026



21



2



5

Share

[](https://substackcdn.com/image/fetch/$s_!6n1H!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff872226f-f316-4a3a-a107-61ea64ed0a9c_625x621.jpeg)

![](https://substackcdn.com/image/fetch/$s_!6n1H!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff872226f-f316-4a3a-a107-61ea64ed0a9c_625x621.jpeg)





Figure : A dragon-like ouroboros in a 1478 drawing in an alchemical tract.

Figure : The **ouroboros** is an ancient symbol depicting a snake or dragon eating its own tail. The ouroboros entered Western tradition via ancient Egyptian iconography and the Greek magical tradition. It was adopted as a symbol in Gnosticism, Hermeticism, and alchemy. The term derives from Ancient Greek **οὐροβόρος**, from **οὐρά** **oura** ‘tail’ plus -**βόρος** -**boros** ‘-eating’. The ouroboros is often interpreted as a symbol for eternal cyclic renewal or a cycle of life, death and rebirth; the snake’s skin sloughing symbolises the transmigration of souls. The snake biting its own tail is a fertility symbol in some religions: the tail is a phallic symbol and the mouth is a yonic or womb-like symbol.

In Hindu mythology too, we find the symbolism of the ouroboros within the concept of **kuṇḍalinī**. An excerpt from the **Yogakuṇḍali Upanisad**, a late Vedic Sanskrit text, reads as follows:

> *The divine power, **Kuṇḍalinī**, shines like the stem of a young
> lotus; like a snake, coiled round upon herself she holds her tail in
> her mouth and lies resting half asleep at the base of the body.’*
>
> **Yogakuṇḍali Upaniṣad**

[](https://substackcdn.com/image/fetch/$s_!pp9H!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31718dda-b6a6-4611-aae1-73fdee407316_568x616.png)

![Ouroboros unclear if it's eating its own tail, or sh\*tting out a new snake](https://substackcdn.com/image/fetch/$s_!pp9H!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F31718dda-b6a6-4611-aae1-73fdee407316_568x616.png "Ouroboros unclear if it's eating its own tail, or sh*tting out a new snake")





What is the connection between this ancient symbol of a snake eating its own tail and the topic of bootstrapping in modern software engineering? Get through the end of this article to understand why!

Every high-level programming language bridges a vast abstraction gap: humans think in structured, mathematical logic, but silicon processors execute only primitive binary instructions. You cannot leap across that chasm separating these two very different levels of thinking in a single step. How else do you cross the chasm then? The answer lies in one of the most elegant, self-sustaining loops in human engineering: **bootstrapping**. It is the ultimate "chicken-and-egg" puzzle of the digital age; a silent, recursive magic where a system uses primitive scaffolding to forge a more powerful successor, eventually kicking away the ladder entirely to stand completely on its own.

I am not an expert in computer programming. I have begun studying and experimenting with it since a few months only. Yet, there is something that I learnt in my exploration which I felt was too good to be known only in the circle of software engineers and programmers, and have to be appreciated by a general audience. It is what is called as **bootstrapping** in the computer science community and it blew my mind especially given my interests in mathematics and linguistics as well. I also made a linguistic analogy to explain it to myself and understand it. But, to my surprise, I found it nowhere in textbooks. I will first start with this analogy and then go on to its computing counterpart. This article is split into three parts.

1.  Translation between Natural Languages

2.  Basics of Programming Languages and Compilers

3.  Translation between Programming Languages

------------------------------------------------------------------------

# Klingon to English : Self-Sustaining Translators



Imagine that the members of the alien race of **Klingon** in the **Star Trek** Universe want to talk to humans (actually just Americans because as I learnt from Hollywood, aliens love to invade only America! ) and instruct them to do something that they want. Imagine that human brains are not wired in such a way to understand and use this alien Klingon language by mere exposure (like how humans pick up any other human language they do not know with adequate exposure and immersion) and hence have to be explicitly instructed in English (assume that the Americans whom the aliens interact with know only English, which is not an unreasonable assumption!) regarding how to translate from Klingon to English. So, there has to be an instruction manual for humans written in English that tells how to translate from Klingon to English. But, there is another problem. The Klingon race can understand and operate in English but just that they find it too cumbersome to use it because they find it too long (single words in Klingon translate to dozens of long words into English) and sucks up a lot of their cognitive energy so that using a large amount of English leads to a lot of mental exhaustion. So, these Klingon aliens want to minimise their usage of English as much as possible despite their brains being advanced enough to grasp and use it completely just by exposure to humans. So, we are faced with two competing constraints :

1.  The alien who understands English and is capable of using it but
    finds it mentally exhausting because it is very lengthy unlike his
    compressed Klingon language

2.  The human who simply cannot just pick up Klingon by just getting
    exposed and immersed into the language and who needs an instruction
    manual in English that tells how to translate Klingon into English

With this being the case, the Klingons cannot write an entire long instruction manual in English that instructs humans as to how to translate from Klingon to English. That is out of the picture completely as they want to minimise their usage of English and use their own Klingon language as much as possible. But, the human being needs every translation instruction in English and his brain is not advanced enough to naturally use and understand Klingon. The Klingons come up with a solution to this problem that ensures that the humans receive all their translation instructions in English while they themselves use English only as much sparingly as possible.

The Klingons split their language into three levels - **Basic**, **Intermediate**, and **Complete**. In the Basic level, the vocabulary is limited, say only a set of 500 words, and only a restricted set of grammatical and syntactical constructs are employed. In the Intermediate level, the vocabulary expands to a set of 5000 words in total and longer and more complex expressions are possible to be conveyed by expanding the grammatical and syntactical repertoire. In the final and third Complete level, the full range of words (say 50,000 words), grammar (all tenses, numbers, moods ….) , and syntax of the Klingon language is mastered. This is not at all strange and whenever you have learnt any foreign language, you yourself can map your proficiency in that language to three levels. If you are familiar with the CEFR system for European languages, these correspond to the levels A, B, and C which are called as **Basic**, **Intermediate**, and **Advanced**. Thus, so far, nothing complex has been introduced.

Now, the alien Klingons write their first instruction book in English that tells humans how to translate basic Klingon into English. This is the only time that the Klingons will write something in English. Remember that the Klingons need to minimise their English usage as much as possible. So, they only write the instruction set in English to teach Basic Klingon which is hence a very short book as it teaches only the basics. This is depicted below.

[](https://substackcdn.com/image/fetch/$s_!2NLv!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99dc7f7e-d281-4659-a152-24fda02e033c_1356x850.png)

![](https://substackcdn.com/image/fetch/$s_!2NLv!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F99dc7f7e-d281-4659-a152-24fda02e033c_1356x850.png)





Now, this instruction book can be read by humans since it is written in English. Reading this instruction book enables humans to translate Basic Klingon to English, but this is not enough.

But, the aliens now realise that the humans now would know Basic Klingon after reading this. So, they now write a second book in Basic Klingon that now instructs how to translate from Intermediate Klingon into English (all books written in the various stages of Klingon are shown in brown while those in English are shown in black) .

[](https://substackcdn.com/image/fetch/$s_!Sa4S!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51aa5328-5a0c-4d19-a58d-7d86386e85d3_1352x976.png)

![](https://substackcdn.com/image/fetch/$s_!Sa4S!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F51aa5328-5a0c-4d19-a58d-7d86386e85d3_1352x976.png)





So, this second book now instructs as to how to translate from Intermediate Klingon to English. Note that this book that teaches Intermediate Klingon will be longer. But, the aliens write this in Basic Klingon and hence it is not difficult for them to write (as it is not in English, which is a cumbersome language for them to handle). Note that the aliens have written this brown book teaching Intermediate Klingon in the Basic Klingon language and hence cannot directly be used by humans. But, humans already have the first book that instructs how to translate Basic Klingon into English. So, using the first book, they can translate the second book into English which is as follows :

[](https://substackcdn.com/image/fetch/$s_!_M62!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d5fec07-913d-4838-8b2b-fa18cb2db481_1360x1092.png)

![](https://substackcdn.com/image/fetch/$s_!_M62!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d5fec07-913d-4838-8b2b-fa18cb2db481_1360x1092.png)





So, after this translation of Book 2 using Book 1, we get a second book in English that instructs humans how to translate Intermediate Klingon into English. Note that after we get the English version of this second book, we can throw away the first book ( (that teaches translating just Basic Klingon into English) because we now have the second book in English, which tells us how to translate the much larger language of Intermediate Klingon into English. Let me illustrate what we have done so far.

[](https://substackcdn.com/image/fetch/$s_!xGrn!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b80c250-b6ef-4dcd-9ec7-c478449d166f_1316x982.png)

![](https://substackcdn.com/image/fetch/$s_!xGrn!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0b80c250-b6ef-4dcd-9ec7-c478449d166f_1316x982.png)





So, we now have two books. One originally written in Basic Klingon by the aliens that tells how to translate Intermediate Klingon into English. And its English translation (that also tells how to translate Intermediate Klingon into English) through Book 1 that is later thrown away after we get the translation of the Book 2.

Now, the humans have an English book that tells how to translate Intermediate Klingon into English. So, the aliens now write another third book in Intermediate Klingon that instructs how to translate Complete Klingon into English. It is again much easier for them to write as it is written in Intermediate Klingon.

[](https://substackcdn.com/image/fetch/$s_!U-ES!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73afc414-e90a-4eb1-8fd5-6da008202c64_1386x840.png)

![](https://substackcdn.com/image/fetch/$s_!U-ES!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F73afc414-e90a-4eb1-8fd5-6da008202c64_1386x840.png)





So, this third book now instructs as to how to translate from Complete Klingon to English. Note that this book that teaches Complete Klingon will be longer. But, the aliens write this in Intermediate Klingon and hence it is not difficult for them to write (as it is still not in cumbersome English). Note that the aliens have written this brown book teaching Complete Klingon in the Intermediate Klingon language and hence cannot directly be used by humans. But, humans already have the translation of the second book that instructs in English, how to translate Intermediate Klingon into English. So, using the translation instructions of the second book, they can now translate the third book (written in Intermediate Klingon) into English which is as follows :

[](https://substackcdn.com/image/fetch/$s_!xqMl!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F962ba5e6-4f55-4c4e-a2d3-55fcfaf70287_1360x1114.png)

![](https://substackcdn.com/image/fetch/$s_!xqMl!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F962ba5e6-4f55-4c4e-a2d3-55fcfaf70287_1360x1114.png)





So, after this translation of Book 3 using the English translation of Book 2, we get a third book in English that instructs humans how to translate Complete Klingon into English. Note that after we get the English version of this third book, we can throw away the English translation of the second book (that teaches translating just Intermediate Klingon into English) because we now have the third book in English, which tells us how to translate the much larger language of Advanced Klingon into English. Let me illustrate what we have done so far.

[](https://substackcdn.com/image/fetch/$s_!_EtP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2aa44f6-b135-4989-92e2-9199768e7db4_1292x956.png)

![](https://substackcdn.com/image/fetch/$s_!_EtP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa2aa44f6-b135-4989-92e2-9199768e7db4_1292x956.png)





So, now the Klingons had written a book in Intermediate Klingon to instruct humans how to translate Complete Klingon to English. The humans have this book translated by following the translation instructions of the translation of the second book that teaches how to translate from Intermediate Klingon (the language of the third book) into English. Thus, after translation, they now have an English book that instructs them how to translate Complete Klingon into English.

Now, this cycle can continue. Let us assume that a hundred years pass and the Klingon language has acquired new grammatical techniques and new word and is updated. Let this new language be called Updated Klingon. Then, again not to worry at all. The aliens can now write a fourth book in the Complete Klingon language (the un-updated language) that tells how to translate Updated Klingon into English. The humans already have the English translation of the third book which instructs how to translate Complete Klingon into English. They can hence use this third book to translate the fourth book written in Complete Klingon into English, So, this translated fourth book will now contain the instructions on how to translate Updated Klingon into English. After getting this, they can now throw away the translation of the third book and just keep the translation of the fourth book which contains the instructions on how to translate the most current and updated version of Klingon into English.

[](https://substackcdn.com/image/fetch/$s_!0tfD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d1821b6-b554-49fb-9496-5bc2977c044d_1300x974.png)

![](https://substackcdn.com/image/fetch/$s_!0tfD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2d1821b6-b554-49fb-9496-5bc2977c044d_1300x974.png)





This mechanism is technically what people would call as **self-sustaining**. Why? Because, the intermediate translators can be thrown away once the translation of the most updated version of the language is gotten. Also, after the very first seed stage, there is no need at all to use English by the aliens. They can write translations for all future updates in their own current version of the Klingon language only; and then have them translated into English using the most current English translated version of the current book that tells how to translate the current language into English.

Thus, all future updates to the translation instructions due to language updations can be written by the aliens in their own current version of the Klingon and have them translated to English using the English translated instructions for the current language. After this English translated instructions for the updated language is gotten, the previous translation for the previously current language can be thrown away.

------------------------------------------------------------------------

# The Computer Context



The very first electronic computers were gigantic monstrosities occupying a space and consuming power equivalent to that of a factory and costed millions of dollars in the 1940s. But, they had much less computing power than even the simplest primitive cellphones fifteen years ago and were much slower than even modern pocket calculators.

[](https://substackcdn.com/image/fetch/$s_!YB8n!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd02aa881-b4ef-4db6-a2c1-60b087d13301_630x455.jpeg)

![](https://substackcdn.com/image/fetch/$s_!YB8n!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd02aa881-b4ef-4db6-a2c1-60b087d13301_630x455.jpeg)





**ENIAC** (**Electronic Numerical Integrator and Computer**) was the first programmable, electronic, general-purpose digital computer, completed in 1945. In this picture, Cpl. Irwin Goldstein (foreground) sets the switches on one of ENIAC's function tables at the Moore School of Electrical Engineering. (U.S. Army photo, 1946)

The programmers who instructed these machines coded in what is technically called “**machine language**” which is a sequence of 0s and 1s that directly controls the processor in all its details, causing it to perform simple operations on data like addition, comparison, insertion, moving, and deletion at appropriate times. Writing a program at this level of detail is a tedious task but this was indeed the practice because these early programmers believed that their own time (spent grudging lots of 0s and 1s) was less valuable than the computer’s. For example, in a modern programming language like Python, if you want to add two numbers, one simply defines two variables like “a” and “b” and then define the sum as “sum = a + b” and the command to print the sum is added. Then, pressing enter key and running the program instantly gives the answer. The following program is in the Python programming language to add two numbers 56 and 45.

``` shiki a = 56 
b = 45 
sum = a + b print(sum) ```





If you compile this, you get the result on the screen as

``` shiki 101 ```





Even if you do not know the basics of programming, you can intuitively understand what the simple program above does. It is simple to code by a programmer and easy to understand by anyone who sees it (in this particular case above, the program is so simple that even a layman who has no knowledge of computer programming can understand what this program is doing).

But, if you think about it deeply, there are lot of things going on in the background when you run this program. First of all, one has to decide how many bytes of memory have to be allocated in storing the two numbers to be added. Then, they have to be converted into binary representation involving just 0s and 1s. Then, one has to decide the memory locations in which these two numbers “a” and “b” represented in binary have to be stored. Then, one has to copy and move these two numbers into the core of the processor where the operations happen. The first number should be copied and moved to the **accumulator** (**Register A**) of the processor and the second number should be copied and moved to another **register** of the processor (say it is moved to **register B** which is free). Then, the addition operation needs to be triggered between the contents of the accumulator (Register A) and the register B. After addition, the accumulator is rewritten with the sum. Then, the program should contain another instruction to copy the content of this accumulator (which now has the sum) and move it to be stored in another memory location. Then, another instruction should be given to read out the contents of this memory and print it on the display after converting it from binary to decimal representation. Specifying a complex program at this much level of detail is mind-numbingly pain for anyone. Consider a super complex program where additions are just a small part among the thousands of other operations. Then, every time one encounters addition, one cannot think about these **low-level operations** like converting numbers to binary, and **low level decisions** like deciding where to store the numbers to be added (scanning the available free memory locations and selecting two among them), moving one number (which one?) to the accumulator, and the other number to a register that is free (what registers are free and among them, where to put?), and after the addition, copying and moving the sum from the accumulator to another free memory location (what locations are free and among them, where to store?). Thus, even a simple program to add two numbers becomes complicated and non-obvious to write in this detailed level. Programming at this much level of detail is called **machine language** or **assembly language**.

Actually, these two terms are not equivalent. **Machine language** consists of raw strings of 0s and 1s that represent the low-level instructions that the processor of the computer accepts for carrying out the requisite instructions. **Assembly language** consists of mnemonics to represent these elementary instructions in a human friendly manner.

For example, to add the numbers between the accumulator and the register B, the raw machine language instruction in the Machine language of the Intel 8085 processor would be `10000000`. In Assembly language, this would be abbreviated as `ADD B`. Note that both

`10000000`

`ADD B`

represent the exact same instruction. The instruction is to add the contents of the accumulator (Register A) and Register B with the sum rewritten in the accumulator (Register A) only. Just that ADD B is a human-friendly representation or an abbreviation or a mnemonic of it. Ultimately, programs called **assemblers** were written in the machine language that convert or translate these assembly language instructions to the standard binary language of the machine. Assemblers were eventually augmented with elaborate “**macro-expansion**” facilities to permit programmers to define even more sophisticated abbreviations for common sequences of instructions. The correspondence between assembly language and machine language however remains obvious and explicit, however.

Programming in Assembly language is still a machine-centred enterprise where the exact sequence of low-level decisions have to be explicitly thought out by the programmer and coded: and assembly language programmers too thought and have to think in terms of the explicit and exact sequence of instructions that the machine would actually execute. Just that they are represented in human friendly mnemonics and abbreviations.

As computers evolved with many competing designs, it became increasingly frustrating to have to rewrite programs for every new machine in the machine language. Even in Assembly language, it soon became increasingly difficult for human programmers to keep track of the wealth of detail in complex assembly language programs. We have just seen above that even a simple addition of two numbers involves dozens of steps that involve lots of low-level operations and decision making especially in memory management. People began to wish for a programming language that was both

- **machine-independent** : so that the same code could run on any
  machine

- **high-level :** so that frequent operations (like addition which we
  saw above) could be simple and could be expressed in something more
  closely resembling mathematical formulae (like we saw in the Python
  language code).

These wishes led in the mid-1950s to the development of the first commercially viable high-level programming language called **Fortran**. Other high-level languages soon followed, notably **Lisp** and **Algol** and eventually, also the **C** language (which is popular today). But, this does not mean that the low-level decisions can be ignored. There has to be some mechanism that translates these high-level commands into machine-level detailed sequence of instructions and manage memory for carrying out the tasks of the program.

The machine language program that translates these high-level commands in the high-level programming language to the appropriate sequence of machine-level commands is called the **compiler**. Note that compilers are substantially more complicated than assemblers because the one-to-one correspondence between source and target operations no longer exists when the source is a high-level language. High-level programming languages like C, Fortran, and Python, are not simply elaborate abbreviations of the machine language commands like Assembly language. Lot of machine level details are abstracted out in high-level programming languages. For instance, even in this simple program to add two numbers, there are a lot of options to choose from. Where to store the two numbers to be added? This involves checking what all memory locations are free (there are thousands of other things going on inside your computer apart from your program and they all demand and occupy some part of the computer memory for storage of whatever is required for them) and then choosing two sets of free locations to store the two numbers. Similarly, for addition, one of the numbers to be added has to be copied and sent to Register A (accumulator) and one has to decide which of the two has to be sent. The second number to be added has to be sent to another register but again there are lots of registers to choose from (checking which among them is free and allocating one among them). When the sum is updated into the accumulator, again the decision has to be made regarding at what memory location it has to be copied so that it can be stored there permanently. So, translating from a high-level programming language to the low-level machine language is not a matter of expanding abbreviations but also involves a lot of complex managerial and executive decisions that also involve interactions with other programs running in the computer. In a high level, if you instruct your son to “buy two pumpkins for the house”, this may look like a simple command. But even this involves a lot of low-level decisions like knowing where the cash register is for buying the pumpkin, estimating the price of the two pumpkins, knowing which shops in the neighbourhood sells pumpkins, what to choose from, how to know if a pumpkin is good by looking at it, going to the shop and buying it, and figuring out where to keep the purchased pumpkins in the house. But, we humans are able to easily translate these high-level commands to low-level actions by awareness of the context and the intuition that we developed. It is these things precisely that the computer cannot do. Every low-level instruction needs to be specified to it in mind-numbing detail and nothing can be left to “context” or “decide for yourself” including handling all possible contingencies.

But, this translation from a high-level programming language into the low-level machine language has to be done because machine language is the only language machines can understand. One has to write a code in the machine language only that instructs the computer how to translate a program containing a sequence of high-level commands to the appropriate sequence of low-level machine language instructions that get the job demanded by the program to be done as efficiently as possible under all possible scenarios. This is what a compiler does. It is a set of machine language instructions that scans the entire high-level program and translates to the appropriate sequence of machine language instructions.

Hence, to run a high-level programming language (say C), one has to write a compiler for the language which is basically a gigantic instruction set written in the machine language to translate any legit high-level program to the exact sequence of low-level machine tasks. It is not that humans cannot understand machine language but just that they want to avoid using it as much as possible because it is mind-numbingly long and tedious to handle. This is the exact problem faced in the Klingon assembly. The humans here are machines which can only understand machine language and have to be explicitly instructed how exactly to translate. The aliens here are the humans who can understand machine language but find it too tedious to think and write in it and hence want to minimise its usage as much as possible. So, programmers who write compilers adopt the same strategy that we saw adopted by the Klingon aliens to instruct humans.

------------------------------------------------------------------------

# Bootstrapping Compilers



Let us say that we are designing a brand new hypothetical programming language called **Pop**. So, I have to write a compiler for this language Pop that converts a Pop code into a machine language code. I obviously have to ultimately produce a gigantic instruction set in machine language that reads a Pop program and converts it into a sequence of machine language instructions. But, I do not want to write the entire compiler from scratch myself in machine language as it is extremely tedious. So, I divide my Pop language into three levels.

1.  Basic Pop

2.  Intermediate Pop

3.  Complete Pop

This is the same approach I followed in the first section regarding writing an instruction set for Klingon to English translator. The Basic Pop contains only the very basic commands and expressions in the Pop language. So, I strain myself hard to write a small compiler in machine language for that compiles Basic Pop.

[](https://substackcdn.com/image/fetch/$s_!1HB6!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F285e922d-08b2-4c81-b190-a6f52771384c_1392x1068.png)

![](https://substackcdn.com/image/fetch/$s_!1HB6!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F285e922d-08b2-4c81-b190-a6f52771384c_1392x1068.png)





Programmers prefer to represent this in terms of what are called **T-diagrams** or **Tombstone diagrams** shown below. The language in which the compiler itself is written is shown at the bottom inside yellow. The source language that the compiler translates from is written on the left at the top and the destination language that the compiler translates into is written on the right at the top, both inside blue.

[](https://substackcdn.com/image/fetch/$s_!haws!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e0fda0f-5753-411d-9f58-d3818323e49a_644x400.png)

![](https://substackcdn.com/image/fetch/$s_!haws!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2e0fda0f-5753-411d-9f58-d3818323e49a_644x400.png)





For the first compiler that compiles Basic Pop, its specific diagram is shown below. It is shown in grey because it is written in machine language.

[](https://substackcdn.com/image/fetch/$s_!g7MM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11382aa5-3fdc-4cf4-bfbd-9e3df5553e7d_648x468.png)

![](https://substackcdn.com/image/fetch/$s_!g7MM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11382aa5-3fdc-4cf4-bfbd-9e3df5553e7d_648x468.png)





Now, we design a second compiler for Intermediate Pop. But, we write it not in machine language but in Basic Pop.

[](https://substackcdn.com/image/fetch/$s_!8Ssc!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ef5fec2-5b23-4410-bada-0833d88e8074_1310x1130.png)

![](https://substackcdn.com/image/fetch/$s_!8Ssc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8ef5fec2-5b23-4410-bada-0833d88e8074_1310x1130.png)





The T-diagram corresponding to the above compiler is given below.

[](https://substackcdn.com/image/fetch/$s_!bzqq!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e568079-d26b-4fa5-acbd-77d789376048_662x474.png)

![](https://substackcdn.com/image/fetch/$s_!bzqq!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e568079-d26b-4fa5-acbd-77d789376048_662x474.png)





But, this human written second compiler cannot be understood by the machine as it is written in Basic Pop. But, we can send this compiler code in Basic Pop into the first compiler which will translate it into machine language.

[](https://substackcdn.com/image/fetch/$s_!THFT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2155d4b-a10d-45ac-a15d-597e98023faf_638x590.png)

![](https://substackcdn.com/image/fetch/$s_!THFT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2155d4b-a10d-45ac-a15d-597e98023faf_638x590.png)





So, we now have a translated compiler 2 that instructs in machine language how to convert intermediate Pop commands into the appropriate machine language commands. After we got this, we can throw away the first compiler since we now have got a better one. We need to only keep this translated second compiler.

[](https://substackcdn.com/image/fetch/$s_!To3z!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57906b0a-a826-432b-bbbf-b33040063d63_634x460.png)

![](https://substackcdn.com/image/fetch/$s_!To3z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F57906b0a-a826-432b-bbbf-b33040063d63_634x460.png)





Now, we write a third compiler in Intermediate Pop that instructs how to translate Complete Pop into machine language. This compiler itself cannot be run by the machine as it is written in Intermediate Pop. But worry not, we got the translated second compiler in machine language that can translate from Intermediate Pop. So, we send the third compiler written in Intermediate Pop to the translated second compiler which translates into machine language and instructs the machine how to translate Complete Pop into machine language.

[](https://substackcdn.com/image/fetch/$s_!fP4X!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff3204c43-d98a-4d45-82f1-8d0d3286e349_648x606.png)

![](https://substackcdn.com/image/fetch/$s_!fP4X!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff3204c43-d98a-4d45-82f1-8d0d3286e349_648x606.png)





Thus, this translated third compiler contains all the instructions in machine language as to how to translate from Complete Pop to machine language and hence it is the full blown compiler for the Pop language that we originally wanted. But, we did not write this entire compiler in machine language and instead bootstrapped our way out after writing only the very basic first compiler in the machine language and then we wrote later compilers in our own language and kept translating that into machine language from the compiler that we translated in the immediately preceding previous stage.

Any updates to the language Pop can also be handled in a similar way as shown below.

[](https://substackcdn.com/image/fetch/$s_!O22k!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1034d87-608e-482d-8454-dd3bd638eb9e_700x592.png)

![](https://substackcdn.com/image/fetch/$s_!O22k!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe1034d87-608e-482d-8454-dd3bd638eb9e_700x592.png)





This mechanism is once again, if we recall from the first section, technically what people would call as **self-sustaining**. Why? Because, all the intermediate compilers can be thrown away once the translation of the most updated version of the language is gotten after passing it through the immediately preceding previous translated compiler. Also, after the very first seed stage, there is no need at all to use machine language to write the later compilers. Humans can write translations for all future updates in their own current version of the high-level programming language only; and then have them translated into machine language using the most current machine translated version of the current compiler that tells how to translate the current language into machine language.

> Hence, bootstrapping is an extremely powerful technique in compiler
> design that enables the creation of advanced or updated compilers by
> starting with a simple, basic version. This process allows for gradual
> improvement and self-compilation, making the development of complex
> compilers more efficient over time. It simplifies the development
> cycle by enabling incremental improvements, and its ability to
> generate compilers that are portable across different systems makes it
> a valuable tool.

------------------------------------------------------------------------

Ultimately, bootstrapping reveals a profound structural truth about complex systems: evolution is rarely a direct leap to the summit; it is an iterative ladder of self-creation. Whether teaching a human to translate an alien tongue or teaching a processor to understand a high-level programming language, the underlying architecture remains the same. You construct a primitive seed, use it to forge a more powerful successor, and discard the scaffoldings after the system becomes self-sustaining. The historical artefacts fade into the background, leaving behind a living engine capable of maintaining, updating, and rewriting its own future. In the end, the most enduring systems are not those built by external hands, but those that learned how to build themselves.

**Much like the ancient symbol of the Ouroboros that was shown at the beginning of this article, where the serpent endlessly consumes its own tail to sustain its life, compiler bootstrapping is the ultimate computational strange loop like the snake. In this recursive dance, the software consumes its own source code to forge its own successor, closing the loop between creator and creation. Once the scaffolding is kicked away and the system achieves self-sustainability, it becomes a closed, autonomous engine of logic that needs no external world to grow. It is a rare and striking testament to how complex systems pull themselves up by their own foundations, looking into their own reflection and learning to walk entirely on their own.**

P.S. If you enjoyed this article and want to know more about the range of topics that interest me (spoiler : it is a lot!) and see an organised list of my articles published in Substack so far, click below.

[](https://ramaseshanchandrasekaran.substack.com/p/master-post-post-of-posts)

## Master Post - Post of posts

[Rama Seshan Chandrasekaran](https://substack.com/profile/195425058-rama-seshan-chandrasekaran)

·

September 25, 2025

Here, I update the list of all my posts on Substack topicwise

[](https://ramaseshanchandrasekaran.substack.com/p/master-post-post-of-posts)

Read full story

------------------------------------------------------------------------

#### Subscribe to Rama’s Substack

By Rama Seshan Chandrasekaran · Launched a year ago

My personal Substack

Subscribe

By subscribing, you agree to Substack's [Terms of Use](https://substack.com/tos), and acknowledge its [Information Collection Notice](https://substack.com/ccpa#personal-data-collected) and [Privacy Policy](https://substack.com/privacy).

[](https://substack.com/profile/410367201-govind-kumar-upadhyay)

![govind Kumar upadhyay's avatar](https://substackcdn.com/image/fetch/$s_!OuCH!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8e038f39-d09a-4cbc-8ca3-bd8d182d1668_3120x3119.jpeg)

[](https://substack.com/profile/175607674-gajah)

![𓃰 गज (Gajaḥ) 𓃰's avatar](https://substackcdn.com/image/fetch/$s_!0FKq!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4cce856-fe09-4acb-aca7-abd3fcf353ae_4184x3152.jpeg)

[](https://substack.com/profile/7409416-che-naik)

![Ché Naik's avatar](https://substackcdn.com/image/fetch/$s_!IxR5!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19c0010d-953b-42ea-ba29-d7ae428e3a3d_1660x1660.jpeg)

[](https://substack.com/profile/29518863-sanjay-bhatnagar)

![Sanjay Bhatnagar's avatar](https://substackcdn.com/image/fetch/$s_!0EEY!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1a0d8ee3-8c69-40df-8a4f-c2d0df07b35c_144x144.png)

[](https://substack.com/profile/44210558-akshat-maurya)

![Akshat Maurya's avatar](https://substackcdn.com/image/fetch/$s_!X7EC!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6de8e062-901e-45f9-b182-42c5e9a310f3_646x862.jpeg)

21 Likes∙

[5 Restacks](https://substack.com/note/p-218328352/restacks?utm_source=substack&utm_content=facepile-restacks)



21



2



5

Share
