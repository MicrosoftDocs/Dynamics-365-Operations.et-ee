---
title: Tühistatud sisestustööleht
description: See teema kirjeldab võimeid, mis võimaldavad kandeid kannete loendist või finantslehtedelt tagasi võtta.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ab53f4b8888f77cd41ccbd7956ed307ba1b54ff
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897132"
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

Kandeid saab tühistada ainult juhul, kui need vastavad nende tühistamise ärireeglitele. Hankija makseid ei saa muuta, kasutades selles teemas kirjeldatud võimalusi. Hankija maksed tuleb tagasi võtta, järgides juhiseid, mis on toodud teemas [Hankija makse storneerimine](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]