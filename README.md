# Fundamentos ReactJS Desafio
It will list all transactions and use an extra screen to import CSV file.

## Dashboard
Atualizar useEffect

### formattedValue
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

### formattedDate
```js
formattedDate: new Date(transaction.created_at).toLocaleDateString('pt-BR')
```

## Balance
interface Balance came with all strings.
It was changed to numbers.  And each number would be called with formatValue function described before.

## Transactions
interface Transactions had extra:
  formattedValue: string;
  formattedDate: string;

The abovewas added on each transaction. No need to convert in the html.

## Import
submitFile receives the file name and needs to be divided on
interface FileProps {
  file: File;
  name: string;
  readableSize: string;
}

Then run the setUploadedFiles
Attention because this funcion was created to accomodate several files.
We just need one.

Then create 'data' using FormData();
So we can use inside the api.post

history.push('/'); is just an addition there.

