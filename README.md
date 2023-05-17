# PR22LPTS
Repository for FRI-PR datamining project


## Uvod
Seminarska naloga govori pandemiji Covid v Sloveniji, ki je trajala od leta 2020 do 2022. Izbrala sva jo, ker je v času korone veliko vprašanj ostalo neodgovorjenih, ljudje so delali špekulacije in teorije zarote. Sedaj sva dobila priložnost, da na podlagi resničnih podatkov pripraviva neko zanimivo statistiko, ki bo razjasnila veliko vprašanj in to negotovo obdobje pojasnila z dejstvi in grafi prikazani na zanimiv način.

## Delavno okolje
### Podatki

Podatke večinoma črpava iz Spletne strani Covid Sledilnik oz. njegovega Git repozitorija, kjer imajo shranjene v csv datotekah. Časovno obdobje je za večino obdobje pandemije torej od leta 2020 do danes(maj 17). Večinoma sva črpala podatke iz datotek o stanju v bolnišnicah, okuženosti, smrtnosti in cepljenju. Vsebujejo pa tudi druge bolj splošne podatke kot so smrtnost v zadnjih 20 letih, policijska poročila, stanje v kanalizacijah, podatke o šolah, itd.
Podatke imajo načeloma shranjene vedno skozi čas, kjer imajo shranjene dnevne podatke, večinoma pa jih hranijo v sistemu »to date« oz. vsak dan je seštevek vseh prejšnjih plus današnji.
Prav tako sva uporabila StatSi skjer sva črpala smrtnost in rodnost v Sloveniji.

## Knjižnice

Za delo sva v večini uporabljala knjižnico Pandas oz. njegov dataframe za obdelovanje podatkov in kot dodatek po potrebi Numpy za sezname. Za prikazovanje podatkov, kot so grafi pa sva uporabljala matplotlib.

## Študije
### Smrtnost
V Sloveniji je bilo veliko govora o smrtnosti, češ da vsak, ki umre okužen z covidom, je umrl zaradi njega. Tukaj preizkušava to tezo. To sva se lotila tako, da izračunava pričakovano smrtnost in nato primerjava, če se presežek ujema z številom žrtev covida.

![image](https://user-images.githubusercontent.com/82542995/232958681-5956ce6e-7d89-4d38-8245-c01bdff7de6c.png)

Slika 1: Graf števila umrlih ljudi v Sloveniji po letih (modra), pričakovana smrtnost (oranžna)


Graf pokaže z modro črto koliko ljudi je umrlo od leta 2010 do 2022. Z oranžno pa sva poskušali ugotoviti trend rasti na podlagi letnega števila smrti in populacije, ki znaša 0.87% letno od 2010 do 2019. Na ta način sva dobila neko pričakovano smrtnost za covidna leta, ampak kot vidimo je umrlo veliko več ljudi.
Da bomo še bolj natačni, smo izračunali še povprečno napako, ki znaša `~16` ljudi.

Povzamimo vsa tri leta:
2020: Predvidenih je 21657 smrti, a bilo jih je 24962, kar je 3305(3321) ljudi preveč. 
2021: Predvidenih je 21845 smrti, a bilo jih je 24103, kar je 2258(2274) ljudi preveč. 
2022: Predvidenih je 22034 smrti, a bilo jih je 23300, kar je 1266(1282) ljudi preveč. 

![image](https://user-images.githubusercontent.com/82542995/232958949-7a6a3de7-4046-46d9-bb48-18fae51539c5.png)

Slika 2: Smrtnost z pričakovano vrednostjo plus prijavljene žrtve covida
 
Sedaj pa sva pa sva tej napovedi dodala število ljudi, za katere je bil vzrok smrti covid, ki naj bi bili dodatek. Kot vidimo je leta 2020 umrlo nekaj 279 več ljudi kot bi pričakovali. Torej so v prvem letu dokaj konzervativno in korektno ocenili smrtnost s covidom. Naslednje leto je umrlo največ ljudi za covidom. Razlika v grafu je 852 ljudi, kar je že kar veliko ljudi, katerih vzrok smrti je bil napačno ocenjen. Zadnje leto korone, pa očitno niso več kaj dosti komplicirali. Razlika je kar 1459 ljudi, kar predstavlja 7% vseh umrlih in je relativno velika napaka. 
Torej lahko potrdimo tezo da je bilo v letu 2021 in 2022 veliko vzrokov smrti napačno ocenjenih in v realnosti za covidom ni umrlo 9201 človek kot je uradni podatek. Pravi podatek se seveda ne da izračunati, ampak glede na najino oceno o pričakovani smrtnosti je to 6611 ljudi, raylika torej 2590.


### Okuženost med cepljenimi in necepljenimi
Slovenci smo bili do 1. 2. 2022 57,2 procentno precepljeni, kar pomeni, da jih je veliko takih, ki se niso želeli cepiti (skoraj polovico). Cepljenje je seveda osebna odločitev, zanima pa naju, kako vpliva na število okužb oziroma na možnosti za okužbo.

![image](https://user-images.githubusercontent.com/82542995/232959271-d4758423-f385-4ac4-9410-c5cfe4c49f68.png)

Slika 3: Procent okuženih cepljenih in necepljenih ljudi

Na grafu sva z oranžno črto prikazala razmerje vseh do sedaj okuženih in cepljenih proti vsem cepljenim ter z modro črto razmerje vseh do sedaj okuženih ki niso bili cepljeni proti vsem necepljenim. Vidimo da je okuženih cepljenih precej manj, zato bi lahko rekli, da cepljenje dela. Vendar pridemo do problema, da ob začetku najhujšega koronskega vala podatkov o obolelih in cepljenih niso več posodabljali, kar je precej vprašljivo. Na grafu vidimo, da funkcija začenja eksponentno rasti, o njenih nadaljnih stanjih pa lahko le spekuliramo.


### Vpliv na človeško psiho

Veliko prebivalcev je govorilo o slabšanju mentalnega stanja, predvidevava pa, da je karantena psihično najbolj vplivala na najstnike ki se še mentalno razvijajo in za to potrebujejo socialne interakcije, ter najstarejše, ki so bili večinoma že tako sami. Poglejmo si kako se to izraža v največjem ekstremu - samomorih.

![image](https://github.com/NuddleMeister/PR22LPTS/assets/82542995/3f290065-8e67-4a8d-83ca-963a140371e2)

Slika 4: Primerjava povprečnega števila samomorov med 2010 in 2019 ter leta 2020 po starostnih skupinah

Vidimo, da se je samomorilnost pri srednjih letih leta 2020 zmanjšala, pri najstarejših pa močno povečala, le ti pa so že tako ali tako najbolj ogrožena skupina ljudi. Podatke za število samomorov imava samo do leta 2020, zato je težko sklepati, ali se je trend pri najstarejših nadaljeval ali ne.


## Zaključek
Seminarska naloga pokriva skoraj vsa področja epidemije in je bilo tudi za naju izredno zanimivo primerjati, kaj so mediji govorili po poročilih, kakšna je bila ulična propaganda, kako je takratna vlada reagirala z ukrepi. Meniva da so mediji velikokrat nekorektno predstavljali informacije, verjetno samo z namenom, da imajo zgodbo, realnost pa ni bila tako siva.
 
## Viri
•	Covid Sledilnik: https://covid-19.sledilnik.org/sl/stats
•	Covid Sledilnik (Git): https://github.com/sledilnik/data-api/ 
•	Pandas: https://pandas.pydata.org/
•	Matplotlib: https://matplotlib.org/
•	Numpy: https://numpy.org/
•	SiStat: https://pxweb.stat.si/SiStat/sl

