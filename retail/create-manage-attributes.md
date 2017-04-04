---
title: Atribuutide loomine ja haldamine
description: "Selles artiklis kirjeldatakse Microsoft Dynamics 365 toimingute atribuudid. Atribuudid võimaldavad teil kasutaja määratletud väljade kaudu toodet ja selle omadusi kirjeldada."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16461
ms.assetid: 2b85491c-f830-4e79-a2cb-681b7ced6988
ms.search.region: global
ms.search.industry: Retail
ms.author: prabhup
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 26c628e10aaa5f47bc87d7510ca8f41ab3630204
ms.lasthandoff: 03/31/2017


---

# <a name="create-and-manage-attributes"></a>Atribuutide loomine ja haldamine

Selles artiklis kirjeldatakse Microsoft Dynamics 365 toimingute atribuudid. Atribuudid võimaldavad teil kasutaja määratletud väljade kaudu toodet ja selle omadusi kirjeldada.

Atribuudid võimaldavad teil kasutaja määratletud väljade kaudu toodet ja selle omadusi kirjeldada. Näiteks saate määrata toote mälu suuruse ja kõvaketta võimsuse ning näidata, kas toode vastab energiatähisele. Atribuute saab seostada erinevate jaemüügiüksustega, nagu tootekategooriad ja jaemüügikanalid, ning neile saab määrata vaikeväärtused. Tooted pärivad nende atribuudid ja atribuutide vaikeväärtused, kui need seostatakse tootekategooriate või jaemüügikanalitega. Vaikeväärtusi saab alistada üksiku toote tasemel, jaemüügikanali tasemel või jaemüügikataloogis.

#### <a name="examples"></a>Näited

Kategooria

Atribuut

Lubatud väärtused

Vaikeväärtus

Teler ja video

Tootemark

Mis tahes kehtiv väärtus **Kaubamärk**

Puudub

Teler

Ekraani suurus

**20 tolli**–**80 tolli**

Puudub

Vertikaallahendus

**480i**, **720p**, **1080i** või **1080p**

**1080p**

Ekraani värskendussagedus

**60 Hz**, **120 Hz** või **240 Hz**

**60 Hz**

HDMI-sisendid

**0**–**10**

**3**

DVI-sisendid

**0**–**10**

**1**

Koondsisendid

**0**–**10**

**2**

Komponendi sisendid

**0**–**10**

**1**

LCD

3D-valmidus

**Jah** või **Ei**

**Jah**

3D lubatud

**Jah** või **Ei**

**Ei**

Plasma

Töötemperatuur alates

**32**–**110** kraadi

**32**

Töötemperatuur kuni

**32**–**110** kraadi

**100**

Projektsioon

Projektsioonitoru garantii

**6**, **12** või **18** kuud

**12**

\#Projektsioon torude

**1**–**5**

**3**

## <a name="attribute-type"></a>Atribuudi tüüp
  [![atribuutide kinnitatud koopia](./media/attributes-fixed-copy.png)](./media/attributes-fixed-copy.png) omadused põhinevad Atribuuditüübiga. Atribuudi tüübid tuvastavad andmete tüübi, mida saab konkreetse atribuudi jaoks sisestada. Praegu Microsoft Dynamics 365 toiminguteks toetab järgmisi:

-   **Currency** – see atribuudi tüüp toetab valuuta väärtusi. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **DateTime** – see atribuudi tüüp toetab kuupäeva ja kellaaja väärtusi. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **Decimal** – see atribuudi tüüp toetab kümnendkohti sisaldavaid arvväärtusi. See toetab ka mõõtühikuid. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **Integer** – see atribuudi tüüp toetab arvväärtusi. See toetab ka mõõtühikuid. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
-   **Text** – see atribuudi tüüp toetab tekstväärtusi. See toetab ka eelmääratletud võimalike väärtuste kogumit (loetelu).
-   **Boolean** – selle atribuudi tüüp toetab binaarväärtustele (**tõsi**/**false**).
-   **Viide**.

## <a name="attribute"></a>Atribuut
  [![createandmanageattribute-8](./media/createandmanageattribute-8.png)](./media/createandmanageattribute-8.png) nimi, lühinimi, kirjeldus ja abi teksti, Lisaks võimalik püüda ühe või mitme järgmist tüüpi teavet, atribuudi:

-   Vaikeväärtus
-   Atribuudi metaandmed, nagu metaandmed, mis näitavad, kas atribuuti saab otsida, täpsustada või sortida.

## <a name="attribute-group"></a>Atribuudigrupp
  [![createandmanageattribute-10](./media/createandmanageattribute-10.png)](./media/createandmanageattribute-10.png) pärast atribuute pole määratud, nende seas on atribuut pakuvad. Atribuudigrupid võimaldavad üksikute atribuutide rühmitamist ja neid saab määrata jaemüügikategooriatele või jaemüügikanalitele.

## <a name="assigning-attribute-groups-to-retail-categories"></a>Atribuudigruppide määramine jaemüügikategooriatele
  [![createandmanageattribute-12](./media/createandmanageattribute-12.png)](./media/createandmanageattribute-12.png) üks või mitu atribuuti rühma saab seostada kategooria sõlmed jaemüügi kategooria hierarhia. Kui tooted on kategoriseeritud, pärivad need atribuudigruppidesse kaasatud atibuudid.

## <a name="assigning-attribute-groups-to-retail-stores"></a>Atribuudigruppide määramine jaemüügikauplustele
  [![createandmanageattribute-13-1024 x 576](./media/createandmanageattribute-13-1024x576.png)](./media/createandmanageattribute-13-1024x576.png) üks või mitu atribuuti rühma saab siduda ühe või mitme jaemüük kauplustes, jaemüük kauplustes hierarhia. Kui tooted on rikastatud kindlate jamüügikaupluste jaoks, pärivad need atribuudigruppidesse kaasatud atibuudid.

## <a name="overriding-attribute-values"></a>Atribuudi väärtuste alistamine
### <a name="at-the-product-level"></a>Toote tasemel

  [![createandmanageattribute-14-1024 x 576](./media/createandmanageattribute-14-1024x576.png)](./media/createandmanageattribute-14-1024x576.png) atribuutide väärtused võib tühistada toote tasandil (st üksiktoodetele).

### <a name="in-a-retail-catalog"></a>Jaemüügikataloogis

  [![createandmanageattribute-2](./media/createandmanageattribute-2.png)](./media/createandmanageattribute-2.png) atribuutide väärtused võib tühistada üksiktoodetele teatud kataloogid, mis on suunatud konkreetseid kanaleid.

### <a name="at-the-retail-channel-level"></a>Jaemüügikanali tasemel

  [![createandmanageattribute-1](./media/createandmanageattribute-1.jpg)](./media/createandmanageattribute-1.jpg) atribuutide väärtused võib tühistada üksiktoodetele teatud kataloogid, mis on suunatud konkreetseid kanaleid.


