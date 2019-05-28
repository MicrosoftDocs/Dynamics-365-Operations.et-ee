---
title: Käsitsi koostatava mallkoosluse loomine
description: Saate luua mallkoosluse, kasutades mitmesuguseid meetodeid.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566580"
---
# <a name="create-a-template-bom"></a>Käsitsi koostatava mallkoosluse loomine   

[!include [banner](../includes/banner.md)]


Saate luua mallkoosluse, kasutades üht järgmistest meetoditest. Kõikide meetodite puhul on väljad **Kuupäevast** ja **Kuupäevani** valikulised ja ainult informatiivsed.

## <a name="create-a-template-bom-manually"></a>Mallkoosluse loomine käsitsi

1.  Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Käsitsi**.

4.  Sisestage väljale **Kaubakood** kaup tüübist **Kooslus** .

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Klõpsake nupul **OK**.

Luuakse uus tühi mallkooslus.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Mallkoosluse loomine teise mallkoosluse baasil

1.  Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Mallkooslus**.

4.  Valige väljal **Viitenumber** olemasolev mallkooslus, mida soovite uude mallkooslusesse kopeerida.

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Klõpsake nupul **OK**.

Luuakse uus mallkooslus, kasutades ridu, mis vastavad algse mallkoosluse ridadele.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Mallkoosluse loomine teise mallkoosluse baasil

1.  Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Kooslus**.

4.  Valige koosluse versioon väljal **Viitenumber**. Kaup tüübist kooslus kopeeritakse väljale **Kaubakood**.

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Klõpsake nupul **OK**.

Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslused** loendatud koosluse ridadele.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Mallkoosluse loomine tootmiskoosluse baasil

1.  Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.

2.  Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.

3.  Valige jaotisest **Kopeeri koosluseread viitest** suvand **Tootmine**.

4.  Valige tootmiskooslus väljal **Viitenumber**.

5.  Sisestage malli nimi väljale **Nimi**.

6.  Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.

7.  Klõpsake nupul **OK**.

Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslus** loendatud koosluse ridadele.

## <a name="see-also"></a>Vt ka

[Mallkooslused](template-boms.md)

  


