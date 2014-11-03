# British Library Labs Symposium 2014 #
*Dissemination Event, British Library Conference Centre. London*

## Monday, 3 November 2014 ##

### Keynote: Big Data, Small Data and Meaning: the conundrums of tool use in the humanities ###
Tim Hitchcock, Professor of Digital History, University of Sussex

#### Blurb ####
While 'big data' has grabbed the headlines in recent years, the creation of new digital tools has also changed how we undertake forms of 'close reading'. This talk will explore how 'big data' and 'close reading' can be more effectively integrated into a single research strategy that acknowledges the importance of seeing inherited culture both in detail - close up; and in context - at scale. It will also consider these methodological developments in light of the continuing importance of more traditional humanist theory.

#### Notes ####

[..in media res...]

+ We must remember the 'power of the particular' in macroscopic analyses
  + Big Data falls down when it fails to refocus
  + TH worries that we are losing our ability to see detail in a way that make Thompson et al so compellling. 

+ Humanities scholars should have self-confidence in their abilities
  + We can do certain things STEM scholars don't do very well
  + Close reading of a single datum
  + Big data supposedly let's you 'get away with dirty data'
  + We need tools to do a close reading of data that makes up big data
  
+ Radical contextualisation
  + Understand the history and usage of a word so we can recognise when it is used in a way that is new or would look odd to contemporary readers
  + "Where is the tool to do that? Where is the project?"

### The Text to Image Linking Tool - winner of the British Library Labs 2014 competition ###
Desmond Schmidt, Research Scientist and Anna Gerber, Technical Project Manager of the University of Queensland

#### Blurb ####
Historical printed and manuscript material is often difficult to read and understand. Once digitised, researchers create detailed transcriptions, but making links between page images and the transcribed text is difficult and time-consuming. Desmond and Anna have been developing semi-automated techniques to build these links, to verify them, and to capture information that goes beyond text to include differences in lineation, type-size and line-spacing.

#### Notes ####

Background to the problem
+ Why link text to images
  + Library contain thousands of literary and historical texts
  + People expect to be able to access them on their ipads!
+ Digitisation is an obvious first step
  +'Bilwidering' number of thumbnails
+ Can attach text to page image (on top)
  + OCR 
  + hard to fix errors
  + text can't be formatted / annotated
  + can search
+ Can put it side by side (page level)
  + Need to be synchronised
  + Lots of mental effort to move back and forth between formats / size / etc
+ Link at line level
  + Can't reflow
+ Word Level
  + Works even if hyphenated across lines

Manual Approach
+ Manually draw shapes around words
+ Link to text with mark up
+ Tedious, expensive
+ Markup too complex
+ Two transcriptions needed
  + One for links
  + One for formatting
  
Basic Idea of TILT
+ Find words in an image **without** recognising their content
+ Use and existing ransciption of the page ontent
+ Link these two compnents mostly automatically
+ GeoJSON overlay links to image and transcription but not part of either

Method
+ Colour to greyscale
+ to Black and White
+ Find lines (can handle curves and slants)
+ Find words shapes (blobs of connected pixels with small gaps between them)
  + If you have 300 words, are the 299 biggest gaps the spaces?
+ link word-shapes to text

*Please don't have black verticle lines when digitising text!*

+ update anchors whenever words get out of alignment 
+ last resort: manually draw polygon around words


### Victorian Meme Machine ###
Bob Nicholson, Lecturer, Edge Hill University

Bob will present the work he has been doing with Labs on the Victorian Meme Machine. What would it take to make a Victorian joke funny again? While the great works of Victorian art and literature have been preserved and celebrated by successive generations, even the period’s most popular jokes have now been lost or forgotten. Fortunately, thousands of these endangered jests have been preserved within the British Library’s digital collections. This project has begun to find these forgotten jokes and bring them back to life.

### Projects using British Library digital content and data ###

The British Library Labs have been working with researchers around the world to enable them to make use of the Library's digital content / data; the session highlights some examples.

### Palimpsest: an Edinburgh Literary Cityscape ###
Dr Beatrice Alex, Research Fellow in Text Mining, School of Informatics, University of Edinburgh 

We are creating a literary cityscape through text mining vivid, evocative and dramatic extracts of Edinburgh-based literary works from the early modern period to the twentieth century. Palimpsest enables users to explore the dimensions of literary Edinburgh through their encounters with geo-located extracts of literary works either via the web resource or in the city streets via a smartphone or tablet. The project is producing an interactive website and database of Edinburgh - based literary texts which is revealing a range of cityscapes that will newly engage scholars and the public with the urban environment and its literature.

### Digital Music Lab: Analysing Big Music Data ###
Daniel Wolff, Research Fellow for the Digital Music Lab project at the Music Informatics Research Group, City University London and Adam Tovell, Curator, Digital Music, British Library

The Digital Music Lab is developing research methods and software infrastructure for exploring and analysing large-scale music collections, and to provide researchers and users with datasets and computational tools to analyse music audio, scores and metadata. The team will present some of their initial findings including some startling visualisations.

### Measuring the value of public domain data ###
Peter Balman , Software Developer and Winner of the Technology Strategy Board and British Library's Innovation Challenge (IC Tomorrow) -The value of public-domain data.

Peter will talk about a tool he is developing that will proactively search for British Library's digital content on the web and give a detailed breakdown of where, how and by whom it is being used. Having visibility on this kind of data could help the BL make choices around targeting users by releasing similar content and encourage further use and deeper engagement within these groups.

### The surprising tale of the mechanical curator and 1 million images ###
Mahendra Mahey, Manager and Ben O'Steen, Technical Lead of the British Library Labs

The Labs team will tell the surprising story of one digital collection that the Library holds and how their work with it produced results no one expected, not even them! They will show how and - more importantly - why they created the ‘Mechanical Curator’ and uploaded over a million illustrations taken from books onto Flickr. These images have stirred great interest from artists, researchers and the general public, garnering 200 million views and over 100,000 descriptive tags in under a year. The team will provide some examples of the creative and academic work that the collection has inspired as well as showing the impact the release has had.


### What the Library has learned from the British Library Labs project and how it will be supporting Digital Scholars in the future ###
Adam Farquhar, Head of Digital Scholarship and Principal Investigator of the British Library Labs project

Adam will highlight key lessons that we’ve learned working closely with researchers since the Labs were formed and discuss how the Labs is transforming our approach to providing services to support digital research and scholarship. He will also outline plans for the Labs over the coming years and give further details of the 2015 Competition. 

### Sound making today and in the Victorian era ###
Sarah Angliss, composer, automatist and sound historian

Sarah explores some unlikely affinities between sound making today and in the Victorian era. This will include references to the phonograph, ventriloquism, the learned pig and recordings held at the British Library. She will be available during the final reception in the Chaucer room to talk about the technology behind her creations and will host a special drop in D.I.Y session where you will be able to record your own voice on a wax cylinder using an original Edison phonograph, and hear how this 19th century sound recording equipment changes the way you sound.

____
#### Nota Bene

***This work is licensed under a Creative Commons Attribution 3.0 Unported License.***

<a rel="license" href="http://creativecommons.org/licenses/by/3.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by/3.0/88x31.png" /></a>

***Taken Live and should not be considered a definative or complete record