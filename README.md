Цель проекта - построить модель для предсказания стоимости машин на вторичном рынке. 

Заранее благодарю за ревью, основной вопрос, на который бы хотелось получить ответ: почему моя метрика MAPE ухудшилась, когда я попыталась больше предобработать данные? 

Первый и лучший результат (0.23) был получен, когда было совершено минимум усилий с моей стороны, а именно - я заполнила пропуски в категориальных данных "no_info", в числовых столбцах заполнила пропуски медианными значениями. Не кодировала категориальные переменные, сразу передала train CatBoost. Итого, MAPE 0.23.

![image](https://github.com/aiyrash-ku/Masterskaya_1/assets/132774506/9d34c108-2351-4813-a79e-fe3778b93e06)

Второй заход - я обработала дубликаты, перевела все слова в верхний регистр, вручную заменила дубликаты в make, body. После добавления  этих операций метрика MAPE ухудшилась, стало 0.25

Третий и худший заход: ко всему прочему добавила кодирование категориальных переменных TargetEncoder. Теперь метрика 1.1. В GitHub загружена эта версия тетрадки.
