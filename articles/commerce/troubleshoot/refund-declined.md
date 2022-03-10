---
title: Tagastustellimuse tagasimakse on tagasi lükatud
description: See teema annab tõrkeotsingu juhised, mis võivad aidata, kui tagastustellimusel tagasimakse lükatakse tagasi, sest arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist.
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
ms.openlocfilehash: 8880d72d702758d611755bce48a331e3f2e28ca1b7abf485e8b4f7301317c875
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738620"
---
# <a name="refund-on-a-return-order-is-declined"></a>Tagastustellimuse tagasimakse on tagasi lükatud

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis võivad aidata, kui tagastustellimusel tagasimakse lükatakse tagasi, sest arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist.

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
