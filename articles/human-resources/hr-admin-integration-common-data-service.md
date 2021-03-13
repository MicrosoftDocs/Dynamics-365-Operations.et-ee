---
title: Dataverse'i integratsiooni konfigureerimine
description: Saate Microsoft Dataverse’i ja Dynamics 365 Human Resourcesi vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja tabelit uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112270"
---
# <a name="configure-dataverse-integration"></a>Dataverse'i integratsiooni konfigureerimine

Saate Microsoft Dataverse’i ja Dynamics 365 Human Resourcesi vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja tabelit uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.

> [!NOTE]
> Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

Kui lülitate integratsiooni välja, saavad kasutajad teha muudatusi rakenduses Human Resources või Dataverse, kuid neid muudatusi ei sünkroonita kahe keskkonna vahel.

Rakenduste Human Resources ja Dataverse vahelise andmete integratsioon on vaikimisi välja lülitatud.

Võib-olla soovite integratsiooni välja lülitada järgmistes olukordades.

- Te täidate andmeid andmete halduse raamistiku kaudu ja peate andmeid õige oleku saavutamiseks mitu korda importima.

- Andmed on seotud kas rakendusega Human Resources või Dataverse. Kui lülitate integratsiooni välja, saate kustutada kirje ühes keskkonnas, kustutamata seda teises. Kui lülitate integratsiooni tagasi sisse, sünkroonitakse kirje keskkonnas, kus seda ei kustutatud, tagasi keskkonda, kus see kustutati. Sünkroonimine algab järgmisel korral, kui käivitub rakenduse **Dataverse integratsioon vastamata nõude sünkroonimise** pakett-töö.

> [!WARNING]
> Kui lülitate andmete integreerimise välja, veenduge, et te ei redigeeriks sama kirjet mõlemas keskkonnas. Kui lülitate integratsiooni uuesti sisse, sünkroonitakse viimati redigeeritud kirje. Seega, kui te ei teinud mõlemas keskkonnas kirjes samu muudatusi, võib esineda andmekadu.

## <a name="access-the-dataverse-integration-page"></a>Juurdepääs rakenduse Dataverse integratsiooni lehele

1. Valige rakenduse Human Resources eksemplaris, kus soovite integratsiooni sätteid rakendusega Dataverse vaadata või konfigureerida, paan **Süsteemihaldus**.

    [![Süsteemihalduse paan](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Valige vahekaart **Lingid**.

    [![Vahekaart Lingid](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Valige jaotises **Integratsioonid** rakenduse **Dataverse konfiguratsioon**.

    [![Dataverse’i konfiguratsiooni link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Rakenduste Human Resources ja Dataverse vahelise andmete integratsiooni sisse ja välja lülitamine

- Integratsiooni sisselülitamiseks määrake suvand **Luba Dataverse'i integratsioon** väärtusele **Jah** lehel **Microsoft Dataverse'i integratsioon**.

    > [!NOTE]
    > Kui lülitate integratsiooni sisse, sünkroonitakse andmed järgmisel korral, kui **Dataverse’i integratsiooni vastamata nõude sünkroonimise** pakett-töö käivitub. Kõik andmed peaksid olema kättesaadavad pärast pakett-töö lõpetamist.

- Integratsiooni väljalülitamiseks seadke suvandi väärtuseks **Ei**.

[![Rakenduse Dataverse integratsiooni sisse või välja lülitamine](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Soovitame andmete migreerimisega tegeledes tungivalt Dataverse'i integratsiooni välja lülitada. Mahukate andmete üleslaadimine võib jõudlust oluliselt mõjutada. Näiteks võib 2000 töötaja üleslaadimine võtta mitu tundi, kui integratsioon on lubatud, ja vähem kui üks tund, kui see on keelatud. Näites toodud numbrid on mõeldud ainult selgitamiseks. Kirjete importimiseks kuluv täpne aeg võib mitme teguri põhjal olla väga erinev.

## <a name="view-data-integration-details"></a>Andmete integratsiooni üksikasjade ülevaade

Rakenduse **Microsoft Dataverse integratsiooni** lehe kiirkaardil **Haldamine** saate vaadata, kuidas on rakenduste Human Resources ja Dataverse read ühendatud.

- Tabeliridade vaatamiseks valige tabel väljalt **Dataverse'i tabel**. Ruudustik kuvab kõik read, mis on seotud valitud tabeliga.

> [!NOTE]
> Kõik Dataverse’i tabelid pole praegu loetletud. Ruudustikus kuvatakse ainult tabelid, mis toetavad kohandatud väljade kasutamist. Uued tabelid muutuvad kättesaadavaks rakenduse Human Resources jätkuväljaannetes.

Ruudustik sisaldab järgmisi välju.

- **Dataverse'i tabel** - tabeli nimi Dataverse'is.
- **Dataverse'i tabeli viide** - identifikaator, mida Dataverse kasutab kirje tuvastamiseks. See väärtus võrdub rakenduse Human Resources väärtusega **RecId**. Selle identifikaatori leiate, avades rakenduse Dataverse tabeli Microsoft Excelis.
- **Rakenduse Human Resources üksuse nimi** - Human Resourcesi üksus, mis viimasena sünkroonis andmeid rakendusega Dataverse. Üksusel võib olla kas Dataverse’i eesliide või muu eesliide.
- **Rakenduse Human Resources viide** – väärtus **RecId**, mis on seotud kirjega rakenduses Human Resources.
- **Kustutati Dataverse'ist** - väärtus, mis näitab, kas rida kustutati Dataverse'ist.

> [!NOTE]
> Rakenduse Human Resources kirjed vastavad ridadele Dataverse'is.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Eemaldage rakenduse Dataverse realt kirje seos rakendusega Human Resources

Kui teil tekib probleeme rakenduste Human Resources ja Dataverse vahelise sünkroonimise ajal, saate neid lahendada, tühjendades jälgimise ja lastes jälgimise tabeli uuesti sünkroonimise. Kui eemaldate seose ja seejärel muudate või kustutate rea rakenduses Dataverse, ei sünkroonita muudatusi rakendusega Human Resources. Kui teete muudatusi rakenduses Human Resources, luuakse uus jälgimise kirje ja rida uuendatakse rakenduses Dataverse.

- Kirje seose eemaldamiseks rakenduste Human Resources ja Dataverse'i rea vahel, valige tabel väljal **Dataverse'i tabel** ja seejärel valige käsk **Tühjenda jälgimise teave**.

[![Jälgimisteabe kustutamine](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Tabeli täieliku sünkroonimise käivitamiseks pärast jälgimise tühjendamist vaadake järgmist protseduuri.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Sünkroonige tabel rakenduste Human Resources ja Dataverse vahel

Kasutage seda protseduuri, kui:

- Dataverse'i muudatuste kuvamine rakenduses Human Resources võtab liiga kaua aega;

- pärast jälitamise tühjendamist peate värskendama jälgimise tabelit.

Rakenduse Human Resources ja Dataverse'i vahelise tabeli täieliku sünkroonimise käivitamiseks tehke järgmist.

1. Valige tabel väljal **Dataverse'i tabel**.

2. Valige **Sünkrooni kohe**.

[![Täieliku sünkroonimise käivitamine](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Vt ka

[Dataverse'i tabelid](hr-developer-entities.md)<br>
[Dataverse'i virtuaalsete tabelite konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resourcesi virtuaaltabelite KKK](hr-admin-virtual-entity-faq.md)<br>
[Mis on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminoloogia uuendused](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
