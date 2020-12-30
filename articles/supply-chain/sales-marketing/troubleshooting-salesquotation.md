---
title: Müügipakkumiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426213"
---
# <a name="troubleshoot-sales-quotations"></a>Müügipakkumiste tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega töötamisel tekkivaid probleeme.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Ma ei saa muuta teenusüksuse puhul müügipakkumise müügikogust.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui proovite määrate müügipakkumise real müügikoguse (väli **SalesQty**) kauba jaoks, mille tüüp on *Teenus*, kuvatakse järgmine teade: „Värskendamine pole välja „Kogus” puhul lubatud”.

### <a name="issue-resolution"></a>Probleemi lahendamine

Te ei saa määrata kogust toodete jaoks, mis on teenusüksused. Näiteks kui pakute teenust kauba installimiseks, ei ole mõtet kogust salvestada, kuna füüsiline kaup puudub. Olemas on ainult teenus.

