# Сафарі і висота картинки

```CSS
img {
    height: auto;
}
```

Браузер сафарі не масштабує висоту зображення пропорційно до розмірів, тому якщо потрібно підскавляти висоту зображення автоматично, то   
просто використайте рядок нижче

```CSS
img {
    object-fit: contain;
}
```

Якщо img має батьківський елемент, то можна використати 2 варіант

```HTML
<div class="image-container">
    <img class="image" src="img.png" />
</div>
```

```CSS
.image-container {
    display: flex;
}

.image {
    justify-self: flex-start;
}
```

[Стаття з рішеннями](https://stackoverflow.com/questions/10760243/safari-image-size-auto-height-css)
