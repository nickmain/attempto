## ACE Texts

An ACE text is a sequence of [[Construction Rules#Declarative Sentences|declarative]], [[Construction Rules#Interrogative Sentences|interrogative]] and [[Construction Rules#Imperative Sentences|imperative]] sentences. All sentences can anaphorically refer to preceding declarative sentences, but not to interrogative and imperative sentences.

>[!example]
>Mary enters a card into a machine. Its screen blinks or Mary waits.
>
>A man has a car. Does he see the car? John, identify the car!

## Sentences
### Declarative Sentences

Declarative sentences are simple sentences, _there is/are_-sentences, boolean formulas, and composite sentences.

#### Simple Sentences

Simple sentences have the structure

> [[Construction Rules#Noun Phrases|noun phrase]] + [[Construction Rules#Verb Phrases|verb phrase]].

>[!example]
>A customer waits.
>
>A customer inserts a card.
>
>A customer gives a card to a clerk.
>
>A customer gives a clerk a card.
>
>A customer inserts a card manually into a slot.
>
>A customer manually inserts a card into a slot.

#### _there is/are_-Sentences

It is possible to create well-formed sentences without a verb, by using the _there is/are_ construction.

> _there is_ + [[Construction Rules#Noun Phrases|noun phrase]]
> 
> _there are_ + [[Construction Rules#Noun Phrases|noun phrase]]

This construct just introduces the entities described by the noun phrase into the discourse, or if negated, denies their existence. For this reason noun phrases following _there is/are_ cannot be and cannot contain definite noun phrases, universally quantified noun phrases, proper names, numbers, arithmetic expressions, strings, sets, or lists. 

>[!example]
>There is a customer.
>
>There is some water.
>
>There are more than 6 clerks.
>
>There are a cat and 2 dogs.
>
>There is X.
>
>There is no man who sleeps.
>
>There is a cat in a garden.
>
>There is a cat that sleeps.

#### Boolean Formulas

Boolean formulas also count as sentences. They are built from numbers, arithmetic expressions, proper names and variables with the help of the comparison operators `=`, `\=`, `>`, `>=`, `<` and `=<`. As other sentences boolean formulas can be coordinated by `and`, `or`, `,and` and `,or`.

>[!example]
>10 = 4 + 6.
>
>X \= 2.
>
>5 > 3.
>
>X >= 13.4 and X < 20.
>
>2 ^ (2 ^ 2) = (2 ^ 2) ^ 2

#### Composite Sentences

Composite sentences are recursively built from simple sentences, _there is/are_-sentences, boolean formulas, and other composite sentences with the help of the predefined constructors:

- coordination
- quantification 
- global quantification
- subordination

##### Coordinated Sentences

##### Locally Quantified Sentences

##### Globally Quantified Sentences

##### Subordination

ACE knows five forms of sentence subordination:

- conditional sentences (_if-then_ sentences)
- logical negation
- negation as failure
- modality
- sentence subordination

###### Conditional Sentences
###### Logical Negation
###### Negation as Failure
###### Modality
###### Sentence Subordination


### Interrogative Sentences



### Imperative Sentences

ACE supports simple imperative sentences, briefly called commands. A command consists of a [[Construction Rules#Noun Phrases|noun phrase]] (the addressee), followed by a comma, followed by an uncoordinated [[Construction Rules#Verb Phrases|verb phrase]] (possibly negated). A command must end with an exclamation mark.

>[!example]
>John, go to your own bank!
>
>John and Mary, clean yourselves!
>
>Every dog, do not bark!
>
>John's brother, return the book to Mary!

## Phrases

### Noun Phrases

### Verb Phrases

