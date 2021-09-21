---
title: Teenusüksuse müügikogust ei saa muuta müügipakkumise real
description: Müügipakkumistega töötades ei saa te määrata müügikogust toodetele, mis on teenusüksused, kuna puuduvad füüsilised kaubad, mida loendada.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476161"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Teenusüksuse müügikogust ei saa muuta müügipakkumise real

## <a name="symptoms"></a>Sümptomid

Kui proovite määrate müügipakkumise real müügikoguse (**Müügikogus** väli) kauba jaoks, mille tüüp on *Teenus*, kuvatakse järgmine teade:

> Uuendamine pole välja Kogus puhul lubatud.

## <a name="cause"></a>Põhjus

Selline käitumine on nii kavandatud. Te ei saa määrata kogust toodete jaoks, mis on teenusüksused. Näiteks kui pakute teenust kauba installimiseks, ei ole mõtet kogust salvestada, kuna füüsiline kaup puudub. Olemas on ainult teenus.
