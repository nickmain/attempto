In order to define aliases, i.e. word forms that are parsed in exactly the same way, one has to create several entries with the same logical symbol. Some examples:

``` prolog
adj_itr(gray, gray).
adj_itr(grey, gray).

noun_sg(cactus, cactus, neutr).
noun_pl(cacti, cactus, neutr).
noun_pl(cactuses, cactus, neutr).

pndef_pl('United-States', 'USA', neutr).
pndef_pl('USA', 'USA', neutr).
```
