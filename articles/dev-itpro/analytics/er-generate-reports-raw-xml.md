---
title: Aruannete loomine sisu lisamisega XML-toorandmetena
description: "Saate kujundada elektroonilise aruandluse vormingud, mis loovad väljaminevaid dokumente XML-vormingus."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 56a5f53e1d3da8aa57e98e7d34fbc9c4005b6df8
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="generate-reports-by-adding-content-as-raw-xml"></a>Aruannete loomine toore XML-i sisu lisamisega

[!include[banner](../includes/banner.md)]

Saate kasutada uut vorminguelementi **RAW XML**, et kujundada elektroonilise aruandluse vormingud, mis loovad väljaminevad dokumendid XML-vormingus. Mõnel juhul võite eelistada toor-XML-i andmete lisamist neile aruannetele ühel või mitmel järgmisel põhjusel.

- Toor-XML-i kasutamine aruande algse kujunduse ja edasise haldamise jaoks on mugavam, kuna XML-struktuuri saab automaatselt luua, käivitades käitusaja avaldise. Seetõttu pole kujundamise ajal vaja mitme vorminguelemendi jaoks määrata mitut seost. See on võimalik, kui kasutatavad andmeallikad sisaldavad teavet, mida saab kasutada aruande loomise ajal XML-elementide koostamiseks.
- Ühtki muud meetodit ei saa kasutada aruande täitmiseks XML-sisuga, mis on varem süsteemi vastu võetud ja salvestatud. Näiteks võib loodav XML-vastus sisaldada varem saadetud XML-taotluse sisu.
- Ühtki muud meetodit ei saa kasutada loodud dokumenti tärkide sisestamiseks nende numbrikoodide põhjal. Mõne keele ja tärgi puhul pole seda tüüpi koode olemas. Need on näiteks kreeka keele täht roo (ρ) ja HTML-olemikoodid, nagu \&eacute akuudiga *e* (é) jaoks.

> [!NOTE]
> Arvestage, et raamistik ei kontrolli, kas loodud dokumenti vorminguelemendi **RAW XML** abil paigutatav XML-sisu on õige.

Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhiseid **Elektrooniline aruandlus: XML-toorandmete kasutamine XML-aruannete loomiseks (1. osa)** ja **Elektrooniline aruandlus: XML-toorandmete kasutamine XML-aruannete loomiseks (1. osa)**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** ning mille saab alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684). Need tegevusejuhised selgitavad teile elektroonilise aruandluse vormingu konfigureerimise protsessi XML-toorandmete sisestamiseks loodud failidesse.
