---
title: Parandage plaanimismootori tõrge ja piiratud võimsus, et ei leitud piisavalt võimsust
description: See artikkel annab teavet põhjuste ja lahenduste kohta, mida ei saanud %1 tootmistellimusele planeerida. Ajastamismootori tõrge ei leitud' pole piisav.
author: t-benebo
ms.date: 7/29/2021
ms.topic: article
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4f54c06a07b3cdd0b8fe2cc52614189ff31ba7f
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135595"
---
# <a name="fix-the-not-enough-capacity-could-be-found-scheduling-engine-error"></a>Ajastamismootori tõrke 'Ei leitud piisavalt võimsust' lahendamine

[!include [banner](../includes/banner.md)]

Ajakava koostamisel võite saada järgmise veateate:

> Tootmistellimust %1 ei saa plaanida. Piisavat võimsust ei leitud.

On mitu põhjust, miks planeerimismootor võib nurjuda ja väljastada selle tõrketeate. See artikkel annab juhised, mis aitavad teil leida tõrke juurpõhjuse ja seejärel selle leevendada.

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

Tõrge võib ilmneda, kui planeerite piiratud, kuid vaba võimsus puudub.

Piiramatu võimsuse planeerimise läbimiseks järgige neid samme.

1. Minge **tootmisjuhtimine \> tootmistellimused \> kõik tootmistellimused** ja valige või avage tootmistellimus, mida ei saa planeerida.
1. Valige Tegevuspaani vahekaardil **Ajagraafik** grupis **Tootmistellimused** suvand **Operatsioonide plaanimine** või **Planeeri tööd**.
1. Seadke dialoogiboksis **Operatsioonide planeerimine** või **Tööde planeerimine** suvandi **Piiratud võimsus** väärtuseks *Ei*.
1. Tellimuse planeerimiseks valige nupp **OK**.

Ressursi saadaoleva võimsuse ülevaatamiseks järgige neid samme.

1. Minge **Organisatsiooni haldus \> Ressursid \> Ressurssid** ja valige ressurss, mis on rakendatav tellimusele, mida ei saa planeerida.
1. Valige tegevuspaani vahekaardi **Ressurss** **·** **grupis Vaade suvand Võimsuse koormus või Võimsuse koormus graafiliselt ja veenduge,** et võimsus on olemas.**·**

Ressursi grupi saadaoleva võimsuse ülevaatamiseks järgige neid samme.

1. Minge **Organisatsiooni haldus \> Ressursid \> Ressurssi grupid** ja valige ressursi grupp, mis on rakendatav tellimusele, mida ei saa planeerida.
1. Valige **tegevuspaani** **·** **·** **vahekaardi Ressursigrupp jaotises Vaade suvand Võimsuse koormus või Võimsuse koormus graafiliselt ja veenduge,** et võimsus on olemas.

## <a name="master-planning-books-a-resource-when-the-resource-calendar-is-closed"></a>Koondplaneerimisel plaanitakse ressurss, kui ressursikalender on suletud.

Operatsioonide planeerimisel planeerib koondplaneerimine võimsust vastavalt esmase ressursigrupi kalendrile. See raamatutab teisese operatsiooni esmase operatsiooniga samaaegselt ega võta arvesse teisese operatsiooni kalendreid ega võimsusi. Selle tulemuseks võib olla tootmistellimuse plaanimine suletud kalendris või ajal, mil teisene operatsioon ei ole saadaval (kalender suletud, võimsus puudub).

Tööde planeerimisel võtab koondplaneerimine arvesse tellimuse planeerimisel esmase ja teisese operatsiooni võimsust ja kalendrit. Tellimuse plaanimiseks peavad mõlema operatsiooni ressursside kalendrid olema avatud ja vaba võimsusega.

## <a name="maximum-job-lead-time-is-too-short"></a>Maksimaalne töö täitmisaeg on liiga lühike.

Planeerimismootor ei saa **tellimust** planeerida, kui saidi maksimaalne töö täitmisaeg on väiksem kui kaubale määratud täitmisaeg tellimuse vaikesätetes või laovarude sätetes.

Oma saidi maksimaalse töö täitmisaja **sätte** vaatamiseks või redigeerimiseks minge Tootmise **juhtimise \> seadistuse \> tootmise juhtimise parameetritesse** ja avage **vahekaart** Üldine.

Kauba tellimuse vaikesätete vaatamiseks või redigeerimiseks järgige neid samme:

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige loendist vastav toode.
1. Tegevuspaanil avage vahekaart **Halda varusid** ja valige tellimuse **vaikesätted**.
1. Laiendage **lao** kiirkaarti ja vaadake või redigeerige varude **täitmisaja** sätet vastavalt vajadusele.

Kauba laovarude sätete vaatamiseks või redigeerimiseks järgige neid samme:

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige loendist vastav toode.
1. Tegevuspaanil avage vahekaart **Plaan ja** valige kauba **laovarud**.
1. Avage vahekaart **Täitmisaeg** ja vaadake või redigeerige **tootmise aja** väärtust vastavalt vajadusele.

## <a name="excessive-quantity-of-required-resources"></a>Vajalike ressursside üleliigne kogus

Planeerimise ajal püüab mootor vastavalt toimingu ressursinõuetele vastendada protsessi operatsiooni jaoks seatud nõutud ressursikogust kohaldatavate ressurssidega. Liiga kõrge ressursikoguse seadistamine võib põhjustada marsruudi ebatõhususe, mis toob kaasa planeerimisvea.

Kasutage järgmist protseduuri, et kontrollida nii määratud kogust kui ka rakendatavaid ressursse valitud toote, protsessi ja protsessi operatsiooni puhul:

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige ruudustikust vastav toode.
1. Tegevuspaanil avage vahekaart **Insener** ja valige **protsess**.
1. Otsige ja valige ruudustikust vastav protsess.
1. Avage lehe **allosas** olevale vahekaardile Ülevaade.
1. Valige operatsioon valitud protsessi operatsioonide loendist.
1. Valige **rakendatavad** ressursid dialoogi avamiseks, kus saate vaadata valitud protsessi operatsioonile rakendatavaid ressursse.
1. Avage vahekaart **Ressursi** koormus. Sellel **väljal** Kogus kuvatakse valitud protsessitoimingu jaoks vajalik ressursikogus. Vaadake ja/või redigeerige seda vastavalt vajadusele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
