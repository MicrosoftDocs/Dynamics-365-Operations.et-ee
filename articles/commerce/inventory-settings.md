---
title: Varude sätete rakendamine
description: See teema hõlmab varude sätteid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce rakendada.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7fc81c190806a0bdb50569f526589cfa1808ce0c
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417434"
---
# <a name="apply-inventory-settings"></a>Varude sätete rakendamine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab varude sätteid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce rakendada.

## <a name="overview"></a>Ülevaade

Varude sätted määratlevad, kas varusid tuleks enne toodete ostukorvi lisamist kontrollida. Samuti määratletakse nende abil varudega seotud kaubandusteated, nagu näiteks „Olemas“ ja „Ainult mõni alles“. Need sätted tagavad, et toodet ei saa soetada, kui see on laost otsas.

Dynamics 365 Commerce annab vabade toodete saadavuse hinnangu. Lisateavet vabade varude saadavuse hinnangu arvutamise kohta vt teemast [Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md).

Commerce'i saidiehitajas saab määratleda toote või kategooria varude künnised ja vahemikud. Need määratlevad, kas varude liigituseks on „olemas“, „madal varu“ või „laost otsas“. Lisateavet vt teemast [Varude puhvrite ja varude tasemete konfigureerimine](inventory-buffers-levels.md).

## <a name="inventory-settings"></a>Varude sätted

Commerce'is määratletakse varude sätted saidiehitajas jaotises **Saidi sätted \> Laiendused \> Varude haldus**. On neli varude sätet, millest üks on aegunud.

- **Luba rakenduses varude kontrollimine** – see säte lülitab sisse tootevarude kontrollimise võimaluse. Seejärel kontrollitakse moodulite ostukast, ostukorv ja poodi järeletulemine raames tootevarusid ja lubatakse lisada toode ostukorvi vaid siis, kui vastavad varud on saadaval.
- **Varude taseme alus** – see säte määratleb, kuidas arvutatakse varude tasemeid. Saadaolevad väärtused on **Kokku saadaval**, **Füüsiliselt saadaval** ja **Laost otsas künnis**. Commerce'i saidiehitajas saab määratleda iga toote või kategooria varude künnise ja vahemikud. Varude API-d hangivad toote varusid puudutavat teavet nii **Kokku saadaval** atribuudi kui ka **Füüsiliselt saadaval** atribuudi kohta. Jaemüüja otsustab, kas varude arvu ja vastavate olemas ja laost otsas vahemike määramiseks tuleks kasutada väärtust **Kokku saadaval** või **Füüsiliselt saadaval**.

    Sätte **Varude taseme alus** väärtus **Laost otsas künnis** on vana (pärand), aegunud väärtus. Selle valimisel määratakse varude arv väärtuse **Kokku saadaval** tulemuste alusel, kuid künnis määratletakse hiljem kirjeldatava numbrilise sätte **Laost otsas künnis** alusel. See künnis kehtib kõikidele toodetele kogu e-kaubanduse saidil. Kui varud jäävad alla künnise numbri, siis arvatakse toode olevat laost otsas. Vastasel juhul on toode aga olemas. Väärtuse **Laost otsas künnis** võimalused on piiratud ja me ei soovita seda kasutada versioonis 10.0.12 ega hilisemates versioonides.

- **Varude vahemikud** – säte määratleb varude vahemikud, mille kohta kuvatakse saidi moodulites teade. See on kohaldatav vaid juhul, kui sätte **Varude taseme alus** jaoks valitakse väärtus **Kokku saadaval** või väärtus **Füüsiliselt saadaval**. Saadaolevad väärtused on **Kõik**, **Varud madalad ja laost otsas** ja **Laost otsas**.

    - Suvandi **Kõik** valimisel kuvatakse kõik varude vahemikud, alates olemasolevast (teade „olemas“) ja lõpetades väärtusega laost otsas (teade „Laost otsas“).
    - Suvandi **Varud madalad ja laost otsas** valimisel kuvatakse kõik varude vahemikud, v.a väärtus olemasolev (teade „olemas“).
    - Suvandi **Laost otsas** valimisel kuvatakse ainult teade „Laost otsas“.

- **Laost otsas künnis** – see vana numbrisäte jõustub ainult siis, kui sätte **Varude taseme alus** jaoks valitakse väärtus **Laost otsas künnis**.

## <a name="modules-that-use-inventory-settings"></a>Varude sätteid kasutavad moodulid

Ostukasti, soovinimekirja, kaupluse valija, ostukorvi ja ostukorvi ikooni moodulid kasutavad varude sätteid varude vahemike ja teadete kuvamiseks.

Järgmisel pildil on toodud toodete üksikasjade lehe näide, kus kuvatakse teadet laos olemas („Olemas“).

![Laos olemas teadet kuvava toote üksikasjade lehe mooduli näide](./media/pdp-InStock.png)

Järgmisel pildil on toodud toodete üksikasjade lehe näide, kus kuvatakse teadet laost otsas („Laost otsas“).

![Laost otsas teadet kuvava toote üksikasjade lehe mooduli näide](./media/pdp-outofstock.png)

Järgmisel pildil on toodud ostukorvi näide, kus kuvatakse teadet laos olemas („Olemas“).

![Laos olemas teadet kuvava ostukorvi mooduli näide](./media/cart-instock.png)

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Varude puhvrite ja varude tasemete konfigureerimine](inventory-buffers-levels.md)

[Ostukorvimoodul](add-cart-module.md)

[Ostukasti moodul](add-buy-box.md)

[Kontohalduse lehed ja moodulid](account-management.md)

[Kaupluse valimise moodul](store-selector.md)
