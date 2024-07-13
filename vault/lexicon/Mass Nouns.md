Countable nouns (e.g. "water", "fear", "money") are represented by only one kind of entry:

``` prolog
noun_mass(WordForm, LogicalSymbol, Gender).
```

Mass nouns have only one word form. Defining a mass noun "water", for example, you can say "some water", "all water", or "5 kg of water". The gender of mass nouns is defined in the same way as for countable nouns (see previous section). Some concrete examples:

``` prolog
noun_mass(water, water, neutr).

noun_mass(fear, fear, neutr).

noun_mass(money, money, neutr).
```

It is recommended to use the word form also as the logical symbol.