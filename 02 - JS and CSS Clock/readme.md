Clock

To make the clock hands rotate at right side we need use transform and transition elements.
The transition element is used to change the hand

```css
.hand{
    transform:rotate(90deg);
    transform-origin:100% ;
    transition: all 0.5s;
    transition-timing-function: cubic-bezier(0.42, 0, 0.11, 0.77);
}
```
