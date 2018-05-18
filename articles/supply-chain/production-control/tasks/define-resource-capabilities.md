--- 
title: "Ressursivõimaluste määratlemine"
description: "Ressursi võimalused kirjeldavad, milliseid operatsioone ressursid teha saavad."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 99c230c0e6a580f77d863b6f0be298615966c479
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="define-resource-capabilities"></a>Ressursivõimaluste määratlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ressursi võimalused kirjeldavad, milliseid operatsioone ressursid teha saavad. Planeerimisel vastendatakse iga töö ja operatsiooni nõuded saadaolevate ressursside võimalustega. Selles tegevuse juhises aidatakse teil ressursi võimalust luua ja seda ressursile määrata. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-resource-capability"></a>Ressursi võimaluse loomine
1. Avage Ressursi võimalused.
2. Klõpsake Uus.
3. Sisestage ressursi võimaluse ID väljale Võimalus.
    * Selle operatsiooni puhul kasutage võimaluse ID-d, et määrata võimalus, mis ressurssidel selle operatsiooni teostamiseks peab olema.  
4. Sisestage võimaluse kirjeldus väljale Kirjeldus.

## <a name="assign-capability-to-a-resource"></a>Ressursile võimaluse määramine
1. Klõpsake vahekaarti Lisa.
2. Sisestage ressursi ID väljale Ressurss.
    * Ressursi võimaluse saab määrata ühele või mitmele ressursile.  
3. Sisestage kuupäev väljale Aegumine.
    * Saate seda välja kasutades ressursile ainult piiratud ajaks võimaluse määrata.  
4. Sisestage arv väljale Prioriteet.
    * Tööde ja operatsioonide planeerimisel saate määrata, kas ressursse valitakse prioriteedi järgi. Kui otsustate selle valiku kasuks, kuid töö või operatsiooni saab soovitud kuupäevaks sooritatud rohkem kui üks ressurss, valitakse nõutava võimaluses suhtes madalaima prioriteediga ressurss.  
5. Sisestage arv väljale Tase.
    * Kui määrate tööle või operatsioonile kindla nõutava võimaluse, saate määrata ka minimaalse nõutava taseme. Sama tööd erineval kiirusel, tugevusel, suurusel jms tegevate ressursside eristamiseks saate kasutada võimaluse taset.  


