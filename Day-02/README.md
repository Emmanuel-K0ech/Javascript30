# Day 2: CSS + JS Clock ⏰

This project is part of the **30 Days of JavaScript** challenge by Wes Bos. It involves building a dynamic clock using HTML, CSS, and JavaScript. The clock includes a smooth rotation for the hour, minute, and second hands, updating in real-time.

## Project Overview

This project demonstrates how to:
- Use CSS to style and position elements with `transform-origin` and `rotate` properties.
- Utilize JavaScript to manipulate the DOM and animate the clock hands in real-time.
- Apply the `Date()` object in JavaScript to access the current time and dynamically calculate the rotation angles of the clock hands.

## Technologies Used

- **HTML5**: To structure the clock elements.
- **CSS3**: To style the clock and rotate the hands.
- **JavaScript (ES6)**: To update the time every second and apply smooth animations.

## Features

- **Real-Time Clock**: The second, minute, and hour hands rotate based on the current time.
- **Smooth Animations**: The clock hands move smoothly across the clock face for a visually appealing effect.

## How It Works

1. The current time is fetched using JavaScript’s `Date()` object.
2. The second, minute, and hour values are converted into corresponding degrees.
3. The `transform: rotate()` CSS property is dynamically updated using JavaScript to rotate the clock hands based on time values.

### Key JavaScript Logic

- **Seconds Calculation**: 
   ```javascript
   const seconds = now.getSeconds();
   const secondsDegrees = ((seconds / 60) * 360) + 90;
   secondHand.style.transform = `rotate(${secondsDegrees}deg)`;
   ```
  
- **Minutes Calculation**:
   ```javascript
   const mins = now.getMinutes();
   const minsDegrees = ((mins / 60) * 360) + 90;
   minsHand.style.transform = `rotate(${minsDegrees}deg)`;
   ```
  
- **Hours Calculation**:
   ```javascript
   const hours = now.getHours();
   const hoursDegrees = ((hours / 12) * 360) + 90;
   hourHand.style.transform = `rotate(${hoursDegrees}deg)`;
   ```

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/30-days-js-challenge.git
   ```
2. Navigate to the project directory:
   ```bash
   cd day-02
   ```
3. Open the `index.html` file in your browser to see the clock in action.
