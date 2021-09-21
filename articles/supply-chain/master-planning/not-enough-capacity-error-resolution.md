---
title: Ajastamismootori tõrke 'Ei leitud piisavalt võimsust' lahendamine
description: Selles teemas antakse teavet tootmistellimuse põhjuste ja käskude %1 kohta, mida ei saa planeerida. Ajastamismootori tõrge ei leitud' pole piisav.
author: crytt
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 37c990067a0c175d93ecf298866041f4d2afc1bc
ms.sourcegitcommit: ab1455c67f6ee6ca36bec148bea0dbb0f7704eda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/26/2021
ms.locfileid: "7428921"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Ajastamismootori tõrke 'Ei leitud piisavalt võimsust' lahendamine

[!include [banner](../includes/banner.md)]

Ajakava koostamisel võite saada järgmise veateate:

> Tootmistellimust %1 ei saa plaanida. Piisavat võimsust ei leitud.

On mitu põhjust, miks planeerimismootor võib nurjuda ja väljastada selle tõrketeate. See teema annab juhised, mis aitavad teil leida tõrke juurpõhjuse ja seejärel selle leevendada.

## <a name="review-the-applicable-resources"></a>Rakendatavate ressursside ülevaatamine

Tõrge võib ilmneda, kui ükski rakendatav ressurss ei täida toimingu vajadusi tootmistellimuse saidil.

Selleks et vaadata läbi kohaldatavad ressursid, järgige neid samme.

1. Minge **tootmisjuhtimine \> tootmistellimused \> kõik tootmistellimused** ja avage või valige tootmistellimus, mida ei saa planeerida.
1. Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Tootmise üksikasjad** valik **Marsruut**.
1. Valige **tootmise marsruudil** lehel operatsioon ja seejärel valige tegevuspaanil **rakendatavad ressursid**.
1. Seadke dialoogiboksis **Rakendatavad ressursid** välja **Kasutusnõuded** väärtusele *Operatsioonide planeerimine* või *Tööde planeerimine* sõltuvalt kasutatavast planeerimistüübist.
1. Veenduge, et tootmistellimuse saidil on rakendatavad ressursid.

## <a name="review-the-calendars-that-are-associated-with-resources"></a>Vaadake üle kalender, mis on seotud ressurssidega

Tõrge võib ilmneda, kui ressursi ega ressursigrupiga pole seotud ühtegi kalendrit või kui seostatud kalender pole õigesti häälestatud (nt kalendril pole tööaegu või kui selle efektiivsus protsendina on 0 \[null\]).

Veenduge, et kalender on seostatud ressursi või ressursigrupiga, järgige neid samme.

1. Minge **tootmisjuhtimine \> tootmistellimused \> kõik tootmistellimused** ja avage või valige tootmistellimus, mida ei saa planeerida.
1. Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Tootmise üksikasjad** valik **Marsruut**.
1. Valige **tootmise marsruudil** lehel operatsioon ja seejärel valige tegevuspaanil **rakendatavad ressursid**.
1. Valige dialoogiboksis **Rakendatavad ressursid** ressurss ja seejärel valige suvand **Kuva ressurss**. Teise võimalusena valige ja hoidke all (või paremklõpsake) väljal **Ressursside grupp** ja valige käsk **Kuva üksikasjad**.
1. Veenduge, et kalender on seostatud **Ressursid** lehega või **Ressursigrupid** lehega **Kalendrid** vahekaardil.

> [!NOTE]
> Kui operatsioonide planeerimisel ilmneb tõrge, peate veenduma, et kalender on seotud kõigi rakendatavate ressursigruppidega.

Kalendri häälestuse ülevaatamiseks järgige neid samme.

1. Minge **organisatsiooni halduse \> Seadistus \> Kalendrid \> Kalendrid** ja valige kalender mis on seostatud ressursi või ressursigrupiga.
1. Valige tegevuste paanil käsk **Töö ajad**.
1. Veenduge **Tööajad** lehel, et see leht pole tühi. Lisaks veenduge teid huvitavate päevade puhul, et välja **Juhtelement** väärtuseks ei ole seatud *Suletud*, tööajad on olemas ja välja **Efektiivsus protsent** väärtuseks ei ole *0* (null).

Kui kalender on seotud põhikalendriga, peate ka läbi vaatama põhikalendri seadistuse.

> [!NOTE]
> Toimingute planeerimisel kasutatakse ressursirühma kalendrit iga toimingu algus- ja lõppaja määramiseks. Samuti piirab see ajalimiiti, mille süsteem saab ühe kindla operatsiooni jaoks planeerida ühe kindla päeva jaoks ühes ressursigrupis. Näiteks kui ressursigrupi tööajad konkreetsel päeval on kella 08.00–16.00, ei tohi ühe operatsiooni poolt ressursigrupile määratav koormus ületada koormust, mis võib olla sobiv kaheksaks tunniks, sõltumata ressursigrupi saadaolevast võimsusest. Olemasolev võimsus võib koormust siiski veelgi piirata.

## <a name="review-the-scheduling-parameters"></a>Ajakava parameetrite üle vaatamine

Hea jõudluse tagamiseks otsib planeerimismootor ressurssi ainult teatud aja jooksul ja teatud arvu planeerimiskonflikte.

Kalendri ajakava parameetrite üle vaatamiseks järgige neid samme.

1. Minge **Organisatsiooni haldus \> Seadistus \> Ajakava parameetrid**.
1. Järgige üht neist sammudest.

    - Kui **planeerimise ajalõpp on lubatud** atribuut on seatud väärtusele *Ei*, liikuge samm 3 juurde.
    - Kui **planeerimise ajalõpp on lubatud** on seatud väärtusele *Jah*, siis suurendage **maksimaalset planeerimisaega seeria** välja kohta et töötlemisele leida veel aega.

1. Järgige üht neist sammudest.

    - Kui **planeerimise optimeerimise aeg sisse lülitatud** atribuut on seatud väärtusele *Ei*, liikuge samm 4 juurde.
    - Kui **planeerimise optimeerimise ajalõpp on lubatud** on seatud väärtusele *Jah*, siis suurendage **optimeerimise katse ajastus** välja kohta, et töötlemisele leida veel aega.

1. Kui muutsite mõne lehe sätetest, planeerige tellimus uuesti.

## <a name="review-capacity"></a>Võimsuse ülevaade

Tõrge võib ilmneda, kui planeerite piiratud ajakava, kuid vaba võimsus puudub.

Piiramatu võimsuse planeerimise läbimiseks järgige neid samme.

1. Minge **tootmisjuhtimine \> tootmistellimused \> kõik tootmistellimused** ja valige või avage tootmistellimus, mida ei saa planeerida.
1. Valige Tegevuspaani vahekaardil **Ajagraafik** grupis **Tootmistellimused** suvand **Operatsioonide plaanimine** või **Planeeri tööd**.
1. Seadke dialoogiboksis **Operatsioonide planeerimine** või **Tööde planeerimine** suvandi **Piiratud võimsus** väärtuseks *Ei*.
1. Tellimuse planeerimiseks valige nupp **OK**.

Ressursi saadaoleva võimsuse ülevaatamiseks järgige neid samme.

1. Minge **Organisatsiooni haldus \> Ressursid \> Ressurssid** ja valige ressurss, mis on rakendatav tellimusele, mida ei saa planeerida.
1. Valige tegevuspaani vahekaardi **Ressurss** grupis **Vaade** suvand **Võimsuse koormus** või **Võimsuse koormus graafiliselt**  ja veenduge, et võimsus on olemas.

Ressursi grupi saadaoleva võimsuse ülevaatamiseks järgige neid samme.

1. Minge **Organisatsiooni haldus \> Ressursid \> Ressurssi grupid** ja valige ressursi grupp, mis on rakendatav tellimusele, mida ei saa planeerida.
1. Valige tegevuspaani vahekaardi **Ressursi grupp** vahekaart **Vaade** suvand **Võimsuse koormus** või **Võimsuse koormus graafiliselt** ja veenduge, et võimsus on olemas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
