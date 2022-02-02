---
title: Vara rentimise funktsiooni kasutamise alustamine
description: Selles teemas kirjeldatakse vara rentimise võimalust ja näidatakse, kuidas renditavat vara luua ja nende varade teavet vaadata.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeasingWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 72c362e651787d2ff120944925e3bc35523f0059
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982005"
---
# <a name="asset-leasing-get-started"></a>Vara rentimise funktsiooni kasutamise alustamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse vara rentimise võimalust ja näidatakse, kuidas renditavat vara luua ja nende varade teavet vaadata. Teemas on toodud ka kasutajaliideses ja dokumentatsioonis kasutatud terminoloogia. Vara rentimine on täiustatud võimalus renditavate varade finantskannete haldamiseks, jälgimiseks ja automatiseerimiseks teenuses Microsoft Dynamics 365 Finance. Vara rentimise funktsioon vastab rahvusvahelistele raamatupidamisstandarditele (IFRS 16) ja Ameerika Ühendriikide üldaktsepteeritavate raamatupidamispõhimõtete (GAAP) standarditele (ASC 842). Vara rentimise funktsioon kogub ja töötleb renditavate varade põhiteavet ning aitab luua töölehe sisestusi terve renditava vara elutsükli jooksul alates esialgsest tuvastamisest, igakuistest töölehe sisestustest kuni renditava vara väärtuse langemiseni ja rentimise lõppemiseni. Vara rentimise funktsioon integreerub sujuvalt teiste rakenduse Dynamics 365 Finance komponentidega, sealhulgas põhivarad, ostureskontro ja pearaamat.

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada **funktsioonihalduse** tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Otsige tööruumis **Funktsioonihaldus** üles suvand **Vara rentimine** ja seejärel klõpsake nuppu **Luba kohe**.

Lisateavet raamatupidamisstandardite kohta leiate rahvusvaheliste raamatupidamisstandardite (IFRS 16) ja Ameerika Ühendriikide üldaktsepteeritavate raamatupidamispõhimõtete (GAAP) standardite (ASC 842) standarddokumentatsioonist.

## <a name="asset-leasing-elements"></a>Vara rentimise elemendid
Järgmisel diagrammil on toodud rentimise protsessi peamised elemendid.

[![Vara rentimise elemendid.](./media/overview-01.png)](./media/overview-01.png)

Renditav vara hõlmab järgmisi põhikomponente.

- **Rendileping** – rendileandja omab vara ja nõustub rentima rentnikule vara kindlaks perioodiks vastutasuks perioodiliste rendimaksete eest. Lisaks seaduslikule lepingule rendileandja ja rentniku vahel sätestatakse rendilepingus haldusotsused, nt pikendamise ja omandi ülemineku tõenäosus.

- **Rendi arvutamine ja klassifikatsioon raamatupidamisstandardi järgi** – rendi arvutamine ja klassifikatsioon määratlevad raamatupidamisstandardi, mida rakendatakse algses ja järgnevas mõõtmises, ning ka klassifikatsioonitesti, mis määrab, milline on rendi tüüp. Rent võib olla kapitalirent, kasutusrent, lühiajaline rent või väikese väärtusega rent. Süsteem arvutab ka hindamise ja klassifikatsiooni eesmärgil tulevaste minimaalsete rendimaksete praeguse väärtuse.

- **Rendikanded** – vara rentimise funktsioon toetab rentimise korral kasutamisõiguse esemeks oleva vara esialgset tuvastamist bilansis, samuti sellele järgnevat mõõtmist nii bilansisisese kui ka bilansivälise rentimise puhul. Esialgse tuvastamise kanne mõõdab tulevaste minimaalsete rendimaksete praeguse väärtuse. Neid andmeid kasutatakse organisatsiooni bilanssi mõjutavate esmase kasutamisõiguse esemeks oleva vara ja rendikohustise väärtuse määramiseks. Järgnev igakuiste rendikannete mõõtmine hõlmab intressi akumuleerimist rendikohustisel, mis suurendab rendikohustist. Samuti mõõdab see rendimaksete akumuleerimist, mis vähendavad rendikohustist ja mis makstakse seejärel rendileandjale. Mõõtmine hõlmab ka kasutamisõiguse esemeks oleva vara amortisatsiooni.

  Bilansivälise rentimise puhul arvutab süsteem lineaarse rendikulu selle põhjal, mis on lühem: vara majanduslik eluiga või rendiperiood. Rendikorrigeerimised mõõdavad lepingu muudatusi, nt rendilepingu pikendamist või laienemist, ning väärtuse languse kannet, mis kasutab luhtunud kulude puhul kasutamisõiguse esemeks olevat vara.

  Vara rentimise funktsioon integreerub pearaamatuga, et tagada, et kõik sisestatud rendikanded värskendavad teie kontoplaani. Vara rentimise funktsioon integreerub ostureskontroga, et jälgida rendileandja arveid ostureskontros ja võtta sealt tulevasi makseid. Integratsioon põhivarade funktsiooniga võimaldab teil jälgida põhivarade registris olevaid renditud varasid ning sisestada kasutamisõiguse esemeks oleva vara kandeid, sh vara esialgset tuvastamist, kulumit ja väärtuse langust põhivarade funktsiooni kaudu.   

## <a name="asset-leasing-components"></a>Vara rentimise komponendid 
Vara rentimise funktsioon vastendab renditeavet, maksegraafikuid, algus- ja lõppkuupäevasid ning maksete sagedust. Samuti automatiseerib see praeguse väärtuse, igakuiste rendimaksete, intressi ja renditava vara amortisatsiooni arvutamised. Süsteem teeb konfiguratsioonist sõltuvalt rendi klassifikatsiooniteste. Süsteem loob ja sisestab ka vastavaid rendikandeid, mis põhinevad raamistikul, mis on määratletud rakenduvas raamatupidamisstandardis.

Järgmine diagramm näitab rendiraamatut, renditeavet, arvutatud maksegraafikut, rendi ja rendiraamatute klassifitseerimise teste ning vastavaid raamatupidamiskandeid.

[![Rentimine, rendiraamat ja maksegraafik.](./media/overview-02.png)](./media/overview-02.png)

- **Rendiraamat** – rendiraamat sisaldab kogu rendilepingu teavet, nagu renditingimused, õiglane väärtus ja rendimaksed. See hõlmab ka raamatupidamisstandardit, mida te järgite, renditüüpi ja lävesid, mida arvestatakse rendi klassifikatsioonitestis. Rendiraamat sisaldab ka pearaamatusse sisestatud rendikandeid. 
  
- **Rent** – rent sisaldab renditeavet, mis esindab vara rentimise alust. Renditeabe allikad on rendileping ja haldamisotsus, mis tehakse mõlemad väljaspool rakendust Dynamics 365 Finance. Vara õiglane väärtus on hind, mis makstaks vara eest mõõtmise päeval tehtud kandes. See väärtus võib sõltuda vara tüübist, turutingimustest ja muudest kriteeriumidest, mida saab hindamisel arvestada. Vara õiglast väärtust arvestatakse klassifikatsioonitesti võrrandis.

- **Vara kasulik tööiga** – see tähistab vara kasuliku tööaja järelejäänud perioode alates rentimise alguskuupäevast. Vara kasulikku tööiga arvestatakse klassifikatsioonitesti võrrandis. See erineb põhivarades määratletud kasulikust tööeast.

- **Alternatiivne laenuintressimäär** – See on intressimäär, mida kasutatakse praeguse väärtuse arvutamiseks. Süsteem kasutab kaudset määra, kui see on rendiandmetes määratletud, et arvutada rendimaksete praegune väärtus. Kui kaudset määra ei ole määratletud, kasutab süsteem alternatiivset laenuintressimäära.

- **Annuiteedi tüüp** – see on rendimakse, mis kuulub tasumisele kas makseperioodi alguses või lõpus. See võib olla ettemakse ehk perioodieelne annuiteet (rendimakse perioodi alguses) või tavaline annuiteet (rendimakse perioodi lõpus).

  Ettemakse puhul loetakse esimene kuu perioodiks numbriga null; perioodijärgsete maksete puhul loetakse esimene kuu esimeseks perioodiks.

- **Liitintervall** – see näitab perioodide arvu, mille korral intress aasta jooksul koguneb. See võib olla kord kuus (12 perioodi aastas), kord kvartalis (4 perioodi aastas), kord poole aasta tagant (2 perioodi aastas) või kord aastas (1 periood aastas). Perioodide arv võetakse arvesse praeguse väärtuse arvutamisel.

- **Alguskuupäev** – see on kuupäev, mil rendileandja annab vara rentnikule kasutamiseks üle. Kõik rendiarvutused ja -kanded põhinevad alguskuupäeval. Alguskuupäev peaks olema perioodi alguses (kuu esimene päev), et tagada järgnevate arvutuste täpsus. Saate kasutada välja **Lepingu allkirja kuupäev**, et sisestada lepingu allkirjastamise tegelik kuupäev.

- **Rendiperiood** – see on rendiperioodi pikkus kuudes.

> [!NOTE] 
> Rendiperioodi mõiste aluseks on maksegraafiku ridade perioodide arv või intervallid. Määratud intervallide arv teisendatakse kuudeks.

- **Maksegraafiku rida** – see talletab rendimakseid perioodi kohta. Samuti täpsustatakse selles, kas kasutamisõiguse esemeks olev vara ja rendikohustise esmasel mõõtmisel kasutatakse ja kaasatakse pikenemisperiood. Saate määrata tasumisele kuuluvate rendimaksete alguskuupäeva ja perioodiintervallid, mis tähistavad rentimise kestust, mis võivad olla päevad, kuud või aastad.

- **Maksete sagedus** – see näitab, kas makse tehakse kord kuus, kord kvartalis, kord poole aasta tagant või kord aastas. Lõppkuupäev arvutatakse automaatselt alguskuupäeva ja sisestatud perioodide arvu alusel.

- **Maksegraafik** – See on arvutatud praegune väärtus, mis põhineb kõikide rendimaksete perioodi pikkusel, maksete summal, liitperioodidel ja annuiteedi tüübil.

- **Perioodid** – need on rendiperioodid, mis kajastavad liitintervalli ja annuiteedi tüüpi. Liitintervall määrab, kuidas perioode jagatakse. Saate seada järgmised liitintervallid.

  - Kord kuus, 12 perioodi aastas
  - Kord kvartalis, 4 perioodi aastas
  - Kord poole aasta tagant, 2 perioodi aastas
  - Kord aastas, 1 periood aastas

Esimene periood algab nullist, kui annuiteedi tüüp on perioodieelne annuiteet. Muul juhul algab esimene periood number ühega, kui annuiteedi tüüp on perioodijärgne makse.

- **Kuud** – see näitab kalendrikuude arvu rendilepingu kehtivuse jooksul. Maksesumma on tasumisele kuuluv summa, mis on määratud maksete sageduses. Arvutatud praegune väärtus hõlmab praegusel väärtusel põhinevat rendimakset perioodi kohta, liitintervalle ja alternatiivset laenuintressimäära.

> [!NOTE] 
> Praegune väärtus arvutatakse diskonteeritud rahavoo võrrandi alusel.

- **Raamatud** – see on eelkonfigureeritud seadistus, mis seotakse iga rendiga. Raamat määratleb rakendatud raamatupidamisstandardi, rendi tüübid ja läve, mida kasutatakse klassifikatsioonitestide alusena. Klassifikatsiooniteste kasutatakse rendi tüübi automaatseks määramiseks.

- **Raamatupidamisraamistik** – see näitab valitud raamatupidamisstandardit, kas IFRS 16 või ASC 842, mida toetate. Raamatupidamisstandard on määratud raamatus, mis on rendiga seotud. Raamatupidamisstandard määratleb pearaamatu kontod, mis on täpsustatud sisestusreeglites.

- **Rendi tüübid** – see näitab, kas tegemist on kapitali- või kasutusrendiga. Kapitalirendi korral vastutab renditud varaga seotud riskide ja hüvede eest rentnik. Kasutusrendi korral jäävad renditud varaga seotud riskid ja hüved rendileandja vastutada. Kolmas suvand on tuvastada rendi tüüp automaatselt (kas kapitali- või kasutusrent), võttes arvesse raamatus määratletud lävesid. See automaatne tuvastamine tehakse rendi ümberklassifitseerimise testi ajal.

- **Läved** – seda kasutatakse rendi klassifikatsioonitestides, et määrata, kas vara on liigitatud üheks järgmistest.

  - **Rendiperiood** – see on klassifikatsioonitestis kasutatava kasuliku tööea protsent. Süsteem liigitab rendi kapitalirendiks, kui rendi tüüp on seadistatud automaatseks ja kui rendiperiood vara kasuliku tööea jooksul on suurem kui siin määratletud protsent või sellega võrdne.

  - **Praegune väärtus** – See on klassifikatsioonitestis kasutatava vara õiglase väärtuse protsent. Süsteem liigitab rendi kapitalirendiks, kui rendi tüüp on seadistatud automaatseks ja kui tulevaste rendimaksete praegune väärtus on vara õiglase väärtuse põhjal suurem kui siin määratletud protsent või sellega võrdne.

  - **Lühiajaline rent** – kui rendiperiood on määratletud väärtusest väiksem või sellega võrdne, siis liigitatakse rent lühiajaliseks rendiks.

  - **Väike väärtus** – kui vara õiglane väärtus on määratletud väärtusest väiksem või sellega võrdne, siis liigitatakse rent väikese väärtusega rendiks.

  - **Rendi klassifikatsioon ja kanded** – rendi klassifikatsioon on automatiseeritud protsess, et liigitada rent raamatutes määratletud lävede ja muude klassifikatsioonitesti kriteeriumide põhjal, et teha kindlaks, kas rent on kapitalirent, kasutusrent, lühiajaline rent või väikese väärtusega rent. Seda kasutatakse ka selleks, et määrata, kas järgitakse edasilükatud rendi protsessi.

Klassifikatsioonitestid hõlmavad omandi üleminekut, ostuvalikut, rendiperioodi, praegust väärtust ja kordumatut vara. Järgmine diagramm illustreerib neid rendi klassifikatsiooniteste.

[![Rendi klassifikatsioonitestid.](./media/overview-03.png)](./media/overview-03.png)

Iga rendi tüübi puhul on raamatupidamine eri rendikannete puhul erinev. Kannete hulka kuuluvad esialgne tuvastamine, intressikulu, tasumisele kuuluv rendimakse ja rendikulum ning need põhinevad teie järgitavatel raamatupidamisstandarditel (IFRS 16 või ASC 842). Pearaamatukontod määratletakse iga kandetüübi ja raamatupidamisraamistiku jaoks rendi sisestusreeglites.

## <a name="asset-leasing-transactions"></a>Vara rentimise kanded

#### <a name="initial-recognition"></a>Esialgne tuvastamine 
Renditava vara esialgne tuvastamine kasutab arvutatud praegust väärtust, et seda saaks bilansis kajastada. Selle jaoks luuakse raamatupidamiskirje automaatselt. See kanne debiteerib kasutamisõiguse esemeks olev vara kontot ja krediteerib kasutusrendi kohustise kontot järgmiselt. Kui rendiga on seotud põhivara, kajastub esialgse tuvastamise kanne põhivara soetamisena. Selle stsenaariumi puhul peate määratlema põhivara sisestusreeglid, et sisestada kasutamisõiguse esemeks olev vara kontole. 

> [!NOTE]
> Kasutusrenti toetab ainult USA GAAP (ASC 842).

|     Tüüp                                          |     Deebet                     |     Kreedit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Kasutusrent US GAAP alusel            |     Kasutamisõiguse esemeks olev vara        |     Kasutusrendi kohustis     |
|     Kapitalirent IFRS-i ja USA GAAP põhjal      |     Kasutamisõiguse esemeks olev vara        |     Kapitalirendi kohustis       |

#### <a name="lease-liability-amortization-interest-expense"></a>Rendikohustise amortisatsioon (intressikulu) 
Rendi intress tuvastatakse, arvutades järgmised väärtused: rendi algbilanss, perioodi rendimakse, intressimäär ja liitintervalli perioodid aastas. Intressisumma suurendab kasutusrendi kohustise kontot seda krediteerides, mis kajastub organisatsiooni bilansis. Kanne hõlmab ka intressikulu konto debiteerimist, mis kajastub kapitalirendi puhul kasumiaruandes ning kasutusrendi puhul rendikulu kontol.

|     Tüüp                                          |     Deebet                     |     Krediit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Kasutusrendi kohustise kirje USA GAAP (ASC 842) põhjal    |     Rendikulu         |     Kasutusrendi kohustis         |
|     Kapitalirendi kohustis IFRS-i ja USA GAAP põhjal      |     Intressikulu          |     Kapitalirendi kohustis           |

#### <a name="accrued-lease-payment"></a>Akumuleerunud rendimakse
Akumuleerunud rendimakse on tulevane rendimakse, mida töödeldakse maksekandena panga- või sularahakontolt. Tasumisele kuuluv rendimakse vähendab rendikohustist, debiteerides rendikohustise kontot selle põhjal, kas hankija alammoodul on rendileandja puhul määratletud hankijana, või sisestades kreediti poole tasumisele kuuluvate vekslite pearaamatukontole, pärast mida tehakse makse kas hankija või tasumisele kuuluvate vekslite põhjal.

|     Tüüp                                          |     Deebet                     |     Kreedit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Kasutusrent US GAAP alusel              |  Kasutusrendi kohustis    |   Hankija kohustis (alammoodul) / tasumisele kuuluvad vekslid  |
|     Kapitalirent IFRS-i ja USA GAAP põhjal        |  Kapitalirendi kohustis      |   Hankija kohustis (alammoodul) / tasumisele kuuluvad vekslid  |

#### <a name="asset-depreciation"></a>Vara kulum
Kasutamisõiguse esemeks olev vara amortiseeritakse selle põhjal, kumb on kõige lühem: vara kasulik tööiga või rendiperiood. US GAAPi kasutusrendi (ASC 842) kulumiarvestuse meetod põhineb lineaarse rendikulu ja intressisumma vahelisel erinevusel. Kapitalirendi kulum arvutatakse standardse lineaarse meetodi abil. Rendikulum mõjutab intressikulu debiteerides kasumi ja kahjumi väljavõtet. Bilanssi mõjutab kapitalirendi akumuleeritud kasutamisõiguse esemeks olev vara krediteerimine. Kui rent on seotud põhivaraga, tehakse kulumikanded ainult põhivarade moodulist. 

|     Tüüp                                          |     Deebet                     |     Kreedit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Kasutusrent US GAAP alusel              |  Rendikulu                |   Kasutamisõiguse esemeks olev vara akumuleeritud kulum     |
|     Kapitalirent IFRS-i ja USA GAAP põhjal        |   Kasutamisõiguse esemeks olev vara kulu kulum   |   Kasutamisõiguse esemeks olev vara akumuleeritud kulum    |

#### <a name="short-term-lease"></a>Lühiajaline rendileping
Lühiajaline rent kajastatakse kuluna, mis mõjutab organisatsiooni kasumiaruannet. Loodud tasumisele kuuluv rendimakse debiteeritakse rendikulu kontol ja krediteeritakse tasumisele kuuluvate vekslite või hankija alammooduli kontol.

|     Tüüp                                          |     Deebet                     |     Kreedit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Lühiajalise rendi kirje IFRS-i ja USA GAAP põhjal     |  Rendikulu                |   Hankija kohustis (alammoodul) / tasumisele kuuluvad vekslid  |

#### <a name="low-value-lease"></a>Väikese väärtusega rent
Väikese väärtusega rent kajastatakse kuluna, mis mõjutab teie organisatsiooni kasumiaruannet. Loodud tasumisele kuuluv rendimakse debiteerib rendikulu ja krediteerib tasumisele kuuluvaid veksleid või hankija alammoodulit.

|     Tüüp                                          |     Deebet                     |     Kreedit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Väikese väärtusega rendi kirje IFRS-i ja USA GAAP põhjal      |  Rendikulu                |   Hankija kohustis (alammoodul) / tasumisele kuuluvad vekslid  |


#### <a name="index-revaluation"></a>Indeksi ümberhindamine
See on vara rentimise konto muutuvate rendimaksete jaoks, mida mõõdetakse indeksimäära põhjal. Indeksimäära kõikumistest põhjustatud rendimaksete muutused kujutavad endast IFRS 16 põhjal rendi korrigeerimist. Rendikohustist ja kasutamisõiguse esemeks olevaid varasid korrigeeritakse uute maksete arvestamiseks. 

|     Tüüp                                          |     Deebet                             |     Kreedit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Indeksi ümberhindamise kirje IFRS-i põhjal suurenemise korral  |  Kasutamisõiguse esemeks olev vara       |   Kasutusrendi kohustis |
|   Indeksi ümberhindamise kirje IFRS-i põhjal vähenemise korral  |  Kasutusrendi kohustis  |   Kasutamisõiguse esemeks olev vara      |

Kui maksed muutuvad indeksimäära muutumise tõttu, muutuvad ainult muutuvad maksed, välja arvatud juhul, kui rahavood muutuvad veelgi, nagu näiteks indeksimääraga seotud renditingimuste muutumise korral USA GAAP (ASC 842) põhjal.

#### <a name="lease-adjustment"></a>Rendi korrigeerimine
Vara rentimise funktsioon võimaldab renti korrigeerida, kui rendiperioodi muudetakse, rentimist pikendatakse või kui on veel tingimusi, mille alusel rent vajab korrigeerimist. Rendi korrigeerimised sisestatakse kasutamisõiguse esemeks olev vara ja rendikohustise suurendamiseks või vähendamiseks. Korrigeerimise protsess kasutab kohustise amortisatsiooni ja varabilansi ülekantavaid lõppbilansse korrigeerimise kuupäeva seisuga. Kui rent on seotud põhivaraga, sisestatakse kasutamisõiguse esemeks olev vara korrigeerimine, kasutades põhivarades määratud ID-d. 

|     Tüüp                                          |     Deebet                             |     Kreedit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Rendi korrigeerimise kanne IFRS-i ja USA GAAP puhul suurenemise korral     |  Kasutamisõiguse esemeks olev vara       |   Kasutusrendi kohustis |
|   Rendi korrigeerimise kanne IFRS-i ja USA GAAP puhul vähenemise korral     |  Kasutusrendi kohustis  |   Kasutamisõiguse esemeks olev vara      |


#### <a name="lease-impairment"></a>Renditava vara väärtuse langus
See kajastab kasutamisõiguse esemeks olev vara ülekantavat bilansi vähendamist. Tuvastage väärtuse languse summa, kande kuupäev ja järelejäänud perioodid. Allesjäänud kasutamisõiguse esemeks olev vara amortiseeritakse lineaarselt. Renditava vara väärtuse languse loogika arvestab vara ülekande väärtust, mis on vara kulumigraafikus.  

|     Tüüp                                          |     Deebet                             |     Kreedit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Väärtuse languse kirje IFRS-i ja USA GAAP jaoks           |  Väärtuse languse kulu                   |    Kasutamisõiguse esemeks olev vara     |

>[!NOTE]
> Kui rent on seotud põhivaraga, tuleb renditava vara väärtuse langus sisestada põhivarade moodulist, kuna vara kulumit käitatakse põhivarade moodulist.

**Topeltvaluuta** – rendikandeid saab sisestada arvestus- ja aruandlusvaluutast erinevas valuutas. Valuuta vahetuskurss määratletakse pearaamatus alguskuupäeval. Valuutakursse saate muuta, kui määrate rendi loomisel välja **Fikseeritud kurss** väärtuseks **Jah**. Rendikannete sisestamisel kasutatakse esialgse tuvastamise ja järgnevate kulumikannete jaoks alguskuupäeval kehtinud vahetuskurssi. Järgnevad makse- ja intressikanded kasutavad praegust aktiivset vahetuskurssi. 

## <a name="create-an-asset-lease"></a>Renditava vara loomine
Uue renditava vara loomiseks läbige järgmised etapid. 

1. Funktsiooni **Vara rentimine** kasutamiseks peate selle lubama tööruumis **Funktsioonihaldus**. Valige tööruumis **Funktsioonihaldus** suvand **Kõik**, et kõik funktsioonid oleksid lehel loetletud. Valige **Vara rentimine** ja seejärel valige **Luba kohe**.
2. Avage **Vara rentimine > Ühine > Rendi kokkuvõte**. Sisestage kiirkaardil **Üldine** vajalikud väljad. 
   - **Rendi üksikasjad**
   - **Vara kasulik tööiga (kuudes)**
   - **Rendigrupp**
   - **Alternatiivne laenuintressimäär (%)**
   - **Liitintervall**
   - **Annuiteedi tüüp**
   - **Valuuta**
   - **Alguskuupäev**

3. Avage kiirkaart **Maksegraafiku read** ja sisestage makserida ning seejärel valige **Loo graafikud**.

4. Valige **Raamatud**. 

5. Aktiveerige kiirkaart **Üldine**. Arvutatakse **Esialgne kasutamisõiguse esemeks olev vara** ja **rendikohustis**. 

6. Avage kiirkaart **Rendi klassifikatsioonitest**, et kontrollida välja **Rendi tüüp** väärtust. 

   Automaatne **rendi tüüp** liigitatakse kriteeriumide alusel, mis on määratletud lehel **Raamatud**.

7.  Avage **Maksegraafik**, mis asub jaotises **Funktsioon**.  

   Lehel **Maksegraafik** on loetletud rendi ID tulevased maksegraafikud. Valige **Kinnita graafik**, et saaksite sisestada **esialgse tuvastamise** kanded. 

[![Esialgse tuvastamise funktsioon.](./media/overview-13.png)](./media/overview-13.png)

8. Valige **Esialgne tuvastamine**, et luua esialgse tuvastamise tööleht. 

9. Valige **Vara rentimise töölehed**, et sisestada esialgse tuvastamise kanne. 

   Maksegraafikust saate avada üksikasjaliku lehe, kus on loetletud kasutamisõiguse esemeks olev vara kanded. 
 
   **Rendikohustise amortisatsioonigraafik** näitab iga perioodi jaoks arvutatud intressisummat.
   
10. Looge tööleht ja seejärel avage **Vara rentimise töölehed**. **Rendikohustise amortisatsioonigraafik** näitab ka intressikandeid.

   Lehel **Vara kulumigraafik** kuvatakse valitud rendi ID kulumikanded. 

   [![Kasutamisõiguse esemeks olev vara kande leht.](./media/overview-20.png)](./media/overview-20.png)

   Lehel **Kasutamisõiguse esemeks olev vara** loetletakse esialgne tuvastamine, akumuleerunud kulum ja vara saldo. 

   Lehel **Rendikohustise kanded** kuvatakse esialgne tuvastamine, rendi intressimakse, rendimakse ja rendikohustise saldo. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
