## NPM Package name and their installation command.
1. Bootstrap
```
npm i bootstrap@5.3.5
```
2. FontAwesome Free
```
npm i --save @fortawesome/fontawesome-free
```
With the Unicode value found, you can add it to your recently-written custom CSS
```
.icon::before {
  /* Set the font for this icon style */
  font-family: 'Font Awesome 6 Free';
  /* Set the weight for this icon style */
  font-weight: 900;
  /* Make sure icons render pixel-perfect */
  -webkit-font-smoothing: antialiased;
  /* Set the Unicode value for the "fa-ghost" icon */
  content: '\f6e2';
}
```
3. Slick Slider
```
npm i slick-slider
```