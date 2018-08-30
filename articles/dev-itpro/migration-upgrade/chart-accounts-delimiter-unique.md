---
title: Kontoplaani eraldaja kordumatuks muutmine
description: "Rakenduses Dynamics 365 for Finance and Operations ei saa kontoplaani ja dimensiooniväärtuste eraldaja sama olla. Pärast versiooniuuendust peate eraldaja väärtusi muutma."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Kontoplaani eraldaja kordumatuks muutmine

[!include [banner](../includes/banner.md)]

Rakenduses Microsoft Dynamics AX 2012 saate kasutada kontoplaani ja dimensiooniväärtuste puhul sama eraldajat. Rakenduses Dynamics 365 for Finance and Operations ei saa kontoplaani ja dimensiooniväärtuste eraldaja sama olla. Topelteraldaja korral saate seda pärast versiooniuuendust muuta. 

See funktsioon on saadaval järgmistes rakenduste versioonides.
- Dynamics 365 for Finance and Operationsi versioon 8.0
- Dynamics 365 for Finance and Operationsi versioon 7.1, KB 4094701 puhul ei saa finantsdimensioone sisestada, kui dimensiooniväärtused sisaldavad kontoplaani eraldajat
- Dynamics 365 for Finance and Operations versioon 7.2 KB 4092967 puhul ei saa valida alamprojekti dimensioonina, kui alamprojekti vorming sisaldab dimensiooni eraldajat

## <a name="update-delimiter"></a>Eraldaja värskendamine
Kontoplaani konflikti korral saab muuta kontoplaani eraldaja ja projekti/alamprojekti ID vormingut. Ühtegi teist dimensiooni eraldajat muuta ei saa. 
- Kontoplaani eraldajat saate muuta pärast üleminekut Finance and Operationsile, kui valite **Üldised pearaamatu parameetrid** > **Kontoplaan ja dimensioonid** > **Muuda eraldajat**. 
- Kui konfliktne on ainult projekti/alamprojekti ID vorming, saate selle väärtust muuta, valides **Projektihalduse ja -arvestuse parameetrid** > **Üldine** > **Alamprojekti vormingu muutmine**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Kuidas teha kindlaks, kas teie keskkonna puhul on nõutud eraldajate värskendamine? 
Kui täiendatud keskkonnas esineb eraldajatega seoses konflikte, võib segmenditud sisestamise või dimensiooni kirje juhtimises väärtuste sisestamisel ilmneda ebastabiilsus. See tähendab, et teil tuleb alati konto ja dimensiooni kombinatsioonide sisestamisel kasutada otsinguid või hüpikmenüüd.

