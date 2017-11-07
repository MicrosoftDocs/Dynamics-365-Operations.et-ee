---
title: "Standardkulu teisendamise ülevaade"
description: "See artikkel annab protsessiülevaate, mis aitab teil standardkulu teisendust seadistada ja käitada. Nimetatud toimingud on mõeldud tegemiseks pärast standardkulu teisenduse eeltingimuste täitmist."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2e59fd6e137d5f677ed4055385ef88922c8c42ba
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="standard-cost-conversion-overview"></a>Standardkulu teisendamise ülevaade

[!include[banner](../includes/banner.md)]


See artikkel annab protsessiülevaate, mis aitab teil standardkulu teisendust seadistada ja käitada. Nimetatud toimingud on mõeldud tegemiseks pärast standardkulu teisenduse eeltingimuste täitmist. 

Kasutage lehte **Standardkulude teisendused**, et teisendada valitud kaubapartii laomudel tegeliku kulu mudeli asemel standardkulu mudeliks. Teisendusprotsess hõlmab eeltingimusena lao sulgemist, üleminekuperioodi jooksul mitme sammu tegemist (mis on määratud ülemineku algus- ja lõppkuupäevaga) ning seejärel teisendamist ja sellega seotud lao sulgemist.

-   Lao sulgemine enne üleminekuperioodi – lao sulgemine kujutab endast eeltingimuse etappi, sest see tasakaalustab kauba avatud kanded vana hinnamääramismeetodi abil. Üleminekuperioodi jooksul, saate lisada ja sisestada tagasiulatuvaid kandeid, näiteks arveid, et eelmine periood sulgeda. Lao sulgemise kuupäev peab olema üks päev enne ülemineku alguskuupäeva, et tagada puhas üleminek vanalt hinnamääramismeetodilt.
-   Teisendamise sammud üleminekuperioodi jooksul – kasutage lehte **Standardkulu teisendused**, et luua teisenduskirje, mis sisaldab ka uue kuluarvestuse versiooni kasutaja määratud identifikaatorit. Tuvastate kaubad, mis nõuavad teisendust, ja sisestate siis kauba ootel standardkulud uude kuluversiooni. Kontrollite valitud kaupu, et tuvastada probleemid, mis võivad teisendamist takistada, lahendate probleemid ja kontrollite siis veel kord. Kui kaubad on kontrollimise edukalt läbinud, määrate teisenduskirje olekuks **Valmis**. Plaanitud teisendamiskuupäeval sooritate teisenduse ja lisate soovi korral lao sulgemise. Kauba laoliikumised üleminekuperioodil sisestatakse ja hinnatakse vana laomudeli alusel. Seejärel, pärast edukat teisendamist, hinnatakse laoliikumised ümber standardkuluks.
-   Lao sulgemine enne teisendamist – lao sulgemise saab kaasata teisendamise osana planeeritud teisendamise kuupäeval või saab selle sooritada eraldi sammuna enne teisendamist.

Kui teisendusprotsess on edukalt lõpule viidud, põhineb iga kauba laomudel standardkulul ja kauba standardkuul on lubatud. Järgnevad laokanded hinnatakse kauba standardkulu alusel. Lisaks teisendab süsteem kauba sissetulekute ja väljaminekute füüsilised laokanded standardkuluks teisendamise kuupäeva põhjal. Süsteem teisendab ka kauba finantsilise vaba kaubavaru standardkuluks ja sisestab väärtuse erinevuse laovarude ümberhindamisena. Kõik kanded, mis toimuvad pärast teisendamist, hinnatakse kauba standardkulu alusel. Te ei saa enne teisenduse kuupäeva sisestada tagasiulatuvaid kandeid, kuna varude sulgemist tuleb teha üks päev enne teisenduse kuupäeva. Teisendust saab teha ainult siis, kui varude sulgemine tehti üks päev varem. Seda lao sulgemist ei saa tühistada.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Määratlege standardse kulu teisenduskirje ja sellega seotud kuluversioon
Kasutage teisenduskirje loomiseks lehte **Standardkulu teisendused**. Uue teisenduskirje saab luua ainult juhul kui olemasolevad teisenduskirjed on lõpetatud. Planeeritud ülekandeperioodi kestus määratletakse ülekande alguskuupäeva ja planeeritud konversioonikuupäevaga. Plaanitud üleminekuperiood võib kesta vaid ühe päeva. Plaanitud üleminekuperiood aitab tagada, et teisendusprotsessil on piisavalt aega kõigi etappide läbimiseks. Lao sulgemine peab olema tehtud üks päev enne ülemineku alguskuupäeva, et tasakaalustused oleksid lõpetatud enne teisendusprotsessi alustamist. Veendumaks, et ülemineku alguskuupäev ja lao sulgemise kuupäev on õigesti järjestatud, saate muuta ülekande alguskuupäeva nii, et seal oleks kuupäev, mis oleks üks päev hilisem kui olemasolev lao sulgemine, või sulgeda lao. Teisenduskirjet sisestades sisestate uuele kuluversioonile ka kasutaja määratletud identifikaatori, mis sisaldab teisendatud kaupade standardkulusid. Kuluarvestuse versioon luuakse teisenduskirje salvestamisel automaatselt.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. Teisenduskirje uue kuluversiooni ülevaatamine ja muutmine
Uus kuluarvutuse versioon on määratud teisenduskirjele, nagu näitab kuluarvestuse tüüp **Teisendus**. Vastav kuluversioon sarnaneb standardsete kulude kuluversioonile ja sisaldab teisenduskirjega seotud kaupade kulukirjeid. Teisenduskirje kuluarvutuse versioonil on järgmised sätted, mis tuleks üle vaadata ja mida tuleks mitmesugustel vahekaartidel vajaduse järgi muuta.

-   **Kuluarvutuse tüüp:** selle välja säte peab olema **Standardkulu**.
-   **Versioon:** ID kajastab teavet, mis on sisestatud kuluversiooni ID teisenduskirjele.
-   **Nimi:** vaikimisi on nimi tühi. Saate soovi korral nime sisestada.
-   **Blokeeri:** selle välja väärtus peab olema **Ei**. Saate sisestada kuluarvutuse versiooni kulukirjeid, kuni teisenduskirje olekuks on määratud **Valmis**. Olek **Valmis** näitab, et valitud üksused on kontrollitud ja et kulukirjete muudatused ei tohiks olla lubatud.
-   **Blokeeri aktiveerimine:** selle välja väärtus peab olema **Jah**. Ootel kulukirjet ei saa sellele määratud kuluarvutuse versioonis käsitsi aktiveerida. Aktiveerimine toimub teisendamisel.
-   **Alguskuupäev:** alguskuupäev kajastab teisenduskirjesse sisestatud teisendamise planeeritud kuupäeva.
-   **Laoala:** jätke see väli tühjaks, et iga laoala kohta saaks kulukirjeid sisestada.
-   **Luba hinna tüübi väljagrupp:** määrake selle välja väärtuseks **Jah**, et sisestada saaks ainult omahinna kirjeid.
-   **Taande põhimõte:** selle väärtuseks on määratud **Pole**. Määrake taande põhimõtteks **Aktiivne**, kui vajate kuluteavet, mis on muudes kuluarvutuse versioonides aktiveeritud. Näiteks võib olla vaja kuluteavet komponentide, kulukategooriate ja kaudsete kulude kohta, et arvutada toodetud kaupade kulusid.
-   **Taanda kuluarvutuse versioon:** jätke see väli tühjaks.

Kauba kuluteavet sellele määratud kuluarvutuse versioonis saab hallata ainult lehelt **Standardkulu teisendused**. Teisenduse ajal ei saa kuluarvutuse versiooni kulude arvutamiseks kasutada lehte **Kuluarvutuse versiooni seadistus** või **Kuluarvutuse versiooni hooldus**. Kuid saate kasutada neid lehti kuluarvutuse versiooni haldamiseks pärast teisendusprotsessi lõpuleviimist.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. Tuvastage kaubad, mis teisendatakse standardseks kuluks.
Tuvastage lehel**Standardkulu teisendused** eraldi üksused, mis tuleks standardkuluks teisendada. Lehel **Lisa üksusi standardkulu teisendusele** saate lisada mitu üksust. Üldjuhul peaksite lisama kõik toodetud kaubad ühte teisenduskirjesse, mis aitab tagada kulude õige arvutamise.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. Sisestage või arvutage iga kauba puhul ootel standardsed kulud, mida teisendatakse.
Kasutage lehte **Kauba hind**, et sisestada ootel standardkulud vastava kuluversiooni raames ostetud kaupade ja üleviidavate kaupade jaoks. Kulukirjed on laoalapõhised ja kauba ootel kulud tuleb sisestada iga laoala puhul. Kasutage lehte **Kauba hind**, et arvutada ootel standardkulud toodetavate kaupade jaoks. Toodetava kauba ootel kulud tuleb arvutada iga tootmiskoha jaoks, kui laoalaks pole üleviimisala. Sel juhul tuleb ootel kulud käsitsi sisestada. Mõnel kaubal võivad olla värvi, suuruse või konfiguratsiooni tootedimensioonid. Lehel **Standardkulu teisendused** näitab märkeruut **Kasuta omahinda variantide alusel** iga tootedimensioonide kombinatsiooni standardkulu. Kui see märkeruut on tühjendatud, tuleb kauba jaoks sisestada ainult ootel kulu.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. Kontrollige ja lahendage teisendatavate kaupade puhul kõik probleemid.
Aruande **Standardkulude teisendamise kontrollimine** abil saate tuvastada probleeme teisendatavate kaupadega. Kui kaubal pole ühtegi probleemi, määratakse selle olekuks teisenduskirjes **Kontrollitud**. Kui kaubal on probleeme, tuleb probleemid lahendada ja käivitada siis aruande uuesti, kuni kauba olekuks määratakse **Kontrollitud**. Kui te kaubaga seotud probleeme õigeaegselt lahendada ei suuda, saate kauba valikuliselt teisenduskirjest kustutada ja teisendada kauba hiljem.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Muutke teisenduskirje olek väärtusele Valmis
Kui teisenduskirje olekuks määratakse **Valmis**, teeb süsteem lõpliku kontrollimise enne standardkulu teisendamist. Olekuks määratakse **Valmis** ainult juhul, kui täidetud on järgmised tingimused.

-   Iga teisenduskirje üksuse olek on **Kontrollitud**.
-   Lao sulgemine tehti kuupäeval, mis on üks päev enne ülemineku alguskuupäeva. Veendumaks, et ülemineku alguskuupäev ja lao sulgemise kuupäev on õigesti järjestatud, saate muuta ülekande alguskuupäeva nii, et seal oleks kuupäev, mis oleks üks päev hilisem kui olemasolev lao sulgemine, või sulgeda lao.

## <a name="7-back-up-the-database-before-conversion"></a>7. Varundage andmebaas enne teisendamist
Varukoopia võimaldab andmebaasi taastada, kui teisendamise käigus peaksid ilmnema tõrked.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Tehke teisendamine, kui teisenduskirjel on olek Valmis.
Teisendusprotsessi puhul on vaja, et lao sulgemine oleks tehtud kuupäeval, mis on üks päev enne plaanitud teisendamise kuupäeva. See nõue aitab tagada, et tagasiulatuvaid kandeid ei saa üleminekuperioodil sisestada. Kui lao sulgemist pole veel tehtud, küsitakse teilt, kas soovite seda teisendusprotsessi käigus teha. Teisendusprotsess käsitleb korraga ühte kaupa. See alustab tootestruktuuri madalaimatest üksustest, tuginedes kauba madala taseme koodile. Kui üksus on edukalt teisendatud, määratakse selle olekuks teisenduskirjes **Teisendatud**. Kui teisendusprotsess katkestatakse, on kõigil kaupadel, mida pole edukalt teisendatud, olek **Kontrollitud**. Teisendusprotsessi edukal lõpetamisel on järgmine mõju.

-   Teisenduskirje olekuks määratakse oleku **Valmis** asemel **Lõpetatud** ja iga valitud üksuse olekuks määratakse oleku **Kontrollitud** asemel **Teisendatud**.
-   Teisendatud kaupade mudeligrupp on muudetud nii, et see kajastab uut standardkulu laomudeliga gruppi.
-   Teisendatud kaupade standardkulud on vastava kuluversiooni raames lubatud.
-   Kuluarvutuse versiooni kuluarvutuse tüübiks on määratud tüübi **Teisendus** asemel **Standardkulu** ja kuluarvutuse versioon sarnaneb nüüd teistele standardkulude arvestuse versioonile.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. Kontrollige ja viige vastavusse laovarude väärtused teisendatud kaupade puhul.
Aruanne **Hälbe analüüsi väljavõte** võimaldab analüüsida ümberhindluse hälvet ja aruanne **Laoväärtus** võimaldab vaadata laoväärtust konkreetsel kuupäeval.

-   Analüüsige ümberhindluse hälbed. Kasutage aruannet **Hälbe analüüsi väljavõte**, et vaadata lao ümberhindluse hälbeid teisendatud kaupade puhul. Samuti saate kasutada lehte **Standardkulu kanded**, et vaadata lao ümberhindluse kandeid teisendatud laovarudega kaupade puhul.
-   Analüüsige laoväärtust enne üleviimise alguskuupäeva. Aruande **Laoväärtus** abil saate teisendatud kaupade laoväärtusi vaadata. Aruande väärtusena Lõppkuupäev kasutage päeva, mis on üks päev enne ülemineku alguskuupäeva.
-   Analüüsige laoväärtust enne teisendamise kuupäeva. Aruande **Laoväärtus** abil saate teisendatud kaupade laoväärtusi vaadata. Aruande väärtusena Lõppkuupäev kasutage päeva, mis on üks päev enne ülemineku kuupäeva.
-   Analüüsige laoväärtust teisendamise kuupäeval. Kasutage aruannet **Laoväärtus**, et vaadata laoväärtusi teisendamise kuupäeva seisuga. Nii aruande algus- kui ka lõppkuupäev peaksid vastama teisendamiskuupäevale. Aruande valikukriteerium peab kajastama teisendatud kaupu.
-   Analüüsige tagasiulatuvaid laoliikumisi. Kasutage aruannet **Laoväärtus**, et vaadata tagasiulatuvaid laoliikumisi, mis sisestati pärast teisendamist. Aruande algus- ja lõppkuupäev peaksid vastama ülemineku alguskuupäevale ja teisendamise kuupäevale miinus üks päev. Aruande valikukriteerium peab kajastama teisendatud kaupu. Aruanne näitab laoliikumisi, mis ülekandeperioodi jooksul standardkuluga tehti.


<a name="see-also"></a>Vt ka
--------

[Standardkulu teisendamise eeltingimused](prerequisites-standard-cost-conversion.md)




