---
title: Tagastustellimuse tagasimakse on tagasi lükatud
description: See teema annab tõrkeotsingu juhised, mis võivad aidata, kui tagastustellimusel tagasimakse lükatakse tagasi, sest arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5961e77de1de5dc23454fc1a6e16f8c0b4e7cc6a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801551"
---
# <a name="refund-on-a-return-order-is-declined"></a>Tagastustellimuse tagasimakse on tagasi lükatud

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis võivad aidata, kui tagastustellimusel tagasimakse lükatakse tagasi, sest arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist.

## <a name="description"></a>Kirjeldus

Tagasimakse lükatakse tagasi, kui tagastustellimuse arveldamiseks kasutatav krediitkaart erineb algse makse autoriseerimisel kasutatud kaardist. Saate järgmise tõrketeate: "Mõned maksed ei ole sisestamiseks õiges olekus. Palun kinnitage uuesti kõikide maksete olek enne arveldamist."

Makse autoriseerimise üksikasjad sisaldavad järgmist tõrketeadet: " Adyen gateway SendRequest() nurjus olekuga 'InternalServerErrorr'.22144; Tühi tagastatyd vastus Adyenìlt. (22001);"

![Tagastustellimuse tagasimakse on tagasi lükatud](media/refund-order-decline.jpg)

## <a name="resolution"></a>Eraldusvõime

### <a name="enable-blind-returns-in-adyen"></a>Luba pimedad tagastused Adyen`is

Pimetagastuste lubamiseks järgige [Dynamics 365 Payment Connectori Puhvri probleemi tõrkeotsing](adyen-support.md) et võtta ühendust Adyen tugimeeskonnaga ja taotleda pimedate tagastuste lubamist Adyeni kontol.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 maksekonnektor Adyeni jaoks](../dev-itpro/adyen-connector.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.adyen.com/plugins/microsoft-dynamics)
