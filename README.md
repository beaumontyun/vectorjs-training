- Download WebServer for Chrome to create a local environment via Chrome's extension.

- Open console and right click "Control" and "Interactive", then select "store object as global variable".

- Assign each variable into its own name:
```
var control = temp1
```
```
var interactive = temp2
```

- Once done, you can manipulate the object:
```
control.x = 100
``` 
```
interactive.circle(100, 100, 50);
```

- Once a circle is created, a new variable will appear, assign this variable again as:
```
var circle = temp3
```

- If you want to move the circle as your mouse move the object, assign the circle to be dependant on the position of the object:
```
circle.addDependency(control);
```

```
circle.update = function() {
    circle.cx = control.x;
    circle.cy = control.y
};
```

- Now the circle will move with your mouse's movements.