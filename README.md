# LAB1-WEB
##MUzička streaming aplikacija LAB-1
##Člannovi tima:
Ramo Kozlić
Emir Đelilbašić
##Opis modela i relacija:
Album sadrži id,naziv,izvodjac,godinaIzdanja,listu pjesama.
Pjesma sadrži id,naziv,trajanjeSekunde,žanr i referencu na pripadajući album.
Relacija je 1:N(Jedan album sadrži više pjesama).
##Rute:
a- Lista svih albuma
b- Lista svih Pjesama 
a/action/{id}- Prikaz pojedinačnog albuma sa listom njegovih pjesama.
