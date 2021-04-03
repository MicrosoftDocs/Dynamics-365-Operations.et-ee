---
title: Seadme häälestamine tootmisosakonna käivitusliidese käitamiseks
description: Tootmisosakonna käivitusliides seadistakse iga tootmisosakonnas oleva seadme jaoks. Ettevõtted seadistavad tavaliselt iga seadme erinevalt, sõltuvalt seadme otstarbest. Näiteks võib ettevõttel olla üks seade vastuvõtualal, kus töötajad sisse ja välja registreerivad ning teine tootmisjaoskonnas, kus töötajad oma töid haldavad.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecution, HcmWorker, JmgProductionFloorExecutionDeviceConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 641273dd3ae189853326bf7af7ceb06d48465b5c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500546"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Seadme häälestamine tootmisosakonna käivitusliidese käitamiseks

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tootmisosakonna käivitusliides seadistakse iga tootmisosakonnas oleva seadme jaoks. Ettevõtted seadistavad tavaliselt iga seadme erinevalt, sõltuvalt seadme otstarbest. Näiteks võib ettevõttel olla üks seade vastuvõtualal, kus töötajad sisse ja välja registreerivad ning teine tootmisjaoskonnas, kus töötajad oma töid haldavad.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Kindla seadme konfiguratsiooni ja filtrite häälestamine

Seadme konfiguratsiooni ja tööfiltrite seadistamiseks logige sisse lehele **Tootmisosakonna käivitus**, kasutades kontot, millel on turberolli, mis sisaldab kohustust  *Ajahalduse järelevaataja*. (Valmislahenduse turberollide seast on see kohustus ainult *Tööde järelevaatajal*.) Seejärel toimige järgmiselt.

1. Minge seadme juurde, mida soovite häälestada, ja logige tööde juhatajana sisse Microsoft Dynamics 365 Supply Chain Managementi. (Kasutage kontot, mis sisaldab kohustust *Ajahalduse järelevaataja*.)
1. Veenduge, et konfiguratsioon oleks saadaval seadmele, mida seadistate. Kui konfiguratsioon pole olemas, pakutakse vaikekonfiguratsiooni. Lisateavet konfiguratsiooni seadistamise kohta leiate teemast [Tootmisosakonna käivitusliidese konfigureerimine](production-floor-execution-configure.md).
1. Avage **Tootmise juhtimine \> Tootmise käivitamine \> Tootmisosakonna käivitus**.

    Kui tootmisosakonna käivitusliides on praegusel seadmel juba vähemalt ühe korra konfigureeritud, kuvatakse sisselogimisleht. Vastasel juhul kuvatakse tervituskuva.

1. Sisselogimislehel või tervituskuval valige **Konfigureeri**.
1. Valige loendist konfiguratsioonigrupp.
1. Valige **Edasi**.
1. Valige vähemalt üks filter, mida rakendada praegusele seadmele. Nende filtrite aibil saate kuvada seadmel ainult asjakohased tööd. Filtri seadistamiseks valige filtri tüüp, et avada väärtuste loend ja valige seejärel filtreeritav väärtus. Saadaval on järgmised filtrid.

    - **Tootmisüksus** – see on kõrgeima taseme filter. Tavaliselt viitab see suurele tööalale, millel on mitu ressurssigruppi ja üksikuid ressursse.
    - **Ressursigrupp** – see on kesktaseme filter. Tavaliselt viitab see seostatud ressursside kogumile tööruumi piiratud alal. Kui valite esmalt filtri **Tootmisüksus**, kuvatakse ressursigruppide loendis ainult selle üksuse grupid. Vastasel juhul kuvatakse kõik saadaolevad ressursigrupid.
    - **Ressurss** – see on kõige täpsem filter. Tavaliselt viitab see kindlale masinale või muule üksikule ressursile. Kui valite esmalt filtri **Ressursigrupp** ja/või **Tootmisüksus**, kuvatakse ressursside loendis ainult selle grupi ja/või üksuse ressursid. Vastasel juhul kuvatakse kõik saadaolevad ressursid.

1. Valige nupp **OK**.
1. Kuvatakse sisselogimisleht ja teie seade on kasutamiseks valmis.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Töötajal vaikefiltrite alistamise lubamine

Saate anda konkreetsetele töötajatele filtri muutmise õiguse mis tahes kasutatavas seadmes. Töötajatele, kellel on see luba, annab tootmisosakonna käivitusliides nupu **Filter** lehtedel **Kõik tööd** ja **Aktiivsed tööd**.

> [!NOTE]
> Kui töötaja muudab filtrit, rakendub sellest hetkest uus filter kõigile kasutajatele, kes seadmesse sisse logivad.

Et töötaja saaks alistada seadmele seadistatud vaikefiltreid, toimige järgmiselt.

1. Avage **Tööajaarvestus \> Seadistus \> Ajalise registreerimise töötajad**.
1. Valige loendist töötaja, et avada selle töötaja leht **Ajalise registreerimise töötajad**.
1. Määrake vahekaardil **Aja registreerimine** suvandi **Määra filtrid** väärtuseks *Jah*.

## <a name="run-the-interface-in-full-screen-mode"></a>Kasutajaliidese käivitamine täisekraanrežiimis

Sageli käivitatakse tootmisosakonna käivitusliides seadmes, mida kasutatakse ainult selleks otstarbeks. Seetõttu võib olla mõttekas käitada liidest täisekraanrežiimis, kus poleks kuvatud navigeerimispaani ja/või Chrome'i brauserit.

- Supply Chain Managementis kuvatava navigeerimispaani peitmiseks lisage brauseri aadressiribale URL-i lõppu järgmine tekst: `\&limitednav=true`.
- Brauseri aadressiriba peitmiseks kasutage brauseri kohalikku täisekraanrežiimi. (Juhiste saamiseks vaadake oma brauseri dokumentatsiooni.)

Järgmise illustratsiooni ülemises on kuvatud, kuidas kasutajaliides vaikimisi välja näeb. Alumises osas kuvatakse, kuidas see näeb välja täisekraanrežiimis, kui navigeerimispaan on peidetud.

![Standardne või täisekraani liides](media/pfei-full-screen.png "Standardne või täisekraani liides")

## <a name="extend-the-session-past-12-hours"></a>Seansi pikendamine üle 12 tunni

Vaikimisi logib tootmisosakonna juhtimise liides automaatselt välja, kui keegi seda 12 tunni jooksul ei kasuta. Supply Chain Managementi kasutaja peab seejärel uuesti sisse logima. Kuid ajalõpu limiiti saate pikendada kuni 90 päevani.

Ajalõpu limiidi pikendamiseks logige Supply Chain Managementi sisse ja avage **Süsteemihaldus \> Kasutajad \> Seansi pikendused**. Määrake Supply Chain Managementi kasutajakonto, mida kasutatakse seadmesse sisse logimiseks ja tundide arv, mille jooksul peaks seanss aktiivseks jääma.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]