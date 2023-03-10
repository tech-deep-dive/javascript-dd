# Map

Map is a `collection of keyed data items`, just like an Object. But the main difference is that `Map allows keys of any type` and `maintain order insertion`

Methods and properties are:

- `new Map()` – creates the map
- `map.set(key, value)` – stores the value by the key
- `map.get(key)` – returns the value by the key, undefined if key doesn’t exist in map
- `map.has(key)` – returns true if the key exists, false otherwise
- `map.delete(key`) – removes the element (the key/value pair) by the key
- `map.clear()` – removes everything from the map
- `map.size` – returns the current element count

```
  const map = new Map([[1, "one"]]);
  map.set({ num: 2 }, "two");

  console.log(map); // Map(2) {1 => 'one', 2 => 'two'}
```

## # Iteration over Map

For looping over a map, there are 3 methods:

- `map.keys()` – returns an iterable for keys
- `map.values()` – returns an iterable for value
- `map.entries()` – returns an iterable for entries [key, value], it’s used by default in for..of

```
  let recipeMap = new Map([
    ['cucumber', 500],
    ['tomatoes', 350],
    ['onion',    50]
  ]);

  for (let vegetable of recipeMap.keys()) {
    alert(vegetable); // cucumber, tomatoes, onion
  }

  for (let amount of recipeMap.values()) {
    alert(amount); // 500, 350, 50
  }

  for (let entry of recipeMap) { // the same as of recipeMap.entries()
    alert(entry); // cucumber,500 (and so on)
  }
```

Besides that, Map has a built-in forEach method, similar to Array

```
  recipeMap.forEach( (value, key, map) => {
    alert(`${key}: ${value}`); // cucumber: 500 etc
  });
```

## # Map from Object

```
  let obj = {
    name: "John",
    age: 30
  };

  let map = new Map(Object.entries(obj));
```

## # Object from Map

```
  let map = new Map();
  map.set('banana', 1);
  map.set('orange', 2);
  map.set('meat', 4);

  let obj = Object.fromEntries(map.entries());
```
