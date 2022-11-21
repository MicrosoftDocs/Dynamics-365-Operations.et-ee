---
title: 'Kliendi aegumise hetktõmmised '
description: See artikkel annab teavet kliendi aegumise hetktõmmiste kohta. Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: e4ccc8ac9b5374ca0713167a17b8704727c687fd
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775232"
---
# <a name="customer-aging-snapshots"></a>Kliendi aegumise hetktõmmised 

[!include [banner](../includes/banner.md)]

See artikkel annab teavet kliendi aegumise hetktõmmiste kohta. Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel. Looge aegumise hetktõmmise kirjed kõigile klientidele või kliendikausta klientidele.

Aegumise hetktõmmise teave kuvatakse loendilehel **Aegunud saldod** ja lehel **Sissenõuded**. Enne kui saate **Aegunud saldod** loendilehte kasutada, peate looma aegumise hetktõmmise. Loendilehel kuvatakse teavet vaid püsiklientidele, kelle jaoks on aegumise hetktõmmis loodud.

**Kliendi krediidi ja sissenõuete** tööruum näitab ka kliendi aegumist. Lisateavet vt [krediidi ja sissenõuete halduse Power BI sisust](credit-collections-power-bi.md).

> [!NOTE]
> Aegumise hetktõmmise loomiseks vajaliku aja vähendamiseks lülitage funktsioonihalduse tööruumis **sisse järgmised funktsioonid**: 
> - **Klientide aegumise jõudlustäiustus** 
> - **Kliendi aegumise jõudluse täiustus kliendikaustadega**  
>Kui mõlemad funktsioonid on lubatud, **saab aegumise** hetktõmmise loomisel kasutada kliendikaustu. 

Kliendi aegumise hetktõmmise loomisel kasutage selle kohta teabe sisestamiseks järgmisi välju:

- **Aegumisperioodi definitsioon** – Valige väljal loodud aegumisperioodi definitsioon. Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis. Aegumise hetktõmmis ja aegumisperioodi definitsioon tuleb eraldi luua.
- **Kausta ID** – Väli on valikuline. Saate kasutada kausta, et määrata klientide komplekt, mis tuleb aegumise hetktõmmises töödelda. Kliendikausta valimisel rakendatakse aegumise hetktõmmise töötlemist ainult kliendikausta kuuluvatele kliendikontodele. Valitud kliendi kaust peab olema **Aegumise hetktõmmis** tüüpi. Kui jätate selle välja tühjaks, luuakse aegumise hetktõmmis kõigi kliendikontode jaoks.


- **Kriteeriumid** – Aegumise hetktõmmis aegub valitud kuupäeva alusel:

    - **Kande kuupäev** – Iga kande aegumine põhineb selle kande kuupäeval.
    - **Tähtaeg** – Iga kande aegumine põhineb selle tähtajal.
    - **Dokumendi kuupäev** – Iga kande aegumine põhineb selle dokumendi kuupäeval.

- **Vanus alates** – Valige kuupäev, mida kasutada aegumise hetktõmmise **Praeguse kuupäevana**. Aegumisperioodid arvutatakse selle kuupäeva alusel. 

    - **Tänane kuupäev** – Kasutage süsteemi kuupäeva. Tehke see valik, kui töötlemine on seadistatud toimuma korduva partiina. Seejärel kasutatakse iga kord partii käitamisel selle käituse süsteemikuupäeva.
    - **Valitud kuupäev** - Kasutage enda määratud kuupäeva. Selle valiku korral peate sisestama aegumise kuupäeva.

   Näiteks on praegune aegumisperiood 30 päeva. Kui valite sellel väljal väärtuse **Tänane kuupäev** algab praegune aegumisperiood tänasest kuupäevast ja kaasab siis eelmised 29 päeva. Kui valite sellel väljal väärtuse **Valitud kuupäev** algab praegune aegumisperiood tänasest kuupäevast ja kaasab siis eelmised 29 päeva.

- **Värskendage märgukirja olekut** – Määrake selle valiku väärtuseks **Jah** et värskendada kannete sissenõude olekut **Sissenõuete** lehel **Lubadus maksta** **Lubadus maksta jaotatuna** kui aegumiskuupäev on pärast kuupäeva, mis on märgitud **Makse lubaduse kuupäeva** väljal. Määrake selle valiku väärtuseks **Ei** kui soovite jätta sissenõuete kogumi oleku muutmata **Sissenõuete** lehel.
- **Kaasa nullsaldoga kliendid** – Määrake selle suvandi väärtuseks **Jah** et kaasata kõik kliendid olenemata nende saldost. Kui kaasate kõik kliendid, soovitame **teil** **sisse lülitada nii kliendi aegumise jõudluse täiustus kui ka kliendi aegumisjõudluse täiustus koos kliendikaustade funktsioonidega.** Ainult saldoga klientide kaasamiseks määrake selle valiku väärtuseks **Ei**. See säte kiirendab jõudlust, kuna tasakaaluta kliendid jäetakse vahele.
- **Möödu krediidilimiidi arvutustest** ajalise jaotuse ajal – **·** **kui** see valik on seatud väärtusele Jah, ei arvutata aegumisprotsessis uuesti saatelehe vahesummat, **·** **avatud** tellimuse vahesummat ja iga kliendi jaoks saadaolevat krediiti. Need saldod kuvatakse lehel Aegunud **saldod** jaotises **Krediidilimiit**. Aegumise protsessi kiiremaks jõudluseks määrake selle suvandi väärtuseks **Jah**. Seadistage aegumisprotsessi **käigus** saldode ümberarvutamise väärtuseks Ei. 
- **Ettevõtte vahemik** – Valige vahekaardil **Ettevõtte vahemik** juriidilised isikud (ettevõtted), kes kaasatakse aegumise hetktõmmisse. Valida saab ainult tsentraliseeritud maksete jaoks seadistatud juriidilisi isikuid. Valitud juriidiliste isikute kanded kaasatakse siis aegumisperioodidesse klientide puhul, kellel on kõigis juriidilistes isikutes sama osapoole ID. Summad talletatakse aegumise hetktõmmise uuendamise ajal sisselogitud juriidilise isiku arvestusvaluutas.

Soovitame teil planeerida see protsess pakktöötlusena.

> [!NOTE]
> Partii jõudluse parandamiseks aegumise hetktõmmiste loomisel sisestage number **Partiiülesannete maksimumarv** väljal **Sissenõuete vaikekaardile** kiirkaardil **Sissenõuded** vahekaardil **Müügireskontro parameetrite** lehel. Väljal Kliendi **vanus saldod** on soovitatav alustada väärtusega vahemikus 12 kuni **20** **ning korrigeerida väärtust siis nii,** et see optimeeriks teie olukorras töötlemist. Me ei soovita selle väärtuse seadmist rohkem kui **30**, kuna see mõjutab jõudlust. 

