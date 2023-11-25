### Добро пожаловать на кейс госкорпорации Росатом "ИИ оптимизирует производство атомного топлива"!
***
Описание датасета:
Датасет представляет из себя набор дискретных, не связанных между собой дней, в каждом из которых вам предстоит оптимизировать распределение т.н. "серий" по работающим в своем режиме печам. Общий формат дня представляет из себя json-файл следующего образца:
```
{
    "ovens": [          <--- Список доступных печей
        {
            "start_temp": 1220,  <--- Температура печи в 00-00 (начало дня)
            "working_temps": [   <--- Температуры, которые могут быть достигнуты в печи (полагая, что для смены 
                960,                    температуры достаточно 15 минут)
                1030,
                1190,
                1100,
                1230,
                1070,
                1110,
                1080,
                1240,
                1220
            ],
            "operations": [     <--- Операции, которые могут выполняться в этой печи
                "prokat",
                "kovka"
            ]
        },
        ...
    ],
    "series": [         <--- Список серий, запланированный на день
        {
            "temperature": 1080,   <--- Температура, которая должна быть достигнута для этой серии
            "operations": [         <--- Список последовательных операций, которые необходимо 
                {                               выполнить для этой серии (названия транслитом)
                    "name": "nagrev", 
                    "timing": 245   <--- Время выполнения в минутах
                },
                {
                    "name": "prokat",
                    "timing": 15
                }
            ]
        },
        ...
    ] 
```

***
##### Вашей задачей будет c помощью ИИ оптимизировать алгоритм загрузки и работы прессов и печей в производстве топлива из редких цветных металлов.

# ЖЕЛАЕМ УДАЧИ!




P.S. Не забудьте посетить экспертные сессии и не стесняйтесь задавать вопросы)