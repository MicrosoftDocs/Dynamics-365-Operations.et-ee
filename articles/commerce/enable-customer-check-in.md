---
title: Luba kliendi sisseregistreerimise teatised kassas (POS)
description: See teema kirjeldab, kuidas lubada kliendi sisseregistreerimise teatisi Microsoft Dynamics 365 Commerce kassas (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271421"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Luba kliendi sisseregistreerimise teatised kassas (POS)

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lubada kliendi sisseregistreerimise teatisi Microsoft Dynamics 365 Commerce kassas (POS).

Oma "komplekt kasutamiseks valmis olevas tellimuses" võivad organisatsioonid anda lingi või nupu, mis lubab klientidel teavitada kauplust, et nad on valdustes ja ootavad oma paketi välja tuua. Kliendid saavad seejärel sisseregistreerimise kinnituse ja kauplus saab kassarakenduses ülesandena teatise. See ülesanne on viip müügipartnerile tellimuse tarnimiseks kliendi sõidukisse. Seetõttu ei pea klient kauplust sisestama.

Kliendi sisseregistreerimise töövoogu saab konfigureerida ka klientidelt lisateabe kogumiseks, nt klientide parkimise punktinumber, sõiduki tootja, mudel ja värv ning tarnejuhised. Kaupluse töötaja saab seda teavet tellimuse täitmise hõlbustamiseks kasutada.

## <a name="enable-customer-check-in"></a>Kliendi sisseregistreerimise lubamine

Kui kliendi sisseregistreerimise funktsioon on sisse lülitatud, loob Commerce tellimuse kinnituse ID (tuntud ka kui kanaliviite ID). Samuti loob see tellimuse kinnitus ID-d tellimustele, mis luuakse kassa (POS) või kõnekeskuse kanalite kaudu. 

Kliendi sisseregistreerimise funktsiooni sisselülitamiseks Commerce'i peakontoris toimige järgmiselt.

1. Avage **Tööruumid \> Funktsioonihaldus**.
2. Otsige kanali funktsiooni **Ühtse kanaliviite ID-vormingu loomine üle kanalite**. 
3. Valige funktsioon ja seejärel valige atribuutide paanil nupp **Luba kohe**. 

## <a name="create-a-check-in-confirmation-page"></a>Sisseregistreerimise kinnituslehe loomine

Oma e-kaubanduse saidil peate looma uue lehekülje, mis toimib sisseregistreerimise kinnituse kogemusena. Täiendava konfiguratsiooni abil võib leht sisaldada ka vormi, mis kogub klientidelt tellimuse täitmise hõlbustamiseks täiendavat teavet. Teavet selle kohta, kuidas seadistada lehekülge ja moodulit, vt [kliendi sisseregistreerimise moodulit](check-in-pickup-module.md).

## <a name="configure-the-transactional-email-template"></a>Kande meilimalli konfigureerimine

Peate lisama siia lingi **Olen siin** või nupu mallile kandemeilide jaoks, mille kliendid saavad, kui nende tellimus on valmis peale võtma. Kliendid kasutavad seda linki või nuppu, et teavitada kauplust, et nad on saabunud tellimust kätte saama. 

Lisage mallile link või nupp, mis on vastendatud **lõpuleviidud pakkimise** teatise tüübiga ja tarneviisiga, mida kasutate tellimuse täitmise curbside'i täitmiseks. Looge mallis HTML-link või nupp, mis viitab teie loodud sisseregistreerimise kinnituslehe URL-ile. Siin on näide.

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
Lisateavet e-kirjade mallide konfigureerimise kohta vt [Kande e-kirjade kohandamine tarneviisi alusel](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Kassas luuakse sisseregistreerimise kinnitusülesanne

Pärast seda, kui klient teavitab kauplust, et nad on vastuvõtmiseks kohal, saavad nad sisseregistreerimise kinnituse teatise ja ülesanne luuakse müügikoha ülesannete loendis kaupluses, kus klient tellimuse peale võtab. Ülesanne sisaldab kogu kliendi ja tellimuse teavet, mis on tellimuse täitmiseks vajalik. Ülesandes näitab juhiste väli kogu teavet, mis koguti kliendilt täiendava teabe vormi kaudu. 

## <a name="additional-resources"></a>Lisaressursid

[Pealevõtmismooduli sisseregistreerimine](check-in-pickup-module.md)
