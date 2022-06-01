---
title : Javascript ABC's
---

## Javascript naming convention

```javascript
function get[element]Array() {}
function set[element]() {}
function get[element]PlaceHolderHtml () {}
function render[element]() {}
```

---

## Fetch data from API

```javascript
fetch("https://dog.ceo/api/breeds/image/random")
    .then(response => response.json())
    .then(data => {
        console.log(data)
        document.body.innerHTML = `
            <img src="${data.message}" />
        `
    })
```

## Object creator

```javascript
class Character {
    constructor(data) {
        Object.assign(this, data)
    }
    getCharacterHtml() {
        const {name, image, description} = this
        return `
            <div class="character">
                <h2>${name}</h2>
                <img src="${image}" />
                <p>${description}</p>
            </div>
        `
    }
}
```

## Local Storage

```javascript
localStorage.setItem("name", "John")
localStorage.getItem("name")
localStorage.removeItem("name")
localStorage.clear()
// Convert JSON to JavaScript
const charactersFromLocalStorage = JSON.parse(localStorage.getItem("characters"))
// Convert JavaScript to JSON (JSON needs to be a string)
localStorage.setItem("characters", JSON.stringify(characters))
```