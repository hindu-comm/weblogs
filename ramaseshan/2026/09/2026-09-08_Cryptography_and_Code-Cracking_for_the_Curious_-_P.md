+++
title = "Cryptography and"
full_title = "Cryptography and CodeCracking for the Curious Part 1 From Antiquity to WWII"
upstream_url = "https://ramaseshanchandrasekaran.substack.com/p/cryptography-and-code-cracking-for"
date = "2026-09-08"
+++
Source: [here](https://ramaseshanchandrasekaran.substack.com/p/cryptography-and-code-cracking-for).

Cryptography and Code-Cracking for the Curious - Part 1 : From Antiquity to WWII

# Cryptography and Code-Cracking for the Curious - Part 1 : From Antiquity to WWII

### I give a historically organised two-article introduction to cryptography for the general audience who are curious as to what algorithms and mathematics lie behind securing messages and cracking them.

[](https://substack.com/@ramaseshanc)

![Rama Seshan Chandrasekaran's avatar](https://substackcdn.com/image/fetch/$s_!ZHOm!,w_36,h_36,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F11e50d60-b811-4831-8bbc-4d320762e60b_96x96.png)

[Rama Seshan Chandrasekaran](https://substack.com/@ramaseshanc)

Sep 09, 2026



17





6

Share

[](https://substackcdn.com/image/fetch/$s_!4Shg!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F825aa5e4-e9b8-4d99-850f-6f9fe321d444_1024x572.jpeg)

![](https://substackcdn.com/image/fetch/$s_!4Shg!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F825aa5e4-e9b8-4d99-850f-6f9fe321d444_1024x572.jpeg)





Are you curious about what Whatsapp exactly means when they say that your messages are protected by end-to-end encryption? Are you interested in knowing what exactly is it that mathematicians like **Marian Rejewski** and **Alan Turing** did to crack the **Enigma** machine (used in the encryption of messages by Nazi Germany in their strategic communications) that played a key role in hastening the victory of the Allied forces in the Second World War? Do you want to read a comprehensive treatment regarding the history of cryptography from those used by ancient Roman commanders and recommended to women by the ancient Indian text of *Kāmasūtra*, to modern gangsters and modern encryption algorithms? Like me, do you want to feel a bit like a RAW detective while learning about cryptograms and solving interesting problems based on historical cases? If your answer is yes to any or all of the above questions, you have come to the right place. The first article here deals with the history of cryptography until World War II.

**Note on organisation** : This article cannot claim to be exhaustive in covering all the interesting historical examples in cryptography. The sections are organised by the nature of the techniques used. One example is discussed in detail to anchor the method and then at the end of that section, interesting other historical examples based on the same technique as the anchor example are pointed out along with exercises to try for yourself (the solutions to which are given at the end).

------------------------------------------------------------------------

# Introduction, Basic Vocabulary & Setting



The aim of any cryptographic system is to disguise confidential information in such a way that its meaning is unintelligible to any person other than the intended recipient. This information may be stored in a database or may be transmitted through a communication channel. In either case, the fact that a message is encrypted does not mean that unauthorised people cannot access it; but what the encryption is supposed to guarantee is that when they do access it, they will not be able to understand what they see.

### Components of a Cryptosystem



Here are some basic terms used in discussions regarding the subject matter.

- **Plaintext** / **Message** : The original message in a natural
  language that is to be protected.

- **Encryption** : The process or the set of rules that are involved in
  disguising the plaintext of the message into a form that is not
  understandable to an interceptor or attacker is called encryption.

- **Ciphertext / Encrypted Text / Cryptogram** : The encrypted message
  that is not understandable to an interceptor is called a ciphertext or
  a cryptogram.

- **Decryption** : The process or the set of rules that are involved in
  converting the encrypted message back to the plain text by the
  intended recipient is called decryption.

- **Encryption Key** : The crucial input (like a number or a password or
  a code) that goes into the encryption algorithm (apart from the plain
  text) to deliver the ciphertext is called the encryption key.

- **Decryption Key** : The input (like a code) that goes into the
  decryption algorithm to convert the ciphertext back to the plain text
  is called the decryption key. It is assumed in all cryptographic
  algorithms that only the intended receiver(s) of the message know(s)
  this decryption key.

- **Interceptor / Adversary / Attacker** : Any person or agent who is
  not the intended recipient of the message but who is trying to access
  it.

- **Crib** : A specific (often small) part of the plain text message (a
  name or a word or a phrase) that is known to be present for sure in
  the message. The attacker can know these cribs because of the
  awareness of the general context of the communication or other clues
  or intelligent guessing.

These concepts are summarised below in the picture.

[](https://substackcdn.com/image/fetch/$s_!zMcS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3e0a636-8623-4c88-a16a-c53b760d0295_3302x1280.png)

![](https://substackcdn.com/image/fetch/$s_!zMcS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc3e0a636-8623-4c88-a16a-c53b760d0295_3302x1280.png)





### Aims of Cryptography



The aim of cryptography is to ensure that any interceptor, without the prior knowledge of the decryption key, should be unable to determine the decryption key (which would enable him to decrypt and decipher the plaintext from the encrypted message), even in the worst case when he has access to all of the following information

1.  the entire encrypted message

2.  the knowledge of the entire process employed in encryption and
    decryption

3.  the knowledge of even some parts of the plain text message
    (**crib**) or general statistical information related to the plain
    text message

The three conditions above are entirely reasonable to ask. Condition 1 above is a reasonable assumption because if there is no possibility of interception, then there is no need to use cryptography in the first place. Therefore, the communicators are not able to control when the interceptions of their encrypted messages take place and hence, the safest option is to assume that all transmissions can be intercepted. Condition 2 implies that the crypto-system should not rely upon the secrecy of the details behind the processes of encryption and decryption. This might have worked in the past (as we will see in the next section that surveys pre-modern cryptographic technique) but not now anymore, given that encryption of messages and also the awareness of the processes behind them, are both more widespread than ever. In fact, nowadays, the algorithms behind a encryption and decryption are standardised and are made public in order to provide assurance regarding the security of the system.

Condition 3 is also a realistic condition because the interceptor or attacker might gain access to a small part of the plain text message by determining that some words or phrases are there in the plaintext of the message, by making intelligent guesses based on the known context of communication. A historic example of this comes from World War II itself. The electromechanical codebreaking machines of the Allied forces relied fundamentally on these **"cribs "** (fragments of known or guessed plaintext corresponding to specific stretches of intercepted ciphertext). To manufacture a crib when none occurred naturally, the code-breakers demanded the Allied forces to provoke the German forces into generating predictable cribs. At one instance, for example, the code breakers for the Allied forces requested that the Royal Air Force or the Royal Navy conduct a minor, specific strike (such as dropping sea mines in a specific grid or strafing an isolated navigational marker). German military communication followed strict, standardised administrative reporting procedures. An incident at sea required local naval stations to broadcast warning messages to coastal convoys and headquarters immediately. In the incident recorded by Brian Johnson in ***The Secret War***, British forces attacked a German navigational light buoy. The attack ensured that the German coastal monitoring station would transmit an emergency hazard warning containing the specific German word `LEUCHTTONNE` (the word for “light buoy” in German) alongside the predictable grid coordinates where the attack took place. As we will see in a later section, the knowledge of the presence of these known cribs in the ciphertext (like the word Leuchttonne and the grid coordinates) played a crucial role in deciphering and decrypting the ciphertext by the Allied forces. We will see about this in more detail in the last section of this article. What we want from the cryptographic system is that even if the attacker gets to know these small parts of the message, this should not enable him to figure out how to decrypt and unlock the rest of the message.

### Types of Attacks



We already got introduced to one type of attack in the previous subsection, which involves knowledge of some portions of the plaintext. One might even assume further that the attacker knows which part of the ciphertext corresponds to the crib (known plaintext). Such an attack which utilises the existence of known plaintext and ciphertext pairs in the message is called a **known plaintext attack**. If the plaintext is selected by the attacker, (as was the situation with the above light buoy example), then it is a **chosen plaintext attack**. Finally, an attack that only uses direct knowledge of the ciphertext is known as a **ciphertext-only attack**. If we assume that the attacker knows the decryption algorithm used, then there is one obvious method of attack available to any adversary. They could, at least in theory, try all possible values for the decryption keys and hope that they identify the correct one. Such an attack is called an **exhaustive key search attack** or, alternatively, a **brute force attack**. Of course such an attack cannot possibly succeed unless the attacker has some way of recognising the correct decryption key, or (as is more common) at least being able to eliminate most incorrect ones. In a known plaintext attack, for example, it is clear that any choice of the decryption key that does not give a readable plaintext in the natural language cannot possibly be the correct one. However, as we will see in detail in later sections, unless there is sufficient volume of corresponding plaintext and ciphertext pairs, there may be many incorrect choices for the decryption key that give the correct answers for all the available ciphertext. If the underlying language of the communications is sufficiently structured, then the statistics of the language can also be used to eliminate certain keys. We will see this in detail in the next section with a worked out example.

### Symmetric vs Asymmetric Cryptosystems



One fundamental classification of cryptographic algorithms is based on the nature of the encryption and decryption keys. A cryptographic algorithm is called **symmetric** if the decryption key is same as the encryption key or if the decryption key is easily deducible from the knowledge of the encryption key. Hence, they are also called as **one-key systems** or **secret-key systems**. However, if the decryption key is practically impossible to deduce from the encryption key, then such systems are called **asymmetric** or **two-key systems** or **public-key** **systems**. The reason why they are called public-key systems is because the knowledge of the encryption key can be made public (and is usually made so) in two-key systems, since it is anyway impossible to deduce the decryption key from the encryption key.

Note that cryptography relies on the assumption that the intended receiver knows the decryption key and is able to keep it secret. One consequence of accepting the three worst-case conditions above is that we have to assume that **the only information that distinguishes the genuine recipient from the interceptor is knowledge of the decryption key**. Thus the security of the system is totally dependent on the secrecy of the decryption key. For a symmetric system this necessitates that the encryption key should also be kept secret. In fact the general problem of **key management,** which includes key generation, distribution, storage, change, and destruction, is one of the most difficult aspects of obtaining a secure system, but it is not a part of cryptographic studies.

### Security Requirements



The kinds of cryptographic algorithms that are used depend on a lot of things and there is not a one-size-fits-all approach. The kind of algorithm used for a cheap, fast, low-level, short-term secure communication is different from that used for an expensive, high-level, long-term secure communication. The relevant question is hence not, ‘*Is this a perfectly secure system*?’, but, rather, ‘*Is this system secure enough for this particular application satisfying these particular constraints*?’. We are already in a position where we can begin to give some very basic criteria for assessing the suitability of a given cryptosystem for any particular application. The users of the system specify a cover time. The designers should know the number of decryption keys. If the designers now make assumptions about the speed with which an attacker could try each decryption key and see if it works, then they can estimate the expected time for an exhaustive key search to reveal the key. If the time for an exhaustive key search is shorter than the cover time, then the cryptosystem is clearly too weak. Thus our first crude requirement is: **the estimated time required for an exhaustive key search should be significantly longer than the cover time**. Again, for systems that involve low-level temporary security, it might be enough that the message remain secret only for a short amount of time and hence one would use a cheap cryptosystem to secure the message. Having seen the basic concepts, let us now dive into the waters of this field.

For the rest of this article, we will survey cryptosystems that were used before the recent era, starting from historical times until the first half of the twentieth century. They are definitely not anywhere close to the best but they do give us some valuable insight into the general aspects concerning cryptosystem design, despite being outdated. All these systems are symmetric (the encryption and decryption key is the same).

------------------------------------------------------------------------

# Caesar Cipher



[](https://substackcdn.com/image/fetch/$s_!ib38!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F734af516-9bfd-482c-9d99-152ef0e58c71_250x453.jpeg)

![](https://substackcdn.com/image/fetch/$s_!ib38!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F734af516-9bfd-482c-9d99-152ef0e58c71_250x453.jpeg)





One of the earliest examples of a cryptosystem is the Caesar cipher attributed to the Roman emperor Julius Caesar who used it in his campaigns. In this particular cipher, each of the letters from A to W is encrypted by substituting it with a letter that occurs three places after it in the alphabetical order. The last three letters X, Y, and Z are substituted by A, B, and C respectively. That is,

A → D  
B → E  
C → F  
D → G   
E → H  
.  
.  
.  
.  
U → X  
V → Y  
W → Z  
X → A  
Y → B  
Z → C

Although the specific cipher is said to have used this ‘shift’ of 3 (each letter shifted three places into the alphabet), a similar effect could have been achieved using any number from 1 to 25. The figure below shows an elegant visualisation to implement a Caesar Cipher with the shift of 3 with two concentric rings containing the Latin alphabets, of which the outer one is free to rotate. Shifting the angle of the outer ring with respect to the inner ring by three places, we get the Caesar cipher to be encrypting the letters of the text message in the inner ring by that of the corresponding letter above in the outer ring. The decryption message then consists of replacing the letters of the encrypted message in the outer ring by that of the corresponding letter below in the inner ring by doing the shift in reverse.

[](https://substackcdn.com/image/fetch/$s_!N0y4!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F87964238-3968-4516-85d7-48283e62cfcc_1070x964.png)

![](https://substackcdn.com/image/fetch/$s_!N0y4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F87964238-3968-4516-85d7-48283e62cfcc_1070x964.png)





So, the Latin message CARTHAGO DELENDA EST (which means in Latin : Carthage must be destroyed) in this 3-shifted Caesar cypher would be encrypted as FDUWKDJR GHOHQGD HVW (which is unintelligible gibberish to someone who knows Latin). Although the specific version used by Caesar shifted the letters by three places in the alphabetical order, in general one can go for other numbers ranging all the way from including the shift of 0 (which of course is the same as a shift of 26 which is the same as not shifting at all) till 25 which is also equivalent to shifting one position to the left. All in all, there are now 26 possible values for the shift. For a Caesar Cipher, the encryption key and the decryption key are both the shift number of the outer ring of this device relative to the inner ring, and hence the decryption key has twenty-six possible values from 0 to 25.

**Ceasar cipher**

**Encryption** : Shift by K units of the alphabet in the alphabetical order

**Decryption** : Reverse shift by K units of the alphabet in the alphabetical order

**Encryption**/**Decryption** **Key** : The number K (ranges from 0 to 25)

You may already begin to see several vulnerabilities in this Caesar cipher. If someone figures out that Caesar used this shifting method to encrypt his messages, they can easily figure out the key (shift value K) by several means :

- If someone is able to figure out that the letter E in the plain text
  corresponds to the letter H in the ciphertext (for e.g, by figuring
  out that the Latin word EST occurs in the ciphertext as HVW), then
  they can easily figure out that E → H means that the shift is three
  since H is three places after E. They can then decrypt the rest of the
  message. Thus, even the knowledge of even a single plain letter
  equivalent of a single letter in the ciphertext enables one to figure
  out the decryption key (shift) which then makes it possible to decrypt
  the entirety of the rest of the message, which is an extremely small
  amount of information, making it vulnerable to crib attacks.

- Even if one does not know anything in advance regarding parts of the
  message (like the knowledge of the decrypted value of just one
  cipherletter in the above example), a mere knowledge of the language
  in which the plain text is written, makes it vulnerable to the brute
  force attack. Since there are only 26 possible values of the key, one
  can simply try all numbers from 0 to 25 and see which decryption
  produces an intelligible English message (if the message is known to
  be in English). Let us assume that we see a five letter word in the
  encrypted message which is XMZVH that is known to be using the Caesar
  cipher and written in the English language. Then, we try all possible
  values of the shifts from 0 to 25 and try to read the decrypted
  message, assuming all these possible shifts. But, all except one of
  the readings are gibberish and only one of them produces a legit
  English word which is CREAM (shown in the picture below). So, we
  figure out that the shift is 21 (C → X, D → Y, E → Z, …) which enables
  us to decrypt the entire rest of the message. So, the Caesar cipher is
  also extremely vulnerable to brute force attack.

  [](https://substackcdn.com/image/fetch/$s_!0W8j!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c53757f-8587-4730-842c-02e542c98503_3064x1408.png)
  ![](https://substackcdn.com/image/fetch/$s_!0W8j!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9c53757f-8587-4730-842c-02e542c98503_3064x1408.png)
  
  

From this demonstration above, it must be clear as light that the Caesar Cipher is very easy to break by today’s standards. The fact that it was used securely in the distant past has more to do with the fact that others did not even realise that a cipher was being used in the first place. Today, everyone is much more aware of encryption and also encryption algorithms which are made public and are common place.

**Example 1.1 :** **Instructions from a gangster**

**Gary Klivans** is a ex policeman from New York state (now forensic consultant) who studied intensively on the encryption methods used by gangsters and prisoners. I recommend his book “**Gang Secret Codes : Deciphered**” if you are interested in this sort of stuff. Here is an encrypted message that he provides in his book from a prison inmate.

[](https://substackcdn.com/image/fetch/$s_!HFbz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1cd9d0c-fed8-4455-8275-31c9cec131c9_980x812.png)

![](https://substackcdn.com/image/fetch/$s_!HFbz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1cd9d0c-fed8-4455-8275-31c9cec131c9_980x812.png)





Note that every word in this message ends with the pair of letters YP. This makes it clear that YP has no meaning and is added at the end of every word only to confuse the codebreaker and hence has to be ignored. Look at the second word MZXZDQZ. You can see that Z occurs in this word thrice. It occurs at the end of the word too. Since the letter is repeated so often in the same word, it has to be a vowel. And since it also occurs at the end of the word, it has to be an E (think of the silent Es at the end of so many English words like name, time, game, blame, shape, etc). So, if you know that this prison inmate has used a Caesar cipher that sends E → Z, can you figure out the shift and decode the entire message by yourself? Try this out and see for yourself what he is saying which is very interesting (spoiler alert : he explains to his recipient how to pack drugs \[MRR strips\] into a condom and Saran wrap and also advises the person to hand him these drug packages during a visit, in order to immediately swallow them and smuggle the drugs into his prison cell). If you want to check your decipherment, the solution is at the end of this article.

**Example 1.2 : An espionage attempt in the US Air Force**

**Brian Regan** was a Master Sergeant in the US Air Force and tried to sell highly classified documents to foreign governments for a high price before he was caught in time and convicted of espionage in 2003. He used many encryption methods to conceal information and the code-breaking unit of the FBI was able to break most of them. Among them, one is very simple and is found to be encrypted in a Caesar cipher (note that the digits of numbers are also shifted by the same amount that the letters are).

[](https://substackcdn.com/image/fetch/$s_!EtKa!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F780d6101-54aa-4039-a5d6-b35e57318a84_836x342.png)

![](https://substackcdn.com/image/fetch/$s_!EtKa!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F780d6101-54aa-4039-a5d6-b35e57318a84_836x342.png)





MM-56NVOAIPG CBIOIPG-TUS VCT-AV-533341011943418 SS-CVOEFTQMBUA3CFSO-576795218837795

The part CVOEFTQMBUA is actually the name of a city. Can you adopt a brute force strategy yourself and try a few shifts (hint : it is not too large and hence won’t take more than four or five trials) and see which reading sounds like a city’s name? If you want to check your decipherment, check the answers at the end of this article.

**Example 1.3 : An exercise from a codebreaker**

**Herbert Yardley** (1889 - 1958) who was a codebreaker working for the US Department of State wrote a book called ***Ciphergrams*** in 1932 and gives a Caesar cipher to decode as an exercise which is shown below.

[](https://substackcdn.com/image/fetch/$s_!MY2C!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F250e20ca-7ccf-4ec4-8e11-fb8d9bbab003_976x484.png)

![](https://substackcdn.com/image/fetch/$s_!MY2C!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F250e20ca-7ccf-4ec4-8e11-fb8d9bbab003_976x484.png)





Can you decode SNSZK KXCHR ZAKDC KNMFH STCDE NQSXK ZSHST CDRDU DMSXS GQDD yourself by brute force without any help from me this time? Note that here the spaces in the message are not the spaces between words in the actual message. The space breaking in the ciphertext is arbitrary and is designed to confuse you. Try deciphering the entire message at once without any space in brute force and read out loud and then see if you can separate out legit words. Again, the shift involved is not a large number and you will succeed within a few guesses. Just beware of not spacing the message as per the cipher message and read the entire thing out loud to see if it makes sense. Check your decipherment in the solutions section at the end of this article.

------------------------------------------------------------------------

# Simple Substitution Cipher



We see that a major source of vulnerability of the Caesar cipher has got to do with having a very low numbers of possible values for the key (just twenty-six numbers from 0 to 25) making it vulnerable to brute force attacks. Thus, having a large number of possible values for the key is demonstrated to be a necessary requirement for cryptographic security. But, it is also not a guarantee that the cryptosystem is strong because other information regarding the general context of the message might make it possible to eliminate a large number of these possibilities and narrow down unto a very small set of possible keys. The case of the simple substitution cipher presented in this section will demonstrate this. The encryption and decryption key here are just the alphabet written in a randomly chosen order. An example is shown below.

[](https://substackcdn.com/image/fetch/$s_!mCq9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76612bc7-09b4-4918-a1e2-be999ea97189_1294x372.png)

![](https://substackcdn.com/image/fetch/$s_!mCq9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F76612bc7-09b4-4918-a1e2-be999ea97189_1294x372.png)





The encryption rule for this simple substitution cipher consists of replacing each letter in black by its red counterpart below and the decryption rule is the reverse process of replacing each letter in red by its black counterpart above. The encryption key and the decryption key coincide and is nothing but the sequence of the red letters that are known to be communicated in advance to the receiver from the sender. In the example I have given above, it is the sequence **RAMHOPESTYUNJICLBDFGKQVWXZ**. Normally, a random sequence of alphabets is difficult to memorise and communicate accurately. So, the strategy that is commonly followed is that one takes a meaningful English sentence and then removes repeated letters and then adds the missing letters at the end in order after it. In my illustration above, I have chosen the sentence “*Rama hopes that you enjoy the article*” (which is easier to remember and communicate accurately and quickly). Removing all the repeated letters from this sentence, we get “RAM HOPES T YU NJ ICL” which when written as a sequence, gives “RAMHOPESTYUNJICL”. Then, the letters missing from this sequence are added in alphabetical order at the end to give **RAMHOPESTYUNJICLBDFGKQVWXZ.**

Note that the Caesar cipher is a special case of this simple substitution cipher where the red letters are shifted versions of the black letters by a fixed amount of shift. For example, the message “ASSEMBLE AT BAKER STREET TOMORROW MORNING” would be encrypted into ciphertext as “RFFOJANO RG ARUOD FGDOOG GCJCDDCV JCDITIE” under the substitution rule in the picture above.

How many possible values are there for the decryption key? The decryption key is nothing but a jumbled sequence of the letters of the alphabet. So, the number of possible decryption keys correspond to the number of arrangements of the 26 letters of the alphabet (one of which is shown in red in the picture above). The first red letter has 26 possibilities, the second red letter then has 25 possibilities, the third red letter can have 24 possibilities (letters cannot repeat) and hence the total number of possibilities of the red sequence of letters is given by 26 x 25 x 24 x 23 x 22 x …. x 3 x 2 x 1 (also popularly denoted by 26! in mathematics) whose value is 403,291,461,126,605,635,584,000,000 which is an astronomically large number. So, one is unlikely to discover the correct key by an exhaustive search and hence brute force attack seems to be unlikely, at least when done naively. Also, knowledge of let us say a word or two in the plain text also seems to be of not much use. If I know that the message text has the word STREET and I also know that it corresponds to the word FGDOOG in the cipher text, I can only discover a part of the correspondence shown in yellow below which correspond to four positions.

[](https://substackcdn.com/image/fetch/$s_!bhra!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e3c71b7-2268-40b2-98e4-8e74e96c0b64_1282x350.png)

![](https://substackcdn.com/image/fetch/$s_!bhra!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F3e3c71b7-2268-40b2-98e4-8e74e96c0b64_1282x350.png)





This leaves us the knowledge of the remaining 22 positions which leave with 22! = 22 x 21 x 20 x 19 x … x 3 x 2 x 1, which is still a prohibitively large number. So, this scheme also seems to be robust to crib attacks, at least as long as the size of the known crib does not have much letters compared to 26.

But, this simple substitution cipher too can be broken very easily when the text encoded in the cipher is “long enough”. This is because of the statistical properties of the English language. The English language (like any natural human language) is not a gibberish of random letters where every letter has equal chances of occurring. After analysing a large corpus of texts in English, the percentage of occurrences of the various letters of the alphabet in English texts are shown below.

[](https://substackcdn.com/image/fetch/$s_!_Jvf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8cf9c2ef-b084-4359-8620-d4223fd21e53_3126x1376.png)

![](https://substackcdn.com/image/fetch/$s_!_Jvf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8cf9c2ef-b084-4359-8620-d4223fd21e53_3126x1376.png)





This graph says that the letter E is the most frequently occurring letter in English texts with about 12% of occurrence. Next comes the letter T with about 9% and then A with about 8%. Thus, when one encounters a large amount of simply substituted ciphertext that is known to be in English, one can calculate and see what letter in the ciphertext occurs about 12% of the time and that has to got to correspond to the letter E. Similarly, the letter in the ciphertext message that occurs about 9% of the time has to correspond to the letter T. Once the attacker knows which letters correspond to T and E, since the most frequently occurring three letter word in English is THE, he can figure out the letter corresponding to H, even without doing the rest of the calculation for H explicitly.

While it is cumbersome to take a long text and count manually how many times each letter has occurred and dividing them by the total number of letters to get the percentage frequencies of each letter and manually plotting them, a computer program can do that in milliseconds for you. Here is a program below in Python that does this job. If you are interested, run this code in Google Colabs (it is like Google Docs for Python code). When you copy this code and run it (click the play icon in the Colab), you will be asked to enter a text. Type the text and then press enter after which you will get the frequency histogram of every letter in that text you entered.

``` shiki from collections import Counter import string import matplotlib.pyplot as plt

# 1. Input text sample text = input("Enter your text here : ") 
# 2. Clean the text: convert to lowercase and filter only valid lowercase alphabet letters # This automatically ignores spaces, full stops, commas, and numbers. cleaned_text = [char for char in text.lower() if char in string.ascii_lowercase]

# 3. Calculate frequencies and total count letter_counts = Counter(cleaned_text) total_letters = len(cleaned_text)

# 4. Ensure all 26 letters are accounted for (even if they have a frequency of 0) alphabet = list(string.ascii_lowercase) percentages = [(letter_counts[letter] / total_letters) * 100 for letter in alphabet]

# 5. Plotting the histogram (Categorical Bar Plot) plt.figure(figsize=(10, 6)) plt.bar(alphabet, percentages, color='skyblue', edgecolor='black', width=0.8)

# Adding labels and titles plt.title("Percentage Occurrence of Each Letter in Text", fontsize=14, fontweight='bold') plt.xlabel("Letters of the Alphabet", fontsize=12) plt.ylabel("Percentage (%)", fontsize=12)

# Grid layout for readability plt.grid(axis='y', linestyle='--', alpha=0.7)

# Display the plot plt.show() ```





We end this subsection by confessing that we have not quantified our concept of a ‘long’ ciphertext. There is, of course, no precise answer. While 200 characters are almost certainly sufficient for the statistics to be reliable, it might go up or down depending on the exact content of the message, if it is speciaised. As an extreme example of how the statistics of a message might be deliberately manipulated, note that there is a 160-page novel in English that does not use the letter E at all (which is the most frequent letter in English), called ***Gadsby*** written by the author Ernest Vincent Wright). Thus, this simple substitution works for :

1.  for encrypting random data (like numerical coordinates of a
    particular place) which do not have any statistical preferences for
    the individual symbols which are digits of numbers

2.  or for encrypting very short messages where the statistics of the
    message cannot be reliably determined.

Also, there is one more easier way to mathematically verify whether an encrypted text is encoded in a simple substitution cipher or not. We saw in frequency analysis that a natural language like English is not a sequence of random letters where all the letters occur with equal probability but has structured frequencies of its various letters with some letters occurring very frequently and some occurring very rarely. So, one way to verify whether a ciphertext uses simple substitution is to plot the frequencies of its various letters and see if the histogram can be matched with that of standard expected histogram by letter swapping. But, this is a cumbersome process. We would love it if there were a single number that can be calculated from the text that would tell instantly whether something is a simply substituted ciphertext or not. One such number is called the **index of coincidence**. When a sequence of letters are written randomly, what is the probability that two randomly chosen letters from the sequence are the same letter? This is easy to calculate. Since the two chosen letters are random, there are a total of 26 x 26 possibilities for the pairs of letters. But for the pair of letters to be same, the second letter has to be same as the first letter and this hence can happen only in 26 of those 26 x 26 pairs of letters. Hence, the probability that two randomly chosen letters of the text are the same is

$`\frac{26}{26 \times 26} \times 100\% = 3.85\%`$

But an English text is not a sequence of randomly written letters. So, we can take huge swathes of English text, choose millions of pairs of letters randomly from them, and check what percentage of these pairs consists of the same letters. It turns out that the answer is 6.7 % to 6.8 %. Note that this number does not change when we swap the letters since two identical letters still go to two identical letters and two non-identical letters still go to two non-identical letters after swapping. Hence, any kind of simple substitution still preserves this statistics. One could hence take a thousand random pairs of letters from the ciphertext and measure how many percentage of those pairs consists of same letters and check if the number is close to 6.7 %. If yes, we can be pretty confident that the ciphertext is an encryption of an English plaintext. For any other language, the same logic applies except that instead of 6.7 %, we will have some other target number. This is difficult to check manually but very easy for a computer. For example, here is a simple Python code that does it for you below. If you are interested, run this code in Google Colabs (it is like Google Docs for code). When you copy this code and run it (click the play icon), you will be asked to enter a text. Type the text and then press enter after which you will get the index of coincidence of that corpus.

``` shiki # Calculating index of coincidence

import random import re

# 1. Take text input from the user text = input("Enter your text: ")

# 2. Clean the text: keep only letters and capitalize them cleaned_text = re.sub(r"[^A-Z]", "", text.upper())

# Check if there are enough letters to form pairs if len(cleaned_text) < 2:
    print("The text must contain at least 2 letters.") else:
    num_pairs = 50000
    same_count = 0
    text_length = len(cleaned_text)

    # 3. Take 50,000 randomly chosen distinct pairs of letters
    for _ in range(num_pairs):
        idx1, idx2 = random.sample(range(text_length), 2)

        # 4. Check if the two chosen letters are the same
        if cleaned_text[idx1] == cleaned_text[idx2]:
            same_count += 1

    # 5. Calculate the empirical index of coincidence
    index_of_coincidence = (same_count / num_pairs)*100

  
    print(f"Index of Coincidence is: {index_of_coincidence:.4f}") ```





[](https://substackcdn.com/image/fetch/$s_!QQdU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb36ed28-350a-4caa-bd9c-3d148e4939d8_3560x1610.jpeg)

![](https://substackcdn.com/image/fetch/$s_!QQdU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fcb36ed28-350a-4caa-bd9c-3d148e4939d8_3560x1610.jpeg)





Another much earlier documented usage of simple substitution ciphers comes from ancient India. One of the earliest descriptions of encryption by substitution appears in the ***Kāmasūtra***, a text written around the turn of the common era by the scholar **Vātsyāyana**. The text recommends that women should study 64 arts, including cooking, dressing, massage and the preparation of perfumes (not surprising for an ancient text). But, the list also includes some less obvious arts, including conjuring, chess, bookbinding and carpentry. Number 45 on the list is something that stands out for our article which is **mlecchita-vikalpa**, the art of secret writing, advocated in order to help women conceal the details of their illicit liaisons! The exact details are not known but later commentator to the text provide details on it and all of the recommended techniques involve substitutions of letters (for example, one of them involves randomly pairing letters of the alphabet, and then substituting each letter in the original message with its partner).

**Example 2.1 : Kryptos Sculpture**

Here is the first half of an encrypted inscription on the famous ***Kryptos*** sculpture made by the American artist Jim Sanborn now on display at the CIA Headquarters.

[](https://substackcdn.com/image/fetch/$s_!hvTS!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4447be5c-bce5-4069-bfc8-89218bbf4a08_980x680.png)

![](https://substackcdn.com/image/fetch/$s_!hvTS!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4447be5c-bce5-4069-bfc8-89218bbf4a08_980x680.png)





The first half of the encrypted text reads as follows (for you to copy paste) : EMUFPHZLRFAXYUSDJKZLDKRNSHGNFIVJYQTQUXQBQVYUVLLTREVJYQTMKYRDMFDVFPJUDEEHZWETZYVGWHKKQETGFQJNCEGGWHKK? DQMCPFQZDQMMIAGPFXHQRLGTIMVMZJANQLVKQEDAGDVFRPJUNGEUNAQZGZLECGYUXUEENJTBJLBQCRTBJDFHRRYIZETKZEMVDUFKSJHKFWHKUWQLSZFTIHHDDDUVH? DWKBFUFPWNTDFIYCUQZEREEVLDKFEZMOQQJLTTUGSYQPFEUNLAVIDX  
FLGGTEZ?   
FKZBSFDQVGOGIPUFXHHDRKFFHQNTGPUAECNUVPDJMQCLQUMUNEDFQ  
ELZZVRRGKFFVOEEXBDMVPNFQXEZLGREDNQFMPNZGLFLPMRJQYALMGNUVPDXVKPDQUMEBEDMHDAFMJGZNUPLGEWJLLAETG

Prove that this is not a simple substitution cipher by either using frequency analysis or by measuring the index of coincidence (use the two codes that we saw in this section). We will decipher this in the next section.

**Example 2.2 : Reading an intimate letter of a prisoner**

One need not always do a frequency analysis to decipher a simple substitution cipher. One can learn to detect other patterns and figure out by guessing, if the ciphertext leaves spaces between words. Gary Klivans (whom we got introduced to in Example 1.1 as an American expert on prison codes) gives in his book, an example of a letter from a prisoner written in a substitution cipher.

[](https://substackcdn.com/image/fetch/$s_!lSER!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14d7415f-2bb2-45c1-9dba-a0ab4e7f1fe3_796x1104.png)

![](https://substackcdn.com/image/fetch/$s_!lSER!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14d7415f-2bb2-45c1-9dba-a0ab4e7f1fe3_796x1104.png)





As we can see here, the sender has converted letters into a set of non-alphabetic symbols and our job is to figure out what symbol he used for what letter. He cracked this code easily not by doing any mathematical analysis but by simply observing patterns. For example, he observed the following word repeated twice shown in the boxes below.

[](https://substackcdn.com/image/fetch/$s_!zK44!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8b124801-9388-4ef8-9e87-54f230d5abe8_580x342.png)

![](https://substackcdn.com/image/fetch/$s_!zK44!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8b124801-9388-4ef8-9e87-54f230d5abe8_580x342.png)





We see that the word has five letters with the third and fourth letter being the same. What commonly used five letter American English words have this pattern? There were two guesses - HOLLA (American slang for ‘hello’) and GONNA (American slang for ‘going to’). Both guesses have their second letter as O and end with the last letter A. Hence, Gary figured out that the dashed line at the end of the rectangled word stands for the letter A and the symbol that looks like a line inside a semi-circle is the letter O. Looking around, he then could figure out the indefinite article “A” which is a single letter word using the letter he had already cracked. Now, he looked for another symbol that occurred on its own a lot of times. The only other single letter word in English apart from the article “a” is the first person pronoun “I” in English. Looking around, he found it out and it is boxed below (two semicircles).

[](https://substackcdn.com/image/fetch/$s_!omqZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee16505c-c950-4b08-b4e3-5dcbfecedecf_778x484.png)

![](https://substackcdn.com/image/fetch/$s_!omqZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fee16505c-c950-4b08-b4e3-5dcbfecedecf_778x484.png)





Garry then saw this pair of words shown below.

[](https://substackcdn.com/image/fetch/$s_!usU0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a7a9860-0a51-422c-9883-7e02078319ed_760x280.png)

![](https://substackcdn.com/image/fetch/$s_!usU0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8a7a9860-0a51-422c-9883-7e02078319ed_760x280.png)





By the knowledge of the letters already known, he figured out that this word pair had got to be of the form OA\*\*\*A\* \*OO\*\*\*\* which is a uniquely distinct and peculiar pattern that only a particular word pair could satisfy. Based on this pattern, he now guessed that this word pair was OATMEAL COOKIES (a very commonly used product’s name in America) which later proved to be correct and consistent with the rest of his decipherment. Using this, he now knew what the symbols for T, M, E, L, C, K, I, and S were. Using this, he figured out that the word at the beginning could not be HOLLA but only GONNA since the third and fourth letter was not matching with the symbol for L he deciphered from guessing the phrase OATMEAL COOKIES. Hence, he could now figure out the symbol for G and N as well now, given that he knew the word GONNA. Now, armed with the knowledge of twelve letters, he proceeded further to partially read the message and figure out the gaps based on word guessing again, which became easier as he progressed because the number of letters he knew kept increasing and the number of letters he did not know kept decreasing. He then figured out the entire substitution table.

![](https://substackcdn.com/image/fetch/$s_!SW_Z!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa8436b63-91df-41ec-98a4-44a2a3da2d2c_1010x110.png)

The plain text letter now reads :

> WELL BEAUTIFUL, JUST FINISHED EATING LUNCH, HAD CHICKEN PATTIES, THEY
> WERE ALRIGHT. BABE, I LOVE YOUR LETTERS. WHAT YOU SAY ABOUT THESE
> WOMEN IN HERE IS HILARIOUS. BONT LET THEIR FART GAS GET TO YOU
> BEAUTIFUL. ALRIGHT, BABE, I JUST READ YOUR LETTER THAT TALKED ABOUT US
> HAVING CHILDREN. IM GONNA KEEP THIS SHORT AND SWEET I LOVE YOU!!! YOUR
> GONNA BE MY WIFE

Looks like this is an ordinary romantic letter and had nothing to do with his crime and he had encrypted it not because he was doing something illegal but because he had intimate information !

Based on this example, let me give you a smaller problem to solve for yourself. This is the fragment of a message sent by an unknown person to a prisoner in Pennsylvania in 2013. Gary Klivans cracks this using the same process we just saw above. It turns out that this mysterious alphabet is nothing but the Star-Wars writing system named ***Aurebesh***. Without the prior knowledge of this font though, can you break it by doing only eyeballing and word guessing? Ignore the diacritical marks as they are punctuations. The ' is the apostrophe as in English. Also, the mirror image of each symbol denotes capital letters.

[](https://substackcdn.com/image/fetch/$s_!MpNB!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14bf2fb8-ca9a-44d9-a927-09eee78142c5_1018x328.png)

![](https://substackcdn.com/image/fetch/$s_!MpNB!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F14bf2fb8-ca9a-44d9-a927-09eee78142c5_1018x328.png)





Let me start this process for you. There are two single letter words here which are :

![](https://substackcdn.com/image/fetch/$s_!1s-D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf97c25a-3582-40a5-bc92-14b1dd5ff24e_140x82.png)

One of the above has to be “I” and another has to be “A”. Keep going on your own from here. Do not forget that ‘ is an apostrophe. To check your answer, see the solutions at the end of this article.

**Example 2.3 : NSA Monday Challenge**

When the ciphertext in a simple substitution cipher does not have spaces between words (or if it leaves spaces but deliberately wrong from that of the plaintext message), then it becomes harder to decipher intuitively (by guessing words) and some sort of mathematical and frequency analysis is required. In technical terms (for some reason), a simple substitution cipher that does not convey word boundaries is called a **patristocrat** whereas one that does is called as an **aristocrat**. The previous pair of examples we saw were patristocrats. Note that a patristocrat is not only more difficult to crack for an attacker but also more difficult to read for the intended recipient because it creates ambiguities. If you look at a cipher with no spaces or spaces left deliberately at regular intervals of letters, then it is a patristocrat. Is there any way to crack a patristocrat without complex computing? Let us illustrate with an example. The NSA (a United States intelligence agency responsible for global monitoring, signals intelligence, and protecting U.S. government communications) is active on social media and publishes crypto-puzzles in their Facebook and Twitter page. The people who solve the puzzle grab their attention. As an example, here is one of the four ciphers they tweeted on the Mondays of May 2014 and hence referred to as the “*NSA Monday Challenges*”.

[](https://substackcdn.com/image/fetch/$s_!BfhM!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F962f43d4-6206-47f7-ae81-e8ad0072ac19_1188x386.png)

![](https://substackcdn.com/image/fetch/$s_!BfhM!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F962f43d4-6206-47f7-ae81-e8ad0072ac19_1188x386.png)





It reads : tpfccdlfdtte pcaccplircdt dklpcfrp?qeiq lhpqlipqeodf gpwafopwprti izxndkiqpkii krirrifcapnc dxkdciqcafmd vkfpcadf. The spaces here are merely decorative and occur in blocks of twelve characters (which does not reflect the spacing between the actual words in the plaintext). Perform a frequency analysis or an index of coincidence test (using the code I gave) to verify that it satisfies the conditions for the simple substitution cipher. But, we do not need to rely on it to crack the code. Like in the previous example, if you are interested in cracking the substitutions without using a computer and just by the knowledge of English, continue reading further. Let us count the most frequently occurring letter-pairs in this cipher that occur twice or more.

The most frequent letter pair : **CA** → occurs 4 times in the cipher  
The second most frequent pairs : **CD, PQ, PC, IQ** → occur 3 times in the cipher  
The third most frequent pairs : **CC, AF, QL, QE, II, FC, KI, DK, DF, LI, PW, RI, DT, IR** → occur 2 times in the cipher.

Here are some relevant facts related to the English language which are not surprising if you think about them deeply.

- The most frequent letter pairs in the English language are : TH (part
  of the “th” sound and the most frequent word “the”), HE (a very
  frequent pronoun), and EN (think of so many words with “en” like
  English, engage, enrage, enrich, pen, hen, men, den, dent, scent,
  bend, lend, mentor, ascend, fallen, chicken, etc…). Others include EN,
  ER, IN, AN, and RE.

- The letter pair that is very frequent when read both ways is ER / RE
  (think of many words that have “er” and “re” like the comparative
  suffix and the agent suffix -er, the prefix re-, words like repair,
  reduce, reply, relate, brother, father, breaker, …)

- The most frequent doubled letter pair in English is LL (think of many
  frequent words like call, ball, tall, mall, will, pillow, ill, bill,
  mill, full, bull, etc…). Others include SS and TT (e.g. grass, bottle,
  settle, mass, essential, …), and some frequent ones after them that
  deserves mention include EE, and OO (e.g. sheep, book, deep, boot,
  etc…).

Triplet frequencies are also relevant in some cases but not here because the message is too short and there are only two triplets that occur more than once here. But in case, for future reference the most frequent triplet of letters in English is THE (a word by itself) followed by AND, ING, ENT, ION, HER, FOR, and THA. For even longer ciphers, quadruplets and quintuplets also could be analysed. But, for now, let us be content with analysing letter pairs here. By manual counting, it easy to figure out that most frequent single letters are P (12.5%), C (11.54%), and I (10.58%). The length of the text is not long enough to figure out the exact statistics but the three most frequent letters {P, C, I} got to correspond to the three most frequent letters in the English language which are {E, T, A}. But we don’t know what exactly map to what between {P, C, I} and {E, T, A}. It is here when the statistics about pairs of letters comes in. The letter pair AA is super rare in English (I can’t think of any common word containing it) but the two pairs EE and TT are very common. In our cipher, the pairs CC and II occur twice but the pair PP is not seen. So, it must be the case that PP maps to AA and hence P in the cipher must map to A. This leaves us to choose how the two letters {C, I} maps to the letters {E, T}. Now, we have only two options to choose from. They are :

- C → E , I → T (option 1)

- C → T, I → E (option 2)

Let us try option 1 and try reading this text partially. In this option, P→A, C→ E, and I→T. The cipher now reads as follows after this partial decipherment (the stars represent unknown true letters)

\*A\*EE\*\*\*\*\*\*\***AE\*EEA**\*T\*E\*\*\*\*\*AE\*\*A? **T**\*A\*\*TA\*\*\*\*\*\*A\*\*\*\*A\*A\*\*TT\*\* \*\*\*T\*A\*TT\*\*T\*\*T\*E\*A\*E\*\*\*\*ET\*E\*\*\*\*\*\*\*AE\*\*\*

We observe the sequence AE\*EEA which sounds impossible in English (can you think of any English words having letter pairs like “ae” or letter triplets like “eea”?). So, let us now try option 2.

\*A\*TT\*\*\*\*\*\*\***AT\*TTA**\*E\*T\*\*\*\*\*AT\*\*A?\*\*E\*\*\*A\*\*EA\*\*\*\*\*\*A\*\*\*\*A\*A\*\*EE\*\* \*\*\*E\*A\*EE\*\*E\*\*E\*T\*A\*T\*\*\*\*TE\*T\*\*\*\*\*\*\*AT\*\*\*

This sounds much more plausible. In fact, we can consider the same spot which now reads AT\*TTA. The letter in between has to be a vowel (otherwise we will have a sequence of four consonants which is so rare in English). The vowel can be I, O, U or Y. Let us guess it to be I to so that we get a sequence like ATITTA and this can be read as “at it ta…”. So, let us assume that the star letter (which is actually A in the cipher) maps to I (a → i). Applying this guess to the rest of the message gives the following incomplete message.

\*A\*TT\*\*\*\*\*\*\*ATITTA\*E\*T\*\*\*\*\*AT\*\*A?\*\*E\*\*\*A\*\*EA\*\*\*\*\*\*A\*I\*\*A\*A\*\*EE\*\* \*\*\*E\*A\*EE\*\*E\*\*E\*TIA\*T\*\*\*\*TE\*TI\*\*\*\*\*\***ATI\*\***

Since it is NSA, and we are looking at the trailing sequence, it sounds plausible that the last word looks like NATION (with the contextual clue and the ATI at the middle). This further suggests us the following maps : d→o, f→n. Applying these to the rest of the message, we get :

**\*ANTTO**\*NO\*\*\*ATITTA\*E\*TO\*O\*\*ATN\*A?\*\*E\*\*\*A\*\*EA\*\*\*ON\*A\*IN\*A\*A\*\* EE\*\*\*O\*E\*A\*EE\*\***E\*\*ENTIA\***TO\*\*OTE\*TIN\***O\*\*NATION**

This is already looking pretty good. One of the most frequent letter pair EN is now showing up. We can further guess the trailing sequence O\*\*NATION as OUR NATION which suggests the maps : v→u, k→r. Applying these to the rest of the message now reads : E\*\*ENTIA\* mostly means ESSENTIAL because the two letters in E\*\*E are the same. This further suggests the following maps : r→s, n→l. The sequence in the beginning \*ANTTO has only one missing letter and we can easily guess it has WANT TO. Hence, this suggests the mapping t→w. Applying all these, the message now reads :

WANTTO\*NOWW\*ATITTA\*ESTOWOR\*ATNSA?\*\*E\*\*\*A\*\*EA\*\*\*ON\*A\*IN\*A \*ASWEE\*\*LORE\*AREERSESSENTIALTO\*ROTE\*TIN\*OURNATION

Guessing the remaining letters and reading the text is straightforward. The complete plain text here is :

WANT TO KNOW WHAT IT TAKES TO WORK AT NSA? CHECK BACK EACH MONDAY IN MAY AS WE EXPLORE CAREERS ESSENTIAL TO PROTECTING OUR NATION.

There are a lot of other ways in which this can be deciphered. Let us assume that we know from some source that the word CAREER appears in the plaintext (even if we don’t have this information, CAREER is a likely word in an NSA challenge cryptogram that is made to attract talented codebreakers). So, we can use it as a crib. The word CAREER contains the string REER, which has a letter pattern of the type 1221. We can search for this pattern in the ciphertext. In fact, we find two strings of this kind: KIIK, IRRI. We can eliminate IRRI because there is the letter R left of the first I, so the letter pattern is actually 21221. This doesn’t fit with CAREER. This means that KIIK is the only string that fits. If our guess is correct, QPKIIK stands for CAREER. The letters A, C, E and R that we can now identify should be enough to determine the remaining letters. There is lot of logic and science behind code cracking but the process is more of an art of strategy than science.

To try for yourself, here is another NSA’s Monday challenge to try for yourself. I will give a hint that this has to be read backwards for deciphering. Other than that, keep in mind the facts regarding frequent letter pairs and triplets and try based on your own instincts. The detailed solution is not worked out at the end of this article as there are lots of ways to arrive at it.

[](https://substackcdn.com/image/fetch/$s_!HRH8!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc6642da-1438-482f-b3a0-512bc1a4ee74_1172x378.png)

![](https://substackcdn.com/image/fetch/$s_!HRH8!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbc6642da-1438-482f-b3a0-512bc1a4ee74_1172x378.png)





# Nomenclator Cipher & Homophonic Cipher



In a **homophonic cipher**, the message is written in another set of symbols whose number is greater than that of the alphabet of the target language. This means that some letters of the plain text language map to more than one symbol of the encrypted symbol list. It makes sense to assign more symbols to the letters of the alphabet that occur more frequently. If the letter E occurs twice as much frequently as the letter H in the English language and thrice as frequent as the letter D in the English language, it makes sense to assign three symbols to E, two symbols to H, and one symbol to D. If the choice between the symbols within a given alphabet is random, then it means that all the 3 + 2 + 1 = 6 symbols in the cipher occur with equal probability in the encrypted text. Thus, the purpose of the homophonic cipher is to mask the frequency distribution and make it closer to equal frequencies so that no frequency statistics techniques can be used to decipher the encrypted text. There is one obvious difference between any simple substitution cipher and a homophonic cipher: the latter requires a larger ciphertext alphabet. So, if you encounter a ciphertext that is written in the standard alphabet (A–Z) or another alphabet with about twenty-six letters, at the very least you can assume that it is not a homophonic cipher. But, even Nomenclator ciphers (which we will see next) have more symbols than the number of letters of the alphabet.

**Example 3.1 : Deciphering a homophonic cipher which denotes word boundaries**

Today, the best approaches for solving homophonic ciphers are of course computer-based (like for all others). If you want to solve a homophonic cipher without computers, your chance of success increases heavily if the spaces between the words are visible. If not, the task becomes very difficult unless you have a very long ciphertext to analyse. If, however, the word boundaries are indicated, the chances are quite good as long as there aren’t too many homophones in play. Let us consider the following ciphertext as an example below which was given in a competition :

> U3EI0 RH84 MB9Y B3 0GN DEIYP1C DZEX5 KJB4 7ELN1SB XI5JY 3NK AP95U
> 1F40O HT XFHZSKC0F1 FK IHEL 3MF 0MJ13R TH9ZFM 3GN THH0DBEO KF40G
> 3OIH8CG 3OJ TFI5U0 ET054 E7H83 F1J YP9HAN05I 3BYN B 4SCG0 EKL MBZY
> E9F1C 3OJ T5KXN BT05I USQ O81L4JL AN05IU RH8 MP99 4NEXG B DPX1SX DZBXJ
> MP3O E D9ERCIF8KL SK 0G5 XN13N4 HT 0O5 DPXKSX DZBXJ 3G5IN PU E OB0 S1
> 3G5 9FM54 DBI0 HT 3GJ 4NE4 MB9Z FT 0OJ OB3 7JGSKL 0O5 7N1XG RH8 MPZ9
> TS1L E UABZ9 D9BU3PX 7FQ XHK0ESKP1C T8I3O5I SKU0I8X3SF1U CFHL Z8XY

This ciphertext uses thirty-six symbols derived from the twenty-six alphabets and ten digits. So, there are ten extra symbols used as homophones. Performing a frequency analysis gives us quite a smooth frequency distribution of symbols as expected. But, since the cryptogram contains spaces, we can make use of some word statistics in English.

Next, let’s assume that in an ordinary English text there are two different representations of each of the five most frequent letters A, E, I, O and T (i.e., homophones). We’ll call these A1 and A2; E1 and E2; I1 and I2, O1 and O2, as well as T1 and T2. We have chosen A, E, I, O and T because they are the most frequent letters in the English language. If we replace each of these with one of two corresponding homophones and if we use the two representations of each letter roughly equally often, the frequency distribution of a typical English text will look as shown below (pic from the book : Dunin, Elonka; Schmeh, Klaus. Codebreaking: A Practical Guide)

[](https://substackcdn.com/image/fetch/$s_!ItuC!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6aeca14-8e1f-4c34-b708-4ce602159254_1044x1070.png)

![](https://substackcdn.com/image/fetch/$s_!ItuC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd6aeca14-8e1f-4c34-b708-4ce602159254_1044x1070.png)





We see that word initially, T is the most frequent letter and the symbols corresponding to T (T1, T2) are still more frequent, even while using two homophones for it. So, this fact can be used to decipher the symbols for T1 and T2. But, T1 and T2 are not that frequent when we judge them by their overall frequency. A similar argument can be made after observing the frequency distribution of the letters in the word final position. The letter I almost never ends a word in English and this can help us in finding out the symbols for I. By counting the frequencies of the symbols, we get the following graph :

[](https://substackcdn.com/image/fetch/$s_!eJ1v!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb48a454d-38e6-44ce-9d4f-77bb6ec54a1f_992x356.png)

![](https://substackcdn.com/image/fetch/$s_!eJ1v!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb48a454d-38e6-44ce-9d4f-77bb6ec54a1f_992x356.png)





Here are the following sequences of observations that gradually leads us to the solution. The symbols 3 and E are the most frequent initial letters but less common in the entire text, which resembles the properties of the letters corresponding to T. So, they must correspond to T. The symbols H and S have about the same and quite high frequency in both overall category and as initial letter category but don’t appear all in the word final category which means they should correspond to I.

[](https://substackcdn.com/image/fetch/$s_!vgs1!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bbf1922-9107-4b30-b29d-2bd5fc1390b0_1306x342.png)

![](https://substackcdn.com/image/fetch/$s_!vgs1!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7bbf1922-9107-4b30-b29d-2bd5fc1390b0_1306x342.png)





Symbols B and E are single letter words. They can only be A and I. The following two letters words appear in the cipher : B3, HT (three times), FK, SK, BU, S1, FT. They should correspond to {OF, TO, IN, IT, IS, BE, AS, AT, SO}. What can we do with this? B and E stand for A and I but what exactly for what? Both B and E occur word finally as well, so they both can only correspond to A (there is no word “I” in our text). Since we figured that 3 and E map to T, the fourth word in the cipher text B3 should stand for “AT”. Since 3O is a very frequent letter pair, does it stand for TH? Maybe yes. The word 3OJ appears twice and if our assumption of 3O → TH makes sense, 3OJ must represent THE. So, this means that J decrypts to E. The ciphertext also has the word 3GJ which is T\*E. So, maybe G also stands for H, as a homophone and hence O, G → H. Now that we know the equivalents of A, E, H, and T, we can guess others. The word MP3O which is \*\*TH might stand for WITH and MP99 is likely WILL. Maybe MPZ9 also has the same meaning and hence Z and 9 are homophones for L. Now, looking at MB9Y gives us WAL\* which makes us guess the word WALK. We can keep going like this and decipher the plain text fully. The answer is given at the end of this article.

[](https://substackcdn.com/image/fetch/$s_!_Bx0!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07b6f66a-8ed6-4ee7-ba3c-423bda3d4065_1242x828.png)

![](https://substackcdn.com/image/fetch/$s_!_Bx0!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F07b6f66a-8ed6-4ee7-ba3c-423bda3d4065_1242x828.png)





One of the most famous historical examples of the next type of cipher (Nomenclator) in Western history comes from England during the turbulent sixteenth century when Europe was put into chaos due to the raging Protestant Reformation. This cipher and was employed by **Mary, Queen of Scots**. The fervently Catholic queen Mary was forced to abdicate her throne and flee Scotland following a rebellion by Scottish Protestant nobles who were also provoked by her marital disasters and political choices. She took refuge in England but was imprisoned there from 1568 to 1587 by her cousin **Queen Elizabeth of England**, when she began to gather support among English Catholics to overthrow her Anglican cousin Queen Elizabeth. Mary’s correspondence with her supporters during her imprisonment was encrypted using what is called as the **Nomenclator cipher** and the ciphered messages were hidden inside the bung of a beer barrel. We will see this in more detail soon, but a Nomenclator cipher is basically a simple substitution cipher but with extra substitutions for frequently occurring words, phrases, and names (to hide and distort the frequency statistics). This correspondence was intercepted and decrypted by Elizabeth’s officials, and then resealed and sent on to the intended recipients. Mary’s correspondence contained her plans to not only escape from imprisonment but also to assassinate Queen Elizabeth (so that Mary could claim the English throne for herself). However, Mary and her conspirators openly discussed their plans at length (oblivious to the efforts of decipherment by the officials employed by Elizabeth) in these encrypted letters, as they believed no one else would be able to read them. But, this substitution cipher was indeed deciphered by the officials of Elizabeth (Walsingham and Phelippes) using the combination of the same frequency analysis and crib attacks as enumerated above. With the encryption system broken, Walsingham could easily monitor the message exchange between Mary and the conspirators, which became more and more intensive. Finally, Walsingham and Phelippes faked a message to Mary asking her to provide a list of the conspirators; a plan that succeeded. Based on this evidence, Mary’s conspirators were arrested, condemned to death and executed in 1586. After a separate trial, Mary, Queen of Scots, herself was found guilty of treason and beheaded on 8 February 1587. This correspondence was used as evidence at her trial.

A Nomenclator cipher uses a substitution but also in addition to that, uses more symbols for most frequently occurring words, names, and phrases so that no statistical exploitation of patterns in most frequent words and names can be used. We tend to do the latter to some extent too in our informal writing when we use “&” for “and” and smileys for words related to emotions and feelings. The specific cipher she used employed the following substitutions shown below.

[](https://substackcdn.com/image/fetch/$s_!w1aQ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a1ede7e-5654-4ada-a69a-b5c180aa46c5_998x476.png)

![](https://substackcdn.com/image/fetch/$s_!w1aQ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5a1ede7e-5654-4ada-a69a-b5c180aa46c5_998x476.png)





How to detect a Nomenclator cipher? Once again, when the symbols used are far greater than 26 (or the number of letters in the alphabet of the target language), what we are seeing is either a **Nomenclator cipher** or a **Homophonic cipher** (where more frequent letters are mapped to more than one symbols) or a combination of both. How does one crack and solve a Nomenclator cipher? If there are substitutions of too many words by single symbols and there are large number of such symbols representing words, it is indeed very difficult unless we have a lot of clue. But, when the symbol size is manageable (like the one used by Mary), we can indeed get some progress on it. Once we are able to eliminate the words, we can use the usual frequency analysis for the letters. But, there is no neat approach for it and it depends on the specificity of the problem. analysis. We don’t know exactly how Phelippes worked, but probably he assumed that the most frequent symbols stood for the most frequent letters of the English language, though he may have been confused by a few nulls (symbols that did not correspond to any letter or word and inserted purely to confuse decipherment). After some analysis, Phelippes was able to reconstruct the whole nomenclator as shown in the figure above.

------------------------------------------------------------------------

# Vigenère Cipher



In this section, we will survey a more complex substitution cipher where the substitution of a letter depends on the place in which it occurs in the message. To demonstrate this, let us take a specific example of what is called the **Vigenère cipher** (named after a 16th French diplomat and a mathematician) that is known to have been used by the Confederacy against the Union in the American Civil War.

[](https://substackcdn.com/image/fetch/$s_!z2HT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27aa1220-8652-4e64-8f4c-87694ea46ad5_1280x853.png)

![](https://substackcdn.com/image/fetch/$s_!z2HT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F27aa1220-8652-4e64-8f4c-87694ea46ad5_1280x853.png)





A reproduction of the Confederacy's cipher disk used in the American Civil War on display in the National Cryptologic Museum

This is based on the Caesar cipher but works in a more complex way. It uses a sequence of varying Caesar ciphers in rotation that is determined by a decryption key which is basically a sequence of letters. Let us say for example that the decryption key is JOEY. First, the number of letters in the key is 4. The letters in the key are J, O, E, and Y. Let us figure out how much they are shifted relative to the letter A.

> A → J = 9 shifts to the right  
> A → O = 14 shifts to the right  
> A → E = 4 shifts to the right  
> A → Y = 24 shifts to the right (or 2 shifts to the left)

Now, in the plain text message, what we do is that we lay the plain text right below the repetitions of the key. Then, for every letter, we implement a Caesar cipher with a shift depending on what letter in the key is below it (if it is J, we do 9 shifts; if it is O, we do 14 shifts; if it is E, we do 4 shifts; if it is Y, we do 24 shifts). An example of this is shown below.

[](https://substackcdn.com/image/fetch/$s_!aUZz!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e95d893-deb5-4887-892b-d143380c9943_1536x1024.png)

![](https://substackcdn.com/image/fetch/$s_!aUZz!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0e95d893-deb5-4887-892b-d143380c9943_1536x1024.png)





Now we show another example of this cipher with a three-letter key.

[](https://substackcdn.com/image/fetch/$s_!JF5F!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00bb469e-c82c-4b07-9145-41d118b97401_1048x646.png)

![](https://substackcdn.com/image/fetch/$s_!JF5F!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F00bb469e-c82c-4b07-9145-41d118b97401_1048x646.png)





Here, we see that we use four Caesar ciphers of shifts 9, 14, 4, and 24 and rotate them periodically to encrypt letters. We see that the E in the word ONCE and the E in the word TIME go to different cipherletters (C and N respectively) because they align with different key letters in this rotation (Y and J respectively). The following write up below narrates a running story in this encryption.

> Full ciphertext :
>
> XBGC DDSL J HMKN O QGPVXW UWSL UWZCM WR Y PFIYC TSPNGX. FN KEQ OSEPNR
> FW NJIPH QVCJHYPN KLM BVEPNR XFN KSMMG AGCV LGV. VMQ YCACATYJ KCHW JBH
> RNFVGKZI PXOV KJRI CESR RQS FPJJIQC ORGVOPQ JJSGM VMQ YOXF. XBI UJFQ
> YOHIPWCSL CVI JRCR DRBMQQSH FDBXGWU ELM ZEW KSRCJHL Y BVEBH HVCN. GSMW
> VI DNZP GWHS Y MSIN BZICY.
>
> O PGCHPC VCYQN ZMTNR RCJFFW. CVI KXIWC LOQC XIX QNOVAQWRE OCV DXCH YWR
> FCPOR PDBRGWU XFACYEQ HLC PFEQB. VI BRR RMC BSRRQI RQS WJNSTGWU PGXB
> YLCWP FN OGARRILCOPJH FEL JQVMBG XFN ZMMWG ILXFQMDG TYF. HLC UWSL
> JKSIN WQKNRMYCSPW. QS TJJQIB QWW NJK STNF XFN TVGPVXCWSH KXIWC JBH
> NASTYASH RX YMJU VMK.
>
> CVI KXIWC CFIKKZIB FWXF OSEP. QS FCPUIB CVI JRCR RX GTYAS LGB ZMDN. VI
> NACQGBSH RQOX QXAIBJM LC FCYJM FINJM XFN YMLMBIQB. HLC UWSL OCYLM HLGB
> WHCJ OQSBWRE. QS GMDZH LXH MKJUMLN VSU BIGF J HMLH QVCJHYPN QSSUR ITNF
> LCUD EL JBMKJZ EQ BHVMWU EQ QWQQNZJ. QCWPJ CVI JRCRQ JBKCA
> RMQJDTCJFIB. QS PGOHIB QWW NJK ELM OPJXKIB CVI KXIWC CC IQLOTC.
>
> BSZCAOP BJMW NJGWCM. CRC VCVLRBK FDBXCAG ILCSVCM HLC OCVCBH ELM DPYLSH
> Y BHVMWU RCC OQMWU XFN HVCNG. XFN ZMMW KELMSVCM HLPXIKF CVI UXCHQ JBH
> QCSTNNR HGASGRUM MLCC XFN HVYY. HLC WSX RRULRNBIB JFSSWR LGB PSBH. VI
> QCFYEPZIB FWXF JZP FRG WRASRECV. CCC SZCAM QMESQCWH SLUM QYMS XFN
> FSNNG XGPVXCW TYPCVIP. JH PYBH XFN SBFJIWRNR PGXB VMJFIB MSWNNFERNZC
> DXF LCUD.
>
> XFN ZMRCZI KXIWC QSEPM HLC ACEP OFSK OOV YFOC. FN FIAXURGBSH RQS ZMRQI
> MO HLC UWSL FVS FJR WNJFIB QWQ. FN VYPAWIB CVVMDUL RQS JMASWR DBXGU VI
> PNOGFNR XFN HVYY. HLCAS LC BOA RQS KPNOX JRCR JHWRE QSPNUSWQ KSRCJHL
> RQS VMYSW.
>
> RQS QMDGI GVAIBROXCUM FCPOR UXFOGWU. LC YFIQBSH FRG WFJFT RNSXF
> JUEGWGX MWS SD CVI PXDIQ JBH QCOVRNR FGCWRE. CVI PXDI UJG XFRQO YWR
> XFN KSPT KEQ MWJDRQYJC. HLC VCYQN QSLCWRSNR TYCWILCZC. QUCAJH HLC
> OWFPNG FPXYI YYOVR. QS QMESH RX ORMCVIP ACTC JBH RQSR YWCXFNF. ER UOWR
> QS QYMS EL XDILRBK JJFKC NBSSPV JMA HLC UWSL CC IQLOTC.
>
> CVI JRCR PXGI DACQ RQS FPXYIL WSX YWR PMXYIB JH XFN ASSBS AGCV
> KPJHMRDRI. FN FIKNAFCASH FXK LC QOH JJIKFNR AFNB XFN ZMRCZI AASERDFI
> NACQGBSH RX FINJM LGV. BSU QS YLMSVQCCSB CVER BHVCWUXF LCYJM OTNNOV GW
> IRCGDIACSH DXFQQ. QWW EASER LZEUB ORB YCACATYJ VIWAUSW FJR FCNB
> YQNZIQB OKYRBWR CVI FDBXCAG RCC. HLC CWRW CSIRQ CJ RQS QMDGI FJR
> EALCQNUWWFNR AFJH LGB GXPNBKRQ QSSUR RMC.
>
> HLC VCYQN KEQ YZIYBSH RQOX FN VEB TSTR QWW NACQGBS. XFN ZMMW HLYWYIB
> QWQ YWR RCESV YPOML SIHENR ELXHLCA QVCJHYPN AIPNZC ZH WXQ BWDC. CVIW
> YOVRNR EQ OFMCWRW YWR GYAFMCM HLC USWQXB AGCV XFNA XFACYEQ HLC OCVCBH.
>
> OGWRRCBG MQ WSZCA KEQCSH. Y PSRCACYQ JQX KJM VCCIVL FVIL RH MQ USEQC
> SBNNQXCM. BS AASERDFI GB GS QVOPJ CVER RH GYWBSR KS YQNTYJ. WC
> GPNOXSAS MQ BC TMFSVDDZ XFJH MR FWPJ WSZCA BICM VIJY.

This seems to be much more sophisticated than the simple substitution ciphers. Here, a particular letter in the plain text is not mapped to a unique cipherletter but is mapped to any one among four different possibilities of cipherletters based on its position in the rotation scheme of the four Caesar ciphers. So, this evens out the statistical patterns of the English language. For example, the frequency histogram of the letters for the above text is shown below.

[](https://substackcdn.com/image/fetch/$s_!d0Mo!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4eb76340-0019-4b3e-8868-0dd289ad1773_1722x1108.png)

![](https://substackcdn.com/image/fetch/$s_!d0Mo!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F4eb76340-0019-4b3e-8868-0dd289ad1773_1722x1108.png)





There is no letter that occurs more than 12% here as with the natural English text where the letter E occurs a little more than 12% of the time. Here, the most frequent letter is C that a little less than 9% of the time but we see that the distribution above is much more evened out compared to the distribution in the original English language which is shown again below for recollection.

[](https://substackcdn.com/image/fetch/$s_!_Jvf!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8cf9c2ef-b084-4359-8620-d4223fd21e53_3126x1376.png)

![](https://substackcdn.com/image/fetch/$s_!_Jvf!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8cf9c2ef-b084-4359-8620-d4223fd21e53_3126x1376.png)





Therefore, the Vigenère Cipher disguises the letter frequency of the underlying language in its ciphertext. Also, a brute force attack appears to be impossible here as it would lead one to guess the decryption key which can be any sequence of letters of any possible length. For centuries, the Vigenère cipher and other polyalphabetic ciphers were considered unbreakable by many, ‘*le chiffre indéchiffrable*’ (the indecipherable cipher). But, it turns out that this cipher too can be broken if the text is much longer by adopting a more intelligent strategy. The approach to break this cipher is called the **Kasiski** **test** which was also independently cracked by **Charles Babbage**.

The first step in this test is to determine the number of letters in the key which is equal to the period of rotation of the Caesar cipher schemes (in our case, it is 4 as the key is JOEY which has four letters). Let us now choose a small word in the English language that occurs very frequently like THE. Since the period is 4, there are four possible encryptions of the word THE, depending on where exactly in the periodic cycle the word lies (it might be some other number than 4 but some small number in general). But since it just four possibilities and the word is very frequent and occurs a lot of times, we see that it has to pass through only four possibilities and hence there will always be a repetition. So, we look for three letter sequences that repeat a lot in this ciphertext. The sequence XFN seems to be occurring a lot in the ciphertext (about 17 times). The ciphertext with XFN highlighted is shown below.

[](https://substackcdn.com/image/fetch/$s_!KYVT!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F284a8438-03bf-4469-b1e5-bea029f11d9b_1182x1290.png)

![](https://substackcdn.com/image/fetch/$s_!KYVT!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F284a8438-03bf-4469-b1e5-bea029f11d9b_1182x1290.png)





Let us observe carefully one segment of a text beginning from one XFN to the next. It is shown below.

> **XFN** HVCNG. **XFN**

The space between them is 8 letters. Which means that the consecutive XFNs are sepearated by a distance of 8 letters. But we know that since the same XFN ciphers denotes the same word or sequence in the plain text, they have to be in the same periodic rotation cycle of the keys. This means that the distance between them (which is 8 here) must be an integer multiple of the period of the key (as a rotation cycle repeats every period). What numbers are divisible by 8? They are 1, 2, 4, and 8. So, the period has to be one among one of these four factor numbers. We have narrowed the period (the number of letters of the decryption key) to just four possibilities. The highest possible candidate among them is 8 (we know that the actual period is 4 but let us assume we do not know about this). What we know from the guess is for sure that every eighth letter is encrypted using the same Caesar cipher (it is actually every fourth letter but if it holds for every fourth letter, it holds for every eighth letter too). Given that every eighth letter is known to be using the same Caesar cipher for encryption, what can we do now? We can now observe every eighth letter in the ciphertext as shown below.

[](https://substackcdn.com/image/fetch/$s_!_OtW!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F734f5d1a-5754-41c4-b278-0fe309fabeb1_1208x1140.png)

![](https://substackcdn.com/image/fetch/$s_!_OtW!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F734f5d1a-5754-41c4-b278-0fe309fabeb1_1208x1140.png)





We know that all these eight sequences of letters use the same Caeasar cipher. We can use the same technique we used to decipher the Caesar cipher to these eight batches of letters separately in the ciphertext that observe the ciphertext every eight units (by observing the frequency distribution of letters every eighth letter and comparing it with that of the expected statistics of the English language). We can see where the letter A goes to in all these eight parts of the ciphertext and we could get JOEYJOEY which is the key that we have but repeated twice. In principle, each segment of the tet might have used a substitution cipher (instead of the Caesar cipher) and we can still apply the methods of deciphering simple substitution ciphers by observing every eighth letter.

Thus, the Kasiski test takes advantage of the fact that most frequently repeated words are sometimes encrypted using the same key letters (when they are separated by integer multiples of the period and thus falling into the same cycle), leading to repeated groups in the ciphertext. This lets us narrow down the period at least by some multiple and applying statistics to every periodic repetition enables us to decipher the ciphertext if it is long enough (so that not many cycles of periodic rotation have passed through in the length of the message). For this encryption to be secure, the period has to be long enough and comparable to the length of the message. But, if the period is comparably as long as the message itself, the next question to ask is how do we share such a clumsy key with so many letters (as long as the text itself) beforehand? The period cannot definitely be very large because otherwise communicating it would be as difficult as communicating the original message.

The moral of the story seen so far is that periodic rotation of a set of simple substitution ciphers is not a foolproof encryption mechanism either and can be decrypted when the message length becomes very large compared to the period.

Just in case you were wondering what did I actually encrypt in the example text using my Vigenère, here is the actual text.

[](https://substackcdn.com/image/fetch/$s_!0pPE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F28d62941-fbfb-480a-a625-1c8c1fe09d82_1318x1226.png)

![](https://substackcdn.com/image/fetch/$s_!0pPE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F28d62941-fbfb-480a-a625-1c8c1fe09d82_1318x1226.png)





Example 4.1 : **Kryptos Sculpture**

We already introduced in Example 2.1. The lines 3-13 on the top left reads :

> VFPJUDEEHZWETZYVGWHKKQETGFQJNCE GGWHKK?DQMCPFQZDQMMIAGPFXHQRLG
> TIMVMZJANQLVKQEDAGDVFRPJUNGEUNA QZGZLECGYUXUEENJTBJLBQCRTBJDFHRR
> YIZETKZEMVDUFKSJHKFWHKUWQLSZFTI HHDDDUVH?DWKBFUFPWNTDFIYCUQZERE
> EVLDKFEZMOQQJLTTUGSYQPFEUNLAVIDX FLGGTEZ?FKZBSFDQVGOGIPUFXHHDRKF
> FHQNTGPUAECNUVPDJMQCLQUMUNEDFQ ELZZVRRGKFFVOEEXBDMVPNFQXEZLGRE
> DNQFMPNZGLFLPMRJQYALMGNUVPDXVKP

Try to break this assuming it is a Vigenère cipher. Check your answer at the end of this article.

------------------------------------------------------------------------

# Enigma Machine



[](https://substackcdn.com/image/fetch/$s_!5088!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F453fc6e8-f120-457d-a4e1-721650fcbc48_1039x1133.jpeg)

![Enigma machine with plugboard and rotors](https://substackcdn.com/image/fetch/$s_!5088!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F453fc6e8-f120-457d-a4e1-721650fcbc48_1039x1133.jpeg "Enigma machine with plugboard and rotors")





Enigma machine with plugboard and rotors.

In this section, we will see the encryption used by the Nazis to secure their communication and how the Allies managed to decrypt them. It is a more sophisticated version of the previous Vigenère encryption in the same way that the Vigenère encryption itself is a more sophisticated version of the Caesar / simple substitution encryption.

### Architecture of the Enigma



The Enigma machine is an electromechanical device such that when a key corresponding to a particular letter is pressed, the circuit design makes the display of some other letter to be on and hence get typed. But, what letter exact letter got displayed depends on a complex mechanism. One of the most important parts of the machine is called the rotor system. To understand easily how the system works, I have given the illustration for the case when there are only six alphabets (A-F) and three rotors (note that the actual machine was designed for twenty six letters and sometimes four rotors). First, observe the diagram below and then let me explain.

[](https://substackcdn.com/image/fetch/$s_!6FAJ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe242484f-0751-409f-b18d-a31728f01723_1042x786.png)

![](https://substackcdn.com/image/fetch/$s_!6FAJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe242484f-0751-409f-b18d-a31728f01723_1042x786.png)





Rotor encryption machine using a number of wired rotors. Pressing a key (plaintext) completes an electrical connection and causes a letter lamp (ciphertext) to light up.

When the key A is pressed, this completes an electrical connection (which is shown dark in the figure above) which makes the lamp representing a ciphertext letter light up (in the figure above, it is B as shown in the bulb). Similarly, by tracing the remaining dotted lines from the respective keys corresponding to their alphabets, you can figure out what cipher letter bulb will glow. But, if the entire setup were static, then this would just be another example of a simple substitution cipher which can easily be cracked. The thing is that the positions of the rotors get rotated as one types along the machine. After each letter is entered, the rightmost rotor (here \#3 in the figure) turns by one unit. After a complete turn of this rotor (six units here since there are six alphabets only here), the next middle rotor (here \#2 in the figure) turns by one unit, too; and once this middle one has revolved fully, the last rotor (here \#1 in the figure) moves by one unit.

[](https://substackcdn.com/image/fetch/$s_!t2iE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1caad4ee-91a4-4820-8ea0-8275197d52f9_4034x3275.png)

![](https://substackcdn.com/image/fetch/$s_!t2iE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1caad4ee-91a4-4820-8ea0-8275197d52f9_4034x3275.png)





Enigma rotor assembly. In the Enigma, three movable rotors are sandwiched between two fixed wheels: the entry wheel, on the right, and the reflector on the left.

This is exactly how the rotors work in the mechanical odometer counter in your bike or car that keeps track of how many kilometres (or miles) you have travelled. The rightmost counter represents the last digit for your kilometre and hence turns by one digit for every one kilometre distance you cover. The next left odometer counter which tracks the second digit fom the right rotates by one revolution only after your first rotor completes a full revolution so that after 10 kilometres, the rightmost odometer comes back to 0 (after completing a full cycle 0 → 1 → 2 → … 8 → 9 → 0) whereas the counter to its immediate left shows 1 and hence together, they read 10 which is ten kilometres. In the same way, in the enigma machine, the substitutions done by each rotor is not static but rotate with nested periods like your car’s speedometer where the rotor to the left rotates its substitution by one unit every time the rotor to its immediate right rotates through the entire alphabet. So, if there are 3 rotors with 6 alphabets, the periodicity of the entire encryption would be 6 x 6 x 6 = 216 letters after which all the rotors come back to the initial position of their substitution. In case we have 26 alphabets and 4 rotors, the periodicity is 456976 letters, which is very large (for three rotors, it is 17,576 which is still a large number). Since the lengths of all the messages communicated via these enigma machines hardly exceed even a few hundred letters, they are way below this threshold length of 17,576. Hence, one cannot use the method we used in the last section to break this cipher by observing just a few hundred letters.

[](https://substackcdn.com/image/fetch/$s_!rgOX!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F082ecbf7-0d91-4be2-9a5c-b6d5f6e45971_600x564.png)

![](https://substackcdn.com/image/fetch/$s_!rgOX!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F082ecbf7-0d91-4be2-9a5c-b6d5f6e45971_600x564.png)





> Note : This odometer picture for the rotors is not exactly true. The
> real Enigma used turnover notches and exhibited a phenomenon called
> "double stepping", so its stepping sequence was slightly more
> complicated than a sequence of three literal base-26 counters.

There are more things that further complicates the design of this machine. For a complex machine like this, we need to figure out the inverse mapping of all of these maps under each rotor configuration and build another machine with rotors. So, we have to build two machines - one for encryption and another for decryption, which is very cumbersome. So, actual enigma machines used another trick so that the machine itself served as both the encryption and decryption machine. Which means that if you enter HEIL HITLER in the keys of the machine and you get out CVXR UIOAE as the cipher text in the display, then when you enter CVXR UIOAE in the keys of the machine, you get back HEIL HITLER in the display. This ensures that the same message can be used for both encryption and decryption. A person wanting to send HEIL HITLER will type it into the machine and send CVXR UIOAE while the person receiving that encrypted message CVXR UIOAE will type it into the same machine and get back the original message which is HEIL HITLER. How could this be done? Look at the illustration below, which is again shown for the case of six letters and three rotors. There is an additional device after the rotors called the **reflector** (**Umkehrwalze**) at the left most section which exchanges letters in a fixed manner and traces the reverse of the rotary circuit going back to right from left. Now, you can verify for yourself by tracing the connections that when you press A in the key, if E glows up, the symmetry of the circuit because of the reflection and reverse tracing, ensures that when you press E at the same rotor configuration and start from there, you come back to A while ending the circuit by tracing the same path in reverse.

[](https://substackcdn.com/image/fetch/$s_!3DcE!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dc301dd-dd65-4bd8-8bea-0e32efe43fd2_1028x620.png)

![](https://substackcdn.com/image/fetch/$s_!3DcE!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F7dc301dd-dd65-4bd8-8bea-0e32efe43fd2_1028x620.png)





The rotors along with reflector circuit.

To add one more final layer of complication, the machine had another **plugboard** or **stecker** placed directly between the keyboard and the first rotor. It swapped pairs of letters (usually 10 pairs out of 26) before and after they passed through the rotor assembly. A basic Enigma machine had 158,962,555,217,826,360,000 possible keys and used a complicated encryption process. This led the users to believe that the Enigma machine was unbreakable. **An extremely important feature of the Enigma machine is that this steckerboard (plugboard) is reciprocal**. If the steckerboard maps "A" to "E", then it also maps "E" to "A". They were made of pairwise swaps. This was to ensure that the encryption matched with the decryption. This reciprocal nature of the steckerboard is not required for the Enigma machine to work was exploited by Turing and others to crack the ciphers.

[](https://substackcdn.com/image/fetch/$s_!lcMI!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8231e57-2236-494a-886e-801d0c2aa6f4_844x646.png)

![](https://substackcdn.com/image/fetch/$s_!lcMI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fe8231e57-2236-494a-886e-801d0c2aa6f4_844x646.png)





The Enigma was incredibly difficult to crack for two reasons:

1.  The specific circuits that connected key entries to lampboard
    outputs depended on the configuration of the steckerboard
    (plugboard) and rotors, of which there were *way* too many to
    exhaustively search. Also, these were instructed to be changed from
    day to day.

2.  The internal circuitry changed with every keypress due to the
    rotation of the rotors. Since the rotors inside the Enigma machine
    would rotate each time the user pressed a key, completely changing
    the internal circuitry, if a user keyed the string `AAAAA` into the
    machine, they would not get a string of 5 of the same characters
    back out. They would get something like a cipher like `RBUEL.`

If you want to simulate the Enigma using a C program, click [here](https://vanhunteradams.com/Enigma/Enigma.html).

### Using the Enigma



Encryption :

1.  The Enigma operator consults their provided codebook, and configures
    the steckerboard and rotors in accordance with that date’s
    specifications, which is pre-decided (this means that it changes
    everyday). He rotates the rotors to the correct *indicator setting*.
    The indicator setting tells the operator which characters on each
    rotor should be rotated to be facing directly upward.

2.  The operator then thinks up a random 3-character sequence (a code
    for resetting the three rotors) that they will use to encipher their
    message. They code this sequence into the Enigma, and they write
    down the output sequence. For example, the operator may decide to
    encipher their message using the sequence `EVN`. They would key
    `EVN `into the Enigma and some other sequence, perhaps `SDK` would
    be output from the Enigma. The operator would take note of the
    sequence `SDK`. In this example, `EVN` is the “message setting” and
    `SDK` is the “enciphered message setting.”

3.  The operator would then rotate the rotors in the machine so that
    their chosen message setting, `EVN`, was facing directly upward. The
    machine is now ready for enciphering.

4.  The operator would key the plaintext into the machine, and record
    the ciphertext. For example, they may key in `HELLOWORLD` and it
    would be enciphered to `ONENUUNPOX`.

5.  The operator would then send *both* the enciphered message setting,
    and the enciphered message.

Decryption :

1.  The receiving Enigma operator would have the same codebook in their
    posession as the sender, and would configure their Enigma machine in
    accordance to that date’s specifications (which would be exactly the
    same as those that the sender used).

2.  The operator would then key in the enciphered message setting `SDK`.
    Because of the reciprocal nature of the Enigma, this would output
    `EVN`, the message setting that the sender used to encode their
    message.

3.  The operator would then rotate the rotors in the machine so that the
    deciphered message setting, `EVN`, was facing directly upward. The
    machine is now ready for deciphering.

4.  The operator would key the ciphertext into the machine, and write
    down the plaintext returned by the machine. In this example, the
    operator would key in `ONENUUNPOX` and the machine would output
    `HELLOWORLD`.

Note that the Enigma did not support spaces, punctuation, or lower case letters. All these were to be determined from the context and intuition of the German language. The character `X` was sometimes used to represent a space, if there was any ambiguity.

So, given this much complex design and use of the encryption, how did the mathematicians in the service of the Allied forces crack the Enigma cipher without having direct access to the details of the circuitry of the Enigma machine? The mathematics is complex and involves the knowledge of a branch of mathematics called “**Group Theory**” which is a branch of mathematics that studies the symmetries of transformations of objects. So, it cannot be described in a small section in this article and deserves an article of its own, wherein I teach group theory in detail. So, I will later write a dedicated article about it in the future. Here, I will just lay down the gist of the decipherment work in the remainder of this section. The first work in breaking the Enigma machine was conducted by Polish cryptographers in the 1930s. The subsequent wartime effort was centred at Bletchley Park in England, which is now a museum. It is estimated that this work shortened the war by two years.

The key breakthrough came in when Alan Turing worked through the mathematics of these complex rotor operations and proved one important result which came to be the Achilles Heel of this machine. It is the result that :

> **A letter in the plaintext CANNOT encrypt to itself in the ciphertext
> under any rotor configuration**

This result above is mathematically a little intricate to prove and hence is not given here. It means that when you type A, no matter whatever is the state of the rotors, the bulb corresponding to the letter A will not glow for sure. Same for other pairs of letters. Alan Turing used this result, combined with a 'crib' (a guess at what part of the plaintext might say), to logically eliminate trillions of incorrect machine configurations. For example, let us assume that the cipher message starts out as

![](https://substackcdn.com/image/fetch/$s_!vh8-!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9dbcefa7-6e37-42b0-a991-d1224b414b76_1732x96.png)

Let us say that we know that somewhere in this beginning segment, lies the cipher for the phrase SECRET MESSAGE (this is the crib which we know to be there in the message for sure). Now, we know the result that under no circumstances, a plain text letter will map to itself after encryption into a cipher. So, let us place the crib below the ciphertext and keep sliding. If at any configuration, we find that a letter maps to itself, we eliminate that possibility and keep moving ahead. Doing so, we eliminate many possibilities and are left with only two as shown in the picture below (the cribs used actually were German phrases like HEIL HITLER or LEUCHTTONNE).

[](https://substackcdn.com/image/fetch/$s_!Vv8x!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffbbb3ca9-eb7c-4183-aa74-ad61c6e3d649_1700x1410.png)

![](https://substackcdn.com/image/fetch/$s_!Vv8x!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ffbbb3ca9-eb7c-4183-aa74-ad61c6e3d649_1700x1410.png)





Picture source : https://www.101computing.net/enigma-crib-analysis/

Let us say that we are able to figure out exactly where the crib is located in the ciphertext by eliminating invalid alignments using context, procedural clues, and the fundamental Enigma rule: **no letter can ever encrypt to itself**. Once aligned, we establish an exact letter-by-letter pairing at consecutive machine steps. Let us say that we know that the phrase SECRET MESSAGE is there in the plain text and corresponds to the phrase YSAWQSTNTLGKP (the answer 4 in the picture above).

Because the rotors step forward with every single keystroke, the internal circuit changes after every character. But, the inside of an Enigma was predictable: if you knew the rotor positions, you knew exactly how the wheels scrambled a letter. The real nightmare was the **plugboard on the front**. It swapped unknown pairs of letters using patch cables (like plugging `A` into `J`). There were over **150 trillion** ways to plug those cables in. Testing every rotor position combined with every plugboard variation was physically impossible. Turing’s genius was finding a way to test and figure out the rotors **without** having to guess the whole plugboard. Simply typing the plaintext into a test machine with guessed rotor positions will not produce the ciphertext, because an incorrect plugboard setup will scramble the letters into random noise (there are no “close misses” in cryptography).

This is where Alan Turing’s mathematical magic comes in. Instead of testing 150 trillion plugboard combinations by brute force, Turing searched the crib for **closed loops of letters** (known as a “**menu**”). For example, here our alignment shows SECRET MESSAGE → YSAWQSTNTLGKP. Then we know that there is a closed loop in this exact crib. Look at the relations involving letters **S** and **T** in the mapping :

- At **Step 6**: Plaintext `T` maps to Ciphertext `S` (meaning T⟷S at
  position 6)

- At **Step 9**: Plaintext `S` maps to Ciphertext `T` (meaning S⟷T at
  position 9)

Tracing through the steps forms a **2-step cycle**. This forms a closed logical loop.

![](https://substackcdn.com/image/fetch/$s_!kUOD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F1661bf41-dfb4-44f7-baf6-1c97f73dd10b_414x134.png)

Suppose we want to test if the rotors were set to the position 01-02-05. Doing this deduction by hand on paper took hours. Turing built a machine, **the Bombe**, to do it at the speed of electricity.

- **Simulating the wheels:** The Bombe contained dozens of stacked
  Enigma rotors wired together according to the crib’s loop.

- **Injecting the guess:** An operator sent an electrical current into a
  wire representing a single guess (e.g., *“Current on wire A”*).

- **The chain reaction:** The current surged through the simulated
  rotors, hopping from letter to letter just like our deductions.

- **The Welchman Diagonal Board:** Gordon Welchman added a
  cross-switchboard ensuring that if the machine deduced `R` connects to
  `K`, it automatically electrified `K` connects to `R`.

- **The “Stop”:**

  - If a rotor setting was **wrong**, contradictions multiplied
    instantly. Electricity back-fed through the loops and energized
    almost all 26 wires at once. A relay detected this flood and kept
    the electric motor spinning to the next rotor position.

  - If the rotor setting was **correct**, the circuit did not
    short-circuit into contradictions. The electricity remained confined
    to only the logically consistent wires.

  - The motor would abruptly **clunk to a stop**.

The Bombe tested candidate rotor orders and positions systematically, stepping through the 17,576 possible rotor configurations at high speed. At each position, it made a provisional test guess about a single plugboard cable (e.g., *“Suppose letter E is swapped with letter A”*). It then routed an electrical current through the rotor banks corresponding to the steps in the loop. If that initial guess was logically impossible, the circuit quickly cascaded into an absurd contradiction (such as implying that plugboard socket **E** must be simultaneously connected to both **A** and **K**). When a contradiction occurred, the electrical current energised a relay that rejected that setup and advanced the Bombe to the next rotor position in a fraction of a second. Only when a configuration generated **no contradictions** did the Bombe stop. This narrow set of “stops” handed the codebreakers the correct rotor positions and the core plugboard pairings, cracking the day’s cipher without ever needing to guess through trillions of combinations.

------------------------------------------------------------------------

With this, I hope you enjoyed the first article in this series, In the next and last article in this series, I will introduce modern methods of cryptography that involves the extensive use of computers and algorithms over representations of messages in binary bits (as computers represent everything as sequences of 0s and 1s) . Await the link for the next article in the series here.

------------------------------------------------------------------------

# Answers



**Solution to Example 1.1**

Ignoring the YPs, the decrypted message is :

> YOU’LL RECEIVE \# MRR STRIPS MAKE SURE THAT YOUR HANDS ARE COMPLETELY
> DRY BEFORE YOU TOUCH THEM. DON’T RIP THEM AND MOST IMPORTANTLY DO NOT
> GET THEM WET. TAKE \# OR OF THEM FOLD THEM TOGETHER AS SMALL AS
> POSSIBLE TIGHTLY SIR-RAN-WRAP THEM TWICE. PUT THEM INSIDE OF A RUBBER
> COMPRESS IT TWIST THE RUBBER AND TIE A KNOT. CUT THE EXCESS RUBBER OFF
> THEN PUT IT INSIDE OF ANOTHER AND DO THE SAME THING. REPEAT THAT
> PROCESS \# I TIMES THE FINISHED PRODUCT SHOULD BE LAYERED WITH \#H
> COATS OF SIR-RAN-WRAP \#I RUBBERS THEN REPEAT THE SAME STEPS FOR THE
> OTHER \# OR SO THERE WILL ONLY BE \#H THINGS FOR ME TO SWALLOW. MAKE
> SURE THAT YOU USE HAND SANITIZER BEFORE YOU COME IN

**Solution to Example 1.2**

The shift is just one letter where A → B. Using this, we see that the name of the city is BUNDESPLATZ.

**Example 1.3**

Again, the shift in the encryption is just by one unit to the left this time (A → Z, B→A). To undo this, shift every letter one unit right in the message. Without any space, you will get TOTALLYDISABLEDLONGITUDEFORTYLATITUDESEVENTYTHREE which when spaced appropriately, reads a TOTALLY DISABLED ; LONGITUDE FORTY; LATITUDE SEVENTY THREE.

**Solution to Example 2.1**

You can run the code and check that the index of coincidence is 4.5% which is way below the expected 6.8%.

**Solution to Example 2.2**

There are many directions one can take to decipher this but I am just giving the one I followed. We figured out that one of the symbols below is A and another is E.

![](https://substackcdn.com/image/fetch/$s_!1s-D!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faf97c25a-3582-40a5-bc92-14b1dd5ff24e_140x82.png)

But how to figure out which is which? Read the text again. We know that the letter A begins so many English words much more frequently than the letter I. In this text, we see lots of words beginning with the symbol below than the other one.

![](https://substackcdn.com/image/fetch/$s_!ZZrx!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F66d45154-9bbe-48df-ba0c-f52cf637dd65_78x82.png)

Hence, since A is much more likely to begin a word than I, and also A begins many words in English, we must have that

[](https://substackcdn.com/image/fetch/$s_!aRiG!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12bdf01d-b0fe-49ca-909a-fbe186ae8629_296x320.png)

![](https://substackcdn.com/image/fetch/$s_!aRiG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F12bdf01d-b0fe-49ca-909a-fbe186ae8629_296x320.png)





Now, see the three letter word in the line before the last which is

![](https://substackcdn.com/image/fetch/$s_!dpbN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc7a90b7d-d91b-4e5e-88de-ce874dde5fb7_118x50.png)

We see that it is the letter I followed by two consecutive letters. There is an apostrophe there. So, that word has to be I’LL and hence we have also now figured out

![](https://substackcdn.com/image/fetch/$s_!plcZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F42d8aac9-9f44-43f5-b72e-22342d4d63f8_408x236.png)

Note that even without the apostrophe, we know that there are only three words in English that begin with an I and followed by two same letters. They are ILL, I’LL, and INN. The latter is less frequent while the first two options give L as the candidate. So, we now have got three letters under our sleeve. We next observe another two letter contraction I ’ \*\*

![](https://substackcdn.com/image/fetch/$s_!-Qxc!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa0767fbf-7086-4d55-b67b-81b9e167a312_136x56.png)

The pronoun “I” has only two two-letter contractions - I’LL and I’VE. We already recognised I’LL and hence this one has to be I’VE. Hence, we have

[](https://substackcdn.com/image/fetch/$s_!WH64!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F426d8576-11ce-4ee2-9ba2-3746e45b48a7_402x488.png)

![](https://substackcdn.com/image/fetch/$s_!WH64!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F426d8576-11ce-4ee2-9ba2-3746e45b48a7_402x488.png)





Next, let us look at the word I’VE together with its next word as shown below.

![](https://substackcdn.com/image/fetch/$s_!EJ3b!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F9fc7eb4d-aee6-44b4-815f-ff4c015d1ab1_338x64.png)

We see that I’VE is followed by a four letter word of the form \*EE\_ where middle two letters are the same vowel E. In most probability (because of English grammar), this is the word BEEN. Hence, we now have the symbols for B and N.

[](https://substackcdn.com/image/fetch/$s_!006_!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c5fa82e-c82b-4b0d-aa55-0e5ae0c918ee_406x428.png)

![](https://substackcdn.com/image/fetch/$s_!006_!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2c5fa82e-c82b-4b0d-aa55-0e5ae0c918ee_406x428.png)





We now see a big word in the middle of the first line which is

[](https://substackcdn.com/image/fetch/$s_!RDnD!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec81e84f-5d34-44f0-a0c6-929a14020919_1238x486.png)

![](https://substackcdn.com/image/fetch/$s_!RDnD!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fec81e84f-5d34-44f0-a0c6-929a14020919_1238x486.png)





Based on what we know so far, it is of the form \_*ENE\*A*\_ \_\* where the \* should correspond to the same letter. This is most likely the word GENERATOR. Now, we got the symbols for the letters G, R, T, and O.

[](https://substackcdn.com/image/fetch/$s_!LhIN!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5837ea3-9d8f-4b88-967a-d3c60440f3f1_438x866.png)

![](https://substackcdn.com/image/fetch/$s_!LhIN!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc5837ea3-9d8f-4b88-967a-d3c60440f3f1_438x866.png)





In the last line, we look at the word below which we read as ABO_T.

[](https://substackcdn.com/image/fetch/$s_!Rvc9!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f5052e0-b97a-443c-96d7-b762ff33ec01_726x460.png)

![](https://substackcdn.com/image/fetch/$s_!Rvc9!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0f5052e0-b97a-443c-96d7-b762ff33ec01_726x460.png)





Clearly, this is the word ABOUT and hence we now also have the symbol for the letter U.

![](https://substackcdn.com/image/fetch/$s_!pTNG!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2fd4e833-3b86-4b9c-8b54-5681d82b5060_378x206.png)

Observing the following word, we think it must be READING and hence get the symbol for D now.

[](https://substackcdn.com/image/fetch/$s_!MILP!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18447cbf-c518-4943-b0c2-5fe0b05d94a7_826x402.png)

![](https://substackcdn.com/image/fetch/$s_!MILP!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18447cbf-c518-4943-b0c2-5fe0b05d94a7_826x402.png)





![](https://substackcdn.com/image/fetch/$s_!9iwC!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F017ef824-9948-4e15-b904-f7342b9fddb7_338x200.png)

Look at the following two letter word. It begins with O. There are only two two-letter words in English that begin with O. They are ON and OF. But clearly, it can’t be ON as we have already deciphered N. So, it must be OF and this enables us to read OF.

![](https://substackcdn.com/image/fetch/$s_!JiM4!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F8eb5b7cb-45ec-4935-9f7c-940545caea3c_112x58.png)

![](https://substackcdn.com/image/fetch/$s_!vffJ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1e491e1-60f4-4583-81b7-999ffdb70b1b_328x212.png)

Reading the following word in the end of the first line where only one letter is unknown, it must be ONLINE which gives the symbol for L.

[](https://substackcdn.com/image/fetch/$s_!4GVL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01a1b48e-819e-4699-a7a0-4fa06b1e4183_774x410.png)

![](https://substackcdn.com/image/fetch/$s_!4GVL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F01a1b48e-819e-4699-a7a0-4fa06b1e4183_774x410.png)





![](https://substackcdn.com/image/fetch/$s_!ZdI7!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc65562e2-fac9-4944-bd61-f48d5118e262_400x208.png)

We know look at this word pair in the last line shown below. The context is supplied from the previous two words which gives us the phrase ABOUT IT *\_IT\_ \_O*\_E

[](https://substackcdn.com/image/fetch/$s_!i7EZ!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa734a76-a6be-4754-b5ce-82f896440b5e_1120x430.png)

![](https://substackcdn.com/image/fetch/$s_!i7EZ!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Faa734a76-a6be-4754-b5ce-82f896440b5e_1120x430.png)





The phrase has to be WITH SOME and hence this gives us the symbols for W, H, S, and M.

[](https://substackcdn.com/image/fetch/$s_!_85B!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd88a9cf8-3326-490e-a4e7-f57880fc6a9e_462x970.png)

![](https://substackcdn.com/image/fetch/$s_!_85B!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd88a9cf8-3326-490e-a4e7-f57880fc6a9e_462x970.png)





Again, in the last paragraph, we guess the word HOLIDAY and get the symbol for Y.

[](https://substackcdn.com/image/fetch/$s_!V4VF!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd39880c0-11c6-4dcf-b7b1-ca5619547f61_854x414.png)

![](https://substackcdn.com/image/fetch/$s_!V4VF!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd39880c0-11c6-4dcf-b7b1-ca5619547f61_854x414.png)





[](https://substackcdn.com/image/fetch/$s_!7E1W!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F308d6926-0bbb-411e-b5d9-c0346f65db3f_376x244.png)

![](https://substackcdn.com/image/fetch/$s_!7E1W!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F308d6926-0bbb-411e-b5d9-c0346f65db3f_376x244.png)





If we try to read the entire last line, we get the symbols for few more letters.

![](https://substackcdn.com/image/fetch/$s_!otLI!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd79f59ec-68a6-4b65-a573-a00da8b7ab8b_1760x292.png)

By guessing the words ARTICLE and EXAMPLES, we get the symbols for the letters C, X, and P.

[](https://substackcdn.com/image/fetch/$s_!0XTL!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9a022cb-8552-4f1f-b6ac-779d7ef53e3f_408x742.png)

![](https://substackcdn.com/image/fetch/$s_!0XTL!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb9a022cb-8552-4f1f-b6ac-779d7ef53e3f_408x742.png)





I think the remainder of the letter can be read smoothly.

> HEY MARK,  
> SO I COULD NOT FIND A GENERATOR ONLINE BUT THERE IS AN AURUBESH FONT
> YOU CAN DOWNLOAD FOR BOTH MAC AND PC AND INSTALL. I’VE BEEN READING
> INTO HOW TO TAKE PICTURES OF INDIVIDUAL SNOWFLAKES. AFTER THE HOLIDAY,
> I’LL SEND YOU IN AN ARTICLE ABOUT IT WITH SOME EXAMPLES.

**Solution to Example 3.1**

Solution :

> START YOUR WALK AT THE PARKING PLACE NEAR BADENIA CREEK TEN MILES
> NORTH OF COOLINGTON ON ROAD TWO TWENTY FOLLOW THE FOOTPATH NORTH
> THROUGH THE FOREST AFTER ABOUT ONE KILOMETER TAKE A RIGHT AND WALK
> ALONG THE FENCE AFTER SIX HUNDRED METERS YOU WILL REACH A PICNIC PLACE
> WITH A PLAYGROUND IN THE CENTER OF THE PICNIC PLACE THERE IS A HAT IN
> THE LOWER PART OF THE REAR WALL OF THE HAT BEHIND THE BENCH YOU WILL
> FIND A SMALL PLASTIC BOX CONTAINING FURTHER INSTRUCTIONS GOOD LUCK

**Solution to Example 4.1**

Solution :

> IT WAS TOTALLY INVISIBLE HOWS THAT POSSIBLE? THEY USED THE EARTHS
> MAGNETIC FIELD X THE INFORMATION WAS GATHERED AND TRANSMITTED
> UNDERGRUUND TO AN UNKNOWN LOCATION X DOES LANGLEY KNOW ABOUT THIS?
> THEY SHOULD ITS BURIED OUT THERE SOMEWHERE X WHO KNOWS THE EXACT
> LOCATION? ONLY WW THIS WAS HIS LAST MESSAGE X THIRTY EIGHT DEGREES
> FIFTY SEVEN MINUTES SIX POINT FIVE SECONDS NORTH SEVENTY SEVEN DEGREES
> EIGHT MINUTES FORTY FOUR SECONDS WEST ID BY ROWS

------------------------------------------------------------------------

The next article can be found at :

(Wait for the link to be released)

[](https://substackcdn.com/image/fetch/$s_!5JVU!,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b940dba-95a2-401d-9f27-5c9a0ca399e0_1024x768.jpeg)

![How Does Cryptography Work? - Logsign](https://substackcdn.com/image/fetch/$s_!5JVU!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2b940dba-95a2-401d-9f27-5c9a0ca399e0_1024x768.jpeg "How Does Cryptography Work? - Logsign")





------------------------------------------------------------------------

#### Subscribe to Rama’s Substack

By Rama Seshan Chandrasekaran · Launched a year ago

My personal Substack

Subscribe

By subscribing, you agree to Substack's [Terms of Use](https://substack.com/tos), and acknowledge its [Information Collection Notice](https://substack.com/ccpa#personal-data-collected) and [Privacy Policy](https://substack.com/privacy).

[](https://substack.com/profile/175607674-gajah)

![𓃰 गज (Gajaḥ) 𓃰's avatar](https://substackcdn.com/image/fetch/$s_!0FKq!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc4cce856-fe09-4acb-aca7-abd3fcf353ae_4184x3152.jpeg)

[](https://substack.com/profile/284920280-ravinder-reddy)

![Ravinder Reddy's avatar](https://substackcdn.com/image/fetch/$s_!2Tvm!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F77da9531-28fb-41f8-b757-599e5b73f4c6_1202x1204.png)

[](https://substack.com/profile/7409416-che-naik)

![Ché Naik's avatar](https://substackcdn.com/image/fetch/$s_!IxR5!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F19c0010d-953b-42ea-ba29-d7ae428e3a3d_1660x1660.jpeg)

[](https://substack.com/profile/185382374-bhaskar-kamble)

![Bhaskar Kamble's avatar](https://substackcdn.com/image/fetch/$s_!EkBl!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbf8f0bc1-e9b7-45e9-b21d-615aeb35b3ef_400x400.jpeg)

[](https://substack.com/profile/415333735-amitesh-sirvaiya)

![Amitesh Sirvaiya's avatar](https://substackcdn.com/image/fetch/$s_!73i8!,w_32,h_32,c_fill,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F36318189-4f2a-4553-8f73-30a45d6d1b24_803x803.png)

17 Likes∙

[6 Restacks](https://substack.com/note/p-214447554/restacks?utm_source=substack&utm_content=facepile-restacks)



17





6

Share
