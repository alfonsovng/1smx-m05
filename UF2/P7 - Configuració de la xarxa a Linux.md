# Pràctica 7

## 1. Xarxa NAT amb Virtual BOX

Primer de tot, crea una xarxa NAT pròpia amb VirtualBox:

![p7-xarxa-nat-propia.png](images/p7-xarxa-nat-propia.png)

Farem servir la xarxa privada 192.168.1.0/24

Consulta l'enllaç següent i prova d'entendre i explicar AMB LES TEVES PAREULES quines opcions de xarxa permet Virtual Box i en que consisteixen: https://www.virtualbox.org/manual/ch06.html#networkingmodes

## 2. Ubuntu Server 18.04 LTS

Crea una nova màquina virtual con VirtualBox fent servir la ISO ubuntu-18.04.1-live-server-amd64.iso que tens al repositori samba del Institut. Selecciona com a xarxa la xarxa NAT que has creat en el punt anterior i posa-li un disc dur dinàmics de 10GB.. Com a hostname has de posar el teu nom i el mòdul, és a dir, en el meu cas seria m05-alfonso. No cal documentar el procés d'instal·lació.

Respon, amb les teves paraules, a les següents preguntes:

1. Què vol dir LTS?
2. Fins quan té suport aquesta versió que has instat·lat?
3. Quina diferència hi ha entre un Ubuntu Server i un Ubuntu Desktop?
4. Per a que es fa servir generalment un Ubuntu Server (o qualsevol altre distribució similar)? Pots buscar informació sobre aquest punt en aquest enllaç: https://es.godaddy.com/blog/que-es-ubuntu-y-para-que-sirve/

## 3. Comanda lshw

Executa les següents comandes:

    sudo lshw | more
    
    sudo lshw -class network
    
    sudo lshw -class network -short

Busca i tracta d'explicar,, AMB LES TEVES PARAULES, què fa la comanda lshw. Pots buscar-ho per internet i/o també pots buscar informació amb la comanda `man`:

	man lshw

## 4. Comanda ethtool

A la columna Device de la darrera instrucció apareix el nom de la targeta de xarxa que tindràs. En el meu cas es diu *enp0s3*. Executa la instrucció següent possant, si cal, el nom del teu dispositiu de xarxa enlloc del *enp0s3*:

	sudo ethtool enp0s3

Quina informació surt? Què fa la comanda ethtool? Igual que abans, pots consultar-ho amb la comanda `man`:

	man ethtool

## 5. Loopback

Executa ara la comanda `ip a`. Quantes targetes de xarxa apareixen? Hi ha una que és diu **loopback**. Busca informació sobre que és i per a que serveix. Pots consultar aquest enllaç si vols: https://askubuntu.com/questions/247625/what-is-the-loopback-device-and-how-do-i-use-it



*... continuarà ...*