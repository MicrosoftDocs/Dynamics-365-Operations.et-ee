---
title: Tagastustellimuse tagasimakse on tagasi lükatud
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui tagastustellimusel tagasimakse lükatakse tagasi, kuna arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8360be76fe5ef5ddfbcf290cf6272825bc1849f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879973"
---
# <a name="refund-on-a-return-order-is-declined"></a>Tagastustellimuse tagasimakse on tagasi lükatud

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui tagastustellimusel tagasimakse lükatakse tagasi, kuna arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist.

## <a name="description"></a>Kirjeldus

Tagasimakse lükatakse tagasi, kui tagastustellimuse arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist. Saate järgmise tõrketeate: "Mõned maksed ei ole sisestamiseks õiges olekus. Palun kinnitage uuesti kõikide maksete olek enne arveldamist."

Makse autoriseerimise üksikasjad sisaldavad järgmist tõrketeadet: " Adyen gateway SendRequest() nurjus olekuga 'InternalServerErrorr'.22144; Tühi tagastatyd vastus Adyenìlt. (22001);"

![Tagastustellimuse tagasimakse on tagasi lükatud.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Lahendus

### <a name="enable-blind-returns-in-adyen"></a>Luba pimedad tagastused Adyen`is

Pimetagastuste lubamiseks järgige [Dynamics 365 Payment Connectori Puhvri probleemi tõrkeotsing](adyen-support.md) et võtta ühendust Adyen tugimeeskonnaga ja taotleda pimedate tagastuste lubamist Adyeni kontol.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 maksekonnektor Adyeni jaoks](../dev-itpro/adyen-connector.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.adyen.com/plugins/microsoft-dynamics)
