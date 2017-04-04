---
title: "Intressikoodile intressimäära seadistamine"
description: "Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Intressikoodile intressimäära seadistamine

Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul.

Saate seadistada ühe intressikoodi ja rakendada seda mitme kliendi sisestusreeglitele, arvelduskoodidele või kindlatele arveridadele. Intressikoodi üksikasjade muutumisel rakendavad kõik koodi kasutavad funktsioonid muutusi automaatselt uutele kannetele. Iga intressikoodi puhul saate seadistada kaht tüüpi määrasid.
-   Intressitulu määrad − need kujutavad endast tulu, mis on saadud arvete ja viivisearvete intressidest.
-   Intressimaksete määrad − need kujutavad endast kulu, mis tasutakse kreeditarvete intressidena.

Mõlemad määratüübid võivad eksisteerida samal ajal ja samas intressikoodis. Intressimäärad võivad põhineda kolmel arvutamistüübil.
-   Intress protsendi järgi.
-   Intress summa järgi.
-   Intress vahemiku järgi, mille tulemuseks on üksik protsent või summa.

Kui intressi arvutamiseks kasutatakse intressikoodi, luuakse iga intressimäära kohta eraldi viivisearve, mis kehtib seni, kuni makse on ületanud kande tähtaja. Vahekaardi **Tulud** abil lehel **Intressikood** saate seadistada intressimäärasid intressi jaoks, mida intressi küsides teenite. Makstava intressi määra seadistamiseks kasutage vahekaarti **Maksed**.

## <a name="interest-rates-based-on-a-percentage"></a>Protsendil põhinevad intressimäärad
Saate seadistada intressimäärad, mis arvutavad kindlaksmääratud protsendi.

-   Intressimäär kehtib kõigile valuutadele.
-   Sisestada saab valikulisi intressisumma limiite.
-   **Protsent** valitakse ** ** linnas on **arvutamiseks vastavalt** välja jäetud ning **huvi tähiste** lehekülg.

Nt kes hindab 5% intressi iga kahe kuu tagant mis arve ületab tehingu viivisekoodi seadistamiseks maksetähtaega, sisestage 2 on **arvutamiseks iga** välja ja valige **kuu**.

## <a name="interest-rates-based-on-amounts"></a>Summal põhinevad intressimäärad
Saate seadistada intressimäärad, mis arvutavad määratud summa valuuta kaupa.
-   Intressi summa määratakse iga intressikoodi valuuta jaoks.
-   Sisestada saab valikulisi intressisumma limiite.
-   ** Summa ** on valitud selle **arvutamiseks vastavalt** kohta välja ning **huvi tähiste** lehekülg.

Nt kes hindab 25,00 huvi iga 20 päeva mis arve ületab tehingu viivisekoodi seadistamiseks maksetähtaega, sisestage 20 ning **arvutamiseks iga** välja ja valige **päev**.

## <a name="interest-rates-based-on-ranges"></a>Vahemikel põhinevad intressimäärad
Saate seadistada intressimäärad, mis varieeruvad sõltuvalt tähtaja ületanud summast, summa hilinemise päevadest või kuudest.
-   Saate kasutada vahekaarti **Tulud valuuta järgi** konkreetsete intressisätete määratlemiseks iga valuuta jaoks. Siin saate määratleda ka vahemiku.
-   Lisage nupuga **Vahemikud** ridu, mis kajastavad vahemikke, mida seadistada soovite. Väärtus **Alates** kajastab vahemiku algust ja arv **Intressi väärtus** kajastab kas protsenti või summat, sõltuvalt valikust väljal **Intressi arvutusalus:** lehel **Intressikoodide seadistamine**.

## <a name="example-1-interest-by-range--amount"></a>Näide 1: Intress vahemiku järgi = summa
Saate seadistada intressikoodi, mis määrab intressi üks kord iga kolme kuu tagant, mil arve makse ületab kande tähtaega. Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele summaintervallidele. Intressi väärtus on 1 protsent arvesummadest kuni 1000.00, 2 protsenti summadest alates 1001.00 kuni 5000.00 ja 3 protsenti summadest, mis on suuremad kui 5000.00. Saate seadistada intressikoodi välja väärtused järgmiselt.

| **Välja nimi**                  | **Välja väärtus** |
|---------------------------------|-----------------|
| **Viivise kood**               | 3M%ByAmt        |
| **Arvuta intress iga**    | 3/kuu         |
| **Intress vahemiku järgi**           | Summa          |
| **Intressi arvutusalus:** | Protsent      |

Saate seadistada vahemiku andmed järgmiselt.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>Näide 2: Intress vahemiku järgi = päevad
--------------------------------------------------

Saate seadistada intressikoodi, mis määrab intressi üks kord iga 15 päeva tagant, mil arve makse ületab kande tähtaega. Soovite arvutuse aluseks võtta summapõhise intressiväärtuse, vastavalt astmelistele päevaintervallidele. Intressi väärtus on 10.00 15 päeva kohta esimese 60 päeva jooksul, 15.00 15 päeva kohta päevadel 61 kuni 90 ja 20.00 15 päeva kohta 91. päevast edasi. Saate seadistada intressikoodi välja väärtused järgmiselt.

| **Välja nimi**                  | **Välja väärtus** |
|---------------------------------|-----------------|
| **Viivise kood**               | 15DAmtXDay      |
| **Arvuta intress iga**    | 15/päev          |
| **Intress vahemiku järgi**           | Päevi            |
| **Intressi arvutusalus:** | Summa          |

Saate seadistada vahemiku andmed järgmiselt.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | sept.                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>Näide 3: Intress vahemiku järgi = kuud
----------------------------------------------------

Saate seadistada intressikoodi, mis määrab intressi üks kord iga kuu tagant, mil arve makse ületab kande tähtaega. Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele kuuintervallidele. Intressi väärtus on 1,5 protsenti kuus kolmel esimesel tähtaja ületanud kuul, 2,0 protsenti kuus järgmised kolm kuud ja 2,5 protsenti kuus kõigil järgnevatel kuudel. Saate seadistada intressikoodi välja väärtused järgmiselt.

| **Välja nimi**                  | **Välja väärtus** |
|---------------------------------|-----------------|
| **Viivise kood**               | 1M%ByMth        |
| **Arvuta intress iga**    | 1/kuus         |
| **Intress vahemiku järgi**           | Kuud          |
| **Intressi arvutusalus:** | Protsent      |

Saate seadistada vahemiku andmed järgmiselt.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Uued versioonid
Intressikoodidel on kehtivuskuupäevad. Kui soovite intressimäära muuta, saate luua **uue versiooni**, mis kehtib tulevasest kuupäevast.

Erinevate versioonide vaatamiseks võite kasutada kuupäeva valimiseks menüüvalikut **Alates kuupäevast**. Saate valida ka **Kuva kõik kirjed** kõigi intressikoodide kuvamiseks lehel.


