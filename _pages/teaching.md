---
layout: page
permalink: /teaching/
title: teaching 
description: ALL IN RUSSIAN. Not teaching regular courses, but supervising a lot of students.
nav: true
years: [2020, 2019, 2018, 2017, 2016, 2015]
---

## Supervised students

### 2020

[PhD] __Закирзянов Илья Тимурович__.
Методы генерации детерминированных конечных автоматов с использованием сокращения пространства поиска при решении задачи выполнимости.

[MS] __Сушенцев Игорь Михайлович__. 
Поиск оптимального профиля многослойной диэлектрической антенны с использованием эволюционных алгоритмов.
Выпускная квалификационная работа магистра. 2020.
[Руководитель: Ульянцев В.И., научный консультант: Ладутенко К.С.]

[MS] __Павленко Артем Леонидович__.
Разработка эволюционных методов декомпозиции задач обращения криптографических функций с использованием статистических тестов и инкрементальных SAT-решателей.
Выпускная квалификационная работа магистра. 2020.
[Руководитель: Ульянцев В.И., научный консультант: Семенов А.А.]
[[thesis]]({{ site.baseurl }}/assets/thesis/2020-Pavlenko-thesis.pdf)
[[presentation]]({{ site.baseurl }}/assets/thesis/2020-Pavlenko-presentation.pdf)

[BS] __Глухов Евгений Дмитриевич__.
Разработка методов анализа записей матчей в многопользовательских играх от первого лица.
Выпускная квалификационная работа бакалавра. 2020.
[Руководитель: Ульянцев В.И.]
[[thesis]]({{ site.baseurl }}/assets/thesis/2020-Glukhov-thesis.pdf)
[[presentation]]({{ site.baseurl }}/assets/thesis/2020-Glukhov-presentation.pdf)

      
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  
  {% for entry in site.data.students %}{% if entry[1].year == y %}
    <p>
    {{ entry[1].student }}

    </p>
  {% endif %}{% endfor %}
  
{% endfor %}

  {% for entry in site.data.students %}
    {{ entry }}
    {{ entry[0] }} , {{ entry[1].year }}
  {% endfor %}
