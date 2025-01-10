---
layout: default
title: "Обо мне"
permalink: /about/
---
<style>
/* Основные стили */
body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 0;
}

/* Шапка сайта */
header {
  padding: 20px 0;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1000;
}

header nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: flex-start;
  gap: 20px;
  padding-left: 20px;
}

header nav li {
  display: inline;
}

header nav a {
  text-decoration: none;
  font-weight: bold;
  font-size: 18px;
  padding: 12px 25px;
  border-radius: 5px;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

header nav a:hover {
  transform: scale(1.05);
}


/* Стили для блока "Обо мне" */
.about-me {
  display: flex;
  align-items: left;
  gap: 20px;
  margin: 20px;
  font-family: Arial, sans-serif;
  flex-wrap: wrap;
  justify-content: flex-start;
}

.about-me-img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
}

.about-me-header {
  font-size: 2rem;
  margin-bottom: 10px;
  font-weight: bold;
}

.about-me-text {
  max-width: 600px;
  line-height: 1.6;
  font-size: 18px;
  text-align: justify;
}

</style>

<div class="about-me">
  <div>
    <h2 class="about-me-header">Меня зовут Сафин Рамаз</h2>
    <p class="about-me-text">
      Я учусь в РГПУ им. А. И. Герцена на 4 курсе, в группе 4об_ИВТ-1/21.
      Специальность — «Информатика и вычислительная техника», профиль — «Технологии разработки программного обеспечения».
    </p>
  </div>
</div>

<img src="{{ site.baseurl }}/images/secondphoto.jpg" alt="Фотография на всю ширину" class="fullwidth-img">