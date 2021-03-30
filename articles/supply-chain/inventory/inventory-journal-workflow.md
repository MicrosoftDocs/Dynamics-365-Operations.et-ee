---
title: Varude töölehe kinnitamise töövood
description: Selles teemas kirjeldatakse, kuidas seadistada ja kasutada varude töölehe kinnitamise töövoogusid eri tüüpi füüsiliste laokannete jaoks. Varude töölehe töövood aitavad tagada, et kannetesse saab sisestada ainult kinnitatud varude töölehti.
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 596182dfd7430e4d1e35ffebb795fbcf98d45e33
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247906"
---
# <a name="inventory-journal-approval-workflows"></a>Varude töölehe kinnitamise töövood

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada ja kasutada varude töölehe kinnitamise töövoogusid mitmesuguste füüsiliste laokannete jaoks, nt väljaminekud ja sissetulekud, varude liikumised, kooslused (BOM-id) ning füüsiliste varude vastavusseviimine. Varude töölehe töövood aitavad tagada, et kannetesse saab sisestada ainult kinnitatud varude töölehti.

> [!NOTE]
> Varude töölehe kinnitamise töövood rakenduvad ainult kannete puhul, mis on salvestatud varude halduse mooduli abil. Need ei tööta laohalduse moodulist käivitatud varude töölehtedega.

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a>Varude töölehe kinnitustöövoogude funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *varude ja laohaldus*
- **Funktsiooni nimi**: *Varude töölehe kinnitamise töövoog*

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

    ![Töölehe loomise dialoogiboks](media/journal-workflow-create-workflow.png "Töölehe loomise dialoogiboks")

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

    ![Töövoo määramine töölehe nimele](media/journal-workflow-journal-name.png "Töövoo määramine töölehe nimele")

1. Avage ripploend **Töövoog** ja valige sobiv töövoog. Loendis on kuvatud kõik aktiivsed töövood, mille olete loonud töövooredaktori rakenduse abil.

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a>Varude töölehe loomine ja kinnitamiseks saatmine

Pärast varude töölehe nime seostamist sellega ühtiva varude töölehe kinnitamise töövooga saate luua uusi varude töölehti, mis seda nime kasutavad, ja seejärel saata selle töövoo abil need töölehed kinnitamiseks. Te ei saa varude töölehte sisestada enne, kui töövoos konfigureeritud kinnitajad on selle kinnitanud.

1. Laiendage navigeerimispaanis **Varude haldus \> Töölehekirjed \> Kaubad** ja seejärel valige varude töölehe tüüp.
1. Valige **Uus**, et luua valitud tüübi jaoks uus tööleht.
1. Avaneb dialoogiboks **Varude töölehe loomine**. Täitke vorm vajaduse järgi ja seejärel valige töölehe salvestamiseks **OK**.
1. Täitke tööleht vajaduse järgi.
1. Kui loote või avate varude töölehe sellega seotud kinnitamise töövooga, on toimingupaanil aktiivne nupp **Töövoog**. Kui olete valmis töölehte kinnitamiseks saatma, valige nupp **Töövoog**, et avada rippdialoogiboks, ja seejärel valige **Esita**. Kinnitustaotlus saadetakse seejärel asjakohasele kinnitajale, keda teavitatakse töövoo jaoks konfigureeritud teatamismeetodi abil.

    ![Töölehe esitamine kinnitamiseks](media/journal-workflow-inventory-journal.png "Töölehe esitamine kinnitamiseks")

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