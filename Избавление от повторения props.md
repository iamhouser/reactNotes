Нередко будет ситуация, когда мы создали пропсы и все их передаем дальше в таком формате

```js
function Profile({ person, size, isSepia, thickBorder }) {  
	return (  
	<div className="card">  
		<Avatar  
			person={person}  
			size={size}  
			isSepia={isSepia}  
			thickBorder={thickBorder}  
		/>  
	</div>  
	);  
}
```

По сути мы переписываем все тоже самое в дочернем компоненте. Эта запись читабельна, но ее можно сократить до такой записи

```js
function Profile({ person, size, isSepia, thickBorder }) {  

	return (  
		<div className="card">  
		<Avatar {...{ person, size, isSepia, thickBorder }} />  
		</div>  
	);  

}
```

Однако к такому методу надо относиться с осторожностью и не всегда применять. Если вы всегда применяете его, то нужно четко понимать, можно ли использовать все пропсы для данного компонента. Может оказаться, что часть можно, а часть нельзя. Это вызовет ошибки

Такой метод называется spread