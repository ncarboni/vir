
{{TOC}}

## Introduction

This document presents an extension of CIDOC-CRM to support propositions about visual items. With the term visual items we refers to those signs identified in the visual space as distinct and documentable units, and subject of a status assignment by a group or a single person. 
Goal of this model is to provide a framework for specifying, as the interpretation of an actor, the identity and the relation of those signs, providing the necessary classes to sustain propositions about their constituent elements, reference, symbolic content and source.
The overall model is based on a constructivist approach, which differentiates between the reality identified, and the interpretation given to its visual structure by a person. This distinction allows us to present the gestalt of an item as a first layer of meaning in the identification of visual features. The assignment, by an actor, of one (or multiple) particular identity/ies to a representation is the second level of meaning. The model takes into account that the recognition of a representation is based on the attributes linked to it by a certain tradition.
Moreover, the model clearly separates the identity of the object and its subject matter which, as each construct which is culturally linked, can vary between different systems. For such reason, while providing the means for expressing the relationships between a representation and its subject matter, the ontology does not offer any subject-based classification, but rely on the ones already present and accepted by the art historical community, such as iconclass, the thésaurus iconographique of Garnier and others. 


### Naming

All the classes declared were given both a name and an identifier constructed according to the conventions used in the CIDOC CRM model.
For the classes, the identifier consists of the two letters IC followed by a number. Resulting properties were also given a name and an identifier: the letter K followed by a number. Inverse properties share the same identifier, the letter K followed by a number, plus the character “i” (inverse). every time the property is mentioned “backwards”, i.e., from target to domain (inverse link). 

## Examples

In this section we are going to present diverse examples of the possible use for the model in identifying iconographical objects, attributes and personification, as well as linking a particular text to a visual representation or specifying its visual prototype.


/NEW_symbolic.png  

*<small>Fig 1 — Mapping of the information about the visual recognition of the panel of Anastasia and Anastasia in Asinou, Cyprus</small>*  

The example uses a specific wall painting present in the narthex of the Asinou Church. The panel is identified and described throughout a [IC12 Visual Recognition], which defined a specific portion of the wall as the [IC1 Iconographical Atom] carrying carrying two [IC9 Representation]s, Anastasia Samaralina and St. Anastasia.  
The [IC12 Visual Recognition] is defined as an interpretation over a physical portion of the reality which classify it with the assignment of a specific meaning, in this case the two representations. The granularity of the recognition is, however, defined by the researchers, and the same [IC1 Iconographical Atom] can carry single or multiple representations depending on the interpretative action that has being carried out.


/san_george_itatti.png

*<small>Fig 2 — Mapping of the information about the St. George wall painting in Asinou, Cyprus</small>*

The figure above present show the mapping of the [IC10 Attribute]s and [IC16 Character]s depicted in a [IC9 Representation]. The identified figure of "St. George killing the dragon" is recognised to have six attributes (castle, horses, lakes, spears, princess, dragon) and to portray the figure of Saint George. The number of attributes of a representation changes depending on the time and context of production, and no fixed amount is here intended.

/asinou_personification.png

*<small>Fig 3 — Mapping of the information about a Personification</small>*

Figure 3 presents the mapping of the information about the depiction of a specific character, a [IC11 Personification], which is a human, or anthropomorphic figure, that represents an abstract idea or a concept.

/prototype.png

*<small>Fig 4 — Mapping of the information about a prototype</small>*

This last example presents the mapping of the information about the prototype of a representation. In this case, the "Allegory of the Immaculate Conception" by Vasari is linked with a drawing previously made by the author and used as a preparatory sketch. The possibility to define the type of prototype is given using K4.1 has type, which allow to specify further information such as "after" as in this case, or "preparatory sketch" and others. 

## Classes


### IC1 Iconographical Atom

Subclass of: **E25 Man-Made Feature**

An iconographical atom is a physical arrangement of forms/colours created by human activity

#### Proprieties

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

#### Proprieties:

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

#### Proprieties:

+ [K17 is attribute of (has attribute)](#k17): [IC9 Representation]
+ [K21 depict things of type (is depiction of attribute)]: E55 Type
+ [K14 symbolize (has symbolic value)]: E90 Symbolic Object
+ [K15 has been used by (use feature)](#k15): E12 Production

### IC11 Personification

Subclass of: **IC16 Character**

A human, or anthropomorphic figure, that represents an abstract idea or a concept.

**Example:**

	- Marianne in "La Liberté guidant le people" of Delacroix.

#### Proprieties:

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

#### Proprieties:
+ [K9 assigned status to (has status assigned by)]: E18 Physical Thing
+ [K11 assigned (was assigned by)]: [IC9 Representation]
+ [K10 on the base of (is basis for)]: E89 Propositional Object

### IC16 Character

Subclass of: **F38 Character**

This class comprises fictional individuals, or groups, appearing in a
representation. Each character portrayed can have a type, for example "Saint" or "layman". Every saint portrayed is considered here as a character and not as an actor.

**Example**:

	- St. Anastasia in the Panel "Anastasia & Anastasia" in Asinou.

#### Proprieties:

+ [K26 has source (is source of)]: E39 Actor
+ [K24 is portrayed in (portray)](#k24): [IC9 Representation]

### IC19 Recto

Subclass of: **E19 Physical Feature**

The front or face of a single sheet or the right-hand page of an open book. The feature is presents in object such as codex, books, pamphlets, documents, photographs and painting.

**Example**:

	- The recto of the drawing 57 E r "Busto di giovane donna di profile" by Raphael, preserved in the Department of Prints and Drawings, Uffizi.
	- The recto of the photograph of St. John the Baptist by Vicino da Ferrara

#### Proprieties:

+ [K6 has back (has front)](#k6): [IC20 Verso]
+ [K7 is recto of (has recto)]: E22 Man-Made Object

### IC20 Verso

Subclass of: **E19 Physical Feature**

The back or underside of a single sheet of paper, or the left-hand page of an open book. The feature is presents in object such as codex, books, pamphlets, documents, photographs and painting.

**Example**:

	- The verso of the drawing 57 E v "Testa di donna di profile" by Anonymous XVI century, preserved in the Department of Prints and Drawings, Uffizi
	- The photographer's stamp in the verso of the photograph of St. John the Baptist by Vicino da Ferrara

#### Proprieties:

+ [K6 has front (has back)](#k6): [IC19 Recto]
+ [K8 is verso of (has verso)]: E22 Man-Made Object

## Properties

#### K1 Denotes (is denoted by)

Domain: E18 Physical Thing  
Range: E36 Visual Item  
Subproperty: P65 show visual items  

The property documents the assignment of an iconographical object to a specific physical man-made object. It is a shortcut for the more fully developed path IC12 Visual Recognition assign (K9) to a E18 Physical Thing the status of (K11) IC9 Representation.

#### K4 is visual prototype of (has visual prototype)

Domain: [IC9 Representation]  
Range: [IC9 Representation]  
Subproperty: P67 refers to  

The property documents the use of a specific prototypical example for an image. The nature of the relationships helps define a map of relationships between prototypical items used in the arts.

#### K4.1 prototypical mode

Domain: [K4 is visual prototype of (has visual prototype)]  
Range: E55 Type  
<a name="k6">
#### K6 has back (has front)</a>

Domain: [IC19 Recto]  
Range: [IC20 Verso]  
Subproperty: P46 is composed of

The property documents the presence of a Verso or a Recto, respectively in the back or in the front of an object.

#### K7 is recto of (has recto)

Domain: [IC19 Recto]  
Range: E22 Man-Made Object  
Subproperty: P46 is composed of  

The property indicates the presence of a recto in the described object.

#### K8 is verso of (has verso)

Domain: [IC20 Verso]  
Range: E22 Man-Made Object   
Subproperty: P56 bears feature  

The property indicates the presence of a verso in the described object.

#### K9 Assigned status to (has status assigned by)

Domain: [IC12 Visual Recognition] 
Range: E18 Physical Thing   
Subproperty: P140 assigned attribute to (was attributed by)  

The property documents the assignment of status to a specific physical
thing.

#### K10 On the base of (is basis for)

Domain: E7 Activity  
Range: E89 Propositional Object   
Subproperty: P16 used specific object (was used for)  

The property describes the source used for the status assignment.

#### K11 Assigned (was assigned by)

Domain: [IC12 Visual Recognition] 
Range: [IC9 Representation]   
Subproperty: P141 assigned attribute to  

The property indicates the status assigned during the status assignment
event.

#### K14 symbolize (has symbolic value)

Domain: [IC10 Attribute]  
Range: E90 Symbolic Object   
Subproperty: P138 Represents   

The property indicates the symbolic value of the attribute presents in a representation.
<a name="k15">
#### K15 use features (has been used by)</a>

Domain: E12 Production   
Range: [IC10 Attribute]   
Subproperty: P33 used specific technique   

The property indicates the specific attribute used during the production of a visual object
<a name="k17">
#### K17 has attribute (is attribute of)</a>

Domain: [IC9 Representation]   
Range: [IC10 Attribute]   
Subproperty: P106 is composed of (forms part of)   

This property associates an attribute with the representation where it is depicted.

#### K20 is composed of (forms part of)

Domain: [IC9 Representation]  
Range: [IC9 Representation]   
Subproperty: P148 has component (is component of)  

This property put in relation an iconographical object with a part of itself.

#### K21 depict things of type (is depiction of attribute)

Domain: [IC10 Attribute]  
Range: E55 Type   
Subproperty: P137 exemplifies (is exemplified by)  

This property indicates the type of object depicted by an iconographical attribute.

#### K22 has personification (is present in)

Domain: [IC9 Representation]  
Range: [IC11 Personification]   
Subproperty: P138 Represents   

This property indicates the membership of a personification in an iconographical object.

#### K23 Connote (is connotation of)

Domain: [IC9 Representation]    
Range: [IC9 Representation]    
Subproperty: P138 Represents   

This property indicates the connotation relationships, formalized by Barthes, between a conceptual entity and an iconographical object. It is a shortcut for the more fully developed path IC12 Visual Recognition assign (K9) to a IC9 Representation a new (K11) IC9 Representation. It
doesn't offer any information about when and whom established the connotation relationship.
<a name="k24">
#### K24 Portray (is portrayed in)</a>

Domain: [IC9 Representation]  
Range: [IC16 Character]  
Subproperty: P138 Represents  

This property put in relation an iconographical object with the
portrayed character.

#### K25 express (is abstraction of)

Domain: [IC11 Personification]  
Range: E90 Symbolic Object   
Subproperty: P138 Represents   

This property put in relation a symbolic object with a personification in a work of art.

#### K26 Has source (is source of)

Domain: [IC16 Character] 
Range: E39 Actor   
Shortcut: E57 is based on   

This property associates an instance of IC16 Character with an instance of E39 Actor that the character is motivated by or is intended to represent.

#### K34 Illustrate (is illustrated by)

Domain: [IC9 Representation]  
Range: E73 Information Object   
Subproperty: P67 Refers to  

This property associates an information object to a iconographical representation.