
# Команды в html

```
<html></html>
```
- Указывает программе просмотра страниц, что это HTML документ.

```
<head></head>
```
- Определяет место, где помещается различная информация не отображаемая в теле документа. Здесь располагается тег названия документа и теги для поисковых машин.

```
<body></body>
```
- Определяет видимую часть документа

```
<h1></h1>
```
- Создает заголовок

```
<a href="URL"></a>
```
- Создает гиперссылку на другие документы или часть текущего документа.

```
<li></li>
```
- Определяет каждый элемент списка и присваивает номер

```
<DOCKTYPE>
```
- Ключевое слово в коде HTML

```
<p></p>
```
- Представляет собой абзац

<bold>БАЗОВЫЙ СИНТАКСИС</bold>
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Страница на HTML</title>
</head>
<body>
  <h1>Моя первая страница</h1>
  <p>Описание моей первой страницы</p>
</body>
</html>
```
- Теги и их атрибуты пишутся строчными буквами.
Для значений атрибутов всегда используются двойные кавычки.
Для отступов у вложенных элементов используется табуляция

```
<body>
  <ul>
    <li>Один</li>
    <li>Два</li>
    <li>Три</li>
  </ul>
</body>
```
- Закрывающий слеш у одиночных тегов (<img>, <br> и другие) не ставится.
В остальных случаях (таких, как <body></body> или <ul></ul>) обязателен закрывающий тег.

```
<head>
  <meta charset="utf-8">
  <title>Заголовок страницы</title>
</head>
```
- Кодировка символов на странице всегда должна быть явно указана, чтобы обеспечить корректное отображение текста. В нашем случае нужно utf-8 кодировка.

```
<!DOCTYPE html>
<html lang="ru">
...
</html>
```
- Для элемента <html> в атрибуте lang должен указываться соответствующий язык документа.
Это нужно для правильной работы синтеза речи, для переводчиков и т.д.

```
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```
- Internet Explorer поддерживает специальный мета-тег, который указывает, в какой версии следует показать страницу. На данный момент целесообразно использовать так называемый Edge-мод.
Подробнее тут.

```
<!-- Правильно: стилевой файл подключён в секции head -->
<!DOCTYPE html>
<html lang="ru">
  <head>
    <link rel="stylesheet" href="main.css">
  </head>
  <body>…</body>
</html>
```
- Стилевые файлы с помощью <link> подключаются внутри <head>. Атрибут type не указывается. А вот атрибут rel - обязателен, иначе страница "не поймет", что вы подключили.

```
<a class="element element-big" id="element" href="/" data-name="element">Ссылка</a>

<input class="form-control" type="text" name="test">

<img class="pets-picture" src="cats.jpg" alt="Изображение котиков">
```
- Атрибут класса у HTML-элементов пишется первым. Это важно для идентичности написания кода. Так проще увидеть какой-либо class, id и т.д. Остальные атрибуты можно указывать в любом порядке, но желательно чтобы их порядок от элемента к элементу сохранялся.

```
<!-- disabled="disabled" необязательно -->
<input type="checkbox" required checked>

<input type="text" disabled>

<select>
<option value="1" selected>1</option>
</select>
```
- Для логических атрибутов (например, checked, disabled, required) значение не указывается, а сами атрибуты указываются последними и в единообразной последовательности во всём документе.

```
<!-- Правильно: элемент формы radio связан с подписью через идентификатор -->
<input type="radio" id="choose">
<label for="choose">Радио кнопка</label>

<!-- Правильно: элемент формы radio и подпись обёрнуты в label -->
<label>
  <input type="radio"> Радио кнопка
</label>

<!-- Неправильно: подпись не связана с элементом формы -->
<input type="radio" id="choose"> Радио кнопка
```
- Для улучшения взаимодействия пользователя с элементами форм, при нажатии на подпись поля, оно должно активироваться. Для этого элемент формы связывается с его описанием с помощью идентификатора и атрибута for тега <label>.

```
<!-- Правильно: атрибут alt задан -->
<img src="img/picture.png" alt="Картинка">

<!-- Неправильно: атрибут не задан -->
<img src="img/picture.png" alt="">
```
- Обязательно нужно указывать атрибут alt у тега img, чтобы было чем "заменить" непоявившееся по любой причине изображение.


                