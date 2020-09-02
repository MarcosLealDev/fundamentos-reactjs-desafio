### Fundamentos ReactJS Desafio

## Dashboard
Atualizar useEffect

# formattedValue
utils/formatValue.ts must be eddited to
```js
const formatValue = (value: number): string =>
  Intl.NumberFormat('pt-BR', {
    style: 'currency',
    currency: 'BRL',
  }).format(value);
  ```

Then you can use:
```js
formatValue(transaction.value)
```

# formattedDate
```js
formattedDate: new Date(transaction.created_at).toLocaleDateString('pt-BR')
```

# Balance
interface Balance came with all strings.
It was changed to numbers.  And each number would be called with formatValue function described before
