<h1 align = 'center'>Objects</h1>

## Объект - самостоятельная единица, имеющая свойства и определенный тип. 

<h1 align = 'center'>Создание Объекта</h1>

```javascript
let person = {
    firstName: 'Abubakr',
    lastName: 'Ashurov',
    age: 15,
}
```

## Object - Methods
+ Object.entries()
```javascript
let people = {
    name: 'Adam',
    age: 43,
}
console.log(Object.entries(people))
// Output [['name', 'Adam'], ['age', 43]] 
```
+ Object.keys()
```javascript
let people = {
    name: 'Adam',
    age: 43,
}
console.log(Object.keys(people))
// Output ['name', 'age']
```
+ Object.values()
```javascript
let people = {
    name: 'Adam',
    age: 43,
}
console.log(Object.values(people))
// Output ['Adam', 43] 
```

## Destructuring & Spread
```javascript
const person = {
    name: 'Sara',
    age: 18,
    gender: 'female',
}

let name = person.name;
let {age, gender} = person;
let cloneObj = {...person} // Spread
console.log(cloneObj)
// Output  {name: 'Sara', age:18, gender: 'female',}
console.log(cloneObj == person) // false
console.log(name) // Sara
console.log(age) // 25
console.log(gender) // female
```

<h1 align = 'center'>This</h1>

## This - это ссылка на некий объект к свойствам которого можно получить доступ внутри вызова функции.

+ In an object method, `this` refers to the Object
+ Alone, `this` refers to the Global Object
+ In a function, `this` refers to the Global Object
+ In a function, in strict mode, `this` is `undefined`.

### `this` is **NOT** a variable. It is a **keyword**. You can not change the value of `this`.
```javascript
const jonas = {
    name: 'Jonas',
    year: 1989,
    calcAge: function(){
        return 2023 - this.year
    }
};
jonas.calcAge(); // 48
```
