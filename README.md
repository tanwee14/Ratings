# ⭐ Feedback Rating App

A simple, interactive feedback rating UI built with HTML, CSS, and JavaScript. Users can select a satisfaction rating and submit it. Upon submission, a thank-you message with their selected rating is shown.

## 🚀 Features

* Clickable rating icons (e.g., 😐, 🙂, 😄)
* Highlights the selected rating
* Displays a confirmation message upon submission

## 🖼️ Demo

> *When a user selects a rating and clicks **Send**, they receive a thank-you message with the selected feedback.*

## 🧱 Built With

* **HTML** - Structure of the page
* **CSS** - Styling and layout
* **JavaScript** - Interactivity and DOM manipulation

## 📁 Project Structure

```
rating-app/
│
├── index.html
├── style.css
└── script.js
```

## 🧠 How It Works

### JavaScript Highlights

```js
// 1. Listen for clicks on the ratings container
ratingsContainer.addEventListener("click", e => {
    if (e.target.parentNode.classList.contains("rating")) {
        removeActive();
        e.target.parentNode.classList.add("active");
        selected = e.target.nextElementSibling.innerHTML;
    }
});

// 2. On "Send" button click, show thank you message
sendBtn.addEventListener("click", () => {
    panel.innerHTML = `
        <p class="heart">❤️❤️</p>
        <strong>THANK YOU !!</strong>
        <strong>Feedback Submitted : ${selected}</strong>
    `;
});

// 3. Remove previously active rating
function removeActive() {
    ratings.forEach(rating => rating.classList.remove("active"));
}
```


## ✨ Customization

* You can add more ratings (e.g., emojis or icons).
* Change the `selected` default value from `"Satisfied"` to any other initial choice.
* Improve accessibility by adding `aria-labels` or keyboard controls.

