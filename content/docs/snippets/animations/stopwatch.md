# Stopwatch

The inspiration for this snippet is from the timer animation on Chess.com. It's basically a circle with a line in it that rotates 360 degrees in 4 steps of 90 degrees clockwise. 

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