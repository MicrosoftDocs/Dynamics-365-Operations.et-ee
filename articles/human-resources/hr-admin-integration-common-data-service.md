---
title: Common Data Service'i integratsiooni konfigureerimine
description: Saate Common Data Service’i ja Microsoft Dynamics 365 Human Resourcesi eksemplari vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja üksust uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008724"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service'i integratsiooni konfigureerimine

Saate Common Data Service’i ja Microsoft Dynamics 365 Human Resourcesi eksemplari vahelise integratsiooni sisse või välja lülitada. Samuti saate vaadata sünkroonimise üksikasju, tühjendada jälgimise andmeid ja üksust uuesti sünkroonida, et aidata nende kahe keskkonna vahel probleeme lahendada.

Kui lülitate integratsiooni välja, saavad kasutajad teha muudatusi rakenduses Human Resources või Common Data Service, kuid neid muudatusi ei sünkroonita kahe keskkonna vahel.

Vaikimisi on rakenduste Human Resources ja Common Data Service vaheline integratsioon välja või sisse lülitatud, olenevalt keskkondade demoandmetest.

- **Välja** lülitatud uute keskkondade puhul, mis ei sisalda demo andmeid
- **Sisse** lülitatud uute keskkondade puhul, mis sisaldavad demo andmeid

Uued keskkonnad, mis sisaldavad demoandmeid, hakkavad andmeid nende ettevalmistamisel sünkroonima.

Võib-olla soovite integratsiooni välja lülitada järgmistes olukordades.

- Te täidate andmeid andmete halduse raamistiku kaudu ja peate andmeid õige oleku saavutamiseks mitu korda importima.

- Andmed on seotud kas rakendusega Human Resources või Common Data Service. Kui lülitate integratsiooni välja, saate kustutada kirje ühes keskkonnas, kustutamata seda teises. Kui lülitate integratsiooni tagasi sisse, sünkroonitakse kirje keskkonnas, kus seda ei kustutatud, tagasi keskkonda, kus see kustutati. Sünkroonimine algab järgmisel korral, kui käivitub rakenduse **Common Data Service integratsioon vastamata nõude sünkroonimise** pakett-töö.

> [!WARNING]
> Kui lülitate andmete integreerimise välja, veenduge, et te ei redigeeriks sama kirjet mõlemas keskkonnas. Kui lülitate integratsiooni uuesti sisse, sünkroonitakse viimati redigeeritud kirje. Seega, kui te ei teinud mõlemas keskkonnas kirjes samu muudatusi, võib esineda andmekadu.

## <a name="access-the-common-data-service-integration-page"></a>Juurdepääs rakenduse Common Data Service integratsiooni lehele

1. Valige rakenduse Human Resources eksemplaris, kus soovite integratsiooni sätteid rakendusega Common Data Service vaadata või konfigureerida, paan **Süsteemihaldus**.

    [![Süsteemihalduse paan](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Valige vahekaart **Lingid**.

    [![Vahekaart Lingid](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Valige jaotises **Integratsioonid** rakenduse **Common Data Service konfiguratsioon**.

    [![Common Data Service’i konfiguratsiooni link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Rakenduste Human Resources ja Common Data Service vahelise andmete integratsiooni sisse ja välja lülitamine

- Integratsiooni sisselülitamiseks seadke **Luba integreerimine rakendusele Common Data Service** valikule **Jah**.

    > [!NOTE]
    > Kui lülitate integratsiooni sisse, sünkroonitakse andmed järgmisel korral, kui **Common Data Service’i integratsiooni vastamata nõude sünkroonimise** pakett-töö käivitub. Kõik andmed peaksid olema kättesaadavad pärast pakett-töö lõpetamist.

- Integratsiooni väljalülitamiseks seadke suvandi väärtuseks **Ei**.

[![Rakenduse Common Data Service integratsiooni sisse või välja lülitamine](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Andmete integratsiooni üksikasjade ülevaade

Rakenduse **Common Data Service integratsiooni** lehe kiirkaardil **Haldamine** saate vaadata, kuidas on rakenduste Human Resources ja Common Data Service kirjed ühendatud.

- Üksuse kirjete vaatamiseks valige väljal **CDS-üksuse nimi** olev üksus. Ruudustik kuvab kõik kirjed, mis on seotud valitud üksusega.

[![Üksuse kirjete vaatamine](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Kõik Common Data Service’i üksused pole praegu loetletud. Ruudustikus kuvatakse ainult üksused, mis toetavad kohandatud väljade kasutamist. Uued üksused muutuvad kättesaadavaks rakenduse Human Resources jätkuväljaannetes.

Ruudustik sisaldab järgmisi välju.

- **CDS-üksuse nimi** – üksuse nimi rakenduses Common Data Service.
- **CDS-üksuse viide** – identifikaator, mida Common Data Service kasutab kirje tuvastamiseks. See väärtus võrdub rakenduse Human Resources väärtusega **RecId**. Selle identifikaatori leiate, avades rakenduse Common Data Service üksuse Microsoft Excelis.
- **Rakenduse Human Resources üksuse nimi** – üksus, mis viimasena sünkroonis andmeid rakendusega Common Data Service. Üksusel võib olla kas Common Data Service’i eesliide või muu eesliide.
- **Rakenduse Human Resources viide** – väärtus **RecId**, mis on seotud kirjega rakenduses Human Resources.
- **Kustutati CDS-ist** – väärtus, mis näitab, kas kirje kustutati rakendusest Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Eemaldage rakendusest Common Data Service kirje seos rakendusega Human Resources

Kui teil tekib probleeme rakenduste Human Resources ja Common Data Service vahelise sünkroonimise ajal, saate neid lahendada, tühjendades jälgimise ja lastes jälgimise tabeli uuesti sünkroonimise. Kui eemaldate seose ja seejärel muudate või kustutate kirje rakenduses Common Data Service, ei sünkroonita muudatusi rakendusega Human Resources. Kui teete muudatusi rakenduses Human Resources, luuakse uus jälgimise kirje ja kirje uuendatakse rakenduses Common Data Service.

- Kirje seose eemaldamiseks rakenduste Human Resources ja Common Data Service vahel, valige üksus väljal **CDS-üksuse nimi** ja seejärel käsk **Tühjenda jälgimise teave**.

[![Jälgimisteabe kustutamine](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Üksuse täieliku sünkroonimise käivitamiseks pärast jälgimise tühjendamist vaadake järgmist protseduuri.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Sünkroonige üksus rakenduste Human Resources ja Common Data Service vahel

Kasutage seda protseduuri, kui muudatused rakenduses Common Data Service võtavad liiga kaua aega, et ilmuda rakenduses Human Resources, või kui peate pärast jälgimise tühjendamist värskendama jälgimise tabelit.

- Üksuse täieliku sünkroonimise käivitamiseks rakenduste Human Resources ja Common Data Service vahel valige üksus väljal **CDS-üksuse nimi** ja seejärel käsk **Sünkrooni kohe**.

[![Täieliku sünkroonimise käivitamine](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


