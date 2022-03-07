---
title: Maksegraafiku rakendamine arve töölehele
description: Selles teemas kirjeldatakse, kuidas hankija arve töölehele makset lisada.
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
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075733"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Maksegraafiku rakendamine arve töölehele

[!include [banner](../includes/preview-banner.md)]

Microsofti Dynamics 365 Finance väljalaskes 10.0.25 toetatakse nüüd hankija arve töölehel maksegraafikut.

Selle funktsiooni kasutamiseks peate funktsioonihalduse funktsioonis lubama **funktsiooni Rakenda maksegraafik arvežurnaalile**.

Kui funktsioon on lubatud, **lisatakse lehele Arve žurnaali** uus **maksegraafiku** väli. Arvežurnaali rea loomisel, kui hankijal säilitatakse maksetingimused ja maksegraafikus on valitud maksetingimused, **värskendatakse** välja Maksegraafik **lehel Arve**.

Kasutatavat maksegraafikut saate muuta vastavalt oma ettevõtte vajadustele. Hankija arve töölehe konteerimisel luuakse hankija avatud kanded vastavalt maksegraafikule.

Maksegraafikust loodud mitme hankija avatud kande ülevaatamiseks minge ostureskontro **\> arved \> Avatud hankijaarved** ja sisestage arve number või hankija konto.

Maksegraafiku ülevaatamiseks või konfigureerimiseks minge ostureskontro makse häälestuse **maksegraafikusse.\>\>**

Maksetingimuste konfigureerimiseks ja maksegraafiku määramiseks minge ostureskontro **makse seadistamise \>\> tingimustesse**.

Hankija maksetingimuste säilitamiseks minge ostureskontrole **\> Kõik hankijad**, valige hankija konto ja seejärel seadke **vahekaardil** Makse **välja Maksetingimused**.

Maksegraafiku funktsioon on saadaval **ka hankija arveregistri** protsessis. Kui arveregistri töölehel on valitud maksegraafik, ei **looda** arveregistri konteerimisel mitut hankija makserida. Hankija makseread luuakse arve kinnitamisel.

## <a name="limitation"></a>Kitsendus

Ootel hankija arve puhul, kui maksegraafik on arvepäises, on olemas täpsem leht, mis võimaldab kasutajatel makseridu redigeerida. (Näiteks saavad kasutajad muuta iga makserea tähtaega ja väärtust.) Arvežurnaalist loodud makseridade väärtus on maksegraafikust.

See funktsioon on saadaval hankija arve töölehe ja ootel arvete jaoks tulevases väljaandes.
