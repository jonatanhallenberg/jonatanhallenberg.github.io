---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

![bg left:40% 80%](../../Customization/iths-logo.png)

# CSS i React

Jonatan Hallenberg

---

# Intro

- Det finns olika sätt att använda sig av CSS i React
- Vi ska gå igenom:
  - Global CSS
  - Inline Styling
  - CSS modules
- Samt se hur man länkar i Google Fonts i Create React App

---

# Global CSS

- Precis som att länka in en CSS fil i en HTML-sida
- En CSS-class som finns här kan användas var som helst på sidan

```tsx
import './App.css';
```

---

# Scoped styling

- I React vill man undvika global styling
- Istället ska varje komponent ha sin egen lokala CSS som är oberoende av andra komponenters CSS
- Detta kallas **scoped styling** och kan åstadkommas på flera sätt

---

# Inline Styling

- Style attributet används och sätts till ett javascript-objekt
- Objektet har attribut som motsvarar CSS-attribut
- Attributen måste skrivas i camelCase så t.ex. background-color blir backgroundColor
- Attributvärdena måste oftast skrivas som strängar

---

# Inline styling - exempel

```tsx
    const ButtonStyle = {
        backgroundColor: "#333333",
        borderRadius: "3px",
        padding: "5px 10px",
        color: "white"
    };
```

```html
<button style={ButtonStyle}>En stylad knapp!</button>
```
---

# Övning - Inline Styling

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

# CSS Modules

- CSS Modules är ett annat sätt att ha *scoped styling*
- En fil för CSS-moduler har filändelsen *.module.css*
- I den filen skriver man helt vanliga CSS-klasser
- Genom att importera filen i komponenten får man tillgång till CSS-klasserna och kan applicera på olika element via className

---

# CSS Modules - exempel

```css
/*button.module.css*/
.button {
    background-color: #333333;
    border-radius: 3px;
    padding: 5px 10px;
    color: white;
};
```

```tsx
import styles from './button.module.css';
const ButtonCSSModule = () => (
    <button className={styles.button} type="button">Klicka här</button>
);
export default ButtonCSSModule;
```
---

# Övning - CSS Modules

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

# Google Fonts

- För att vara säker på att kunna använda ett visst typsnitt är Google Fonts smidigt
- Det finns lite olika sätt att länka in Google Fonts till Create React App. Läs mer om dessa här https://blog.greenroots.info/3-quick-ways-to-add-fonts-to-your-react-app
- Det enklaste är att länka in CSS-filerna från Google CDN direkt i public/index.html