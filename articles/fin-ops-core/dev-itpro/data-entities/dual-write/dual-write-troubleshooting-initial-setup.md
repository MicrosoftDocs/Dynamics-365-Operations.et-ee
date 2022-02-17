---
title: Tõrkeotsingu probleemid algse häälestuse ajal
description: See teema annab teavet, mis võib aidata lahendada probleeme, mis ilmnevad topeltkirjutuse esialgse häälestamise käigus.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9a70de253eff2a3273be4a31ab32757bb014328f
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061463"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Tõrkeotsingu probleemid algse häälestuse ajal

[!include [banner](../../includes/banner.md)]



See teema pakub tõrkeotsinguteavet finance and Operationsi rakenduste ja rakenduse kahe kirjutamise integreerimiseks Dataverse. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda topeltkirjutuse esialgse häälestamise käigus.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Rakendust Finance and Operations ei saa linkida Dataverse

**Topeltkirjutaja seadistamise vajalik roll:** süsteemiadministraator finance and Operationsi rakendustes ja Dataverse.

Tõrkeid lehel **Dataverse'i häälestuse link** põhjustab tavaliselt puudulik häälestus või lubade probleemid. Veenduge, et kogu seisundikontroll läbitakse lehel **Dataverse'i häälestuse link**, nagu näidatud järgmisel joonisel. Topeltkirjutust ei saa linkida, kui tervet seisundikontrolli pole läbitud.

![Edukas seisundikontroll.](media/health_check.png)

Finance and Operationsi ja keskkondade Azure AD linkimiseks peab teil Dataverse olema rentnikuadministraatori identimisteave. Pärast keskkondade linkimist saavad kasutajad sisse logida oma konto mandaadiga ja värskendada olemasoleva tabeli vastenduse.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Leidke juriidiliste tabelite või ettevõtete arvu piirang, mida saab siduda topeltkirjutusega

Kui proovite lubada vastendusi, võidakse kuvada järgmine tõrketeade.

*Topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: [(Osavastendust ei saanud tuua projektile DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Tõrge ületab maksimaalse lubatud osade arvu vastendusele DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Ilmnes üks või mitu tõrget.*

Praegune piirang keskkondade linkimiseks on umbes 40 juriidilist tabelit. See tõrge ilmneb, kui proovite lubada vastendusi ja rohkem kui 40 juriidilist tabelit on lingitud keskkondade vahel.

## <a name="connection-set-failed-while-linking-environment"></a>Ühenduse kogum nurjus keskkonna linkimisel

Topeltkirjutuskeskkonna linkimisel ebaõnnestub tegevus tõrketeatega:

*Ühenduskomplekti salvestamine nurjus! Sama võtmega kaup on juba lisatud.*

Topeltkirjutus ei toeta mitut sama nimega juriidilist isikut/ettevõtet. Näiteks kui teil on kaks ettevõtet nimega "DAT", siis rakenduses Dataverse kuvatakse see tõrketeade.

Kliendi blokeerimise tühistamiseks eemaldage tabelist **cdm_company** duplikaatkirjed rakenduses Dataverse. Kui tabelil **cdm_company** tühja nimega kirjeid, eemaldage need kirjed või parandage need.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Tõrge topeltkirjutuslehe avamisel finance and Operationsi rakendustes

Kui proovite Dataverse keskkonda kahekordse kirjutamise jaoks linkida, võidakse kuvada järgmine tõrketeade:

*Vastuse oleku kood ei näita edu: 404 (ei leitud).*

See tõrge ilmneb, kui nõusoleku etappi pole lõpule viidud. Saate kinnitada, kas nõustumine on antud `portal.azure.com` rentniku administraatori kontoga sisselogimisel, ja kontrollige, kas 3 osapoole rakendus, mille ID `33976c19-1db5-4c02-810e-c243db79efde` on näha AAD ettevõtte rakenduste loendis. Kui mitte, käivitage uuesti nõustumiste etapp, nagu kirjeldatud järgmises jaotises.

### <a name="providing-app-consent"></a>Rakendusele loa andmine

+ Avage järgmine URL administraatori mandaadiga.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Valige **Nõustu** nõustumiseks. Olete andnud loa rakenduse (koos `id=33976c19-1db5-4c02-810e-c243db79efde`) oma rentnikusse installimiseks.
+ See rakendus on vajalik finance and Operationsi rakendustega suhtlemiseks Dataverse.

    ![Tõrkeotsingu probleemid algse häälestuse ajal.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Kui see ei tööta, käivitage URL Microsoft Edge privaatrežiimis või Chrome inkognito režiimis.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finants- ja tegevuskeskkond ei ole leitav

Sellisel juhul kuvatakse järgnev veateade:

*Finance and Operationsi rakenduste keskkond \*\*\*.cloudax.dynamics.com pole leitav.*

On kaks põhjust, mis võivad põhjustada probleemi, kus keskkond pole leitav:

+ Sisselogimiseks kasutatav kasutaja pole eksemplariga Finance and Operations samas rentnikus.
+ On mõned varasemad finance and Operationsi eksemplarid, mis olid Microsofti hostitud ja millel oli avastamisega probleeme. Selle parandamiseks värskendage eksemplari Finance and Operations. Keskkond muutub avastatavaks iga värskendusega.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
