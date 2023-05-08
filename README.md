# Isogramma

## programma in C# console tast based che con un inserimento di una stringa dice se è un isogramma o no

### isogramma = parola con nessuna lettera ripetuta

# Codice:


### varaibili e soluzioni basialri:

```C#

char lettera, lettera2;
bool Verifica = true;

// soluzioni basilari
if (word.Length == 0){
  return true;
}

```


### programma principale:

```C#
for (int x = 0; x < word.Length-1; x++){

  lettera = word[x];

  if (Char.IsLetter(lettera)){     // controlla se è una lettera, e in caso di risultato positivo fa partire il programma

      lettera = Char.ToLower(lettera);

      for  (int i = x+1; i < word.Length; i++){   // for di verifica per l' uguaglianza
                    
        lettera2 = Char.ToLower(word[i]);

          if (lettera == lettera2)
          {
              Verifica = false;
          }

      }
  }
}
```


### restituzione del risultato:


```C#

if (Verifica){   // restituisce il risultato
  return true;
} else {
  return false;
}
```
