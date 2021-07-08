---
title: Valitud valeminumber pole partiitellimuse jaoks kinnitatud
description: Kui proovite plaanitud tellimust kinnitada, kuvatakse tõrketeade, mis ütleb, et valitud valeminumber pole partiitellimuse jaoks kinnitatud.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294052"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a>Valitud valeminumber pole partiitellimuse jaoks kinnitatud

Tõrkekood: PRO2614

## <a name="symptoms"></a>Sümptomid

Kui proovite plaanitud tellimust kindlustada, kuvatakse järgmine tõrketeade:

> Valitud valeminumber ei ole partiitellimuse puhul kinnitatud.

## <a name="cause"></a>Põhjus

Süsteem kinnitab kinnitamistoimingu veendumaks, et aktiivse kauba jaoks on saadaval kinnitatud valem. Tõenäoliselt peate valemi kinnitama.

## <a name="resolution"></a>Lahendus

Valemi kinnitamiseks toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Kooslused ja valemid \> Valemid**.
1. Valige asjaomane valem.
1. Valige tegumiriba vahekaardi **Valem** grupis **Halda** suvand **Kinnita valem**.
1. Valige dialoogiboksis **Koosluse või valemi kinnitamine** kinnitaja ja seejärel valige **OK**.
