Properties(props) или свойства - это параметры того или иного компонента. Например

```js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
const element = <Welcome name="Sara" />;
root.render(element);
```

У нас есть функция Welcome, которая принимает в себя  какое-то значение, а потом берет это значение и подставляет в теги `<h1></h1>`

props в примере выше - это объект, поэтому запись `{props.name}` добавляет поле name к этому объекту. Если мы захотим, мы могли бы написать любую другую переменную, `{props.age},{props.weight},{props.gender}...`.  

В итоге, когда мы будем использовать этот компонент и захотим передать какое-то значение в параметр, то просто можем написать в формате `параметр = значение`. Так мы и сделали в этой строчке

```js
const element = <Welcome name="Sara" />;
```

Если бы у нас был бы еще props.age, то мы могли еще написать 

```js
const element = <Welcome name="Sara" age="50" />
```


	Всегда следует писать компонент с большой буквы!