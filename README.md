# Payment Form with Custom Radio Buttons & Dark Mode

## Demo
https://asmanord.github.io/OnlinePayment/

## Custom Radio Button Images Implementation
This project showcases an advanced implementation of clickable images as radio button selectors for payment methods. The technique combines hidden radio inputs with associated images, creating an intuitive and visually appealing user interface.

### How it Works

1. **HTML Structure**
```html
<div class="payment-options">
    <label>
        <input type="radio" name="payment" value="visa">
        <img src="visa.jpg" alt="Visa">
    </label>
</div>
```

2. **CSS Implementation**
- Radio inputs are hidden using `display: none`
- Images act as visual replacements for radio buttons
- Selection state is indicated through border styling
- Hover effects enhance user interaction

```css
.payment-options input {
    display: none;
}

.payment-options img {
    width: 60px;
    height: auto;
    transition: transform 0.2s ease-in-out;
}

.payment-options input:checked + img {
    border: 2px solid blue;
    border-radius: 5px;
}
```

## Dark Mode Implementation
The project features a JavaScript-free dark mode implementation using modern CSS selectors.

### Key Features

1. **:has() Selector**
- Utilizes the modern CSS `:has()` selector for theme switching
- Enables parent element styling based on child state
- No JavaScript required

2. **Theme Switch**
```html
<label class="switch">
    <input type="checkbox" id="switch-input">
    <svg class="light-icon">...</svg>
    <svg class="dark-icon">...</svg>
</label>
```

3. **CSS Theme Implementation**
```css
/* Light Mode (Default) */
body {
    background: linear-gradient(to right, #4facfe, #00f2fe);
}

/* Dark Mode */
body:has(.switch input:checked) {
    background: linear-gradient(to right, #2c3e50, #3498db);
}
```

### Dark Mode Features
- Automatic theme switching for all components
- Smooth transitions between themes
- Persistent styling across all form elements
- Contrast-appropriate color schemes
- Accessible color combinations

## Browser Compatibility
- The `:has()` selector is supported in modern browsers:
  - Chrome 105+
  - Safari 15.4+
  - Firefox 121+
  - Edge 105+

## Technical Highlights
- Pure CSS implementation
- No JavaScript dependencies
- Smooth transitions
- Accessible design
- Responsive layout
- Modern CSS selectors
