---
title: Jaemüügikanalite määratlemine ja haldamine
description: Selles teemas antakse ülevaade füüsilistele kaupluste, mida nimetatakse Dynamics 365 Commerce'is kauplusteks, seadistamise protsessist. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast kaupluse seadistamist.
author: mugunthanm
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7a2db169adafa1b8a0113024f3f58522c2cee6d2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802017"
---
# <a name="define-and-maintain-retail-channels"></a>Jaemüügikanalite määratlemine ja haldamine

[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade füüsilistele kaupluste, mida nimetatakse Dynamics 365 Commerce'is kauplusteks, seadistamise protsessist. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast kaupluse seadistamist.

Commerce toetab mitmeid kanaleid, nagu võrgupoed, kõnekeskused ja traditsioonilised kauplused. Traditsioonilist kauplust nimetatakse kaupluseks. Igal kauplusel võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal. Enne kaupluse loomist tuleb seadistada kõik need elemendid. Kui olete kaupluse loonud, saate määrata seal müüdavad tooted. Saate kauplusele määrata ka töötajad, registrid ja kliendid. Viimaks peate lisama uue kaupluse organisatsioonihierarhiasse.

## <a name="setting-up-stores"></a>Kaupluste seadistamine

Enne kui saate rakenduses Commerce kaupluse seadistada, peate täitma mõne eeltingimuseks oleva ülesande. Seejärel saate luua kaupluse ja lisada üksikasjad.

### <a name="prerequisites"></a>Eeltingimused

Enne kui saate kaupluse seadistada, peate tegema järgmised toimingud.

1. Saate konfigureerida organisatsiooni struktuuri ja seadistada organisatsiooni hierarhiad jaemüügisortimendi, täiendamise ja aruannete jaoks.
2. Saate seadistada kauplust kajastava lao.
3. Kaupluste, kaupluse väljavõtete ja väljavõttekannete numbriseeriate seadistamine.
4. Commerce'i parameetrite konfigureerimine.
5. Kaupluses aktsepteeritavate makseviiside seadistamine.
6. Kassaregistrites krediitkaardikannete töötlemiseks saate seadistada ka makseteenused.
7. Käibemaksugruppide seadistamine.
8. Seadistage tooted. Selle toimingu raames seadistate ka tootehierarhiad, tootevariandid ja tootesortimendid.
9. Toote hinnagruppide seadistamine.
10. Toote hinnakujunduse seadistamine. Selle toimingu raames seadistate ka hinnakorrektsioonid, allahindlused ja allahindluse perioodid.
11. Töötajate seadistamine.

    > [!NOTE]
    > Peate määrama töötajatele ka vajalikud õigused, et nad saaksid sisse logida ja teha toiminguid, kasutades kassasüsteemi.

12. Kauplusele määratavate kassa profiilide konfigureerimine. See toiming hõlmab mitmeid toiminguid, nagu registrite, ühenduseta profiilide ning kviitungivormingute ja -profiilide seadistamine.

Vaadake kõik eeltingimustes nimetatud toimingud üle ja tehke ainult teid puudutavad toimingud.

### <a name="set-up-a-store"></a>Kaupluse seadistamine

Kui eeltingimuseks olevad ülesanded on täidetud, täitke kaupluse üksikasjade seadistamiseks järgmised ülesanded.

1. Looge kauplus.
2. Kauplusele käibemaksugrupi määramine.
3. Kauplusele aktsepteeritavate makseviiside määramine.
4. Üksikasjade lisamine oma kauplustes pakutavatele toodete kirjeldusse. Näiteks saate lisada rtf-teksti ja pilte. Toote üksikasjad kuvatakse erinevates kontekstides, nt kassaregistri või prinditud siltidel.
5. Lisage kauplus organisatsiooni vaikehierarhiasse, mis on määratud eesmärgile **Jaemüügi sortiment**, **Jaemüügi täiendamine** või **Jaemüügi aruandlus**.

### <a name="after-you-set-up-a-store"></a>Pärast kaupluse seadistamist

Kui kaupluse üksikasjad on sisestatud, täitke uue kaupluse andmete kassasse saatmised järgmised ülesanded.

1. Kaupluse kassaregistrite konfigureerimine.
2. Tootesortimentide määramine kauplusele.
3. Sortimentide töötlemine, et luua sortimenti kaasatav tooteloend ja teha tooted kaupluses kättesaadavaks.
4. Andmete (numbriseeriad, riistvaraprofiilid ja kassaekraanide paigutus) saatmine kassa registritesse.
5. Kaupluse avaldamine kaupluse andmete saatmiseks kassasse.
6. Tööde käivitamine kaupluse andmete saatmiseks kassasse.

## <a name="organization-hierarchies"></a>Organisatsiooni hierarhiad

Commerce kasutab organisatsiooni hierarhiaid kanalite struktureerimiseks. Organisatsiooni hierarhia kajastab ettevõttesse kuuluvate organisatsioonide vahelisi seoseid. Kaupluste seadistamisel saate need lisada organisatsiooni hierarhiasse. Seejärel on sortimentide, täiendamise ja aruandluse jaoks kasutatavad andmed kaupluste vahel ühiskasutuses.

> [!NOTE]
> Commerce’i müügifunktsiooni kasutamiseks peab suvandi **Mitu saajat** konfiguratsioonivõti olema lubatud. Selle konfiguratsioonivõtme leiate **Kaubanduse konfiguratsiooni** võtmetest asukohas **Süsteemihaldus**\> **Seadistus** \> **Litsentsi konfiguratsioon**. See on nõutav erinevate valideerimiste tõttu, mis põhinevad müügitellimuse rea tasemel konfigureeritud tarneaadressil.



[!INCLUDE[footer-include](../includes/footer-banner.md)]