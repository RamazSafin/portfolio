---
layout: default
title: Главная
---

# Добро пожаловать на моё портфолио!

Портфолио для программиста — это важный инструмент, который помогает показать работодателям, что ты умеешь. Даже если ты учишься в вузе, имея портфолио с реальными проектами, ты можешь продемонстрировать свои практические навыки. Это лучше, чем просто диплом, потому что показывает, что ты умеешь работать с реальными задачами и технологиями.

Кроме того, портфолио помогает отслеживать твой рост как специалиста — с каждым новым проектом ты показываешь, что развиваешься. Это также отличная мотивация: ты видишь результаты своей работы и понимаешь, что достиг большего.

Для студента портфолио — это шанс выделиться на фоне других кандидатов при поиске первой работы или стажировки. Работая над проектами для портфолио, ты получаешь практический опыт и учишься решать настоящие задачи, а это важно для дальнейшего карьерного роста.

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
  align-items: center;
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