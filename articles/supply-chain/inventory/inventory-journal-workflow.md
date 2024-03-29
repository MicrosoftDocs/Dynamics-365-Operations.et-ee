---
title: Varude töölehe kinnitamise töövood
description: See artikkel kirjeldab, kuidas seadistada ja kasutada laotöölehe kinnitustöövooge erinevat tüüpi füüsiliste laokannete puhul. Varude töölehe töövood aitavad tagada, et kannetesse saab sisestada ainult kinnitatud varude töölehti.
author: yufeihuang
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3a97eaeae24850282c39196a61e3baa29307aa93
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334651"
---
# <a name="inventory-journal-approval-workflows"></a>Varude töölehe kinnitamise töövood

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada ja kasutada laotöölehe kinnitustöövooge erinevat tüüpi füüsiliste laokannete puhul, nt väljaminekud ja sissetulekud, lao liikumised, kooslused ning füüsilise laoseisu vastavusseviimine. Varude töölehe töövood aitavad tagada, et kannetesse saab sisestada ainult kinnitatud varude töölehti.

> [!NOTE]
> Varude töölehe kinnitamise töövood rakenduvad ainult kannete puhul, mis on salvestatud varude halduse mooduli abil. Need ei tööta laohalduse moodulist käivitatud varude töölehtedega.

## <a name="turn-the-inventory-journal-approval-workflows-feature-on-or-off"></a>Laotöölehe kinnitustöövoogude funktsiooni sisse- või väljalülitamine

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.21 puhul lülitatakse funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides Varude töölehe kinnitamise töövoo funktsiooni Funktsioonihalduse tööruumis.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="create-your-inventory-journal-approval-workflows"></a>Varude töölehe kinnitamise töövoogude loomine

Selle funktsiooni seadistamiseks peate looma töövoo iga varude töölehe tüübi jaoks, mida soovite kontrollida. Kuna eri varude töölehe tüüpidel võivad olla eri kinnitushierarhiad ja töövooetapid, saate konfigureerida iga varude töölehe tüübi jaoks eraldi töövood.

Töövood toetavad versioonihaldust ning igal neist on töövoo ID ja aktiivne versioon. Saate iga uue töövoo versiooni kohe pärast loomist aktiveerida või seda passiivsena hoida. Kui vajate sama töölehe tüübi jaoks eri töövooge, looge selle töölehe tüübi jaoks mitu töövoogu ja seejärel määrake igaüks eri töölehe nimele, mis seda tüüpi kasutab.

Varude töölehe kinnitamise töövoogude loomiseks tehke järgmist.

1. Avage **Varude haldus \> Seadistus \> Varude halduse töövood**.
1. Valige Toimingupaanil suvand **Uus**.
1. Valige varude töölehe tüüp, mille jaoks soovite töövoogu seadistada.
    - **Märgistatud varude inventuuritööleht**
    - **Varude omandiõiguse muutmise tööleht**
    - **Varude liikumise tööleht**
    - **Varude ülekandmistööleht**
    - **Varude inventuuritööleht**
    - **Varude koosluse tööleht**
    - **Varude korrigeerimistööleht**

    ![Töölehe loomise dialoogiboks.](media/journal-workflow-create-workflow.png "Töölehe loomise dialoogiboks")

1. Teie arvutis käivitub töövooredaktori rakendus. (Teil võidakse paluda see tegevus kinnitada.) Kasutage seda vajaduse järgi oma töövoo kujundamiseks. Lisateavet töövooredaktori kasutamise kohta leiate teemast [Töövoosüsteemi ülevaade](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).
1. Pärast salvestamist ja töövooredaktori rakenduse sulgemist peate valima, kas see töövoo versioon aktiveerida või hoida seda passiivsena.

> [!NOTE]
> Töövood pakuvad versioonihaldust, mis tähendab, et saate vaadata loodud versioonide loendit ja valida, milline neist on aktiivne. Saadaolevate versioonide loendi vaatamiseks ja aktiivse versiooni valimiseks valige töövoog lehelt **Varude halduse töövood**. Avage toimingupaanilt vahekaart **Töövoog** ja valige **Versioonid**. Iga töövoo ID puhul võib korraga olla aktiivne ainult üks versioon.

## <a name="assign-approval-workflows-to-inventory-journal-names"></a>Kinnitamise töövoogude määramine varude töölehtede nimedele

Järgmiseks määrake varude töölehe töövoog igale varude töölehe nimele. Saate iga varude töölehe tüübi jaoks seadistada mitu varude töölehe nime.

Varude töölehe töövoo seostamiseks varude töölehe nimega tehke järgmist.

1. Avage **Varude haldus \> Seadistus \> Töölehtede nimed \> Varud**.
1. Valige loendiveerust töölehe nimi, et avada selle sätete leht.
1. Seadke kiirkaardil **Üldine** suvandi **Kinnitamise töövoog** väärtuseks **Jah**. Kui teil palutakse tegevus kinnitada, valige **Jah**.

    ![Töövoo määramine töölehe nimele.](media/journal-workflow-journal-name.png "Töövoo määramine töölehe nimele")

1. Avage ripploend **Töövoog** ja valige sobiv töövoog. Loendis on kuvatud kõik aktiivsed töövood, mille olete loonud töövooredaktori rakenduse abil.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Varude töölehe loomine ja kinnitamiseks saatmine

Pärast varude töölehe nime seostamist sellega ühtiva varude töölehe kinnitamise töövooga saate luua uusi varude töölehti, mis seda nime kasutavad, ja seejärel saata selle töövoo abil need töölehed kinnitamiseks. Te ei saa varude töölehte sisestada enne, kui töövoos konfigureeritud kinnitajad on selle kinnitanud.

1. Laiendage navigeerimispaanis **Varude haldus \> Töölehekirjed \> Kaubad** ja seejärel valige varude töölehe tüüp.
1. Valige **Uus**, et luua valitud tüübi jaoks uus tööleht.
1. Avaneb dialoogiboks **Varude töölehe loomine**. Täitke vorm vajaduse järgi ja seejärel valige töölehe salvestamiseks **OK**.
1. Täitke tööleht vajaduse järgi.
1. Kui loote või avate varude töölehe sellega seotud kinnitamise töövooga, on toimingupaanil aktiivne nupp **Töövoog**. Kui olete valmis töölehte kinnitamiseks saatma, valige nupp **Töövoog**, et avada rippdialoogiboks, ja seejärel valige **Esita**. Kinnitustaotlus saadetakse seejärel asjakohasele kinnitajale, keda teavitatakse töövoo jaoks konfigureeritud teatamismeetodi abil.

    ![Töölehe esitamine kinnitamiseks.](media/journal-workflow-inventory-journal.png "Töölehe esitamine kinnitamiseks")

Kinnitustaotluse tagasivõtmiseks avage asjakohane tööleht, valige nupp **Töövoog** ja seejärel valige **Võta tagasi**. See lähtestab töövoo.

Kui teie tööleht on kinnitatud, saate selle sisestada. Töölehe sisestamiseks valige toimingupaanilt **Sisesta**. Kui nupp **Sisesta** ei ole aktiivne, pole tööleht veel kinnitatud.

## <a name="respond-to-an-inventory-journal-approval-request"></a>Varude töölehe kinnitamise taotlusele vastamine

Kui olete kinnitaja, peaksite saama teate iga kord, kui teie kinnitust on vaja (nagu on konfigureeritud asjakohases töövoos). Seejärel saate töölehe kinnitamise taotluse järgmiselt kinnitada või tagasi lükata.

1. Laiendage navigeerimispaanis **Varude haldus \> Töölehekirjed \> Kaubad** ja seejärel valige varude töölehe tüüp.
1. Avage asjakohane tööleht ja vaadake see üle.
1. Valige toimingupaanilt nupp **Töövoog**, et avada rippdialoogiboks. Valige üks järgmistest.
    - **Kinnita** – taotluse kinnitamiseks.
    - **Lükka tagasi** – taotluse tagasilükkamiseks.
    - **Rohkem \> Taotle muudatust** – taotlejale teate saatmiseks, paludes tal midagi kindlat muuta ja seejärel uuesti esitada.
    - **Rohkem \> Delegeeri** – kinnitamise delegeerimine teisele kasutajale.
    - **Rohkem \> Võta tagasi** – kinnitustaotluse tagasivõtmiseks (töövoog lähtestatakse).
    - **Rohkem \> Töövoo ajalugu** – praeguse kinnitamistöövoo ajaloo vaatamiseks.

## <a name="review-the-approval-history"></a>Kinnitamisajaloo ülevaatamine

Nagu teiste töövoo tüüpide puhul, saate kasutada lehte **Töövoo ajalugu**, et vaadata ükskõik millise töölehe kinnitamistöövoo ajalugu.

Töölehe töövoo ajaloo vaatamiseks tehke järgmist.

1. Laiendage navigeerimispaanis **Varude haldus \> Töölehekirjed \> Kaubad** ja seejärel valige varude töölehe tüüp.
1. Avage asjakohane tööleht.
1. Valige toimingupaanilt nupp **Töövoog**, et avada rippdialoogiboks. Valige **Töövoo ajalugu**. Lisateavet leiate teemast [Töövoo ajaloo vaatamine](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]