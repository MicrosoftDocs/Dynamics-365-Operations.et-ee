---
title: Saadetise automaatvärskendused
description: See teema annab ülevaate saadetise automaatvärskenduse funktsioonidest.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6215bc21bd3ee377274556f09ba29231118e5002
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201360"
---
# <a name="shipment-auto-updates"></a>Saadetise automaatvärskendused

[!include [banner](../includes/banner.md)]

Saadetise automaatvärskenduse funktsioon uuendab automaatselt koormusreal olevaid saadetisega seotud koguseid (nii suurendab kui ka vähendab) pärast koorma vabastamist lattu. See funktsioon on sisse lülitatud seni, kuni saadetise või koormuse koormusrida läbib töötlusvoo. Selle kasutamisel saavad tellimuse värskendused käsitsi sekkumata lao automaatselt läbida kuni laotöö loomiseni.

Kui saadetise automaatvärskenduse funktsiooni ei kasutata, väheneb automaatselt ainult kogus kuni laotöö loomiseni. Kasutajad peavad ridu käsitsi uuendama või kustutama ning seejärel uuesti vabastama, kui suurendatakse tellimuse koguseid või lisatakse uusi tellimuse ridu. Saadetise automaatvärskenduse funktsiooni kasutamisel saavad ettevõtted vaevatult ladu värskendada, muretsemata, et seotud saadetised ja koormused ei vasta tellimusrea uuendustele.

Saadetise automaatvärskenduse funktsioon rakendub nii müügitellimuse kui ka edastamise ridadele ja see on sisse lülitatud kindla lao jaoks. Tänu sellele saavad ettevõtted vastavalt vajadusele rakendada ladudes erinevaid saadetise automaatvärskenduse poliitikaid. Vaikimisi rakendub koguse vähenemise saadetise automaatvärskenduse poliitika kõikidele ladudele, mis kasutavad laohalduse protsesse. Kui kasutusel on see vaikepoliitika, väheneb automaatselt ainult saadetise ja koormuse kogus kuni laotöö loomiseni. See sarnaneb käitumisele, mida kasutati enne saadetise automaatvärskenduse funktsiooni kasutuselevõttu.

## <a name="main-elements-of-the-functionality"></a>Funktsiooni põhielemendid

Saadetise automaatvärskenduse funktsioon toetub määramisel, kas koormusreal olevat kogust tuleks muuta siis, kui muudatus tehakse müügitellimuse või edastamise real, peamiselt saadetise olekule. Samuti toetub see määramisel, millal luua automaatselt uus koormusrida olemasolevasse koormusse, peamiselt saadetise olekule. Kui saadetise olekuks on **Voog moodustatud** või kõrgem, siis automaatset uuendamist ei toimu.

Voogude olekut arvestatakse ka automaatvärskenduse puhul. Kui koormusreaga seotud vool on olekuks **Peatatud**, **Teostamine**, **Vabastatud**, **Komplekteeritud** või **Saadetud** ja kui kasutaja püüab vähendada koormust koormusreal (müügitellimuse või edastamise rea koguse vähenemisega) kuvatakse järgmine tõrketeade: "Reserveeringuid ei saa eemaldada, kuna on loodud töö, mis sõtlub nendest reserveeringutest." Lisaks, kui vool on üks eelnevalt mainitud voo olekutest, ei suurene koormusrea kogus automaatselt, kui kasutaja püüab müügitellimuse või edastamise rea koguse vähendamisega kaudselt suurendada koormusrea kogust. Sel juhul tuleb koormusrida käsitsi uuendada.

## <a name="scenarios"></a>Stsenaariumid

Saadetise automaatvärskenduse funktsioon toetab nelja stsenaariumi: uue tellimuserea lisamine, tellimusrea koguse suurendamine, tellimusrea koguse vähendamine ja tellimusrea eemaldamine.

- **Uue tellimuserea lisamine** – kui väli **Saadetise automaatvärskendus** kiirkaardil **Ladu** lehel **Laod** (**Laohaldus \> Seadistus \> Ladu \> Laod**) on seatud olekusse **Alati**, ei värskendata olemasolevat koormust, kui tellimuse saadetis on olemas ja müügitellimusele või edastamise tellimusele lisatakse uus tellimusrida pärast müügitellimusele koormuse loomist. Luuakse uus koormusrida, millel puudub viide olemasoleva koormusega, ja seostatakse olemasoleva saadetisega. Koormusele lisatakse uus rida ja vabastatakse.
- **Tellimusrea koguse suurendamine** – kui välja **Saadetise automaatvärskendus** väärtuseks on seatud **Alati**, suurendatakse koormusrida tellimusreaga sama koguse võrra, kui tellimuse saadetis on olemas ja olemasoleva müügitellimuse või edastamise rea kogust suurendatakse pärast seda, kui müügitellimusele on koormus juba loodud. Kui koormus vabastati, kuid tööd ei loodud, suurendatakse koormusrida tellimusreaga sama koguse võrra.
- **Tellimusrea koguse vähendamine** – kui välja **Saadetise automaatvärskendus** väärtuseks on seatud **Alati** või **Koguse vähendamisel**, uuendatakse seostatud koormusrea kogus võrdväärseks, kui tellimuse saadetis on olemas ja olemasoleva müügitellimuse või edastamise rea kogust vähendatakse pärast seda, kui müügitellimusele on koormus juba loodud, juhul, kui selle koormusrea kogus ei ole juba võrdne või väiksem kui tellimusrea uus kogus. Sel juhul see ei mõjuta koormusrida. Kui koormus vabastati, kuid tööd ei loodud, uuendatakse seostatud koormusrea kogus võrdväärseks, välja arvatud juhul, kui koormusrea kogus on juba võrdne või väiksem kui tellimusrea uus kogus. Sel juhul see mõjutab koormusrida.
- **Tellimusrea eemaldamine**– kui välja **Saadetise automaatvärskenduse** väärtuseks on seatud **Alati** või **Koguse vähendamisel**, kuvatakse tõrketeade, kui kasutaja püüab eemaldada tellimusrida, mille koormusrida on juba olemas.

## <a name="example-scenario"></a>Näidisstsenaarium

Sellisel juhul peavad teil olema installitud demoandmed ja peate kasutama **USMF** demoandmete ettevõtet.

### <a name="turn-on-the-auto-update-shipment-functionality"></a>Saadetise automaatvärskenduse funktsiooni sisselülitamine

Saadetise automaatvärskenduse funktsiooni sisselülitamine toimub järgmiste toimingute abil.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
2. Valige ladu **24**.
3. Muutke kiirkaardil **Ladu** välja **Saadetise automaatvärskendus** väärtus olekust **Koguse vähendamisel** olekusse **Alati**.

Väärtuse muutmisel olekusse **Alati**, kajastuvad valitud ladude saadetistes ja koormustes kõik müügitellimuse ja edastamise ridadel tehtavad koguste suurendamised ja vähendamised ning uute ridade lisamised eespool nimetatud kitsenduste põhjal.

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>Voomalli muutmine selliselt, et koormusridu ei töödeldaks automaatselt

Selleks, et konfigureerida voomalli nii, et see ei töötleks koormusridu automaatselt, toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
2. Valige voomall **24 Saadetise vaikemall**.
3. Valige suvand **Redigeeri**.
4. Muutke kiirkaardil **Üldine** valik **Voo automaatne loomine** olekusse **Jah** ja veenduge, et teised valikud oleksid seatud olekusse **Ei**.

On oluline, et voo loomise protsessi osana ei loodaks ega vabastataks ühtki tööd automaatselt. Pärast müügitellimuse rea jaoks loodud koormusreaga seotud töö loomist ei uuendata koormusrida enam automaatselt, kui müügitellimuse rea kogust muudetakse.

### <a name="create-a-sales-order"></a>Loo müügitellimus

Müügitellimuse loomiseks tehke järgmist.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
2. Valige klient **US-003**.
3. Looge rida kauba numbrile **A0001**.
4. Sisestage kogus **10**. (Veenduge, et kasutate ladu **24**.)
5. Valige käsk **Salvesta**.
6. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**. Luuakse saadetis ja voog.

Koormust ja tööd ei looda, sest muutsite eelmises protseduuris voomalli. Saadetis on olekus **Avatud** ja voog on olekus **Loodud**.

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>Müügitellimuse rea koguse vähendamine

Müügitellimuse rea koguse vähendamiseks toimige järgmiselt.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
2. Valige äsja lattu vabastatud müügitellimus.
3. Valige müügitellimuse rida. Muutke välja **Kogus** väärtus **10** pealt **8** peale.
4. Müügitellimuse realt valige **Ladu \> Saadetise üksikasjad**. Lehel **Saadetise üksikasjad** kiirkaardil **Koormusread** peegeldab kogus müügitellimuse rea muudatust.

### <a name="increase-the-quantity-on-a-sales-order-line"></a>Müügitellimuse rea koguse suurendamine

Müügitellimuse rea koguse suurendamiseks toimige järgmiselt.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
2. Valige eelnevalt lattu vabastatud müügitellimus.
3. Muutke rea kogus **8** pealt **12** peale.
4. Valige käsk **Salvesta**.
5. Minge tagasi lehele **Kõik müügitellimused** ja valige müügitellimus uuesti.
5. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Saadetise üksikasjad**. Lehel **Saadetise üksikasjad** kiirkaardil **Koormusread** peegeldab kogus müügitellimuse rea muudatust.

Kuigi koormusrea kogus tõusis 8-lt 12-ni, jääb reserveeringusse ainult kaheksa üksust, kui automaatset reserveerimist ei ole sisse lülitatud. Kui olemasolevale saadetisele lisatud kogust ei reserveerita ja kui praegusel hetkel voogu töödelda ilma reserveeringuta, siis luuakse töö ainult eelnevalt reserveeritud kogusega.

> [!NOTE]
> Kui tellimuserea kogust vähendada, ei mõjuta see koormusrea kogust, kui see on juba võrdne või väiksem kui tellimusrea uus kogus. Kui tellimusrea kogust suurendada, suurendatakse koormusrea kogust sama koguse võrra kui tellimusrida. Kui tellimusreal olev kogus erineb koormusrea kogusest, jääb erinevus alles.

### <a name="add-a-sales-order-line"></a>Müügitellimusrea lisamine

Müügitellimuse rea lisamiseks järgige neid juhiseid.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
2. Valige eelnevalt lattu vabastatud müügitellimus.
3. Looge rida kauba numbrile **A0002**.
4. Sisestage väljale **Kogus** väärtus **10**. (Veenduge, et kasutate ladu **24**.) Uus rida lisatakse automaatselt olemasolevale saadetisele.
5. Valige käsk **Salvesta**.
6. Minge tagasi lehele **Kõik müügitellimused** ja valige müügitellimus uuesti.
7. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Saadetise üksikasjad**. Lehe **Saadetise üksikasjad** kiirkaardil **Koormusread** vaadake teist koormusrida.

Kui olemasolevale saadetisele lisatud kogust ei reserveerita ja kui praegusel hetkel voogu töödelda, luuakse töö ainult esimese müügitellimuse rea ja esimese koormusrea koguse jaoks.

### <a name="process-a-wave"></a>Töötle voogu

Voo töötlemiseks tehke järgmist.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
2. Valige varem loodud voog.
3. Tehke tegumiriba vahekaardil **Voog** grupis **Voog** valik **Töötlus**.

Voog töödeldakse ja luuakse töö koormusrea reserveeritud kogustele. Saadetise olek värskendatakse olekust **Avatud** olekusse **Voog moodustatud**. Kuna saadetise olek on uuendatud olekusse **Voog moodustatud**, siis kõik toimuvad muudatused, nagu rea koguste vähendamine või suurendamine või müügitellimusele uute ridade lisamine, ei mõjuta see moodustatud vooga saadetise olemasolevaid koormusridu.

Kui saadetise olekuks on **Voog moodustatud** või kõrgem, ei kajastu müügitellimuse rea koguse värskendused ega ole valideeritud selle saadetisega seostatud koormusrea suhtes. Koormusrea koguse muudatused tuleb teha otse koormusreal.

Valideerimine toimub pärast koormusreale töö loomist ja reserveering on tehtud. Müügitellimuse rea koguse vähendamine valideeritakse seejärel töörea reserveeringu suhtes.
