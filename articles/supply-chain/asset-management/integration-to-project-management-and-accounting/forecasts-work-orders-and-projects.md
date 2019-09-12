---
title: Ennustused, töökäsud ja projektid
description: Selles teemas kirjeldatakse ennustuste ja töökäsu integratsiooni projekti halduse ja varahalduse raamatupidamismooduliga.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886812"
---
# <a name="forecasts-work-orders-and-projects"></a>Ennustused, töökäsud ja projektid

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varahalduses integreeritakse mooduliga **Projekti haldus ja raamatupidamine**, et optimeerida kulu, võimaldades kasutajatel jälgida hooldustöö tüübi ennustuste ja töökäsu tööde kulusid.

Hooldustöö tüübi ennustuste jälgimiseks peab seadistama kahte seadet:

1. valige projekt kohas **Varahaldus** > **Seadistus** > **Varahalduse näitajad** > **Varad** link > **Projekt** FastTab > asuvas väljas **Hoolduse ennustamisprojekt**;

2. hooldustöö tüübi tavarea loomisel luuakse valikus **Hooldustöö tavatüübid** rea tegevuse number automaatselt (**Varahaldus** > **Seadistus** > **Tööd** > **Hooldustöö tavatüübid**).

Hooldustöö tüübi ennustamisel on kaks eesmärki: saate jälgida hooldustöö tüübi ennustuste kulusid moodulis **Projekti haldus ja raamatupidamine**. Lisaks edastatakse ennustused automaatselt töökäsu töö projekti, kui valite töökäsu töö hooldustöö tüübi.

Töökäsu tööde kulud jälgimiseks peate esmalt seadistama töökäsu projektid. Tegevuse kirjeldust vt jaotisest [Töökäsu projekti seadistamine](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Töökäsu töö projektid

Kui loote töökäsu töö, määratakse töökäsu projekt töökäskude ülemprojekti seadistamisega kohas **Varahaldus** > **Seadistamine** > **Töökäsud** > **Projekti seadistamine**.

Töökäsu töö projekte luuakse järgmise töökäsu teabe kombinatsiooni alusel:

- töökäsus valitud tüüp; 
- töökäsu varaga seotud töö asukoht;
- töökäsu varaga seotud vara tüüp;  
- töökäsu eeldatav algus- ja lõpuaeg.  

Võimalik, et töökäsus pole kogu allpool nimetatud teavet. Seega otsitakse töökäsu ülemprojekti saadaval andmete kombinatsiooni alusel ja valides projekti ID, mis vastab töökäsu andmetele.

Näide: alumises joonises tähendab vara tüübi „Sõiduki mootor“ seadistus seda, et iga selle vara tüübiga loodud töökäsu töö on projekti ID „000186“ alamprojekt.

![Joonis 1](media/01-integration-to-pma.png)

Töökäsu töö projekti ID ja asjakohase tegevuse numbri (**Vara haldus** > **Ühine** > **Töökäsud** > **Kõik töökäsud** > valige loendist töökäsk > **Rea andmed** FastTab > väli **Projekti ID** ja väli **Tegevuse number**) eesmärk on jälgida moodul **Projekti haldus ja raamatupidamine** töökäsu tööga seotud kulutusi ja töökäsu töös valitud vara. 

Alumisel joonisel näete töökäsu projektide ja asjakohaste projektide toimingute graafilist ülevaadet.

![Joonis 2](media/02-integration-to-pma.png)

Kui töökäsus luuakse uus töö, luuakse selle jaoks automaatselt projekt. Töökäsu tööga seotud vara finantsdimensioonid edastatakse automaatselt töökäsu projekti. Töökäsu töö jaoks loodud projekti aktiivsuses on manustatud asjakohane teave hooldustöö tüübi, selle variandi ja müügi kohta. Nendest andmetest on kasu näiteks töökäsu ostutellimuse loomisel (vt [Hankimine](../work-orders/procurement.md)) või mooduli **Projekti haldus ja raamatupidamine** kasutamisel aja registreerimiseks.  

Kui vara paigaldati töö asukohta ja see vara paigaldatakse hiljem teise töö asukohta, värskendatakse automaatselt uue töö asukohaga seotud vara finantsilisi dimensioone Hiljem, kui loote vara töökäsu töö, saab töökäsu töö projekt automaatselt nüüd varaga seotud finantsilised dimensioonid. See tähendab seda, et kui kasutate töö asukohti, saab alati jälgida töö asukohtade, kuhu vara paigaldati mistahes ajal, kulusid. Finantsiliste dimensioonide automaatne värskendamine tagab kulude põhjaliku jälgitavuse projekti haldamise ja aruandluse jaoks.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Töökäsu projektid, töökäsu tsükli olekud, projekti etapid ja projekti tüübid

Töökäsu tsükli olekute ja töökäskude asjakohase projekti etappide õige kasutamise tagamiseks pidage silmas sõltuvusi vastavalt moodulile **Projekti haldus ja raamatupidamine**:

- Mooduli **Projekti haldus ja raamatupidamine** projekti etapid on seadistatud valiku **Projekti haldus ja raamatupidamise näitajad** projekti tüüpidega.  
- Pidage meeles, et valite moodulis **Projekti haldus ja raamatupidamine** kõikide kasutatavate projekti tüüpide asjakohase projekti etapi märkeruudud. Alumises joonises on valitud projekti tüüpide „Aeg ja materjal“ ja „Sisemine“ viis etappi: **Loodud** - **Hinnatud** - **Ajastatud** - **Pooleli** - **Valmis**. Need viis etappi on vajalikud nii sisemise hoolduse kui ka teenuse hoolduse töödele.  
- Valikus **Varahaldus** määratletakse projekti tüüpe projekti rühmade seadistate neid ankeedi **Töökäsu projekti seadistus** > lingi **Projekti rühm** järgi.  
- Valiku **Töökäsu projekti seadistus** projekti rühmade seadistust kasutatakse, uute töökäskude loomisel. Kui luuakse töökäsk, koostatakse selle jaoks automaatselt projekt.  
- Töökäsu tsükli kõikidel olekutel peab olema asjakohane projekti etapp.  
- Töötsükli olekuga seotud projekti etapp peab olema rühma aktiivne etapp. Töökäsu projekt koostatakse automaatselt.  
- Kui loote uute töökäsu, põhineb töökäsu projekti automaatne eraldus valiku **Töökäsu projekti seadistamine** (**Varahaldus** > **Seadistamine** > **Töökäsud** > **Projekti seadistamine**).  

Töökäsu projekti rühmade, asjakohaste projekti tüüpide, projekti etappide ja töökäsu tsükli olekute omavahelised seosed on kujutatud alumistes joonistes.  

![Joonis 3](media/03-integration-to-pma.png)

![Joonis 4](media/04-integration-to-pma.png)

![Joonis 5](media/05-integration-to-pma.png)

Töökäsu projektide seadistamiseks vt [Töökäsu projekti seadistamine](../setup-for-work-orders/work-order-project-setup.md) ja töökäsu tsükli olekuid vt [Töökäsu tsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).

Alumine joonis näitab moodulis **Varahaldus** loodud (et võimaldada integratsiooni mooduliga **Projekti haldus ja raamatupidamine**) erinevate projektid graafilist ülevaadet ja ka projektidega seotud töö toiminguid.

![Joonis 6](media/06-integration-to-pma.png)

