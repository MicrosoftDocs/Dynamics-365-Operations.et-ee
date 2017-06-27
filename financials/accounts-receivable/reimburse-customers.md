---
title: Klientide kulude korvamine
description: "Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua. Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c3201166eb7054205647a54ed80f98968fcfda6e
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="reimburse-customers"></a>Klientide kulude korvamine

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua. Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada. 

Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

| Eeltingimus                                                            | Kirjeldus                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Juriidilise isiku minimaalse tagasimakse summa määramine.          | Sisestage lehe **Müügireskontro parameetrid** ala **Üldine** väljale **Minimaalne tagasimakse** miinimumsumma, mille saab kliendi ülemaksete puhul tagastada. |
| Valikuline: hankija konto lisamine igale kliendile, kellele saab tagasimakse teha. | Valige kliendi puhul hankija konto lehe **Kliendid** kiirkaardi **Mitmesugused üksikasjad** väljalt **Hankija konto**.                                           |

Korvamiskannete loomisel luuakse kreeditsaldo summa kohta hankija arve. Korvamisprotsess eemaldab kreeditsaldo kliendi kontolt ja loob kliendile vastava hankija konto saldo.

1.  Käivitage müügireskontros protsess **Korvamine**.
2.  Järgige üht neist sammudest.
    -   Kindlate kliendikontode korvamiseks klõpsake käsku **Vali** ja määrake päringus kliendikontod.
    -   Kõigi kliendikontode korvamiseks klõpsake nuppu **OK**.

    Kreeditsummad kantakse klientide hankijakontodele ja töödeldakse tavaliste maksetena. Kui kliendil ei ole hankija kontot, loob programm kliendi jaoks automaatselt ühekordse hankija konto.
3.  Loodud korvamiskannete vaatamiseks kasutage lehte **Korvamine**.
4.  Looge ostureskontros korvamisprotsessi tulemusena loodud hankija arvete makse.





