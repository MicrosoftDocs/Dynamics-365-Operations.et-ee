---
title: Müügi- ja üleviimisrea komplekteerimise erandite käsitsi käsitsemine
description: See artikkel kirjeldab, kuidas administraatorid saavad laokandeid käsitsi komplekteeritud (või mitte komplekteeritud) laokannetest kahjustatud müügi- ja üleviimistellimuse andmetest põhjustatud probleemide lahendamiseks.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404416"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Müügi- ja üleviimisrea komplekteerimise erandite käsitsi käsitsemine

[!include [banner](../includes/banner.md)]

Müügi käsitsi töötlemine ja rea komplekteerimise erandite ülekandmine võimaldab administraatoritel parandada probleemid, mis on põhjustatud rikutud müügi- ja üleviimistellimuse andmetest. See võimaldab usaldusväärsetel kasutajatel müügi- ja üleviimistellimuse ridadega seotud laokandeid käsitsi komplekt kanda (või selle komplekt eemaldada), kui laoprotsessid on juba pooleli.

Siin kirjeldatud funktsioone tuleks kasutada ainult juhul, kui süsteem ei saa laoprotsesside pinu töötlemist tavalisel viisil lõpetada. Vaikimisi lubatakse seda kasutada ainult kasutajatel, kellel on süsteemiadministraatori roll. Sellele juurdepääsu saate siiski anda, määrates müügiridade *komplekteeritud ridade määramise teistele rollidele* vastavalt vajadusele käsitsi privileegi.

## <a name="turn-on-this-feature-for-your-system"></a>Selle funktsiooni sisselülitamine teie süsteemi jaoks

Enne kui saate selles artiklis kirjeldatud funktsioone kasutada, tuleb need teie süsteemis sisse lülitada. Administraatorid saavad kasutada funktsioonihalduse [sätteid](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et kontrollida funktsioonide olekut ja lülitada need sisse. **Funktsioonihalduse tööruumis** loetletakse funktsioonid järgmiste nimede abil:

- *Käsitsi müügirea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele*<br>(Tarneahela halduse versiooni 10.0.25 kohaselt on see funktsioon kohustuslik ja seda ei saa välja lülitada.)
- *Käsitsi ülekanderea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Müügi- või üleviimistellimuse ridadega seotud kannete korrigeerimine

Kasutage järgmist protseduuri müügi- või üleviimistellimuse ridadega seotud kannete parandamiseks.

1. Vastavalt tellimuse tüübile, mida peate korrigeerima, järgige ühte järgmistest sammudest:

    - Müügitellimusega seotud kande parandamiseks minge laohalduse perioodiliste ülesannete **\>\> juurde Müügirea käsitsi \> puhastamine.**
    - Üleviimistellimusega seotud kande parandamiseks minge laohalduse perioodiliste ülesannete **\> juurde.\>\>**

1. Kasutage **müügiridade** **käsitsi** noppimiseks või üleviimisridade käsitsi valimiseks ruudustiku ülaosas filtreid otsitav rida ja valige seejärel ülemisel ruudustikul sihttellimuse rida.
1. Valitud rea **kohta lisateabe** saamiseks **kasutage** alumises jaotises laokandeid, **·** **koorma** ridu, tööridu ja konteineri ridu. Nende vahekaartide teave annab põhiülevaate seotud laoprotsessidest ja nende olekutest.
1. Tegevuspaanil valige suvand **Komplekteeritud**, et avada laokannete valitud **tellimuserida** lehel Komplekteeritud. Seda sammu saate lõpetada ka juba lattu väljastatud tellimuseridade puhul. (Tavaliselt ei saa lattu väljastatud tellimuseridu enam laos avada **Komplekteeritud** leht.)

    > [!NOTE]
    > Kui avate lehe Komplekteeritud, võite saada erinevaid **hoiatusi**. Tehke mis tahes toiming, mida need hoiatused soovitavad. Näiteks võite saada hoiatuse laotööga seotud tellimuseridade kohta. Sel juhul on mõtet proovida tühistada [tööd, kasutades standardseid tühistamistöö](cancel-warehouse-work.md) funktsioone, enne kui teete käsitsi paranduse.

1. Valige rida ruudustikus **Kanded** ja seejärel valige tööriistaribal **Kanded** suvand Lisa **komplekteerimisrida**.
1. Valitud rida teisaldatakse komplekteerimisridade **ruudustikku**. Seadistage sobivad väärtused veergudele, mis puuduvad nõutavast teabest. (Näiteks määrake asukoht ja litsentsiplaat, millelt kaup komplekteeritud/mitte komplekteeritud.)
1. Valige **komplekteerimisridade tööriistaribal** **kõigi valimine**.

## <a name="correct-load-line-quantities"></a>Õiged koormarea kogused

Kasutage järgmist protseduuri koormarea koguse parandamiseks.

1. Vastavalt tellimuse tüübile, mida peate korrigeerima, järgige ühte järgmistest sammudest:

    - Müügitellimusega seotud kande parandamiseks minge laohalduse perioodiliste ülesannete **\>\> juurde Müügirea käsitsi \> puhastamine.**
    - Üleviimistellimusega seotud kande parandamiseks minge laohalduse perioodiliste ülesannete **\> juurde.\>\>**

1. Kasutage **müügiridade** **käsitsi** noppimiseks või üleviimisridade käsitsi valimiseks ruudustiku ülaosas filtreid otsitav rida ja valige seejärel ülemisel ruudustikul sihttellimuse rida.
1. Alumise jaotise **vahekaardil** Koorma read valige tööriistaribal **käsitsi suvand Õiged koormaread**.
1. Vaadake laokannete **ruudustikus** leheküljel **Õiged** koormaread käsitsi üle valitud koormareaga seotud laokanded.
1. Ülemisel ruudustikul parandage koormarea kogused järgmistes veergudes vastavalt vajadusele:

    - **Töö loodud kogus**
    - **Komplekteeritud kogus**
    - **Plaanitud ristlaadimise kogus**

    Süsteem kinnitab kõik nendes veergudes tehtud muudatused.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
