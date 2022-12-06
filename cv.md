# Maxim Toroshscin

![Maxim Toroshscin](https://avatars.githubusercontent.com/u/29151316?v=2 'Avatar - Maxim Toroshscin')

#### Junior Frontend Developer

---

## Contact Information

**Phone**: +7 981 719 78 00

**E-mail**: maximiloi@gmail.com

[Telegram](https://t.me/maximiloi) | [Github](https://github.com/maximiloi) | [Codepen](https://codepen.io/maximiloi) | [HeadHunter](https://spb.hh.ru/resume/728f02fcff05c744230039ed1f636130386133)

---

## About Me

I develop responsive mobile-first websites (also with attention to semantic
layout) for more than 3 years. I have experience of commercial development as a
team member. I have excellent experience in HTML and CSS. I’m profound in
reading and fixing peers code. My current work includes integrating JQuery
plugins and also adapting vanilla JavaScript code on different projects. My
hobbies are collecting vinyl, playing and popularising flag-football in Saint
Petersburg.

---

## Skills

- HTML5, CSS3, Bem, SASS, SCSS, LESS
- Gulp
- Figma, Photoshop
- Git
- JavaScript (base)
- React (base)
- Php (base)
- PHPMailer
- Gulp
- Figma, Photoshop

---

## Work

- Freelancer (2018 - Present)

  Create and rework clients websites in order to improve loading speed and general usability. Create adaptive components for websites and applications. Tuning marketing campaigns for clients - getting more marketing leads by email, CRM and Telegram Accounts for clients. Setting up hosting, domain and website installations for clients.

---

## Education

#### Novgorod State University

- Institute of Agriculture and Natural Resources - Animal Science (1998 - 2003)

#### Additional Education

- HTML Academy profile

  - HTML и CSS, уровень 1 (2018)

  - HTML и CSS, уровень 2 (2018)

- ITgid

  - JavaScript v.2.0 (2020)

  - ООП в JavaScript (2020)

- Hexlet, Code-Basics

---

## Sample code

```
  document.addEventListener('click', function (e) {
  const targetItem = e.target;

  if (targetItem.closest('[data-ripple]')) {
    // Создание span элемента
    const button = targetItem.closest('[data-ripple]');
    const ripple = document.createElement('span');
    const diameter = Math.max(button.clientWidth, button.clientHeight);
    const radius = diameter / 2;

    ripple.style.width = ripple.style.height = `${diameter}px`;
    ripple.style.left = `${e.pageX - (button.getBoundingClientRect().left + scrollX) - radius}px`;
    ripple.style.top = `${e.pageY - (button.getBoundingClientRect().top + scrollY) - radius}px`;
    ripple.classList.add('button__ripple');

    //  Работа анимации один раз или постоянно
    button.dataset.ripple === 'once' && button.querySelector('.button__ripple') ? button.querySelector('.button__ripple').remove() : null;

    // Добавление span элемента на страницу
    button.appendChild(ripple);

    // Удаление span елемента
    const getAnimationDuration = () => {
      const animDuration = window.getComputedStyle(ripple).animationDuration;

      return animDuration.includes('ms') ? animDuration.replace('ms', '') : animDuration.replace('s', '') * 1000;
    };

    const timeOut = getAnimationDuration(ripple);

    setTimeout(() => {
      ripple ? ripple.remove() : null;
    }, timeOut);
  }

  // Работа с выпадающим меню
  if (!targetItem.closest('.select__item') && document.querySelector('.search-tour__title.open') && document.querySelector('.select__head.open')) {
    // По щелчку по любой области если открыто меню оно закрывается
    document.querySelector('.select__head.open').nextElementSibling.style.display = 'none';
    document.querySelector('.select__head.open').classList.remove('open');
  }

  if (targetItem.closest('.select__head')) {
    //  Открытие и закрытие меню по заголовку таблицы
    if (targetItem.classList.contains('open')) {
      targetItem.classList.remove('open');
      targetItem.parentNode.previousElementSibling.classList.remove('open');
      targetItem.nextElementSibling.style.display = 'none';
    } else {
      targetItem.classList.add('open');
      targetItem.parentNode.previousElementSibling.classList.add('open');
      targetItem.nextElementSibling.style.display = 'block';
    }
  }

  if (targetItem.closest('.select__item')) {
    // Перенос значения из выпадающего меню в заголовок
    targetItem.parentElement.previousElementSibling.classList.remove('open');
    targetItem.parentNode.parentNode.previousElementSibling.classList.remove('open');
    targetItem.parentElement.previousElementSibling.innerText = targetItem.innerText;
    targetItem.parentElement.style.display = 'none';
  }
});
```

---

## Languages

- Russian (native)
- Ukrainian (native)
- English (A2)
