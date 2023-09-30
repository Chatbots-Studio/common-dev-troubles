# Відключення можливості використовувати зуми на сторінці

Першим кроком варто добавити метатег viewport

```HTML
 <meta
      name="viewport"
      content="width=device-width, height=device-height, initial-scale=1, maximum-scale=1, user-scalable=no, shrink-to-fit=no, target-densitydpi=device-dpio, orientation=portrait"
    />
```

[Стаття про viewport](https://www.w3schools.com/css/css_rwd_viewport.asp)

minimal-scale - вказує мінімальний масштаб;

maximal-scale - встановлює максимальний масштаб;

user-scalable - вказує, чи може користувач керувати масштабом чи ні.

Якщо розмір шрифту input становить менше 16 пікселів, Safari на iOS зробить зум до введення, тому що він вважає цей розмір замалим і хоче, щоб ви бачили, що ви робите. Щоб обмежети це варто збільшити розмір шрифта хоча б до 16px

```CSS
@media screen and (max-width: 767px) {
    input[type="text"],
    input[type="number"],
    input[type="email"],
    input[type="tel"],
    input[type="password"] {
        font-size: 16px;
    }
}
```


Якщо поперднього рішення не достатньо, то можна добавити в стилі фрагмент нижче, який дозволяє юзеру переміщатись тільки по вісям X, Y

```CSS
:root {
    touch-action: pan-x pan-y;
    height: 100%
}
```

[Стаття про touch-action](https://developer.mozilla.org/ru/docs/Web/CSS/touch-action)

P.S якщо на сайті юзаються сторонні фрейми(оплата, супорт), то вплинути на їх стилі і обмежити зумування ми не можемо