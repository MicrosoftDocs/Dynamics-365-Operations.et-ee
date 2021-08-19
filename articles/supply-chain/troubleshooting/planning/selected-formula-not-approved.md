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
ms.openlocfilehash: a41cf955d151726348bea83e52a24bc8784352c2d07268ced944e4cc6bf35491
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712906"
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
