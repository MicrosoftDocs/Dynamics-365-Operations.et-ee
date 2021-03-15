---
title: Tarbimise kulum
description: Selles artiklis antakse ülevaade kulumi tarbimismeetodist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e78e2481724aede93ecb997d95a0ef8032618bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989023"
---
# <a name="consumption-depreciation"></a>Tarbimise kulum

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade kulumi tarbimismeetodist.

Kui valite põhivara kulumireeglid ja teete valiku **Tarbimine** väljal **Meetod** lehel **Kulumireeglid**, määratakse põhivara kulumireeglitele kasutuse põhjal. Lehel **Kulumireeglid** pole vaja protsente ega intervalle seadistada. Pärast meetodit Tarbimine kasutavate kulumireeglite loomist on meetodi seadistamiseks mitmesuguseid võimalusi.

## <a name="set-up-and-use-consumption-depreciation"></a>Tarbimiskulumi seadistamine ja kasutamine
1.  Looge lehel **Kulumireeglid** kulumireeglid. Tarbimise arvutuste sooritamiseks peab kulumiarvestusreeglil olema ID, nimi ja valitud peab olema **Tarbimine** väljal **Meetod**.
2.  Seadistage lehel **Tarbimistegurid** tarbimistegurid. Igal tarbimisteguril peab olema ID, nimi ja tarbimistegur, mis on määratud koguse või protsendina.
3.  Seadistage lehel **Tarbimisühikud** tarbimisühikud. Igal tarbimisühikul peab olema ID ja nimi. Kulumiühikuid kasutatakse tarbimise kulumi arvutamiseks lehel **Tarbimise kulum**. Ühikuteks on näiteks kilomeeter (km), kilogramm (kg) ja tund.
4.  Seadistage lehel **Põhivara** eraldi põhivarad. Valige iga põhivara puhul väärtusmudelid ja kulumiraamatud, millel on kulumireeglid. Peate seadistama tarbimiskulumi jaoks väärtusmudelid või kulumiraamatud, kui mõni põhivara kasutab meetodil Tarbimine põhinevaid kulumireegleid. See seadistamine toimub kas vahekaardil **Kulum** lehel **Väärtusmudelid** või kiirkaardil **Üldine** lehel **Kulumireeglid**. Sama väärtusmudelit saab kasutada mitme põhivara puhul. Kulumireeglid on iga põhivara jaoks valitava väärtusmudeli või kulumiraamatu osa. Kulumireegleid ei saa otse lehel **Põhivara** lisada ega muuta. Kulumireegleid saab muuta ainult lehel **Kulumiraamatud**.
5.  Sisestage lehel **Väärtusmudelid** või lehel **Kulumiraamatud** väljagrupis **Tarbimise kulum** teave järgmistele väljadele.
    -   Tarbimistegur
    -   Ühik
    -   Ühikukulum
    -   Eeldatav tarbimine

    Väljal **Sisestatud tarbimine** kuvatakse põhivara väärtusmudeli või kulumiraamatu puhul juba sisestatud tarbimiskulum määratud ühikutes. Selle välja väärtust ei saa käsitsi värskendada.

## <a name="examples"></a>Näited
### <a name="example-1"></a>Näide 1

31. jaanuari jaoks on seadistatud järgmine tarbimistegur:

-   Kogus on 1000.
-   Põhivarale määratud ühikukulumi väärtus on 1,5.

Kulumisoovitus on 31. jaanuaril järgmine: kogus × ühikukulum 1000 × 1,5 = 1500 Kui põhivarale määratud tegur on protsenditegur, korrutatakse kogust, mis on prognoositud põhivara väärtusmudelile väljal **Eeldatav tarbimine**, valitud lõppkuupäeva jaoks seadistatud protsendiga. Saadud kogus pakutakse seejärel välja perioodi kulumikogusena.

### <a name="example-2"></a>Näide 2

Järgmine tarbimiskulumi tegur on seadistatud 31. jaanuari jaoks:

-   protsendimäär on 10.
-   Põhivarale määratud ühikukulumi väärtus on 1,5.
-   Eeldatav põhivara kogus on 2000.

Kulumisoovitus on 31. jaanuaril järgmine: hinnanguline kogus × protsent × ühikukulum 2000 × 0,10 × 1,5 = 300





[!INCLUDE[footer-include](../../includes/footer-banner.md)]