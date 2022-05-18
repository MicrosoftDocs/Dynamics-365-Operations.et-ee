---
title: TDS-i parameetrite määramine
description: See teema kirjeldab, kuidas seadistada parameetreid määratud kannetes allika (TDS) funktsioonis mahaarvatud maksu aktiveerimiseks. See on vajalik samm allika TDS-is maha arvatud maksu kasutamiseks.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f7c8802d10a065c60894e80c8ff3cb19163d5ffe
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726917"
---
# <a name="set-the-tds-parameters"></a>TDS-i parameetrite määramine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada parameetreid määratud kannetes allika (TDS) funktsioonis mahaarvatud maksu aktiveerimiseks. See on vajalik samm allika TDS-is maha arvatud maksu kasutamiseks.

1. Avage **Pearaamat \> Pearaamatu seadistamine \> Pearaamatu parameetrid**.
2. Jaotises **Otsesed maksud** vahekaardil **Allikast mahaarvatud** väljal seadke suvand **Aktiveeri TDS** suvandiks **Jah** et aktiveerida TDS-funktsioon ning kasutatavad lehed ja väljad.
3. Seadke **Arve** valikule **Jah** et aktiveerida väljad, mida kasutatakse TDS-i arvutamiseks ja mahaarvamiseks arve tasemel.
4. Seadke **Makse** valikule **Jah** et aktiveerida väljad, mida kasutatakse TDS-i arvutamiseks ja mahaarvamiseks arve tasemel.

    [![Otsesed maksud vahekaart.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Leidke **Numbriseeriate** vahekaardil rida, kus **Viitenumbri** väärtuseks on seatud **Kinnipeetava maksu makse**. Sisestage **Numbriseeria kood** väljale rea jaoks numbriseeria kood väljale . Numbriseeria koodi kasutatakse TDS-i perioodilise tasakaalustusprotsessi jaoks kandenumbrite loomiseks.

    > [!NOTE]
    > Perioodilise TDS-i tasakaalustusprotsessi käivitamiseks minge **Maks \> Deklaratsioon \> kinnipeetava maksu \> Kinnipeetava maksu makse**.

    [![Vahekaart Numbriseeriad.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Sulgege leht.
