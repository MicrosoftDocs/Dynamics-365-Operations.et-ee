---
title: Arve põhiandmed ostureskontrosse kinnitamise töölehe abil
description: See teema selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kinnituslehte kulukontode värskendamiseks.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ce66a4b92f26bcec0849accad3878aef2b2f658
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109652"
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
