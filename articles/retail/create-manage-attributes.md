---
title: Atribuutide loomine ja haldamine
description: "Selles artiklis kirjeldatakse Microsoft Dynamics 365 for Retaili atribuute. Atribuudid võimaldavad teil kasutaja määratletud väljade kaudu toodet ja selle omadusi kirjeldada."
author: pdp1207
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a98527d37040dfcc0e57b74d590802e8aa2cb0b6
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="create-and-manage-attributes"></a>Atribuutide loomine ja haldamine

[!include[banner](includes/banner.md)]


Selles artiklis kirjeldatakse Microsoft Dynamics 365 for Retaili atribuute. Atribuudid võimaldavad teil kasutaja määratletud väljade kaudu toodet ja selle omadusi kirjeldada.

Atribuudid võimaldavad teil kasutaja määratletud väljade kaudu toodet ja selle omadusi kirjeldada. Näiteks saate määrata toote mälu suuruse ja kõvaketta võimsuse ning näidata, kas toode vastab energiatähisele. Atribuute saab seostada erinevate jaemüügiüksustega, nagu tootekategooriad ja jaemüügikanalid, ning neile saab määrata vaikeväärtused. Tooted pärivad nende atribuudid ja atribuutide vaikeväärtused, kui need seostatakse tootekategooriate või jaemüügikanalitega. Vaikeväärtusi saab alistada üksiku toote tasemel, jaemüügikanali tasemel või jaemüügikataloogis.

#### <a name="examples"></a>Näited

| Kategooria   | Atribuut                | Lubatud väärtused          | Vaikeväärtus |
|------------|--------------------------|-----------------------------|---------------|
| Teler ja video | Tootemark                    | Mis tahes kehtiv väärtus Kaubamärk       | Puudub          |
| Teler         | Ekraani suurus              | 20″–80″                     | Puudub          |
| Teler         | Vertikaallahendus      | 480i, 720p, 1080i või 1080p | 1080p         |
| Teler         | Ekraani värskendussagedus      | 60 Hz, 120 Hz või 240 Hz       | 60 Hz          |
| Teler         | HDMI-sisendid              | 0–10                        | 3             |
| Teler         | DVI-sisendid               | 0–10                        | 1             |
| Teler         | Koondsisendid         | 0–10                        | 2             |
| Teler         | Komponendi sisendid         | 0–10                        | 1             |
| LCD        | 3D-valmidus                 | Jah või Ei                   | Jah           |
| LCD        | 3D lubatud               | Jah või Ei                   | Ei            |
| Plasma     | Töötemperatuur alates      | 32–110 kraadi              | 32            |
| Plasma     | Töötemperatuur kuni        | 32–110 kraadi              | 100           |
| Projektsioon | Projektsioonitoru garantii | 6, 12 või 18 kuud         | 12            |
| Projektsioon | # projektsioonitoru    | 1–5                         | 3             |


## <a name="attribute-type"></a>Atribuudi tüüp
  [![attributes-fixed-copy](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) 
  
Atribuudid põhinevad atribuuditüüpidel. Atribuudi tüübid tuvastavad andmete tüübi, mida saab konkreetse atribuudi jaoks sisestada. Praegu toetab Microsoft Dynamics 365 for Retail järgmisi atribuuditüüpe.

-   **Currency** – see atribuudi tüüp toetab valuuta väärtusi. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **DateTime** – see atribuudi tüüp toetab kuupäeva ja kellaaja väärtusi. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **Decimal** – see atribuudi tüüp toetab kümnendkohti sisaldavaid arvväärtusi. See toetab ka mõõtühikuid. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **Integer** – see atribuudi tüüp toetab arvväärtusi. See toetab ka mõõtühikuid. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **Text** – see atribuudi tüüp toetab tekstväärtusi. See toetab ka eelmääratletud võimalike väärtuste kogumit (loetelu).
-   **Kahendmuutuja** – see atribuuditüüp toetab binaarseid väärtusi (**tõene**/**väär**).
-   **Viide**.

## <a name="attribute"></a>Atribuut
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) Lisaks nimele, sõbralikule nimele, kirjeldusele ja spikritekstile saab atribuudi jaoks jäädvustada ka järgmist tüüpi teavet.

-   Vaikeväärtus
-   Atribuudi metaandmed, nagu metaandmed, mis näitavad, kas atribuuti saab otsida, täpsustada või sortida.

## <a name="attribute-group"></a>Atribuudigrupp
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) Pärast atribuutide määratlemist saab need rühmitada atribuudigruppidesse. Atribuudigrupid võimaldavad üksikute atribuutide rühmitamist ja neid saab määrata jaemüügikategooriatele või jaemüügikanalitele.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Atribuudigruppide määramine jaemüügikategooriatele
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) Jaemüügi tootekategooria hierarhia kategooriasõlmedega saab seostada ühe või mitu atribuudigruppi. Kui tooted on kategoriseeritud, pärivad need atribuudigruppidesse kaasatud atibuudid.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Atribuudigruppide määramine jaemüügikauplustele
  [![createandmanageattribute-13-1024x576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) Jaemüügikaupluste hierarhia ühe või mitme jaemüügikauplusega saab seostada ühe või mitu atribuudigruppi. Kui tooted on rikastatud kindlate jamüügikaupluste jaoks, pärivad need atribuudigruppidesse kaasatud atibuudid.

## <a name="overriding-attribute-values"></a>Atribuudi väärtuste alistamine
### <a name="at-the-product-level"></a>Toote tasemel

  [![createandmanageattribute-14-1024x576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) Atribuutide vaikeväärtused saab toote tasemel (st üksikute toodete puhul) alistada.

### <a name="in-a-retail-catalog"></a>Jaemüügikataloogis

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) Atribuutide vaikeväärtused saab kindlatele jaemüügikanalitele sihitud kindlates kataloogides olevate üksikute toodete puhul alistada.

### <a name="at-the-retail-channel-level"></a>Jaemüügikanali tasemel

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) Atribuutide vaikeväärtused saab kindlatele jaemüügikanalitele sihitud kindlates kataloogides olevate üksikute toodete puhul alistada.




