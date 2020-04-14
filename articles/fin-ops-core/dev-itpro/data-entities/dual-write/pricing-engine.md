---
title: Nõudmisel sünkroonimine Dynamics 365 Supply Chain Managementi hinnakujunduse mootoriga
description: Selles teemas kirjeldatakse, kuidas kasutada Dynamics 365 Salesi Microsoft Dynamics 365 Supply Chain Managementi hinnakujunduse mootorit.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173173"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Nõudmisel sünkroonimine Dynamics 365 Supply Chain Managementi hinnakujunduse mootoriga

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management sisaldab hinnakujunduse mootorit, mis tegeleb kaubanduslepete, hinnakirjade, püsikliendi rogrammide, kampaaniate ja allahindlustega. Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks. Kui kasutate topeltkirjutust, kasutate Dynamics 365 Supply Chain Managementi staatilist hinnakujundust või hinnakujunduse mootorit Dynamics 365 Salesi hinnapakkumise ja tellimuse lehtedel.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Supply Chain Managementi hinnakujunduse mootori kasutamine Salesis

1. Avage Salesis **Müük \> Tellimused**.
2. Uue tellimuse loomiseks või olemasolema valimiseks tehke loendis **Minu tellimused** valik **Uus**.
3. Uue tellimusrea lisamine.
4. Kui loote uut tellimust, valige tegevuse paanil suvand **Hinnajärjestus**. Kui värskendate olemasolevat tellimust, valige tegevuse paanil suvand **Uuestiarvutamine**.

    Järgmised väljad täidetakse automaatselt.

    + Üksikasjalik summa
    + Allahindlus %
    + Allahindlus
    + Transpordieelne summa
    + Transpord summa
    + Kogumaks
    + Kogusumma

## <a name="how-it-works"></a>Toimimisviis

Kui teete Salesis valiku **Hinnajärjestus**, kutsutakse seostatud müügitellimuse jaoks Supply Chain Managementi vahekaardil **Müügitellimus \> Kuva** funktsioon **Kogusummad**. Tellimuse kogusumma väärtusi kasutatakse Salesis vastavate Supply Chain Managementi väljade täitmiseks.

Kui Supply Chain Managementis avutatakse müügitellimuse kogusumma, hindab arvutus kliendi ja müügitellimuse jaoks loetletud toodete kehtivaid kaubandusleppeid ja müügilepinguid. Seda teavet kasutatakse kogusummade arvutamiseks. Kui valitud on **Hinnajärjestus**, kajastab Sales automaatselt kõiki Supply Chain Managementis tehtud seadistusi.

## <a name="limitations"></a>Kitsendused

Kui Salesi väljad on täidetud, kehtivad järgmised piirangud.

+ Supply Chain Managementi tasude ja tasu eraldamise seadistusi ei kopeerita Salesi.
+ Hinnakujundus ei arvesta Supply Chain Managementi müügitellimuse rea lehe väljal **Jaemüügi kanal** määratletud jaemüügi erihinnakujundust.
+ Supply Chain Managementi jaotises **Kaubandushüvitise haldus** määratletud allahindlusi ei arvestata.
