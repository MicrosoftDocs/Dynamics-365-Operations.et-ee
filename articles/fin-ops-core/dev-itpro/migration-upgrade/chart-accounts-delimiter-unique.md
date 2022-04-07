---
title: Kontoplaani eraldaja kordumatuks muutmine
description: Selles teemas selgitatakse, kuidas kontoplaani ja dimensiooniväärtuste eraldaja ei saa sama olla. Pärast versiooniuuendust peate eraldaja väärtusi muutma.
author: panolte
ms.date: 03/23/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 433e9f8a7b0a9f476c74096a4bd7fef03c87dee1
ms.sourcegitcommit: 0d5ee97670bdeb1986aaea880f32962b5e374751
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468044"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Kontoplaani eraldaja kordumatuks muutmine

[!include [banner](../includes/banner.md)]

Rakenduses Microsoft Dynamics AX 2012 saate kasutada kontoplaani ja dimensiooniväärtuste puhul sama eraldajat. Finance and Operationsi praeguses versioonis ei saa kontoplaani ja dimensiooniväärtuste eraldaja sama olla. Topelteraldaja korral saate seda pärast versiooniuuendust muuta. 

## <a name="update-delimiter"></a>Eraldaja värskendamine
Kontoplaani konflikti korral saab muuta kontoplaani eraldaja ja projekti/alamprojekti ID vormingut. Ühtegi teist dimensiooni eraldajat muuta ei saa. 
- Kontoplaani eraldajat saate muuta pärast üleminekut, kui valite **Üldised pearaamatu parameetrid** > **Kontoplaan ja dimensioonid** > **Muuda eraldajat**. 
- Kui konfliktne on ainult projekti/alamprojekti ID vorming, saate selle väärtust muuta, valides **Projektihalduse ja -arvestuse parameetrid** > **Üldine** > **Alamprojekti vormingu muutmine**. 

### <a name="other-considerations"></a>Muud kaalutlused
Sarnaselt projekti/alamprojekti ID-ga ei tohi ühelgi teisel finantsdimensioonidena (nt hankijate või klientidena) kasutatavatel koondandmete kirjetel olla konto ID väärtusi, mis kasutavad kontoplaani eraldajaga sama märki. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kuidas teha kindlaks, kas teie keskkonna puhul on nõutud eraldajate värskendamine? 
Kui täiendatud keskkonnas esineb eraldajatega seoses konflikte, võib segmenditud sisestamise või dimensiooni kirje juhtimises väärtuste sisestamisel ilmneda ebastabiilsus. See tähendab, et teil tuleb alati konto ja dimensiooni kombinatsioonide sisestamisel kasutada otsinguid või hüpikmenüüd.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
