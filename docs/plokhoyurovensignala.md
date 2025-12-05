# Плохой уровень сигнала

<blockquote bxstyle="margin: 0 0 0 40px; border: none; padding: 0px;">Метрика. Открытые линии</blockquote>

Работа с изображениями

<p></p><span st="" yle="color: var(--theme-color-main); font-size: 1.14286rem;"></span><ol><li bxstyle="text-align: left;"><br /></li></ol>

<div align="left">Одна из причин по которой могут возникнуть проблемы с интернетом это - Плохой уровень сигнала. <br /><br />Проблема такого характера приводит к понижению скорости, дисконнектам и полной потери соединения.<br /></div>

Как узнать уровень сигнала абонента ?

Переходим в Управление на странице абонента.

Далее копируем Ip в пункте Ip address <br />

<p><br /></p>

<p><br /></p>

Для дальнейшей работы нам необходима утилита PuTTY <br />

Необходимо ввести IP в раздел Host name и выбрать пункт Other.<br /><br />Далее нажимаем Open.<br />

Проверка уровня сигнала через PuTTY

После того как мы нажали <span bxstyle="background-color: rgb(255, 249, 196);"><u><font color="#03a9f4">Open</font></u></span>, потребуются данные для входа:<br /><font color="#4caf50">Username - admin</font><br /><font color="#4caf50">Password - admin</font><font color="#81c784"> </font><br /><br />Далее активируем программу командой - <span bxstyle="background-color: rgb(255, 249, 196);"><u><font color="#03a9f4">ENABLE</font></u></span><br /><br />После активации вписываем команду для проверки сигнала определенного свича:<br /><font color="#03a9f4"><u><span bxstyle="background-color: rgb(245, 245, 245);"><font color="#03a9f4">show epon onu-ctc-optical-transceiver-diagnosis </font></span></u><font color="#03a9f4"><u><span bxstyle="background-color: rgb(245, 245, 245);"><font color="#03a9f4">interface</font></span></u><u><span bxstyle="background-color: rgb(245, 245, 245);"> <font color="#03a9f4">epon </font>0/</span></u></font></font>5 (в нашем случае Lineswitch №5)<br /><br />Порт к которому привязан абонент №6 <br />В списке находим нужный нам порт, в нашем случае epon0/5:6 (epon0/5 это LineSwitch, а цифра 6 это порт к которому привязан абонент)<br /><br />В списке мы видим что самый высокий уровень сигнала у нашего порта -30 , это и есть <font color="#f44336">ПЛОХОЙ/ВЫСОКИЙ</font> уровень сигнала.

После того как мы определили что уровень сигнала до абонента плохой, нам необходимо создать заявку на выезд наших специалистов.

<span bxstyle="font-weight: bold;">Маркетинг и SMM</span>

prod by DariQQ
