Порой нам надо использовать в одном компоненте другой компонент. Это может выглядеть вот так 

```js
export defaut function Contact () {
	return (
		<Button/>
	)
}
```

Этот код будет работать, если компонент <Button/> уже существует или будут статические данные внутри (то есть не будет ситуации, что надо отрисовать другой компонент, исходя из действий пользователя)

Если же одно из условий выше не готово, но мы знаем, что в этом компоненте будет еще лежать, то применяется такая конструкция

```js
export default function Contact ({children}) {
	return (
		{children}
	)
}
```
