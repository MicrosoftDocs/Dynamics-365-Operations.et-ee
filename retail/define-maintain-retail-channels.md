---
title: "Jaemüügikanalite määratlemine ja haldamine"
description: "Selles artiklis antakse ülevaade Telliskivi-ja mördi kauplustes, mis on edaspidi müügipindade Microsoft Dynamics 365 operatsioonide seadistamise protsess. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast jaekaupluse seadistamist."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b775ba34ef7d88dd0b47904e4a3e9be79664f14b
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-retail-channels"></a>Jaemüügikanalite määratlemine ja haldamine

Selles artiklis antakse ülevaade Telliskivi-ja mördi kauplustes, mis on edaspidi müügipindade Microsoft Dynamics 365 operatsioonide seadistamise protsess. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast jaekaupluse seadistamist.

Hulgi- ja kaubanduse dünaamika 365 toiminguteks toetab mitme jaemüügikanalid, näiteks võrgupoed, kõnekeskused ja Telliskivi-ja mördi kauplustes. Moodulis Jaemüük ja kaubandus nimetatakse traditsioonilist kauplust kaupluseks. Igal kauplusel võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal. Enne kaupluse loomist tuleb seadistada kõik need elemendid. Kui olete kaupluse loonud, saate määrata seal müüdavad tooted. Saate kauplusele määrata ka töötajad, registrid ja kliendid. Viimaks peate lisama uue kaupluse organisatsioonihierarhiasse.

## <a name="setting-up-retail-stores"></a>Kaupluste seadistamine
Enne kauplusesse Dynamics 365 toiminguteks peate täitma mõned eelduseks olevad ülesanded. Seejärel saate luua kaupluse ja lisada üksikasjad.

### <a name="prerequisites"></a>Eeltingimused 

Enne kui saate kaupluse seadistada, peate tegema järgmised toimingud.

1.  Saate konfigureerida organisatsiooni struktuuri ja seadistada organisatsiooni hierarhiad jaemüügisortimendi, täiendamise ja aruannete jaoks.
2.  Saate seadistada kauplust kajastava lao.
3.  Kaupluste, kaupluse väljavõtete ja väljavõttekannete numbriseeriate seadistamine.
4.  Saate jaemüügi parameetreid konfigureerida.
5.  Kaupluses aktsepteeritavate makseviiside seadistamine.
6.  Jaemüügi kassaregistrites krediitkaardikannete töötlemiseks saate seadistada ka makseteenused.
7.  Käibemaksugruppide seadistamine.
8.  Jaemüügitoodete seadistamine. Selle toimingu raames seadistate ka jaemüügihierarhiad, tootevariandid ja tootesortimendid.
9.  Toote hinnagruppide seadistamine.
10. Jaemüügitoodete hinnakujunduse seadistamine. Selle toimingu raames seadistate ka hinnakorrektsioonid, allahindlused ja allahindluse perioodid.
11. Töötajate seadistamine. **Märkus:** tuleb määrata ka vastavad õigused töötajatele, et nad saavad sisse logida ja ülesannete abil Dynamics 365 Retail POS süsteem operatsioonide.
12. Kauplusele määratavate Retail POS-i profiilide konfigureerimine. See toiming hõlmab mitmeid toiminguid, nagu registrite, ühenduseta profiilide ning kviitungivormingute ja -profiilide seadistamine.

Vaadake kõik eelduses nimetatud toimingud üle ja tehke ainult teid puudutavad toimingud.

### <a name="set-up-a-retail-store"></a>Jaemüügikaupluse häälestus

Kui eeltingimuseks olevad ülesanded on täidetud, täitke kaupluse üksikasjade seadistamiseks järgmised ülesanded.

1.  Jaemüügikaupluse loomine.
2.  Kauplusele käibemaksugrupi määramine.
3.  Kauplusele aktsepteeritavate makseviiside määramine.
4.  Üksikasjade lisamine oma kauplustes pakutavatele toodete kirjeldusse. Näiteks saate lisada rtf-teksti ja pilte. Toote üksikasjad kuvatakse erinevates kontekstides, nt kassaregistri või prinditud siltidel.
5.  Lisage kauplus organisatsiooni vaikehierarhiasse, mis on määratud eesmärgile **Jaemüügi sortiment**, **Jaemüügi täiendamine** või **Jaemüügi aruandlus**.

### <a name="after-you-set-up-a-retail-store"></a>Pärast kaupluse seadistamist

Kui kaupluse üksikasjad on sisestatud, täitke uue kaupluse andmete saatmiseks rakendusse Retail POS järgmised ülesanded.

1.  Kaupluse kassaregistrite konfigureerimine.
2.  Tootesortimentide määramine kauplusele.
3.  Sortimentide töötlemine, et luua sortimenti kaasatav tooteloend ja teha tooted kaupluses kättesaadavaks.
4.  Andmete (numbriseeriad, riistvaraprofiilid ja kassaekraanide paigutus) saatmine rakenduse Retail POS registritesse.
5.  Kaupluse avaldamine kaupluse andmete saatmiseks rakendusse Retail POS.
6.  Tööde käivitamine kaupluse andmete saatmiseks rakendusse Retail POS.

## <a name="organization-hierarchies"></a>Organisatsiooni hierarhiad
Jaemüük kasutab jaemüügikanalite struktureerimiseks Microsoft Dynamics AX-i organisatsiooni hierarhiaid. Organisatsiooni hierarhia kajastab ettevõttesse kuuluvate organisatsioonide vahelisi seoseid. Kaupluste seadistamisel saate need lisada organisatsiooni hierarhiasse. Seejärel on sortimentide, täiendamise ja aruandluse jaoks kasutatavad andmed kaupluste vahel ühiskasutuses.


