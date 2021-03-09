# Kazniva dejanja v Sloveniji od leta 2009 dalje - Projektna naloga pri predmetu Podatkovno rudarjenje

## Opis problemska in podatkov, ki jih bomo analizirali v projektu
Za našo projektno nalogo smo si izbrali problematiko kaznivih dejanj v Sloveniji, pri čemer bomo uporabili podatke o 
zabeleženih zločinih od leta 2009 dalje. Menimo, da je koristno ugotoviti razne povezave in podobnosti med storjenimi kaznivimi dejanji, kar bi lahko veliko doprineslo k področju kriminalistike. Dandanes, ko je kriminal precej razširjen, je namreč dobro odkriti vzorce, ki se ponavljajo med podobnimi zločini in tako morebiti preprečiti v prihodnje, da bi se podobna kazniva dejanja dogajala še naprej.

Naši glavni cilji so zato predvsem iskati zanimive korelacije med zločini, ki so se dogajali, najti podobnosti, ki zares izstopajo ter ugotoviti ključne dejavnike oz. atribute, ki so najpogostejši. Na primer, odkriti, če je kakšna povezava med starostjo storitelja in vrsto zločina, če se določene vrste kaznivih dejanj dogajajajo ob določenih urah, ali kakšna Policijska uprava posebej izstopa z različnimi zločini.

Podatke smo našli na portalu [OPSI](https://podatki.gov.si/dataset/mnzpkazniva-dejanja-od-leta-2009-dalje), kjer so za vsako leto od 2009 dalje posebej objavljeni podatki o storjenih kaznivih dejanjih, za katera je policija vložila kazensko ovadbo ali poročilo. Za vsako leto je od 50 000 do 100 000, kar nam bo pripomoglo k res temeljitemu raziskovanju in rudarjenju.

Struktura podatkovne baze je sledeča:

- *ZaporednaStevilkaKD*: zločini so oštevilčeni z zaporedno številko, pri čemer se štetje vsako leto znova začne z 1.
- *MesecStoritve*: datum v formatu MM.LLLL
- *UraStoritve*: podana v intervalu
- *DanVTednu*
- *PUStoritveKD*: policijska uprava, ki je vložila kazensko ovadbo oz. zapisala zapisnik za storjen zločin
- *Povratnik*: atribut o tem, ali je osumnljenec policiji znan ali ne (DA ali NE)
- *OpisKD*: zakon/člen/odstavek/točko/alinejo akta, ki je bil kršen in naziv
- *PoglavjeKD*: poglavje zakonika, ki obravnava določeno kaznivo dejanje
- *GospodarskiKriminal*: kaznivo dejanje označeno kot 'SPLOSNA' ali 'GOSPODARSKA'
- *OrganiziraniKriminal*: pri kaznivih dejanjih, za katera se je ugotovilo, da niso organizirana, ni zapisa, pri organiziranih pa je vrednost 'ORGANIZIRANA'
- *MladoletnikaKriminaliteta*: v primeru, da gre za mladoletniško kriminaliteto, je atribut enak 'MLADOLETNIŠKA', sicer ni zapisa.
- *Poskus*: dokončanost kaznivega dejanja (DA ali NE)
- *KriminalistinaOznacba1*: oznaka kaznivega dejanja, npr. Z VLOMOM
- *KriminalisticnaOznacba2*
- *KriminalisticnaOznacba3*
- *UporabljenoSredstvo1*: sredstvo, ki se je uporabilo pri storitvi kaznivega dejanja (številka sredstva - sredstvo)
- *UporabljenoSredstvo2*
- *UporabljenoSredstvo3*
- *UporabljenoSredstvo4*
- *UpravnaEnotaStoritve*: Upravna enota, ki je obravnavala kaznivo dejanje
- *OpisKraja*: podroben opis prizorišča kaznivega dejanja
- *LetoZakljucnegaDokumenta*: leto, ko se je primer obravnave kaznivega dejanja zaprl oz. končal
- *VrstaZakljucnegaDokumenta*: OVADBA ali POROČILO
- *ZaporednaStevilkaOsebeVKD*: številka za štetje in ločevanje oseb, ki so bile udeležene v kaznivem dejanju
- *VrstaOsebe*: vloga osebe v kaznivem dejanju (ŽRTEV, OVADENI OSUMLJENEC ali OSTALO)
- *StarostniRazred*: interval (razred) starosti, ki mu oseba pripada ob storitvi kaznivega dejanja
- *Spol*: ŽENSKI, MOŠKI ali PRAVNA OSEBA
- *Drzavljanstvo*: SLOVENSKO ali TUJE
- *Poskodba*: če ni prisotna, zapis BREZ POŠKODBE, sicer ni zapisa
- *VplivAlkohola*: ali je bila oseba pod vplivom alkohola (NN ali NE)
- *VplivMamil*: ali je bila oseba pod vplivom mamil (NN ali NE)
- *OrganiziranaZdruzba*: ali je oseba pripadala organizirani združbi (NE ali ni zapisa)
- *Skoda*: interval materializirane škode v evrih oz. BREZ, če ni bilo škode
