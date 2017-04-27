---
title: "Isikupärastatud tootesoovituste ülevaade"
description: "Microsoft Dynamics 365 for Operationsis saab tootesoovitused kuvada kassa (POS) seadmes. Soovitused on kaubad, millest klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda. Suurte kataloogidega jaemüüjate puhul aitavad soovitused kliendil tooteid avastada. Näidates tooteid, mis on suunatud kliendi huvidele ja ostuharjumustele, võivad tootesoovitused aidata jaemüüjatel lisamüüki ning ristmüüki teha ja klienti hoida. Microsoft Dynamics 365 for Operationsis töötavad tootesoovitused kognitiivsete teenuste ja Microsoft Azure’i masinõppe toel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Isikupärastatud tootesoovituste ülevaade

[!include[banner](includes/banner.md)]


Microsoft Dynamics 365 for Operationsis saab tootesoovitused kuvada kassa (POS) seadmes. Soovitused on kaubad, millest klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda. Suurte kataloogidega jaemüüjate puhul aitavad soovitused kliendil tooteid avastada. Näidates tooteid, mis on suunatud kliendi huvidele ja ostuharjumustele, võivad tootesoovitused aidata jaemüüjatel lisamüüki ning ristmüüki teha ja klienti hoida. Microsoft Dynamics 365 for Operationsis töötavad tootesoovitused kognitiivsete teenuste ja Microsoft Azure’i masinõppe toel.

<a name="scenarios"></a>Stsenaariumid
---------

Tootesoovitused on aktiivsed järgmiste kassastsenaariumide puhul. Need on saadaval pilvekassas või Modern POS-is (MPOS).

1.  Lehel **Toote üksikasjad** toimub järgmine.

-   Kui poemüüja läheb varasemate kannete vaatamise käigus erinevate kanalite lõikes lehele **Toote üksikasjad**, soovitab soovituste mootor täiendavaid kaupu, mida tõenäoliselt koos ostetakse.
-   Kui poemüüja lisab kandele kliendi ja läheb siis lehele **Toote üksikasjad**, edastab soovituste mootor kliendi kannete ajaloo põhjal isikupärastatud soovitusi.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Lehel **Kanne** toimub järgmine.

-   Soovituste mootor soovitab kaupu kogu ostukorvis oleva kaupade loendi alusel.
-   Kui poemüüja lisab kandele kliendi, edastab soovituste mootor kliendi kannete ajaloo ja ostukorvis olevate kaupade põhjal isiklikke soovitusi.

**Märkus** Soovituste kuvamiseks lehel **Kanne** peab jaemüüja muutma Dynamics 365 for Operationsis ekraani paigutust. Juhtelement **Soovitused** tuleb paigutada lehele **Kanne**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Lehel **Kliendi üksikasjad** toimub järgmine.
    -   Soovituste mootor soovitab kaupu kasutaja ID ja kliendi sooviloendis olevate kaupade alusel.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Microsoft Dynamics 365 for Operationsi konfigureerimine kassasoovituste lubamiseks
Tootesoovituste seadistamiseks tuleb teha järgmist.

1.  Veenduge, et oleks valitud õige **juriidiline isik**.
2.  Minge jaotisse **Üksuse kauplus**, valige **Jaemüük** ja klõpsake siis nuppu **Värskenda**.** **Sellisel juhul kasutatakse demoandmeid (või teie andmeid) teie tegevuse andmebaasis ja viiakse need üksuse kaupluse alla.
3.  Valikuline: soovituste kuvamiseks kande ekraanil minge jaotisse **Ekraanipaigutus, **valige ekraanipaigutus, käivitage **Ekraanipaigutuse kujundaja**** **ja paigutage siis **soovituste juhtelement **vajalikku kohta.
4.  Avage **Jaemüügi parameetrid**, valige **Masinõpe** ja valige **Jah **jaotisest **Luba kassasoovitused**.
5.  Soovituste nägemiseks kassal käivitage globaalne konfigureerimistöö **1110**. Kassa ekraanipaigutuse kujundajas tehtud muudatuste kajastamiseks käivitage kanali konfigureerimistöö **1070**.

## <a name="how-does-it-work"></a>[]()Kuidas see käib?
Valiku **Üksuse kauplus** värskendamisel toimuvad järgmised tegevused.

-   Kognitiivsete teenuste nõutavas vormingus andmed ekstraktitakse Microsoft Dynamics 365 for Operationsi tegevuse andmebaasist ja saadetakse üksuse kauplusse.
-   Azure Data Factory (ADF) kasutab neid andmeid andmete puhastamiseks Hive’i skriptide abil ADF-tegevuste käigus. Puhastatud andmed salvestatakse bloobimällu.
-   Bloobimälust võetud andmeid kasutab kognitiivsete teenuste API soovitusmudeli väljaõpetamiseks.

Kui lülitate valiku **Luba soovitused** sisse ja käivitate konfigureerimistööd, siis toimuvad järgmised tegevused.

-   API võtab mudeli identimisteabe ja ID ning salvestab need Dynamics 365 for Operationsi tegevuse andmebaasi, AOS-i web.config-faili ja samuti jaemüügiserverisse.
-   CRT-le tehakse kättesaadavaks mudeli identimisteave ja ID, et saaks arvestada pilvekassa ja MPOS-i tootesoovituste kutseid veebirežiimis.


<a name="see-also"></a>Vt ka
--------

[Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele](add-recommendations-control-pos-screen.md)




