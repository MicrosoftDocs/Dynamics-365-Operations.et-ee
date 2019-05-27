---
title: Hoolduslepped
description: Hoolduslepetes saate määrata ressursid, mida kasutatakse tüüpilisel hoolduskülastusel, ning kuidas neid ressursse kliendiga arveldatakse.
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6425dcf1c89f625d997be0dd4a52aaecb6e6d65
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568277"
---
# <a name="service-agreements"></a>Hoolduslepped

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
