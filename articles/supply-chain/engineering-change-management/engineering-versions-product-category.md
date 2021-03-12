---
title: Tehnilised versioonid ja tehniliste toodete kategooriad
description: See teema annab teavet tehniliste versioonide kontseptsiooni kohta. Tehnilised versioonid tagavad, et toote eri olekud ja selle andmed oleksid ajakohased ja selged ning et neid saaks süsteemis visualiseerida.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c15dcd0adfcf9b9022a919bd516dcf5117ea5041
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987475"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Tehnilised versioonid ja tehniliste toodete kategooriad

[!include [banner](../includes/banner.md)]

Tehnilised tooted arenevad toote töötsükli jooksul mitmel põhjusel. Näiteks võidakse kasutusele võtta muudatused toote teenindamise täiustamiseks, komponendi muutmiseks, kui tarnija seda enam ei paku, uuele teabele vastamiseks või algse kujunduse vigade parandamiseks. On ka palju põhjusi, miks neid muudatusi tuleks säilitada praeguse toote osana, nii et varasemaid andmeid üle ei kirjutata. Mõned neist põhjustest on järgmised.

- Soovite jälgida toodet, kuna see on toodetud ja tarnitud teie klientidele eelmises töötsükli olekus.
- Muudatuste kinnitamise ja rakendamise vahel on vaja aega.
- Soovite igale muudatusele ajatemplit ja soovite eelnevalt toodetud tooted üksteisest eraldi tarnida.

*Tehnilised versioonid* tagavad, et toote eri olekud ja selle andmed oleksid ajakohased ja selged ning et neid saaks süsteemis visualiseerida. Selle kontseptsiooni abil saate säilitada järjepidevuse, lukustada tootmise jaoks materjalide loetelu (BOM-i), kõrvaldada varieeruvuse ja hõlpsalt tuvastada muudatusi.

Üldiselt *vormi, sobivuse ja funktsiooni* reeglit, et määrata, kas muudatus nõuab uut toodet, uut versiooni või olemasoleva versiooni värskendamist. Kõik kolm terminit selle reegli nimes viitavad osa kindlale aspektile, mis aitab tehnikutel osad vastavalt vajadusele sobitada. Vormi, sobivuse ja funktsiooni reegel suurendab kujunduse muudatuste mitmekülgsust, sest osa muutmiseks vajalik dokumentatsioon ja kulu on minimaalne eeldusel, et toote sobivus, vorm ja funktsioon säilitatakse.

- **Sobivus** viitab osa või funktsiooni võimele ühendada, siduda või liita mõni muu funktsioon või osa komplektist. Sobivus võimaldab osal vastata komplekti hälbenõuetele, nii et see võib olla kasulik.
- **Vorm** viitab osa või komplekti omadustele (nt välismõõtmed, kaal, suurus ja visuaalne ilme). Vorm on aspekt, mida tehniku valikud ilme kujundamisel kõige rohkem mõjutavad. See hõlmab korpuse, raami ja juhtpaneeli, mis on toote "näoks".
- **Funktsioon** on kriteerium, mis täidetakse, kui osa töötab tõhusalt ja töökindlalt eesmärgipäraselt. Näiteks elektroonikatootes võib funktsioon sõltuda kasutatavatest tahkiskomponentidest ja tarkvarast või püsivarast. Sageli võib see sõltuda ka valitud korpuse funktsioonidest. Kaks kõige levinumat põhjust, miks korpus funktsiooni kriteeriumitele ei vasta, on kehvasti paigutatud või kehva suurusega pordid ning eksitav või puuduv märgistus. 

## <a name="engineering-versions"></a>Tehnilised versioonid

Kui kasutate tehnilisi tooteid, on igal tootel vähemalt üks tehniline versioon. Esialgne tehniline versioon luuakse automaatselt, kui loote tehnilise toote. Igas tehnilises versioonis talletatakse tehnilisi asjakohaseid andmeid, mis on selle versiooniga seotud. Siin on mõned näited nendest andmetest.

- Versiooni number ja eelmise versiooni number (kui see on olemas)
- Kehtiv algus ja lõpukuupäev
- Toote versiooni aktiivne olek, mis näitab, kas versiooni saab välja anda ja kasutada kannetes (lisateavet vt jaotisest [Toote valmisolek](product-readiness.md).)
- Toote loonud ja seda omav tehnikaettevõte (lisateavet vt jaotisest [Tehnikaettevõtted ja andmete omandiõiguse reeglid](engineering-org-data-ownership-rules.md).)
- Seotud tehnilised dokumendid, nagu komplekti kasutusjuhend, kasutusjuhendid, pildid ja lingid
- Tehnilised atribuudid (lisateavet vt jaotisest [Tehnilised atribuudid ja tehnilise atribuudi otsing](engineering-attributes-and-search.md).)
- Tehniline kooslus
- Tehnilised marsruudid

Seda teavet saate värskendada olemasoleval versioonil või luua uue versiooni, kasutades *tehnika muudatuste järjestust*. (Lisateavet vt jaotisest [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).) Kui loote tootele uue versiooni, kopeerib süsteem kõik tehnilised andmed sellesse uude versiooni. Seejärel saate selle uue versiooni andmeid muuta. Sel viisil saate jälgida kindlaid andmeid iga järjestikuse versiooni kohta. Järjestikuste tehniliste versioonide erinevuste võrdlemiseks kontrollige tehnilise muudatuse tellimust, kus on kõik muudatusi näitavad muudatuste tüübid.

Nadu öeldi, siis esialgne tehniline versioon luuakse automaatselt, kui loote tehnilise toote. Selle versiooni versiooninumberi koostamisel järgitakse toote tehnilises kategoorias määratletud versiooni numbri reeglit. Järgmisele versioonile üleminekuks peate lisama toote tehnilise muudatuse tellimuse reale ja määrama väljale **Mõju** valiku *Uus versioon*. Tehnilise muudatuse tellimus hõlmab praeguse versiooni järgmiseks versiooniks muutmise üksikasju.

Võtke arvesse, et tehniline toode võib korraga olla ainult ühes tehnilise muudatuse tellimuses. See piirang tagab andmete täpsuse ja aitab vältida toodete kattumist või vastuolulisi muudatusi. Pange ka meelde, et tehnilise muudatuste tellimuse vaate **Päis** väljal **Tehnik** kuvatakse tehnik, kes vastutab muudatuse tellimuse eest. Kui tehnik kuulub süsteemi määratud töörühma, kuvatakse väljal **Vastutav isik** selle töörühma juht.

## <a name="track-versions-in-transactions"></a>Kannete versioonide jälgimine

Kui kasutate tehnilise muudatuse haldust, on teie toote koondandmetes alati vähemalt üks tehniline versioon. Tehniliste toodete häälestuses saate valida, kas tehniline versioon on ka *logistiliste kannete* osa. (Lisateavet vt jaotist [Tehniliste toodete kategooriate häälestamine](#product-category), mis tuleb selles teemas hiljem.) Kui logistiline mõju on oluline, on see toodete ja ettevõtete lõikes erinev. Mõnikord kasutatakse ainult toote uusimat versiooni. Seetõttu, kui juurutate uue versiooni, ei saa eelmist versiooni enam kasutada. Muudel juhtudel on varasemat versiooni logistilistes kannetes vaja järgmiste probleemide lahendamiseks.

- Logistikaosakond peab kliendile saatma kaks toote osa. Sel juhul peate otsustama, kas soovite või lubate kaks erinevat versiooni saata.
- Kui hiljem avastatakse, et ilmneb probleem, siis teatakse, et see on seotud konkreetse muudatusega. Sellisel juhul võib olla kasulik määratleda täpselt, milline versioon iga tellimusega saadeti.
- Tavaliselt soovivad ettevõtted saata kõigepealt vanu versioone, et need laost välja viia. Eriti väikese mahuga toodete puhul saab seda lähenemist sageli hallata, määrates uue versiooni kehtimise kuupäevad vastavalt prognoosile, kas vana versiooniga toodete laoseis ammendub. Kuid mõnikord ei pruugi teil olla võimalik seda võrdlust teha või leiate, et laoseisu ei saa kindlalt prognoosida.

Otsus versioonide näitamise kohta laoseisus sõltub sellistest teguritest nagu eelnevalt mainitud, pluss ettevõtte tavadest ja muudes igale ettevõttele omastest kaalutlustest. Saate määrata *tehnilise toote kategooria* käitumise. Seejärel rakendub see kõikidele selle kategooriaga loodud toodetele kõigi ettevõtete puhul, kellele toode on väljastatud.

Toodete puhul, mis on häälestatud nii, et neil on logistiline mõju, tuleb iga kande puhul määrata tehniline versioon. Kuigi süsteem pakub välja *uusima aktiivse versioon*, saate valida kõigi aktiivsete versioonide seast, mis on ettevõtte jaoks saadaval. Toodete puhul, mis on häälestatud nii, et neil pole logistilist mõju, pole iga kande puhul tehnilist versiooni määratud. Siiski kasutab süsteem uusimat aktiivset versiooni. Näiteks kui lisate toote tootmiskooslusse, kasutatakse uusimat versiooni ning koondplaneerimise käivitamisel eeldatakse uusimat versiooni.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Tehniliste toodete kategooriate häälestamine

Tehnilise toote kategooria annab aluse kindla tehnilise toote tootmiseks. Iga kategooria määrab vaikeväärtused ja poliitikad. Seetõttu, kui loote tehnilise toote, valite esmalt kategooria, mille põhjal seda luua.

Võtke arvesse, et uue kategooria hierarhia tüüp (*tehnilise toote hierarhia*) häälestatakse teie eest automaatselt. Kategooriaid saate käsitsi luua, tehes valiku **Tehnilise muudatuse haldus \> Häälestus \> Tehnilise toote kategooria üksikasjad**.

Iga tehnilise toote kategooria määrab selle kategooria alusel loodud tehniliste toodete vaikekäitumise. Kui olete loonud tehnilise toote, ei saa te selle tehnilise toote kategooriat muuta. Kuid kui valite vale kategooria, saate toote kustutada ja seejärel uuesti luua.

Kui tehnilise toote kategooria on loodud, ei saa te järgmisi sätteid muuta.

- Tehnikaettevõte
- Toote tüüp
- Toote alamtüüp
- Tootedimensioonigrupp
- Konfiguratsioonitehnoloogia
- Versiooninumbri reegel

Muud sätted võivad pärida vaikimisi väärtused, mis on häälestatud tehnilise toote kategooria jaoks. Vastavalt süsteemi reeglitele saab neid väärtusi siiski muuta.

Tehniliste toodete kategooriatega töötamiseks valige **Tehnilise muudatuse haldus \> Häälestus \> Tehnilise toote kategooria üksikasjad**. Seejärel järgige üht neist sammudest.

- Uue kategooria loomiseks valige tomingupaanil nupp **Uus** ja seejärel häälestage väljad, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva kategooria redigeerimiseks valige see loendipaanil, valige toimingupaanil nup **Redigeeri** ja seejärel häälestage väljad nii, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva kategooria kustutamiseks valige see loendipaanil ja valige seejärel toimingupaanil nupp **Kustuta**.

### <a name="header"></a>Päis

Häälestage järgmised väljad tehnilise toote kategooria päises.

| Field | Kirjeldus |
|---|---|
| Nimi | Saate sisestada tehnilise toote kategooria nime. |
| Tehnikaettevõte | Valige tehnikaettevõte, kus on võimalik luua selle tehnilise toote kategooriaga tooteid ja kus neid hooldatakse. |

### <a name="details-fasttab"></a>Kiirkaart Üksikasjad

Häälestage järgmised väljad tehnilise toote kategooria kiirkaardil **Üksikasjad**.

| Field | Kirjeldus |
|---|---|
| Toote tüüp | Valige, kas kategooria kehtib toodete või teenuste puhul. |
| Kannete versioonide jälgimine | Valige, kas toote versioon tuleb tembeldada kõigil kannetel (logistiline mõju). Näiteks kui jälgite kannete versiooni, näitab iga müügitellimus, millist kindlat versiooni toode selle müügitellimusega müüdi. Kui te ei jälgi kannete versiooni, ei näita müügitellimused, millist kindlat versiooni müüdi. Selle asemel kuvatakse alati uusim versioon.<ul><li>Kui sellele suvandile määrati väärtus *Jah*, luuakse toote jaoks tooteetalon ja toote iga versioon on variant, mis kasutab *versiooni* tootedimensiooni. Välja **Toote alatüüp** väärtuseks määratakse automaatselt *Tooteetalon* ja peate valima tootedimensiooni grupi, kus *versiooni* dimensioon on aktiivne. Kuvatakse ainult need tootedimensiooni grupid, kus *versioon* on aktiivne dimensioon. Saate luua uusi tootedimensioone, valides nupu **Redigeeri** (pliiatsisümbol).</li><li>Kui selle suvandi väärtuseks määratakse *Ei*, ei kasutata *versiooni* tootedimensiooni. Seejärel saate valida, kas luua toode või tooteetalon, mis kasutab teisi dimensioone.</li></ul><p>Seda valikut kasutatakse sageli toodete puhul, mille kulu versioonide või toodete lõikes erineb, või toodete puhul, kus kliendiga seoses kehtivad erinevad tingimused. Seetõttu on oluline igas kandes näidata, millist versiooni kasutati.</p> |
| Toote alamtüüp | Valige, kas kategoorial on tooteid või tooteetalone. Tooteetalonide puhul kasutatakse tootedimensioone.
| Tootedimensioonigrupp | Säte **Kannete versioonide jälgimine** aitab teil valida toote alatüübi. Kui soovite jälgida kannete versioone, kuvatakse tootedimensioonide rühmad, kus kasutatakse *versiooni* dimensiooni. Muidu kuvatakse ainult need tootedimensiooni grupid, kus *versiooni* dimensiooni ei kasutata. |
| Toote töötsükli olek loomisel | Saate häälestada toote töötsükli vaikeoleku, mis tehnilisel tootel peaks olema, kui see esmakordselt luuakse. Lisateavet vt jaotisest [Toote töötsükli olekud ja kanded](product-lifecycle-state-transactions.md). |
| Versiooninumbri reegel | Valige versiooninumber, mis kategooria korral kehtib.<ul><li>**Käsitsi** – saate valida iga uue versiooni versiooninumbri.</li><li>**Automaatne** – süsteem määrab versiooninumbri, mis põhineb teie määratletud vormingul. Kui häälestate vormingu, kasutage numbrimärki (\#), et tähistada numbrit ja mis tahes muud märki, et tähistada püsiväärtust. Näiteks kui määratlete vormingu *V-\#\#*, on esimene versioon „V-01“, teine versioon on „V-02“ jne.</li><li>**Loend** – süsteem võtab teie määratletud kohandatud väärtuste loendist järgmise numbri.</li></ul> |
| Kehtivuse jõustamine | Valige, kas kehtivuskuupäevad peavad olema järjestikused või kas seal võib olla lünki ja kattumisi. See säte mõjutab seda, kuidas saate kasutada välju **Kehtiv alates** ja **Kehtiv kuni** iga tehnilise versiooni puhul, kus kategooriat rakendatakse.<ul><li>Kui sellele suvandile on määratud väärtus *Jah*, tuleb väärtus **Kehtiv alates** määarata iga versiooni puhul ning versioonid ei tohi kattuda ja nende vahel ei tohi olla lünki. Iga tehnilise versiooni kuupäevavahemik on ühendatud otse eelmise ja järgmise tehnilise versiooniga, kui need on olemas. Selle stsenaariumi puhul kasutatakse alati uusimat versiooni ja vanemaid versioone enam ei kasutata.</li><li>Kui sellele suvandile määratakse väärtus **Ei**, siis ei ole kehtivuskuupäevaga väljade jaoks piiranguid ja nii kattumine kui ka lüngad on lubatud. Selle stsenaariumi puhul võivad mitu versiooni olla aktiivsed samal ajal ja te saate töötada mis tahes aktiivse versiooniga.</li></ul><p>See suvand mõjutab ka kooslusi ja protsesse, mis on seotud toote versiooniga. Lisateavet vt jaotisest [Koosluste ja protsesside ühendamine tehniliste versioonidega](#boms-routes), mis on selles teemas allpool.</p> |
| Numbri reegli nomenklatuuri kasutus | Määrake sellele suvandile väärtus *Jah*, et lubada tootenumbri määratlemise reegleid, kasutades numbriseeriaid, tehniliste atribuutide nimesid ja väärtusi ning tekstikonstante segmentidena. Reeglite loomiseks või muutmiseks valige nupp **Redigeeri**. |
| Nime reegli nomenklatuuri kasutus | Määrake sellele suvandile väärtus *Jah*, et lubada nime määratlemise reegleid, kasutades tehniliste atribuutide nimesid, tehniliste atribuutide väärtusi ning tekstikonstante segmentidena. Reeglite loomiseks või muutmiseks valige nupp **Redigeeri**. |
| Kirjelduse reegli nomenklatuuri kasutus | Määrake sellele suvandile väärtus *Jah*, et lubada kirjelduse määratlemise reegleid, kasutades tehniliste atribuutide nimesid, tehniliste atribuutide väärtusi ning tekstikonstante segmentidena. Reeglite loomiseks või muutmiseks valige nupp **Redigeeri**. |

### <a name="attributes-fasttab"></a>Atribuutide kiirkaart

Kasutage kiirkaardil **Atribuudid** olevat ruudustikku, et määrata tehnilisi atribuute, mis kehtivad sellesse kategooriasse kuuluvate toodete puhul. Teavet tehniliste atribuutide loomise kotha vt jaotisest [Tehnilised atribuudid ja tehnilise atribuudi otsing](engineering-attributes-and-search.md).

Kasutage kiirkaardi **Atribuudid** nuppe, et atribuute ruudustikus lisada, eemaldada ja korraldada.

Kui muudate tehnilise kategooria atribuutide valikut ja sellel kategoorial põhinevad tooted on juba olemas, peate otsustama, kas muudatused neile toodetele rakendada. Kui soovite, et olemasolevad tooted kajastaksid muudatusi, valige kiirkaardil **Atribuudid** nupp **Värskenda olemasolevad tooted**.

Iga ruudustiku lisatava rea jaoks määrake järgmised väljad.

| Field | Kirjeldus |
|---|---|
| Nimi | Valige lisatav atribuut. |
| Väärtus | Valige atribuudi vaikeväärtus. |
| Kohustuslik | Kui sellele suvandile määratakse väärtus *Jah* atribuutide korral, mille tüüp on *Boolean*, peavad kasutajad määrama atribuudile väärtuse *Jah*. Kui selle suvandi väärtuseks määratakse *Ei*, saavad kasutajad atribuudile määrata kas väärtuse *Jah* või *Ei*. Teiste andmetüüpide puhul on selle suvandi säte lihtsalt teave. |
| Partii atribuut | Valige, kas atribuut tuleb paljundada pakkfunktsiooni kaudu. |

### <a name="readiness-policy-fasttab"></a>Kiirkaart Valmisolekupoliitika

Kasutage välja **Toote valmisolekupoliitika**, et valida valmisolekupoliitika, mida rakendatakse sellesse kategooriasse kuuluvate toodete puhul. Lisateavet vt jaotisest [Toote valmisolek](product-readiness.md).

### <a name="release-policy-fasttab"></a>Kiirkaart Vabastamise poliitika

Kasutage välja **Toote vabastamise poliitika**, et valida vabastamise poliitika, mida rakendatakse sellesse kategooriasse kuuluvate toodete puhul. Lisateavet leiate jaotisest [Tootestruktuuride vabastamine](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Koosluste ja protsesside ühendamine tehniliste versioonidega

Suvandi **Kehtivuse jõustamine** määramine on oluline koosluste ja protsesside ühendamiseks igale tehnilise versiooniga. Saate aktiveerida mitu kooslust või protsessi toote kohta ainult juhul, kui mõni järgmistest sätetest on erinev.

- Tootedimensioon
- Kogus
- Laoala
- Kehtivuskuupäevad

Tehnilised kooslused ja protsessid luuakse tehnilisest versioonist, kus neid rakendatakse. Neid saab tuvastada märkeruuduga **Tehniliselt kontrollitav**. Kui töötate tehniliste koosluste ja protsessidega, ei kujunda te neid tavaliselt erinevate koguste abil. Samuti ei kujunda te tavaliselt eri kooslusi saidi kohta. Lisaks on tehniliste koosluste ja protsesside puhul kehtivuskuupäevad alati tehnilisest versioonist võetud. Seetõttu on tehnilisel versioonil, selle kooslusel ja protsessil kõigil samad kehtivuskuupäevad.

Toodete puhul, kus kasutate *versiooni* tootedimensiooni (koos kannete logistilise mõjuga), lisatakse versioon ka kooslustele ja protsessidele. Selline käitumine aitab eristada järjestikuste versioonide kooslusi ja protsesse, vaatamata suvandi **Kehtivuse jõustamine** määramisest.

Toodete puhul, kus ei kasutata *versiooni* tootedimensiooni (ilma kannete logistilise mõjuga), ei lisata versiooni kooslustele või protsessidele. Seetõttu ei ole järjestikuste versioonide koosluste ja protsesside vahel erinevust. Sellisel juhul soovitame tungivalt määrata suvandi **Kehtivuse jõustamine** väärtuseks *Jah*. Sel viisil aitate vältida tehniliste versioonide kattumist ja saate aktiveerida ka uuema versiooni koosluse ja protsessi, ilma et peaksite esmalt aktiveerima eelmise versiooni koosluse ja protsessi. Kui määrate suvandi **Kehtivuse jõustamine** väärtuseks *Jah*, peate enne uusima versiooni aktiveerimist käsitsi aktiveerima vanemate versioonide kooslused ja protsessid.
