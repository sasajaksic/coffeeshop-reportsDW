# Kafeterija Data Warehouse

## Zadatak i ciljevi projekta
Zadatak projekta je da na osnovu opširnih podataka poslovanja franšize kafeterija u *New York*-u, dođemo do odgovora na postavljena pitanja, koja mogu biti od velikog značaja rukovodiocima i menadžerima kafeterija. Ovaj zadatak ostvarujemo transformacijama i manipulacijama izvornih podataka koje zatim smeštamo u DW (*Data Warehouse*) sistem, iz kojeg dalje koristimo podatke za generisanje *Reportova* koji rukovodiocima i menadžerima omogućavaju pregledniji uvid u podatke, na osnovu kojih mogu efikasnije i jednostavnije donositi odluke.
Cilj projekta je da na kraju ovog pocesa imamo razvijen funkcionalan *Data Warehouse* sistem, kreirane izveštaja, odgovore na postavljena pitanja, kao i stečena znanja za razvijanje i proširenja ovakvih sistema.

## Opis posutupka projektovanja DW sistema
Proces projektovanja DW sistema se odvija u više faza:
-Pronalaženje i istraživanje *dataseta*
-Preuzimanje *dataseta*
-Identifikacija veza i odnosa između podataka
-Kreiranje strukture bazirane na OLAP (*Online Analytical Processing*) šemi, na serveru
-Transformacije izvornih podataka tako da odgovaraju prethodnoj strukturi
-Upis transformisanih podataka u bazu podataka
-Kreiranje izveštaja

## Specifikacija zahteva korisnika
Pronaći adekvatan *dataset*: 
1. *Dataset* treba da sadrži barem jednu vremensku odrednicu
2. Transformacije podataka odraditi putem ETL(*Extract-Transform-Load*) procesa
3. Na serveru kreirati tabele koje obuhvataju tabele dimenzija i tabelu činjenica
4. OLAP šema treba da sadrži jednu tabelu činjenica i pet tabela dimenzija (jedna od tih treba da bude vremenska)
5. Podatke iz ETL pocesa upisati u bazu podataka
6. Postaviti barem pet pitanja
7. Za svako pitanje kreirati jedan izveštaj koji će dati odgovor na postavljeno pitanje

## Specifikacija modela
Izvoru podataka se može pristupiti uspomoć linka: [Dataset](https://www.kaggle.com/ylchang/coffee-shop-sample-data-1113).
Tabele dimenzija u okviru OLAP šeme su: “Datum”, “Kupac”, “Zaposleni”, “Račun” i “Kafeterija”, dok tabela “Stavka” predstavlja tabelu činjenica. Najveća promena do koje je došlo, jeste kreiranje nove tabele, “Stavka”, uspomoć koje smo promenili granularnost sa pojedinačnog računa na pojedinačnu stavku računa.

<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1DTZoTPPwMnPdJfIzXKlalS8M63IL9qsV" alt="My cool logo"/>
</div>

## Prikaz izveštaja
Pitanje 1: Koja kafeterija je imala najveći pazar 15.04.2019.?
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1oNMPOi9LTMQl6KSnMxGyGdIMZvUpGiMP"/>
</div>

Pitanje 2: Koja generacija kupaca najviše kupuje proizvode kategorije ‘coffee’ radnim, a koja neradnim danima?
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=11udgaIxNGcnetCXWbkD4nEkH5lLJdBvR"/>
</div>

Pitanje 3: Koji zaposleni u proseku prima najskuplje porudžbine?
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1ojg8w8ofRuRYypA8vB5qYg3cxUO_6aIY"/>
</div>

Pitanje 4: U kojoj kafeteriji se kupci najčešće prijavljuju za karticu lojalnosti?
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=17cE1R_eCwnwWrNOiy29iCWi7A6_ytwQ0"/>
</div>

Pitanje 5: Koji proizvod ima najveću  razliku između maloprodajne i veleprodajne cene?
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=1PayL7W8L5berBt_EgHsT26-mimwg9J_e"/>
</div>

Pitanje 6: Koji proizvodi, koji nisu na promociji, su najprodavaniji ponedeljkom, a koji nedeljom?
<div align="center">
  <img src="https://drive.google.com/uc?export=view&id=16ieDapLd0MnCFG-fhtf4YNlAad--_bdP"/>
</div>
