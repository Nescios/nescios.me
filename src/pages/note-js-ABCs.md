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

## Iterate over an array of data to render 
```javascript
function renderData() = {
    let html = ""
    const data = [{title: "Yo", body: "description"}, {title: "Hi", body: "description"}]
    for (let post of data) {
        html += `<div class="post">
                <h2>${post.title}</h2>
                <p>${post.body}</p>
            </div>`
}   return html
}
document.getElementById("posts").innerHTML = renderData()
```

## Use Map to iterate over an array
    
```javascript
new Array(7).fill(0).map((_, i) => i + 1)
// [1, 2, 3, 4, 5, 6, 7]
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

## Replace word by another word with regex

```javascript
const sentence = "The quick Brown fox jumps over the lazy dog"
sentence.replace(/brown/i, "red")
// With regex /i, it will not be case sensitive
// With regex /g, it will replace all the matches [source](https://www.w3schools.com/js/js_regexp.asp)
```
