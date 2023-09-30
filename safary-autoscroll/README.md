# Сафарі і Autoscroll

Коли елемент введення стає сфокусованим, iOS Safari намагається розмістити його в центрі шляхом прокручування, що призводить до таких неприємних кейсів


Основний вигляд проблеми

![img.png](img.png)

Методом спроб і помилок було знайдено рішення, як таке хендлити

```CSS
html {
    overflow-y: hidden;
}

.body {
    position: fixed;
    
    overflow-y: auto !important;
    
    width: 100%;
    
    height: 100%;

    z-index: 1;
}
```

Результат 

![img_1.png](img_1.png)