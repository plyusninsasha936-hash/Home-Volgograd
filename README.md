<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Каталог недвижимости - Верстка Bootstrap 5</title>
  <!-- Подключение Bootstrap 5 CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet" />
</head>
<body>

<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Недвижимость</a>
    <div class="collapse navbar-collapse">
      <ul class="navbar-nav me-auto">
        <li class="nav-item"><a class="nav-link" href="#auth">Вход / Регистрация</a></li>
        <li class="nav-item"><a class="nav-link" href="#profile">Профиль</a></li>
        <li class="nav-item"><a class="nav-link" href="#catalog">Каталог</a></li>
        <li class="nav-item"><a class="nav-link" href="#edit">Редактировать объект</a></li>
      </ul>
    </div>
  </div>
</nav>

<!-- Страница авторизации и регистрации -->
<section id="auth" class="container my-5">
  <h2 class="mb-4">Авторизация / Регистрация</h2>
  <form>
    <div class="mb-3">
      <label for="email" class="form-label">E-mail</label>
      <input type="email" class="form-control" id="email" placeholder="Введите e-mail" required>
    </div>
    <div class="mb-3">
      <label for="fullname" class="form-label">ФИО</label>
      <input type="text" class="form-control" id="fullname" placeholder="Введите полное имя" required>
    </div>
    <div class="mb-3">
      <label for="phone" class="form-label">Телефон</label>
      <input type="tel" class="form-control" id="phone" placeholder="Введите телефон" required>
    </div>
    <div class="mb-3">
      <label for="password" class="form-label">Пароль</label>
      <input type="password" class="form-control" id="password" placeholder="Введите пароль" required>
    </div>
    <button type="submit" class="btn btn-primary">Войти / Зарегистрироваться</button>
  </form>
</section>

<!-- Страница профиля пользователя -->
<section id="profile" class="container my-5">
  <h2>Профиль пользователя</h2>
  <form>
    <div class="mb-3">
      <label for="fullNameProfile" class="form-label">ФИО</label>
      <input type="text" class="form-control" id="fullNameProfile" value="Иван Иванов" required>
    </div>
    <div class="mb-3">
      <label for="emailProfile" class="form-label">E-mail</label>
      <input type="email" class="form-control" id="emailProfile" value="ivan@example.com" required>
    </div>
    <div class="mb-3">
      <label for="phoneProfile" class="form-label">Телефон</label>
      <input type="tel" class="form-control" id="phoneProfile" value="+7 900 123-45-67" required>
    </div>
    <div class="mb-3">
      <label for="newPassword" class="form-label">Новый пароль</label>
      <input type="password" class="form-control" id="newPassword" placeholder="Введите новый пароль">
    </div>
    <button type="submit" class="btn btn-success">Сохранить изменения</button>
  </form>
</section>

<!-- Страница каталога объектов -->
<section id="catalog" class="container my-5">
  <h2>Объекты недвижимости</h2>
  <div class="mb-4">
    <input type="text" class="form-control" placeholder="Поиск по названию или типу" id="search">
  </div>
  <div class="row g-3">
    <div class="col-md-4">
      <div class="card">
        <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Объект" />
        <div class="card-body">
          <h5 class="card-title">Квартира в центре</h5>
          <p class="card-text">Тип: квартира<br/>Цена: 5 млн<br/>Площадь: 80 кв.м<br/>Этаж: 5<br/>Статус: Продажа</p>
          <a href="#edit" class="btn btn-primary">Подробнее</a>
        </div>
      </div>
    </div>
    <div class="col-md-4">
      <div class="card">
        <img src="https://via.placeholder.com/300x180" class="card-img-top" alt="Объект" />
        <div class="card-body">
          <h5 class="card-title">Дом за городом</h5>
          <p class="card-text">Тип: дом<br/>Цена: 8 млн<br/>Площадь: 150 кв.м<br/>Этажей: 2<br/>Статус: Продажа</p>
          <a href="#edit" class="btn btn-primary">Подробнее</a>
        </div>
      </div>
    </div>
    <!-- Добавляйте новые карточки по аналогии -->
  </div>
</section>

<!-- Страница редактирования объекта -->
<section id="edit" class="container my-5">
  <h2>Редактировать объект</h2>
  <form>
    <div class="mb-3">
      <label for="title" class="form-label">Заголовок</label>
      <input type="text" class="form-control" id="title" placeholder="Введите название объекта" required>
    </div>
    <div class="mb-3">
      <label for="type" class="form-label">Тип объекта</label>
      <select class="form-select" id="type">
        <option>Квартира</option>
        <option>Дом</option>
        <option>Офис</option>
      </select>
    </div>
    <div class="mb-3">
      <label for="price" class="form-label">Цена</label>
      <input type="number" class="form-control" id="price" placeholder="Введите цену" required>
    </div>
    <div class="mb-3">
      <label for="area" class="form-label">Площадь (кв.м)</label>
      <input type="number" class="form-control" id="area" placeholder="Введите площадь" required>
    </div>
    <div class="mb-3">
      <label for="location" class="form-label">Местоположение</label>
      <input type="text" class="form-control" id="location" placeholder="Введите адрес" required>
    </div>
    <button type="submit" class="btn btn-primary">Сохранить</button>
  </form>
</section>

<!-- Подключение Bootstrap 5 JS с Popper -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>

</body>
</html>


Наш сайт предназначен для тех, кто ищет недвижимость мечты. Здесь вы найдете широкий выбор объектов для покупки, аренды или инвестирования. Мы предлагаем удобный интерфейс, интуитивно понятный поиск и подробную информацию обо всех предложениях.
