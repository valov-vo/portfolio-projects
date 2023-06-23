
# Определение токсичных комментариев
## Библиотеки
pandas, numpy, torch, transformers, tqdm, sklearn, catboost
## Описание
**Код подготовлен для запуска с использованием CUDA**
Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 

Нужно обучить модель классифицировать комментарии на позитивные и негативные. В нашем распоряжении набор данных с разметкой о токсичности правок.

**Целевое значение метрики качества *F1* - не меньше 0.75**

Для выполнения проекта было решено применить модель *BERT*. 

**Важно:** ресурсов локальной машины было недостаточно для адекватной по времени работы, поэтому часть кода, формирующей эмбендинги была запущена на компьютере однокурсника по Практикуму. Надеюсь на понимание ревьюера :-)

Ссылка на файл с эмбендингами, полученными на удаленном компьютере и использованными для обучения моделей: https://disk.yandex.ru/d/ZYc6VzeMnf4wxQ

**Статус проекта: закончен**

## Результат проекта
Для работы над проектом был получен датасет не требующий классической предобработки, связанной с заполнением пропусков. Из этой базы данных был взят столбец с комментариями, которые вдальнейшем были преобразованы в эмбендинги с помощью AutoModel и AutoTokenizer из библиотеки transformers, а также весами подгруженными из модели toxic-bert. Обучены несколько моделей и выбрана лучшая.