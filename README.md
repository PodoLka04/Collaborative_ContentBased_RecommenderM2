# 🌐 Language / Язык

[🇬🇧 English](#english) | [🇷🇺 Русский](#russian)

---

## <a name="russian"></a> 

# Collaborative ContentBased Recommender (группа 9)

## 📌 О проекте

Финальный проект по курсу **"Технологии анализа данных"** (Майнор НИУ ВШЭ, 2 Семестр).

**Цель:** создание эффективных рекомендательных систем для фильмов, которые могут прогнозировать предпочтения пользователей.

**Методы:**
- Сетевой анализ (сообщества фильмов)
- Текстовый и сентимент-анализ (теги, тональность)
- Рекомендательные системы: Collaborative Filtering (IBCF) + Content-based

---

> ⚠️ **Важно:** исходные данные хранились на университетском сервере, доступ к которому в настоящее время отсутствует.  
> Поэтому **Rmd-код не может быть выполнен**, но результаты исследования сохранены в HTML-отчётах.

## 📁 Содержимое репозитория

### Групповая часть
| Файл | Описание |
|------|----------|
| `group_code.Rmd` | Исходный код  |
| `group_report.html` | HTML-отчёт с выводами |

### Индивидуальная часть
| Файл | Описание |
|------|----------|
| `individual_code.Rmd` | Исходный код |
| `individual_feedback.png` | Скриншот оценки и отзыва |
| `individual_report.html` | HTML-отчёт |
| `individual_task.png` | Скриншот задания |

---

## 👥 Групповая часть

**Оценка:** 8 / 10

**Что сделано:**
- Сетевой анализ (выделение сообществ фильмов)
- Текстовый анализ (топ-15 тегов, сентимент)
- Две рекомендательные системы (IBCF + Content-based)
- Примеры работы систем и формальные метрики (RMSE, MSE, MAE)

---

## 👤 Индивидуальная часть

**Студент:** Подолин Дмитрий 

**Задача:**  
> Добавить в content-based систему переменную "наличие популярных актеров", где популярными актерами считать топ-5 самых встречающихся в датасете. Сравнить предсказания на одних и тех же примерах в новой (с актерами) и старой (без актеров) системе.

**Топ-5 актёров (по частоте упоминаний):**
1. Jim Carrey
2. Kirsten Dunst
3. Brian Cox
4. Morgan Freeman
5. Gary Oldman

**Результат:**
- Система **без учёта актёров** рекомендует фильмы только по тегам
- Система **с учётом актёров** учитывает ещё и наличие популярных актёров
- На примере фильмов 1995 года результаты различаются, что подтверждает влияние добавленной переменной

**Пример работы:**
```r
user_favorite_movies <- c("Jumanji (1995)", "Sense and Sensibility (1995)", 
                          "Leaving Las Vegas (1995)", "Babe (1995)", 
                          "Seven (a.k.a. Se7en) (1995)")

# Без актёров: фильмы по тегам (без учёта актёрского состава)
# С актёрами: фильмы, где есть хотя бы один из топ-5 актёров

```
**Оценка:** 7.50 / 10.00

## 🚀 Как просмотреть
Групповая часть: group_part/group_report.html
Индивидуальная часть: individual_part/individual_report.html

## 🛠 Инструменты
R, dplyr, ggplot2, igraph, tidytext, recommenderlab, lsa, textstem

## 📌 Авторы
Группа 9 + Подолин Дмитрий 
НИУ ВШЭ, курс "Технологии анализа данных"

---

## <a name="english"></a>

# Collaborative ContentBased Recommender (Group 9)

## 📌 About the project

Final project for the **"Data Analysis Technologies"** course (HSE Minor, 2nd Semester).

**Goal:** creating effective movie recommendation systems that can predict user preferences.

**Methods:**
- Network analysis (movie communities)
- Text and sentiment analysis (tags, sentiment)
- Recommendation systems: Collaborative Filtering (IBCF) + Content-based

> ⚠️ **Important:** The original data was stored on a university server that is currently inaccessible.  
> Therefore, **the Rmd code cannot be executed**, but the research results are preserved in HTML reports.

## 📁 Repository contents

### Group part
| File | Description |
|------|-------------|
| `group_code.Rmd` | Source code |
| `group_report.html` | HTML report with findings |

### Individual part
| File | Description |
|------|-------------|
| `individual_code.Rmd` | Source code |
| `individual_feedback.png` | Screenshot of grade and feedback |
| `individual_report.html` | HTML report |
| `individual_task.png` | Screenshot of assignment |

## 👥 Group part

**Grade:** 8 / 10

**What was done:**
- Network analysis (identifying movie communities)
- Text analysis (top-15 tags, sentiment)
- Two recommendation systems (IBCF + Content-based)
- System examples and formal metrics (RMSE, MSE, MAE)

## 👤 Individual part

**Student:** Dmitrii Podolin

**Task:**  
> Add a "presence of popular actors" variable to the content-based system, where popular actors are defined as the top 5 most frequently occurring actors in the dataset. Compare predictions on the same examples in the new (with actors) and old (without actors) systems.

**Top 5 actors (by frequency):**
1. Jim Carrey
2. Kirsten Dunst
3. Brian Cox
4. Morgan Freeman
5. Gary Oldman

**Result:**
- The **without actors** system recommends movies only by tags
- The **with actors** system also considers the presence of popular actors
- Using 1995 movies as an example, the results differ, confirming the impact of the added variable

**Example:**
```r
user_favorite_movies <- c("Jumanji (1995)", "Sense and Sensibility (1995)", 
                          "Leaving Las Vegas (1995)", "Babe (1995)", 
                          "Seven (a.k.a. Se7en) (1995)")

# Without actors: movies by tags (ignoring cast)
# With actors: movies featuring at least one of the top 5 actors
```

## Grade: 7.50 / 10.00

---

## 🚀 How to view
Group part: group_part/group_report.html

Individual part: individual_part/individual_report.html

## 🛠 Tools
- R,
- dplyr
- ggplot2
- igraph
- tidytext
- recommenderlab
- lsa
- textstem

## 📌 Authors
Group 9 + Dmitrii Podolin
HSE University, "Data Analysis Technologies" course
