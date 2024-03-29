---
title: Ülevaade integratsioonist rakendusega Microsoft Dynamics 365 Field Service
description: See artikkel annab ülevaate integratsioonist Microsoft Dynamics 365 Field Service.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 12a9c57e2587150914c6087c041d63af9783c1f3
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103693"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Ülevaade integratsioonist rakendusega Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]



Tarneahela juhtimine võimaldab äriprotsesside sünkrooniminst rakenduste Dynamics 365 Supply Chain Management ja Dynamics 365 Field Service vahel. Integreerimisstsenaariume konfigureeritakse lubama äriprotsesside sünkroonimist laiendatavates andmeintegraatori mallides ja teenuses Microsoft Dataverse.
Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisaveerge ja tabeleid saab integratsiooni korrigeerimiseks ja konkreetsete ärivajadustega kooskõlla viimiseks vastendada. 

Välja teenuse integreerimine rajaneb olemasoleva potentsiaalse kliendi funktsioonil.

![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/field-service-integration.png)

Rakenduste Field Service ja Supply Chain Management integreerimise esimeses faasis keskendutakse rakenduse Field Service töötellimuste ja lepingute arveldamise lubamisele rakenduses Supply Chain Management. Toetatud voog algab rakenduses Field Service, kus töötellimuste teave sünkroonitakse müügitellimustena rakendusse Supply Chain Management. Rakenduses Supply Chain Management arveldatakse müügitellimused arve dokumentide loomiseks. Lisaks sünkroonitakse rakenduse Field Service lepingu arvete teave rakendusse Supply Chain Management. Microsoft Dynamics 365 andmeintegraator sünkroonib andmed kohandatavate projektide abil. Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisaveerge, samuti tabeleid saab integratsiooni korrigeerimiseks ja konkreetsete nõuetega kooskõlla viimiseks vastendada.

Rakenduste Field Service ja Supply Chain Management integratsiooni esimeses faasis võimaldatakse sünkroonida järgmisi kaupu.

- [Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega](field-service-product.md)
- [Sünkroonige rakenduse Field Service töötellimused rakenduse Supply Chain Management müügitellimustega](field-service-work-order.md)
- [Sünkroonige leppe arved rakenduses Field Service vabas vormis arveteks rakenduses Supply Chain Management](field-service-invoice.md)

Näite saamiseks, kuidas sünkroonida töökäsk Field Service’i ja Supply Chain Managementi vahel, vaadake YouTube’i lühivideot [Töökäsu sünkroonimine rakenduse Microsoft Dynamics 365 integratsiooniga](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integratsioon rakendusega Field Service, sh arvatud varude ja projekti teave

Lisafunktsioon selles teises etapis on suunatud väljatehnikutele ülevaate andmiseks laoinfo kohta rakendusest Supply Chain Management, võimaldades neil laovarude tasemeid uuendada ja teha materjali ülekanded. Lisaks saavad installimise või müüdud kaupade hooldamisega tegelevad firmad kasu paremast ülevaatest ja kogu müügi ja teenuse protsessi nähtavusesti koos integratsiooniprojektidega.

### <a name="functionality-includes-integration-of"></a>Funktsionaalsus sisaldab integratsiooni nende vahel:
- Laoteave
- Kaubavaru tegelik teave
- Varude ülekanded
- Varude reguleerimine
- Töötellimustega seotud Dynamics 365 Field Service rakenduse Supply Chain Management projektid
- Dynamics 365 Field Service’i töökäsud lingiga Supply Chain Managementi projektidele rakendavad selle projekti numbri müügitellimusele, et lubada projektist arveldamine. 

![Supply Chain Management ja Field Service vaheliste äriprotsesside sünkroonimine, sealhulgas varude ja projekti teave.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Rakenduste Field Service ja Supply Chain Management integratsiooni teises faasis võimaldatakse sünkroonida järgmisi malle:
- Laod (rakendus Supply Chain Management rakendusele Field Service) – laod rakendusest Supply Chain Management rakendusse Field Service [Täpsem päring] 
- Tootevarud (rakendus Supply Chain Management rakendusele Field Service) – varude taseme teave rakendusest Supply Chain Management rakendusse Field Service [Täpsem päring] 
- Lao korrigeerimine (rakendus Field Service rakendusele Supply Chain Management) – lao korrigeerimised rakendusest Field Service rakendusse Supply Chain Management [Täpsem päring] 
- Varude ülekanded (rakendus Field Service rakendusele Supply Chain Management) – varude ülekanded rakendusest Field Service rakendusse Supply Chain Management [Täpsem päring] 
- Projektid (rakendus Supply Chain Management rakendusele Field Service) – projektiloend rakendusest Supply Chain Management rakendusse Field Service 
- Projekti töötellimused (rakendus Field Service rakendusele Supply Chain Management) – töötellimused rakenduses Field Service müügitellimuste kohta rakenduses Supply Chain Management, koos projektitoega [täpsem päring] 
- Rakenduse Field Service tooted laoühikuga (Supply Chain Management müügile) – rakenduse Supply Chain Management „Müüdavad väljastatud tooted” müügile „Tooted” rakenduse Field Service jaoks, sh laoühikud 

## <a name="system-requirements"></a>Süsteeminõuded

### <a name="system-requirements-for-supply-chain-management"></a>Süsteemi nõuded rakendusele Supply Chain Management
Rakenduse Field Service integratsioon toetab järgmisi versioone.

- Dynamics 365 Finantside ja toimingute versioon 8.1.2 (2018. a detsember 2018) vabastati detsembris 2018 ja selle rakenduse järgu number on 8.1.195 platvormi värskendusega 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Rakenduse Field Service süsteeminõuded
Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.

- Rakendus Field Service (versioon 8.2.0.286) või uuem rakenduses Dynamics 365 9.1.x – väljastati novembris 2018
- Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Rakenduse Field Service integreerimis-, projekti- ja laoseisulahendus Dynamics 365 jaoks, versioon 2.0.0.0 või hilisem versioon. Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
