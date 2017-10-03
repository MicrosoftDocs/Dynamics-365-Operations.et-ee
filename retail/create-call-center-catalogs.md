---
title: "Kõnekeskuse kataloogi loomine"
description: "See artikkel annab ülevaate kõnekeskusele kataloogi loomise protsessist."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 28aaa84c11a897b895b2a106ca5f0cd6168997b2
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017

---

# <a name="create-a-call-center-catalog"></a>Kõnekeskuse kataloogi loomine

[!include[banner](includes/banner.md)]


See artikkel annab ülevaate kõnekeskusele kataloogi loomise protsessist. 

Kõnekeskuses saate kasutada tootekatalooge, et tuvastada tooteid, mida soovite klientidele pakkuda. Kõnekeskused kasutavad tavaliselt prinditud katalooge. Trükitud kataloogi kujundust ja tootmist hallatakse väljaspool Microsoft Dynamics 365 for Retaili. Kuid saate luua ja talletada kataloogi digitaalse vormi, kasutades samu vorme, mida kasutate võrgus jaemüügikataloogide seadistamiseks. Enne kataloogi loomist tuleb seadistada toote sortimendid ja määrata sortimendid kõnekeskusele. Seejärel saate lisada tooteid kataloogi, valides need sortimentidest. Pärast toodete lisamist kataloogi ja kataloogi lõpetamist tuleb kataloog andmete õigsuse kontrollimiseks kinnitada. Seejärel tuleb kataloog ülevaatamiseks ja heakskiitmiseks esitada. Kui kataloog on kinnitatud, võib selle avaldada. Kui kõnekeskuse kataloog on loodud, saate kataloogi avaldamise hetkel kataloogi andmetest hetktõmmise teha. See hetktõmmise funktsioon võimaldab juurdepääsu kataloogi konkreetsele versioonile isegi siis, kui kataloogi hiljem muudetakse ja uuendatakse. Kõnekeskuse kataloogid saab seadistada ka nii, et neis sisalduvad järgmised valikulised funktsioonid.

-   **Lähtekoodid** – koodid, mida kasutatakse kliendi reageeringu jälgimiseks konkreetsetele kataloogipostitustele.
-   **Tasuta tooted** – kliendi tellimusse lisatasudeta kaasatud tooted. Need tooted lisatakse kataloogi lähtekoodi tellimusse sisestamisel automaatselt tellimusele.
-   **Skriptid** – tekstid, mida kõnekeskuse töötaja kliendile müügitellimuse loomisel ette loeb. Skriptid võivad sisaldada tervitusi või ostusoovitusi.
-   **Kaupade ülesmüük või ristmüük** – tellimusele teatud toote lisamisel soovitusena kuvatavad kaubad.

Need suvandid tuleb seadistada enne kataloogi kinnitamist ja avaldamist.

## <a name="prerequisites"></a>Eeltingimused 
Enne alustamist peavad olema täidetud järgmised ülesanded.

-   Toodete ja tootesortimentide seadistamine.
-   Jaemüügitoodete seadistamine.
-   Sortimendi seadistamine.
-   Kõnekeskuse loomine.
-   Seadistage kõnekeskus.
-   Organisatsioonihierarhiasse kõnekeskuse lisamine.
-   Organisatsioonihierarhia loomine või muutmine.

## <a name="create-a-catalog"></a>Kataloogi loomine
Esmalt tuleb luua kataloog, lisada kataloogi tooted ja vaadata seejärel üle ning uuendada toodete atribuute.

## <a name="validate-the-catalog"></a>Kataloogi valideerimine
Kui olete kataloogi seadistamise lõpetanud, peate selle valideerima. Valideerimisprotsess kontrollib, kas kanali- ja tooteatribuutide jaoks nõutavad andmed on terviklikud ja kehtivad ning kas kataloogi saab avaldada.

## <a name="submit-the-catalog-for-review-and-approval"></a>Kataloogi esitamine ülevaatuseks ja kinnitamiseks
Kui kataloog on kontrollitud, saate esitada kataloogi ülevaatamiseks ja kinnitamiseks. Kataloog peab olema kinnitatud enne avaldamist. Töövoo saate konfigureerida nii, et kataloogid kinnitatakse automaatselt või need nõuavad käsitsi kinnitamist.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Valikuline: lähtekoodide, tasuta toodete ja skriptide lisamine
Saate sisestada kõnekeskuse kataloogi ka järgmisi üksusi. Need üksused on valikulised.

-   **Lähtekoodide** abil saavad trükitud katalooge pakkuvad ettevõtted jälgida kliendi reageeringut kindlatele kataloogidele. Lähtekoodid trükitakse sageli kataloogi tagaküljele ja sisestatakse müügitellimusse, kui klient sooritab ostu. Lähtekoodi kataloogi lisamiseks peate esmalt looma sihtturu. Sihtturg vastendatakse tavaliselt omandisse kuuluva või renditud postiloendiga.
-   **Tasuta tooted** on kampaaniakaubad, mis lisatakse kataloogi viitamisel kliendi tellimusele tasuta.
-   **Skriptide** abil saab suunata töötaja suhtlust klientidega kataloogi või kataloogis oleva toote kontekstis.

## <a name="publish-the-catalog"></a>Kataloogi avaldamine
Kõnekeskuse jaoks kataloogi avaldamisega saate tooteteabe kataloogis lõpetada. Avaldamine näitab ka, et kataloog on valmis lisategevusteks, mida soovite teha. Näiteks saate luua trükitud kataloogi. Katalooge saab avaldada käsitsi või kasutades pakktöötlust graafiku alusel avaldamiseks. Enne kataloogi avaldamist peab kataloog olema kontrollitud ja kinnitatud. Kataloogi muutmiseks pärast avaldamist saate selle tagasi võtta ja siis uuesti avaldada.




