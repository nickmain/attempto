Countable nouns (e.g. "woman", "credit-card", "month") are represented by two different kinds of entries, defining the singular form and the plural form respectively:

``` prolog
noun_sg(SingularForm, LogicalSymbol, Gender).
noun_pl(PluralForm, LogicalSymbol, Gender).
```

Defining a countable noun "credit-card", for example, you can say "a credit-card", "every credit-card", or "at most 5 credit-cards". The plural form should usually be the singular form with an 's' at the end like "credit-cards" or "months". Some concrete examples:

``` prolog
noun_sg(woman, woman, fem).
noun_pl(women, woman, fem).

noun_sg('credit-card', 'credit-card', neutr).
noun_pl('credit-cards', 'credit-card', neutr).

noun_sg(month, month, neutr).
noun_pl(months, month, neutr).
```

Gender has to be one of {undef, neutr, human, masc, fem} and specifies the linguistic gender of the noun. undef is the top category having two direct subcategories neutr and human where human has again two subcategories masc and fem. Depending on the gender, different forms of pronouns are supported. The table below shows the concrete pronouns. Note that not only the pronouns listed for a particular gender but also all pronouns of all super- and subcategories can be used.

| Gender | Anaphoric Pronouns                                                 | Possessive Pronouns                        | Relative Pronouns |
| ------ | ------------------------------------------------------------------ | ------------------------------------------ | ----------------- |
| undef  | they, them, themselves                                             | their, their own                           | that, whose       |
| neutr  | it, itself                                                         | its, its own                               | which             |
| human  | he/she, she/he, him/her, her/him, himself/herself, herself/himself | his/her, her/his, his/her own, her/his own | who               |
| masc   | he, him, himself                                                   | his, his own                               |                   |
| fem    | she, her, herself                                                  | her, her own                               |                   |

It is recommended to use the singular form also as the logical symbol. Furthermore, it is recommended to define a singular form for each plural form, and vice versa.