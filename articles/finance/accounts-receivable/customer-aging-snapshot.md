---
title: 'Kliendi aegumise hetktõmmised '
description: Selles teemas kirjeldatakse kliendi aegumise hetktõmmiseid. Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel.
author: JodiChristiansen
ms.date: 05/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 54db3e53cd31936ce80f0cdf1147535216d0d4b4
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722991"
---
# <a name="customer-aging-snapshots"></a>Kliendi aegumise hetktõmmised 

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse kliendi aegumise hetktõmmiseid. Aegumise hetktõmmis sisaldab arvutatud aegunud saldosid kliendi kohta kindlal ajahetkel. Looge aegumise hetktõmmise kirjed kõigile klientidele või kliendikausta klientidele.

Aegumise hetktõmmise teave kuvatakse loendilehel **Aegunud saldod** ja lehel **Sissenõuded**. Enne kui saate **Aegunud saldod** loendilehte kasutada, peate looma aegumise hetktõmmise. Loendilehel kuvatakse teavet vaid püsiklientidele, kelle jaoks on aegumise hetktõmmis loodud.

**Kliendi krediidi ja sissenõuete** tööruum näitab ka kliendi aegumist. Lisateavet vt [krediidi ja sissenõuete halduse Power BI sisust](credit-collections-power-bi.md).

> [!NOTE]
> Aegumise hetktõmmise loomiseks vajaliku aja vähendamiseks lülitage sisse **Kliendi aegumise jõudluse** funktsioon **Funktsioonihalduse** tööruumis. Ärge siiski kasutage kliendikaustu, kui see funktsioon on sisse lülitatud. Kliendikausta valimisel funktsioon ei tööta, kuid saate aegumise hetktõmmise siiski luua.

Kliendi aegumise hetktõmmise loomisel kasutage selle kohta teabe sisestamiseks järgmisi välju:

- **Aegumisperioodi definitsioon** – Valige väljal loodud aegumisperioodi definitsioon. Iga aegumisperioodi määratluse kohta saab olla üks aktiivne hetketõmmis. Aegumise hetktõmmis ja aegumisperioodi definitsioon tuleb eraldi luua.
- **Kausta ID** – Väli on valikuline. Saate kasutada kausta, et määrata klientide komplekt, mis tuleb aegumise hetktõmmises töödelda. Kliendikausta valimisel rakendatakse aegumise hetktõmmise töötlemist ainult kliendikausta kuuluvatele kliendikontodele. Valitud kliendi kaust peab olema **Aegumise hetktõmmis** tüüpi. Kui jätate selle välja tühjaks, luuakse aegumise hetktõmmis kõigi kliendikontode jaoks.

    > [!NOTE]
    > Kui kliendi **Aegumisjõudluse täiustuse** funktsioon on sisse lülitatud, ärge valige kliendikausta.

- **Kriteeriumid** – Aegumise hetktõmmis aegub valitud kuupäeva alusel:

    - **Kande kuupäev** – Iga kande aegumine põhineb selle kande kuupäeval.
    - **Tähtaeg** – Iga kande aegumine põhineb selle tähtajal.
    - **Dokumendi kuupäev** – Iga kande aegumine põhineb selle dokumendi kuupäeval.

- **Vanus alates** – Valige kuupäev, mida kasutada aegumise hetktõmmise **Praeguse kuupäevana**. Aegumisperioodid arvutatakse selle kuupäeva alusel. 

    - **Tänane kuupäev** – Kasutage süsteemi kuupäeva. Tehke see valik, kui töötlemine on seadistatud toimuma korduva partiina. Seejärel kasutatakse iga kord partii käitamisel selle käituse süsteemikuupäeva.
    - **Valitud kuupäev** - Kasutage enda määratud kuupäeva. Selle valiku korral peate sisestama aegumise kuupäeva.

    Näiteks on praegune aegumisperiood 30 päeva. Kui valite sellel väljal väärtuse **Tänane kuupäev** algab praegune aegumisperiood tänasest kuupäevast ja kaasab siis eelmised 29 päeva. Kui valite sellel väljal väärtuse **Valitud kuupäev** algab praegune aegumisperiood tänasest kuupäevast ja kaasab siis eelmised 29 päeva.

- **Värskendage märgukirja olekut** – Määrake selle valiku väärtuseks **Jah** et värskendada kannete sissenõude olekut **Sissenõuete** lehel **Lubadus maksta** **Lubadus maksta jaotatuna** kui aegumiskuupäev on pärast kuupäeva, mis on märgitud **Makse lubaduse kuupäeva** väljal. Määrake selle valiku väärtuseks **Ei** kui soovite jätta sissenõuete kogumi oleku muutmata **Sissenõuete** lehel.
- **Kaasa nullsaldoga kliendid** – Määrake selle suvandi väärtuseks **Jah** et kaasata kõik kliendid olenemata nende saldost. Kui kaasate kõik kliendid, on soovitatav lülitada sisse **Kliendi aegumise jõudluse täiustus** funktsioon ja mitte kasutada kliendikaustu. Ainult saldoga klientide kaasamiseks määrake selle valiku väärtuseks **Ei**. See säte aitab jõudlust kiirendada, kuna tasakaaluta kliendid jäetakse vahele.
- **Ettevõtte vahemik** – Valige vahekaardil **Ettevõtte vahemik** juriidilised isikud (ettevõtted), kes kaasatakse aegumise hetktõmmisse. Valida saab ainult tsentraliseeritud maksete jaoks seadistatud juriidilisi isikuid. Valitud juriidiliste isikute kanded kaasatakse siis aegumisperioodidesse klientide puhul, kellel on kõigis juriidilistes isikutes sama osapoole ID. Summad talletatakse aegumise hetktõmmise uuendamise ajal sisselogitud juriidilise isiku arvestusvaluutas.

Soovitame teil planeerida see protsess pakktöötlusena.

> [!NOTE]
> Partii jõudluse parandamiseks aegumise hetktõmmiste loomisel sisestage number **Partiiülesannete maksimumarv** väljal **Sissenõuete vaikekaardile** kiirkaardil **Sissenõuded** vahekaardil **Müügireskontro parameetrite** lehel. Väljal **Kliendi vanus saldod** on soovitatav alustada vaikeväärtusega **100** ja seejärel korrigeerida väärtust, et optimeerida oma olukorra töötlemist.

