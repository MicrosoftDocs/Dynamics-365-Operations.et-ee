---
title: Elektroonilise aruandluse hankija näidistšekid
description: Selles teemas antakse üldist teavet selle kohta, kuidas kasutada elektroonilise aruandluse tšekkide näidisvorminguid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 72581a6d852fe6eb5b4ad894027c1f5a3b5363e5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250598"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Elektroonilise aruandluse hankija näidistšekid

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) abil saab hankija tšekke vormindada. Turul on saadaval palju pangapõhiseid ja tšeki pakkuja põhiseid tšekivorminguid. Tšeki näidisvormingud on lisatud ER-i tööriistahoidla tšekimudelisse Makse. Need näidistšekid on märgistatud valikutega **Tšekk keskel (USA)** ja **Tšekk üleval, konts all (USA)**.

## <a name="what-check-formats-are-currently-supported"></a>Milliseid tšekivorminguid praegu toetatakse?

Saate alati minna teenuses Microsoft Dynamics Lifecycle Services (LCS) olevasse ühiste varade teeki ja vaadata ajakohast loendit saadaolevatest failidest, mille vara tüüp on **GER-i konfiguratsioon**. Järgmine jaotis „Mida pean seadistamiseks tegema?” sisaldab linki teema juurde, mis selgitab, kuidas luua LCS-hoidlat, et saadaolevaid konfiguratsioone üle vaadata ja valitud konfiguratsioone importida.

Microsoft Dynamics 365 Finance sisaldab ka näidisvormingut, kus tšekk on ülal ja sellele järgneb kaks ülekande jaotist. See sisaldab ka näidisvormingut, kus tšekk on keskel, kahe ülekande jaotise vahel. Need näidisvormingud vastavad Deluxe-tšekivormingutele.

## <a name="what-do-i-have-to-set-up"></a>Mida pean seadistamiseks tegema?

- Enne, kui saate ER-i abil tšekke printida, tuleb ER-i aruandluse konfiguratsioonidesse importida vähemalt üks aktiivne tšeki konfiguratsioon. Juhiste saamiseks vaadake teemat [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Kui konfigureerite pangakontole sularaha ja pangahalduse tšekke, siis märkige ruut **Üldine elektrooniline ekspordivorming** ja valige siis ekspordivormingu konfiguratsiooniks sobiv tšekivorming.
- Määrata tuleb ka ülekandele prinditavate kviitungiridade arv. Lisage selle numbri arvutamisel kindlasti päiseread. Kahe tšeki näidisvormingu puhul on soovitatav kviitungiridade arv 17. Kuid see arv erineb, olenevalt teie tšekivarudest ja printeridraiveritest.
- Soovitame printida tšeki paigutuse kontrollimiseks proovitšeki. Proovitšeki printimiseks valige suvand **Prindi proov**. Tšeki näidisvormingud toimivad kõige paremini, kui Microsoft Exceli täpsemates printeriatribuutides on suvandi **Veerised** sätteks on valitud **Puudub**. Kui tšekk on loodud, lubage Exceli väljundi redigeerimine ja konfigureerige lehe paigutus, nii et kõik veerised oleksid määratud väärtuseks **0** (null). Võrrelge tšekkide proovieksemplari oma tšekivarudega ja reguleerige sätteid, kuni olete joondusega rahul.
- Maksetöölehel konfigureeritud pangakontole maksete loomisel prinditakse tšekid, kasutades määratud vormingut.

Lisateavet leiate jaotisest [Elektroonilise aruandluse vormingu muutmine](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]