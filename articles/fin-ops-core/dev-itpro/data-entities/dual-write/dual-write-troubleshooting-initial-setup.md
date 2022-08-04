---
title: Tõrkeotsingu probleemid algse häälestuse ajal
description: See artikkel annab teavet, mis aitab teil lahendada probleeme, mis ilmnevad topeltkirjutuse integreerimise algsel installimisel.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2e2759ff15dd8d146c642fc0da90d1a38fe855d1
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111196"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Tõrkeotsingu probleemid algse häälestuse ajal

[!include [banner](../../includes/banner.md)]



See artikkel pakub tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning Dataverse. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda topeltkirjutuse esialgse häälestamise käigus.

> [!IMPORTANT]
> Mõned küsimused, mida see artikkel käsitleb, võivad nõuda kas süsteemiadministraatori rolli või Microsofti Azure Active Directory (Azure AD) rentniku administraatori mandaate. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Finantside ja toimingute rakendust ei saa linkida rakendusega Dataverse

**Nõutav roll topeltkirjutuse häälestamiseks:** süsteemiadministraator finantside ja toimingute rakendustes ning Dataverse.

Tõrkeid lehel **Dataverse'i häälestuse link** põhjustab tavaliselt puudulik häälestus või lubade probleemid. Veenduge, et kogu seisundikontroll läbitakse lehel **Dataverse'i häälestuse link**, nagu näidatud järgmisel joonisel. Topeltkirjutust ei saa linkida, kui tervet seisundikontrolli pole läbitud.

![Edukas seisundikontroll.](media/health_check.png)

Teil peab olema rentniku Azure AD administraatori mandaadid, et linkida finantsid ja toimingud ning Dataverse keskkonnad. Pärast keskkondade linkimist saavad kasutajad sisse logida oma konto mandaadiga ja värskendada olemasoleva tabeli vastenduse.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Leidke juriidiliste tabelite või ettevõtete arvu piirang, mida saab siduda topeltkirjutusega

Kui proovite lubada vastendusi, võidakse kuvada järgmine tõrketeade.

*Topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: [(Osavastendust ei saanud tuua projektile DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Tõrge ületab maksimaalse lubatud osade arvu vastendusele DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Ilmnes üks või mitu tõrget.*

Praegune piirang keskkondade linkimiseks on umbes 40 juriidilist tabelit. See tõrge ilmneb, kui proovite lubada vastendusi ja rohkem kui 40 juriidilist tabelit on lingitud keskkondade vahel.

## <a name="connection-set-failed-while-linking-environment"></a>Ühenduse kogum nurjus keskkonna linkimisel

Topeltkirjutuskeskkonna linkimisel ebaõnnestub tegevus tõrketeatega:

*Ühenduskomplekti salvestamine nurjus! Sama võtmega kaup on juba lisatud.*

Topeltkirjutus ei toeta mitut sama nimega juriidilist isikut/ettevõtet. Näiteks kui teil on kaks ettevõtet nimega "DAT", siis rakenduses Dataverse kuvatakse see tõrketeade.

Kliendi blokeerimise tühistamiseks eemaldage tabelist **cdm_company** duplikaatkirjed rakenduses Dataverse. Kui tabelil **cdm_company** tühja nimega kirjeid, eemaldage need kirjed või parandage need.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Tõrge topeltkirjutuslehe avamisel finantside ja toimingute rakendustes

Kui proovite Dataverse keskkonda kahekordse kirjutamise jaoks linkida, võidakse kuvada järgmine tõrketeade:

*Vastuse oleku kood ei näita edu: 404 (ei leitud).*

See tõrge ilmneb, kui nõusoleku etappi pole lõpule viidud. Saate kinnitada, kas nõustumine on antud `portal.azure.com` rentniku administraatori kontoga sisselogimisel, ja kontrollige, kas 3 osapoole rakendus, mille ID `33976c19-1db5-4c02-810e-c243db79efde` on näha AAD ettevõtte rakenduste loendis. Kui mitte, käivitage uuesti nõustumiste etapp, nagu kirjeldatud järgmises jaotises.

### <a name="providing-app-consent"></a>Rakendusele loa andmine

+ Avage järgmine URL administraatori mandaadiga.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Valige **Nõustu** nõustumiseks. Olete andnud loa rakenduse (koos `id=33976c19-1db5-4c02-810e-c243db79efde`) oma rentnikusse installimiseks.
+ See rakendus on vajalik finantside Dataverse ja toimingute rakendustega suhtlemiseks.

    ![Tõrkeotsingu probleemid algse häälestuse ajal.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Kui see ei tööta, käivitage URL Microsoft Edge privaatrežiimis või Chrome inkognito režiimis.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finantside ja toimingute keskkond pole leitav.

Sellisel juhul kuvatakse järgnev veateade:

*Finantside ja toimingute rakenduste \*\*\* keskkond .cloudax.dynamics.com ole leitav.*

On kaks põhjust, mis võivad põhjustada probleemi, kus keskkond pole leitav:

+ Sisselogimiseks kasutatav kasutaja pole samas rentnikus kui finantside ja toimingute eksemplar.
+ Leiti pärand-finantse ja toimingute eksemplare, mis hostiti Microsofti majutatud probleemiga avastamisprobleemiga. Selle parandamiseks värskendage finantside ja operatsioonide eksemplari. Keskkond muutub avastatavaks iga värskendusega.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

