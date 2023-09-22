# Stopwatch

The inspiration for this snippet comes from the timer animation on Chess.com. The code is not for the timer countdown, just for the stopwatch/clock animation. It's basically a circle with a line in it that rotates 360 degrees in 4 steps of 90 degrees clockwise. 

The steps() method divides the animation by whatever number you fill in between the parameters. In our case we want 1 turn or 360 degrees divided by 4 steps, so 1 step is 90 degrees. We've also set 1 turn equal to 4 seconds to get 1 step per second. 

{{< button href="https://codepen.io/rickywaldt/pen/zYyROYO" >}}View in CodePen{{< /button >}}
{{< button href="https://github.com/rickyharvywaldt/CSS50/blob/main/content/docs/snippets/animations/stopwatch.md" >}}Contribute{{< /button >}}

## CSS
```css
.clock {
  width: 200px;
  height: 200px;
  border-radius: 50%; 
  border: 10px solid #111;
  position: relative;
  transform: rotate(180deg);
}

.hand {
  position: absolute;
  top: 50%;
  left: calc(50% - 10px / 2);
  width: 10px;
  height: 70px;
  background-color: #111;
  border-radius: 10px;
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