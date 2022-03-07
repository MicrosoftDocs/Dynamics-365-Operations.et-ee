---
title: Atribuudipõhised müügihinnad piirangupõhistele tootekonfiguratsioonidele
description: Selles teemas kirjeldatakse, kuidas luua müügihinna mudeleid müügihindadega, mis põhinevad komponentidel ja atribuutidel, mitte füüsilisel kooslusel ja protsessil.
author: t-benebo
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e50b2d1e9ccf03a58e0ddf6d4ecfb34c6c504161
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577452"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Atribuudipõhised müügihinnad piirangupõhistele tootekonfiguratsioonidele

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua müügihinna mudeleid müügihindadega, mis põhinevad komponentidel ja atribuutidel, mitte füüsilisel kooslusel ja protsessil. Igale tootekonfiguratsiooni mudelile saate luua mitu müügihinna mudelit.

## <a name="set-relevant-product-information-management-parameters"></a>Asjakohaste tooteteabe halduse parameetrite seadmine

Enne kui alustate oma hinnamudelite loomist, peate määratlema vaikevaluuta, mida kasutatakse müügihinna mudelite loomisel. Samuti saate valida, kas lisada Microsoft Exceli fail, milles on kõikide tellimuse või pakkumise ridade hinnajaotus. Hinnajaotus võimaldab teil jagada üksikasju klientidega selle kohta, kuidas te arvutasite konfigureeritud toote jaoks kindla müügihinna.

Vaikevaluuta seadistamiseks tehke järgmist.

1. Avage **Tooteteabe haldus \> Seadistus \> Tooteteabe halduse parameetrid**.
1. Avage vahekaart **Piirangupõhise tootekonfiguratsiooni mudelid**.
1. Avage ripploend **Vaikevaluuta** ja valige valuuta.

    ![Vaikevaluuta seadmine piirangupõhise tootekonfiguratsiooni jaoks.](media/prod-config-currency.png "Vaikevaluuta seadmine piirangupõhise tootekonfiguratsiooni jaoks")

1. Kui soovite lisada kõigi tellimuse või pakkumise ridade hinnajaotusega Exceli faili, siis seadke jaotises **Hinnamudel** suvandi **Manusta** väärtuseks *Jah*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Müügihinna mudelite loomine

Müügihinna mudeli loomiseks tehke järgmist.

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Valige sobiv tootekonfiguratsiooni mudel.
1. Valige toimingupaanil vahekaart **Mudel** ning valige rühmas **Seadistamine** suvand **Hinnamudelid**.
1. Avaneb leht **Hinnamudelid**.
1. Valige hinnamudel või lisage ruudustikku uus.
1. Valige **Redigeeri**, et avada valitud mudeli jaoks redigeerimisleht, mis sisaldab järgmisi funktsioone.
    - Vormi päises kuvatakse vaikevaluuta ja seal saate oma hinna seadistamiseks lisada uusi valuutasid.
    - Vasakpoolne paan näitab kõiki tootemudeli komponente ja kasutajanõudeid. Igal tootemudeli puu sõlmel võib olla üks baashinna avaldis ja ükskõik kui palju avaldisereegleid. Avaldisereegel koosneb tingimusest ja avaldisest ning iga avaldisereegel hõlmab tootesuvandit, mis aitab reguleerida toote hinda.
    - Kui koostate oma tingimused ja avaldised, saate kasutada samu tehtemärke, mis on saadaval tootemudeli arvutuste jaoks. Avaldiseredaktor toetab nii tingimusi kui ka avaldisi.
1. Valige vasakus veerus sõlm ja kasutage seejärel eelmises sammus kirjeldatud funktsioone, et luua selle jaoks hinnakujunduse reeglid (vt ka pärast seda toimingut toodud näidet). Korrake seda sammu vajaduse järgi iga sõlme puhul.

Järgmises näites on toodud baashind 899,95 eurot staatilise arvuna, mida saab muuta ühe või mitme järgmise viie avaldisereegliga sõltuvalt kliendi valitud konfiguratsioonist.

- Valge korpuse puhul lahutage 59,95 eurot.
- Nurgakaitsete puhul lisage 35,95 eurot.
- Metallist eesvõre puhul lisage 89,95 eurot.
- Puitu imiteeriva korpuse puhul lisage 119,95 eurot.
- Lisage 12,95 eurot iga kõlari kõrguse ühiku kohta.

![Näidishinnamudel.](media/prod-config-rules-example.png "Näidishinnamudel")

## <a name="add-support-for-multiple-currencies"></a>Mitme valuuta toe lisamine

Konfigureeritava toote müümise korral kontrollib süsteem, kas hinnad on seadistatud otse kliendi valuutas. Kui jah, siis kasutatakse otseseid väärtusi. Kui mitte, kasutab süsteem selle ettevõtte jaoks määratud valuutakursse, et teisendada vaikevaluutas väärtus kliendi valuutasse.

Otseste hindade lisamiseks lisavaluutas tehke järgmist.

1. Avage oma hinnamudeli jaoks redigeerimisleht, nagu on kirjeldatud jaotises [Müügihinna mudelite loomine](#build-price-model).
1. Valige hinnamudeli päises nupp **Lisa**, et avada rippdialoogiboks **Valuutad**, kus on loetletud saadaolevad valuutad.
1. Valige rippdialoogiboksis **Valuutad** valuuta, mille soovite lisada, ja seejärel valige **OK**.
1. Ripploend **Praegune valuuta** sisaldab nüüd äsja lisatud valuutat ning kõiki muid valuutasid, mis võisid olla varem lisatud. Valige uus valuuta ja pange tähele, et jaotises **Avaldisereeglid** olev ruudustik sisaldab nüüd kaht avaldisevälja.
    - **Avaldis** – näitab hinna otsimiseks kasutatavat avaldist (või püsiväärtust), kasutades praegust valuutat, mis valiti suvandis **Praegune valuuta**.
    - **Vaikeavaldised** – näitab hinna otsimiseks kasutatavat avaldist (või püsiväärtust), kasutades vaikevaluutat (kuvatud väljal **Vaikevaluuta**).

    > [!NOTE]
    > Avaldisereeglite välja **Tingimus** „omanik” on vaikevaluuta, mis tähendab, et te ei saa muuta tingimust teistes valuutades. Samuti ei saa te lisada uusi avaldisereegleid, kui praegu on valitud valuuta, mis ei ole valitud suvandis **Praegune valuuta**.
1. Redigeerige veerus **Avaldis** olevaid väärtusi praeguse valuuta jaoks vajaduse järgi.

Alltoodud näites on _EUR_ vaikevaluuta ja _USD_ on lisatud lisavaluutana.

![Mitme valuutaga mudeli näide.](media/prod-config-rules-currency-example.png "Mitme valuutaga mudeli näide")

> [!NOTE]
> Te ei saa lisada avaldisereegleid, mis kehtivad ainult mittevaikevaluuta puhul. Avaldisereeglite loomiseks, mis kehtiksid ainult valuuta puhul, mis ei ole vaikevaluuta, seadke vaikevaluuta hinnaavaldise väärtus nulliks. Seejärel seadistage mittevaikevaluuta jaoks sobiv avaldis.

## <a name="test-your-price-model"></a>Hinnamudeli katsetamine

Et katsetada, kuidas müügihinnad töötavad konfiguratsiooniseansis, avage oma hinnamudeli jaoks redigeerimisleht, nagu on kirjeldatud jaotises [Müügihinna mudelite loomine](#build-price-model), ning valige seejärel toimingupaanil suvand **Testi**. Avaneb dialoogiboks **Hinnamudeli katsetamine**, kus saate teha järgmist.

- Kasutage siin pakutavaid konfiguratsiooniseadeid, et valida tootesuvandid, ja seejärel vaadake, kuidas need mõjutavad suvandi **Hind ja lähetuskuupäev** väärtust.
- Valige **Kuva hinnajaotus**, et laadida alla Exceli dokument, mis näitab hinna arvutamise kõiki üksikasju.

![Oma tootemudeli katsetamine.](media/prod-config-test.png "Oma tootemudeli katsetamine")

Allalaaditud arvutustabel näitab iga aktiivse hinnaelemendi puhul nii absoluutset väärtust kui ka kasumi protsenti. Kui olete seadistanud lehel **Tooteteabe halduse parameetrid** hinnamudeli suvandi **Manusta**, lisatakse see Exceli leht tellimuse või pakkumise reale.

![Exceli arvutustabel, milles on kuvatud hinnajaotus.](media/prod-config-excel-example.png "Exceli arvutustabel, milles on kuvatud hinnajaotus")

## <a name="set-up-selection-criteria-for-price-models"></a>Valikukriteeriumide seadistamine hinnamudelite jaoks

Kui teie hinnamudelid on seadistatud, tuleb teil luua vähemalt üks valikukriteerium, et hinnamudel pakkumise või tellimuse konfigureerimisel üles leida. Seda saate teha ühe või mitme päringu seadistamisega. Koos ühtivate müügihinna mudelitega pakuvad päringud suurt paindlikkust, kui kohandate hindu kindlate klientide, regioonide, perioodide ja muude kriteeriumide alusel.

Valikukriteeriumide seadistamiseks hinnamudelite jaoks tehke järgmist.

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Valige sobiv tootekonfiguratsiooni mudel.
1. Valige toimingupaanil vahekaart **Mudel** ning valige rühmas **Seadistamine** suvand **Hinnamudeli kriteeriumid**. Avaneb leht **Hinnamudeli kriteeriumid**.
1. Kui vajalikku päringurida ei ole veel olemas, valige toimingupaanil suvand **Uus**, et lisada ruudustikku uus rida, ning sätestage see järgmiselt.
    - **Nimi** – sisestage selle rea nimi.
    - **Kirjeldus** – kirjeldage lühidalt päringut ja milleks see on.
    - **Hinnamudel** – valige [hinnamudel](#build-price-model) (praegusest konfiguratsiooni mudelist), mida päring käivitamisel rakendab.
    - **Tellimuse tüüp** – valige tellimuse tüüp, mille puhul päring rakendatakse.
    - **Kehtiv alates** – määrake esimene kuupäev, millal päring rakendub.
    - **Aegub** – määrake päringu rakendumise viimane kuupäev.

    ![Hinnamudeli kriteeriumid.](media/prod-config-price-model-criteria.png "Hinnamudeli kriteeriumid")

1. Valige päringu rida, mida soovite määratleda, ja seejärel valige **toimingupaanil** suvand **Redigeeri**. Avaneb päringukujundaja dialoogiboks. See toimib nagu enamik päringukujundajaid rakenduses Supply Chain Management. Kasutage seda, et määratleda tingimused, mille alusel tuleks valitud rea puhul hinnamudelit rakendada.

1. Korrake samme 4‑5 iga päringu puhul, mida teil vaja on.
    > [!TIP]
    > Saate säästa aega, kopeerides olemasoleva rea, mis on juba sarnane uuega, mida teil on vaja lisada. Selleks valige sihtrida ja seejärel toimingupaanilt **Dubleeri**.

1. Kui olete kriteeriumide seadistamise lõpetanud, pange need loendis **Hinnamudeli kriteeriumid** õigesse järjekorda. Rea ümberpaigutamiseks valige rida ja seejärel toimingupaanilt **Üles** või **Alla**.

    > [!IMPORTANT]
    > Konfigureerimise ajal alustab süsteem otsingut loendi algusest ja kasutab esimest päringut, mis ühtib pakkumise või tellimuse rea andmetega. Seetõttu peate panema oma kõige täpsemad päringud ülevale. Kui paigutate loendi algusesse üldise päringu, kasutatakse seda ka siis, kui loendis on allpool mõni päring, mis kehtib täpselt selle konfiguratsiooni kliendi või potentsiaalse kliendi puhul.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Atribuudipõhiste müügihindade seadmine tootemudeli versiooni jaoks

Viimane samm on määrata tootemudeli versiooni jaoks atribuudipõhised müügihinnad. Selleks tehke järgmist.

1. Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.
1. Valige sobiv tootekonfiguratsiooni mudel.
1. Valige toimingupaanil vahekaart **Mudel** ning valige rühmas **Hinnamudeli üksikasjad** suvand **Versioonid**.
1. Avaneb leht **Versioonid**. Veenduge, et suvandi **Hinnakujundusmeetod** väärtuseks oleks seatud **Atribuudipõhine**.
    ![Hinnakujundusmeetodi seadmine atribuudipõhiseks.](media/prod-config-versions.png "Hinnakujundusmeetodi seadmine atribuudipõhiseks")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]