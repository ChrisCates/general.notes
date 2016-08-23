# Code Conventions and Best Practices

## Why good conventions?

- Legibility and cleanliness of code.
- More scalable when you have larger teams.
- Easier to look at 6 months down the line.

## TABS OR SPACES IT DOESNT MATTER JUST DO IT.

### Bad spacing in HTML

```html
<html>
<body>
<h1>
Hello world
</h1>
</body>
</html>
```

#### Why is it bad?

- Hard to read.
- Hard to tell where it starts or ends.

### Good spacing in HTML

```html
<html>
  <body>
    <h1>Hello world</h1>
  </body>
</html>
```

#### Why is it good

- Clear separation of concern.
- Easy to identify where tags start and end.
- Easier to read from top to bottom.

## Camel Case or Snake Case are both good

### Bad Naming Conventions

```javascript
var obj = {
  mykeyvalue: 'foobar',
  mykeyvalue2: 'foobar'
}
```

#### Why is it bad?

- Unclear what the key is named.
- Is long and obfuscated.
- Hard to read.


### Good Camel Case Conventions

```javascript
var obj = {
  myKeyValue: 'foobar',
  myKeyValue2: 'foobar'
}
```

#### Why is it good?

- + Clear to see what the key is named.
- + Shorter the snake case.
- + Easy to read.
- - Slightly harder to read then Snake Case.


### Good Snake Case Conventions

```javascript
var obj = {
  my_key_value: 'foobar',
  my_key_value_2: 'foobar'
}
```

#### Why is it good?

- + Clear to see what the key is named.
- - Longer then Camel Case.
- + Easy to read.
- + Easier to read then Camel Case.
