---
title: Maksegraafiku rakendamine arve töölehele
description: See teema kirjeldab, kuidas lisada makse hankija arve töölehele.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f6481c3fc033acf4bb563bf1716789216646b60b
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358335"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Maksegraafiku rakendamine arve töölehele

[!include [banner](../includes/preview-banner.md)]

Rakenduses Microsoft Dynamics 365 Finance Release 10.0.25 on nüüd hankija arve töölehel **toetatud maksegraafik**.

Selle funktsiooni kasutamiseks peate funktsioonihalduses lubama **maksegraafiku rakendada arvetöölehe** funktsioonile.

Kui funktsioon on lubatud, lisatakse arve **töölehelehele** uus maksegraafiku **väli**. Arve töölehe rea loomisel, kui maksetingimused säilitatakse hankijal ja maksetingimused valitakse maksegraafikus, **·** **uuendatakse maksegraafiku väli arve töölehelehel.**

Kasutatavat maksegraafikut saate muuta vastavalt oma äritegevuse nõuetele. Hankija arve töölehe sisestamisel luuakse hankija avatud kanded vastavalt maksegraafikule.

 - Mitme hankija avatud kande ülevaatamiseks, mis loodi maksegraafikust **, \>\> minge ostureskontro arvete avatud hankijaarvetele** ja sisestage arvenumber või hankija konto.
 - Maksegraafiku ülevaatamiseks või konfigureerimiseks minge Ostureskontro **makse seadistuse maksegraafikusse \>\>.**
 - Maksetingimuste konfigureerimiseks ja maksegraafiku määramiseks minge ostureskontro **\> makseseadistuse \> maksetingimustele**.
 - Maksetingimuste säilitamiseks hankija **\>** puhul minge jaotisesse Ostureskontro kõik hankijad, **valige** hankija konto ja seejärel määrake vahekaardil Makse väli **Maksetingimused.**

Maksegraafiku funktsioon on saadaval ka hankija arve **registreerimise protsessis**. Kui arveregistri töölehel on valitud maksegraafik, siis **arveregistri** sisestamisel mitut hankija makserida ei looda. Hankija makseread luuakse siis, kui arve kinnitatakse.

## <a name="limitation"></a>Kitsendus

Ootel hankija arve korral, kui maksegraafik on arve päises, on täpsem leht, mis võimaldab kasutajatel makseridu redigeerida. (Näiteks saavad kasutajad redigeerida iga makserea maksetähtaega ja väärtust.) Arve töölehelt loodud makseridadel on väärtus maksegraafikust.

See funktsioon on tulevikus saadaval hankija **arve töölehe ja** **ootel** arvete jaoks.
