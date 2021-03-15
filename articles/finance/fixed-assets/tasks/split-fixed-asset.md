---
title: Põhivara tükeldamine
description: See teema selgitab, kuidas tükeldada ühe vararaamatu protsenti uude vararaamatusse.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75938e6fdf5fd8f10ac9719fc449a586c08d06b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975937"
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