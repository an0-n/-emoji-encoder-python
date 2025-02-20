# unicode disguise
A codec that can hide ciphertext under cover of disguise, so what you see may not be what you get.
The principle comes from [https://github.com/paulgb/emoji-encoder](https://github.com/paulgb/emoji-encoder)
This project implements its principle in Python, and adds interaction with the clipboard for ease of use.
# usage
Now you can copy any text to the clipboard and run
`python unicode_encoder.py -e`, the program will read the data in the clipboard, encode it, and write the result to the clipboard.
You can copy the encrypted text to the clipboard and then run
`python unicode_encoder.py -d`, the program will read the data in the clipboard, decode it, and write the result to the clipboard.
The default cover text (the text that is rendered after encoding for third parties to see) is '😀'. You can actually specify any cover text by using the -b parameter:
`python unicode_encoder.py -e -b abc`
You don't need to specify the cover text for decoding, the algorithm will automatically decode it
# environment
Platform: Windows
The pandas package is used to read and write the clipboard. If your Python environment does not have pandas, use pip install pandas to install it.
# more
If you think the ciphertext is not hidden enough, you may consider using RSA or other algorithms to encrypt in advance, and then use this encoder to disguise it. Like here ---> https://github.com/KuroLabs/stegcloak
