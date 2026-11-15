# Разработка LLM-приложений с LangGraph

Материалы курса для студентов ВИТШ КГУ о том, как строить приложения на основе больших языковых моделей: от первого HTTP-запроса к модели до агентов, которые сами вызывают инструменты.

Курс построен по принципу «снизу вверх». Сначала мы разбираемся, что происходит под капотом, и пишем всё руками на чистом Python и `requests`. Затем подключаем фреймворки, когда уже понятно, какую проблему они решают. Каждое занятие включает презентацию и Jupyter-ноутбук с практикой.

## Требования к подготовке

- Уверенная работа с компьютером: установка программ, работа с файлами и терминалом.
- Опыт программирования не обязателен: основы Python разбираем на втором занятии.

## Программа

| Занятие | Тема | Материалы |
|---|---|---|
| [Занятие 1](lesson_1/) | Какие задачи решает ИИ: обзор возможностей и сценариев применения | презентация, [видео](https://vimeo.com/1238843571) |
| [Занятие 2](lesson_2/) | Python с нуля до запроса к LLM: основы языка, классический NLP (pymorphy3, Natasha, TF-IDF), первый запрос к модели через API | презентация, ноутбук, [видео](https://vimeo.com/1238836667) |
| [Занятие 3](lesson_3/) | От обёртки к агенту: системный промпт, история диалога, prompt-инъекции и защита, наивный RAG, tool calling вручную и анонс LangGraph | презентация, ноутбуки (GigaChat и AITunnel), [видео](https://vimeo.com/1246963521) |
| [Занятие 4](lesson_4/) | Управление потоком исполнения: маршрутизация через if-else, явный граф (свой мини-движок на networkx), checkpointer и подтверждение человеком, ReAct-цикл и выбор архитектуры | презентация, ноутбуки (GigaChat и AITunnel) |

*Программа будет пополняться по мере выхода новых занятий.*

## Открыть в Colab

Ноутбуки открываются в Google Colab прямо из репозитория. Чтобы сохранить свои изменения, выберите в Colab «Файл → Сохранить копию на Диске».

| Занятие | Ноутбук | |
|---|---|---|
| Занятие 2 | Практика Python (OpenRouter) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chernyatiev/llm_apps_course/blob/main/lesson_2/%D0%9F%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B0_Python.ipynb) |
| Занятие 3 | От обёртки к агенту — GigaChat | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chernyatiev/llm_apps_course/blob/main/lesson_3/llm_evolution_gigachat.ipynb) |
| Занятие 3 | От обёртки к агенту — AITunnel | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chernyatiev/llm_apps_course/blob/main/lesson_3/llm_evolution_aitunnel.ipynb) |
| Занятие 4 | Управление потоком исполнения — GigaChat | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chernyatiev/llm_apps_course/blob/main/lesson_4/flow_control_gigachat.ipynb) |
| Занятие 4 | Управление потоком исполнения — AITunnel | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/chernyatiev/llm_apps_course/blob/main/lesson_4/flow_control_aitunnel.ipynb) |

## Как работать с материалами

1. Клонируйте репозиторий:
   ```bash
   git clone https://github.com/chernyatiev/llm_apps_course.git
   ```
2. Откройте ноутбуки в Jupyter, VS Code или Google Colab.
3. Для запросов к моделям понадобится доступ к API. Ноутбуки третьего и четвёртого занятий есть в двух вариантах:
   - **GigaChat** (бесплатный тариф Freemium);
   - **AITunnel** (агрегатор с доступом к разным моделям).

   Ключ API храните в переменных окружения или секретах Colab. Не коммитьте его в репозиторий.
