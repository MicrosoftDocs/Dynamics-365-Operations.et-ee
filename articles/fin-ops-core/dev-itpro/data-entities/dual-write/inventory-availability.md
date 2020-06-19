---
title: Varude saadavuse topeltkirjutus
description: See teema annab teavet varude saadavuse topeltkirjutamise kontrollimise kohta.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426978"
---
# <a name="inventory-availability"></a>Varude saadavus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varude saadavuse abil saate kontrollida oma varusid enne, kui lisate Dynamics 365 mudelipõhistes rakendustes uue toote vormidele **Päringud**, **Tellimused** või **Arved**. Näiteks on varude kontrollimine ja täitmiskuupäeva kindlaks määramine [potentsiaalne klient-raha](dual-write-prospect-to-cash.md) protsessi raames oluline ülesanne. Kui teil puuduvad piisavad varud, siis saate hinnata eeldatava varude vastuvõtu ja väljastamise alusel sissetulekuaega. Samuti saate kontrollida toote saadaval lubamiseks teavet, kus leiate saadaval lubamiseks koguse eelmääratletud ajapiiri raames.

## <a name="on-hand-inventory"></a>Vaba kaubavaru 

Rakenduses Dynamics 365 Sales on vormide **Päringud**, **Tellimused** või **Arved** päisesse lisatud uus nupp **Vaba kaubavaru**. Nupule klõpsates ilmub dialoogiaken ning te saate määratleda ettevõtte ja toote, mille kohta soovite kontrollida vaba kaubavaru. See hangib rakendusest Dynamics 365 Supply Chain Management varude teabe ja kuvab sama teabe, mis sisaldub [Vabas kaubavarus](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Teave sisaldab järgmisi koguseid.

- **Laos olev kogus**
- **Reserveeritud laos olev kogus**
- **Saadaolev laos olev kogus**
- **Tellitud kogus**
- **Tellimisel kogus**
- **Reserveeritud tellitud kogus**
- **Saadaolev kogus kokku**

## <a name="atp-information"></a>ATP teave

Rakenduses Dynamics 365 Sales on vormide **Päringud**, **Tellimused** või **Arved** rea kaupadele lisatud uus nupp **Saadaval lubamiseks teave**. Nupule klõpsates ilmub dialoogiaken ning te saate määratleda ettevõtte, varude saidi, varude lao ja tellimuse koguse. See hangib rakendusest Supply Chain Management **saadaval lubamiseks teabe** ja kuvab jaotises [Toote lubamine](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) kirjeldatud sätted. Teabe hulka kuulub **Saadaval lubamiseks kogus**, **Sissetulekukogus**, **Väljastatav kogus** ja **Vaba kogus**.
