<div align="center">

# ◈ Даня Абрамов

**Фотогалерея на основе Swiper.js**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Swiper](https://img.shields.io/badge/Swiper.js-v11-6332F6?style=flat-square&logo=swiper&logoColor=white)

</div>

---

## 📖 О проекте

Полноэкранная галерея изображений с навигацией. Слайды занимают весь экран, переключаются стрелками или клавиатурой. Тёмный фон, минималистичный UI.

---

## 📁 Структура проекта

```
danil/
├── index.html          ← разметка слайдера
├── script.js           ← инициализация Swiper
├── style.css           ← стили (fullscreen, тёмная тема)
├── reset3.css          ← сброс стилей
└── image/
    ├── В атаке.png
    ├── В ожидании.png
    ├── Атака провалена.png
    └── Успешно сходил в атаку.png
```

---

## 🚀 Запуск

Никаких зависимостей для установки — Swiper подключён через CDN.

Просто открой `index.html` в браузере.

---

## ⚙️ Как работает

### Зависимость — Swiper.js v11

Подключается через CDN:

```html
<!-- CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.css" />

<!-- JS -->
<script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-bundle.min.js"></script>
```

### Инициализация (`script.js`)

```js
const swiper = new Swiper('.swiper', {
  loop: true,        // бесконечная прокрутка
  speed: 500,        // скорость анимации (мс)
  keyboard: { enabled: true },  // управление стрелками клавиатуры
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
  },
  spaceBetween: 30,  // отступ между слайдами
})
```

---

## 🖼️ Слайды

| # | Описание |
|---|----------|
| 1 | В атаке |
| 2 | В ожидании |
| 3 | Атака провалена |
| 4 | Успешно сходил в атаку |

---

## 🎨 Дизайн

- **Фон:** чёрный `#060606`
- **Изображения:** `height: 100vh`, сохраняют пропорции через `object-fit: contain`
- **Кнопки навигации:** полупрозрачные круги с `backdrop-filter: blur`, плавное увеличение при наведении
- **Пагинация:** точки внизу экрана, активная точка увеличивается

---

## ⌨️ Управление

| Действие | Управление |
|----------|------------|
| Следующий слайд | `→` / кнопка `›` |
| Предыдущий слайд | `←` / кнопка `‹` |
| Пагинация | точки внизу экрана |