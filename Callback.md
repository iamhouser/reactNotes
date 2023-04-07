**Это функция**, которая выполняется после того, как выполнено действие с первым аргументом функции
Например

```js
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```

У нас есть две функции `greeting` и `processUserInput`. Первая просто выводит алерт, а вторая принимает в себя функцию, которую должна выполнить внутри своего кода

Финальная функция `processUserInput(greeting)` запросит имя и после получения выполнит следующее действие, а не убежит вперед

