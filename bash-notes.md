###Level 0

#ssh -p 2220 bandit0@bandit.labs.overthewire.org   --Povezivanje na server preko ssh

##########################################################################################################################################

###Level 0 → Level 1

#cat readme   --izlistavanje sadrzaja fajla “readme”

##########################################################################################################################################

###Level 1 → Level 2

#cat ./-  --znak - predstavlja posebno ime datoteke koje označava standardni ulaz ili standardni izlaz. Kada koristimo – kao imena fajla, fajlu mozemo pristupiti  koristeći prefiks ./ i onda dodamo ime fajla -.

###########################################################################################################################################

###Level 2 → Level 3

#cat "spaces in this filename"  --izlistavanje sadrzaja fajla za navodnicima  "spaces in this filename" jer imaju razmaci u nazivu

#########################################################################################################################################

###Level 3 → Level 4

#cd  inhere     --prelazak u folder “inhere”
#ls -la    --izlistavanja sadrzaja foldera “inhere”
#cat .hidden   --izlistavanje sadrzaja fala “.hidden”

#########################################################################################################################################

###Level 4 → Level 5

#cd  inhere    -- prelazak u folder “inhere”
#file ./* --komandom file provjeravamo tipove fajlova. ./ stavljano jer fajlovi pocinju sa – a * znaci svi fajlovi u tom folderu. 
#Komanda je vratila izlaz  “ASCII text” za fajl “-file07”. To znaci da se lozinka nalazi u “-file07”.
#cat ./-file07   --ispis sadrzaja fajla “-file07”   

#########################################################################################################################################

###Level 5 → Level 6

#find inhere -type f -size 1033c   --ovom komandom pretazujemo fajlove velicine 1033 bajta u folderu infere. Izlaz ove komande je bio “inhere/maybehere07/.file2”
#cat inhere/maybehere07/.file2
########################################################################################################################################

###Level 6 → Level 7

#find / -type f -user bandit7 -group bandit6 -size 33c   --ova komanda ptretrazuje fajlove velicine 33 bajta I da fajl pripada korisniku “bandit7” I grupi “bandit6” na cijelom sistemu. 
#cat /var/lib/dpkg/info/bandit7.password

#########################################################################################################################################

###Level 7 → Level 8  

#grep millionth data.txt --pretrazivanje rijeci “millionth” u fajli  “data.txt”

#########################################################################################################################################

###Level 8 → Level 9

#cat data.txt | sort | uniq -u   --sa "cat" comandom izlistavamo sadrzaj fajla data.txt, sa komandom “sort” sortiramo po abecesnom recu, I sa konadom “uniq -u” ispisujemo jedinstevene linije koje se ne ponavljaju u fajlu.

##########################################################################################################################################

####Level 9 → Level 10

#strings data.txt | grep "=="  --komandom Izlistavamo sve nizove znakova iz binarnog fajla"data.txt" I poslije grep komandom filtiramo sve linije  koje sadrže niz "==".

#########################################################################################################################################

###Level 10 → Level 11

#cat data.txt | base64 –decode   --ovom komandom dekorieamo I izlistavamo sadrzaj fajla “data.txt”

