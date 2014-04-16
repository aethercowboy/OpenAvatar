OpenAvatar
==========

An XML specification to describe your virtual personae. This is not associated with VastPark's project of the same name (http://vastpark.org/projects/1/wiki/OpenAvatar), but they're welcome to incorporate it if they like. :)

Definition
----------

Avatar here is a word used to describe the physical characteristics of player character (or "toon") in a video game or
other environment in which a virtual persona would prove beneficial. It does not refer to a user icon, as one might see
on a blogging site, or through something like Gravatar or Libravatar.

Purpose
-------

My long-term goal for this project is for major players in the video game field to adopt this technology into their own
products, allowing their users to easily import/export their characters to/from the game, allowing players to transfer
a likeness of their character to a new game without too much overhead.

If you would like to join this project, please contact one of its members.

Documentation
-------------

In the text below, if an attribute value is rendered in CAPS, it is the default value. In the case of a discrepancy
between the documentation and the software, please file an issue, but take note that the specifications in the 
documentation reflect the desired behavior, and as such, the code will typically be adjusted to reflect the behavior
described here.

If you feel that the document should be amended, please write an issue as well describing your concern.

### OAML

The OAML tag is the main tag. It contains the OpenAvatar Markup that describes the character.

**Tags**

NAME, BODY

**Attributes**

none

### NAME

The NAME tag contains the name of the avatar. This could be used to attempt to automatically name the character if that
name is not already registered.

**Tags**

text

**Attributes**

none

### BODY

The BODY tag contains all the pieces of the character's body. It also describes certain physical properties of the 
character itself.

**Tags**

HEAD, SKIN, ARMS, LEGS

**Attributes**

*gender* {REQUIRED} (male|female|other|unknown)

>  The character's gender. Can be used to specify certain physiological traits on the character.

*build* (LEAN|fat|muscular)

>  The character's build. Can be used to make more muscular or more fat characters.

*shape* (v|hourglass|apple|pear|STRAIGHT)

>  The character's body shape. Can be used to determine distribution of girth.

*height* (short|AVERAGE|tall)

>  The character's height. Can be used to make them taller or shorter.

*weight* (light|AVERAGE|heavy)

>  The character's weight. Can be used to make them skinnier or thicker.
  
### HEAD

The HEAD tag contains the description of the character's head.

**Tags**

HAIR, EYES, EARS, MOUTH, NOSE

**Attributes**

none

### SKIN

The SKIN tag describes the character's skin.

**Tags**

none

**Attributes**

*color* (CDATA)

>  The color of the character's skin. Can use standard ways of specifying color in an XML document.
  
*tone* (pale|light|AVERAGE|tan|dark)

>  A modifier for skin tone. Can be used to adjust lightness or darkness atop specified color.

### ARMS

The ARMS tag contains a description for the arms of the character.

**Tags**

ARM{*}

**Attributes**

*length* (none|short|AVERAGE|long)

>  The length of the arms.

*count* (CDATA)

>  The number of arms the character has. The default value is 2.
  
### LEGS

The LEGS tag contains a description for the legs of the character.

**Tags**

LEG{*}

**Attributes**

*length* (none|short|AVERAGE|long)

>  The length of the legs.

*count* (CDATA:2)

>  The number of legs the character has. The default value is 2.

### HAIR

The HAIR tag describes the hair of the character.

**Tags**

none

**Attributes**

*color* (CDATA)

>  The preferred hair color.

*length* (none|short|AVERAGE|long)

>  The preferred hair length. None is bald.

### EYES

The EYES tag describes the character's eyes.

**Tags**

EYE{*}

**Attributes**

*color* (CDATA)

>  The preferred eye color (the iris).

*shape* (narrow|AVERAGE|wide)

>  The preferred shape of the eye.

*vergence* (cross|AVERAGE|wall)

>  Which way the eyes are looking (straight ahead, at each other, or away from each other)

*size* (small|AVERAGE|large)

>  The size of the eyes.

*count* (CDATA:2)

>  The number of eyes. Default 2.

### EARS

The EARS tag describes the ears of the character.

**Tags**

EAR{*}

**Attributes**

*shape* (ROUNDED|pointed)

>  The preferred shape of the ears: human or elvish.

*size* (small|AVERAGE|large)

>  The size of the ears.
  
*count* (CDATA:2)

>  How many ears? Default 2.

### MOUTH

The MOUTH tag describes the character's mouth.

**Tags**

none

**Attributes**

*shape* (narrow|AVERAGE|wide)

>  The shape of the character's mouth.

*size* (small|AVERAGE|large)

>  The size of the character's mouth.

*type* (smile|NEUTRAL|frown)

>  Is the character smiling, frowning, or keeping straight-faced?

### NOSE

The NOSE tag describes the character's nose.

**Tags**

none

**Attributes**

*size* (none|small|AVERAGE|large)

>  The size of the character's nose.

### ARM

The ARM tag is used to describe a particular arm of the character.

**Tags**

HAND

**Attributes**

*side* {REQUIRED} (left|right)

>  Which side is the arm on?

*length* (none|short|AVERAGE|long)

>  The length of the arm.
  
### LEG

The LEG tag describes a particular leg of the character.

**Tags**

FOOT

**Attributes**

*side* {REQUIRED} (left|right)

>  Which side is the leg on?

*length* (none|short|AVERAGE|long)

>  The length of the leg.

### EYE

The EYE tag describes a particular eye of the chracter.

**Tags**

IRIS, PUPIL, SCLERA

**Attributes**

*side* {REQUIRED} (left|right|middle)

>  Which side is the eye on?

*color* (CDATA)

>  What color is the eye (iris)?

*shape* (narrow|AVERAGE|wide)

>  The shape of the eye.

*vergence* (cross|AVERAGE|wall)

>  The way the eye is pointing.

*size* (none|small|AVERAGE|large)

>  The size of the eye.

### EAR

The EAR tag describes a particular ear of the character.

**Tags**

none

**Attributes**

*side* {REQUIRED} (left|right)

>  What side is the ear on?

*shape* (RONDED|pointed)

>  Is the ear rounded or pointed?
  
*size* (none|small|AVERAGE|large)

>  The size of the ear.

### HAND

The HAND tag describes a particular hand of the character.

**Tags**

FINGERS

**Attributes**

*side* {REQUIRED} (left|right)

>  What side is the hand on?

*size* (none|small|AVERAGE|large)

>  The size of the hand.
  
### FOOT

The FOOT tag describes a particular foot of the character.

**Tags**

TOES

**Attributes**

*side* {REQUIRED} (left|right)

>  What side is the foot on?

*size* (none|small|AVERAGE|large)

>  The size of the foot.

### IRIS

The IRIS tag describes a particular iris (the colored part of the eye) of the character.

**Tags**

none

**Attributes**

*color* (CDATA)

>  The preferred eye color.

*size* (none|small|AVERAGE|large)

>  The size of the iris.

### PUPIL

The PUPIL tag describes a particular pupil (the black part of the eye) of the character.

**Tags**

none

**Attributes**

*color* (CDATA:black)

>  The color of the pupil. Default black.

*size* (none|small|AVERAGE|large)

>  The size of the pupil.
  
*shape* (slit|CIRCLE|camera)

>  The shape of the pupil. Slit are like cat pupils. Camera are like octopus pupils.

### SCLERA

The SCLERA tag describes a particular sclera (the white part of the eye) of the character.

**Tags**

none

**Attributes**

*color* (CDATA:white)

>  The color of the sclera. Default white.

### FINGERS

The FINGERS tag describes a collection of fingers of the character.

**Tags**

FINGER{*}

**Attributes**

*count* (CDATA:5)

>  How many fingers? Default 5.

*length* (none|short|AVERAGE|long)

>  The length of the fingers.

### TOES (toe*)>

The TOES tag describes a collection of toess of the character.

**Tags**

TOE{*}

**Attributes**

*count* (CDATA:5)

>  How many toes? Default 5.

*length* (none|short|AVERAGE|long)

>  The length of the toes.

### FINGER

The FINGER tag describes a particular finger of the character.

**Tags**

none

**Attributes**

*index* {REQUIRED} (CDATA)

>  The index of the finger (zero-indexed).

*length* (none|short|AVERAGE|long)

>  The length of the finger.

### TOE

The TOE tag describes a particular toe of the character.

**Tags**

none

**Attributes**

*index* {REQUIRED} (CDATA)

>  The index of the toe (zero-indexed).
  
*length* (none|short|AVERAGE|long)

>  The length of the toe.
