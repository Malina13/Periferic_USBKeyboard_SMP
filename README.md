# Periferic_USB_SMP
 
În cadrul acestui proiect, am realizat un dispozitiv de tip HID (mai exact o tastatură), ce va completa automat o semnătură rapidă, ce poate fi folosită, de exemplu, pentru un email.

Drept componente pentru acest periferic am folosit o plăcută de dezvoltare Arduino UNO, un buton, un led cu o rezistență de 220 ohmi și partea de interfațare electrică cu conexiunea USB (2 diode Zener de 3.6V, 2 rezistente de 100 ohmi și o rezistență de 2K ohmi).

Liniile conexiunii USB Vcc și GND se interconectează la pinii 5V și GND ai plăcii Arduino asigurând alimentarea sistemului în modul de funcționare periferic USB de tip HID. De asemenea, ledul se aprinde în momentul în care sistemul este conectat la o sursă de curent.

Butonul este conectat la Pinul digital 12, iar atunci când plăcuța Arduino va primi semnalul LOW de la el, acesta va trimite prin USB, rând pe rând, fiecare caracter ca și când ar fi fost apăsat de pe tastatura laptopului. 

Conexiunea USB presupune ca linia D+ să fie legată printr-o rezistență de 100 ohmi la pinul digital 2, iar linia D- să fie legată printr-o rezistență de 100 ohmi la pinul digital 4 și printr-o rezistența de 2K ohmi la pinul digital 5. Ambele linii sunt legate prin câte o Dioda Zener la masă.

La apăsarea butonului, sistemul va trimite pe USB textul de semnătură, ca și cum ar fi fost tastat, asemenea unei cărți de vizită.