# Drone Detection MVP 🚁
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-1.9+-red.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-In%20Development-yellow.svg)
> Акустическая детекция и классификация БПЛА по звуку винтомоторной группы.

## 📋 О проекте
Разрабатывается система обнаружения дронов на охраняемых объектах на основе анализа звука. Проект выполняется в рамках летней практики.

## 🎯 Цели
- Детекция наличия дрона по аудиозаписи (бинарная классификация)
- Классификация типа источника звука (в перспективе)
- Работа в условиях сложного фона (газонокосилка, дрель, вертолет)

## 📁 Структура репозитория
```
drone-detection-mvp/
├── data/
│ ├── raw/ # Исходные аудиофайлы
│ ├── processed/ # Мел-спектрограммы (.npy)
│ └── splits/ # CSV-файлы с разбивкой train/val/test
├── src/
│ ├── data_prep.py # Подготовка данных и аугментация
│ ├── train.py # Обучение модели
│ └── infer.py # Инференс на новых записях
├── notebooks/ # Jupyter для экспериментов
├── requirements.txt # Зависимости
└── README.md # Этот файл
```

## 🚀 Быстрый старт
```bash
# Установка зависимостей
pip install -r requirements.txt

# Скачивание датасета (инструкция будет позже)
python src/data_prep.py --download

# Обучение модели
python src/train.py --config configs/default.yaml

# Инференс на одном файле
python src/infer.py --audio path/to/recording.wav
```

## 📊 Метрики
* ROC-AUC
* PR-AUC

## 👥 Команда
```
Роль - Имя
Тимлид - Андрей
Data Engineer - Илья
Data Scientist - Артем
ML Engineer - Злата
QA/Analyst - Света
```

## 📄 Лицензия
MIT
