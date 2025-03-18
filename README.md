# Digital Clock ⏰

A simple digital clock project built using HTML, CSS, and JavaScript.

## 📌 Features
- Displays the current time in **HH:MM:SS** format.
- Updates **every second**.
- Styled with CSS for a **modern look**.
- Works on all browsers and devices.

## 📂 Project Structure
```
digital-clock/
│── index.html      # Main HTML file
│── style.css       # CSS for styling
│── script.js       # JavaScript for functionality
└── README.md       # Project documentation
```

## 🚀 Live Demo
[🔗 View Digital Clock](https://DilaCode.github.io/digital-clock/) *(Update with your GitHub Pages link)*

## 🔧 How to Run
1. **Download or clone** the repository:
   ```sh
   git clone https://github.com/DilaCode/digital-clock.git
   ```
2. **Open** `index.html` in your browser.

## 🛠️ Technologies Used
- **HTML** - Structure of the clock.
- **CSS** - Styling for a modern look.
- **JavaScript** - Updates the time dynamically.

## 📜 Code Explanation
### **HTML (`index.html`)**
Creates the digital clock structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="clock-container">
        <h1 id="digital-clock">00:00:00</h1>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

### **CSS (`style.css`)**
Stylizes the clock:
```css
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #222;
    color: white;
    font-family: Arial, sans-serif;
    margin: 0;
}

.clock-container {
    text-align: center;
    font-size: 3rem;
    background: #333;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
}
```

### **JavaScript (`script.js`)**
Updates the time every second:
```js
function updateClock() {
    let now = new Date();
    let hours = now.getHours();
    let minutes = now.getMinutes();
    let seconds = now.getSeconds();

    hours = hours < 10 ? "0" + hours : hours;
    minutes = minutes < 10 ? "0" + minutes : minutes;
    seconds = seconds < 10 ? "0" + seconds : seconds;

    let timeString = `${hours}:${minutes}:${seconds}`;
    document.getElementById("digital-clock").textContent = timeString;
}

setInterval(updateClock, 1000);
updateClock();
```

## ✨ Future Improvements
- ✅ Add **AM/PM format**
- ✅ Show the **current date**
- ✅ Add **dark/light mode toggle**
- ✅ Customize clock **themes** (different colors/styles)

## 🤝 Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.

## 💡 Author
Created by **[DilaCode](https://github.com/DilaCode)**.  
Feel free to **contribute** and improve the project! 🚀

