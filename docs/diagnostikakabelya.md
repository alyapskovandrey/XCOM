# Диагностика кабеля

<blockquote bxstyle="margin: 0 0 0 40px; border: none; padding: 0px;">Метрика. Открытые линии</blockquote>

Работа с изображениями

<p></p><span st="" yle="color: var(--theme-color-main); font-size: 1.14286rem;"></span><ol><li bxstyle="text-align: left;"><br /></li></ol>

<span bxstyle="font-weight: bold;">Диагностика кабеля</span>

ИНСТРУКЦИЯ по Диагностике кабеля в коммутаторах DLINK DES-1228, DES-1210-28, DES-1210-52, DGS-3200

В боковом меню на странице веб интерфейса коммутатора нажимаем:
<br />
<br />1. Monitoring
<br />2. Cable Diagnostics
<br />3. Port (выбираем нужный порт)
<br />4. <span bxstyle="font-weight: bold;">Test Now</span><p><span st="" yle="font-family: var(--ui-font-family-primary,var(--ui-font-family-helvetica));"><br /></span></p><p><span st="" yle="font-family: var(--ui-font-family-primary,var(--ui-font-family-helvetica));">DGS-3120-24SC</span><br /></p><p>
<br />1. OAM
<br />2. Cable Diagnostics
<br />3. Port <span bxstyle="font-weight: bold;">(выбираем нужный порт)
</span><br />4. <span bxstyle="font-weight: bold;">TEST
</span><br />На коммутаторах DES-2108 и DES-2110 - отсутствует возможность проверить кабель<br /></p>

Прядок диагностики кабеля

<span bxstyle="color: rgb(183, 28, 28);">Чтобы проверить длину кабеля, обязательно попросите абонента отключить кабель от устройства!
</span><br /><span bxstyle="color: rgb(183, 28, 28);">Диагностику кабеля необходимо провести 2-жды: подключенным к устройству абонента и отсоединенным от него!</span>

<div class="landing-table-container landing-table-scroll-hidden" table-prepare="true" title="" title-added="true"><table class="landing-table landing-table-style-1" text-color="#333333"><tbody class="ui-draggable--container"><tr class="landing-table-tr"><th class="landing-table-th landing-table-th-select-all" bxstyle="width: 16px;" title="Выбрать всю таблицу"><div class="th-tech-icon"></div></th><th class="landing-table-th landing-table-col-dnd" bxstyle="width: 201px;"><div class="landing-table-div-col-dnd" title="Потяните для перемещения столбца"></div><div class="landing-table-col-resize" title="Потяните для изменения ширины столбца"></div><div class="landing-table-col-add" title="Добавить столбец"><div class="landing-table-col-add-line" bxstyle="height: 260.838px;"></div></div></th><th class="landing-table-th landing-table-col-dnd" bxstyle="width: 867.977px;"><div class="landing-table-div-col-dnd" title="Потяните для перемещения столбца"></div><div class="landing-table-col-resize" title="Потяните для изменения ширины столбца"></div><div class="landing-table-col-add" title="Добавить столбец"><div class="landing-table-col-add-line" bxstyle="height: 260.838px;"></div></div></th></tr><tr class="landing-table-tr"><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки"><div class="landing-table-row-add" title="Добавить строку"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">OK</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Исправное состояние кабеля</td></tr><tr class="landing-table-tr"><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки"><div class="landing-table-row-add" title="Добавить строку"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Short in Cable</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Короткое замыкание в кабеле</td></tr><tr class="landing-table-tr"><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки"><div class="landing-table-row-add" title="Добавить строку"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Open in Cable</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Кабель, подключенный к порту коммутатора, поврежден или не подключен на другой стороне</td></tr><tr class="landing-table-tr" bxstyle=""><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки"><div class="landing-table-row-add" title="Добавить строку"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Mismatched</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" title="Отредактировать текст" contenteditable="true">Возникли ошибки при диагностике кабеля, требуется перезапустить тест на том же порту</td></tr><tr class="landing-table-tr" bxstyle=""><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки" bxstyle="width: 16px;"><div class="landing-table-row-add" title="Добавить столбец"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" contenteditable="true">Line Driver</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" contenteditable="true">Обнаружено высокое электрическое сопротивление на другой стороне кабеля</td></tr><tr class="landing-table-tr" bxstyle=""><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки" bxstyle="width: 16px;"><div class="landing-table-row-add" title="Добавить столбец"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" contenteditable="true">Cable Fault Distance (meters</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" contenteditable="true">Расстояние от порта коммутатора до поврежденного участка (при длине кабеля менее 2 метров будет сообщение об отсутствии кабеля “No Cable” )</td></tr><tr class="landing-table-tr"><th class="landing-table-th landing-table-row-dnd" title="Потяните для перемещения строки" bxstyle="width: 16px;"><div class="landing-table-row-add" title="Добавить столбец"><div class="landing-table-row-add-line" bxstyle="width: 1091.86px;"></div></div><div class="landing-table-div-row-dnd"></div></th><td class="landing-table-th landing-table-td" bxstyle="width: 201px;color: rgb(51, 51, 51);" contenteditable="true">Cable Length (meter)</td><td class="landing-table-th landing-table-td" bxstyle="width: 867.977px;color: rgb(51, 51, 51);" contenteditable="true">При исправном кабеле (результат “OK”) отобразит общую длину подключенного к порту кабеля</td></tr></tbody></table></div>

С кабелем всё в порядке
<br />Коннектор абонента подключен
<br />к устройству и коммутатору

<p><br /></p>

Короткое замыкание

<p>НАРЯД: Кабель поврежден
<br />Дополнительная информация: Short in a cable 31<br /></p>

1. Поврежден коннектор - наряд
<br />2. Не подключен кабель в устройство (роутер) - засуньте епта!
<br />3. Подключение по локальной сети отключено - включите.
<br />4. Порт абонентского устройства поврежден - попробуйте очистить.
<br />Выслать наряд, только если удостоверились в
<br />работоспособности абонентского оборудования (Роутера или ПК и тд)

<p>НАРЯД: <span bxstyle="font-weight: bold;">Поврежден разъем у абонента</span><br /></p>

Высокое сопротивление

<p>НАРЯД: <span bxstyle="font-weight: bold;">Поврежден кабель у абонента
</span><br />Дополнительная информация: <span bxstyle="font-style: italic;">impedance mismatch 98</span><br /></p>

Кабель не подключён в порт коммутатора (либо не доткнут)

<p>НАРЯД: <span bxstyle="font-weight: bold;">Не подключен кабель в порт</span><br /></p>

Кабель поврежден на 31 метре
<br />измерение производилось с подключенным в компьютер кабелем

<p>НАРЯД:<span bxstyle="font-weight: bold;"> Поврежден кабель/разъем у абонента</span><br /></p>

Кабель поврежден на 31 метре
<br />измерение производилось с подключенным в компьютер кабелем

<p>НАРЯД: <span bxstyle="font-weight: bold;">Поврежден кабель/разъем у абонента</span><br /></p>

Кабель поврежден на 31 метре
<br />измерение производилось при отключенном от компьютера кабеле

<p>НАРЯД: <span bxstyle="font-weight: bold;">Поврежден кабель</span><br /></p>

Перекрёстные помехи

<p>НАРЯД: <span bxstyle="font-weight: bold;">Поврежден кабель</span><br /></p>

Обнаружено высокое электрическое сопротивление на другой стороне кабеля

<p>проблемы с устройством Абонента - требуется замена<br /></p>

<span bxstyle="font-weight: bold;">Маркетинг и SMM</span>
