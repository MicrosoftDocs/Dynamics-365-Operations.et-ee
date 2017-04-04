---
title: "Isikupärastatud ülevaade soovitused"
description: "Dynamics 365 toiminguteks, toote soovitused kuvamiseks Müügikoht (POS) seadme võimet. Soovitused on üksused, mida klient võib olla huvitatud oma ostuajalugu, oma lemmikute loendi üksuste ja teiste klientide internetist ostetud kaupade ja Telliskivi-ja mördi kauplustes. Jaemüüjad suurte kataloogide, soovitused aidata klient toote avastus. Autor tutvustab tooteid, mis on suunatud kliendi huve ja osta harjumusi, toote soovitused aitavad jaemüüjad up-sell ja ristsaastumise müüa ja tõstavad klientide hoidmine. Dynamics 365 toiminguteks, toote soovitused on powered by kognitiivse teenuste ja Microsoft Azure&quot;i masinõppe."
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

# <a name="personalized-product-recommendations-overview"></a>Isikupärastatud ülevaade soovitused

Dynamics 365 toiminguteks, toote soovitused kuvamiseks Müügikoht (POS) seadme võimet. Soovitused on üksused, mida klient võib olla huvitatud oma ostuajalugu, oma lemmikute loendi üksuste ja teiste klientide internetist ostetud kaupade ja Telliskivi-ja mördi kauplustes. Jaemüüjad suurte kataloogide, soovitused aidata klient toote avastus. Autor tutvustab tooteid, mis on suunatud kliendi huve ja osta harjumusi, toote soovitused aitavad jaemüüjad up-sell ja ristsaastumise müüa ja tõstavad klientide hoidmine. Dynamics 365 toiminguteks, toote soovitused on powered by kognitiivse teenuste ja Microsoft Azure'i masinõppe.

<a name="scenarios"></a>Stsenaariumid
---------

Toote soovitused on lubatud POS järgmistel juhtudel. Need on saadaval pilve POS ja kaasaegne POS (MPOS).

1.  Kohta ning **toote üksikasjad** leht:

-   Kui poodi seostada külastust on **toote üksikasjad** lehele, kui lehekülgi vaadates varasemaid tehinguid üle erinevaid kanaleid, soovitus Mootor soovitab täiendavaid esemeid võivad kokku osta.
-   Kui poes siduda lisab kliendile tehingu ja seejärel külastab ka **toote üksikasjad** lehel soovitus Mootor pakub isikupärastatud soovitused, kasutades kliendi tehingute ajalugu.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Kohta ning **tehingu** leht:

-   Soovitus mootor teeb kaupu ostukorvi sisu kogu nimekirja.
-   Kui poes siduda lisab kliendile tehingu, soovitus Mootor annab isiklikke soovitusi kasutades kliendi tehingute ajalugu ja üksuste korvi.

**Märkus** Kuva soovitused on **tehingu** lehel vahendaja peab värskendama ekraani paigutuse Dynamics 365 toiminguteks. Selle **soovitused** kontrolli tuleb loobuda edasi ning **tehingu** lehel. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Kohta ning **kliendi andmed** leht:
    -   Soovitus Mootor soovitab kasutaja ID ja kliendi lemmikute loendi üksusi.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Dynamics 365 POS soovitusi toimingute konfigureerimine
Toote soovitusi seadistamiseks peate tegema järgmist.

1.  Veenduge, et olete valinud õige **juriidilise isiku**.
2.  Liikuge **üksus poe**, valige **jaemüük**, ja seejärel klõpsake **värskendada**. ** ** see kasutada Näidisandmetes (või andmete) toimiv andmebaas ja teisaldage see olem poest.
3.  Valikuline: Display soovitusi tehingu ekraanil, minge ** paigutus, **valida teie paigutus, käivitada selle **ekraani paigutuse disainer**,** ** ja siis tilk on ** soovitused kontrolli ** vajaduse korral.
4.  Mine **hulgi parameetrid**, valige **masinõpet**, valige ** Jah ** alusel **soovitused POS lubade kasutada programmi**.
5.  Vt soovitused POS, käivitage globaalne konfiguratsiooni töö **1110**. POS ekraani paigutuse disainer tehtud muudatuste kajastamiseks kanali konfiguratsiooni töö käivitamiseks **1070**.

## <a name="how-does-it-work"></a>[]()Kuidas see toimib?
Kui värskendate ning **üksus poe** üksus, toimuvad järgmised toimingud.

-   Kognitiivse teenuste nõutud vormingusse kaevandatud Dynamics 365 toimingute toimiv andmebaas ja ettevõte poodi saata.
-   Andmeid kasutatakse Azure andmed tehase (ADF) puhastada andmeid, kasutades taru skripte ADF-i tegevuse raames. Puhastatud andmete talletamise bloobimälu.
-   Bloobimälu andmeid kasutavad kognitiivse services API treenida soovitus mudel.

Kui lülitate **lubade kasutada soovitused programmi** ja konfiguratsiooni tööde, järgmisi toiminguid.

-   Mudel mandaadi ID API korjatud ja on salvestatud toimingute toimiv andmebaas Dynamics 365, AOS Web.config, samuti jaemüügi server.
-   Mudel mandaati ja ID tehakse kättesaadavaks CRT, et nõuab toote soovitused pilve POS ja MPOS ühendusega režiimis saab olla au.


<a name="see-also"></a>Vt ka
--------

[Lisada soovitusi kontrolli tehingu lehele POS seade](add-recommendations-control-pos-screen.md)


