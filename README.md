# Responsive web tips
### For mobile buttons
```
nav a, button {
  min-height: 48px;
  min-width: 48px;
}
```
1. Tap targets should be bigger than the average finger. So, to ensure that all of your elements are at least that size, add min-height: 48px; and min-width: 48px; to every tappable element.  

1. Height and width alone can be a little dangerous because it won't allow the element to resize if the content inside of it is bigger than the container.  

