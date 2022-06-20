---
title: Arve põhiandmed ostureskontrosse kinnitamise töölehe abil
description: See artikkel selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutage kulukontode värskendamiseks kinnitamise töölehte.
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
ms.openlocfilehash: afe1471949bbf892f4e28ed3bea830ee491a517f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909210"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Arve põhiandmed ostureskontrosse kinnitamise töölehe abil

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutage kulukontode värskendamiseks kinnitamise töölehte.

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
