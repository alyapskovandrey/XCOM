# Проверка уровня сигнала до ONU

<blockquote bxstyle="margin: 0 0 0 40px; border: none; padding: 0px;">Метрика. Открытые линии</blockquote>

Работа с изображениями

<p></p><span st="" yle="color: var(--theme-color-main); font-size: 1.14286rem;"></span><ol><li bxstyle="text-align: left;"><br /></li></ol>

Проверка уровня сигнала до ONU / ONT<br />

ONU использует технологию EPON (добавить ссылки)<br />ONT использует технологию GPON

<div>Проверки уровней сигналов происходит по разному, но используется одно приложение <b>PuTTY</b></div><div><b><br /></b></div><font color="#f44336"><b><font color="#f44336">Важно! Не путать ONU / ONT</font></b></font>

Как определить ONU или ONT?<br />

<div>Где используется ONU мы можем попасть в интерфейс OLT используя IP адрес</div><div>Где используется ONT в интерфейс можно попасть только через приложение PuTTY</div>

Проверка уровня сигнал ONU<br />

<ol><li>Открываем приложение <b>PuTTY</b> в поле <b>Host Name (or IP address)</b> вводим <b>IP OLT</b>, ставим галочку на <b>Other</b> и нажимаем <b>Open</b></li><li>Вводим дефолтный логин и пароль от <b>OLT</b></li><li>Логин: <b>admin</b></li><li>Пароль: <b>admin</b></li><li><b>enable</b></li><li><b>show epon onu-ctc-optical-transceiver-diagnosis interface epON 0/<font color="#f44336">3</font></b> <br /></li></ol><div>M17-D104-ASYLPARK/1/2-[LineSwitch-<b><font color="#f44336">3</font></b>]</div>

<br />

<b>Уровень сигнала чем ниже тем лучше. Допустимый сигнал до -28</b>

Проверка уровня сигнал ONT

<ol><li>Открываем приложение <b>PuTTY</b> в поле <b>Host Name (or IP address)</b> вводим <b>IP OLT</b>, ставим галочку на <b>Other</b> и нажимаем <b>Open</b></li><li>    Вводим логин и пароль от OLT</li><li>Логин: <b>operator</b></li><li>Пароль: <b>xcom11546</b></li><li><b>enable</b></li><li><b>config</b></li><li><b>interface gpon 0/<font color="#f44336">4</font></b></li><li><b>display ont optical-info <font color="#4caf50">2</font> all</b></li><li>2 раза <b>Enter</b></li></ol><br />M5-D4-[LineSwitch-<b><font color="#f44336">4</font></b>/2] - <b>interface gpon 0/<font color="#f44336">4</font></b><br />M5-D4-[LineSwitch-4/<b><font color="#4caf50">2</font></b>] - <b>display ont optical-info <font color="#4caf50">2</font> all</b>

<span bxstyle="font-weight: bold;">Маркетинг и SMM</span>
