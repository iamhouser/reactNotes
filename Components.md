Бывают двух видов и отличаются только тем, как они будут созданы через объявление фунции или класс. Для React нет различий между двумя этими методами создания

1. [[Functional]]

```js
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```


1. [[Class]]

```js
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
