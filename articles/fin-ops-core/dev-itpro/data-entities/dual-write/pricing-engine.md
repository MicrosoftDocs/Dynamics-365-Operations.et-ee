---
title: Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga
description: Selles teemas kirjeldatakse, kuidas kasutada Dynamics 365 Salesi Microsoft Dynamics 365 Supply Chain Managementi hinnakujunduse mootorit.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c9f94ec35ebed5a14252377fb543de09cb994ffd
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416176"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Nõudmisel sünkroonimine Supply Chain Managementi hinnakujunduse mootoriga

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management sisaldab hinnakujunduse mootorit, mis tegeleb kaubanduslepete, hinnakirjade, püsikliendi rogrammide, kampaaniate ja allahindlustega. Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks. Kui kasutate topeltkirjutust, kasutate Dynamics 365 Supply Chain Managementi staatilist hinnakujundust või hinnakujunduse mootorit Dynamics 365 Salesi hinnapakkumise ja tellimuse lehtedel.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Supply Chain Managementi hinnakujunduse mootori kasutamine Salesis

1. Avage Salesis **Müük \> Tellimused**.
2. Uue tellimuse loomiseks või olemasolema valimiseks tehke loendis **Minu tellimused** valik **Uus**.
3. Uue tellimusrea lisamine.
4. Kui loote uut tellimust, valige tegevuse paanil suvand **Hinnajärjestus**. Kui värskendate olemasolevat tellimust, valige tegevuse paanil suvand **Uuestiarvutamine**.

    Järgmised veerud täidetakse automaatselt.

    + Üksikasjalik summa
    + Allahindlus %
    + Allahindlus
    + Transpordieelne summa
    + Transpord summa
    + Kogumaks
    + Kogusumma
    
5. Et tagada, et süsteem võtab hinna arvutamisel arvesse kaubandusleppeid ja müügilepinguid, tehke järgmist.
    1. Liikuge teenuses Supply Chain Management oma keskkonna juurde.
    2. Navigeerige jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
    3. Valige külgmisel navigeerimisribal vahekaart **Hinnad**.
    4. Tühjendage kiirkaardil **Kaubandusleppe hindamine** ruut **Käsitsi sisestamine**.

## <a name="how-it-works"></a>Toimimisviis

Kui teete Salesis valiku **Hinnajärjestus**, kutsutakse seostatud müügitellimuse jaoks Supply Chain Managementi vahekaardil **Müügitellimus \> Kuva** funktsioon **Kogusummad**. Tellimuse kogusumma väärtusi kasutatakse Salesis vastavate Supply Chain Managementi veergude täitmiseks.

Kui Supply Chain Managementis avutatakse müügitellimuse kogusumma, hindab arvutus kliendi ja müügitellimuse jaoks loetletud toodete kehtivaid kaubandusleppeid ja müügilepinguid. Seda teavet kasutatakse kogusummade arvutamiseks. Kui valitud on **Hinnajärjestus**, kajastab Sales automaatselt kõiki Supply Chain Managementis tehtud seadistusi.

## <a name="limitations"></a>Kitsendused

Kui Salesi veerud on täidetud, kehtivad järgmised piirangud.

+ Supply Chain Managementi tasude ja tasu eraldamise seadistusi ei kopeerita Salesi.
+ Hinnakujundus ei arvesta Supply Chain Managementi müügitellimuse rea lehe veerus **Jaemüügi kanal** määratletud jaemüügi erihinnakujundust.
+ Supply Chain Managementi jaotises **Kaubandushüvitise haldus** määratletud allahindlusi ei arvestata.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]