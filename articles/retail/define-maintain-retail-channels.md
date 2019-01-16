---
title: "Jaemüügikanalite määratlemine ja haldamine"
description: "Selles teemas antakse ülevaade füüsilistele kaupluste (mida nimetatakse Microsoft Dynamics 365 for Retailis jaekauplusteks) seadistamise protsessist. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast jaekaupluse seadistamist."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.contentlocale: et-ee
ms.lasthandoff: 01/04/2019

---

# <a name="define-and-maintain-retail-channels"></a>Jaemüügikanalite määratlemine ja haldamine

[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade füüsilistele kaupluste (mida nimetatakse Microsoft Dynamics 365 for Retailis jaekauplusteks) seadistamise protsessist. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast jaekaupluse seadistamist.

Dynamics 365 for Retail toetab mitmeid jaemüügikanaleid, nagu võrgupoed, kõnekeskused ja traditsioonilised kauplused. Traditsioonilist kauplust nimetatakse jaekaupluseks. Igal kauplusel võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal. Enne kaupluse loomist tuleb seadistada kõik need elemendid. Kui olete kaupluse loonud, saate määrata seal müüdavad tooted. Saate kauplusele määrata ka töötajad, registrid ja kliendid. Viimaks peate lisama uue kaupluse organisatsioonihierarhiasse.

## <a name="setting-up-retail-stores"></a>Kaupluste seadistamine

Enne kui saate Microsoft Dynamics 365 for Retailis kaupluse seadistada, peate täitma mõne eeltingimuseks oleva ülesande. Seejärel saate luua kaupluse ja lisada üksikasjad.

### <a name="prerequisites"></a>Eeltingimused 

Enne kui saate kaupluse seadistada, peate tegema järgmised toimingud.

1. Saate konfigureerida organisatsiooni struktuuri ja seadistada organisatsiooni hierarhiad jaemüügisortimendi, täiendamise ja aruannete jaoks.
2. Saate seadistada kauplust kajastava lao.
3. Kaupluste, kaupluse väljavõtete ja väljavõttekannete numbriseeriate seadistamine.
4. Saate jaemüügi parameetreid konfigureerida.
5. Kaupluses aktsepteeritavate makseviiside seadistamine.
6. Jaemüügi kassaregistrites krediitkaardikannete töötlemiseks saate seadistada ka makseteenused.
7. Käibemaksugruppide seadistamine.
8. Jaemüügitoodete seadistamine. Selle toimingu raames seadistate ka jaemüügihierarhiad, tootevariandid ja tootesortimendid.
9. Toote hinnagruppide seadistamine.
10. Jaemüügitoodete hinnakujunduse seadistamine. Selle toimingu raames seadistate ka hinnakorrektsioonid, allahindlused ja allahindluse perioodid.
11. Töötajate seadistamine.

    > [!NOTE]
    > Peate määrama töötajatele ka vajalikud õigused, et nad saaksid sisse logida ja teha toiminguid, kasutades süsteemi Dynamics 365 for Retail jaemüügikassale.

12. Kauplusele määratavate Retail POS-i profiilide konfigureerimine. See toiming hõlmab mitmeid toiminguid, nagu registrite, ühenduseta profiilide ning kviitungivormingute ja -profiilide seadistamine.

Vaadake kõik eelduses nimetatud toimingud üle ja tehke ainult teid puudutavad toimingud.

### <a name="set-up-a-retail-store"></a>Jaemüügikaupluse häälestus

Kui eeltingimuseks olevad ülesanded on täidetud, täitke kaupluse üksikasjade seadistamiseks järgmised ülesanded.

1. Jaemüügikaupluse loomine.
2. Kauplusele käibemaksugrupi määramine.
3. Kauplusele aktsepteeritavate makseviiside määramine.
4. Üksikasjade lisamine oma kauplustes pakutavatele toodete kirjeldusse. Näiteks saate lisada rtf-teksti ja pilte. Toote üksikasjad kuvatakse erinevates kontekstides, nt kassaregistri või prinditud siltidel.
5. Lisage kauplus organisatsiooni vaikehierarhiasse, mis on määratud eesmärgile **Jaemüügi sortiment**, **Jaemüügi täiendamine** või **Jaemüügi aruandlus**.

### <a name="after-you-set-up-a-retail-store"></a>Pärast kaupluse seadistamist

Kui kaupluse üksikasjad on sisestatud, täitke uue kaupluse andmete saatmiseks rakendusse Retail POS järgmised ülesanded.

1. Kaupluse kassaregistrite konfigureerimine.
2. Tootesortimentide määramine kauplusele.
3. Sortimentide töötlemine, et luua sortimenti kaasatav tooteloend ja teha tooted kaupluses kättesaadavaks.
4. Andmete (numbriseeriad, riistvaraprofiilid ja kassaekraanide paigutus) saatmine rakenduse Retail POS registritesse.
5. Kaupluse avaldamine kaupluse andmete saatmiseks rakendusse Retail POS.
6. Tööde käivitamine kaupluse andmete saatmiseks rakendusse Retail POS.

## <a name="organization-hierarchies"></a>Organisatsiooni hierarhiad

Retail kasutab organisatsiooni hierarhiaid jaemüügikanalite struktureerimiseks. Organisatsiooni hierarhia kajastab ettevõttesse kuuluvate organisatsioonide vahelisi seoseid. Kaupluste seadistamisel saate need lisada organisatsiooni hierarhiasse. Seejärel on sortimentide, täiendamise ja aruandluse jaoks kasutatavad andmed kaupluste vahel ühiskasutuses.

