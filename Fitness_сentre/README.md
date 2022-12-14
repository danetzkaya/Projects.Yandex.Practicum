# Прогноз оттока посетителей сети фитнес-центров

Проект завершен.

## Данные

В наличии были данные, которые содержат информацию за месяц до оттока и факт оттока на определённый месяц.
- Данные клиента за предыдущий до проверки факта оттока месяц:
    - пол
    - проживание или работа в районе, где находится фитнес-центр
    - сотрудник компании-партнёра клуба (сотрудничество с компаниями, чьи сотрудники могут получать скидки на абонемент — в таком случае фитнес-центр хранит информацию о работодателе клиента)
    - факт первоначальной записи в рамках акции «приведи друга» (использовал промо-код от знакомого при оплате первого абонемента)
    - наличие контактного телефона
    - возраст
    - время с момента первого обращения в фитнес-центр (в месяцах)
- Информация на основе журнала посещений, покупок и информация о текущем статусе абонемента клиента:
    - длительность текущего действующего абонемента (месяц, 6 месяцев, год);
    - срок до окончания текущего действующего абонемента (в месяцах);
    - факт посещения групповых занятий;
    - средняя частота посещений в неделю за все время с начала действия абонемента;
    - средняя частота посещений в неделю за предыдущий месяц;
    - суммарная выручка от других услуг фитнес-центра: кафе, спорттовары, косметический и массажный салон.
    - факт оттока в текущем месяце.

## Задача

- научиться прогнозировать вероятность оттока (на уровне следующего месяца) для каждого клиента;
- сформировать типичные портреты клиентов: выделить несколько наиболее ярких групп и охарактеризовать их основные свойства;
- проанализировать основные признаки, наиболее сильно влияющие на отток;
- сформулировать основные выводы и разработать рекомендации по повышению качества работы с клиентами:   
    - выделить целевые группы клиентов;
    - предложить меры по снижению оттока;
    - определить другие особенности взаимодействия с клиентами.

## Используемые библиотеки

pandas, numpy, seaborn, matplotlib, sklearn, scipy, itertools


## Результаты: 

Больше всего клиентов попадает в отток, которые:

- Всего пару месяцев являются клиентами фитнес-центра;
- Покупают абонемент не более, чем на 2 месяца;
- Срок до окончания текущего действующего абонемента в районе одного месяца;
- Минимальное количество посещений (1-2 раза в неделю/месяц).

**Разделили клиентов по нескольким характеристикам на пять кластеров.** 

- Группа под номером 0 - это те клиенты, которые являются сотрудниками компании-партнёра клуба, и те, кто пришел по акции "приведи друга".
- Группа под номером 1 - это те клиенты, которые живут или работают далеко от фитнес центра.
- Группа под номером 2 - это новые клиенты, которые совсем недавно ходят в зал и приносят меньше всего выручки от допуслуг, а также имеют большой процент оттока.
- Группа под номером 3 - это те клиенты, которые чаще посещают зал в месяц и дольше всего по времени, группа клиентов, где меньше всего оттока.
- Группа под номером 4 - это те клиенты, которые не оставили свой номер телефона.
  
**Рекомендации для стратегии взаимодействия с клиентами и их удержания:**

- В отток часто попадают новые клиенты, которые приобрели абонемент всего на пару месяцев. Они редко бывают в фитнес-центре, не посещают групповые занятия, видимо стоит чем-то замотивировать данных клиентов, например, бонусным предложением о продлении абонемента или же интересными групповыми программами: мастер-класс от известного тренера;
- Фитнес-центр редко посещают те клиенты, которые не живут и не работают рядом, стоит задуматься об открытии нового филиала или, например, предусмотреть услугу такси при покупке допуслуг;
- Lifetime влияет на выручку от других услуг фитнес-центра, стоит обратить внимание, как удерживать постоянных клиентов, например, делать приятные скидки и слать рассылки с благодарностями, что они - ваши дорогие клиенты;
- Проверять наличие контактных данных, чтобы все клиенты фитнес-центра своевременно получали полезные рассылки и предложения.

