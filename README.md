-----

# ⏰ SVG Animated Digital Clock

A stylish and modern digital clock that visualizes time using animated SVG circles. This project displays the current hours, minutes, and seconds, each with its own circular progress indicator and a rotating dot, blending digital readability with an analog aesthetic.

-----

## ✨ Features

  * **Real-Time Display**: Shows the current time, updating every second.
  * **12-Hour Format**: Displays time in a 12-hour format with an AM/PM indicator.
  * **SVG Animation**: Each time unit (hours, minutes, seconds) is represented by a circular progress bar that fills up as time passes.
  * **Rotating Indicators**: A glowing dot rotates around each circle, mimicking the hands of an analog clock.
  * **Clean & Modern UI**: A sleek, dark-themed design makes the colorful, glowing time elements pop.
  * **Pure Vanilla JS**: Built with plain HTML, CSS, and JavaScript—no frameworks or libraries needed.

-----

## 🚀 How to Use

No installation or build steps are required. Simply open the `index.html` file in any modern web browser.

1.  **Download or Clone**: Get the project files (`index.html`, `index.css`, `index.js`).
2.  **Open**: Double-click the `index.html` file to run it locally in your browser.

-----

## 🛠️ How It Works

The clock's logic is built on three core web technologies:

### HTML (`index.html`)

The structure consists of a main container (`#time`) holding three sections for **hours**, **minutes**, and **seconds**. Each section contains:

  * An `svg` element with two `<circle>` shapes to create the background track and the animated progress ring.
  * A `div` with a dot class (`.hr_dot`, `.min_dot`, `.sec_dot`) for the rotating indicator.
  * A `div` to display the digital number and its corresponding label ("Hours", "Minutes", "Seconds").

### CSS (`index.css`)

The styling is responsible for:

  * **Layout**: Centering the clock on the page using Flexbox.
  * **Appearance**: Creating the circular elements, dark background, and font styles.
  * **Color Scheme**: Using a CSS custom property (`--clr`) to easily apply a unique, glowing color to each time unit.
  * **Animation Logic**:
      * The circular progress animation is achieved by manipulating the `stroke-dashoffset` property of the SVG circles.
      * The rotating dots are animated by updating the `transform: rotate()` property.

### JavaScript (`index.js`)

The core functionality resides in the JavaScript file:

  * A `setInterval` function runs every second to keep the clock updated.
  * Inside the interval, the `new Date()` object is used to get the current hours, minutes, and seconds.
  * The time values are formatted (e.g., converting to 12-hour format and adding leading zeros).
  * The script updates the `innerHTML` of the corresponding elements to display the digital time.
  * Finally, it calculates and applies the correct `strokeDashoffset` and `rotate` degree for the SVG circles and dots based on the current time. For example, the seconds circle offset is calculated as `440 - (440 * s) / 60`.

-----

## 🎨 Customization

You can easily change the colors of the clock elements. In the `index.html` file, modify the `--clr` custom property for each circle:

```html
<div class="circle" style="--clr:#ff2972;">

<div class="circle" style="--clr:#fee800;">

<div class="circle" style="--clr:#04fc43;">
```

Simply replace the hex color codes with your desired colors.
