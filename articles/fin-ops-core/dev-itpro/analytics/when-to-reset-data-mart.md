---
title: Millal andmevakka lähtestada?
description: Selles teemas loetletakse tingimused, mida võib saada parandada andmevaka lähtestamisega, ja tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093208"
---
# <a name="when-to-reset-a-data-mart"></a>Millal andmevakka lähtestada?

Andmevaka lähtestamine võib aega võtta. Olenevalt olukorrast ei pruugi see toiming olla vajalik lahendus. Selles teemas loetletakse nii tingimused, mida võib saada parandada andmevaka lähtestamisega, kui ka tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Millal tuleb andmevakk lähtestada?
Enne andmevaka lähtestamist laakuge järgmist. Ühele või mitmele küsimusele jaatavalt vastamine võib näidata, et teie organisatsioon võib andmevaka lähtestamisest kasu saada.

- Rakenduse andmebaas taastati, kuid andmevaka andmebaasi ei taastatud.
- Raamatupidamisperioodi kohta kuvatakse valesid andmeid, mis pole aruande kujundusega seotud probleemi tulemus.
- Raamatupidamisperioodi kohta kuvatakse valed andmed ja kirjed loetletakse lehel **Integratsiooni olek** integreerimiskatsete all aruandekujundajas (käivitage aruandekujundaja ja valige **Tööriistad > Integratsiooni olek**).
- Olete avanud tugijuhtumi ja tugiinsener on juhendanud teid lähtestama andmevaka tõrkeotsingu sammu osana.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Millal pole andmevaka lähtestamine sobiv lahendus?
Mõne olukorra puhul me ei soovita andmevakka lähtestada. Need hõlmavad järgmist. 

- Igal ajal, kui põhjus pole selles teemas loetletud.
- Teil esineb andmete sünkroonimisega seotud jõudlusprobleeme. Sellisel juhul ei ole andmevaka lähtestamine tõenäoliselt abiks.
- Kui teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster. 
  - **Puuduvad andmed** – kõigepealt eemaldage aruande kujunduse probleemid ja andmete sünkroonimise ajastusprobleemid, näiteks märkate, et faktikaart pole puuduvate andmete sisestamisest alates käivitunud.
  - **Integratsiooni kinni jäänud olek** – kui integratsioon on aeglane või näib kinni jäänuna, siis andmevaka lähtestamine tõenäoliselt probleemi ei lahenda.
  - **Lähtestamise katsed nurjusid** – kui tehti palju lähtestamise katseid ja need ei õnnestunud puuduvate andmete tõttu, soovitame avada tugijuhtumi ja teha tugiinseneriga koostööd, et analüüsida teie olukorda enne andmete uuesti lähtestamist.
  - **Aegunud kirjed** – aegunud kirjed ei pruugi andmevaka lähtestamist alati õigustada. Kui teil on suur andmekomplekt, võtab lähtestamisprotsess aega, kuid tõenäoliselt on see täiustus.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Mida andmevaka lähtestamine ei tee?  
- Lähtestamine algab ainult siis, kui olemasolevad ülesanded on lõpetatud. See tagab, et vanu andmeid ei lisata. Selles punktis võite näha järgmist teadet: „Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda. Proovige hiljem uuesti.”
- Lähtestamine keelab integratsioonitoimingud ja kustutab kõik andmevaka andmed. Integratsioon lubatakse uuesti.

> [!NOTE]
> Järgmised punktid määravad kaks asja, mida andmevaka lähtestamine *ei* tee. <br>
> - Lähtestamised ei tühjenda aruande kujundusi. <br>
> - Lähtestamised ei kustuta ettevõtte ega kasutaja andmeid, kui need pole valitud.
