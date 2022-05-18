---
title: Hoolduslepete arendamise ja sisseseadmise ülevaade
description: Hoolduslepetes saate määrata ressursid, mida kasutatakse tüüpilisel hoolduskülastusel, ning kuidas neid ressursse kliendiga arveldatakse.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 559f4571a60ea8ec048b291e3b6a0a93e8bc9d44
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677698"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Hoolduslepete arendamise ja sisseseadmise ülevaade

[!include [banner](../includes/banner.md)]

Hoolduslepetes saate määrata ressursid, mida kasutatakse tüüpilisel hoolduskülastusel, ning kuidas neid ressursse kliendiga arveldatakse.

Iga hoolduslepe on lisatud projekti juurde, mille kaudu kanded sisestatakse ja arveldatakse. Te saate siiski ka arveldada hooldustellimuste kandeid vahetult projekti kaudu, ilma et ühendaksite hooldustellimuse esmalt hooldusleppega. Võite otsustada toimida nii juhul, kui hooldustellimus on ühekordne hoolduskülastus ning hoolduskannete töötlemise vajadus kaalub kiiresti üles klienti puudutava üksikasjaliku hooldusleppe teabe haldamise ajaperioodil.

## <a name="service-agreement"></a>Teenuseleping

Igas hooldusleppes peate määrama projekti, hooldusleppe ID ja hooldusleppegrupi. Hooldusleppegruppi saab kasutada hoolduslepete sortimiseks ja korraldamiseks.

Hooldusleppe päis hõlmab järgmiseid sätteid, mis kehtivad kõikide lisatud lepinguridade puhul.

-  Kas hoolduslepe on peatatud. Kui hoolduslepe on peatatud, ei saa hooldusleppest hooldustellimusi luua.
-  teenuselepingu kestus;
-  kuidas teenusetellimuste ridu teenusetellimustesse ühendada;
-  Kas hoolduslepe on mall.

Hooldusleppe päises saate seadistada ka kõik hooldusobjektid ja hooldustoimingud, mida saab hooldusleppe raames kasutada, sisestades kindlad hooldustoiminguid või hooldusobjektid, mis seotakse leppe eri ridadega.

Hooldusleppe päisest saate ka kopeerida hooldusleppe read või hooldusmalli read praegusesse hooldusleppesse.

Võite peatada hoolduslepped ja lõpetada individuaalsed hooldusleppe read.

Kui valite märkeruudu **Peatatud** hooldustellimuse real, ei saa te teha järgmist.

-    Luua hooldusleppest automaatselt või käsitsi hooldustellimusi.

Kui valite märkeruudu **Seisatud** hooldustellimuse real, ei saa te teha järgmist.

-    Luua hooldusleppe reast automaatselt või käsitsi hooldustellimusi.
-    kopeerida teenusetellimuse rea teise teenuselepingusse või teenusetellimusse.


> [!NOTE]
> Kui hoolduslepe on peatatud, lõpetatakse kõik seotud read hoolimata nende individuaalsest olekust.

## <a name="service-agreement-lines"></a>Hooldusleppe read

Iga hooldusleppe rida kirjeldab üksikasjalikult kavandatava hooldustöö sisu. Need read hõlmavad järgmisi sätteid.

-  Kandetüüp ja kandetüübi kirjeldus;
-  töötaja, kes teeb teenusetöid;
-  objektid, millel tuleb teenuselepingu alusel teenust teha;
-  sagedus, mil töö tehakse ning registreeritakse kaup, kulu ja tasukanded;
-  Kellaaja aken, mille ajal saab hooldustellimuste ridu grupeerida hooldustellimusse.
-  Hooldustoimingud, mida kasutatakse lepperidade komplektide grupeerimiseks tööülesannetesse ning hooldustehnikutele ja klientidele kokkuvõtlikult kirjeldamiseks, millist hooldustoimingut läbi viia.
-  Kas rida peatatakse. Kui rida peatatakse, ei saa te sellele üksikreale hooldustellimusi luua.
-  Projektisätted, nt kategooria ja rea atribuut.

## <a name="related-topics"></a>Seotud teemad

[Hoolduslepete loomine](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]