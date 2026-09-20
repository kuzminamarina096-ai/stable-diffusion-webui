# Резервная копия русской версии Stable Diffusion

Архив `stable-diffusion-russian-backup.zip` содержит исходники установленной версии AUTOMATIC1111, русский интерфейс, локальный перевод русских описаний и настройки для RealVisXL / RTX 5060 8 ГБ.

Это резервная копия программы, а не размещённый в интернете генератор. Модели, Python, библиотеки, фотографии, история запросов и пароли в архив не включены. Перемещение объектов мышкой пока не реализовано.

## Восстановление на Windows

1. Распакуйте архив в отдельную папку на диске с достаточным свободным местом (рекомендуется не менее 25 ГБ).
2. Установите Python 3.10 и Git, добавив их в PATH.
3. Скачайте [RealVisXL 5.0 FP16](https://huggingface.co/SG161222/RealVisXL_V5.0/resolve/main/RealVisXL_V5.0_fp16.safetensors) в `stable-diffusion-webui/models/Stable-diffusion`.
4. В папке распакованного архива выполните `python download-translator.py`. Переводчик останется рядом с папкой программы.
5. Запустите `Start-Russian-WebUI.cmd`. При первом запуске установятся библиотеки (несколько гигабайт).
6. Откройте локальный адрес, показанный в окне запуска; обычно это http://127.0.0.1:7860.

Русские описания переводятся на компьютере; перевод может искажать отдельные обороты. Эта конфигурация проверялась на RTX 5060: RealVisXL, 832×1216, 30 шагов, DPM++ SDE / Karras. На компьютере наблюдался сбой Python; его причина не установлена, последующая пробная генерация прошла успешно. Восстановление на чистой системе отдельно не проверено.

## Источники и лицензии

- AUTOMATIC1111: https://github.com/AUTOMATIC1111/stable-diffusion-webui — AGPL-3.0, текст лицензии внутри архива.
- Русская локализация: https://github.com/Northerner1/stable-diffusion-webui-localization-ru_RU и https://github.com/ProfaneServitor/stable-diffusion-webui-localization-ru_RU, дополнена для этой сборки.
- Переводчик: https://huggingface.co/Helsinki-NLP/opus-mt-ru-en — CC BY 4.0.
- RealVisXL: https://huggingface.co/SG161222/RealVisXL_V5.0 — условия модели доступны на её странице.

Исходный коммит: `1937682a20f7f0442311a1ede68f9f0cb480163b`.
