---
title: Kanalite ülevaade
description: Selles artiklis antakse ülevaade kanalitest Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.assetid: ''
ms.openlocfilehash: ad31f466563aeb38f28f9761828e6708895005b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280416"
---
# <a name="channels-overview"></a>Kanalite ülevaade


[!include [banner](includes/banner.md)]

Selles artiklis antakse ülevaade kanalitest Microsoft Dynamics 365 Commerce. See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast iga kanali seadistamist.

## <a name="types-of-channels"></a>Kanalite tüübid

Dynamics 365 Commerce toetab kolme erinevat kanali tüüpi: jae-, kõnekeskuse- ja veebikanalid.

### <a name="retail-channels"></a>Jaemüügikanalid

Jaemüügi kanalid tähistavad standardseid füüsilisi kauplusi. Igal kauplusel võivad olla kassaregistrid, tulu- ja kulukontod ning personal. 

### <a name="call-center-channels"></a>Kõnekeskuse kanalid

Kõnekeskuse kanalid esindavad kõnekeskuse tellimuste ja klientide haldust.

### <a name="online-channels"></a>Võrgukanalid

Veebikanalid esindavad e-kaubanduse poode. Kui veebikanal on loodud, tuleb luua Microsoft Dynamics 365 Commerce'i saidiehitustööriista või kolmanda osapoole e-kaubanduse lahenduse abil sait.

## <a name="channel-setup-basics"></a>Kanali seadistuse põhitõed

Kanali seadistus teostatakse tööriistas Commerce. Igal kanalil võivad olla oma makseviisid, hinnagrupid, toote hierarhiad, sortimendid ja toodete kogumid. Kui olete kanali loonud, saate määrata seal müüdavad tooted. Igal kanali tüübil on ainulaadne funktsioonide kogum, mida võib olla vajalik konfigureerida. Näiteks vajab jaemüügi kanal määratud töötajaid, registreid ja kliente. Kui uus kanal on loodud, tuleb see määrata organisatsiooni hierarhiale.

## <a name="channel-setup-prerequisites"></a>Kanali seadistamise eeltingimused

Enne kanali seadistamist peate täitma mõned eeltingimuseks olevad ülesanded, mis põhinevad kanali tüübil. Lisateavet vaadake jaotisest [Kanali seadistuse eeltingimused](channels-prerequisites.md).

## <a name="set-up-a-channel"></a>Kanali seadistamine

Pärast eeltingimuseks olevate ülesannete täitmist kasutage järgmisi linke edasiste seadistamise juhiste saamiseks.

- [Jaemüügikanali seadistamine](channel-setup-retail.md)
- [Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)
- [Veebikanali häälestamine](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>Lisaressursid

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)
    
[Veebikanali häälestamine](channel-setup-online.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)

[Organisatsiooni hierarhiate seadistamine](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
