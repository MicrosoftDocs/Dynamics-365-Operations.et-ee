---
title: Kliendi osalises summas maksed
description: "Mõnikord teevad kliendid makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 7025072cd29aac4ceb13b5594c3e321350777cf1
ms.lasthandoff: 03/31/2017


---

# <a name="customer-payments-for-a-partial-amount"></a>Kliendi osalises summas maksed

Mõnikord teevad kliendid makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist.

<a name="partial-payment-with-no-discount"></a>Allahindluseta osalised maksed
--------------------------------

Kliendid võivad teha osalise makse, sest neil ei pruugi olla kogu arve maksmiseks piisavalt sularaha või kuna arvel oleva kauba üle on vaidlus. Sellises olukorras saab arve maksega osaliselt tasakaalustada. Arve jääb avatuks ja näitab saldot.

## <a name="discount-amounts"></a>Allahindluse summad
Saate pakkuda klientidele enne tähtaegselt tasutud arve puhul skontot. Näiteks sisestate arve summas 100,00, millel on määratud skonto 2%, kui arve tasutakse 10 päeva jooksul. Tähtaeg on 30 päeva. Kui saate makse 98,00 10 päeva jooksul, sisestate makse 98,00. Kui arve on tasakaalustamiseks märgitud, võetakse skonto automaatselt.

## <a name="partial-payments-with-cash-discounts"></a>Osalised maksed skontodega
Osalise makse tegemisel kavatsevad kliendid ilmselt teha täiendava osamakse arve täielikuks tasakaalustamiseks. Võtta osaliselt skonto, peate seadma selle ** osalise makse skonto arvutamiseks ** võimalus **Jah** kohta on **Müügireskontro parameetrid** lehel. 

Näiteks pakute 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Arve summas 100,00 on sisestatud. Kui saate makse 49,00 10 päeva jooksul, sisestate krediidi 49,00 maksetöölehele. Kui tasakaalustate osalise makse lehel **Kannete tasakaalustamine**, ilmub **1,00** väljale **Skonto summa võtmiseks**. Allahindluse summa sisestatakse skontokontole. 

> [!NOTE] 
> Kui sisestate osaliselt ja jätta kogu arve summa on **summa lahendada** välja, on **skonto summa võtta** välja automaatselt ümber, kui kandeid sisestada.

## <a name="credit-notes-with-discounts"></a>Allahindlustega kreeditarved
Kui kliendid tagastavad osa arvel olevatest kaupadest, võite väljastada kreeditarve. Kui skonto võeti algselt arvelt, peab kliendi krediiditeatis olema kliendi võetud skonto netosumma. Kui lehe **Müügireskontro parameetrid** jaotise **Arvuta skontod kreeditarvete jaoks** suvandi väärtuseks on seatud **Jah**, arvutatakse kreeditarve jaoks automaatselt allahindlus. 

Näiteks pakkusite maksetingimusi, mis määravad 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Sisestati arve 100,00 ja klient võttis skonto. Kui klient tagastab kaubad ja väljastate kreeditarve, saate sisestada kreeditarve –100,00. Kui vaatate kreeditarvet lehel **Avatud kannete tasakaalustamine**, ilmub** 98,00** väljale **Tasakaalustatav summa** ja **–2,00** ilmub väljale **Skonto summa**. Allahindluse summa sisestatakse skontokontole.

## <a name="overpaymentunderpayment-amounts"></a>Üle-/alamakse summad
Kui kliendid teevad makse, võib olla väga väike summa, mis tuleb tasakaalustada. Näiteks esitate kliendile arve 1000,00 ja klient maksab 999,90. Kui järelejäänud summa on väiksem kui summa, mis on määratud üle- või alamaksete puhul lehel **Müügireskontro parameetrid**, sisestatakse erinevus automaatselt üle-/alamakse pearaamatukontole.

## <a name="full-settlement"></a>Täielik tasakaalustamine
Hotelli võib teha osalise makse kui jääksummat ei maksta, kuid on määratud alamakse summa üle ning **moodustavad Ostureskontro parameetrid** lehel. Kui soovite märkida arve nagu täielikult tasakaalustatud, saate selle **täielik lahendamise** ostuoptsiooni on **kande tasakaalustamiseks** lehel. (Saate lubada täieliku tasakaalustamise funktsiooni, kasutades konfiguratsioonivõtit.) Näiteks sisestatakse arve summas 1000,00 ja klient maksab 990,00. Olete nõustunud, et klient ei ole maksta ülejäänud 10.00. Pärast arve tasakaalustamiseks, võite need märkida valige **lahendamise täis**. Arvet käsitletakse siis täielikult tasakaalustatuna. Erinevus 10,00 sisestatakse skonto kontole täiendava skonto summana.


