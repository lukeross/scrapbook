# [How to align input forms in HTML](https://stackoverflow.com/a/23741073)

The accepted answer (setting an explicit width in pixels) makes it hard to make
changes, and breaks when your users use a different font size. Using CSS
tables, on the other hand, works great:

```
form  { display: table;      }
p     { display: table-row;  }
label { display: table-cell; }
input { display: table-cell; }
```

```
<form>
  <p>
    <label for="a">Short label:</label>
    <input id="a" type="text">
  </p>
  <p>
    <label for="b">Very very very long label:</label>
    <input id="b" type="text">
  </p>
</form>
```
