# Автонастройка коммутатора

<blockquote bxstyle="margin: 0 0 0 40px; border: none; padding: 0px;">Метрика. Открытые линии</blockquote>

Работа с изображениями

<p></p><span st="" yle="color: var(--theme-color-main); font-size: 1.14286rem;"></span><ol><li bxstyle="text-align: left;"><br /></li></ol>

<span bxstyle="font-weight: bold;">Автонастройка коммутатора</span>

Ошибки:

<p><span bxstyle="font-weight: bold;">Не совпадает мак на коммутаторе:</span><br /></p><p>SNMP маркер выдает значение <span bxstyle="font-weight: bold; color: rgb(245, 245, 245); background-color: rgb(129, 199, 132);">online</span> Содержимое Журнала настройки:<br /></p>START (11.05.2013 16:56:07) M4-D67A-[2108]
<br /><span bxstyle="color: rgb(183, 28, 28);">GetDeviceMAC...MAC not equal DataBase MAC 10:19:5B:52:DE:CD [1.3.6.1.4.1.171.10.61.2.11.13.0 => 00 19 5B 52 DE CD]</span><br />VLANResult=0<br />FilterResult=0<br />DeleteTask=1<br />DONE - 0 sec<p><br /></p><p>Решение: В данном случае правильным мак подчеркнут.
<br />Скопируйте его и перейдите в 'Изменение данных коммутатора.
<br />Этот MAC нужно внести в поле MAC-адрес, затем сохранить.<br /></p>

Коммутатор не отвечает:

<br />Автонастройка
<br />Настраивается 00:02
<br />Журнал настройки << Ошибка
<br />SNMP маркер выдает значение <span bxstyle="background-color: rgb(240, 98, 146); color: rgb(245, 245, 245); font-weight: bold;">offline
</span><br />Содержимое журнала настройки :<p><br /></p><p>START (11.05.2013 16:55:39) M1-BEREG-ARAKS-[2110]
<br /><span bxstyle="color: rgb(183, 28, 28);">GetDeviceMAC...Failed to get device MAC, ENoError [1.3.6.1.4.1.171.10.61.1.11.13.0 => - none -]</span><br />VLANResult=0<br />FilterResult=0<br />DeleteTask=0<br />DONE - 9 sec</p><p>Решение:
<br />IP адрес на коммутаторе не совпадает с IP в RS, выяснить когда была смена коммутатора, Вбить нужный IP в RS. Найти ответственного и дать ему по ушам.
<br />Очистить ARP
<br />Проверить правильно ли указана Модель* коммутатора
<br />1. Проверить Линк
<br />2. Замерить магистральный кабель
<br />3. Отключить/включить порт (Дернуть порт)
<br />4. Нет электричества (свое питание - коммутатор запитан от дома, на котором стоит )
<br />5. Направить ребят для устранения неполадки с коммутатором только после выполнения всех вышеописанных пунктов.<br /></p><p></p>

ENoError

SNMP маркер выдает значение  <span bxstyle="font-weight: bold; color: rgb(245, 245, 245); background-color: rgb(129, 199, 132);">online</span><br />Содержимое журнала настройки :<p>START (29.07.2014 18:31:08) M27-D76-[1210-28]
<br />
<br /><span bxstyle="color: rgb(183, 28, 28);">GetDeviceMAC...Ok (1C:AF:F7:E0:FF:11)
</span><br /><span bxstyle="color: rgb(183, 28, 28);">CheckLinks...Failed to get port operation status, ENoError [1.3.6.1.2.1.[1.3.6.1.2.1.2.2.1.8.1 => - none -]
</span><br /><span bxstyle="color: rgb(33, 33, 33);">All ports operation status is DOWN!
</span><br />VLANResult=0
<br />FilterResult=0
<br />DeleteTask=0
<br />
<br />
<br />DONE - 9 sec</p><p>ENoError - Exeption No "Error" (от англ. Исключение Нет "Ошибка") - да ХЗ, либо это означает что ошибка не обнаружена, либо ошибка не известна - то есть ошибка в получение имени ошибки.
<br />
<br />Решение: Грузануть коммутаторы по цепочке, скорее всего проблема на коммутаторе с недавно обновленной прошивкой, ан котором битые порты не заблокированы и создают ежесекундные трапы, что, в свою очередь, создает дополнительную нагрузку на процессор.
<br />После перезагрузки проверить автонастройку коммутатора.
<br />Возможно ранее этот коммутатор был настроен не корректно (завис, пропало соединение во время настройки и тп.)<br /></p>

Не совпадение модели коммутатора (ENoSuchName):

SNMP маркер выдает значение <span bxstyle="color: rgb(245, 245, 245); background-color: rgb(129, 199, 132); font-weight: bold;">online
</span><br />Содержимое журнала настройки :
<br />
<br />
<br />Содержимое журнала настройки :
<br />START (12.07.2014 17:26:29) M13-D49K-[1210-28]
<br /><span bxstyle="color: rgb(183, 28, 28);">GetDeviceMAC...Ok (1C:7E:E5:16:2D:58)
<br />CheckLinks...Failed to get port operation status, ENoSuchName [1.3.6.1.2.1.2.2.1.8.1 => ]
</span><br />All ports operation status is DOWN!
<br />VLANResult=0
<br />FilterResult=0
<br />DeleteTask=0
<br />
<br />
<br />DONE - 0 sec
<br />ENoSuchName - Exeption NO SUCH NAME (от англ. "Исключение НЕТ ТАКОГО ИМЕНИ") - не совпадает модель коммутатора.
<br />
<br />Решение: В RS выбрать нужную модель коммутатора

Не заливается мак адрес абонента:

Не заливается мак адрес абонента:
<br />Автонастройка
<br />Ожидает проверки 00:04
<br />Журнал настройки << Ошибка
<br />SNMP маркер выдает значение <span bxstyle="font-weight: bold; color: rgb(245, 245, 245); background-color: rgb(129, 199, 132);">online
</span><br />1. Содержимое журнала настройки :<p><br /></p><p>START (19.03.2014 20:11:04) M1-D4-[1210-52]
<br />GetDeviceMAC...Ok (AC:F1:DF:7F:D0:53)
<br />CheckLinks...Ok (111100011)
<br />GetAutoLearning...Ok (1)
<br />GetMACsList...Ok (8 MAC's)
<br />CheckStaticMAC(MAC=00:1E:8C:9F:D9:07, Port=1, VID=101)...Unchanged
<br />CheckStaticMAC(MAC=00:19:21:40:CB:F2, Port=2, VID=101)...Unchanged
<br />CheckStaticMAC(MAC=00:E0:52:93:B0:F8, Port=3, VID=101)...Unchanged
<br />CheckStaticMAC(MAC=6C:F0:49:77:1D:D0, Port=4, VID=101)...Unchanged
<br /><span bxstyle="color: rgb(183, 28, 28);">CheckStaticMAC(MAC=00:56:56:56:56:00, Port=5, VID=1010)...Failed to create StaticMAC, EBadValue [1.3.6.1.4.1.171.10.75.7.9.3.1.4.1010.0.86.86.86.86.0.5 => 34]
</span><br />CheckStaticMAC(MAC=8C:89:A5:CC:86:6B, Port=6, VID=101)...Unchanged
<br />CheckStaticMAC(MAC=E4:11:5B:3B:7A:9A, Port=7, VID=103)...Unchanged
<br />CheckStaticMAC(MAC=00:16:E6:5A:1A:12, Port=8, VID=102)...Unchanged
<br />CheckAutoLearningPorts(Mask=01111111111)...Unchanged
<br />SaveConfig...Ok
<br />VLANResult=1
<br />FilterResult=0
<br />DeleteTask=0
<br />
<br />
<br />DONE - 8 sec
<br />
<br />Решение:
<br />1. Внимательно прочитать выделенный текст ошибки.
<br />2. Обратить внимание на VID
<br />3. Проверить в какой группе находиться абонент
<br />4. Проверить правильно ли назначен IP-адрес
<br />5. Проверить залился ли коммутатор
<br />2. Содержимое журнала настройки :
<br />
<br />START (12.08.2014 13:41:41) M26-D1-[1210-28ME]
<br />GetDeviceMAC...Ok (28:10:7B:B3:F2:83)
<br />CheckLinks...Ok (0011000010001000001010100011)
<br />CheckVLAN(Members=0000000000000000000000000011, UnTagged=0000000000000000000000000011, VID=1, Name=default)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000011, UnTagged=0000000000000000000000000000, VID=2600, Name=switches26-1)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000011, UnTagged=0000000000000000000000000000, VID=2601, Name=users26-1)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000011, UnTagged=0000000000000000000000000000, VID=2602, Name=users26-2)...Unchanged
<br />CheckVLAN(Members=0000000000000000000010000011, UnTagged=0000000000000000000010000000, VID=2603, Name=users26-3)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000011, UnTagged=0000000000000000000000000000, VID=2604, Name=users26-4)...Unchanged
<br />CheckVLAN(Members=0010000010000000000000000011, UnTagged=0010000010000000000000000000, VID=2605, Name=users26-5)...Unchanged
<br />CheckVLAN(Members=0000000000000000001000000011, UnTagged=0000000000000000001000000000, VID=2606, Name=users26-6)...Unchanged
<br />CheckVLAN(Members=0000000000001000000000000011, UnTagged=0000000000001000000000000000, VID=2607, Name=users26-7)...Unchanged
<br />CheckVLAN(Members=0001000000000000000000000011, UnTagged=0001000000000000000000000000, VID=2608, Name=users26-8)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000011, UnTagged=0000000000000000000000000000, VID=2609, Name=users26-9)...Unchanged
<br />CheckVLAN(Members=1100111101110111110101111111, UnTagged=1100111101110111110101111100, VID=2610, Name=guests26)...Unchanged
<br />GetAutoLearning...Ok (1)
<br />GetMACsList...Ok (7 MAC's)
<br />CheckStaticMAC(MAC=D0:27:88:3D:4C:16, Port=1, VID=2610)...Unchanged
<br />CheckStaticMAC(MAC=A0:F3:C1:64:EE:17, Port=3, VID=2605)...Unchanged
<br /><span bxstyle="color: rgb(183, 28, 28);">CheckStaticMAC(MAC=CC:B2:55:96:55:5D, Port=4, VID=2608)...Failed to create StaticMAC, EGenErr [1.3.6.1.4.1.171.10.75.15.2.9.3.1.4.2608.204.178.85.150.85.93.4 => 34]
</span><br />CheckStaticMAC(MAC=A0:F3:C1:64:CF:65, Port=9, VID=2605)...Unchanged
<br />CheckStaticMAC(MAC=BC:5F:F4:4A:20:F4, Port=13, VID=2607)...Unchanged
<br />CheckStaticMAC(MAC=00:23:8B:E7:4D:04, Port=19, VID=2606)...Unchanged
<br />CheckStaticMAC(MAC=A0:F3:C1:44:84:DD, Port=21, VID=2603)...Unchanged
<br />CheckStaticMAC(MAC=F8:1A:67:FF:0E:FD, Port=23, VID=2610)...Unchanged
<br />CheckAutoLearningPorts(Mask=0100111101110111110101011111)...Unchanged
<br />CheckDHCPScreening(Mask=1111111111111111111111111100)...Unchanged
<br />VLANResult=1
<br />FilterResult=0
<br />DeleteTask=0
<br />DONE - 9 sec
<br />START (08.10.2014 21:16:46) M26-D11-[1210-28ME]
<br />GetDeviceMAC...Ok (28:10:7B:B3:E9:23)
<br />CheckLinks...Ok (1010000000001000001101100001)
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000001, VID=1, Name=default)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=2600, Name=switches26-1)...Unchanged
<br />CheckVLAN(Members=0000000010000000000000000001, UnTagged=0000000010000000000000000000, VID=2601, Name=users26-1)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=2602, Name=users26-2)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000100001, UnTagged=0000000000000000000000100000, VID=2603, Name=users26-3)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=2604, Name=users26-4)...Unchanged
<br />CheckVLAN(Members=0000001000000000000000000001, UnTagged=0000001000000000000000000000, VID=2605, Name=users26-5)...Unchanged
<br />CheckVLAN(Members=0000000000000000001000000001, UnTagged=0000000000000000001000000000, VID=2606, Name=users26-6)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=2607, Name=users26-7)...Unchanged
<br />CheckVLAN(Members=1000000000000000000000000001, UnTagged=1000000000000000000000000000, VID=2608, Name=users26-8)...Unchanged
<br />CheckVLAN(Members=0010000000001000000001000001, UnTagged=0010000000001000000001000000, VID=2609, Name=users26-9)...Unchanged
<br />CheckVLAN(Members=0101110101110111110110011111, UnTagged=0101110101110111110110011110, VID=2610, Name=guests26)...Unchanged
<br />GetAutoLearning...Ok (1)
<br />GetMACsList...Ok (13 MAC's)
<br />CheckStaticMAC(MAC=00:1C:25:37:F7:08, Port=1, VID=2608)...Unchanged
<br />CheckStaticMAC(MAC=E8:9A:8F:EF:A1:E0, Port=2, VID=2610)...Unchanged
<br />CheckStaticMAC(MAC=00:01:6C:62:2D:0D, Port=3, VID=2609)...Unchanged
<br />CheckStaticMAC(MAC=D0:27:88:19:E6:F8, Port=4, VID=2610)...Unchanged
<br />CheckStaticMAC(MAC=00:1A:80:FB:A6:16, Port=7, VID=2605)...Unchanged
<br />CheckStaticMAC(MAC=1C:75:08:58:D0:C4, Port=9, VID=2601)...Unchanged
<br />CheckStaticMAC(MAC=00:19:03:05:35:09, Port=10, VID=2610)...Unchanged
<br /><span bxstyle="color: rgb(183, 28, 28);">CheckStaticMAC(MAC=E8:94:F6:54:2B:B9, Port=13, VID=2609)...Failed to create StaticMAC, EGenErr [1.3.6.1.4.1.171.10.75.15.2.9.3.1.4.2609.232.148.246.84.43.185.13 => 34]
</span><br />CheckStaticMAC(MAC=D4:3D:7E:B8:32:2F, Port=19, VID=2606)...Unchanged
<br />CheckStaticMAC(MAC=00:89:84:6B:BF:00, Port=20, VID=2610)...Unchanged
<br />CheckStaticMAC(MAC=00:17:31:6B:20:4A, Port=21, VID=2610)...Unchanged
<br />CheckStaticMAC(MAC=54:04:A6:38:FD:7F, Port=22, VID=2609)...Unchanged
<br />CheckStaticMAC(MAC=64:70:02:D8:BB:E1, Port=23, VID=2603)...Unchanged
<br />CheckStaticMAC(MAC=DC:0E:A1:9E:1A:2A, Port=24, VID=2610)...Unchanged
<br />CheckAutoLearningPorts(Mask=0000110100110111110000001111)...Unchanged
<br /><span bxstyle="color: rgb(183, 28, 28);">CheckDHCPScreeningFailed to get DHCP Screening, ENoError [1.3.6.1.4.1.171.10.75.15.2.14.7.1.0 => - none -]
</span><br />VLANResult=1
<br />FilterResult=0
<br />DeleteTask=0
<br />DONE - 55 sec
<br />Решение: Сменить MAC-адрес абонента<br /></p><p></p>

Терминология

Чтение Журнала автонастройки
<br />
<br />START (07.02.2014 13:56:40) M17-DUKATx1-[1228]
<br />GetDeviceMAC...Ok (00:21:91:F1:DB:E8)
<br />CheckLinks...Ok (0000101110001000000000000001)
<br />GetVLANMode...Ok (1)
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000001, VID=1, Name=default)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=1700, Name=switches17-1)...Unchanged
<br />CheckVLAN(Members=1000000010000000000000000001, UnTagged=1000000010000000000000000000, VID=1701, Name=users17-1)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=1702, Name=users17-2)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=1703, Name=users17-3)...Unchanged
<br />CheckVLAN(Members=0000101000000000000000000001, UnTagged=0000101000000000000000000000, VID=1704, Name=users17-4)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=1705, Name=users17-5)...Unchanged
<br />CheckVLAN(Members=0000000100001000000000000001, UnTagged=0000000100001000000000000000, VID=1706, Name=users17-6)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=1707, Name=users17-7)...Unchanged
<br />CheckVLAN(Members=0000000000000000000000000001, UnTagged=0000000000000000000000000000, VID=1708, Name=users17-8)...Unchanged
<br />CheckVLAN(Members=0000000001000000000000000001, UnTagged=0000000001000000000000000000, VID=1709, Name=users17-9)...Unchanged
<br />CheckVLAN(Members=0111010000110111111111111111, UnTagged=0111010000110111111111111110, VID=1710, Name=guests17)...Unchanged
<br />GetAutoLearning...Ok (1)
<br />GetMACsList...Ok (10 MAC's)
<br />CheckStaticMAC(MAC=00:26:9E:77:48:6E, Port=1, VID=1701)...Unchanged
<br />CheckStaticMAC(MAC=1C:AF:F7:16:B6:F3, Port=4, VID=1710)...Unchanged
<br />CheckStaticMAC(MAC=90:F6:52:5A:EB:B7, Port=5, VID=1704)...Unchanged
<br />CheckStaticMAC(MAC=90:FB:A6:65:C4:DF, Port=6, VID=1710)...Unchanged
<br />CheckStaticMAC(MAC=40:4A:03:D6:5C:37, Port=7, VID=1704)...Unchanged
<br />CheckStaticMAC(MAC=90:E6:BA:F0:DC:DA, Port=8, VID=1706)...Unchanged
<br />CheckStaticMAC(MAC=00:1D:7D:E7:0F:6D, Port=9, VID=1701)...Unchanged
<br />CheckStaticMAC(MAC=00:13:77:94:86:20, Port=10, VID=1709)...Unchanged
<br />CheckStaticMAC(MAC=00:1B:22:01:70:31, Port=12, VID=1710)...Unchanged
<br />CheckStaticMAC(MAC=00:1F:D0:8A:A3:32, Port=13, VID=1706)...Unchanged
<br />CheckAutoLearningPorts(Mask=0110000000100111111111111111)...Unchanged
<br />VLANResult=1
<br />FilterResult=1
<br />DeleteTask=1
<br />DONE - 7 sec<p><br /></p><p>GetDeviceMAC - получение MAC адреса коммутатора, сопоставление его со значением в Базе Данных RS.
<br />CheckLinks - проверка линков на партах. 0 - линка нет, 1 линк есть.
<br />GetVLANMode - получение режима VLAN - устарело.
<br />CheckVLAN - проверка членства портов в определенной подсети VLAN, где
<br />
<br />VID - идентификатор подсети; Name - условное название подсети;
<br />UnTagged - не антегирован ли порт в этой VLAN;
<br />проверка изменений в списке данной VLAN, Unchanged - нет изменений, Сhanged - есть изменения.
<br />Список подсетей и значения IP адресов принадлежащих определенной подсети вы можете найти на странице Список подсетей IP-адресов в RS. Для этого просто выберите в фильтре нужную группу по микрорайонам.
<br />GetAutoLearning - проверка Автообучения абонентских портов по MAC адресу. где 0 - не включена, 1 - включена.
<br />
<br />Если AutoLerning включен, то коммутатор следит за за портами, в которых включена строгая фильтрация.
<br />GetMACsList - проверка списка статических мак адресов (количество записей)
<br />CheckStaticMAC - проверка статических значений MAC адресов на порте с указанием идентификатора подсети...изменен/не изменен. действительно ли мак адрес разрешен на порту. Если мак адрес клиента отличается от статического мак адреса, вписанного в БД коммутатора, то ни один пакет не пройдет через этот порт.
<br />CheckAutoLearningPorts - проверка портов , 0 - строгая фильтрация MAC адреса, 1 - фильтрация отключена.
<br />
<br />На всех гостевых портах фильтрация отключена.
<br />VLANResult - 1 настройка VLAN закончилась успехом, 0 закончилась с ошибкой.
<br />FilterResult - 1 Фильтрация портов завершилась успехом, 0 - закончилась с ошибкой.
<br />DeleteTask - 1 задача автонастройки будет удалена, 0 задача автонастройки сохраняется и коммутатор будет поставлен в очередь для повторной операции.
<br />
<br />Коммутаторы DES-2108 и DES-2110 полностью заливаются в среднем по 7 минут, модификация происходит в среднем за 3 минуты.<br /></p><p><br /></p><p>START (07.03.2018 11:35:35) M13-D10A-[2108]
<br />GetDeviceMAC...Ok (00:1B:11:50:A3:0B)
<br />CheckLinks...Ok (00000001)
<br />GetVLANMode...Ok (2)
<br />CheckVLAN(Members=11111111, UnTagged=00000001, VID=1, Name=default)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1300, Name=switches13-1)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1300)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1301, Name=users13-1)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1301)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1302, Name=users13-2)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1302)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1303, Name=users13-3)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1303)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1304, Name=users13-4)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1304)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1305, Name=users13-5)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1305)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1306, Name=users13-6)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1306)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1307, Name=users13-7)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1307)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1308, Name=users13-8)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1308)...Unchanged
<br />CheckVLAN(Members=00000001, UnTagged=00000000, VID=1309, Name=users13-9)...Unchanged
<br />CheckPVID(  Ports=00000000, VID=1309)...Unchanged
<br />CheckVLAN(Members=00111111, UnTagged=00111110, VID=1310, Name=guests13)...Unchanged
<br />CheckPVID(  Ports=00111110, VID=1310)...Unchanged
<br />GetAutoLearning...Ok (1)
<br />GetMACsList...Ok (0 MACs)
<br /><span bxstyle="color: rgb(183, 28, 28);">CheckAutoLearningPorts(Mask=00011111)...Failed set AutoLearning ports, EBadValue [1.3.6.1.4.1.171.10.61.2.21.2.0 => 1F 00 00 00]
</span><br />VLANResult=1
<br />FilterResult=0
<br />DeleteTask=0
<br />DONE - 7 sec<br /></p>

<span bxstyle="font-weight: bold;">Маркетинг и SMM</span>
