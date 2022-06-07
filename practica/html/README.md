# html exercises

In this exercises you will have to complete the missing html or remark what should we include. For example:

What is wrong with this HTML?

```html
<customtag>lorem ipsum dolor</customtab>
```

Answer: It is using a key that does not exists.

## Exercise 1

Add what is missing in our html `<head>` tag.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Document</title>
  </head>
</html>
```


## Exercise 2

This html is not semantic what could we do to improve it.

```html
<div class="main">
  <section class="section">
    <ol>
      <li class="list-item">List item</li>
      <li class="list-item">List item</li>
      <li class="list-item">List item</li>
      <li class="list-item">List item</li>
    </ol>
  </div>
  <div class="section">
    <form class="form">
      <label>description</label>
      <input type="text">
    </form>
  </section>
</div>
```

## Exercise 3

If we want to include two CSS files like `reset.css`, `main.css`, and one javascript file `app.js`. Where should we include it in this html?

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="main.css">
  <title>Document</title>

</head>
<body>
  
<script src="app.js"></script>
</body>

</html>

```

## Exercise 4

We need to improve this html form markup. This form will call and endpoint `/register` with the right method. We also have to include the correct input type and mark all fields as required.

```html
<form action="/register">
  <div>
    <label>name</label>
    <input required>
  </div>
  <div>
    <label>surname</label>
    <input required>
  </div>
  <div>
    <label>phone</label>
    <input required>
  </div>
  <div>
    <label>email</label>
    <input required>
  </div>
  <div>
    <label>password</label>
    <input required>
  </div>
  <input type="submit" value="register">
</form>

```
