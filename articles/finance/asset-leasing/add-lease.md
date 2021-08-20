---
title: Rendikirjete lisamine või kopeerimine (eelversioon)
description: Selles teemas kirjeldatakse, kuidas luua uus rentimine, sisestades selle teabe vara rentimisest või kopeerides teabe olemasolevast rendikirjest.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2f2e6837819158688f3fd6bc28909a106a05a098ca917cab9032a2d0044042fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761322"
---
# <a name="add-or-copy-leases-preview"></a>Rendikirjete lisamine või kopeerimine (eelversioon)

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas luua rentimine vara rentimisel nullist ja samuti kuidas luua rentimist kopeerides olemasolevast rendikirjest. Rendikirje nullist loomise toiming hõlmab teabe sisestamist uude rendikirjesse ja seejärel rentimise ajakava loomist. Pärast vähemalt ühe rendikirje häälestamist võib olla lihtsam kopeerida teave olemasolevast rendikirjest ja seejärel muuta seda teavet vastavalt vajadusele, et luua uus rendikirje.

## <a name="create-a-lease"></a>Rendi loomine

Vara rentimises rendikirje loomiseks tehke järgmist.

1. Valige toimingupaani lehel **Rendi kokkuvõte** suvand **Uus**.
2. Sisestage rendi teave. Nõutavatel väljadel on punased ääred.

## <a name="create-a-lease-schedule"></a>Rendigraafiku loomine

Pärast rendikirje teabe sisestamist tehke rendiajakava loomiseks järgmist.

> [!NOTE]
> Finantsdimensioonid võivad mis tahes kohandatud finantsdimensiooni põhjal muutuda.

1. Rendiraamatute loomiseks valige **Loo graafikud**. Rendiraamatute hulka kuuluvad makse, amortisatsiooni, kulumi ja kulude graafikud.
2. Rendiraamatutele juurdepääsuks vastloodud graafikute vaatamiseks valige vahekaart **Raamatud**.

    Leht **Raamatu üksikasjad** näitab, kuidas renti sellele eraldatud raamatutega arvestatakse. Siit saate vaadata rendigraafikuid.

    Maksegraafik sisaldab vahekaardi **Maksegraafiku read** sisendeid lehel **Rendi lisamine**. Saate iga makse summat ja muutuvat makset endiselt muuta. Rendikohustis arvutatakse muudetud maksegraafiku põhjal.

4. Kui olete maksegraafiku läbivaatamise lõpetanud valige **Kinnita graafik**. Pärast graafiku kinnitamist pole rendikirje redigeerimiseks enam saadaval.

    > [!NOTE]
    > Süsteem arvutab rendiperioodi lehel **Rendi lisamine** maksegraafiku ridade põhjal automaatselt.
    >
    > Rendiperioodi kuudes arvutamiseks leiab süsteem konkreetse maksegraafiku rea jaoks alguskuupäeva ja lõpukuupäeva erinevuse. Seejärel liigub see järgmisele maksegraafiku reale ja leiab erinevuse uuesti. Lõpuks liidab süsteem kõik summad, et määrata rendiperiood kuudes.

5. Arvutatud perioodi intressikulu vaatamiseks avage leht **Kohustise amortiseerimise graafik**. Arvutatud lineaarse kulumi vaatamiseks avage leht **Vara kulumigraafik**.
6. Kui olete arvutatud summa läbivaatamise lõpetanud, saate luua lehel **Esialgne tuvastamine** esialgse tuvastamise tööleje kirje. Teile kuvatakse teade, et tööleht on loodud.

    > [!NOTE]
    > Töölehe kirjet ei sisestata pearaamatusse enne, kui sisestate kirje käsitsi.

7. Kui soovite pakutud algse tuvastamise kirje enne sisestamist läbi vaadata, valige **Vara rentimise tööleht**.

    > [!NOTE]
    > Vara rentimise töölehte ei saa käsitsi luua. See luuakse rendiajakavade loomise ajal automaatselt.

8. Kui olete algse tuvastamise töölehe kirje läbi vaadanud ja olete valmis selle sisestama, valige suvand **Sisesta**, et tuvastada kasutamisõiguse esemeks olev vara ja rendikohustis pearaamatus.

## <a name="copy-a-lease"></a>Rendi kopeerimine

Vara rentimine võimaldab teil kopeerida rendi üksikasjad, et luua uus rendikirje, millel on sama teave. Saate seejärel muuta rendikirje välju, enne kui loote kopeeritud rentimise graafiku.

1. Valige lehel **Rendikokkuvõte** kopeerimiseks rendikirje ja valige seejärel tegevuspaanil suvand **Kopeeri rendikirje**.

    > [!NOTE]
    > Kui parameeter **Käsitsi** on rendi ID-de numbriseeria jaoks välja lülitatud, luuakse automaatselt kopeeritud rendikirje rendi ID automaatselt. Kui parameeter **Käsitsi** on sisse lülitatud, kuvatakse teade, mis palub teil enne müügikirje kopeerimist sisestada rendi ID.

2. Valige suvand **Kopeeri**. Valitud rendikirje üksikasjad kopeeritakse uude rendikirjesse. Seejärel saate muuta uue rendikirje üksikasju, enne kui selle salvestate ja loote rendigraafikud.

## <a name="asset-leasing-journal"></a>Vara rentimise tööleht

Kõik vara rentimises loodavad töölehe kanded sisalduvad vara rentimise töölehel. Lehel **Vara rentimise tööleht** (**Vara rentimine \> Töölehe kirjed \> Vara rentimise tööleht**) saate filtreerida, sisestades oleku, vaadates kindlaid töölehe kirjeid ja kandeid ning sisestada sisestamata töölehe kirjed.

> [!NOTE]
> Vara rentimise töölehte ei saa käsitsi luua. See luuakse rendiajakavade loomise ajal automaatselt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]