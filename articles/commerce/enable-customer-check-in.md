---
title: Luba kliendi sisseregistreerimise teatised kassas (POS)
description: See artikkel kirjeldab, kuidas lubada kliendi sisseregistreerimise teatisi Microsoft Dynamics 365 Commerce kassas.
author: bicyclingfool
ms.date: 12/03/2021
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
ms.openlocfilehash: ae53657c95128eae793f670bd9dbc31d9fac0fe4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885141"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a>Luba kliendi sisseregistreerimise teatised kassas (POS)

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lubada kliendi sisseregistreerimise teatisi Microsoft Dynamics 365 Commerce kassas.

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

Lisage mallile link või nupp, mis on vastendatud **lõpuleviidud pakkimise** teatise tüübiga ja tarneviisiga, mida kasutate tellimuse täitmise curbside'i täitmiseks. Mallis looge HTML-link või nupp, mis osutab teie loodud sisseregistreerimise kinnituslehe URL-ile ja mis sisaldab parameetrite nimesid ja väärtusi, nagu näidatud järgmises näites.

`<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%confirmationid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>`

Lisateavet e-kirjade mallide konfigureerimise kohta vt [Kande e-kirjade kohandamine tarneviisi alusel](customize-email-delivery-mode.md). 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a>Kassas luuakse sisseregistreerimise kinnitusülesanne

Pärast seda, kui klient teavitab kauplust, et nad on kättesaamiseks olemas, näitab sisseregistreerimise leht kinnitusteadet ja valikulist QR-koodi, mis sisaldab kliendi tellimuse kinnituse ID-d. Samal ajal luuakse ülesanne kassa ülesannete loendis kaupluse jaoks, kus klient tellimuse peale võtab. See ülesanne sisaldab kogu kliendi ja tellimuse teavet, mis on tellimuse täitmiseks vajalik. Ülesande juhiste väljal kuvatakse kogu teave, mis koguti kliendilt täiendava teabe vormi kaudu.

## <a name="end-to-end-testing"></a>Lõpp-lõpu testimine

Kliendi sisseregistreerimine nõuab kindlate parameetrite ja väärtuste saatmist sisseregistreerimise lehele ja seejärel kliendi sisseregistreerimise API-sse. Seega on hõlpsaim lähenemine katsetada oma funktsiooni keskkonnas, kus katsejärjekorra saab luua ja pakkida. Sel viisil saab luua e-kirja "komplekt kasutamiseks valmis tellimus", kus on URL, mis sisaldab parameetrite nõutavaid nimesid ja väärtusi.

Kliendi sisseregistreerimise funktsiooni testimiseks järgige neid samme.

1. Looge kliendi sisseregistreerimise leht ning seejärel lisage ja konfigureerige kliendi sisseregistreerimise moodul. Lisateabe saamiseks vt sisseregistreerimise [moodulit](check-in-pickup-module.md). 
1. Kontrollige lehte, kuid ärge avaldage seda.
1. Lisage meilimallile järgmine link, mille kutsus kättetoimetamisviisi pakkimise täieliku teatise tüüp. Lisateavet vt teemast Meilimallide [loomine kandesündmuste jaoks](email-templates-transactions.md).

    - **Tootmiseelsetele (UAT) keskkondadele:**[lisage koodilõigud jaotisest Selles artiklis varasema kande meilimalli](#configure-the-transactional-email-template) konfigureerimine.
    - **Tootmiskeskkondadele:** lisage järgmine kommenteeritud kood, et olemasolevaid kliente ei mõjutata.

        `<!-- https://[DOMAIN]/[CHECK_IN_PAGE]?channelReferenceId=%confirmationid%&channelId=%pickupchannelid%&packingSlipId=%packingslipid%&preview=inprogress -->`

1. Saate luua tellimuse, mille puhul on määratud peale selle tarneviis.
1. Kui saate pakkimise täieliku teatise tüübi käivitatud meili, testige sisseregistreerimise voogu, avades sisseregistreerimise lehe, kus on varem lisatud URL. Kuna URL sisaldab lippu `&preview=inprogress`, palutakse teil enne lehe vaatamist autentida.
1. Sisestage kogu lisateave, mis on mooduli konfigureerimiseks vajalik.
1. Kontrollige, kas sisseregistreerimise kinnitusvaade on õigesti kuvatud.
1. Avage kaupluse müügikoha terminal, kuhu tellimus peale võtta.
1. Valige paani **peale võtta tellimused** ja veenduge, et tellimus ilmub.
1. Kontrollige, kas üksikasjapaanil kuvatakse kõik lisateavet, mis on konfigureeritud sisseregistreerimise moodulis.

Pärast seda, kui olete kontrollinud, et kliendi sisseregistreerimise funktsioon töötab lõpust lõpuni, järgige neid samme.

1. Avaldage sisseregistreerimisleht.
1. Kui testite tootmiskeskkonnas, tühistage URL e-kirja mallis "Komplekt kasutamiseks valmis tellimus", **et** kuvataks link või nupp. Seejärel laadige mall uuesti.

## <a name="additional-resources"></a>Lisaressursid

[Pealevõtmismooduli sisseregistreerimine](check-in-pickup-module.md)

[Kandemeilide kohandamine tarneviisi järgi](customize-email-delivery-mode.md)

[Meilimallide loomine kandesündmuste jaoks](email-templates-transactions.md)
