---
title: Rakendage ettemaksu automaatselt hankija arvetele
description: Selles teemas kirjeldatakse hankija arvetele ettemaksete automaatse rakendamise võimalust.
author: sunfzam
ms.date: 10/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: b1ea73a50f5adaa1a00c9ddfa8c983375e0d47be
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675721"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Rakendage automaatselt hankija arvetele

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse hankija arvetele ettemaksete automaatse rakendamise võimalust. Ostutellimuse jaoks saab ettemakse luua osana ostulepingust. Pärast hankija arve saamist saab ettemakset kasutada ostureskontro tasakaalustamiseks hankija arvelt. Uus funktsioon võimaldab süsteemil automaatselt kasutada hankija arvel ostutellimuse numbreid, et otsida vastavaid ettemakseid, kui hankija arve on imporditud.

Kui ettemaksed leitakse ja neid saab rakendada, lisatakse ettemaksete rakendamiseks olemasolevatele arveridadele read. Ettemakse ridu ei loeta arvete vastavusse viimise protsessi ajal kunagi arvesse.

Järgmised punktid kirjeldavad, kuidas ettemakseid erinevate ostuprotsesside puhul rakendatakse:

- **Üks hankija arve ostutellimuse kohta** – ostutellimuse ettemakse rakendatakse hankija arvele.
- **Üks hankija arve mitme ostutellimuse kohta** – kõigi ostutellimuse ettemaksed rakendatakse hankija arvele.
- **Mitu hankija arvet ostutellimuse kohta** – ostutellimuse ettemakse esimesele imporditud hankijaarvele. Kui ettemaksusumma ületab arve summa, siis ettemaksu avaldus nurjub ja te peate ettemakse käsitsi rakendama.
- **Mitu hankija arvet ostutellimuse kohta** – ostutellimuse ettemakse esimesele imporditud hankijaarvele. Kui ettemaksusumma ületab arve summa, siis ettemaksu avaldus nurjub ja te peate ettemakse käsitsi rakendama. Kui esimesele arvele rakendatakse ettemakse järel jäävad ettemaksed, saab neid rakendada järgnevatele arvetele.

Kui süsteem püüab ettemakset rakendada, kuid rakendus nurjub, sõltub käitumine sättest **järeltegevuse automatiseerimisprotsessi ettemakse avalduse nurjumise** suvandist:

- **Jah** - automatiseerimise ajaloosse lisatakse tõrketeade "Automaatne ettemakse rakendamine: nurjus" ja arve jääb ootel hankijaarvete loendisse. Arve jääb blokeerituks kuni ettemakse käsitsi rakendumiseni.

    Ettemaksete käsitsi rakendamiseks minge ootel hankijaarvele. Lehel **Arve üksikasjad** seadistage blokeeritud arve puhul suvand **Kaasa automatiseeritud töötlemisse** väärtusele **Ei**. Nüüd saate ettemakse käsitsi rakendada. Pärast ettemakse rakendamist määrake valik **Kaasa automatiseeritud töötlemisse** tagasi suvandile **Jah** et arvet saaks automaatselt töödelda.

    Samuti võite mööduda ettemakse automaatsest rakendamisest, seades **Kaasa automatiseeritud töötlemisse** suvandi valikule **Ei** ja määrates selle tagasi väärtusele **Jah**. Saate järgmise teate: "Ostutellimuse jaoks on ettemakse juba olemas. Kas soovite seda valitud hankijaarve puhul ignoreerida?" Valige **Jah**. Sõnum "Käsitsi vahele eiratud ettemakse rakendamine" lisatakse automatiseerimise ajalukku ja hankija arvet ei blokeerita, kui automatiseeritud protsess uuesti käivitub.

- **Ei** – järeltegevuse automatiseerimisprotsessid jätkuvad. Te saate ettemakset siiski tasakaalustuse ajal rakendada.
