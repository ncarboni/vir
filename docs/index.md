
{{TOC}}

  ------------------------ ------------ --------- --------- --------- ------------------- ------------------------- ------------------------ ------------------------- ---------------
  [E1]{.underline}         CRM Entity                                                                                                                                  
  [E7]{.underline}         \-           \-        \-        \-        Activity                                                                                         
  [E13]{.underline}        \-           \-        \-        \-        \-                  Attribute Assignment                                                         
  [E14]{.underline}        \-           \-        \-        \-        \-                  \-                        Condition Assessment                               
  [E15]{.underline}        \-           \-        \-        \-        \-                  \-                        Identifier Assignment                              
  [E16]{.underline}        \-           \-        \-        \-        \-                  \-                        Measurement                                        
  **IC12**                 **-**        **-**     **-**     **-**     **-**               **-**                     **Visual Recognition**                             
  [E17]{.underline}        \-           \-        \-        \-        \-                  \-                        Type Assignment                                    
  [E18]{.underline}        \-           \-        \-        \-        Physical Thing                                                                                   
  [E26]{.underline}        \-           \-        \-        \-        \-                  Physical Feature                                                             
  **[IC19]{.underline}**   **-**        **-**     **-**     **-**     **-**               **-**                     **Recto**                                          
  **[IC20]{.underline}**   **-**        **-**     **-**     **-**     **-**               **-**                     **Verso**                                          
  [E24]{.underline}        \-           \-        \-        \-        \-                  Physical Man-Made Thing                                                      
  [E22]{.underline}        \-           \-        \-        \-        \-                  \-                        Man-Made Object                                    
  [E25]{.underline}        \-           \-        \-        \-        \-                  \-                        Man-Made Feature                                   
  **IC1**                  **-**        **-**     **-**     **-**     **-**               **-**                     **-**                    **Iconographical Atom**   
  [E28]{.underline}        \-           \-        \-        \-        Conceptual Object                                                                                
  ***IC16***               ***-***      ***-***   ***-***   ***-***   ***-***             **Character**                                                                
  ***IC11***               ***-***      ***-***   ***-***   ***-***   ***-***             **-**                     **Personification**                                
  *[E90]{.underline}*      *-*          *-*       *-*       *-*       *-*                 Symbolic Object                                                              
  *[E73]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       Information Object                                 
  *[E27]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       *-*                      Design or Procedure       
  ***IC10***               ***-***      ***-***   ***-***   ***-***   ***-***             ***-***                   ***-***                  ***-***                   **Attribute**
  *[E31]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       *-*                      Document                  
  *[E33]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       *-*                      Linguistic Object         
  *[E36]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       *-*                      Visual item               
  ***IC9***                ***-***      ***-***   ***-***   ***-***   ***-***             ***-***                   ***-***                  **Representation**        
  ***IC10***               ***-***      ***-***   ***-***   ***-***   ***-***             ***-***                   ***-***                  **Attribute**             
  *[E38]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       *-*                      Image                     
  *[E41]{.underline}*      *-*          *-*       *-*       *-*       *-*                 *-*                       Appellation                                        
  [E89]{.underline}        \-           \-        \-        \-        \-                  Propositional Object                                                         
  [E55]{.underline}        \-           \-        \-        \-        \-                  Type                                                                         
  ------------------------ ------------ --------- --------- --------- ------------------- ------------------------- ------------------------ ------------------------- ---------------

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
+ [K17 has attribute (is attribute of)]: [IC10 Attribute]
+ [K24 portray (is portrayed in)]: [IC16 Character]
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

+ [K17 is attribute of (has attribute)]: [IC9 Representation]
+ [K21 depict things of type (is depiction of attribute)]: E55 Type
+ [K14 symbolize (has symbolic value)]: E90 Symbolic Object
+ [K15 has been used by (use feature)]: E12 Production

### IC11 Personification

Subclass of: **IC16 Character**

A human, or anthropomorphic figure, that represents an abstract idea or
a concept.

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
+ K24 is portrayed in (portray): [IC9 Representation]

### IC19 Recto

Subclass of: **E19 Physical Feature**

The front or face of a single sheet or the right-hand page of an open book. The feature is presents in object such as codex, books, pamphlets, documents, photographs and painting.

**Example**:

	- The recto of the drawing 57 E r "Busto di giovane donna di profile" by Raphael, preserved in the Department of Prints and Drawings, Uffizi.
	- The recto of the photograph of St. John the Baptist by Vicino da Ferrara

#### Proprieties:

+ [K6 has back (has front)]: [IC20 Verso]
+ [K7 is recto of (has recto)]: E22 Man-Made Object

### IC20 Verso

Subclass of: **E19 Physical Feature**

The back or underside of a single sheet of paper, or the left-hand page of an open book. The feature is presents in object such as codex, books, pamphlets, documents, photographs and painting.

**Example**:

	- The verso of the drawing 57 E v "Testa di donna di profile" by Anonymous XVI century, preserved in the Department of Prints and Drawings, Uffizi
	- The photographer's stamp in the verso of the photograph of St. John the Baptist by Vicino da Ferrara

#### Proprieties:

+ [K6 has front (has back)]: [IC19 Recto]
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

#### K6 has back (has front)

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

#### K15 use features (has been used by)

Domain: E12 Production   
Range: [IC10 Attribute]   
Subproperty: P33 used specific technique   

The property indicates the specific attribute used during the production of a visual object

#### K17 Has attribute (is attribute of)

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

#### K24 Portray (is portrayed in)

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