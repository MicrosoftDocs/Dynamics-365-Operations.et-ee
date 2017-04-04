---
title: Hankija osalises summas maksed
description: "Mõnikord võite teha hankijale makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>Hankija osalises summas maksed

Mõnikord võite teha hankijale makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist. 

<a name="cash-discount-amounts"></a>Skonto summad
---------------------

Hankija võib pakkuda enne tähtaega tasutud arve puhul skontot. Näiteks sisestate arve summas 100,00 ja sellele on määratud skonto 2%, kui arve tasutakse kümne päeva jooksul. Tähtaeg on 30 päeva. Kui maksesoovituse kasutab skonto kriteerium valides arve ja ettepaneku käivitada või enne skonto kuupäev, arve on valitud makse ja makse luuakse 98.00. Skonto saab teha ka käsitsi loodud 2005.

## <a name="partial-payments-with-cash-discounts"></a>Osalised maksed skontodega
Osalise makse tegemisel kavatsete ilmselt teha täiendava osamakse arve täielikuks tasakaalustamiseks. Võtta osaliselt skonto, peate seadma selle ** osalise makse skonto arvutamiseks ** võimalus **Jah** kohta on **moodustavad Ostureskontro parameetrid** lehele. 

Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Arve summas 100,00 on sisestatud. Kui makse 49.00 10 päeva jooksul, sisestada deebet 49.00 maksežurnaali. Millal te langeda osaline makse on **Settle avatud kannete** lehekülg, **1,00** kuvatakse selle **skonto summa võtta** välja. 

> [!NOTE] 
> Kui sisestate osaliselt ja jätta kogu arve summa on **summa lahendada** välja, on **skonto summa võtta** välja automaatselt ümber, kui kandeid sisestada.

## <a name="credit-notes-with-cash-discounts"></a>Skontodega kreeditarved
Võib-olla tagastate osa arvel olevatest kaupadest ja saate kreeditarve. Kui algse arve puhul arvestati skontot, lahutage skonto väärtus ja saate tagasimakse õiges summas. Kui selle ** arvutatakse skonto jaoks kreeditarveid ** määrangu **Jah** kohta on **Ostureskontro parameetrid** leht, allahindlus arvutatakse automaatselt kreeditarve. 

Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Sisestatud on arve summas 100,00. Kui kaup tagastada ja saada kreeditarve, saate sisestada algse arve 100.00, koos 2-% allahindlus ka määratletud kreeditarve kogusumma kreeditarve.  Kui vaatate kreeditarve on **paralleelkäibe** lehel **98.00** ilmub on **summa lahendada** välja, ja **-2.00** kuvatakse selle **skonto summa** välja. Allahindluse summa sisestatakse skontokontole.

## <a name="overpaymentunderpayment-amounts"></a>Üle-/alamakse summad
Võib‑olla teete osalise makse, mille puhul tasakaalustamist vajav osa on väga väike. Näiteks, kui hankija arve on summas 1000,00 ja maksate sellest 999,90. Kui järelejäänud summa on väiksem kui summa, mis on määratud üle- või alamaksete puhul leheküljel **Ostureskontro parameetrid**, sisestatakse erinevus automaatselt üle-/alamakse pearaamatukontole.


