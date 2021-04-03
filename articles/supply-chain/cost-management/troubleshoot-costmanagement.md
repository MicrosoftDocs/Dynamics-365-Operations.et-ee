---
title: Kuluhalduse tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada kuluhaldusega töötamisel tekkivaid probleeme.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: dceaca64132857d796a16c2450a372ba05712cf5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262449"
---
# <a name="troubleshoot-cost-management"></a>Kuluhalduse tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada kuluhaldusega töötamisel tekkivaid probleeme.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funktsionaalsed lüngad varude väärtuse/vananemise aruannete ja nende ladustamise versioonide vahel

[Lao vananemise aruande ladustamise](inventory-aging-report-storage.md) ja [Varude väärtuse salvestamise aruande](inventory-value-report-storage.md) funktsioonid võimaldavad Supply Chain Managementil kuvada suuremahulisi laokandeid. Igal juhul salvestatakse aruande tulemused sirvimiseks ja eksportimiseks, erinevalt nende aruannete mitteladustatavatest versioonidest. Kuid mõned funktsioonid, mis on olemas nende aruannete mitteladustatavates versioonides, pole ladustamisversioonides olemas. Järgmised jaotised summeerivad erinevused ja annavad lahendused.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Ladustamise aruanded ei sisalda vahesummasid, isegi kui need on aruande kavandis lubatud.

Vahesummad võivad põhjustada probleeme, kui tulemus eksporditakse, eriti siis, kui kasutajad muudavad kirje järjestust.

Vahesummade kontrollimiseks saate tulemuse eksportida Microsoft Excel-isse. Teise võimalusena, kui soovite kontrollida vahekokkuvõtteid Supply Chain Managementi siseselt, kasutage [Funktsioonide haldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lubada *Uue ruudustiku juhtelemendi* ja *(Eelvaade) rühmitamise ruudustiku* funktsioonid, mis annavad palju paindlikuma viisi, et vaadata iga grupi jaoks veeru alusel vahekokkuvõtet. Lisateavet vt jaotisest [Ruudustiku võimalused](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Varude väärtuse ladustamise aruanne ei toeta pearaamatu konto teavet.

Saate kasutada protsessi saldot, et saada lao kontode saldo ja võrrelda seda **Varude väärtuse ladustamise** aruandega.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Pearaamatu perioodi oleku muutmisel lao sulgemiseta kuvatakse hoiatused või tõrked.

Microsoft kehtestas järgmised kinnitused, et vältida probleeme, mis on põhjustatud vale perioodi lõpu protsessist omahinna arvutamisel. Kui ilmneb mõni järgmistest tõrketeadetest, vaadake [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3), et saada lisateavet nende probleemide lahendamise kohta.

- Olete käivitamas ümberarvutust kuupäevaga %1 (10.02.2019). Viimane registreeritud ümberarvutus teostati eelmises perioodis kuupäevaga %2 (20-01-2019). Kuupäevaga %3 (31-01-2019) sobiva perioodi lõpuga varude sulgemist ei ole registreeritud. Ärge unustage käitada lao sulgemist %3 (31-01-2019), mis ühtib perioodi lõpuga. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on täidetud.

- Olete muutmas pearaamatu perioodi väärtuselt %1 väärtusele %2. Kuupäevaga %3 sobiva perioodi lõpuga varude sulgemist ei ole registreeritud. Käivitage enne oleku muutmist lao sulgemine kuupäevaga %3, mis ühtib perioodi lõpuga. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on täidetud. Juriidilisest isikust teavitatud %4. Praegu on see informatiivne, kuid tulevikus peate seda tegevust tegema.

- Konto struktuuri %1 on muudetud. Ühte või mitut põhikontot %2 pole enam olemas. Need põhikontod on nõutud kuupäevaks %3 kuupäevaga %4. Palun lisage need põhikontod konto struktuuri %1, enne kui saate %3 tööd jätkata. Praegu on see informatiivne, kuid tulevikus peate seda tegevust tegema.

- Olete käivitamas lao sulgemist kuupäevaga %1 (31-01-2019). Perioodi lõpukuupäevaga %2 (31-01-2019) sobivat omahinna tagasiarvestust ei ole registreeritud. Palun teostage perioodi lõpukuupäevaga %3 (31-01-2019) sobiv omahinna tagasiarvestus. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni see on täidetud.

- Olete käivitamas omahinna ümberarvutust kuupäevaga %1 (28-02-2019). Viimane registreeritud omahinna ümberarvutus teostati eelmises perioodis kuupäevaga %2 (31-01-2019). Perioodi lõpukuupäevaga %3 (31-01-2019) sobivat varude sulgemist ei ole registreeritud.
Ärge unustage käitada perioodi lõpukuupäevaga %3 (31-01-2019) ühtivat lao sulgemist. Varude hindamine, müüdud kaupade kulu ja erinevused ei pruugi olla abiraamatu või pearaamatu puhul õiged, kuni varude sulgemine on teostatud.

## <a name="inventory-aging-report-discrepancies"></a>Varude ajalise jaotuse aruande lahknevused

**Varude aegumise aruandes** kuvatakse erinevate ladustamise dimensioonide (nt saidi või lao) kuvamisel erinevad väärtused. Lisateavet aruandluse loogika kohta vt [Varude vananemise aruande näited ja loogika](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Uuenduse vastuolu ilmneb, kui varude hinna määramise meetod on kas standardne kulu või libisev keskmine

Kui sisestate dokumente, nt laotöölehti, ostutellimuse arveid või müügitellimuste arveid paralleelselt skaleeritavuse ja jõudluse huvides, võite saada tõrketeate uuenduse vastuolu kohta ja mõningaid dokumente ei pruugita sisestada. See probleem võib ilmneda, kui varude hinna määramise meetod on kas *standardne kulu* või *libisev keskmine*. Mõlemad meetodid on pideva keskmise põhimõttel tuginevad kuluarvestusmeetodid. Teisisõnu määratletakse lõplik kulu sisestamise ajal.

Kui kasutate meetodit *Liikuv keskmine*, sarnaneb veateade järgmisele näitele.

> Laoväärtust xx.xx ei oodata pärast proportsionaalse kulu arvutamist

Kui kasutate meetodit *Standardkulu*, sarnaneb veateade järgmisele näitele.

> Standardkulu ei kattu pärast uuendamist finantsilise laovaru väärtusega. Väärtus = xx,xx, kogus = yy,yy, standardkulu = zz,zz

Kuni Microsoft annab probleemi lahendamiseks välja lahenduse, kaaluge järgmiste lahenduste kasutamist nende tõrgete vältimiseks või vähendamiseks.

- Postitage nurjunud dokumendid uuesti.
- Looge dokumente, millel on vähem ridu.
- Vältige standardkulus kümnendkohaga väärtusi. Proovige määratleda standardnkulu nii, et välja **Hinna kogus** väärtuseks oleks seatud *1*. Kui peate määrama **hinna koguse** väärtuseks üle *1*, proovige vähendada kümnendkohtade arvu ühiku standardkulus. (Ideaaljuhul peaks see olema alla kahe komakoha.) Näiteks vältige standardsete kulusätete, näiteks **Hind** = *10* ja **Hinna kogus** = *3*, kuna need tekitavad ühiku standardkulu 3,333333 (kus kümnendväärtus kordub).
- Vältige enamikes dokumentides mitme rea omamist, millel on sama tootekombinatsioon ja finantsiliste varude dimensioon.
- Vähendage paralleelsuse astet. (Sel juhul võib süsteem muutuda kiiremaks, sest tekib vähem uuenduse vastuolusid ja uuesti tegemist.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]