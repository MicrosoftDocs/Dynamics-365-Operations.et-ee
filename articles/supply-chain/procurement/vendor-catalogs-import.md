---
title: Hankija kataloogide importimine
description: Selles teemas kirjeldatakse hankija kataloogi andmete importimise protsessi.
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 9f85b1d1f0b1c2378dd3f278640d984c31923c35
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017870"
---
# <a name="import-vendor-catalogs"></a>Hankija kataloogide importimine
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Hankija kataloogide importimine

Dynamics 365 Supply Chain Managementis saavad ostuspetsialistid luua ja hallata katalooge, mida ettevõtte töötajad saavad kaupade ning teenuste sisemiseks kasutamiseks tellimisel kasutada. Hankekataloogi loomiseks saate lisada kaupu ja teenuseid, mille soovite töötajatele kättesaadavaks teha, importides tootekataloogi andmed või lisades tootekataloogi andmed käsitsi tooteetaloni. 

Saate laadida üles kataloogiandmed, mille hankija on edastanud Microsoft Dynamics 365 kliendist.

Tooteandmed, mille hankija edastab teile kataloogihoolduse nõude (CMR) faili kujul, peavad olema XML-vormingus. CMR-fail peab sisaldama nende toodete andmeid, mida hankija teie ettevõttele tarnib.

## <a name="import-vendor-catalog-data"></a>Hankija kataloogi andmete importimine

Hankija kataloogi andmete importimiseks peate täitma järgmised ülesanded.

1.  Seadistage andmehalduse tööruumis projekt, kus olete määratlenud andmete vastandamise reeglid. Valige **Andmehaldus** ja seejärel valige **Andmeprojektide jaoks vajalike rollide seadistamine**. 

2.  Seadistage hankekategooria hierarhia ja määrake oma hankijad hankekategooriatesse. Artiklikoodide kasutamisel lisage artiklikoodid hankekategooriatesse. Hankekategooria hierarhia seadistamise kohta lisateabe saamiseks vt jaotist [Hankekategooria hierarhia seadistamine](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3.  Konfigureerige kataloogi impordi jaoks hankija. Valige hankija ja seejärel valige **Hange** > **Seadista** > **Kataloogi importimiseks hankija konfigureerimine**.

4.  Konfigureerige töövoogu kataloogi importimiseks. Looge CMR-faili mall ja jagage seda oma hankijaga.

5.  Valige **Hanked** \> **Ühine** \> **Kataloogid** \> **Hankija kataloogid**, et luua hankija kataloog. Selles kataloogis on grupeeritud kataloogihoolduse nõude (CMR) failid, mille saate oma hankijalt. 

6.  Laadige üles CRM-fail.

7.  Vaadake üle, kinnitage või lükake hankija kataloogis olevad tooted tagasi. Tooted vastendatakse automaatselt hankekategooriatega. 
    
Kinnitatud tooted lisatakse tooteetaloni ja väljastatakse valitud juriidilistele isikutele. Hankekataloogi saab lisada ainult kinnitatud tooteid.

## <a name="generate-a-catalog-import-file-template"></a>Kataloogi importimisfaili malli loomine

Kataloogi impordifaili mall on XSD-fail, mille abil saate luua hankija toodete CMR-faili. Saate kasutada CMR-faili uue kataloogi loomiseks, olemasoleva kataloogi asendamiseks või muutmiseks.

1.  Valige **Hanked** \> **Kataloogid** \> **Hankija kataloogid** ja topeltklõpsake kataloogil, millega soovite töötada.

2.  Laadige alla kehtiv kataloogi importimise mall (XSD-fail). Lehel **Kataloogi värskendamine** valikus **Tegumiriba** vahekaardil **Kataloogid** grupis **Seostuv teave** klõpsake suvandil **Kataloogi malli loomine** ja valige **Hankekategooria**.

    -   Suvandiga **Hankekategooria** saate luua kataloogimalli, mis sisaldab hankekategooriaid, milles hankijal on lubatud tooteid pakkuda.

3. Valige dialoogikastis **Salvesta nimega** asukoht, kus soovite kataloogifaili malli talletada ja salvestage fail.

Lisateavet ja näiteid vt ajaveebipostitusest [Hankija kataloogid rakenduses Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).
