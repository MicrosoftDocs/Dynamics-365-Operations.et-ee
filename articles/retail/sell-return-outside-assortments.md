---
title: Kaupluse sortimenti mittekuuluvate toodete müümine ja tagastamine
description: Rakendusega Dynamics 365 for Retail saate müüa ja tagastada tooteid väljaspool sortimenti.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 653a388de1a972fae488abd81f349d1b138fc716
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567903"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a>Kaupluse sortimenti mittekuuluvate toodete müümine ja tagastamine

[!include [banner](includes/banner.md)]

Iga jaemüüja tavapärane stsenaarium on müüa tooteid oma klientidele või võtta vastu tagastusi oma klientidelt, isegi, kui neil pole kaupluses neid kindlaid tooteid (teisisõnu tooted pole kaupluse sortimendis).

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
