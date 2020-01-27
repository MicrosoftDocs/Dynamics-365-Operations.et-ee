---
title: Tühistatud sisestustööleht
description: See teema kirjeldab võimeid, mis võimaldavad kandeid kannete loendist või finantslehtedelt tagasi võtta.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d18b71c1fc7f3f0c39172bd9edf19b4e60a2bf8
ms.sourcegitcommit: cfaad79bcb1460ee0e7ad5a2c596f9199e14c53a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/08/2020
ms.locfileid: "2944424"
---
# <a name="reverse-journal-posting"></a>Tühistatud sisestustööleht

[!include [banner](../includes/banner.md)]

See teema kirjeldab võimalusi lahenduses Microsoft Dynamics 365 Finance, mis lubavad teil kogu töölehe tagasi võtta või ühe või mitu kannet kannete loendist tagasi võtta, sõltumata nende päritolust. 

## <a name="reversing-journals"></a>Töölehtede tühistamine

Töölehe ridu saate ükshaaval muuta. Tühistatud töölehe sisestamisega saate ka kogu Finantstöölehe tagasi võtta. Töölehe tühistamine: 

- Avage finantstööleht ja sisestatud töölehtede filter.
- Valige lehe ülaosas olevas menüüs **Storneeri**.
- Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat
- Valige **Jah**, et kasutada olemasolevaid kande kuupäevi, või **Ei**, et sisestada uus. Mõnel juhul võib algse kande perioodi sulgeda ja tühistamise jaoks tuleb sisestada uue kande kuupäev.
- Kui valisite **Ei**, sisestage tühistamise kande kuupäev. 
- Sisestage kommentaar, mida soovite tühistamise kandele lisada.
- Valige nupp **Storneeri**.

Kanded tühistatakse. 

Kui kande on üle 100 rea, käivitatakse tühistamise protsess pakktöötluse abil. Tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös. Kõik kanded, mida ei saanud tühistada, loetletakse pakett-töö ajaloos.

Kui kandes on kuni 100 rida, käivitub tühistamise protsess kohe. Tulemused esitatakse dialoogiboksis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, koos põhjusega, miks seda ei saanud tühistada. Valige dialoogiboksi sulgemiseks suvand **OK**.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Kande tühistamine kannete loendist. 

Samuti saate kandeid **kannete loendist** tagasi võtta kõigis pearaamatutes. Lisaks saate ümber nimetada rohkem kui ühe kande korraga. 

Ühe või mitme kande tühistamine: 

- Valige lehe ülaosas olevas menüüs **Storneeri**
- Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat.
- Valige **Jah**, et kasutada olemasolevaid kande kuupäevi, või **Ei**, et sisestada uus. Mõnel juhul võib algse kande perioodi sulgeda ja selle tühistamiseks tuleb sisestada uue kande kuupäev.
- Kui valisite **Ei**, sisestage tühistamise kande kuupäev. 
- Saate sisestada märkuse tühistuskande kirjeldamiseks.
- Valige nupp **Storneeri**.

Kanded tühistatakse. 

Kui kandes on üle 100 rea, käivitatakse tühistamise protsess pakktöötluse abil. Tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös. Kõik kanded, mida ei saanud tühistada, tuuakse ära pakett-töö ajaloos.

Kui kanderidade arv on kuni 100, käivitub tühistamise protsess kohe. Tulemused kuvatakse dialoogiboksis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, koos põhjusega. Valige dialoogiboksi sulgemiseks suvand **OK**.

Kandeid saab tühistada ainult juhul, kui need vastavad nende tühistamise ärireeglitele. Hankija makseid ei saa muuta, kasutades selles teemas kirjeldatud võimalusi. Hankija maksed tuleb tagasi võtta, järgides juhiseid, mis on toodud teemas [Hankija makse storneerimine](https://docs.microsoft.com/en-us/dynamics365/finance/accounts-payable/reverse-vendor-payment).

