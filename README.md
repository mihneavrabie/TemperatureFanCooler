                                                                          Vrabie Mihnea
![1](https://user-images.githubusercontent.com/57170170/171375690-6047ad08-5b67-43b5-94b2-deb55600529e.jpeg)
![2](https://user-images.githubusercontent.com/57170170/171375734-a9c6b63d-909f-4d77-a9ef-035f3dc14946.jpeg)


                                                                   Sisteme cu microprocesoare
                                                              Universitatea Politehnica din Bucuresti
                                                             Facultatea de Automatica si Calculatoare


Introducere:

Temperatura este un factor foarte important in diferite medii de lucru. Astfel de exemple relevante pot fi camere de servere, industria alimentara, hoteluri, etc. Proiectul pe care am ales sa il construiesc este o solutie minimala la problema mentierii automata a unei temperaturi optime, aleasa de proiectant si poate sta la baza intelegerii controlului temperaturii unei incaperi. Evident pentru inceput proiectul este unul destul de simplist insa pe parcurs sau in viitor se poate imbunatati foarte mult.

Proiectarea:

Vom construi un ansamblu in care legam un FAN (ventilator) la o placuta Arduino care va functiona la viteze diferite in functie de temperature detectata de un sensor de temperature si umiditate. Pentru practicalitate, eficienta si cost am ales sa folosesc senzorul DHT11. Exist, evident multe alte alternative ce pot fi utilizate (termorezistete sau senzori contactless de temperature). Problema intalnita in timpul documentarii si informarii (research)  a fost ca senzorii contactless tind sa aiba un pret ridicat iar termorezistentele nu sunt atat de practice deoarece necesita contact direct cu o suprafata. Toate aceste aspecte au dus la alegerea senzorului DHT11.

Rezultatul final (proiectul) va avea ca functionaliate de baza modificarea vitezei ventilatorului intr-o incapere in functie de cat de ridicata este temperature inregstrata de senzor. O alta aplicabilitate va fi aceea de a afisa atat temperature, umiditatea cat si viteza fan-ului. Pentru afisaj am ales sa folosesc un Display LCD. Totodata voi avea nevoie de o placa Arduino UNO rezistente, etc. Am ales ca pe parcurs in functie de progres si de rapiditatea cu care ajung piesele comandate sa adaug alte functionalitati dupa disponibilitate.

Cum functioneaza?

Practic pentru proiect exista 3 etape de baza. Prima etapa consta in masurarea de catre senzorul DHT11 a umiditatii si a temperaturii din incapere. In a 2 a etapa senzorul trimite valorile inregistrate convertite si scalate adecvat. In ultima parte se afiseaza pe LCD si se vor trimite semnale care vor controla ventilatorul in mod automat.

Exemple de proiecte similar pe internet:

Mai jos este o lista cu proiecte asemanatoare, unele cu o complexitate mai mare altele mai simpliste. Exista o varietate de exemple pe internet si consider ca intelegerea si capacitatea de a concepe unul de la 0 este un progress bun si o buna exersare a cunostintelor dobandite in facultate.
![create](https://user-images.githubusercontent.com/57170170/171375775-966c8df0-2f64-4441-9ea8-7aede41a0e27.jpg)


Elemente folosite:

- Arduino UNO (ATMega328p)
- LCD 1602
- Senzor obstacol IR
- Senzor temperatură și umiditate DHT11
- Speaker Buzzer 3-24V, 100dB
- Sursă alimentare 12V, 2A
- Ventilator 12V, 60×6015, 6015
- Modul interfață I2C LCD 1602
- Modul releu cu optocuplor, nivel HIGH/LOW selectabil
- Fire de legătură
- LED RGB

![schema_logica_new jpeg](https://user-images.githubusercontent.com/57170170/171375866-8db08cf6-3fb7-40d9-a1f0-9dce92177e4f.jpg)
![schema_electrica](https://user-images.githubusercontent.com/57170170/171375885-709dce20-79be-467a-8d9c-79b382793a90.jpg)


Software Design:

- Mediu de dezvoltare: Arduino IDE
- In implementarea temei am folosit 2 biblioteci:
- LiquidCrystal_I2C.h
- DHT.h
- În funcția setup() declar statusul pinilor și inițializez componentele.
- În funcția loop() extrag inputul(datele ce vin de la senzorul IR și cel DHT) și fac verificările necesare pentru a obține outputul dorit pentru funcționalitățile pe care am urmărit să le implementez.

Concluzii:
Implementarea proiectului m-a ajutat în aprofundarea cunoștiințelor de proiectare de microprocesoare. Am reușit să implementez tot ce mi-am propus.
