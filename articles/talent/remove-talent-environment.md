---
title: Talenti keskkondade eemaldamine
description: See teema selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 for Talent puhul.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304133"
---
# <a name="remove-talent-environments"></a>Talenti keskkondade eemaldamine

[!include [banner](includes/banner.md)]

See teema selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 for Talent puhul.

## <a name="removing-a-test-drive-environment"></a>Proovikeskkonna eemaldamine

Talenti proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga. Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist. 

1. Avage [PowerAppsi administreerimiskeskus](https://admin.businessplatform.microsoft.com/).
2. Valige **Keskkonnad**.
3. Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain
4. Valige **Kustuta** ja kinnitage otsus. 

Olemasolev proovikeskkond eemaldatakse. Kui see on eemaldatud, saate registreerida uue proovikeskkonna. 

## <a name="removing-a-production-environment"></a>Tootmiskeskkonna eemaldamine

See teema eeldab, et olete ostnud rakenduse Talent pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu. 

Kuna üks Talenti keskkond asub ühes PowerAppsi keskkonnas, on kaks suvandit. Esimene valik hõlmab kogu PowerAppsi keskkonna eemaldamist; teine hõlmab ainult Talenti eemaldamist. Esimene suvand on soovitatav, kui lõite PowerAppsi keskkonna spetsiaalselt Talenti ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone. Teine suvand on sobiv, kui teil on PowerAppsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse PowerAppsis ja voogudes.

> [!Important]
> Enne PowerAppsi keskkonna eemaldamist veenduge, et seda ei kasutata rikasandmete integreerimiseks väljaspool Talenti ulatust. Pange tähele, et PowerAppsi vaikekeskkondasid ei saa eemaldada. 

Kogu PowerAppsi keskkonna eemaldamiseks koos Talenti ning seotud rakenduste ja voogudega tehke järgmist.

1. Avage [PowerAppsi administreerimiskeskus](https://admin.businessplatform.microsoft.com/).
2. Valige **Keskkonnad**.
3. Valige eemaldatav keskkond.
4. Valige **Kustuta** ja kinnitage otsus. 
5. Oodake, kuni kustutamine on lõpule viidud.
6. Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite Talenti tellimiseks. 
7. Valige keskkonda sisaldav Talenti projekt. 
8. Valige oma LCS-i projektis paan **Talenti rakendusehaldus**. 
9. Valige eemaldatav eksemplar. 
10. Valige **Eemalda eksemplar** ja kinnitage otsus.  

Talenti eemaldamiseks olemasolevast PowerAppsi keskkonnast tehke järgmist. Pange tähele, et tugimeeskonna kaasamine ja Talenti DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.

1. Eemaldamistaotluse käivitamiseks võtke ühendust toega.
2. Tugimeeskond edastab eemaldamise taotluse Talenti DevOpsi töörühmale. 
3. Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.
4.  Logige LCS-i sisse, kasutades kontot, mida kasutasite Talenti tellimiseks. 
5. Valige keskkonda sisaldav Talenti projekt. 
6. Valige oma LCS-i projektis paan **Talenti rakendusehaldus**. 
7. Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Nurjus**).
8. Valige **Eemalda eksemplar** ja kinnitage otsus. 

