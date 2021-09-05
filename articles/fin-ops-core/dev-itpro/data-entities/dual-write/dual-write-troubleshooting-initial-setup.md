---
title: Tõrkeotsingu probleemid algse häälestuse ajal
description: See teema annab teavet, mis võib aidata lahendada probleeme, mis ilmnevad topeltkirjutuse esialgse häälestamise käigus.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2b75155aac12d79b9d68cce3e066acaaf80d6764
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380184"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Tõrkeotsingu probleemid algse häälestuse ajal

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda topeltkirjutuse esialgse häälestamise käigus.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Finance and Operationsi rakendust ei saa linkida Dataverse'iga

**Topeltkirjutuse seadistamiseks nõutav roll:** Finance and Operationsi rakenduste ja Dataverse'i süsteemiadministraator.

Tõrkeid lehel **Dataverse'i häälestuse link** põhjustab tavaliselt puudulik häälestus või lubade probleemid. Veenduge, et kogu seisundikontroll läbitakse lehel **Dataverse'i häälestuse link**, nagu näidatud järgmisel joonisel. Topeltkirjutust ei saa linkida, kui tervet seisundikontrolli pole läbitud.

![Edukas seisundikontroll.](media/health_check.png)

Keskkondade Finance and Operations ja Dataverse linkimiseks peab teil olema Azure AD rentniku administraatori mandaat. Pärast keskkondade linkimist saavad kasutajad sisse logida oma konto mandaadiga ja värskendada olemasoleva tabeli vastenduse.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Leidke juriidiliste tabelite või ettevõtete arvu piirang, mida saab siduda topeltkirjutusega

Kui proovite lubada vastendusi, võidakse kuvada järgmine tõrketeade.

*Topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: [(Osavastendust ei saanud tuua projektile DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Tõrge ületab maksimaalse lubatud osade arvu vastendusele DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Ilmnes üks või mitu tõrget.*

Praegune piirang keskkondade linkimiseks on umbes 40 juriidilist tabelit. See tõrge ilmneb, kui proovite lubada vastendusi ja rohkem kui 40 juriidilist tabelit on lingitud keskkondade vahel.

## <a name="connection-set-failed-while-linking-environment"></a>Ühenduse kogum nurjus keskkonna linkimisel

Topeltkirjutuskeskkonna linkimisel ebaõnnestub tegevus tõrketeatega:

*Ühenduskomplekti salvestamine nurjus! Sama võtmega kaup on juba lisatud.*

Topeltkirjutus ei toeta mitut sama nimega juriidilist isikut/ettevõtet. Näiteks kui teil on kaks ettevõtet nimega "DAT", siis rakenduses Dataverse kuvatakse see tõrketeade.

Kliendi blokeerimise tühistamiseks eemaldage tabelist **cdm_company** duplikaatkirjed rakenduses Dataverse. Kui tabelil **cdm_company** tühja nimega kirjeid, eemaldage need kirjed või parandage need.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Tõrge topeltkirjutuslehe avamisel Finance and Operations rakendustes

Kui proovite Dataverse keskkonda kahekordse kirjutamise jaoks linkida, võidakse kuvada järgmine tõrketeade:

*Vastuse oleku kood ei näita edu: 404 (ei leitud).*

See tõrge ilmneb, kui nõusoleku etappi pole lõpule viidud. Saate kinnitada, kas nõustumine on antud `portal.azure.com` rentniku administraatori kontoga sisselogimisel, ja kontrollige, kas 3 osapoole rakendus, mille ID `33976c19-1db5-4c02-810e-c243db79efde` on näha AAD ettevõtte rakenduste loendis. Kui mitte, käivitage uuesti nõustumiste etapp, nagu kirjeldatud järgmises jaotises.

### <a name="providing-app-consent"></a>Rakendusele loa andmine

+ Avage järgmine URL administraatori mandaadiga.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Valige **Nõustu** nõustumiseks. Olete andnud loa rakenduse (koos `id=33976c19-1db5-4c02-810e-c243db79efde`) oma rentnikusse installimiseks.
+ See rakendus on vajalik, et Dataverse saaks suhelda rakendustega Finance and Operations.

    ![Tõrkeotsingu probleemid algse häälestuse ajal.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Kui see ei tööta, käivitage URL Microsoft Edge privaatrežiimis või Chrome inkognito režiimis.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations keskkond pole leitav

Sellisel juhul kuvatakse järgnev veateade:

*Finance and Operations rakendusekeskkond \*\*\*.cloudax.dynamics.com pole leitav.*

On kaks põhjust, mis võivad põhjustada probleemi, kus keskkond pole leitav:

+ Sisselogimiseks kasutatav kasutaja pole eksemplariga samas Finance and Operations rentnikus.
+ Leiti Finance and Operations pärandeksemplari, mis hostiti Microsoft`i ja seal oli tuvastamisprobleem. Selle parandamiseks värskendage Finance and Operations eksemplari. Keskkond muutub avastatavaks iga värskendusega.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
