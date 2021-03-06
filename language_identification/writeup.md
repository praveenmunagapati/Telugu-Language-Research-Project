## Overview
`telugu_lang_identifier.py` takes advantage of a very important concept: the telugu language is unique and shares no characters with other languages. Furthermore, the unicode representations of all unique characters exist in the same unicode block, or range, from 0C00–0C7F. This document by the UnicodeConstorium spells out the specifics: [U0C00 Chart](http://unicode.org/charts/PDF/U0C00.pdf). This block is dedicated solely to telugu so my script checks the numerical unicode value of each character from the input stream to determine the language.

    Officially, the language uses no latin characters but it is becoming more frequent to see punctuation integrated into informal writing. In order to handle this correctly, my script returns a probability [0.0 -> 1.0].

    I tested my script on english/french/german sentences, english words, telugu sentences, informal telugu (punctuation), and mixed telugu and english. The results indicated that this simple script was very effective at determining the likelyhood of the input containing telugu.
