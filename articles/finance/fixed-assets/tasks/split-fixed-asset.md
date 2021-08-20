---
title: Põhivara tükeldamine
description: See teema selgitab, kuidas tükeldada ühe vararaamatu protsenti uude vararaamatusse.
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ac7bc9ae9040f9668c36c570be795ebeb7c6970049ff911b1caeadd06f31d0a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778986"
---
# <a name="split-a-fixed-asset"></a>Põhivara tükeldamine

[!include [banner](../../includes/banner.md)]

See teema selgitab, kuidas tükeldada ühe vararaamatu protsenti uude vararaamatusse. See kasutab raamatupidaja rolli ja USMF-i demoandmeid.

## <a name="create-a-new-fixed-asset"></a>Uue põhivara loomine

1. Avage navigeerimispaanil jaotis **Moodulid \> Põhivarad \> Põhivarad \> Põhivarad**.
2. Valige suvand **Uus**.
3. Väljale **Põhivara grupp** sisestage või valige väärtus. Märkige põhivara kood hilisemaks tükeldamisprotsessis kasutamiseks üles.
4. Sisestage väärtus väljale **Nimi**.
5. Sulgege vorm.

## <a name="split-a-fixed-asset"></a>Põhivara tükeldamine

Enne täielikult amortiseeritud vara tükeldamist tuleb vara raamatu olek **Suletud** muuta käsitsi olekuks **Avatud**. See etapp on nõutav, kuna raamatu olek peab olema **Avatud**, kui peate sisestama varale kandeid (nt likvideerimismüük). Samuti peate sisse lülitama parameetri **Luba ühe kande raames mitut kannet** vahekaardil **Üldine** lehel **Pearaamatu parameetrid**. Pärast vararaamatu oleku muutmist ja mitme kande lubamist ühe kande raames tehke vara tükeldamiseks järgmised toimingud.

1. Leidke loendist tükeldatav põhivara ja valige selle link.
2. Valige **Raamatud**. Valige uuele varale tükeldatav raamat.
3. Valige **Funktsioonid**.
4. Valige **Tükelda põhivara**.
5. Sisestage väärtus väljale **Põhivarasse** või valige sellelt väljalt.
6. Klõpsake väljal **Raamatusse** otsingu avamiseks ripploendi nuppu.
7. Sisestage kuupäev väljale **Kande kuupäev**.
8. Sisestage number väljale **Protsent**.
9. Valige või sisestage väärtus väljal **Töölehe nimi**.
10. Valige nupp **OK**.

## <a name="post-the-journal-transaction"></a>Töölehekande sisestamine

1. Avage navigeerimispaanil jaotis **Moodulid \> Põhivarad \> Töölehe kanded \> Põhivarade tööleht**.
2. Valige loendist tükeldamise protsessis loodud tööleht.
3. Valige **Read**.

    - Kontrollige loodud töölehe ridu.
    - Soetamise korrigeerimiskanne luuakse algse vara puhul väärtuse vähendamiseks tükeldamisprotsessis määratud protsendi võrra.
    - Soetamiskanne luuakse uue vara puhul samas summas.

4. Valige **Sisesta**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]