---
title: Rentimise parameetrite konfigureerimine (eelversioon)
description: See teema kirjeldab varade rentimise konfiguratsiooni seadistusi, nagu turbeteave ja raamatupidamise sätteid.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a644b3c9d9ed4fc86a816af1ab338b96b1aa7ad
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968073"
---
# <a name="configure-lease-parameters"></a>Rentimise parameetrite konfigureerimine

[!include [banner](../includes/banner.md)]

Varade rentimise käitumist mõjutavad mitu konfiguratsiooni sätet. Need sätted hõlmavad töölehe nimesid, üldisi parameetreid ja sisestusreeglite sätteid.

1. Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.
2. Valige vahekaardil **Rendikirjed** kiirkaart **Üldine**.

    Parameeter **Luba käsitsi klassifitseerimise alistamise** määratleb, kas rendi klassifikatsiooni saab alistada enne maksegraafiku kinnitamist.

    Ristüksuse **partii** parameeter määrab, kas saate sisestada praeguse juriidilise isiku teistele juriidilistele isikutele. Kui see parameeter on sisse lülitatud, saate luua töölehe kandeid juriidilistele isikutele, millele teil on juurdepääs.

3. Kui soovite **lubada kinnitatud rendide kustutamise, valige suvand** **Jah**, et lubada rendid, mille maksegraafikud on kinnitatud, kustutada. Rendikirjeid saab kustutada, kui nendega on seostatud sisestatud või sisestamata kanded, olenemata selle valiku sättest. Rendikirjet ei saa pärast kustutamist taastada. Kui laadite mõne kustutatud rendikirjetest (käsitsi või andmeolemite), käsitletakse üleslaaditud teavet uuena, mitte olemasoleva rendikirje värskendusena.

    Kui valite selle suvandi väärtuseks **Jah** ja raamatu kande tüüp on **Kumulatiivse järelkulu valik A või B**, määrab süsteem välja **Alternatiivne laenuintressimäär** suvandi **Ülemineku alternatiivne laenuintressimäär** väärtuseks **Raamatu häälestus**. Kui selle suvandi väärtuseks on määratud **Ei**, seatakse põhirendi määr välja **Alternatiivne laenuintressimäär** väärtusele lehel **Raamatu üksikasjad**, sõltumata raamatu ülekande tüübist.

4. Seadke suvand **Luba kulumi tagasipööramine suletud raamatus** valikule **Jah**, et lubada kulumi kulukannete stornmist. Kulukanded saab pöörata ümber isegi siis, kui raamatu versioon on suletud.

    > [!NOTE]
    > Soovitame jätta selle suvandi väärtuseks **Ei**. Selle suvandi valikut kasutatakse kontrollimiseks ja juhtimiseks, et takistada suletud raamatu versiooni juhuslikku amortiseerimist. Kui hoiate suvandi väärtusel **Ei**, saate hoida raamatu netoväärtuse ja tulevased kulumiarvutused täpsena.

5. Seadke valik Luba maksesumma jaotus valikule Jah, et lubada maksesummade liigendust **rendilehe** **·** **maksegraafiku** ridade **kiirkaardil**. Maksejaotuse tüübid määratletakse **seadistuse** lehel **Makse summa** tüübid. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
