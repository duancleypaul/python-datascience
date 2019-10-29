# python-datascience

## Pandas

```
import pandas as pd
import numpy as np
```

## Series
```
s = pd.Series([7, 'Heisenberg', 3.14, -1789710578, 'Happy Eating!'])
s
```

## Mudando Índices
```
s = pd.Series([7, 'Heisenberg', 3.14, -1789710578, 'Happy Eating!'],
              index=['A', 'Z', 'C', 'Y', 'E'])
s
```

## Series a partir de dicionário
```
d = {'Chicago': 1000, 'New York': 1300, 'Portland': 900, 'San Francisco': 1100,
     'Austin': 450, 'Boston': None}
cities = pd.Series(d)
cities
```

## Selecionando dados
```
cities[cities < 1000]
```

## Mostrando itens da series que atendem a condição
```
less_than_1000 = cities < 1000
print(less_than_1000)
print('\n')
print(cities[less_than_1000])
```

## Carregando um DataFrame a partir de um CSV
```
from_csv = pd.read_csv('mariano-rivera.csv')
from_csv.head()
```

## Carregando um DataFrame a partir de uma URL
```
url = 'https://raw.github.com/gjreda/best-sandwiches/master/data/best-sandwiches-geocode.tsv'

# fetch the text from the URL and read it into a DataFrame
from_url = pd.read_table(url, sep='\t')
from_url.head()
```
