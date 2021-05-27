---
title: TDS-i parameetrite määramine
description: See teema kirjeldab, kuidas seadistada parameetreid määratud kannetes allika (TDS) funktsioonis mahaarvatud maksu aktiveerimiseks. See on vajalik samm allika TDS-is maha arvatud maksu kasutamiseks.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023176"
---
# <a name="set-the-tds-parameters"></a>TDS-i parameetrite määramine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada parameetreid määratud kannetes allika (TDS) funktsioonis mahaarvatud maksu aktiveerimiseks. See on vajalik samm allika TDS-is maha arvatud maksu kasutamiseks.

1. Avage **Pearaamat \> Pearaamatu seadistamine \> Pearaamatu parameetrid**.
2. Jaotises **Otsesed maksud** vahekaardil **Allikast mahaarvatud** väljal seadke suvand **Aktiveeri TDS** suvandiks **Jah** et aktiveerida TDS-funktsioon ning kasutatavad lehed ja väljad.
3. Seadke **Arve** valikule **Jah** et aktiveerida väljad, mida kasutatakse TDS-i arvutamiseks ja mahaarvamiseks arve tasemel.
4. Seadke **Makse** valikule **Jah** et aktiveerida väljad, mida kasutatakse TDS-i arvutamiseks ja mahaarvamiseks arve tasemel.

    [![Otsesed maksud vahekaart](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Leidke **Numbriseeriate** vahekaardil rida, kus **Viitenumbri** väärtuseks on seatud **Kinnipeetava maksu makse**. Sisestage **Numbriseeria kood** väljale rea jaoks numbriseeria kood väljale . Numbriseeria koodi kasutatakse TDS-i perioodilise tasakaalustusprotsessi jaoks kandenumbrite loomiseks.

    > [!NOTE]
    > Perioodilise TDS-i tasakaalustusprotsessi käivitamiseks minge **Maks \> Deklaratsioon \> kinnipeetava maksu \> Kinnipeetava maksu makse**.

    [![Vahekaart Numbriseeriad](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Sulgege leht.
