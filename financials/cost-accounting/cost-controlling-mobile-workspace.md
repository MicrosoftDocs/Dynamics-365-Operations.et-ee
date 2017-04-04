---
title: "Kulude kontrolli mobiilne tööruumi Microsoft Dynamics 365 toimingute App"
description: "Kulude kontrolli mobiilne tööruumi, maksab center managers näen kulu center täitmise ajal ja igal pool."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 53 - 04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 84740472-494f-444c-9b74-f83b7342fd25
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 8136efb1d2669c39fcc0f80b60e80ecae983d5d8
ms.lasthandoff: 03/31/2017


---

# <a name="cost-controlling-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Kulude kontrolli mobiilne tööruumi Microsoft Dynamics 365 toimingute App

Kulude kontrolli mobiilne tööruumi, maksab center managers näen kulu center täitmise ajal ja igal pool. 

<a name="prerequisites"></a>Eeltingimused
-------------

| Eeltingimus                                                         | Kirjeldus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lugeda Microsoft Dynamics 365 toimingute mobiilne platvorm | [Dynamics 365 toimingute mobiilne platvorm](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 toiminguteks                                          | Kindlasti kasutamisel keskkond, mis on Microsoft Dynamics 365 toiminguid versiooni 1611 ning Microsoft Dynamics toimingute platvormi update 3 (November 2016). |
| Käigultparanduse KB 3215650                                                    | Installige käigultparandus et tööruumid, mis on esitatud Microsoft Dynamics 365 toiminguteks.                                                                       |
| Mobiilne seade, mis on toimingute App installitud Dynamics 365 | Lae toimingute rakenduse Dynamics 365 mobiilne app-store.                                                                                                      |

## <a name="introduction"></a>Sissejuhatus
Kulude kontrolli mobiilne tööruumi annab instant ülevaate kulukeskuste praegune toimimine võrreldes vastu planeeritud kulud tegelikud kulud. Saab puurida allapoole kuluelementide olekud.

### <a name="example"></a>Näide

Töötaja saab rahvusvahelise konverentsi kutse. Organisatsioon on seotud sõidukulude katmiseks. Töötaja küsib tema sõim, kui ta saab osaleda konverentsil. Juht avab kiiresti kas ta on töötaja osalema konverentsil eelarve kontrolli mobiilne tööruumi mobiiltelefoni kulud.

### <a name="data-security"></a>Andmeturve

Kulude kontrolli tööruumi andmed on tagatud kasutaja mandaati. Hind center manager on lubatud ainult oma kulukeskuse andmeid vaadata. Kuluarvestuse mooduli juhitakse juurdepääsu turvalisus. Kulu raamatupidajate määratleda kontrolli mobiilne tööruumi konfiguratsiooni kuluarvestuse moodulis. Pärast toimingute rakenduse Microsoft Dynamics 365 avaldamist tööruumi, on esitatud toimingute mobiilse rakenduse Dynamics 365. See tagab, et kõik kulud center juhid organisatsiooni vaadata andmeid samas vormis.

### <a name="actions-views-and-links"></a>Meetmed avaldada ja lingid

Kulusid kontrollides mobiilne tööruumi Dynamics 365 toimingute App pakub järgmisi meetmeid, seisukohti ja lingid:

-   Tegevused 
    -   Valige **koosseisude** valida paigutus.
    -   Valige **maksab objektide** valida kulukeskuste soovitud andmete filtreerimine. **Märkus:** loend kuvatakse vastavalt antud mooduli kuluarvestuse juurdepääsu.

<!-- -->

-   Mis on valitud vastavalt **meetmete** ja mis on konfigureeritud kuluarvestuse mooduli, saate vaadata järgmist kaardid. Summa on sama formaati näidata: tegelik, eelarve-, dispersioon- ja dispersiooni %. 
    -   Tegelik vs eelarve (jooksva perioodi)
    -   Tegelik parandatud eelarve (jooksva perioodi)
    -   Tegelik vs eelarve (müügitulu)
    -   Tegelik parandatud eelarve (müügitulu)
    -   Tegelik vs eelarve (Kasvavalt tänaseni)
    -   Tegelik parandatud eelarve (Kasvavalt tänaseni)

<!-- -->

-   Lingid
    -   Praeguse perioodi andmed.
    -   Andmed eelmise perioodi.
    -   Andmed aastast kuupäevani.

Lingid valimisel kuvatakse kaardi kohta kuluelement. Kaardid summa kuvatakse järgmisel kujul: tegelik, eelarve, eelarve erinevus, eelarve erinevuse %, parandatud eelarve, muudetud eelarve erinevus ja muudetud eelarve erinevuse %.  [![kulude kontroll](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="get-started"></a>Alusta
Järgmiste juhiste abil mobiilsideseadmes kasutama kulude kontrolli mobiilirakendus.

1.  Mobiilirakenduse poes, alla laadida ja installida Microsoft Dynamics 365 toimingute app.
2.  Käivitada rakendus oma seadmes.
3.  Sisestage oma Dynamics 365 URL.
4.  Sisestage ettevõtte sisse logima. Sisestage **USMF**.
5.  Esimene kord, kui logite sisse, küsitakse kasutajanime ja parooli teie Microsofti Dynamics 365 operatsioonide tarbeks. Sisestage oma kasutajanimi ja parool. Pärast sisselogimist, näed saadaval tööruumid firmale.

Saate vaadata oma mobiilirakendus tööruumid, peab esmalt avaldama soovitud tööruumid toimingute rakenduse Dynamics 365.

1.  Käivitage Dynamics 365 toiminguteks.
2.  Mine **süsteemi halduse**&gt;**install**&gt;**süsteemi parameetrid**.
3.  Valige **Halda mobiilirakendus**.
4.  Valige tööruum ** kulude kontrolli ** avaldama mobiilsel platvormil.
5.  Valige **avaldada tööruumi**.
6.  Värskendage seadme avaldatud tööruumid.

## <a name="view-the-performance-of-your-cost-center"></a>Vaata oma kulud kaudu täitmise
1.  Mobiilsideseadmes, valige selle **maksab kontrollida** tööruumi.
2.  Valige **maksab objekti kontrollimise**.
3.  Klõpsake **meetmete**.
4.  Klõpsake **Select configuration** kulu kontrollida paigutuse valimiseks.
5.  Click **Done**.
6.  Klõpsake **meetmete**.
7.  Klõpsake **valige kulu objekti** valida kulukeskuste, millele teile on antud juurdepääs.
8.  Click **Done**.
9.  Vaata oma kulud kaudu üldist tulemuslikkust.
10. Klõpsake **andmed praeguse perioodi**.
11. Vaata kuluelementide toimimist.
12. Saate otsida ka teatud kuluelemendid.



