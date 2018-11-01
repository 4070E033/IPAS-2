# IPAS-2

# 針對網路攻擊手法

實體層：線路搭接與線路私接

資料連接層：封包監聽與ARP Spoofing

網路層：Source Route、Smurf、Ping of Death

連接層：SYN Flood、DDoS及Session Hijacking

應用層：DNS Poisoning、Brute force Login、SQL Injection及Cross-Site Scripting

# 實體層

搭接線路進行訊號接聽

防護建議：機房、機櫃、線路室及管道間進行存取控管

採用不同顏色區隔不同網段(安全區域)

定期的線路盤查

# 資料連接層

透過工具或軟體被動蒐集Collision Domain中的網路封包

# 資料連接層封包監聽

監聽工具：Sniffer, MailSnarf

URLSnarf, WebSpy

Tcpdump ,Windump

Wireshark(Ethereal)

Ettercap

NetIntercept

# 防護建議

採用加密連線

改用Switch

網路線路的實體存取控制，避免搭接或私接問題

# IP Spoofing與ARP Spoofin

IP Spoofing使用偽造的來源位址來傳送IP封包，可能會採用受信任來源的IP 位址來嘗試規避防火牆

ARP Spoofing是指攻擊者取得區域網路上的資料封包甚至篡改封包，可讓網路上特定電腦或所有電腦無法正常連線





























