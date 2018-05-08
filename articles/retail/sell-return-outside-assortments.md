---
title: "Toodete müümine ja tagastamine väljaspool sortimenti"
description: "Dynamics 365 for Retaili puhul võite müüa ja tagastada tooteid väljaspool sortimente."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 82b3076eba0d374c80e37572233cf7ba440cc65a
ms.contentlocale: et-ee
ms.lasthandoff: 03/07/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a>Toodete müümine ja tagastamine väljaspool sortimenti

[!include [banner](includes/banner.md)]

Iga jaemüüja tavapärane stsenaarium on müüa tooteid oma klientidele või võtta vastu tagastusi oma klientidelt, isegi kui neil pole kaupluses neid kindlaid tooteid (teisisõnu tooteid pole kaupluse sortimendis).
Tüüpilised stsenaariumid on näiteks järgmised.

+ Jaemüüja ei hoia kõiki oma tooteid kindlas kaupluses. Ülejäänud tooteid hoitakse laos. Kaupluse töötaja võib aidata klienti, otsides või sirvides laos tooteid, lisada neid ostukorvi ja maksta, valides tarneviisi, näiteks tarnimise laost teatud aadressile või lastes kliendil võtta toote peale sellest laost või teisest laost.
+ Jaemüüjal ei ole kindlaid tooteid kaupluses või tal pole neid varudes kaupluses, mida klient külastas, kuid tooted on saadaval teistes kauplustes. Kaupluse töötaja saab aidata klienti, otsides või sirvides teises kaupluses olevaid tooteid, lisada neid ostukorvi ja teha maksmise, valides tarneviisi.
+ Jaemüüjal on konkreetses linnas või sihtnumbril ja nende ümbruses palju kauplusi ning ta ei soovi sundida kliente tagastama tooteid samasse kauplusse, kust need osteti. Selle asemel võivad kliendid tagastada tooteid ükskõik millisesse kauplusse.


Need üldised stsenaariumid on saadaval jaemüüjate puhul, kes kasutavad rakendust Dynamics 365 for Retail. Retailiga saab teha järgmist.
+ Otsida või sirvida tooteid teistes kauplustes.
+ Otsida või sirvida kõiki väljastatud tooteid.
+ Koostada sularahatehinguid või kliendi tellimusi.
+ Valida kliendi tellimustele tarnevõimalusi.
+ Võtta tooteid peale praegusest või mõnest muust kauplusest.
+ Tühistada tellimuse praeguses kaupluses või mõnes muus kaupluses.
+ Tagastada tellimuse kviitungiga või ilma praegusesse või teise kauplusse.

