# a-a_test_simulation
А/А-тестирование мобильного приложения. Необходимо посчитать результаты A/A-теста, проверяя метрику качества FPR (будем проверять на конверсии в покупку). Известно, что сплит-система сломана. Требуется проверить утверждение о поломке и найти ее причины, если сплит-система действительно сломана

# Выводы
Мы посчитали конверсию, группируя по варианту и версии мобильного приложения и выяснили, что почему-то в 0-варианте нашего а/а теста конверсия в покупку около нуля на v2.8.0 версии приложения. На 1-варианте, конечно, тоже пониже конверсия, чем на других версиях, но все же не ноль. К тому же мы видим, что покупок в v2.8.0 версии приложения на 1-варианте сильно больше. При этом увидели, что трафика ушло на все версии примерно одинаковое количество. 
Посчитали pvalue для каждой версии МП с помощью критерия Манна-Уитни. Действительно, для версии v2.8.0 нашего приложения есть значимая разница между распределениями. Без этой версии а/а тест сошелся
