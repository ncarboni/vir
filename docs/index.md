
## Abstract
This document presents VIR (VIsual Representation), an RDFS extension of CIDOC-CRM to support propositions about visual items.  
<p><strong>Namespace:</strong> The namespace for VIR terms is <span class="repeated" style="font-family: courier;">
        http://w3id.org/vir#</span> </p> 
<p><strong>Prefix:</strong> The suggested prefix for VIR is <span class="repeated" style="font-family: courier;">
        bot</span> </p>
<p><strong>RDFS:</strong> an RDFS version of the ontology is available on <a href="https://github.com/ncarboni/vir/blob/master/vir.rdfs.xml">github</a></p>

## Table of Content

{{TOC}}

## Introduction

This document presents VIR, an extension of CIDOC-CRM created to sustain propositions on the nature of visual elements and permit these descriptions to be published on the Web. 
With the term visual element, we refer to those signs identified in the visual space as distinct and documentable units, and subject to an analytical interpretation. 
The scope of this ontology is to s to provide a framework to support the identification, annotation and interconnections between diverse visual elements and presents and assist their documentation and retrieval. Specifically, the model aims to clarify the identity and the relation of these visual signs, providing the necessary classes to characterise their constituent elements, reference, symbolic content and source of interpretation.

VIR expands on key entities and properties from CIDOC-CRM, introducing new classes and relationships responding to the visual and art historical community, specifically building up on the iconographical tradition. The result is a model which differentiates between interpretation and element identified, providing a clear distinction between denotation and signification of an element. As a consequence of such distinction, the ontology allows for the definition of diverse denotative criteria for the same representation, which could change based on traditions and perspective. Visual objects can be, in fact, polysemic and ambiguous, and it is not so easy to pin down a denotative or connotative meaning because they are very much context-dependent.

/img/khmer_filonzana.png

<center>**Figure 1**</center>
<br/>
The two figures above are clear examples. The first one is a column made in order to resemble an elephant, while the second one is the mask of the Filonzana, a typical figure in the carnival of Ottana, in Sardinia, Italy.
While the column shows us the capacity for a "simple" element to denote something else, the mask is clearly a polysemic image which could be interpreted only if we do know how it is being used. Its analysis would, in fact, reveal the interconnections between the depicted character and the Parcae, the Moirai or the Fates in other cultures. Its representation, however, it is plain and only who has knowledge of the rite would be able to characterise its meaning, therefore the act of interpretation it is implicit in its recognition and assignment of status.

For such reasons, the model clearly separates the identity of the object and its subject matter. Moreover, while providing the means for expressing the relationships between a representation and its subject(s) (the process), the ontology does not provide any type of subject-based classification, but rely on the ones already present and widely accepted by the art historical community, such as [Iconclass](http://www.iconclass.org/help/lod), the [Warburg Classification](https://warburg.libguides.com/classification) or the Thesaurus Iconographique by Garnier.  

The core of the ontology has been developed working with two very different projects, the documentation of the Panagia Phorbiotissa church in Cyprus and the mapping of the Berenson photo archive of the Harvard University Center for Italian Renaissance Studies. The analysis of two different visual traditions, Byzantine and Western Art, has helped the development of shared characterisation of the classes and properties which, at the time of writing, covers use cases coming from both a research and a classificatory perspective.
 


### Naming

All the classes declared were given both a name and an identifier constructed according to the conventions used in the CIDOC CRM model.
For the classes, the identifier consists of the two letters IC followed by a number. Resulting properties were also given a name and an identifier: the letter K followed by a number. 
They correspond respectively to letters “E” and “P” in the CIDOC CRM naming conventions, where “E” originally meant “entity” (although the CIDOC CRM “entities” are now consistently called “classes”), and “P” means “property”.
Inverse properties share the same identifier, the letter K followed by the same number, plus the character "i" (inverse).

## Graphical Overview
<br/>
/img/vir.svg
<br/>
<center><small>Figure 2 — Graphical Overview of the classes and properties of VIR</small></center>

## Class and property usage examples

In this section, we present different examples in order to illustrate how VIR can be used to encode information about diverse visual items. In order to make clear the potential of the ontology, we will use diverse representations of St. George, a culturally widespread subject. 

### Statue

The first example is a simple one, the modelling of the [statue of St George slaying the dragon](https://commons.wikimedia.org/wiki/File:Statue_of_St_George_in_Berlin.JPG)  in Berlin. Having already presented in the [Graphical Overview] the prefix used, for readability purpose we will omit this information in the next examples.  
<br/> 
/img/st_george_berlin.svg   
<br/> 
<center><small>Figure 3</small></center>  

The mapping in Figure 2 presents an overview of the classification of a statue through a (IC12) Visual Recognition event. The classification is purely visual and assign a representation to an object, defining the (IC10) features and (IC16) character it portrays. The classificatory act help us track the provenance of the statements, differentiating diverse recognitions carried out by different agents, which do not share the same knowledge of the classified object. 

### Painted flask

The second example is about the information of a beautiful [ceramic Flask](http://id.lib.harvard.edu/images/olvwork245986/urn-3:FHCL:426930/catalog) coming from Ottoman Turkey.

<br/>
/img/flask.svg
<br/>
<center><small>Figure 4</small></center>  

The flask presents two sides, with two different representations, a standing woman and the depiction of St. George on horseback. Both representations appear in the mapping but slightly differently. For the saint, it has been used the modelling proposed in Figure 3 the statue in Berlin, but only two attributes have been recognised in this case, the horse and the spear. The other representation has been described using the property Denote, a shortcut of the full path IC12 Visual Recognition assign (K9) to a E18 Physical Thing the status of (K11) IC9 Representation. In this examples, the statue of Saint George has been classified in relation to two of its Attribute (IC10), which are modelled using a controlled vocabulary. It is important to state that the type here does not identify the attribute depicted but its iconographical type. 

### Photo Archive

The third example is about the photograph of the work of art ["St. George killing the dragon"](https://commons.wikimedia.org/wiki/File:Vittore_carpaccio,_san_giorgio_e_il_drago_01.jpg) by Vittore Carpaccio. The aim of this example it is not to map the information about the original work of art, or the origin of the photo, but only on the iconographical attribution and representation. The mapping is a bit more complicated than the one above, therefore it appears divided into two parts, **a** and **b**. Part **a** presents a mapping of the information about the attribution of the artwork.

<br/>
/img/carpaccio_note.svg
<br/>
<center><small>Figure 5a</small></center>  

The mapping describes two events, the recognition of the representation in the recto and, consequently, the inscription in the Verso of the photograph of the note "With (but not) Carpaccio". The recto and verso of a photograph is described using two VIR classes which, in respect to the classic physical features, allows for clearly stating the front/back relation between the two.
The inscription is described as a (E12) production event, which results in the engraving of a set of sign in the verso, which carries a (E33) linguistic object. 

<br/>
/img/carpaccio.svg
<br/>
<center><small>Figure 5b</small></center>  

The figure 5b above does complete the information in figure 5a, describing the visual information present in the photo. Several attributes were identified in this representation (dragons, princesses, lakes, vessels, castle), and two of them defined as symbolic. The dragon symbolizes the lust, while the castle the city of Silene in Libya, the place where, in the [Golden Legend](https://en.wikipedia.org/wiki/Saint_George_and_the_Dragon#Golden_Legend), St. George killed the dragon. 

### Preparatory sketches

Representation, sometimes at least, have to be seen as the result of a long process which involves preliminary studies and sketches of what, in the end, would be the final version of an artwork. This fourth example presents the mapping of the information about a preparatory [sketch](https://commons.wikimedia.org/wiki/File:Vittore_carpaccio,_san_giorgio_e_il_drago,_disegno_uffizi.jpg) and the [final version](https://it.wikipedia.org/wiki/File:Vittore_carpaccio,_trionfo_di_san_giorgio_01.jpg) of an artwork using the example of the Triumph of St. George by Vittore Carpaccio. 

<br/>
/img/prototype.svg
<br/>
<center><small>Figure 6</small></center>

The mapping in figure 6 clearly present the relationship between the preparatory sketch and the final version, establishing not only a relation, K4 has visual prototype, between the two, but a relationship type. The aim of this property is to relate artwork with their derivations whatever their type. A copy is to be interpreted as using the original as its prototype, as much as an artwork use the drawing as its original form. For such reason, all the diverse type of prototypical form can be modelled using the K4.1 property and a type.

### Diverse representations

Other cases where VIR can be extremely useful would include the description of similar iconographical types which differ in attributes/features, such as episodes having the same character but diverse denotative meaning (diverse episodes of the saint life), or similar attributes over very much diverse representations (St George killing a Dragon and St. Micheal killing a dragon). The examples are numerous and the time limited, but if some help is required the [issue section in the github repository of VIR](https://github.com/ncarboni/vir/issues) would be the best place to ask.



## Classes


### IC1 Iconographical Atom

Subclass of: **E25 Man-Made Feature**

An iconographical atom is a physical arrangement of forms/colours created by human activity

##### Proprieties

+ [K1 denotes (is denoted by)]: E36 Visual Item

### IC9 Representation

Subclass of: **E36 Visual Item**

The nuclear characteristics which are recognised to belong to the same
type

**Example:**

- The painting "La primavera" in Botticelli  
- The last judgment wall painting in Asinou  
- The impresa of Bernardo Cles in the Buonconsiglio castle in Trento  
- The Maria Maddalena statue by Donatello  
- The Bayeux Tapestry  

##### Proprieties:

+ [K20 is composed of (forms part of)]: [IC9 Representation] 
+ [K22 has personification (is present in)]: [IC11 Personification]
+ [K23 connote (is connotation of)]: [IC9 Representation]
+ [K17 has attribute (is attribute of)](#k17): [IC10 Attribute]
+ [K24 portray (is portrayed in)](#k24): [IC16 Character]
+ [K34 illustrate (is illustrated by)]: E73 Information Object
+ [K4 is visual prototype of (has visual prototype)]: [IC9 Representation]

### IC10 Attribute

Subclass of: **E36 Visual Item**

**E29 Design or Procedure**

A set of features considered by a viewer more salient than others and used as a key for the identification of a Representation. The attribute could correspond to iconographical elements or simple signs which the viewer uses to provide a stable identity to a visual object.

**Example:**

- The cross in the Anastasia Samaralina painting in Asinou that symbolize the Martyrdom.
- The dragon in "Saint George and the Dragon" by Tintoretto.

##### Proprieties:

+ [K17 is attribute of (has attribute)](#k17): [IC9 Representation]
+ [K21 depict things of type (is depiction of attribute)]: E55 Type
+ [K14 symbolize (has symbolic value)]: E1 CRM Entity
+ [K15 has been used by (use feature)](#k15): E12 Production

### IC11 Personification

Subclass of: **IC16 Character**

A human, or anthropomorphic figure, that represents an abstract idea or a concept.

**Example:**

- Marianne in "La Liberté guidant le people" of Delacroix.

##### Proprieties:

+ [K25 express (is abstraction of)]: E90 Symbolic Object

### IC12 Visual Recognition

Subclass of: **S4 Observation**

The activity of assigning the iconographical status to a man-made
object, or to one of its parts. It takes into account the possibility to
link it to a speech act or a document where the authoritative
proposition is clearly made.

**Example**:

- An expert saying that object A is a IC9 Representation
- The recognition that a simple drawing represents a type of animal

##### Proprieties:
+ [K9 assigned status to (has status assigned by)]: E18 Physical Thing
+ [K11 assigned (was assigned by)]: [IC9 Representation]
+ [K10 on the base of (is basis for)]: E89 Propositional Object

### IC16 Character

Subclass of: **F38 Character**

This class comprises fictional individuals, or groups, appearing in a
representation. Each character portrayed can have a type, for example "Saint" or "layman". Every saint portrayed is considered here as a character and not as an actor.

**Example**:

- St. Anastasia in the Panel "Anastasia & Anastasia" in Asinou.

##### Proprieties:

+ [K26 has source (is source of)]: E39 Actor
+ [K24 is portrayed in (portray)](#k24): [IC9 Representation]

### IC19 Recto

Subclass of: **E19 Physical Feature**

The front or face of a single sheet or the right-hand page of an open book. The feature is presents in object such as codex, books, pamphlets, documents, photographs and painting.

**Example**:

- The recto of the drawing 57 E r "Busto di giovane donna di profile" by Raphael, preserved in the Department of Prints and Drawings, Uffizi.
- The recto of the photograph of St. John the Baptist by Vicino da Ferrara

##### Proprieties:

+ [K6 has back (has front)](#k6): [IC20 Verso]
+ [K7 is recto of (has recto)]: E22 Man-Made Object

### IC20 Verso

Subclass of: **E19 Physical Feature**

The back or underside of a single sheet of paper, or the left-hand page of an open book. The feature is presents in object such as codex, books, pamphlets, documents, photographs and painting.

**Example**:

- The verso of the drawing 57 E v "Testa di donna di profile" by Anonymous XVI century, preserved in the Department of Prints and Drawings, Uffizi
- The photographer's stamp in the verso of the photograph of St. John the Baptist by Vicino da Ferrara

##### Proprieties:

+ [K6 has front (has back)](#k6): [IC19 Recto]
+ [K8 is verso of (has verso)]: E22 Man-Made Object

## Properties

### K1 denotes (is denoted by)

Domain: E18 Physical Thing  
Range: E36 Visual Item  
Subproperty: P65 show visual items  

The property documents the assignment of an iconographical object to a specific physical man-made object. It is a shortcut for the more fully developed path IC12 Visual Recognition assign (K9) to a E18 Physical Thing the status of (K11) IC9 Representation.

### K4 is visual prototype of (has visual prototype)

Domain: [IC9 Representation]  
Range: [IC9 Representation]  
Subproperty: P67 refers to  

The property documents the use of a specific prototypical example for an image. The nature of the relationships helps define a map of relationships between prototypical items used in the arts.

### K4.1 prototypical mode

Domain: [K4 is visual prototype of (has visual prototype)]  
Range: E55 Type  
<a name="k6">
### K6 has back (has front)</a>

Domain: [IC19 Recto]  
Range: [IC20 Verso]  
Subproperty: P46 is composed of

The property documents the presence of a Verso or a Recto, respectively in the back or in the front of an object.

### K7 is recto of (has recto)

Domain: [IC19 Recto]  
Range: E22 Man-Made Object  
Subproperty: P46 is composed of  

The property indicates the presence of a recto in the described object.

### K8 is verso of (has verso)

Domain: [IC20 Verso]  
Range: E22 Man-Made Object   
Subproperty: P56 bears feature  

The property indicates the presence of a verso in the described object.

### K9 assigned status to (has status assigned by)

Domain: [IC12 Visual Recognition] 
Range: E18 Physical Thing   
Subproperty: P140 assigned attribute to (was attributed by)  

The property documents the assignment of status to a specific physical
thing.

### K10 on the base of (is basis for)

Domain: E7 Activity  
Range: E89 Propositional Object   
Subproperty: P16 used specific object (was used for)  

The property describes the source used for the status assignment.

### K11 assigned (was assigned by)

Domain: [IC12 Visual Recognition] 
Range: [IC9 Representation]   
Subproperty: P141 assigned attribute to  

The property indicates the status assigned during the status assignment
event.

### K14 symbolize (has symbolic value)

Domain: [IC10 Attribute]  
Range: E1 CRM Entity   
Subproperty: P138 Represents   

The property indicates the symbolic value of the attribute presents in a representation.
<a name="k15">
### K15 use features (has been used by)</a>

Domain: E12 Production   
Range: [IC10 Attribute]   
Subproperty: P33 used specific technique   

The property indicates the specific attribute used during the production of a visual object
<a name="k17">
### K17 has attribute (is attribute of)</a>

Domain: [IC9 Representation]   
Range: [IC10 Attribute]   
Subproperty: P106 is composed of (forms part of)   

This property associates an attribute with the representation where it is depicted.

### K20 is composed of (forms part of)

Domain: [IC9 Representation]  
Range: [IC9 Representation]   
Subproperty: P148 has component (is component of)  

This property put in relation an iconographical object with a part of itself.

### K21 depict things of type (is depiction of attribute)

Domain: [IC10 Attribute]  
Range: E55 Type   
Subproperty: P137 exemplifies (is exemplified by)  

This property indicates the type of object depicted by an iconographical attribute.

### K22 has personification (is present in)

Domain: [IC9 Representation]  
Range: [IC11 Personification]   
Subproperty: P138 Represents   

This property indicates the membership of a personification in an iconographical object.

### K23 connote (is connotation of)

Domain: [IC9 Representation]    
Range: [IC9 Representation]    
Subproperty: P138 Represents   

This property indicates the connotation relationships, formalized by Barthes, between a conceptual entity and an iconographical object. It is a shortcut for the more fully developed path IC12 Visual Recognition assign (K9) to a IC9 Representation a new (K11) IC9 Representation. It doesn't offer any information about when and whom established the connotation relationship.
<a name="k24">
### K24 portray (is portrayed in)</a>

Domain: [IC9 Representation]  
Range: [IC16 Character]  
Subproperty: P138 Represents  

This property put in relation an iconographical object with the portrayed character.

### K25 express (is abstraction of)

Domain: [IC11 Personification]  
Range: E90 Symbolic Object   
Subproperty: P138 Represents   

This property put in relation a symbolic object with a personification in a work of art.

### K26 has source (is source of)

Domain: [IC16 Character] 
Range: E39 Actor   
Shortcut: E57 is based on   

This property associates an instance of IC16 Character with an instance of E39 Actor that the character is motivated by or is intended to represent.

### K34 illustrate (is illustrated by)

Domain: [IC9 Representation]  
Range: E73 Information Object   
Subproperty: P67 Refers to  

This property associates an information object to a iconographical representation.