# Смена MAC адреса

<blockquote bxstyle="margin: 0 0 0 40px; border: none; padding: 0px;">Метрика. Открытые линии</blockquote>

Работа с изображениями

<p></p><span st="" yle="color: var(--theme-color-main); font-size: 1.14286rem;"></span><ol><li bxstyle="text-align: left;"><br /></li></ol>

RS<br />Коммутатор<br />OLT<br />

Заходим на карточку абонента в RS и нажимаем <b>Изменить MAC-адрес</b>

<div align="left">В поле MAC адрес обязательно вырезаем MAC адрес и вставляем в раздел <b>Дополнительная информация</b>, <font color="#e57373">это необходимо для того что чтобы Вы не потеряли предыдущий MAC адрес.</font><i> </i><br /></div><div align="left">Новый MAC адрес вставляем в поле MAC адрес. <font color="#e57373">Нет необходимости добавлять двоеточии, RS сама добавит их. к примеру Вы пропишите MAC адрес</font> b04e263c0a9, <font color="#e57373">RS пропишет его как</font> B0:4E:26:3C:0A:A9</div><div align="left">Нажимаем <b>Сохранить изменения </b><br /></div>

<div align="left">На данной модели нет автонастройки, MAC адрес нужно прописывать вручную в коммутаторе</div><div align="left"><ul><li>Заходим в коммутаторе и логинимся. </li><li>Security > MAC address Table > Static MAC</li><li>Нажимаем Add MAC</li><li>Указываем нужный Port</li><li> В поле MAC-address вводим нужный MAC адрес, обязательно вводим через дефис, пример:<br /> 38-6B-1C-2A-F7-B6</li><li>В разделе VID указываем VLAN абонента. </li><li>Нажимаем Apply</li><li>Save<br /></li></ul></div>

<b>D-LINK - DES-1210-10</b>

<b>RS</b><br />

<b>OLT</b>

<div>Заходим на OLT, логинимся</div><div>EPON Interface Config > EPON Port MAC Bind > Detail <br /></div><div><font color="#e57373">epon0/7 - это LineSwitch-7 </font></div>

Нажимаем раздел NEW

<div>ONU ID - указываем порт абонента куда мы привязали учетную запись к LineSwitch <br /></div><div>MAC Address - вводим MAC адрес ONU, прописываем MAC адрес слитно либо через каждые 4 символа пишем точку, пример f8f08217987c или f8f0.8217.987c</div><div>Нажимаем Apply</div><div><font color="#e57373">Примечание: обязательно проверяем сохранился ли MAC адрес, так как на данной OLT может уже прописан тот же MAC адрес ONU у другого абонента, и его необходимо удалить, в противном случае MAC адрес не пропишется. Смотрите статью ниже. </font><br /></div>

Сохраняем конфигурации нажав <b>Save All</b><br /><font color="#e57373">Если не сохраним, то после перезагрузки OLT MAC адрес слетит и абонент останется без интернета. </font>

<b>Удалить MAC с OLT</b><br />

<div>Заходим на OLT в раздел Device Status > ONU Interface State <br /></div><div>В разделе Search: вводим нужный MAC адрес ONU и нажимаем Enter, <font color="#e57373">обазтельно нужно вводить через точки, пример: <font color="#212121">f8f0.8215.87bc</font></font></div><div><font color="#e57373"><font color="#212121">Находим нужный LineSwitch и порт. Пример: EPON0/5:8</font></font></div>

<div align="left">Кликаем EPON Interface Config > EPON Port MAC Bind проходим в нужный LineSwitch нажав на Detail в нашем случае это LineSwitch 5 </div><div align="left">В разделе  Search: вводим нужный MAC адрес ONU, нажимаем Enter, ставим галочку на порту и только потом <font color="#212121">нажимаем Delete</font></div><div align="left"><font color="#e57373">Примечание: Если не соблюдать данную последовательность, то Вы можете удалить MAC адрес у рандомного абонента в данном LineSwitch</font></div>

Смена MAC адреса

We are the
						<br /> best

В большинство коммутаторах имеется автонастройка, и MAC адрес сохраняется автоматически кроме модели <b>D-LINK - DES-1210-10</b>, на данной модели необходимо прописывать MAC адрес не только в RS но и в ручную в коммутаторе.

<span bxstyle="font-weight: bold;">Маркетинг и SMM</span>
