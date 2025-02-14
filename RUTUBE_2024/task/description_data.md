# Состав датасета:

## Файл `logs.csv` - логи просмотров за неделю. Содержат следующие поля:

1. event_timestamp – таймстемп события
2. video_id – уникальный ID видео
3. watchtime – время просмотра в секундах
4. region – регион расположения пользователя
5. city – город расположения пользователя
6. user_id – уникальный ID пользователя

## Файл `video_stat.csv` - содержит информацию и статистику по каждому видео из логов:

1. video_id – уникальный ID видео
2. v_pub_datetime – дата публикации видео на платформе. Момент, когда видео стало доступно на Rutube в публичном доступе
3. v_total_comments – количество комментариев под видео
4. v_year_views – полное число плеер стартов на видео
5. v_month_views – число плеер стартов на видео за последний месяц
6. v_week_views – число плеер стартов на видео за последнюю неделю
7. v_day_views – число плеер стартов на видео за последний день
8. v_likes – число положительных эмоций на видео в данный момент времени
9. v_dislikes – число отрицательных эмоций на видео в данный момент времени
10. v_duration – длительность видео
11. v_cr_click_like_7_days – конверсия плеер старта в положительную эмоцию за последние 7 дней
12. v_cr_click_dislike_7_days – конверсия плеер старта в отрицательную эмоцию за последние 7 дней
13. v_cr_click_vtop_7_days – конверсия плеер старта в нажатие «втоп» за последние 7 дней
14. v_cr_click_long_view_7_days – конверсия плеер старта в долгий просмотр за последние 7 дней
15. v_cr_click_comment_7_days – конверсия плеер старта в комментарий за последние 7 дней
16. v_cr_click_like_30_days – конверсия плеер старта в положительную эмоцию за последние 30 дней
17. v_cr_click_dislike_30_days – конверсия плеер старта в отрицательную эмоцию за последние 30 дней
18. v_cr_click_vtop_30_days – конверсия плеер старта в нажатие «втоп» за последние 30 дней
19. v_cr_click_long_view_30_days – конверсия плеер старта в долгий просмотр за последние 30 дней
20. v_cr_click_comment_30_days – конверсия плеер старта в комментарий за последние 30 дней
21. v_cr_click_like_1_days – конверсия плеер старта в положительную эмоцию за последний день
22. v_cr_click_dislike_1_days – конверсия плеер старта в отрицательную эмоцию за последний день
23. v_cr_click_vtop_1_days – конверсия плеер старта в нажатие «втоп» за последний день
24. v_cr_click_long_view_1_days – конверсия плеер старта в долгий просмотр за последний день
25. v_cr_click_comment_1_days – конверсия плеер старта в комментарий за последний день
26. title – заголовок видео
27. description – описание видео
28. v_avg_watchtime_1_day – средний watchtime на видео за 1 день
29. v_avg_watchtime_7_day – средний watchtime на видео за 7 дней
30. v_avg_watchtime_30_day – средний watchtime на видео за 30 дней
31. v_frac_avg_watchtime_1_day_duration – средний watchtime на видео за 1 день в секундах делить на длительность видео в секундах
32. v_frac_avg_watchtime_7_day_duration – средний watchtime на видео за 7 дней делить на длительность видео в секундах
33. v_frac_avg_watchtime_30_day_duration – средний watchtime на видео за 30 дней делить на длительность видео в секундах
34. v_category_popularity_percent_7_days – доля плеер стартов категории данного видео относительно всех плеер стартов за последние 7 дней
35. v_category_popularity_percent_30_days – доля плеер стартов категории данного видео относительно всех плеер стартов за последние 30 дней
36. v_long_views_1_days – число плеер стартов с последующим "долгим" просмотром за 1 день
37. v_long_views_7_days – число плеер стартов с последующим "долгим" просмотром за 7 дней
38. v_long_views_30_days – число плеер стартов с последующим "долгим" просмотром за 30 дней
39. author_id – ID автора видео
40. category_id – ID категории видео

## Определения:

1)	Долгий просмотр
	1. Если видео больше 5 минут, то долгим просмотром считается если  watchtime > 0.25 * duration
	2. Если видео меньше 5 минут, то долгим просмотром считается watchtime > 30 секунд
