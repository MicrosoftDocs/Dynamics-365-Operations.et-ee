---
title: Käsitsi koostatava mallkoosluse loomine
description: Saate luua mallkoosluse, kasutades mitmesuguseid meetodeid.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169b54a0509a2e11ce2e888404da10fd81db475e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678202"
---
# <a name="create-a-template-bom"></a>Käsitsi koostatava mallkoosluse loomine   

[!include [banner](../includes/banner.md)]


Saate luua mallkoosluse, kasutades üht järgmistest meetoditest. Kõikide meetodite puhul on väljad **Kuupäevast** ja **Kuupäevani** valikulised ja ainult informatiivsed.

## <a name="create-a-template-bom-manually"></a>Mallkoosluse loomine käsitsi

1.  Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Käsitsi**.

4.  Sisestage väljale **Kaubakood** kaup tüübist **Kooslus** .

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Valige nupp **OK**.

Luuakse uus tühi mallkooslus.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Mallkoosluse loomine teise mallkoosluse baasil

1.  Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Mallkooslus**.

4.  Valige väljal **Viitenumber** olemasolev mallkooslus, mida soovite uude mallkooslusesse kopeerida.

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Valige nupp **OK**.

Luuakse uus mallkooslus, kasutades ridu, mis vastavad algse mallkoosluse ridadele.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Mallkoosluse loomine teise mallkoosluse baasil

1.  Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Kooslus**.

4.  Valige koosluse versioon väljal **Viitenumber**. Kaup tüübist kooslus kopeeritakse väljale **Kaubakood**.

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Valige nupp **OK**.

Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslused** loendatud koosluse ridadele.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Mallkoosluse loomine tootmiskoosluse baasil

1.  Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Tootmine**.

4.  Valige tootmiskooslus väljal **Viitenumber**.

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Valige nupp **OK**.

Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslus** loendatud koosluse ridadele.

## <a name="see-also"></a>Vt ka

[Mallkooslused](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]