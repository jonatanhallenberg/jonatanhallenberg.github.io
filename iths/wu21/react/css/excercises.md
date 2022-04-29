# Övningar CSS

**1) Inline Styling**

- Använd inline styling och skapa en React-komponent som är en textruta (input) med följande styling:

```css
input {
    font-size: 18px;
    border: 1px solid gray;
    border-radius: 3px;
    padding: 20px;
}
```
<details>
    <summary>Svar</summary>

```jsx
const textboxStyle = {
    fontSize: "18px",
    border: "1px solid gray",
    borderRadius: "3px",
    padding: "20px"
}
const Textbox = () => (
    <input type="text" style={textboxStyle} />
)
export default Textbox;
```
</details>

**2) CSS Modules**

- Använd CSS Modules och skapa en React-komponent som är en textruta (input) med följande styling:

```css
input {
    font-size: 18px;
    border: 1px solid gray;
    border-radius: 3px;
    padding: 20px;
}
```

<details>
    <summary>Svar</summary>

```css
/* textbox.module.css*/
.textBox {
    font-size: 18px;
    border: 1px solid gray;
    border-radius: 3px;
    padding: 20px;
}
```

```jsx
//Textbox.jsx
import styles from './textbox.module.css'
const Textbox = () => (
    <input type="text" className={styles.textBox} />
)
```
</details>