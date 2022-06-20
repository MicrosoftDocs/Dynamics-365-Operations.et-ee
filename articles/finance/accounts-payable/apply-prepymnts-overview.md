---
title: Rakendage ettemaksu automaatselt hankija arvetele
description: See artikkel kirjeldab hankija arvetele ettemaksete automaatse rakendamise võimalusi.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 547573d187460a900df7f4927ac062bd9d456729
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900067"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Rakendage automaatselt hankija arvetele

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab hankija arvetele ettemaksete automaatse rakendamise võimalusi. Ostutellimuse jaoks saab ettemakse luua osana ostulepingust. Pärast hankija arve saamist saab ettemakset kasutada ostureskontro tasakaalustamiseks hankija arvelt. Uus funktsioon võimaldab süsteemil automaatselt kasutada hankija arvel ostutellimuse numbreid, et otsida vastavaid ettemakseid, kui hankija arve on imporditud.

Kui ettemaksed leitakse ja neid saab rakendada, lisatakse ettemaksete rakendamiseks olemasolevatele arveridadele read. Ettemakse ridu ei loeta arvete vastavusse viimise protsessi ajal kunagi arvesse.

Järgmised punktid kirjeldavad, kuidas ettemakseid erinevate ostuprotsesside puhul rakendatakse:

- **Üks hankija arve ostutellimuse kohta** – ostutellimuse ettemakse rakendatakse hankija arvele.
- **Üks hankija arve mitme ostutellimuse kohta** – kõigi ostutellimuse ettemaksed rakendatakse hankija arvele.
- **Mitu hankija arvet ostutellimuse kohta** – ostutellimuse ettemakse esimesele imporditud hankijaarvele. Kui ettemaksusumma ületab arve summa, siis ettemaksu avaldus nurjub ja te peate ettemakse käsitsi rakendama.
- **Mitu hankija arvet ostutellimuse kohta** – ostutellimuse ettemakse esimesele imporditud hankijaarvele. Kui ettemaksusumma ületab arve summa, siis ettemaksu avaldus nurjub ja te peate ettemakse käsitsi rakendama. Kui esimesele arvele rakendatakse ettemakse järel jäävad ettemaksed, saab neid rakendada järgnevatele arvetele.

Kui ettemakse rakendamise katse nurjub, **määrab** ettemakse avalduse nurjumise korral järeltegevuse automatiseerimisprotsessi säte järgmised sammud.

- **Jah** - automatiseerimise ajaloosse lisatakse tõrketeade "Automaatne ettemakse rakendamine: nurjus" ja arve jääb ootel hankijaarvete loendisse. Arve jääb blokeerituks kuni ettemakse käsitsi rakendumiseni.

Ettemaksete käsitsi rakendamiseks minge ootel hankijaarvele. Lehel **Arve üksikasjad** seadistage blokeeritud arve puhul suvand **Kaasa automatiseeritud töötlemisse** väärtusele **Ei**. Nüüd saate ettemakse käsitsi rakendada. Pärast ettemakse rakendamist määrake valik **Kaasa automatiseeritud töötlemisse** tagasi suvandile **Jah** et arvet saaks automaatselt töödelda.

Samuti võite mööduda ettemakse automaatsest rakendamisest, seades **Kaasa automatiseeritud töötlemisse** suvandi valikule **Ei** ja määrates selle tagasi väärtusele **Jah**. Saate järgmise teate: "Ostutellimuse jaoks on ettemakse juba olemas. Kas soovite seda valitud hankijaarve puhul ignoreerida?" Valige **Jah**. Sõnum "Käsitsi vahele eiratud ettemakse rakendamine" lisatakse automatiseerimise ajalukku ja hankija arvet ei blokeerita, kui automatiseeritud protsess uuesti käivitub.

- **Ei** – järeltegevuse automatiseerimisprotsessid jätkuvad. Te saate ettemakset siiski tasakaalustuse ajal rakendada.
