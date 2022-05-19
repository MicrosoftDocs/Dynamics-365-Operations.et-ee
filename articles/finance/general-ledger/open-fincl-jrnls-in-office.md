---
title: Finantstöölehe mallide avamine Office'is
description: Selles teemas kirjeldatakse probleeme, mis võivad ilmneda kohandatud finantstöölehtede loomisel Microsoft Exceli malli abil.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 099d3c0074a86913b79b732a4c2a34b6e6488672
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723074"
---
# <a name="open-financial-journal-templates-in-office"></a>Finantstöölehe mallide avamine Office'is

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse probleeme, mis võivad ilmneda kohandatud finantstöölehtede loomisel Microsoft Exceli malli abil.

## <a name="symptom"></a>Sümptom

Lõite kohandatud Exceli malli finantstöölehtedele, kuid seda ei kuvata menüüs **Ava read Excelis**. Või kui seda kuvatakse menüüs, avatakse selle valimisel mõni muu mall.

## <a name="resolution"></a>Lahendus

Vaikefunktsioon Ava Excelis kasutab käesoleva lehe juurandmeallikat (tabelit), et määrata, millised Office'i mallid või andmeüksused kuvatakse Exceli menüü **Ava Excelis** suvanditena. Selline käitumine ei ole finantstöölehtede puhul ideaalne kasutuskogemus, kuna finantstöölehed kasutavad juurandmeallikaga samu tabeleid (LedgerJournalTable ja LedgerJournalTrans) paljude muud tüüpi töölehtede seast.

Finantstöölehtede puhul on funktsiooni Ava read Excelis eesmärk kuvada malle, mis on loodud töölehe jaoks, mille kontekstis praegu töötate, näiteks üldine tööleht või maksetööleht. Näiteks mall, mis on mõeldud kasutamiseks hankija makse töölehega, on mõeldud jõustama teie esmase konto hankijakontona.

Kui soovite ülendada malli, et see oleks saadaval menüüs **Ava read Excelis** ja **Ava Excelis**, on lihtne arendajakogemus rakendada liidest **LedgerIJournalExcelTemplate** ja laiendada klassi **DocuTemplateRegistrationBase**. Paljud selle lähenemisviisi näited rakendatakse selles süsteemis. Üks näide, mida saab kasutada viitena, on liides **LedgerDailyJournalExcelTemplate** mis loodi üldise töölehe (või päevase töölehe) jaoks.

Kui liides **LedgerIJournalExcelTemplate** on teie mallile rakendatud, filtreeritakse menüüs **Ava read Excelis** mallid teie töölehe tüübi alusel ja kuvatakse ainult mallid, mis on selle töölehe jaoks saadaval. Liides pakub ka kinnitusmeetodit, mis tagab, et malli ei saa töölehe jaoks avada, kui see ei vasta kontotüübi nõuetele. Näiteks saate määrata, et konto tüüp peab olema **Hankija** või **Pearaamat**.

Lisateavet selle funktsiooni kohta vt [Mallide lisamine menüüsse Ava read Excelis](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
