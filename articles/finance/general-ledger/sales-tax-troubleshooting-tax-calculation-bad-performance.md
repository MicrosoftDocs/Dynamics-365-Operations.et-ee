---
title: Maksuarvestuse jõudlus mõjutab kandeid
description: See artikkel pakub tõrkeotsingu teavet, mis on seotud maksuarvestuse jõudlusega ja selle mõju kannetele.
author: shtao
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3ee0e3a0f8d9c06760776719fbe49e684cb882cf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894902"
---
# <a name="tax-calculation-performance-affects-transactions"></a>Maksuarvestuse jõudlus mõjutab kandeid

[!include [banner](../includes/banner.md)]

Mõnikord mõjutavad kannet jõudlusprobleemid, mis maksuarvestuses tekivad. Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.

## <a name="review-the-transaction-line-count"></a>Vaadake üle tehingu ridade arv

Määrake, kas kandel on suur hulk ridu (nt üle mitmesaja). Kui ei, liigu edasi järgmise jaotise juurde. Kui kandel on mitusada rida, viivitage maksuarvestusega. Lisateavet vt teemast [Luba maksuarvestuse viivitus päevaraamatutes](enable-delayed-tax-calculation.md). 

Järgmisena saate kindlaks teha, kas mõni järgmistest tingimustest on täidetud:

- Imporditehinguid tehakse suurtest failidest.
- Mitu seanssi töötleb sama kande maksuarvestust samal ajal.
- Kandel on mitu rida ja vaadet uuendatakse reaalajas. Näiteks välja **Arvutatud käibemaksusumma** lehel **Pearaamat** uuendatakse reaalaja jooksul rea väljade muutudes.

   [![Arvutatud käibemaksusumma väli päevaraamatu kviitungi lehel.](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)

Kui mis tahes tingimus on täidetud, viivitage maksuarvestusega.

## <a name="review-the-call-stack"></a>Väljakutsete pinu ülevaatamine

Vaadake väljakutsete pinu üle määramaks, kas maksuarvestust kutsutakse välja mitu korda. Kui ei, liigu edasi järgmise jaotise juurde. Kui väljakutsete pinu on alustatakse mitu korda, järgige neid samme, et vähendada maksuarvestuse aega.

1. Kui päevaraamat on kannet arvesse võtnud, viivitage maksuarvestusega. Lisateavet vt teemast [Luba maksuarvestuse viivitus päevaraamatutes](enable-delayed-tax-calculation.md).
2. Kui kanne on ostutellimus ja rakenduse versioon on hilisem kui 10.0.15, võite maksuarvestamisega viivitada kuni lõpliku arvestamiseni lubades flighting **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** jaoks.

## <a name="review-the-call-stack-timeline"></a>Väljakutsete pinu ajajoone ülevaatamine

Vaadake üle väljakutsepinu ajajoon, et teada saada, kas järgmised probleemid on olemas. Kui jah, lubage flighting **TaxUncommittedDoIsolateScopeFlighting** probleemi lahendamiseks.

- Kande tulemusena lõpetab süsteem vastamise, kuni seanss lõpeb. Seetõttu ei saa kanne maksutulemust arvutada. Järgmine näide näitab teateboksi "Sessioon lõpetatud", mille te saate.

    [![Sessiooni lõpetanud teade.](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)

- Meetod **TaxUncommitted** võtab rohkem aega kui teised meetodid. Näiteks järgmisel joonisel võtab meetod **TaxUncommitted::updateTaxUncommitted()** aega 43 347,42 sekundit, kuid teiste meetodite puhul kulub 0,09 sekundit.

    [![Meetodite kestused.](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)

## <a name="customizing-and-calling-tax-calculation"></a>Maksuarvestuse kohandamine ja kutsumine

Kohandamisel ärge kutsuge iga rea puhul meetodile **sisesta()** või **värskenda()** maksuarvestust. Maksuarvestus tuleks kutsuda kande tasemel.

## <a name="determine-whether-customization-exists"></a>Kohanduse olemasolu tuvastamine

Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik. Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
