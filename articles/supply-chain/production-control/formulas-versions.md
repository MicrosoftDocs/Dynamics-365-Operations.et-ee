---
title: Valemid ja valemite versioonid
description: See teema käsitleb valemeid ja valemiversioone. Valem määratleb materjalid, koostisosad ja konkreetse protsessi väljundid protsessi tootmises. Valemeid kasutatakse protsessi tootmises toodete plaanimiseks ja tootmiseks.
author: cvocph
manager: tfehr
ms.date: 09/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule, EcoResProductProdTypeFormulaNoActiveFormulaFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7fb37483412fdd09fe3734ddb148b050ec02951
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426192"
---
# <a name="formulas-and-formula-versions"></a>Valemid ja valemite versioonid

[!include [banner](../includes/banner.md)]

Valem määratleb materjalid, koostisosad ja konkreetse protsessi väljundid protsessi tootmises. Koos vastava protsessiga määratleb valem protsessi tootmises kogu protsessi. Valemeid kasutatakse protsessi tootmises toodete plaanimiseks ja tootmiseks.

Valem koosneb koostisosadest ja kogustest, mis on vajalikud konkreetse valemiüksuse koguse tootmiseks. Olenevalt tehtavast toimingust pääsete valemifunktsioonile juurde varude ja laohalduse või tooteteabe halduse moodulist.

## <a name="formulas-and-formula-lines"></a>Valemid ja valemiread
Valem koosneb vähemalt ühest valemireast, mis tähistavad koostisosi või üksusi, millest valem koosneb. Valemirida võib sisaldada koosluse üksusi, valemiüksusi, tegeliku kaaluga kaupu, ostetud kaupu, kaastooteid või kõrvalsaadusi. Kuna paljusid üksusi kasutatakse mitmes tootes, saab üksust kasutada mitmes valemis.

Valemi näide on šokolaadiküpsise valem. Selle valemi koostisosad (jahu, suhkur, munad, või ja šokolaaditükid) kasutavad mitut rida. Šokolaadiküpsise valem sisaldab koostisosi, mida tõenäoliselt teistes valemites kasutatakse. Šokolaadiküpsiste valmistamisel võib tekkida ülejääke (nt puru) või mõni küpsis võib olla liigselt või ebapiisavalt küpsenud. Need üksused saab seadistada kaastoodete või kõrvalsaadustena, olenevalt tootmistoimingutest.

Valemirea loomisel näidatakse rea tüübi abil, kuidas süsteem peaks rida käsitsema, kui käitate koondplaanimist ja toodate partiitellimusi. Iga rea tüüp annab erineva tulemuse. Järgmises tabelis kirjeldatakse valitavaid reatüüpe. 

| Rea tüüp     | Kirjeldus  |
|---------------|--------------|
| Kaup          | Tehke valik **Kaup**, kui kaubaks on laost võetav toormaterjal või pooltoodang või kui kaubaks on teenus. |
| Fiktiivne       | Valige **Fiktiivne**, kui soovite valemiridadel olevaid madalama taseme valemikaupu jaotada. Partiitellimuse hindamisel, kui valemiüksused jaotatakse, loetletakse koostiskaubad partiitellimusel valemiridadena. Veel lisatakse tootmisprotsessile vastavad protsessid. Valemiüksused jaotatakse kehtiva konfiguratsiooniga. Kui kasutate reatüüpi **Fiktiivne**, saate käsitleda erinevatel valemi tasemetel esinevaid tootmise ja mõõtmise konfiguratsioone. Kui valite lehe **Väljastatud toote üksikasjad** kiirkaardil **Projekteeri** tooteks **Fiktiivne** ja kasutate siis seda toodet valemis, muutub valemirea tüüp tüübiks **Fiktiivne**. Valikut **Fiktiivne** ei saa teha tegeliku kaaluga kauba või kaupade puhul, mille tootmise tüüp on **Kaastoode**, **Kõrvalsaadus** või **Plaanimisüksus**. |
| Kinnistatud tarne | Valige **Kinnistatud tarne** partiitellimuse, tootmistellimuse, kanbani, üleviimistellimuse või ostutellimuse loomiseks valemireal sisalduvale koostisosale. Seotud tellimus määratakse tellimuse vaikesätete ja koostisosa tootmise tüübi põhjal ning luuakse partiitellimuse hindamise ajal. Partiitellimuse jaoks reserveeritakse vajalikud koostisosade kogused. |
| Tarnija        | Tehke valik **Hankija**, kui tootmisprotsess kasutab allhankijat ja te soovite allhankija jaoks alamtootmise või ostutellimuse luua. Allhankija tehtud teenus või töö tuleb luua valemi- või teenusüksuse abil. Kauba saab siduda emaüksusega valemireana. Protsess peab sisaldama allhankija operatsiooniressursile määratud operatsiooni. See toiming seotakse valemireaga valiku **Oper. nr** abil. valik Jah. |

## <a name="formula-versions"></a>Valemiversioonid
Uue valemi koostamisel tuleb kõigepealt luua valemiversioon, enne kui lisate valemi reaüksused ja nende konkreetsed omadused. Igal valemil peab olema vähemalt üks versioon. Valemiversiooni nupp **Kinnitatud** muutub kättesaadavaks alles pärast versioonikirje edukat salvestamist. Iga valemiversiooni kirje seostatakse vähemalt ühe kaastoote ja kõrvalsaadusega, mida saab valmistoote tootmisel toota. Paljud tooted saab valmistada samadest koostisosadest erineva suurusega partiidena, kordsetena või erinevaid tulusid kasutades. Valemist saab luua soovitud arvu versioone.

Mitme aktiivse valemiversiooni haldamiseks saab kasutada kehtivaid kuupäevavahemikke või kogusevälju „alates”. Aktiivseid valemiversioone võib olla mitu ainult juhul, kui kuupäevavahemik ja kogus „alates” ei kattu.

Erinevalt kooslustest, kus üks kooslus seostatakse sageli paljude koosluseversioonidega, on valemi kohta tavaliselt olemas ainult üks valemiversioon. Pidage meeles, et antud toote laovarude dimensioonide ja koguse kohta saab aktiveerida ainult ühe valemiversiooni. Kuid muudel põhjustel võib valemiversioone olla palju ja saate neid partiitellimuse loomisel käsitsi valida.

## <a name="approve-and-activate-formulas-and-formula-versions"></a>Valemite ja valemiversioonide kinnitamine ja aktiveerimine
Valemid ja valemiversioonid tuleb kinnitada, enne kui neid saab plaanimiseks ja tootmiseks kasutada. Valemid aktiveeritakse tavaliselt enne kasutamist. Kuid tootmise ajal saate valida valemiversiooni, mis on kinnitatud, kuid mitte aktiveeritud.

Valemi või valemiversiooni kaitsmiseks saab määrata parameetrid **Blokeeri redigeerimine** ja **Blokeeri kinnituse eemaldamine** lehel **Tootmise juhtimise parameetrid**.

Kui valite **Blokeeri redigeerimine** ja valem kinnitatakse, ei saa ühtegi valemiridade välja kustutada ega redigeerida. Kuid kui valemi kinnituse eemaldate, saate valemiridu kustutada ja muuta. Samuti saate luua uusi valemeid ja uusi valemiversioone.

Kui valite **Blokeeri kinnituse eemaldamine**, ei saa kinnitatud valemi või valemiversiooni kinnitust eemaldada. Kuid saate luua uusi valemeid ja uusi valemiversioone ning eemaldada valemiversiooni aktiveerimise.

Saate lisada veel kontrollitasemeid, kasutades elektroonilise allkirja funktsiooni. Kui kasutaja on seadistatud nii, et valemi kinnitamise ajal on vaja elektroonilist allkirja, kuvatakse valemi aktiveerimisel leht **Allkiri**. Kasutajal peab olema elektroonilise allkirjastamise õigus ja sert peab olema enne muudatuse kinnitamist edukalt valideeritud. Kui allkirja ei saa autentida, siis keeldutakse kinnitusest või kinnituse eemaldamisest ja muudatus, mis kinnitamise või kinnituse eemaldamise algatas, lähtestatakse algolekusse.

## <a name="use-the-scalable-feature"></a>Funktsiooni Skaleeritav kasutamine
Funktsioon Skaleeritav on saadaval ainult juhul, kui kõigile kauba komponentidele valemis on määratud **Muutuv tarbimine**. Funktsioon pole saadaval, kui kauba komponentidele on määratud **Fikseeritud tarbimine** või **Etapiviisiline tarbimine**. Kui muudate funktsiooni Skaleeritav kasutamisel valemi koostisosa, korrigeeritakse teiste valitavate koostisosade kogust. Valemi suurust korrigeeritakse samuti. Samamoodi, kui muudate valemi suurust, muudetakse kõigi skaleeritavate koostisosade kogust. See funktsioon on mõeldud spetsiaalselt valemi koostamiseks ja haldamiseks. See ei näita, kas koostisosa kogust skaleeritakse partiitellimuses üles- või allapoole.

## <a name="use-step-consumption"></a>Etapiviisilise tarbimise kasutamine
Etapiviisiline tarbimine eemaldab nõude, et koostisosa vahekaardile **Valemirida** tuleb sisestada kogus. Selle asemel on etapiviisiline tarbimine konfigureeritud nii, et sellel on väärtus **Lähteseeria** ja väärtus **Kogus**. Kirjest Etapi tarbimine seeria kohta valitakse teave, mis rahuldab koguse partiitellimusel. Etapiviisiline tarbimine on abiks, kui tarbimismäär ei ole partiitellimuse suuruse suhtes lineaarne ja ainult suurendab vajadust, kui konkreetne koguselävi saavutatakse. Selle funktsiooni lubamiseks uuele valemile muutke grupis **Tarbimise arvutamine** vastava koostisosa valemi sätteks väärtuse **Standard** asemel väärtus **Etapp**. Selle tarbimismeetodi saab määrata lehe **Valemirida** vahekaardil **Seadistus**.
