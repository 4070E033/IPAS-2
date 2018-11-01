# IPAS-2

# 針對網路攻擊手法

實體層：線路搭接與線路私接

資料連接層：封包監聽與ARP Spoofing

網路層：Source Route、Smurf、Ping of Death

連接層：SYN Flood、DDoS及Session Hijacking

應用層：DNS Poisoning、Brute force Login、SQL Injection及Cross-Site Scripting

# 實體層

搭接線路進行訊號接聽

# 防護建議：機房、機櫃、線路室及管道間進行存取控管

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

# 網路層

藉由廣播封包封包塞爆受害者網路頻寬的阻斷服務攻擊

# 防護建議：

在防火牆或路由器上阻擋 Network/Broadcast IP的傳送

# 網路層 - Ping of Death

屬於一種阻斷服務攻擊，只要一個Ping封包就讓作業系統當機

攻擊手法：

一般正常的Ping封包大小為56位元(含IP標頭為84位元)

攻擊者故意傳送一個大小超過65536位元的Ping封包給受害者(IP協定允許封包大於65536)

受害作業系統無法處理大於65536位元的Ping封包，導致系統當機或重新開機

攻擊者的來源IP經常是偽冒的IP位

# 防護建議：

修補作業系統弱點

# 連線層 - SYN Flood

攻擊手法：

攻擊者傳送大量的TCP SYN請求封包到受害伺服器

受害伺服器為每一個連線請求分配系統記憶體資源，導致系統連線資源被耗用殆盡，正常的連線無法建立

大量惡意的TCP SYN封包，其來源IP通常也都是偽冒的，因此無法以封鎖來源IP阻擋攻擊

# 防護建議：

防火牆限制同來源IP的連線數量

請求ISP協助

# 連線層 - 分散式阻斷服務攻擊 (DDos) (一次多台電腦大規模攻擊)

攻擊手法：

攻擊者控制多部阻斷服務攻擊主機(DoS Agent)，對受害者發動大規模的阻斷服務攻擊

被攻擊的受害者為主要受害者，被控制的阻斷服務攻擊主機本身也是次要的受害者

其攻擊來源IP太多(數百至數千個)，通常很難透過防火牆封鎖來源IP

# 防護建議：

防火牆限制同一來源IP的連線數量

請求ISP協助



































