---
title: "Taskukohase ravikindlustuse eelnõu aruannete koostamine"
description: "See funktsioon on mõeldud nende tööandjate abistamiseks, kellel on vaja jälgida vormidel 1095-B ja 1095-C esitatud teavet taskukohase ravikindlustuse eelnõu tööandja kohustuse osa toetamiseks. Pange tähele, et see funktsioon on lubatud ainult Ameerika Ühendriikide juriidiliste isikute puhul."
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 1994edc5d6c932be3a285f9bb328a05504c90f07
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---
# <a name="generate-affordable-care-act-reports"></a>Taskukohase ravikindlustuse eelnõu aruannete koostamine

[!INCLUDE [banner](includes/banner.md)]

See funktsioon on mõeldud nende tööandjate abistamiseks, kellel on vaja jälgida vormidel 1095-B ja 1095-C esitatud teavet taskukohase ravikindlustuse eelnõu osa **Tööandja kohustus** toetamiseks. Pange tähele, et see funktsioon on lubatud ainult Ameerika Ühendriikide juriidiliste isikute puhul.

## <a name="getting-started"></a>Alustamine
Vormidele 1095-B ja 1095-C lisatava teabe jälgimise alustamisel tuleb esmalt luua vähemalt üks taskukohase ravikindlustusega hõlmatud grupp. Taskukohase ravikindlustusega hõlmatud gruppide abil näidatakse töötajale antud kindlustuskaitse pakkumist, töötaja osa madalaima kulu igakuisest preemiast (kui kulu ületab föderaalset vaesusepiiri) ning vajaduse korral tööandja kasutatavat Safe Harborit. Taskukohase ravikindlustuse eelnõu gruppide kasutamisel saate hallata nendel väljadel olevaid andmeid, ilma et oleks vaja liikuda läbi kõigi töötajakirjete, kui tingimused on samad. Lisaks saab taskukohase ravikindlustuse grupid määrata hõlpsasti vähemalt ühele töötajale, kasutades lehel massilise määramise funktsiooni.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Mitme kindlustusgrupi versiooni säilitamine
Kindlustusgrupist võib olla mitu versiooni, mis võimaldab teha muudatusi, mis hoiavad grupi andmed ajakohasena, ilma et oleks vaja luua uut gruppi või määrata töötajaid sellesse ümber, kui organisatsioonis või organisatsiooni pakutavates soodustustes midagi muutub. 

Kui olete vajalikud taskukohase ravikindlustuse grupid loonud, võite kasutada lehel nende gruppide massilist määramist töötajatele funktsiooniga **Massiline määramine** või minna iga töötaja juurde ja näidata, kas ACA teavet on selle töötaja puhul vaja jälgida ja registreerida, ning määrata töötaja taskukohase ravikindlustuse gruppi.

Kui taskukohase ravikindlustuse andmeid pole töötaja puhul vaja jälgida või registreerida, näiteks kui tegemist on osalise ajaga töötajaga, siis tuleks välja **Registreeri kindlustus** olekuks määrata Ei. Kuigi iga töötaja, kelle puhul ACA andmeid on vaja jälgida, tuleb määrata taskukohase ravikindlustuse gruppi, võite ikkagi muuta valikuid **Kindlustuspakkumine**, **Töötaja kuluosa** ja **Safe Harbor** mis tahes kuu (või kuude) kohta, mille puhul võivad olla vajalikud taskukohase ravikindlustuse gruppi sisestatud väärtustest erinevad väärtused.

Erandite sisestamiseks mõnesse taskukohase ravikindlustuse grupi väärtusse klõpsake töötaja andmete lehel olevat taskukohase ravikindlustuse linki vahekaardi Töösuhe lisateabe jaotise all.

## <a name="reporting-health-care-coverage"></a>Tervisekindlustuse registreerimine
Lisaks jälgimisele, millist tervisekindlustust täisajaga töötajale pakuti, kui tööandja pakub tööandja enda sõlmitud tervisekindlustust, millega töötaja on liitunud (olenemata sellest, kas töösuhe on täisajaga või osalise ajaga), tuleb vormil 1095 C esitada lisateavet. Iga töötaja (sh ülalpeetavad), kelle puhul tööandja toetusega tervisekindlustus kehtib, peavad olema lisatud nende kuude aruandesse, millal neile kindlustus kehtis. 

Saate näidata iga soodustuse plaani kohta, kas see tuleb aruandesse lisada, märkides ruudu **ACA-le esitatav**.

Lisaks, kui töötajad on otsustanud lasta oma ülalpeetavatele soodustuse määrata, võite lehel Soodustuste haldamine näidata kuupäevad, millal iga töötaja ülalpeetava kaitse kehtis. Näitamiseks, et ülalpeetavale kehtib soodustus, valige kiirkaardi Ülalpeetavad tegumipaanil nupp Redigeeri.

Lehel **Ülalpeetava kindlustuse kuupäevahaldur** saate märkida kuupäevad, millal ülalpeetavale soodustus kehtis. Kuupäevade sisestamisel sellele lehele märgitakse automaatselt ruut **Kaitstud** lehel **Soodustuste haldamine**.

## <a name="generate-1095b-and-1095c-forms"></a>Vormide 1095B ja 1095C loomine
Tootest saab luua ka vormid 109-B ja 1095-C ning jaotada need igale töötajale. Süsteemis saab luua elektrooniliselt ka edastusfaili 1095-C ja vastava faili 1094-C, mida saab kasutada IRS-ile saatmiseks.  

Vormi 1095-C loomisel sisestage sobiv kalender või maksuaasta ja see, kas soovite printida kahest või kolmest lehest koosneva vormi. Kolmest lehest koosnev vorm on vajalik ainult juhul, kui tööandja pakkus enda kindlustust ja töötajal on tema endaga koos üle kuue kaitstud ülalpeetava. Kui töötajal on üle 6 kaitstud ülalpeetava, tuvastab süsteem kahest lehest koosneva vormi loomisel selle automaatselt ega lisa vormi loomisel seda töötajat. Peale selle lisab süsteem kolmest lehest koosneva vormi loomisel ainult need töötajad, kellel on üle kuue kaitstud ülalpeetava.

## <a name="viewing-information"></a>Teabe vaatamine
Lehelt **Töötaja taskukohane ravikindlustus** saate vaadata, millised töötajad on igasse kindlustusgruppi määratud, milliseid töötajaid pole vaja aruandesse lisada ja millised töötajad on määramata.

Kui mõni väärtus taskukohase ravikindlustuse grupist on alistatud, kuvatakse muudetud väärtuse kõrval tärn. Kui kõigi 12 kuu väärtused on samad ja neid pole alistatud, prinditakse väärtus veerus **Kõik 12 kuud**.

Võite vaadata ka päringuakna abil, millised töötajad on märgitud kui mitte ACA-le esitatavad, mis tähendab, et te ei pea jälgima, millist kindlustust neile pakuti, ega väljastama neile aasta lõpus vormi 1095-C. Tehes valiku **Ei ole ACA-le esitatav** väljal **Filtreerimisalus**, saate luua loendi kõigist töötajatest, kes on märgitud vormi 1095-C mitte saama.

Lisaks ACA-le mitte esitatavate töötajate loendi vaatamisele saate vaadata ka töötajaid, kes on määramata (väli **ACA aruandesse kuuluv** on tühi) või kes on määratud taskukohase ravikindlustuse gruppi, mis on väljal **Aasta** valitud aasta puhul aegunud.

Saate koostatud töötajate nimekirju eksportida, kasutades mis tahes Exceli filtreerimisvalikuid.

Kui teil on vaja kindlustuskaitsega inimesi aruandesse lisada, kuna pakute tööandjana oma kindlustust, siis saate vaadata ka kõiki soodustusplaanidega kaetud ülalpeetavaid, kellel on märge **ACA-le esitatav**, valides toimingupaanilt toimingu Kuva ülalpeetava kindlustus.

**Märkus:** päringuaknas kuvatakse ainult need soodustused, mille plaanil on märge **ACA-le esitatav**.

