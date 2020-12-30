---
title: Rentimise parameetrite konfigureerimine (eelversioon)
description: See teema kirjeldab varade rentimise konfiguratsiooni seadistusi, nagu turbeteave ja raamatupidamise sätteid.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442567"
---
# <a name="configure-lease-parameters"></a>Rentimise parameetrite konfigureerimine

[!include [banner](../includes/banner.md)]

Varade rentimise käitumist mõjutavad mitu konfiguratsiooni sätet. Need sätted hõlmavad töölehe nimesid, üldisi parameetreid ja sisestusreeglite sätteid.

1. Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.
2. Valige vahekaardil **Rendikirjed** kiirkaart **Üldine**.

    Parameeter **Luba käsitsi klassifitseerimise alistamise** määratleb, kas rendi klassifikatsiooni saab alistada enne maksegraafiku kinnitamist.

    Parameeter **Ristolemi partii** määratleb, kas saate sisestada praegusest juriidilisest isikust teistesse juriidilistesse isikutesse. Kui see parameeter on sisse lülitatud, saate luua töölehe kandeid juriidilistele isikutele, millele teil on juurdepääs.

3. Määrake suvandi **Luba kinnitatud rendilepingute kustutamine** väärtusele **Jah**, et lubada rendikirjed, milles sisalduvad kustutamiseks kinnitatud maksegraafikuid. Rendikirjeid saab kustutada, kui nendega on seostatud sisestatud või sisestamata kanded, olenemata selle valiku sättest. Rendikirjet ei saa pärast kustutamist taastada. Kui laadite mõne kustutatud rendikirjetest (käsitsi või andmeolemite), käsitletakse üleslaaditud teavet uuena, mitte olemasoleva rendikirje värskendusena.

    Kui valite selle suvandi väärtuseks **Jah** ja raamatu kande tüüp on **Kumulatiivse järelkulu valik A või B**, määrab süsteem välja **Alternatiivne laenuintressimäär** suvandi **Ülemineku alternatiivne laenuintressimäär** väärtuseks **Raamatu häälestus**. Kui selle suvandi väärtuseks on määratud **Ei**, seatakse põhirendi määr välja **Alternatiivne laenuintressimäär** väärtusele lehel **Raamatu üksikasjad**, sõltumata raamatu ülekande tüübist.

4. Määrake suvandi **Luba suletud raamatu versiooni suvand kulumiarvestused** väärtuseks **Jah**, et lubada kulumiarvestuse kannete ümberpööramine. Kulukanded saab pöörata ümber isegi siis, kui raamatu versioon on suletud.

    > [!NOTE]
    > Soovitame jätta selle suvandi väärtuseks **Ei**. Selle suvandi valikut kasutatakse kontrollimiseks ja juhtimiseks, et takistada suletud raamatu versiooni juhuslikku amortiseerimist. Kui hoiate suvandi väärtusel **Ei**, saate hoida raamatu netoväärtuse ja tulevased kulumiarvutused täpsena.
