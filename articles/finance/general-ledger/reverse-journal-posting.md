---
title: Tühistatud sisestustööleht
description: See artikkel kirjeldab võimalusi, mis võimaldavad teil tühistada kandeid kande kandeloendist või finantstöölehtedelt.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 7e3a22f43bcc312fe60b77db2fc3bc94d15950c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284847"
---
# <a name="reverse-journal-posting"></a>Tühistatud sisestustööleht

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab võimalusi Microsoft Dynamics 365 Finance, mis võimaldab teil tühistada terve töölehe või tühistada kande kannete loendist ühe või mitu kannet, olenemata nende päritolust. 

Enne kui saate ühte selles artiklis kirjeldatud funktsioonidest kasutada, peab see olema süsteemist sisse lülitatud. Administraatorid saavad kasutada **funktsioonihalduse** tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.
 - Moodul: Pearaamat
 - Funktsiooni nimi: **mitme dokumendi hulgipööramised**

## <a name="reversing-journals"></a>Töölehtede tühistamine

Töölehe ridu saate ükshaaval muuta. Tühistatud töölehe sisestamisega saate ka kogu Finantstöölehe tagasi võtta. Töölehe tühistamine: 

- Filtreerige sisestatud töölehed ja avage **Read** vaade töölehel.
- Valige lehe ülaosas olevas menüüs **Storneeri**.
- Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat.
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

- Valige lehe ülaosas olevas menüüs **Tühista kogu töölehe ripploend**.
- Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat.
- Valige **Jah**, et kasutada olemasolevaid kande kuupäevi, või **Ei**, et sisestada uus. Mõnel juhul võib algse kande perioodi sulgeda ja selle tühistamiseks tuleb sisestada uue kande kuupäev.
- Kui valisite **Ei**, sisestage tühistamise kande kuupäev. 
- Saate sisestada märkuse tühistuskande kirjeldamiseks.
- Valige nupp **Storneeri**.

Kanded tühistatakse. 

Kui kandes on üle 100 rea, käivitatakse tühistamise protsess pakktöötluse abil. Tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös. Kõik kanded, mida ei saanud tühistada, tuuakse ära pakett-töö ajaloos.

Kui kanderidade arv on kuni 100, käivitub tühistamise protsess kohe. Tulemused kuvatakse dialoogiboksis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, koos põhjusega. Valige dialoogiboksi sulgemiseks suvand **OK**.

Kandeid saab tühistada ainult juhul, kui need vastavad nende tühistamise ärireeglitele. Hankijamakseid ei saa selles artiklis kirjeldatud võimaluse abil tagasi võtta. Hankija maksed tuleb tagasi võtta, järgides juhiseid, mis on toodud teemas [Hankija makse storneerimine](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
