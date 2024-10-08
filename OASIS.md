# 1. Welcome
Introduced us to the syntax of flags which was **OASIS{_}**.<br>
Flag was already given in the challenge quesiton.
# 2. Flagged
Had to find the flag in the discord server. <br> First searched the message history with **OASIS{** prompt but could not find any other than members' messages. Later checked different channels of the server. <br>
Found the flag in the description of the *#rules* channel.
# 3. I swear it was right there
This one was one among the easiest. Found the flag on the desciption of a post from Cryptonite's Instagram handle. To be precise it was on the most recent post right after the pinned posts.
# 4. Ready Player One?
The attachmentt provided was an audio. It was very clearly and obviously an audio encoded with morse code.<br>
So I uploaded the audio to an online morse code decoder and got it decoded. Later submitted the flag in the asked format-OASIS{ALL CAPS}
# 5. Arte-Miss?
The provided attachment was an image. I first tried to find any hidden clues by zooming in and out of the image at various points. Then tried to find the blue color's hax code if I could go forward but it was a dead point.
<br> I surfaced the internet for image decoders and used the application *StegOnline* which helped me decode the image. It had various options of converting the image to a specific base color, extracting hidden files and data and finally hidden strings.
<br> The image had many hidden strings in it, but the first one which the application decoded was in the flag format and hence I found the flag.
# 6. String me to sleep
The attachement was a huge book with numerous pages. I simply used *ctrl+f* and gave in the prompt as *OASIS{*. <br>
As simple as that, I got only one result and it indeed was the flag for this challenge. 
# 7. This or that?
The alpha-numeric code did look like a hexa decimal code. I tried converting it from hexa-decimal to text. But the output was all symbols and it was not the right way to go. <br>
I asked chatgpt what to do witht this hexadecimal code, and it said I had to XOR it. I didnt know how to XOR a hexadecimal. <br>
But I am aware that XOR is a type of logic gate and it inputs only 0 and 1, the output is also 0 and 1. So trying my luck with this knowledge, I converted my hexadecimal code to binary this time and then used an online 
binary to XOR convertor. <br> Surprizingly I had to give a key for the XOR function to convert. I gave ARTEMIS as the key, but the decrypted output did not make sense. <br> 
I then gave WHISPER as the key and now I got the flag as my decrypted output.

# 8. Jekylle and Hide!
This challenge took me to a webpage of an E-Library with little to few books. It had a login interface, but it was dead. None of the buttons/books were dynamic. <br>
So I *inspected* the website and went through it's source code. It was written with internal method to add style to webpage. 2 files, one for the books. When clicked on the additional file it had many lines of codes.
<br> Coincidentally the word **username** caught my eye and it legit had a **if** code written for a specific username. I input that username on the webpage and it worked. I then asked my for a pin.
I again went through those files and *ctrl+f* for the keywords password/pin. I found the pin and it was the correct one. Finally got hold of this challenge's flag and it was the correct flag.

# 9. Keynough is enough
By looking at the challenge question I understood that the long alpha-numeric code and the term "ARTEMIS_WHISPER" were the only key take-away points. I searched online for *online code decoding* and found the application **cryptii**
<br> It had many variants of codes. I asked chatgpt which varient this code was, and it replied with 5 varients which could it could be. Luckily for me out fo those 5, only 2 were present in Cryptii - "Vigenere" and "Cipher". <br>
I tried cipher and all the 26 permutations, but it didnt make any sense. But when I switched to *Vigenere* it all made sense. In this varient I had to give a key on which it would encrypt the given code. <br>
I then gave WHISPER as the key and found my flag.

# 10. BasiKEllY
I again got a long alpha-numeric code to be decrypted. I was cluless on what it was so I asked chatgpt what type of code was this and how do I decrypt it. It replied saying that it was **base64** type.
<br> I proceeded opening an online base64 to text convertor but the output was not making sense as it was all symbols. *Coincidentally* the drop down menu had an option for conversion from **base32** as well.
And yes, when I did that, out of pure coincidence I got my flag. 
# 11. Key-Key do you love me?
This challenge really tested my communication skills. The **F.R.I.D.A.Y.** bot was not budging at all and kept on talking about 15 kittens and how they had to be kept safe. So I manipulated it. <br>
I made it to imagine that the kittens were in danger and only the password would help them, as assumed the bot gave in. The bot gave the password, once said the bot in itself gave the flag.
# 12. Microsoft StrongEdge
This one was also comparitvely easy. <br>
The attachment was a 4 slide ppt. I went through the presentation looking for hidden notes/texts but found nothing. I tried adding custom templates and found that slide 1 and slide 4 could get the template but slide 2 and slide 3 were not getting effected. I investigated more on slide 2 and slide 3 but found nothing. After further investigations of zomming in, zooming out, etc, I finally found a **minimized hidden image** in the left bottom corner of slide 1.
<br> It was a mirror image, once flipped horizontally it represented a code. From my knowledge in *challenge 9* I concluded that this code was a *cipher* and could be easily decrypted among the 26 permutations of each alphabet being shifter across. As guessed, it was indeed a cipher code and was successfully decoded. <br>
The decoded text was the correct flag.

X---------------------------X---------------------------X---------------------------X---------------------------X---------------------------X---------------------------X---------------------------X---------------X
