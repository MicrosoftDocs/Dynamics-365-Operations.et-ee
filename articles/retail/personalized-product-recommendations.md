---
title: Isikupärastatud tootesoovitused
description: See teema sisaldab teavet Dynamics 365 for Retaili tootesoovituste kohta, mida saab kassaseadmes kuvada.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c73bc10332329e81986a259969f8fe34b57f4ee6
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606995"
---
# <a name="personalized-product-recommendations"></a>Isikupärastatud tootesoovitused

[!include [banner](includes/banner.md)]

> [!NOTE]
> Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame. Lisateavet vt teemast [Eemaldatud või aegunud funktsioonid](../dev-itpro/migration-upgrade/deprecated-features.md).

Rakenduses Dynamics 365 for Retail saab tootesoovitused kuvada kassaseadmes. Soovitused on kaubad, millest klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda. Suurte kataloogidega jaemüüjate puhul aitavad soovitused kliendil tooteid avastada. Näidates tooteid, mis on suunatud kliendi huvidele ja ostuharjumustele, võivad tootesoovitused aidata jaemüüjatel lisamüüki ning ristmüüki teha ja klienti hoida. Rakenduses Dynamics 365 for Retail toimivad jaemüügi tootesoovitused kognitiivsete teenuste ja Microsoft Azure’i masinõppe abil.

## <a name="scenarios"></a>Stsenaariumid

Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul. Need on saadaval pilvekassas või Modern POS-is (MPOS).

1. Lehel **Toote üksikasjad** toimub järgmine.

    - Kui poemüüja läheb varasemate kannete vaatamise käigus erinevate kanalite lõikes lehele **Toote üksikasjad**, soovitab soovituste mootor täiendavaid kaupu, mida tõenäoliselt koos ostetakse.
    - Kui poemüüja lisab kandele kliendi ja läheb siis lehele **Toote üksikasjad**, edastab soovituste mootor kliendi kannete ajaloo põhjal isikupärastatud soovitusi.

    [![Soovitused lehel Toote üksikasjad](./media/proddetails.png)](./media/proddetails.png)

2. Lehel **Kanne** toimub järgmine.

    - Soovituste mootor soovitab kaupu kogu ostukorvis oleva kaupade loendi alusel.
    - Kui poemüüja lisab kandele kliendi, edastab soovituste mootor kliendi kannete ajaloo ja ostukorvis olevate kaupade põhjal isiklikke soovitusi.

    > [!NOTE]
    > Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 for Retailis ekraanipaigutust. Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**.

    [![Soovitused lehel Kanne](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3. Lehel **Kliendi üksikasjad** soovitab soovituste mootor kaupu kasutaja ID ja kliendi sooviloendis olevate kaupade alusel.

    [![Soovitused lehel Kliendi üksikasjad](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Dynamics 365 for Retaili konfigureerimine kassasoovituste kuvamiseks

Tootesoovituste seadistamiseks tuleb teha järgmist.

1. Veenduge, et oleks valitud õige **juriidiline isik**.
2. Avage jaotis **Üksuse kauplus**, valige **Jaekaubandus** ja seejärel klõpsake käsku **Värskenda**. See kasutab teie tegevuse andmebaasis olevaid demoandmeid (või teie andmeid) ja teisaldab need üksuse kauplusesse.
3. Valikuline: soovituste kuvamiseks kande ekraanil minge jaotisse **Ekraanipaigutus**, valige ekraanipaigutus, käivitage **Ekraanipaigutuse kujundaja** ja paigutage siis **soovituste juhtelement** vajalikku kohta.
4. Avage **Retaili parameetrid**, valige **Masinõpe** ja valige **Jah** jaotisest **Luba kassasoovitused**.
5. Soovituste nägemiseks kassal käivitage globaalne konfigureerimistöö **1110**. Kassa ekraanipaigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfigureerimistöö **1070**.

## <a name="how-does-it-work"></a>Kuidas see käib?

Valiku **Üksuse kauplus** värskendamisel toimuvad järgmised tegevused.

- Kognitiivsete teenuste nõutavas vormingus andmed eraldatakse Dynamics 365 for Retaili operatsiooniandmebaasist ja saadetakse üksuse kauplusse.
- Azure Data Factory (ADF) kasutab neid andmeid andmete puhastamiseks Hive’i skriptide abil ADF-tegevuste käigus. Puhastatud andmed salvestatakse bloobimällu.
- Bloobimälust võetud andmeid kasutab kognitiivsete teenuste API soovitusmudeli väljaõpetamiseks.

Kui lülitate valiku **Luba soovitused** sisse ja käivitate konfigureerimistööd, siis toimuvad järgmised tegevused.

- API-st võetakse mudeli identimisteave ja ID ning need salvestatakse Dynamics 365 for Retaili tegevuse andmebaasi, AOS-i web.config-faili ja samuti jaemüügiserverisse.
- CRT-le tehakse kättesaadavaks mudeli identimisteave ja ID, et saaks arvestada pilvekassa ja MPOS-i tootesoovituste kutseid veebirežiimis.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Tõrkeotsing, kui tootesoovitused on juba lubatud

- Liikuge kohta **Jaemüügi parameetrid** \> **Masinõpe** \> **Keela tootesoovitused** ja käivitage **Globaalne konfigureerimistöö \[1110\]**. Kui te ei leia vahekaarti **Masinõpe**, võtke ühendust Dynamicsi toega.
- Kui olete oma kandekuvale lisanud **soovituste juhtelemendi**, kasutades **ekraanipaigutuse kujundajat**, eemaldage ka see.

## <a name="additional-resources"></a>Lisaressursid

[Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele](add-recommendations-control-pos-screen.md)
