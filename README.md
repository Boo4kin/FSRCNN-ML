# FSRCNN for Image Super-Resolution

Учебный проект по восстановлению изображений с помощью архитектуры **Fast Super-Resolution Convolutional Neural Network (FSRCNN)**.

Реализация выполнена на TensorFlow / Keras. Модель обучается на изображениях DIV2K и увеличивает разрешение изображения в 4 раза.

## Что сделано

- реализована архитектура FSRCNN;
- подготовлен собственный пайплайн загрузки и аугментации данных;
- настроены обучение, валидация и сохранение весов;
- добавлены ReduceLROnPlateau и EarlyStopping;
- подготовлен ноутбук для inference и визуального сравнения результатов;
- проведено сравнение с bicubic interpolation.

## Результат

На тестовой выборке модель показала PSNR около **26.6 dB**.

Примеры восстановления доступны в папке `docs`.

## Стек

Python · TensorFlow · Keras · NumPy · Jupyter Notebook · DIV2K

## Структура

```text
.
├── train.py
├── config.yaml
├── Inference.ipynb
├── utils/
├── docs/
└── model1.h5
```

## Запуск обучения

Укажите путь к DIV2K в `config.yaml`, затем:

```bash
python train.py --config config.yaml
```

Проект выполнен в учебных целях.
