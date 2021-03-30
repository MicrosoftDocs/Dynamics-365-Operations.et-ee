---
title: Arve põhiandmed ostureskontrosse kinnitamise töölehe abil
description: See teema selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kinnituslehte kulukontode värskendamiseks.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0fee32d9fd1ab89b1a8cedb2e1965674586d4e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227180"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Arve põhiandmed ostureskontrosse kinnitamise töölehe abil

[!include [banner](../../includes/banner.md)]

See teema selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kinnituslehte kulukontode värskendamiseks.

## <a name="create-and-post-and-invoice"></a>Arve loomine ja sisestamine
1. Minge navigeerimispaanil jaotisse **Moodulid > Ostureskontro > Arved > Arveregister**.
2. Valige suvand **Uus**.
3. Valige selle arveregistri nimi, mida soovite kasutada.
4. Registri avamiseks ja kuluridade sisestamiseks valige **Read**.
5. Valige hankija. Näiteks sisestage või valige `US-104`.
6. Sisestage väärtus väljale **Arve**.
7. Sisestage väärtus väljale **Kirjeldus**.
8. Sisestage number väljale **Kreedit**.
9. Väljal **Kinnitaja** valige rippmenüüst kinnitaja.
10. Valige **Sisesta**.

## <a name="approve-an-invoice"></a>Arve heakskiitmine
1. Avage navigeerimispaanil **Moodulid > Ostureskontro > Arved > Arve kinnitus**.
2. Valige suvand **Uus**.
3. Valige soovitud arve kinnitamise töölehe nimi.
4. Valige **Read**, et kuvada leht, kus saate valida arved, mille soovite kinnitada.
5. Valige **Leia vautšerid**, et kuvada kõik kinnitamiseks valmis olevad arved.
6. Märkige loodud arve ja klõpsake siis **Vali**. Ülal valitud kanded viiakse sellesse loendisse pärast nende valimist.  
7. Valige nupp **OK**.
8. Valige **konto numbri** väli, et lisada arvele kulukonto.
9. Sisestage kontonumber ja klõpsake väljapool välja. Sisestage näiteks `600120`.
10. Valige **Sisesta**.
11. Postitatud kirjete vaatamiseks valige **Vautšer**. Kinnituse ootel arvete konto tühistatakse ja asendatakse tegeliku kulukontoga.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]