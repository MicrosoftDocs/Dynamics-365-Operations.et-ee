---
title: Integreeritud hankija koondandmed
description: See artikkel kirjeldab hankija andmete integreerimist finantside ja toimingute rakenduste ning Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112190"
---
# <a name="integrated-vendor-master"></a>Integreeritud hankija koondandmed

[!include [banner](../../includes/banner.md)]



Termin *hankija* viitab tarnijariigi organisatsioonile või ainuomanikule, kes tarnib ettevõttele kaupu või teenuseid. Kuigi *müüja* on loodud mõiste teenusekomplektis Microsoft Dynamics 365 Supply Chain Management, pole teistes kliendikaasamise rakendustes mõistet müüja olemas. Kuid hankija teabe talletamiseks saate ülekoormata tabeli **Konto/kontakt**. Integreeritud müüja koondandmed tutvustavad kliendikaasamise rakendustes selgesõnalist müüja mõistet. Saate kasutada kas uut hankija kujundust või talletada hankija andmeid tabelis **Konto/kontakt**. Topeltkirjutus toetab mõlemat lähenemist.

Mõlemas lähenemisviisis on hankija andmed integreeritud Dynamics 365 Supply Chain Managementi, Dynamics 365 Salesi, Dynamics 365 Field Service'i ja Power Appsi portaalide vahel. Supply Chain Managementis on andmed saadaval töövoogudele (nt ostutaotlused ja ostutellimused).

## <a name="vendor-data-flow"></a>Hankijaandmete voog

Kui te ei soovi talletada hankija andmeid Dataverse’i tabelis **Konto/kontakt**, saate kasutada uut hankija kujundust.

![Hankijaandmete voog.](media/dual-write-vendor-data-flow.png)

Kui soovite jätkata hankija andmete talletamist tabelis **Konto/kontakt**, saate kasutada laiendatud hankija kujundust. Laiendatud hankija kujunduse kasutamiseks peate konfigureerima hankija töövood topeltkirjutuse lahendusepaketis. Lisateavet vaadake teemast [Hankija kujunduste vahel vahetamine](vendor-switch.md).

![Hankijaandmete laiendatud voog.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Kui kasutate iseteeninduse Power Apps hankijate portaale, võib hankija teave otse finantside ja toimingute rakendustesse minna.

## <a name="templates"></a>Mallid

Hankijaandmed sisaldavad kogu teavet hankija kohta (nt hankijagrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil). Tabeli kaartide kogum toimib koos hankijaandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operations rakendused | Klientide kaasamise rakendused     | Kirjeldus
----------------------------|-----------------------------|------------
[CDS-i kontaktid V2](mapping-reference.md#115) | kontaktid | See mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.
[Nime liited](mapping-reference.md#155) | msdyn_nameaffixes | See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.
[CDS V2 maksepäeva read](mapping-reference.md#157) | msdyn_paymentdaylines | See mall sünkroonib nii klientide kui ka hankijate maksepäeva ridade viiteandmed.
[CDS-i maksepäevad](mapping-reference.md#158) | msdyn_paymentdays | See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.
[Maksegraafiku read](mapping-reference.md#159) | msdyn_paymentschedulelines | Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed.
[Maksegraafik](mapping-reference.md#160) | msdyn_paymentschedules | See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.
[Maksetingimused](mapping-reference.md#161) | msdyn_paymentterms | See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.
[Hankijad V2](mapping-reference.md#202) | msdyn_vendors | Ettevõtted, mis kasutavad hankijatele Dataverse kohandatud lahendust, saavad kasutada finance ja toimingute rakenduste integreerimise tõttu juurutatav hankija kontseptsiooni.
[Hankijagrupid](mapping-reference.md#200) | msdyn_vendorgroups | See mall sünkroonib hankijagrupi teabe.
[Tarnija makseviis](mapping-reference.md#201) | msdyn_vendorpaymentmethods | See mall sünkroonib hankija makseviisi teabe.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

