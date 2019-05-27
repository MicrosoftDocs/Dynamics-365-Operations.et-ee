---
title: Kliendi makse ülevaated (eelvaade)
description: Teema kirjeldab, kuidas funktsioon Kliendi makse ülevaated aitab ennustada, millal arve ära makstakse, ja luua optimeerimisstrateegiaid, mis täiustavad õigel ajal maksmise tõenäosust.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566235"
---
# <a name="customer-payment-insights-preview"></a>Kliendi makse ülevaated (eelvaade)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> See funktsioon on suunatud väljalaske osa ja see on saadaval ainult kasutajatele, kes on registreerinud privaatse eelvaate jaoks. See funktsioon lisatakse tulevasse üldiselt kättesaadavasse väljalaskesse.

# <a name="overview"></a>Ülevaade

Organisatsioonidel on tihti raske ennustada, millal klient oma arved ära maksab. Ülevaate puudumine võib põhjustada ebatäpset likviidsuse planeerimist, ebatõhusat kogumist ja võimalust, et tellimused väljastatakse klientidele, kes kujutavad endast krediidiriski. Funktsioon Kliendi makse ülevaated (eelvaade) kasutab arve maksmise ennustamiseks masinõpet. Samuti pakub see optimeerimise strateegiaid, mida saab kohandada, et maksimeerida klientide õigel ajal maksmise tõenäosust.

## <a name="predictions"></a>Ennustused

Maksete ennustused võimaldavad organisatsioonidel täiustada oma äritegevusi järgmiselt.

-   Aitab lihtsalt tuvastada arveid, millele ennustatakse makse hilinemist.
-   Rakendab asjakohaseid meetmeid, et suurendada õigel ajal maksmise tõenäosust.

Funktsioon Kliendi makse ülevaated (eelvaade) kasutab arve maksmise ennustamiseks masinõpet. See kasutab ajaloolisi arvete, maksete ja klientide andmeid, et luua masinõppe mudel, mida kasutatakse arve äramaksmise ennustamiseks.

Funktsioon Kliendi makse ülevaated (eelvaade) ennustab iga avatud arve jaoks kolme maksetõenäosust.

-  Tõenäosus, et makse tehakse õigel ajal (enne arve tähtaega).
-  Tõenäosus, et makse tehakse 30 päeva jooksul pärast arve tähtaega.
-  Tõenäosus, et makse tehakse hiljem kui 30 päeva pärast arve tähtaja möödumist.

Maksete tõenäosusi saate vaadata ennustuste jaotises.

[![Maksete ennustused](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Iga arvele määratakse ka võitnud maksetõenäosus, kasutades ühte kolmest eespool määratletud ennustavat maksetõenäosuse stsenaariumit. Suurima maksetõenäosusega stsenaarium on võitnud stsenaarium.


Oletame näiteks, et ennustuse järgi on arve õigel ajal maksmise tõenäosus 71 protsenti, arve 30 päeva jooksul maksmise tõenäosus 13 protsenti ja arve pärast tähtajast 30 päeva möödumist maksmise tõenäosus 16 protsenti. Suurim tõenäosus näitab, et arve maksmise tõenäoliseim stsenaarium on õigel ajal maksmise stsenaarium, nii et arve märgistatakse õigel ajal maksmise tõenäosusega.

[![Maksete ennustused](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Optimeerimise strateegiad

Peale maksete ennustuste saab funktsioon Kliendi makse ülevaated (eelvaade) kasutada ka optimeerimise strateegiaid, et täiustada õigel ajal maksmiste tõenäosust. See võimaldab organisatsioonidel teha tegurite mõju analüüsi, lastes kasutajatel kohandada arvete ja klientide parameetreid ja seejärel võrrelda muudatuste mõju arvete õigel ajal maksmise tõenäosusele.

Näiteks võib organisatsioon soovida hinnata, kuidas mõjutab maksete õigeaegsust arvete skonto värskendamine. Kui arved on optimeeritud kasutama uut allahindlust, saavad kasutajad üle vaadata, kuidas allahindluse rakendamine mõjutab nende arvete õigeaegset maksmist. Kui allahindluse rakendamise kulu on võrreldes õigeaegse makse eelisega minimaalne, siis võib organisatsioon valida selle allahindluse rakendamise kõikidele tulevastele avatud tellimustele.

> [!NOTE] 
> Praegu on funktsiooni Kliendi makse ülevaated (eelvaade) ainuke saadavalolev optimeerimise strateegia allahindlus.

[![Optimeeritud ennustused](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Kuidas hankida funktsioon Kliendi makse ülevaated (eelvaade)

Kui olete huvitatud funktsiooni Kliendi makse ülevaated (eelvaade) proovimisest, saatke meil [finantsülevaadete eelvaate töörühmale](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Privaatsusavaldus

Eelvaated hoiustavad kliendiandmeid Ameerika Ühendriikides. Peale selle eelvaade 1) võib kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 for Finance and Operations teenus, 2) ei ole hõlmatud selle teenuse teenusetaseme leppes, 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud, ja 4) on piiratud toega.
