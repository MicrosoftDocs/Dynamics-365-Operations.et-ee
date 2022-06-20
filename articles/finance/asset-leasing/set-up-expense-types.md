---
title: Kulutüüpide seadistamine
description: See artikkel kirjeldab, kuidas seadistada kulutüüpe Asset ligemis.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9978041059437d5d3556236c7ac02c00db93f933
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908034"
---
# <a name="set-up-expense-types"></a>Kulutüüpide seadistamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada kulutüüpe Asset ligemis. Kulusid, mida maksegraafik ei esinda, nimetatakse *kuluhindadeks*. Nende kulude näidete hulka kuuluvad kinnisvaramaksud, ühiste pindade hoolduskulud ja kindlustuskulud.

## <a name="add-an-administrative-expense-type"></a>Halduskulu tüübi lisamine

1. Avage **Vara rentimine \> Seadistus \> Kulutüübid**.
2. Valige suvand **Uus**.
3. Sisestage vastavatele väljadele uus kulutüüp ja kirjeldus.

## <a name="assign-accounts-to-administrative-costs"></a>Määrake halduskuludele kontod

Järgmisena peaksite seostama kontod kulutüüpidega. Need kontod debiteeritakse siis, kui kulude graafiku kirjed sisestatakse. Vastaskonto on määratud iga rendi ridadele **Täitekulude maksegraafik**.

1. Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.
2. Valige kulutüüp vahekaardi **Kontod** kiirkaardi **Täitekulud** väljal **Kulu tüüp**.
3. Valige **Lisa**.
4. Valige väljal **Raamatu tüüp** raamatu tüüp halduskuludega sidumiseks.

    > [!NOTE]
    > Sama kulukontoga võib siduda mitu raamatu tüüpi.

5. Määratlega väljal **Konto kood**, millistele rentidele raamat peaks kohalduma.

    - **Kõik** – kohalda raamatut kõigile rentidele.
    - **Grupp** – kohalda raamatud konkreetsele rentide grupile.
    - **Tabel** – kohalda raamatut konkreetsetele rentidele.

6. Kui valisite väljal **Konto kood** suvandi **Grupp** või **Tabel**, siis valige väljal **Konto/grupi number** konto number või grupi number.
7. Valige vastavatel väljadel kapitalirendi põhikonto ja kasutusrendi põhikonto.

Kui olete need sammud lõpule viinud, saate valitud rendi lehe **Rendi üksikasjad** ridade **Täitekulude maksegraafik** kaudu kulusid lisada. Teise võimalusena saate lisada kulusid uue rendilepingu loomisel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
