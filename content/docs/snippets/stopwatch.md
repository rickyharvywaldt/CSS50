# Stopwatch

The inspiration for this snippet is from the timer animation on Chess.com. It's basically a circle with a line in it that rotates 360 degrees in 4 steps of 90 degrees clockwise. 

## CSS
```css
.clock {
  width: 20rem;
  height: 20rem;
  border-radius: 50%; 
  background-color: transparent;
  border: 1rem solid var(--clr-main);
  position: relative;
  transform: rotate(180deg);
}

.hand {
  position: absolute;
  top: 50%;
  left: calc(50% - 1rem / 2);
  width: 1rem;
  height: 7rem;
  background-color: var(--clr-main);
  border-radius: 1rem;
  animation: rotate steps(4) 4s infinite;
  transform-origin: center 0;
}

@keyframes rotate {
  from {
    transform: rotate(0);
  }
  to {
    transform: rotate(1turn);
  }
}
```