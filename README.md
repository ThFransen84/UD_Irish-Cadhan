# Summary

This is the Cadhan Aonair UD treebank, consisting of 
150 sentences randomly sampled from six pre-standard Irish texts.
It was subsequently augmented with a late Early Modern Irish syllabic poem 
representing 43 sentences, described in a
[separate section below](https://github.com/UniversalDependencies/UD_Irish-Cadhan#bardic-segment).

# Introduction

Irish underwent a major spelling standardization in the 1940’s and 1950’s,
and as a result it can be challenging to apply modern language technologies
to older, “pre-standard” texts.
For many years now, the general strategy for tagging and parsing
older Irish texts has been to pre-process them with an automatic
standardizer (Scannell, 2014), and to then use existing tools designed for 
the modern language. This approach has been successful, but has some
inherent limitations. First and foremost, since there are no resources
for directly tagging or parsing pre-standard texts, the standardizer must
do its job without the benefit of linguistic annotations.
This places an upper bound on the performance of the standardizer,
and therefore on the full pipeline for analyzing older texts.
In addition, there are certain grammatical phenomena that have all
but disappeared in the modern language (e.g. the dative case);
these cannot be properly handled with the existing approach.

Our primary aim in creating this treebank was to establish a test set for
evaluating lemmatization, tagging, and parsing of pre-standard Irish texts.
This should enable experimentation with various approaches
that we hope will eventually outperform the existing pipeline.
Although the test set is quite small (150 sentences, 3804 tokens), 
we hope to expand it enough to allow the training of a
parser designed to act directly on pre-standard texts. 

The corpus contains 25 sentences each from six different books
published between 1602 and 1936.
Texts published in the late 19th century and early 20th century
are much easier to process than older texts.  The orthography,
while quite different from the standard, is much more consistent
than what one finds in texts published before the 1880s. 
We selected three books
published in this later period, one
from each of the major Irish dialects: _Deoraidheacht_ by
Pádraic Ó Conaire (1910, Connacht Irish),
_Peig_ by Peig Sayers (1936, Munster Irish),
and _Scairt an Dúthchais_, a translation
of Jack London’s Call of the Wild by Niall Ó Domhnaill (1932, Ulster Irish).
We then selected three older (and consequently more challenging) texts
to round out the corpus: _Foras Feasa ar Éirinn_
by Seathrún Céitinn (1634), the 1602 translation of the
Gospel of John by Uilliam Ó Domhnaill,
and _Cín Lae Amhlaoibh_, a diary kept by Amhlaoibh Ó
Súilleabháin between 1827 and 1835.

The annotations were produced by standardizing the texts,
parsing them with a UDPipe model trained on the 
[modern Irish treebank](https://github.com/UniversalDependencies/UD_Irish-IDT),
projecting the annotations back to the source texts, and then
manually correcting the results. Full details are available
in Scannell (2022).

# Bardic segment

A late Early Modern Irish syllabic (“bardic”) poem entitled
<em>Mo mhallacht ort, a shaoghail</em> (“My curse on you, world”, c. 1655)
was subsequently added to the Cadhan Aonair pre-standard treebank, also
using the pipeline described in Scannell (2022).
The text consists of 1004 tokens and was converted to a UD treebank by
Dr Theodorus Fransen as part of a [CLS INFRA](https://clsinfra.io/)
TNA fellowship at ÚFAL,
Charles University, Prague (CZ), between September and December 2022. 
The version of the poem contained in the treebank is based on a
lightly edited transcription available at 
https://bardic.celt.dias.ie/displayPoem.php?firstLineID=1387. 
Each of the 42 quatrains corresponds to one sentence (with the prefixed identifier `bardic_1387-`), 
with sentence 43 representing _closure_ (a repetition of (part of) the first line of the poem).
It was found that splitting up the poem into smaller units resulted in too fragmented sentences. 
More information can be found at https://github.com/ThFransen84/UD_Irish-Bardic.

# Acknowledgments

* Thanks to Teresa Lynn for her many years of work on the Irish treebank,
without which none of this research would be possible.
* Thanks to my undergraduate students Sai Shreyas Bhavanasi and Jianjun Zhang at Saint Louis University for many discussions that helped me understand the mathematics behind cross-lingual word embeddings more deeply.
* This project arose out of conversations with Charlie Dillon at the
Royal Irish Academy in early 2020 just before the COVID pandemic;
my thanks to Charlie and the RIA for hosting me during that visit,
and for inspiring this line of research.

## References

* Scannell, Kevin P. (2014) [_Statistical models for text normalization and machine translation_](https://cs.slu.edu/~scannell/pub/coling14.pdf), Proceedings of the 1st Celtic Language Technology Workshop at COLING 2014, Baile Átha Cliath, 23 August 2014.
* Scannell, Kevin P. (2022) [_Diachronic Parsing of Pre-Standard Irish_](https://cs.slu.edu/~scannell/pub/dppsi.pdf), Proceedings of the 4th Celtic Language Technology Workshop (CLTW 2022) at LREC 2022, Marseille, France, 20 June 2022.


# Changelog

* 2022-11-15 v2.11
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.11
License: CC BY-SA 4.0
Includes text: yes
Genre: fiction nonfiction bible
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Scannell, Kevin
Contributing: here
Contact: kscanne@gmail.com
===============================================================================
</pre>
