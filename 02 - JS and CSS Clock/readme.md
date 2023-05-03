# JS + CSS Clock

To make the clock hands rotate at right side we need use transform and transition elements.
The transition element is used to move the hand smoothly.

```css
.hand{
    transform:rotate(90deg);
    transform-origin:100% ;
    transition: all 0.5s;
    transition-timing-function: cubic-bezier(0.42, 0, 0.11, 0.77);
}
```

#### Make Clock functions
The querySelector has been used to set the current time in terms of hour, minute and seconds to the clock hands. ```setDate``` function has been used to apply the function to relative hand to make it rotate.

##### Seconds Hand
```javascript
    const secondHand = document.querySelector('.second-hand');
    function setDate() {
      const now = new Date();
      const seconds = now.getSeconds();
    }
    setInterval(setDate, 1000);
 

```

##### Minutes Hand
```javascript
    const minuteHand = document.querySelector('.min-hand');
      const now = new Date();
      const minutes = now.getMinutes();
      const minutesDegrees = (minutes / 60) * 360 + 90;
      minuteHand.style.transform = `rotate(${minutesDegrees}deg)`;
     
```
##### Hours Hand
```javascript
      const now = new Date();
      const hours = now.getHours();
      const HoursDegrees = (hours / 12 * 360) + 90;
      hourHand.style.transform = `rotate(${HoursDegrees}deg)`;

```
