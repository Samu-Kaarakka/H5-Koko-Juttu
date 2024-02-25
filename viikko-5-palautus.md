# Koko juttu

## A)Uuden virtuaalikoneen asennus

Asensin Oracle VM VirtualBoxissa uuden virtuaalikoneen. Asetuksina käytin samoja kuin aikaisemmissa asennuksissa: kieleksi American English, näppäimistön kieleksi Suomi sekä sijainniksi Helsinki. Debian installerissa Users-kohtaan annoin seuraavat tiedot:
![Add file: Upload](Osa1.png)

Seuraavaksi tein tavalliset alkutoimenpiteet:

* Päivitykset komennolla : $ sudo apt-get -y dist-upgrade 

* Palomuurin asennus ja käyttöönotto komennoilla : $ sudo apt-get -y install ufw,
$ sudo ufw enable

### Apache weppipalvelin asennus

Asensin Apachen kommennoilla: 
$ sudo apt-get update
$ sudo apt-get -y install apache2

Tämän jälkeen testasin toimivuuden selaimessa localhost osoitteesta ja kaikki toimi tässä vaiheessa niinkuin pitikin:

![Add file: Upload](Osa2.png)

### SSH-etähallintapalvelimen asennus

Asensin SSH:n komennoilla:
$ sudo apt-get install -y openssh-server
$ sudo systemctl enable ssh

### Uusi etusivu weppi-palvelimelle

Komennolla "sudoedit /etc/apache2/sites-available/testi.conf" avasin tekstieditorissa kyseisen tiedoston sekä muokkasin siihen haluamani <VirtualHost> tiedot:





