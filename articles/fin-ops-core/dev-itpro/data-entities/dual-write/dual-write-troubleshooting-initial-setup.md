---
title: Probleemide tõrkeotsing esmase häälestamise ajal
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada topeltkirjutuse esmasel häälestamisel ilmnevaid probleeme Finance and Operationsi rakenduste ja Common Data Service'i vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172664"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Probleemide tõrkeotsing esmase häälestamise ajal

[!include [banner](../../includes/banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda topeltkirjutuse esialgse häälestamise käigus.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Finance and Operationsi rakendust ei saa linkida Common Data Service'iga

**Topeltkirjutuse seadistamiseks nõutav mandaat:** Azure AD rentniku administraator

Tõrkeid lehel **Common Data Service'i häälestuse link** põhjustab tavaliselt puudulik häälestus või lubade probleemid. Veenduge, et kogu seisundikontroll läbitakse lehel **Common Data Service'i häälestuse link**, nagu näidatud järgmisel joonisel. Topeltkirjutust ei saa linkida, kui tervet seisundikontrolli pole läbitud.

![Edukas seisundikontroll](media/health_check.png)

Keskkondade Finance and Operations ja Common Data Service linkimiseks peab teil olema Azure AD rentniku administraatori mandaat. Pärast keskkondade linkimist saavad kasutajad sisse logida oma konto mandaadiga ja värskendada olemasoleva üksuse vastenduse.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Tõrge Common Data Service'i lehe lingi avamisel

**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin

Kui proovite avada rakenduses Finance and Operations lehte **Common Data Service'i link**, võidakse kuvada järgmine tõrketeade.

*Vastuse oleku kood ei näita edu: 404 (ei leitud).*

See tõrge ilmneb, kui nõusoleku etappi pole lõpule viidud. Selleks, et kontrollida, kas nõusoleku etapp on lõpule viidud, logige sisse lehele portal.Azure.com Azure AD rentniku administraatori kontoga ja kontrollige, kas kolmanda osapoole rakendus, mille ID on **33976c19-1db5-4c02-810e-c243db79efde**, kuvatakse Azure AD **Ettevõtte rakenduste** loendis. Kui seda pole, peate andma rakenduse nõusoleku.

Rakenduse nõusoleku andmiseks toimige järgmiselt.

1. Avage järgmine URL administraatori mandaadiga. Teilt küsitakse nõusolekut.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Valige **Nõustu**, et kinnitada oma nõusolekut rakenduse installimiseks, millel on teie rentniku ID **33976c19-1db5-4c02-810e-c243db79efde**.

    > [!TIP]
    > See rakendus on nõutav rakendusre Common Data Service ja Finance and Operations linkimiseks. Kui teil on selle etapiga probleeme, avage brauser inkognito-režiimis (Google Chrome'is) või InPrivate-režiimis (rakenduses Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Veenduge, et ettevõtte andmed ja topeltkirjutuse meeskonnad on linkimisel õigesti häälestatud

Tagamaks, et topeltkirjutus töötaks õigesti, luuakse konfiguratsiooni ajal valitud ettevõtted Common Data Service'i keskkonnas. Vaikimisi on need ettevõtted kirjutuskaitstud ja atribuudi **IsDualWriteEnable** väärtuseks on seatud **Tõene**. Lisaks luuakse vaikimisi omanikust äriüksuse omanik ja meeskond ning kaasatakse ettevõtte nimi. Enne vastenduste lubamist kontrollige, kas meeskonna vaikeomanik on määratud. Üksuse **Ettevõtted (CDM\_Company)** leidmiseks toimige järgmiselt.

1. Valige filter Dynamics 365 mudeljuhitud rakenduse paremas ülanurgas.
2. Valige ripploendist **Ettevõte**.
3. Tulemuste nägemiseks valige **Käivita**.
4. Valige ettevõte, mis oli topeltkirjutuse konfigureerimisel lingitud.
5. Veenduge, et väljal **Vaikeomanikust meeskond** oleks väärtus. Järgmisel joonisel on välja **Vaikeomanikust meeskond** väärtuseks seatud **USMF topeltkirjutus**.

    ![Vaikeomanikust meeskonna kontrollimine](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Leidke juriidiliste isikute või ettevõtete arvu piirang, mida saab siduda topeltkirjutusega

Kui proovite lubada vastendusi, võidakse kuvada järgmine tõrketeade.

*Topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: \[(Osavastendust ei saanud tuua projektile DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Tõrge ületab maksimaalse lubatud psade arvu vastendusele DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Ilmnes üks või mitu tõrget.*

Praegune piirang keskkondade linkimiseks on umbes 40 juriidilist isikut. See tõrge ilmneb, kui proovite lubada vastendusi ja rohkem kui 40 juriidilist isikut on lingitud keskkondade vahel.
