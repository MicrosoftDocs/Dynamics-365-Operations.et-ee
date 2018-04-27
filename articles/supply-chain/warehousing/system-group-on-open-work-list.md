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
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9ca6b0d4a9909d419d6241a044336d7a02aea02
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="system-grouping-on-an-open-work-list"></a>Süsteemi rühmitamine avatud tööloendis

[!INCLUDE [banner](../includes/banner.md)]

Süsteemi rühmitusvälja abil saate avatud tööloendit filtreerida, ilma et oleks vaja mobiilse seadme menüüelementi redigeerida.
Kui kasutatakse süsteemi rühmitamist, saab selle abil tööloendit ühel tööpäise väljal filtreerida. Süsteemi rühmitamist ei saa kasutada rea taseme väljade filtreerimiseks.

## <a name="set-up-system-grouping-on-an-open-work-list"></a>Süsteemi rühmitamise seadistamine avatud tööloendis
Süsteemi rühmitamise seadistamiseks avatud tööloendis tehke järgmist.

-   Valige mobiilse seadme menüüelemendist **Režiim: kaudne** ja **Tegevuse kood: kuva avatud tööloend**. Kättesaadavaks muutuvad järgmised valikud. Need valikud on vajalikud süsteemi rühmitamise jaoks avatud tööloendis. 

|        Suvand         |                                                                                                                                                                                                                                                                         Kirjeldus                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Luba süsteemi rühmitamine |                                                                                                                                                                                                                                                 Lubab süsteemi rühmitamise valitud tööloendi menüüelemendi puhul.                                                                                                                                                                                                                                                  |
| Süsteemi rühmitusväli | Saadaval ainult juhul, kui valiku <strong>Luba süsteemi töö</strong> olekuks on määratud <strong>Jah</strong>. Valige väli, mis määrab, kuidas komplekteerimistöö töötajate puhul rühmitatakse. Kui valite näiteks välja <strong>ShipmentId</strong>, skannib töötaja komplekteerimistöö rühmitamiseks saadetise ID. Seejärel määratakse kogu saadetisega seotud töö töötajale. Selleks peate looma menüüelemendi, et kasutada süsteemi rühmitatud olemasolevat tööd. Kasutage välja <strong>Süsteemi rühmitussilt</strong> töötaja teavitamiseks sellest, mida skannida. |
| Süsteemi rühmitussilt |                       Saadaval ainult juhul, kui valiku <strong>Luba süsteemi töö</strong> olekuks on määratud <strong>Jah</strong>. Sisestage töötaja jaoks teave selle kohta, mida skannida, kui komplekteerimistöö rühmitatakse. Kui kasutate näiteks komplekteerimistöö rühmitamiseks saadetise järgi välja <strong>ShipmentId</strong>, võib vajalik olla väljale Saadetise ID sisestamine. Selleks peate looma menüüelemendi, et kasutada süsteemi rühmitatud olemasolevat tööd. Peale selle peate valima väljal <strong>Süsteemi rühmitamine</strong> rühmitamise aluseks oleva välja.                       |


