# LiC

This is the working space for Literature in Context, an XML project that seeks to provide open-access, reliably-sourced, and collaboratively-constructed annotated editions of British and American literature of the long 18th century for classroom use. This project is funded by the National Endowment for the Humanities and developed by faculty at The University of Virginia and Marymount University.

## Platform

### Manifold 
Manifold is great for straightforward group annotate-able stand-alone texts, and the “collections” feature might be useful for us. However, out of the box it doesn’t allow: 
- page images (at least, from the html or xml; see the Frankenstein TP as an example. The [page] link that ought to work in the HTML doesn’t, and the added resource was just that--added)
- selecting-->coursepacks/anthologies
- working directly from/with the TEI files. (The Frankenstein text is created from the HTML that Oxygen created when I transformed from XML)

These three things seem to be really important for us, and I’m not sure we want to give up these goals. On the other hand, Manifold offers a beautiful reading interface, crowdsourced annotations, and the possibility of building the reading text online. 

Can Performant hack Manifold or create plugins to allow us to do what we want to do? If not, it really seems that an XML database is a good way to go, because it is made to work directly with the TEI files. There is little of the “middleman” here, outside of hiring someone to create an XSL that works for us. What we lose here is the group annotation feature. 

### eXist-db
Currently, we are working on an eXist install with github connectivity. Texts to work with:
- behn-oroonoko.xml
- behn-rover.xml
- wheatley-poems.xml
- shelley-frankenstein.xml
- finch-nightingale.xml

## Naming conventions
We need to rename all our files to the standard lastname-shorttitle.xml format. This should also be the xml:id of the file, noted in the TEI header.

## Core TEI
What will our core TEI look like, for prose, poetry, drama? We’ve agreed on TEI level-4 for libraries, but there is still a lot of variation there. Some issues:

### Creation
How we create or come by the TEI will have an important role to play . For instance, the xml files from 18th Connect use <ab> (anonymous blocks) for every line of the text. The American Verse Project out of UM looks different. Here are some samples:

+ Finch Miscellany Poems (1713), via 18th Connect: https://drive.google.com/open?id=1fAwGp4b2kxadR2ghjoo1knvWobF2-BEP

+ Wheatley’s Poems on Several Occasions (1773), via AVP: 
https://drive.google.com/open?id=1hjasZUmRem2SR_K_RaLW9JZwDgPNWiOV 

It would be nice (necessary?) to have a custom DTD, and make that available for project participants. I have generated one from Frankenstein and Finch’s poem “To the Nightingale,” but I don’t know if it is strictly valid. The TEI-lite schema doesn’t validate these files in Oxygen. Chris might know more about this!!

### TEI for annotations
Tonya's files use both XML and a plugin called tooltipster that produces popups in eXist-- see http://nic.cerosia.org/finch-nightingale or finch-nightingale.xml on github. 

### Problematic elements
+ person, persName, author
...

### TEI header
Standard TEI header should be in place now (8/1/18).  

## Material sources
How will we indicate the variety of sources from which this digital edition has been constructed? In most cases, there will be multiple witnesses/physical sources--a book, an 18th Connect text encountered via TypeWright, a Project Gutenberg plaintext, an XML or SGML file from another project, even a hard copy that was used for reading. Can we manipulate <sourcerDesc><imprint> element in the header? See above re: validity.

## Annotation content
What should a baseline be? How much variation will we allow? Complete sentences, attributive phrases, reputable sources both popular-scholarly and scholarly? Accessibility? Citation and quotation? Linking within the annotations? 

