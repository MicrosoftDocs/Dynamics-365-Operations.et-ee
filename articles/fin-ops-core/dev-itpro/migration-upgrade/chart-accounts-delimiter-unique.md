---
title: Kontoplaani eraldaja kordumatuks muutmine
description: Selles teemas selgitatakse, kuidas kontoplaani ja dimensiooniväärtuste eraldaja ei saa sama olla. Pärast versiooniuuendust peate eraldaja väärtusi muutma.
author: panolte
manager: AnnBe
ms.date: 03/30/2018
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
ms.openlocfilehash: 183980651a811ef30a49461ff5a5f649d94b079c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565258"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Kontoplaani eraldaja kordumatuks muutmine

[!include [banner](../includes/banner.md)]

Rakenduses Microsoft Dynamics AX 2012 saate kasutada kontoplaani ja dimensiooniväärtuste puhul sama eraldajat. Rakenduse Finance and Operations praeguses versioonis ei saa kontoplaani ja dimensiooniväärtuste eraldaja olla samad. Topelteraldaja korral saate seda pärast versiooniuuendust muuta. 

Seda funktsiooni ei saa järgmistes versioonides kasutada.
- Finance and Operationsi versioon 8.0
- Finance and Operationsi versiooni 7.1, KB 4094701 puhul ei saa finantsdimensioone sisestada, kui dimensiooniväärtused sisaldavad kontoplaani eraldajat
- Finance and Operationsi versiooni 7.2 KB 4092967 puhul ei saa valida alamprojekti dimensioonina, kui alamprojekti vorming sisaldab dimensiooni eraldajat

## <a name="update-delimiter"></a>Eraldaja värskendamine
Kontoplaani konflikti korral saab muuta kontoplaani eraldaja ja projekti/alamprojekti ID vormingut. Ühtegi teist dimensiooni eraldajat muuta ei saa. 
- Kontoplaani eraldajat saate muuta pärast üleminekut, kui valite **Üldised pearaamatu parameetrid** > **Kontoplaan ja dimensioonid** > **Muuda eraldajat**. 
- Kui konfliktne on ainult projekti/alamprojekti ID vorming, saate selle väärtust muuta, valides **Projektihalduse ja -arvestuse parameetrid** > **Üldine** > **Alamprojekti vormingu muutmine**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kuidas teha kindlaks, kas teie keskkonna puhul on nõutud eraldajate värskendamine? 
Kui täiendatud keskkonnas esineb eraldajatega seoses konflikte, võib segmenditud sisestamise või dimensiooni kirje juhtimises väärtuste sisestamisel ilmneda ebastabiilsus. See tähendab, et teil tuleb alati konto ja dimensiooni kombinatsioonide sisestamisel kasutada otsinguid või hüpikmenüüd.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]