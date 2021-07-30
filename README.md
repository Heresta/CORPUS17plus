# TEI17

This repository contains layout analysis and OCR from 17<sup>th</sup> books in TEI files and their ODD.

## Production

Thoses files were created thanks to a pipeline :

1. Segmentation and transcription with [eScriptorium](http://traces6.paris.inria.fr/), using models from 
[datasetsOCRSegmenter17 github repository](https://github.com/Heresta/datasetsOCRSegmenter17/blob/Model)

2. Manual correction of ALTO4 files extracted from eScriptorium

3. Python script pipeline to transform those ALTO4 files in a unique TEI file ([see Extractor repository](https://github.com/Heresta/extractor))
, adding some metadata (extracted from manifest IIIF and SPARQL requests in [data.bnf.fr](http://data.bnf.fr)).

## How TEI file is built ?

This TEI file tries to stick at most to TEI all documentation.

So it contains :

1. `teiHeader` in which there is all metadata recovered with manifest IIIF and SPARQL request, some information about encoding (use of 
[SegmOnto vocabulary](http://github.com/SegmOnto), some information about book's printer(s)

2. `facsimile` in which is all layout informations about different zones, lines, and baselines, with pixels coordinates and links to 
IIIF images

3. `text` in which is all transcription, linked to the concerned line

## Credits

Documents have been encoded by Claire Jahan with the help of Simon Gabay, as part of the [_E-ditiones_](https://github.com/e-ditiones) project.

## Contact
Claire Jahan : claire.jahan[at]chartes.psl.eu

Simon Gabay : Simon.Gabay[at]unige.ch

## Licence

This repository is CC-BY.
<br/>
<a rel="license" href="https://creativecommons.org/licenses/by/2.0"><img alt="Creative Commons License" src="https://i.creativecommons.org/l/by/2.0/88x31.png" /></a>

## Cite this repository

Claire Jahan, Simon Gabay. 2021. _CORPUS17+ - Corpus of TEI encoded 17th French prints._, Paris/Geneva: ENS Paris/UniGE, 2021, https://github.com/Heresta/CORPUS17plus. 

