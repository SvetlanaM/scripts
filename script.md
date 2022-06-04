**Priklady archivacie**

```tar cvzf fotky.tgz *.jpgtar tzf fotky.tgztar xvzf fotky.tgztar xvzf fotky.tgz a.jpg```

```zip fotky *.jpgzip –r archiv adresarunzip fotky.zipunzip fotky.zip a.jpg```

```gzip *.jpggunzip *gzip –r adresargunzip –r adresar```

```tar cvf – *.jpg | gzip > foto.tar.gzgunzip -c foto.tar.gz | tar xvf -```

 
**Priklady na pracu s textom**

```cat /etc/passwd | cut -f 1,6 -d ":" | cut -f 1 -d ":"ls -la |cut -f 1,4,5 -d " " | grep t1ls -la |cut -f 1,4,5 -d " "ls /etc | sortcat /etc/passwd | sort```

skript.sh 

```
#!/bin/bash  # = komentar // v c/c++echo "hello world" #printf

MENO="jano"        #char []VEK=32             #int

echo "$MENO ma $VEK rokov" echo "zadaj novy vek : "read VEK    #scanf 

echo "novy vek je $VEK"

tyzden=(pon uto str stv pia sob ned) #pole vymenovanimmena[0]="fero"

echo "prvy den je ${tyzden[0]}" #vypis hodnotyecho "druha osoba je : ${mena[1]}"echo "vsetky mena = ${mena[*]}"

if [ $VEK -eq 10 ] #if(vek==10)then echo "ma 10 rokov"else

echo $#echo "prvy $0"echo "druhy $1"echo "treti $2"
```

cykly.sh

```
#!/bin/bash

# for(int i=0;i<10;i++) {}

for i in 1 2 4 5 
touch "subor$i"done

for i in {2..10} #zlozene z.do echo 
rm subor$idone

echo ${BASH_VERSION} #vypise verziu bash-ufor i in {2..10..2}
for(int i=2;i

for (( i=1; i<7; i++ )) #syntax ako v cdo echo "ako v C $i" if [ $i -eq 5 ]; then    break fidone

for i in $( ls /etc ); do #iteracia polom z prikazu ls  echo "subor : $i" #>> log
```

```
i=0while [ $i -lt 10 ]; do echo "iteracia : $i"  let i=i+2done #stvorcek :for (( i=0; i

#### switch = alternativa vela IF-ovecho -n "zadaj vstup : "read volbacase $volba in 1|3)  echo "jednotka alebo trojka"   ;; #ako v C break;[4-6])  echo "cislo od 4 po 6"   ;;"AA")  echo "pismenka A"   ;;*)  #defaultne vykonane ak ina moznost nie je  echo "nieco ine"   ;;esac

##### jednoduche menuecho "zvol akciu : "select akcia in uzivatelia server_info odhlasenie koniecdo case $akcia in  uzivatelia)    who   ;;  server_info)    uptime   ;;  odhlasenie) exit ;; #exit=koniec skriptu  koniec) break ;; # ukonci menu-cyklus  *) break ;; #defaultne von z menu ked netrafime volbu esacdone#funkcie piscislo () {     echo "mam $# parametrov" echo "mam cislo : $1 $2 $3"}     piscislo 99piscislo $( ls )
```

php.sh

```
#!/usr/bin/php5-cgi<html><body>

<?php echo "HELLO \n"; $MENO=   "fero"; $vek=12.5; 
echo $MENO; 
echo " on sa volal $MENO \n"; 
echo $vek.' $MENO \n';  
$fakulty[1]="fhi";$fakulty[2]="nhf"; $fakulty["ZLE"]="XX"; 
$kruzky=array('2hi', '3hi');  
if(($MENO == "fero" && ($vek>=12))) {  echo "ano \n"; } 
else echo "nie \n"; for($i=2;$i<10;$i++) echo "robim $i\n"; while($i-->0) 
echo "whilenow $i \n"; sort($fakulty); foreach($fakulty as $index => $f)  
echo "fakulta $index = $f\n"; echo date("d.M.Y");  
file_put_contents("subor","ahoooohj".$vek);   
function NH($pocet) {  $vrat=array();  for($i=0;$i<$pocet;$i++)   
array_push($vrat,rand(0,100));  return $vrat;  } 
$n=NH(10); print_r($n);  $c= file_get_contents("http://www.zoznam.sk"); ?>
</body>
</html>
```
