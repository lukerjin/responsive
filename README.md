# Responsive web tips

### Set Viewport
window.devicePixelRatio = physical pixels / device-independent pixels(dips)  
`<meta name="viewport" content="width=device-width, initial-scale=1.0">`


### For mobile buttons
```
nav a, button {
  min-height: 48px;
  min-width: 48px;
}

nav a {
  padding: 1.5em;
}
```
1. Tap targets should be bigger than the average finger. So, to ensure that all of your elements are at least that size, add min-height: 48px; and min-width: 48px; to every tappable element.  

1. Height and width alone can be a little dangerous because it won't allow the element to resize if the content inside of it is bigger than the container.  

### Box-sizing
```
header, nav, footer, section, article, div {
  box-sizing: border-box;
}
```

border-box tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width. This typically makes it much easier to size elements.

### Media Query
`<link ref="stylesheet" media="screen and (min-width: 500px) href="">`
> Many small files, but many http request
```
@media screen and (max-width: 500px) {

}
```

```  
@media screen and (min-width: 501px) and (max-width: 1000px){

}
```  

> Few big files, less http request

### Flex
1. By default, the flex direction is row, the flex items fit on a single line
```
.container {
  width: 100%;
  display: flex;
}

<div class="container">
  <div class="box dark_blue"></div>
  <div class="box light_blue"></div>
  <div class="box green"></div>
</div>
```
2. By adding flex-wrap: wrap; to the container element, tells the browser it is ok to wrap the elements inside to wrap to the next line.
```
.container {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
```
3. Change layout order
```
 @media screen and (min-width: 500px) {
      .dark_blue { order:3; }
      .light_blue { order:1; }
      .green { order:2; }
  }
```

### Priority Content
Start from small, Mobile -> Tablet -> Desktop. 

### Break Point
Pick break point from small to large  

### References
[DPR and Viewport](https://zhuanlan.zhihu.com/p/26131956)
