---
title: Eelmääratud paigutustega töötamine
description: See artikkel kirjeldab, kuidas kasutada eelseadistatud paigutusi moodulis Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: b588df5702657f07e1e790ffba39d2e459901557
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286272"
---
# <a name="work-with-preset-layouts"></a>Eelmääratud paigutustega töötamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas kasutada eelseadistatud paigutusi moodulis Microsoft Dynamics 365 Commerce.

Enne selle artikli protseduuride sooritamist lugege enne eelseadistatud [ja kohandatud paigutusi](templates-layouts-overview.md#preset-and-custom-layouts). Üldise ülevaate saamiseks vt teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Uue eelmääratud paigutuse loomine

Eelmääratud paigutuse loomiseks on kaks võimalust. Võite salvestada olemasoleva kohandatud paigutuse uue eelmääratud paigutusena või luua nullist eelmääratud paigutuse.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Eelmääratud paigutuse loomine olemasolevast kohandatud paigutusest

Eelmääratud paigutuse loomiseks olemasolevast kohandatud paigutusest tehke järgmist.

1. Avage olemasolev leht, mis ei kasuta praegu eelmääratud paigutust ja millel on mooduli struktuur, mida soovite oma saidi teistel lehtedel uuesti kasutada.
1. Lehe vaatamiseks valige **Redigeeri**.
1. Valige suvand **Salvesta uue paigutusena**. Ilmub dialoogiboks **Salvesta uue paigutusena**.
1. Sisestage eelmääratud paigutuse nimi ja kirjeldus. Sisestatud väärtused kuvatakse teistele autoritele, kui nad loovad teie paigutusest uusi lehti või lähevad sellele üle. Seega sisestage väärtused, mis on kasulikud teistele lehe autoritele.
1. Valige nupp **OK**.

Eelmääratud paigutus on nüüd saadaval, kui loote uued lehed või valite lehele samas malli hierarhias teise paigutuse.

> [!TIP]
> Selleks et kiiresti näha, kas konkreetne leht on parasjagu seotud eelmääratud paigutusega, valige lehtede loendi vaatest leht ja kontrollige paigutuse metaandmeid paremal atribuutide paanil.

### <a name="create-a-new-preset-layout"></a>Uue eelmääratud paigutuse loomine

Eelmääratud paigutuse loomiseks nullist tehke järgmist.

1. Valige navigeerimispaanilt vasakult suvand **Paigutused**.
1. Valige suvand **Uus paigutus**. Ilmub dialoogiboks **Uus paigutus**.
1. Valige eelmääratud paigutuse jaoks kasutatav mall.
1. Sisestage eelmääratud paigutuse nimi ja kirjeldus. Sisestatud väärtused kuvatakse teistele autoritele, kui nad loovad teie paigutusest uusi lehti või lähevad sellele üle. Seega sisestage väärtused, mis on kasulikud teistele lehe autoritele.
1. Valige nupp **OK**, et luua uus eelmääratud paigutus ja avada paigutuse redaktor.
1. Paigutuse redaktoris lisa ja konfigureerige mooduleid, kasutades liigendpuud vasakul ja atribuutide paani paremal. (See protsess meenutab malli moodulite lisamist ja konfigureerimist malli redaktoris.) Moodulite asetus ja lukustatud vaikesätted muutuvad mooduli keskseks konfiguratsiooniks lehtedel, mis kasutavad seda eelmääratud paigutust.

## <a name="modify-a-preset-layout"></a>Eelmääratud paigutuse muutmine

Eelmääratud paigutuse muutmiseks tehke järgmist.

1. Valige navigeerimispaanilt vasakult suvand **Paigutused**.
1. Valige paigutuse redaktorist vasakult liigendpuust moodul, mida soovite muuta. Seejärel järgige neid samme.

    - Mooduli liigutamiseks ülema sees üles või alla valige mooduli kolmikpunkti nupp (**...**) ja seejärel käsk **Nihuta üles** või **Nihuta alla**.
    - Mooduli vaikesätete muutmiseks kasutage atribuutide paani, et sisestada vaikeväärtused, ja lukustage need valikuliselt kõikide järgmiste lehtede jaoks.
    - Uute moodulite või fragmentide lisamiseks konteineri moodulitesse valige kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul** või **Lisa fragment**.
    - Mooduli eemaldamiseks paigutuselt valige kolmikpunkti nupp ja seejärel valige käsk **Kustuta**.

## <a name="change-a-preset-layout-theme"></a>Eelmääratud paigutuse kujunduse muutmine

Tavaline on seadistada kõikidele eelmääratud paigutust kasutavatele lehtedele vaikekujundus.

Kujunduse määramiseks või muutmiseks kõikidele alamlehtedele, mis kasutavad teie eelmääratud paigutust, tehke järgmist.

1. Valige paigutuse redaktorist vasakult liigendpuust lehe konteineri moodul. (Tavaliselt on see moodul teine sõlm ja kannab nime **Vaikeleht**.)
1. **Valige parempoolse** paani atribuudid väljal Kujundus kujundus.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Eelmääratud paigutuse salvestamine, registreerimine, eelvaatamine ja avaldamine

Eelmääratud paigutuse salvestamiseks ja kontrollimiseks tehke järgmist.

1. Valige paigutuse redaktorist ülevalt suvand **Salvesta**. Salvestatud muudatused ei mõjuta järgmisi lehti, kuni need registreeritakse.
1. Valige **Lõpeta redigeerimine**. Teie muudatused on nüüd leitavad järgmiste töövoogude jaoks.

Muudatuste eelvaatamiseks avage olemasolev leht, mis kasutab eelmääratud paigutust, või looge paigutusest uus leht.

Pärast eelmääratud paigutuse muudatuste vaatamist järgige üht alltoodud etappidest paigutuse avaldamiseks reaalajas saidil.

1. Valige suvand **Paigutused**, valige paigutus ja seejärel käsk **Avalda**.
1. Valige paigutuse redaktori avamiseks paigutuse nimi ja seejärel **Avalda**.
1. Avaldage leht, mis viitab avaldamata paigutusele. Paigutus avaldatakse automaatselt.

> [!WARNING]
> Eelmääratud paigutustele saab viidata mitmelt lehelt. Kui avaldate eelmääratud paigutuse, pange tähele, et see võib mõjutada mitme lehe paigutust.

## <a name="rename-a-preset-layout"></a>Eelseadistatud paigutuse ümbernimetamine

Eelseadistatud paigutuse ümber nimetamiseks saidikonstruktoris järgige neid samme.

1. Valige vasakul navigeerimispaanil **kavandid**.
1. Valige selle paigutuse nimi, mida soovite ümber nimetada.
1. Valige **muuda**, et alustada paigutuse redigeerimist.
1. Valige paigutuse atribuutide paanil paigutuse nime kõrvalt amplili sümbol.
1. Redigeerige paigutuse nime vastavalt vajadusele.
1. Nime muudatuse kinnitamiseks märkige see ruut.
1. Valige **Lõpeta redigeerimine**.

## <a name="additional-resources"></a>Lisaressursid

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Mallidega töötamine](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
