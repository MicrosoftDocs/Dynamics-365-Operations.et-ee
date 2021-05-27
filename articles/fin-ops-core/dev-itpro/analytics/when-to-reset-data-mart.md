---
title: Millal andmevakka lähtestada?
description: Selles teemas loetletakse tingimused, mida võib saada parandada andmevaka lähtestamisega, ja tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988988"
---
# <a name="when-to-reset-a-data-mart"></a>Millal andmevakka lähtestada?

Andmevaka lähtestamine võib aega võtta. Olenevalt olukorrast ei pruugi see toiming olla vajalik lahendus. Selles teemas loetletakse nii tingimused, mida võib saada parandada andmevaka lähtestamisega, kui ka tingimused, mille korral teie andmevaka lähtestamine on tõenäoliselt abiks.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Millal tuleb andmevakk lähtestada?
Enne andmevaka lähtestamist laakuge järgmist. Ühele või mitmele küsimusele jaatavalt vastamine võib näidata, et teie organisatsioon võib andmevaka lähtestamisest kasu saada.

- Kas rakenduse andmebaas taastati?
- Kui olete avanud tugijuhtumi ja tugiinsener on juhendanud teid lähtestama andmevaka tõrkeotsingu sammu osana?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Millal pole andmevaka lähtestamine sobiv lahendus?
Mõne olukorra puhul me ei soovita andmevakka lähtestada. Need hõlmavad järgmist. 

- Teil esineb andmete sünkroonimisega seotud jõudlusprobleeme. 
- Kui teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster. 
  - **Puuduvad andmed** 
  - **Kinnise integratsiooni olek** 
  - **Aegunud kirjed** – aegunud kirjed ei pruugi andmevaka lähtestamist alati õigustada. Kui teil on suur andmekomplekt, võtab lähtestamisprotsess aega, kuid tõenäoliselt on see täiustus.
 
## <a name="what-is-a-data-mart-reset"></a>Millal lähtestada andmevakka?
- Lähtestamine algab ainult siis, kui olemasolevad ülesanded on lõpetatud. See tagab, et vanu andmeid ei lisata. Selles punktis võite näha järgmist teadet: „Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda. Proovige hiljem uuesti.”
- Lähtestamine keelab integratsioonitoimingud ja kustutab kõik andmevaka andmed. Integratsioon lubatakse uuesti.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Kui lähtestan andmed marti, kas kaotan aruanded, mis ma juba kujundanud olen? 
Ei, teie aruandeid talletatakse SQL-tabelites, mida ei mõjuta andmete lähtestamine marti. Kui olete mures mõne loodud aruande kaotamise pärast, saate varundada kujundused, mida te ei soovi kaotada. Nende varundamiseks avage aruandekujundaja ja minge **Ettevõtte > Ettevõtted > Koosteüksused > Eksport**.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Kas kõigi kasutajate puhul tuleb andmete lähtestamiseks süsteemist väljuda?
Ei, kasutajad saavad andmete marti lähtestamise ajal süsteemiga tööd jätkata. Kuid enne lähtestamist ei pääse nad juurde aruannetele, mis on loodud finantsaruandluse aru anda. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
