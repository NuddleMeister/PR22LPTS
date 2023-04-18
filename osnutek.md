1. Uvod
Seminarska naloga govori pandemiji Covid v Sloveniji, ki je trajala od leta 2020 do 2022. Izbrala sva jo, ker je v času korone veliko vprašanj ostalo neodgovorjenih, ljudje so delali špekulacije in teorije zarote Sedaj sva dobila priložnost, da na podlagi resničnih podatkov pripraviva neko zanimivo statistiko, ki bo razjasnila veliko vprašanj in to negotovo obdobje pojasnila z dejstvi in grafi prikazani na zanimiv način.

2. Delavno okolje
2.1 Podatki
Podatke črpava iz Spletne strani Covid Sledilnik oz. njegovega Git repozitorija, kjer imajo shranjene v csv datotekah. Časovno obdobje je za večino obdobje pandemije torej od leta 2020 do danes(april 23). Večinoma sva črpala podatke iz datotek o stanju v bolnišnicah, okuženosti, smrtnosti in cepljenju. Vsebujejo pa tudi druge bolj splošne podatke kot so smrtnost v zadnjih 20 letih, policijska poročila, stanje v kanalizacijah, podatke o šolah, itd.
Podatke imajo načeloma shranjene vedno skozi čas, kjer imajo shranjene dnevne podatke, večinoma pa jih hranijo v sistemu »to date« oz. vsak dan je seštevek vseh prejšnjih plus današnji.
2.2 Knjižnice
Za delo sva v večini uporabljala knjižnico Pandas oz. njegov dataframe za obdelovanje podatkov in kot dodatek po potrebi Numpy za sezname. Za prikazovanje podatkov, kot so grafi pa sva uporabljala matplotlib.

3. Študije
3.1 Smrtnost
V Sloveniji je bilo veliko govora o smrtnosti, češ da vsak, ki umre okužen z covidom, je umrl zaradi njega. Tukaj preizkušava to tezo. To sva se lotila tako, da izračunava pričakovano smrtnost in nato primerjava, če se presežek ujema z številom žrtev covida.
 
Slika 1: Graf števila umrlih ljudi v Sloveniji po letih (modra), pričakovana smrtnost (oranžna)
Graf pokaže z modro črto koliko ljudi je umrlo od leta 2010 do 2022. Z oranžno pa smo poskušali ugotoviti trend rasti, ki znaša 0.87% letno od 2010 do 2019. Na ta način sva dobila neko pričakovano smrtnost za covidna leta ampak kot vidimo je umrlo veliko več ljudi.
 
Sedaj pa sva pa sva tej napovedi dodala število ljudi, za katere je bil vzrok smrti covid. Kot vidimo je leta 2020: Umrlo nekaj 100 več ljudi kot bi pričakovali. Torej so v prvem letu dokaj konzervativno in korektno ocenili smrtnost o covidu. Naslednje leto je umrlo največ ljudi za covidom. Razlika v grafu je 847 ljudi, kar je že kar veliko ljudi, katerih vzrok smrti je bil napačno ocenjen. Zadnje leto korone, pa očitno niso več kaj dosti komplicirali. Razlika je kar 1454 ljudi, kar predstavlja 6% vseh umrlih in je relativno velika napaka. 
Torej lahko potrdimo tezo da je bilo v letu 2021 in 2022 veliko vzrokov smrti napačno ocenjenih in v realnosti za covidom ni umrlo 9201 človek kot je uradni podatek. Pravi podatek se seveda ne da izračunati, ampak glede na najino oceno o pričakovani smrtnosti je to 6843 ljudi.

4. Zaključek
Seminarska naloga pokriva skoraj vsa področja epidemije in je bilo tudi za naju izredno zanimivo primerjati, kaj so mediji govorili po poročilih, kakšna je bila ulična propaganda, kako je takratna vlada reagirala z ukrepi. Meniva da so mediji velikokrat nekorektno predstavljali informacije, verjetno samo z namenom, da imajo zgodbo, realnost pa ni bila tako siva.
