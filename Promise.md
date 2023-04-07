Это объект, который возвращает успешное или неуспешное выполнение функции исполнителя. Он связывает исполнителя с функциями потребителями - теми, функциями, которые будут выполняться только когда получат необходимый результат

```js
let promise = new Promise(function(resolve, reject) { 
	// эта функция выполнится автоматически, при вызове new Promise 
	// через 1 секунду сигнализировать, что задача выполнена с результатом "done" 
	setTimeout(() => resolve("done"), 1000); 
});
```

Нам не нужно писать функции `resolve` и `reject` самому - они уже встроены в JS. Нам только нужно передать одну из них в коде (в примере выше мы передали успешно выполненный промис)

![[Screenshot 2023-04-05 at 20.40.48.png]]

Промис - это объект, а значит у него есть следующие состояние (картинка выше)

Исполнитель (код, который выполняется внутри промиса) должен вызвать resolve или reject только один раз

	Reject стоит использовать с объектом Error
	`reject(new Error("…")`

Так как возвращается объект, мы можем указать любые поля и значения в этом объекте и далее работать с ним