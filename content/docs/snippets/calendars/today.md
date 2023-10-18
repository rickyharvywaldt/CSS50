# Today

Today is a simple and minimalistic calendar that focuses on a particular (to)day by eliminating all the date numbers except for 1 date. It also has different styles to distinguish weekdays from weekends.

The weekdays also has a pointer cursor indicating that these days can be clicked as opposed to the weekends. A possible use case could be to only highlight special days, for example days with appointments or tasks that can either be clicked or hovered to display more information.

Of course, JavaScript is needed to make the calendar dynamic.

{{< button href="https://codepen.io/rickywaldt/pen/BavXyMg" >}}View in CodePen{{< /button >}}
{{< button href="https://github.com/rickyharvywaldt/CSS50/blob/main/content/docs/snippets/calendars/today.md" >}}Contribute{{< /button >}}

## CSS

```css
.calendar {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.date {
  font-size: 16px;
}

.wrapper {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  justify-content: center;
  margin: auto;
  gap: 2px;
}

.day {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 15px;
  height: 15px;
  border: 1px solid #1479fc;
  border-radius: 5px;
  color: #fff;
  font-size: 10px;
  cursor: pointer;
}

.day:nth-child(7n + 6),
.day:nth-child(7n + 7) {
  border: 1px solid darkgrey;
  cursor: default;
}

.day:nth-child(19) {
  background-color: #1479fc;
  border: 1px solid #1479fc;
}

.day:nth-child(-n + 2),
.day:nth-child(n + 33) {
  border: none;
  cursor: default;
}
```
