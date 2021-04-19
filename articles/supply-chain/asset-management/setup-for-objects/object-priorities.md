---
title: Valige teenindustase.
description: Selles teemas selgitatakse vara teenindustasemeid varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4163d059fda4ae0120d5c989e744c5a5fe0f5892
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808282"
---
# <a name="asset-service-levels"></a>Valige teenindustase.

[!include [banner](../../includes/banner.md)]

 

Selles teemas selgitatakse vara teenindustasemeid varahalduses. Vara teenindustasemed on seotud varadega ja need kantakse üle hooldustaotlustele ja töökäskudele. Neid kasutatakse töökäskude prioriteedi arvutamiseks töökäsu planeerimisel. Vara teenindustasemeid saab vajaduse korral muuta.

Lisateabe saamiseks häälestuse kohta, mis on seotud töötellimuse planeerimisel reitingusummade arvutamisega, vt teemat [Varahalduse parameetrid](../setup-for-objects/enterprise-asset-management-parameters.md). Peate seadistama vähemalt ühe vaikekirje vara teenindustaseme jaoks. Seda vaikekirjet kasutatakse juhul, kui töökäsu planeerimisel ei leita muud vastet.

**Näide 1:** vaikimisi teenindustase, mida kasutatakse, kui ühtegi muud vastet ei leita. Selles kirjes saate valida ainult teenuse taseme.

**Näide 2:** kõrge teenindustase, mida kasutatakse Volvo veoauto mootori tööde planeerimiseks. Selles kirjes saate valida vastava vara tüübi (nt **veoauto mootor mootor**), tootja (**Volvo**) ja teenindustaseme.

## <a name="set-up-asset-service-levels"></a>Vara teenindustasemete seadistus

1. Valige **Varahaldus**\>**Häälestus**\>**Teenindustasemed**.
2. Valige **Uus**, et luua uus kirje.
3. Sõltuvalt vara teenindustaseme üksikasjalikkuse tasemest tehke asjakohased valikud väljadel **Funktsionaalne asukoht**, **Vara tüüp**, **Tootja**, **Mudel**, **Vara**, **Töökäsu tüüp** ja **Teenindustase**.

    > [!NOTE]
    > Kui hooldustaotluste ja töökäskude puhul kasutatakse vara teenindustaset, vaatab varahaldus võimaliku vaste leidmiseks läbi kõik varade teenindustaseme kirjed. Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena. Teisisõnu kontrollib varahaldus esmalt **Töökäsu tüüp** väli. Kui vastet ei leita, kontrollib see vastet väljale **Vara**. Nagu näete lehe **Varahaldus** paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule. Kui vastet ei leita, kasutatakse vaikimisi kirjet, mille valikutes pole kasutatud ühtegi neist seitsmest väljast.

4. Valige **väljal** hooldustase teenuse tase, mis näitab päringu kiireloomulisust.


> [!NOTE]
> Kui muudate vara teenindustaseme kirjet lehel **Vara teenindustase** pärast seda, kui olete seda töökäsul juba kasutanud, ei värskendata seda teenindustaset hooldustaotlustel ja töökäskudel vastavalt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]