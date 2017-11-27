---
title: "Süsteemi rühmitamine avatud tööloendis"
description: "Selles teemas kirjeldatakse, kuidas filtreerida avatud tööloendit mobiilsel seadmel."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6403fea54be4036f7a15c05b46f70d258d97c3e2
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="system-grouping-on-an-open-work-list"></a>Süsteemi rühmitamine avatud tööloendis

[!include[banner](../includes/banner.md)]

Süsteemi rühmitusvälja abil saate avatud tööloendit filtreerida, ilma et oleks vaja mobiilse seadme menüüelementi redigeerida.
Kui kasutatakse süsteemi rühmitamist, saab selle abil tööloendit ühel tööpäise väljal filtreerida. Süsteemi rühmitamist ei saa kasutada rea taseme väljade filtreerimiseks.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Süsteemi rühmitamise seadistamine avatud tööloendis
Süsteemi rühmitamise seadistamiseks avatud tööloendis tehke järgmist.

-   Valige mobiilse seadme menüüelemendist **Režiim: kaudne** ja **Tegevuse kood: kuva avatud tööloend**. Kättesaadavaks muutuvad järgmised valikud. Need valikud on vajalikud süsteemi rühmitamise jaoks avatud tööloendis. 

| Suvand        | Kirjeldus   | 
| ------------- | ------------- |
| Luba süsteemi rühmitamine   | Lubab süsteemi rühmitamise valitud tööloendi menüüelemendi puhul.| 
| Süsteemi rühmitusväli   | Saadaval ainult juhul, kui valiku **Luba süsteemi töö** olekuks on määratud **Jah**. Valige väli, mis määrab, kuidas komplekteerimistöö töötajate puhul rühmitatakse. Kui valite näiteks välja **ShipmentId**, skannib töötaja komplekteerimistöö rühmitamiseks saadetise ID. Seejärel määratakse kogu saadetisega seotud töö töötajale. Selleks peate looma menüüelemendi, et kasutada süsteemi rühmitatud olemasolevat tööd. Kasutage välja **Süsteemi rühmitussilt** töötaja teavitamiseks sellest, mida skannida. |
| Süsteemi rühmitussilt   | Saadaval ainult juhul, kui valiku **Luba süsteemi töö** olekuks on määratud **Jah**. Sisestage töötaja jaoks teave selle kohta, mida skannida, kui komplekteerimistöö rühmitatakse. Kui kasutate näiteks komplekteerimistöö rühmitamiseks saadetise järgi välja **ShipmentId**, võib vajalik olla väljale Saadetise ID sisestamine. Selleks peate looma menüüelemendi, et kasutada süsteemi rühmitatud olemasolevat tööd. Peale selle peate valima väljal **Süsteemi rühmitamine** rühmitamise aluseks oleva välja.|

