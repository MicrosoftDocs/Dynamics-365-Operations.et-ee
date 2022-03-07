---
title: Laovarude korrigeerimine
description: Sellest teemast saate teavet laovarude korrigeerimist töölehe kohta ja töötlemise kohta, kui kasutate skaalaühikuid.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938222"
---
# <a name="warehouse-inventory-adjustment"></a>Laovarude korrigeerimine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Lao varude korrigeerimise funktsiooni kasutatakse pilve ja servaskaala üksuste käitamisel [tootmise töökoormuste](cloud-edge-workload-manufacturing.md) ja [laohalduse töökoormuste](cloud-edge-workload-warehousing.md) jaoks.

Kui töötaja teeb laovarude korrigeerimist lao rakenduse abil laoala üksuse laohalduse töökoormuse suhtes, peab laohalduse **lao varude korrigeerimise töölehe** pakett-töö töötlema füüsilist vaba laovaru uuendamist, mida käitate ja planeerite, kui soovite minna **Laohaldus > Perioodiliste ülesannete > Lao varude korrigeerimise töölehele**.

Järgmistes lao rakenduste tööprotsessides kasutatakse praegu **laovarude korrigeerimise töölehte** kaaluühiku töökoormustel:

- Korrigeerimine sisse/välja
- Tsükliline inventuur
- Litsentsiplaadi laadimine

Mitmed laokanded luuakse pilve ja varude korrigeerimisprotsessi osana, sest keskuse ja kaalu ühiku juurutamised jagavad laokirjeid.

## <a name="inventory-adjustment-example"></a>Varude korrigeerimise näide

Selles näites on laotöötaja kasutanud lao rakendust, et registreerida vaba kaubavaru lisamine.

Kõigepealt loob kaaluühiku töökoormus lao varude korrigeerimiskande positiivse füüsilise korrigeerimise jaoks, mis seejärel sünkroonitakse keskusega ja suurendab keskuse vaba kaubavaru.

| Tüüp                                    | Skaalaüksus | Direction | Keskus |
|-----------------------------------------|------------|-----------|-----|
| Laovarude korrigeerimine          | +1         | ->        | +1  |

Seejärel töötleb keskus inventuuritöölehe sisestust, mille saab [sõnumiprotsessori teadete](cloud-edge-message-processor-messages.md) kaudu. See uuendab edasist vaba kaubavaru. Topeltlao vältimiseks loob keskus protsessi osana vastaskande ja eemaldab varem kirjendatud vaba kaubavaru, mis on seotud lao varude korrigeerimisega.

| Tüüp                                    | Skaalaüksus | Direction | Keskus |
|-----------------------------------------|------------|-----------|-----|
| Inventuur                                | +1         | <-        | +1  |
| Lao varude korrigeerimine (vastaskonto) | –1         | <-        | –1  |

Pärast seda, kui kaaluühik on keskusele loonud **Lao varude korrigeerimise töölehe**, saate üle vaadata nii **inventuuritöölehte** kui ka **vastastöölehte** mille keskus on loonud korrigeerimisprotsessi osana.

Saate läbi vaadata kõik need töölehe sisestused ja kanded Supply Chain Managementis järgmiste sammude abil:

1. Logige sisse kaaluühikusse.
1. Avage **Laohaldus \> Perioodilised ülesanded \> Laovarude kohandamise tööleht**.
1. **Lao varude korrigeerimise töölehe** lehel otsige ja avage tööleht, mis kirjendas vaba kaubavaru muudatust. **Töölehe ridade** jaotises kuvatakse kõik selle töölehe salvestatud korrektsioonid.
1. Keskusesse sisselogimine.
1. Avage **Laohaldus \> Perioodilised ülesanded \> Laovarude kohandamise tööleht**.
1. **Lao varude korrigeerimise töölehe** lehel peaksite nägema sama töölehte, mis on loetletud, kui keskus ja kaaluühik on sünkroonitud.
1. Avage tööleht. Kui [teateprotsessori teateid](cloud-edge-message-processor-messages.md) on töödeldud, näete linke **inventuuritöölehele** ja päises **vastastöölehele**.
    - **Inventuuritööleht** peab kuvama töölehe ridadega samad dimensiooniväärtused.
    - **Vastaskonto tööleht** peab näitama vastaskontot, mis eemaldab topeltvarude korrigeerimise.
    > [!NOTE]
    > Kui kogu sünkroonimine ja töötlemine on lõpetatud, sünkroonitakse **inventuuri tööleht** ja **vastastööleht** tagasi kaaluühikusse. Neid saab vaadata ka vastaval **laovarude korrigeerimise töölehe** leheküljel.
