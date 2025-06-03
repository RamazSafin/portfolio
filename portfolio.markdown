<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Портфолио</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
</head>
<body>
<style>
/* Основные стили */
body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 20px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  min-height: 100vh;
}

/* Шапка сайта */
header {
  padding: 20px 0;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1000;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
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
  color: white;
}

header nav a:hover {
  transform: scale(1.05);
  background: rgba(255, 255, 255, 0.2);
}

/* Контейнер для семестров */
.semesters-container {
  margin-top: 100px;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
}

/* Изначально скрываем списки дисциплин */
.discipline-list {
  display: none;
  list-style-type: none;
  margin: 10px 0 20px 0;
  padding: 20px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border-radius: 15px;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

/* Показываем список, если у него есть класс open */
.discipline-list.open {
  display: block;
  animation: slideDown 0.3s ease-out;
}

@keyframes slideDown {
  from {
    opacity: 0;
    transform: translateY(-10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.discipline-list li {
  padding: 8px 0;
  color: white;
  font-size: 16px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

.discipline-list li:last-child {
  border-bottom: none;
}

.discipline-list a {
  color: #ffd700;
  text-decoration: none;
  transition: color 0.3s ease;
}

.discipline-list a:hover {
  color: #fff;
  text-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
}

/* Кнопки */
.semester-btn {
  background: linear-gradient(135deg, #333 0%, #555 100%);
  color: #fff;
  font-size: 20px;
  padding: 20px;
  border: 2px solid rgba(255, 255, 255, 0.3);
  border-radius: 15px;
  cursor: pointer;
  transition: all 0.3s ease;
  text-align: center;
  display: block;
  width: 100%;
  margin-bottom: 10px;
  position: relative;
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
}

.semester-btn:hover {
  background: linear-gradient(135deg, #444 0%, #666 100%);
  transform: translateY(-2px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4);
  border-color: rgba(255, 255, 255, 0.5);
}

.semester-btn:focus {
  outline: none;
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
}

.semester-btn:active {
  transform: translateY(0);
}

/* Стили для семестров */
.semester {
  margin-bottom: 20px;
  position: relative;
}

/* Стили для тултипа */
.tooltip {
  position: absolute;
  background: rgba(0, 0, 0, 0.95);
  color: white;
  padding: 15px 20px;
  border-radius: 12px;
  font-size: 14px;
  line-height: 1.6;
  max-width: 400px;
  z-index: 1001;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
  opacity: 0;
  transform: scale(0.8);
  transition: all 0.3s ease;
  pointer-events: none;
  border: 1px solid rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(10px);
}

.tooltip.show {
  opacity: 1;
  transform: scale(1);
}

.tooltip::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  border: 10px solid transparent;
  border-top-color: rgba(0, 0, 0, 0.95);
}

/* Адаптивность */
@media (max-width: 768px) {
  .semester-btn {
    font-size: 18px;
    padding: 15px;
  }
  
  .tooltip {
    max-width: 280px;
    font-size: 13px;
    padding: 12px 16px;
  }
  
  .semesters-container {
    padding: 0 10px;
  }
}
</style>

<header>
  <nav>
    <ul>
      <li><a href="#portfolio">Портфолио</a></li>
      <li><a href="#about">О себе</a></li>
      <li><a href="#contact">Контакты</a></li>
    </ul>
  </nav>
</header>

<div class="semesters-container">
  <div class="semester">
    <button class="semester-btn" data-tooltip="На начальном этапе обучения формировалась база фундаментальных знаний. Изучались дисциплины, закладывающие основы математического, логического и технического мышления, а также развивались навыки академического письма и исследовательской деятельности.">Семестр 1</button>
    <ul class="discipline-list">
      <li>Модуль "Дискретные структуры". Дискретная математика для программистов</li>
      <li>Модуль "Информатика и физика для инженеров". Информатика</li>
      <li>Модуль "Информатика и физика для инженеров". Физика</li>
      <li>Модуль "Информационные технологии в математике и физике". Информационные технологии в математике</li>
      <li>Модуль "Информационные технологии в математике и физике". Основы компьютерной алгебры</li>
      <li>Модуль "Математика для инженеров". Линейная алгебра и теория матриц</li>
      <li>Модуль "Общекультурный мировоззренческий экономический". Безопасность жизнедеятельности</li>
      <li>Модуль "Общекультурный мировоззренческий экономический". Физическая культура и спорт</li>
      <li>Модуль "Общекультурный мировоззренческий экономический". Философия</li>
      <li>Модуль "Общекультурный мировоззренческий экономический". Экономика</li>
      <li>Первая помощь при заболеваниях и травмах</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Образовательный процесс был направлен на расширение теоретических знаний и формирование навыков анализа и решения прикладных задач. Акцент сделан на междисциплинарный подход и развитие алгоритмического мышления.">Семестр 2</button>
    <ul class="discipline-list">
      <li>Модуль "Дискретные структуры"</li>
      <li>Модуль "Информатика и физика для инженеров". Физика</li>
      <li>Модуль "Информационные технологии в математике и физике". Информационные технологии</li>
      <li>Модуль "Математика для инженеров". Аналитическая геометрия</li>
      <li>Модуль "Математика для инженеров". Линейная алгебра и теория матриц</li>
      <li>Модуль "Математика для инженеров". Математический анализ</li>
      <li><a href="https://drive.google.com/drive/folders/1Ab85ZhB8yPWytwndIkNJoFg71iTb69wg?usp=sharing" target="_blank">Модуль "Общекультурный мировоззренческий экономический". Иностранный язык (английский)</a></li>
      <li>Модуль "Общекультурный мировоззренческий экономический". История</li>
      <li>Программирование</li>
      <li>Физическая культура и спорт (элективная дисциплина)</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Продолжилось углубление в профильные дисциплины. Формировались компетенции в области моделирования, проектирования и системного анализа. Значительное внимание уделялось практической реализации теоретических концепций.">Семестр 3</button>
    <ul class="discipline-list">
      <li>Модуль "Информатика и физика для инженеров". Физика</li>
      <li>Модуль "Информационные технологии в математике и физике". Физика полупроводников</li>
      <li><a href="https://drive.google.com/drive/folders/1_XIg_-9ehoj7kbVlUtkgG_qZCruqn_VN?usp=sharing" target="_blank">Модуль "Технологии и методы вычислений". Анализ данных и основы Data science</a></li>
      <li><a href="https://drive.google.com/drive/folders/1w1VdbTrgnDUovlewEbVZEwzV2ySPeeXb?usp=sharing" target="_blank">Модуль "Технологии и методы вычислений". Вычислительная математика</a></li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Обучение сосредоточилось на освоении специализированных инструментов и технологий. Особое внимание уделялось работе в команде, проектной деятельности и применению полученных знаний в практических кейсах.">Семестр 4</button>
    <ul class="discipline-list">
      <li><a href="https://drive.google.com/drive/folders/1KqYW0EuAi2n5zcdYxtmTzGzP2tnxplIZ?usp=sharing" target="_blank">Модуль "Компьютерная графика и управление информацией". Базы данных</a></li>
      <li>Модуль "Математика для инженеров". Интегралы и дифференциальные уравнения</li>
      <li><a href="https://drive.google.com/drive/folders/1Ab85ZhB8yPWytwndIkNJoFg71iTb69wg?usp=sharing" target="_blank">Модуль "Общекультурный мировоззренческий экономический". Иностранный язык (английский)</a></li>
      <li>Модуль "Организация и архитектура ЭВМ". Вычислительная техника</li>
      <li>Модуль "Организация и архитектура ЭВМ". Операционные системы</li>
      <li>Модуль "Проектирование и разработка веб-решений"</li>
      <li><a href="https://drive.google.com/drive/folders/1_XIg_-9ehoj7kbVlUtkgG_qZCruqn_VN?usp=sharing" target="_blank">Модуль "Технологии и методы вычислений". Анализ данных и основы Data science</a></li>
      <li>Модуль "Технологии и методы вычислений". Технологии компьютерного моделирования</li>
      <li>Программирование</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Расширялись профессиональные компетенции за счёт комплексных дисциплин и прикладных курсов. Акцент был сделан на разработку, тестирование и оптимизацию решений, а также на формирование устойчивых навыков проектной деятельности.">Семестр 5</button>
    <ul class="discipline-list">
      <li>Модуль "Информационные ресурсы и средства профессиональной деятельности инженера". Пакеты прикладных программ для статистической обработки и анализа данных</li>
      <li>Модуль "Информационные технологии в управлении в IT-компании". IT-менеджмент</li>
      <li>Модуль "Информационные технологии в управлении в IT-компании". Основы бизнес-информатики</li>
      <li>Модуль "Информационные технологии". Информационные технологии в изучении иностранных языков</li>
      <li>Модуль "Компьютерная графика и управление информацией". Компьютерная графика</li>
      <li>Модуль "Компьютерная графика и управление информацией". Математические основы компьютерной графики</li>
      <li>Модуль "Организация и архитектура ЭВМ". Сети и телекоммуникации</li>
      <li>Программирование</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Значительная часть семестра была посвящена реализации индивидуальных и групповых проектов. Образовательный процесс обеспечивал интеграцию теоретических знаний с профессиональной практикой, укрепляя исследовательские и технические навыки.">Семестр 6</button>
    <ul class="discipline-list">
      <li>Модуль "Информационные ресурсы и средства профессиональной деятельности инженера". Математические основы глубокого обучения</li>
      <li>Модуль "Информационные технологии в управлении в IT-компании". Основы электронного управления</li>
      <li>Модуль "Информационные технологии". Основы корпоративного электронного обучения</li>
      <li>Модуль "Информационные технологии". Прикладные информационные технологии</li>
      <li>Модуль "Компьютерная графика и управление информацией". Инженерная графика</li>
      <li><a href="https://drive.google.com/drive/folders/1Ab85ZhB8yPWytwndIkNJoFg71iTb69wg?usp=sharing" target="_blank">Модуль "Общекультурный мировоззренческий экономический". Иностранный язык (английский)</a></li>
      <li>Модуль "Организация и архитектура ЭВМ". Защита информации</li>
      <li>Модуль "Организация и архитектура ЭВМ". Основы машинного обучения</li>
      <li>Модуль "Организация и архитектура ЭВМ". Техники и технологии визуализации данных</li>
      <li>Программирование</li>
      <li>Физическая культура и спорт (элективная дисциплина)</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Программа семестра была сосредоточена на углублённом изучении профильных дисциплин и подготовке к выпускной квалификационной работе. В рамках занятий особое внимание уделялось прикладным аспектам и междисциплинарным связям. Учебная нагрузка сочеталась с планированием будущих проектов и практической реализацией изученного материала.">Семестр 7</button>
    <ul class="discipline-list">
      <li>Модуль "Информационные ресурсы и средства профессиональной деятельности инженера". Организация электронной образовательной среды</li>
      <li>Модуль "Информационные ресурсы и средства профессиональной деятельности инженера". Управление программными проектами</li>
      <li>Модуль "Общекультурный мировоззренческий экономический". Иностранный язык (английский)</li>
      <li>Модуль "Информационные технологии в управлении в IT-компании". Управление проектами разработки программного обеспечения</li>
      <li>Модуль "Математика для инженеров". Обработка данных и статистика</li>
      <li>Модуль "Математика для инженеров". Теория графов и её применение</li>
      <li>Программирование</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Заключительный семестр ориентирован на завершение учебной траектории и оформление выпускной квалификационной работы. Учебный процесс включал систематизацию теоретических знаний, развитие аналитических навыков и выполнение требований, предусмотренных учебным планом.">Семестр 8</button>
    <ul class="discipline-list">
      <li>Модуль "Информационные ресурсы и средства профессиональной деятельности инженера". Мировые информационные ресурсы и цифровые библиотеки</li>
      <li>Модуль "Информационные ресурсы и средства профессиональной деятельности инженера". Социальные и профессиональные вопросы информатики и ИТ</li>
      <li>Модуль "Информационные технологии в управлении в IT-компании". IT-рекрутмент</li>
      <li>Модуль "Информационные технологии в управлении в IT-компании". Информационные технологии оценки персонала</li>
      <li>Модуль "Информационные технологии и системы"</li>
      <li>Модуль "Информационные технологии и системы". Математические методы для исследования сферы образования</li>
      <li>Модуль "Особенности профеcсиональной иноязычной коммуникации"</li>
      <li>Модуль "Учебно-исследовательский"</li>
      <li>Модуль "Учебно-исследовательский". Языки написания спецификаций</li>
    </ul>
  </div>

  <div class="semester">
    <button class="semester-btn" data-tooltip="Курсовые работы представляют практическое применение полученных знаний и навыков. Каждая работа демонстрирует углубленное изучение определенной области и способность к самостоятельному исследованию и анализу.">Курсовые работы</button>
    <ul class="discipline-list">
      <li><a href="https://docs.google.com/document/d/1TFB7TqZdEFkkUzL1rj_A81dB_XHum6FA/edit?usp=sharing&ouid=108516826124833879059&rtpof=true&sd=true" target="_blank">Вычислительный эксперимент по изучению законов идеального газа</a></li>
      <li><a href="https://docs.google.com/document/d/1W-F8l7CJ-AuVSWiCxvmiyA-25Y9cHSRp/edit" target="_blank">Компьютерное моделирование упругового тела</a></li>
      <li><a href="https://drive.google.com/drive/folders/1T7Aqjhe4q5axJP08q0KDe75FzJEjBHK0?usp=sharing" target="_blank">Исследование взаимосвязи между экономическим развитием и энергетической продукцией: корреляционный анализ</a></li>
      <li><a href="https://docs.google.com/document/d/1VAaOrHn4Kml_B7_E56xf3H8rR53WnVZr/edit?usp=sharing&ouid=108516826124833879059&rtpof=true&sd=true" target="_blank">Проектирование и разработка электронного портфолио по дисциплине "Основы корпоративного электронного обучения"</a></li>
    </ul>
  </div>
</div>

<script>
// Получаем все кнопки с классом .semester-btn
const semesterButtons = document.querySelectorAll('.semester-btn');
let currentTooltip = null;

// Функция для создания тултипа
function createTooltip(text) {
  const tooltip = document.createElement('div');
  tooltip.className = 'tooltip';
  tooltip.textContent = text;
  document.body.appendChild(tooltip);
  return tooltip;
}

// Функция для позиционирования тултипа
function positionTooltip(tooltip, button) {
  const buttonRect = button.getBoundingClientRect();
  const tooltipRect = tooltip.getBoundingClientRect();
  
  // Позиционируем тултип над кнопкой
  let left = buttonRect.left + (buttonRect.width / 2) - (tooltipRect.width / 2);
  let top = buttonRect.top - tooltipRect.height - 15;
  
  // Проверяем, не выходит ли тултип за пределы экрана
  const padding = 10;
  if (left < padding) {
    left = padding;
  } else if (left + tooltipRect.width > window.innerWidth - padding) {
    left = window.innerWidth - tooltipRect.width - padding;
  }
  
  if (top < padding) {
    // Если не помещается сверху, показываем снизу
    top = buttonRect.bottom + 15;
    tooltip.style.transform = 'translateY(0)';
    // Меняем направление стрелки
    tooltip.style.setProperty('--arrow-position', 'top');
  }
  
  tooltip.style.left = left + 'px';
  tooltip.style.top = top + 'px';
}

// Добавляем обработчики событий для каждой кнопки
semesterButtons.forEach(button => {
  // Клик для открытия/закрытия списка дисциплин
  button.addEventListener('click', function() {
    const disciplineList = this.nextElementSibling;
    disciplineList.classList.toggle('open');
  });
  
  // Наведение мыши для показа тултипа
  button.addEventListener('mouseenter', function() {
    const tooltipText = this.getAttribute('data-tooltip');
    if (!tooltipText) return;
    
    // Удаляем предыдущий тултип, если есть
    if (currentTooltip) {
      currentTooltip.remove();
    }
    
    // Создаем новый тултип
    currentTooltip = createTooltip(tooltipText);
    
    // Позиционируем тултип
    setTimeout(() => {
      positionTooltip(currentTooltip, this);
      currentTooltip.classList.add('show');
    }, 10);
  });
  
  // Убираем тултип при уходе мыши
  button.addEventListener('mouseleave', function() {
    if (currentTooltip) {
      currentTooltip.classList.remove('show');
      setTimeout(() => {
        if (currentTooltip) {
          currentTooltip.remove();
          currentTooltip = null;
        }
      }, 300);
    }
  });
});

// Убираем тултип при скролле
window.addEventListener('scroll', function() {
  if (currentTooltip) {
    currentTooltip.classList.remove('show');
    setTimeout(() => {
      if (currentTooltip) {
        currentTooltip.remove();
        currentTooltip = null;
      }
    }, 300);
  }
});

// Убираем тултип при изменении размера окна
window.addEventListener('resize', function() {
  if (currentTooltip) {
    currentTooltip.remove();
    currentTooltip = null;
  }
});
</script>

</body>
</html>
