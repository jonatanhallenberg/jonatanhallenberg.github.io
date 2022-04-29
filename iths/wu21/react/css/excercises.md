# Övningar CSS

**1) Inline Styling**

- Använd inline styling och skapa en React-komponent som är en textruta (input) med följande styling:

```css
input {
    font-size: 18px;
    line-height: 20px;
    border: 1px solid gray;
    border-radius: 3px;
}
```
<details>
    <summary>Svar</summary>

```jsx
const Title = (props) => <h1>{props.text}</h1>
```
</details>

**2) CSS Modules**

- Använd CSS Modules och skapa en React-komponent som är en textruta (input) med följande styling:

```css
input {
    font-size: 18px;
    line-height: 20px;
    border: 1px solid gray;
    border-radius: 3px;
}
```

<details>
    <summary>Svar</summary>

```jsx
const Title = (props) => <h1>{props.text}</h1>
```
</details>

---

**3) Övning - Styled components**

- Skapa en React-komponent som är en textruta (input) med följande styling:

```css
input {
    font-size: 18px;
    line-height: 20px;
    border: 1px solid gray;
    border-radius: 3px;
}
```

---

**4) Övning - Styled Components m. props**

- Skapa en textbox-komponent som tar emot en prop som heter isValid
- Om isValid=true ska bakgrundsfärger vara vit
- Om isValid=false ska bakgrundsfärgen vara ljusröd

```tsx
//Exempel på implementation
<Textbox isValid={false} />
```

---