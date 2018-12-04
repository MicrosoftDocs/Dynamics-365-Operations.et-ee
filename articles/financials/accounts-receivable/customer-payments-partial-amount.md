---
title: Kliendi osalises summas maksed
description: "Mõnikord teevad kliendid makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymEntry
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 6b7494a05392cbee70e6d5883bae0295e8b55ac9
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---

# <a name="customer-payments-for-a-partial-amount"></a>Kliendi osalises summas maksed

[!include [banner](../includes/banner.md)]

Mõnikord teevad kliendid makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist.

<a name="partial-payment-with-no-discount"></a>Allahindluseta osalised maksed
--------------------------------

Kliendid võivad teha osalise makse, sest neil ei pruugi olla kogu arve maksmiseks piisavalt sularaha või kuna arvel oleva kauba üle on vaidlus. Sellises olukorras saab arve maksega osaliselt tasakaalustada. Arve jääb avatuks ja näitab saldot.

## <a name="discount-amounts"></a>Allahindluse summad
Saate pakkuda klientidele enne tähtaegselt tasutud arve puhul skontot. Näiteks sisestate arve summas 100,00, millel on määratud skonto 2%, kui arve tasutakse 10 päeva jooksul. Tähtaeg on 30 päeva. Kui saate makse 98,00 10 päeva jooksul, sisestate makse 98,00. Kui arve on tasakaalustamiseks märgitud, võetakse skonto automaatselt.

## <a name="partial-payments-with-cash-discounts"></a>Osalised maksed skontodega
Osalise makse tegemisel kavatsevad kliendid ilmselt teha täiendava osamakse arve täielikuks tasakaalustamiseks. Osamakse puhul skonto kasutamiseks seadke lehel **Müügireskontro parameetrid** jaotise **Arvuta skontod osaliste maksete jaoks** suvandi väärtuseks **Jah**. 

Näiteks pakute 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Arve summas 100,00 on sisestatud. Kui saate makse 49,00 10 päeva jooksul, sisestate krediidi 49,00 maksetöölehele. Kui tasakaalustate osalise makse lehel **Kannete tasakaalustamine**, ilmub **1,00** väljale **Skonto summa võtmiseks**. Allahindluse summa sisestatakse skontokontole. 

> [!NOTE] 
> . Kui sisestate osalise makse ja jätate täieliku arve summa väljale **Tasakaalustatav summa**, arvutatakse väli **Skonto summa võtmiseks** automaatselt ümber, kui kanded sisestate.

## <a name="credit-notes-with-discounts"></a>Allahindlustega kreeditarved
Kui kliendid tagastavad osa arvel olevatest kaupadest, võite väljastada kreeditarve. Kui skonto võeti algselt arvelt, peab kliendi krediiditeatis olema kliendi võetud skonto netosumma. Kui lehe **Müügireskontro parameetrid** jaotise **Arvuta skontod kreeditarvete jaoks** suvandi väärtuseks on seatud **Jah**, arvutatakse kreeditarve jaoks automaatselt allahindlus. 

Näiteks pakkusite maksetingimusi, mis määravad 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Sisestati arve 100,00 ja klient võttis skonto. Kui klient tagastab kaubad ja väljastate kreeditarve, saate sisestada kreeditarve –100,00. Kui vaatate kreeditarvet lehel **Avatud kannete tasakaalustamine**, ilmub **98,00** väljale **Tasakaalustatav summa** ja **–2,00** ilmub väljale **Skonto summa**. Allahindluse summa sisestatakse skontokontole.

## <a name="overpaymentunderpayment-amounts"></a>Üle-/alamakse summad
Kui kliendid teevad makse, võib olla väga väike summa, mis tuleb tasakaalustada. Näiteks esitate kliendile arve 1000,00 ja klient maksab 999,90. Kui järelejäänud summa on väiksem kui summa, mis on määratud üle- või alamaksete puhul lehel **Müügireskontro parameetrid**, sisestatakse erinevus automaatselt üle-/alamakse pearaamatukontole.

## <a name="full-settlement"></a>Täielik tasakaalustamine
Kliendid võivad teha osalise makse, mille puhul järelejäänud summat ei maksta, kuid mis on suurem kui alamakse summa, mis on määratud lehel **Ostureskontro parameetrid**. Kui soovite märkida arve täielikult tasakaalustatuks, kasutage valikut **Täielik tasakaalustamine** lehel **Kannete tasakaalustamine**. (Saate lubada täieliku tasakaalustamise funktsiooni, kasutades konfiguratsioonivõtit.) Näiteks sisestatakse arve summas 1000,00 ja klient maksab 990,00. Olete kokku leppinud, et klient ei pea maksma järelejäänud summat 10,00. Pärast tasakaalustatava arve märkimist saate märkida ka valiku **Täielik tasakaalustamine**. Arvet käsitletakse siis täielikult tasakaalustatuna. Erinevus 10,00 sisestatakse skonto kontole täiendava skonto summana.


Lisateabe saamiseks vt [Kliendimaksete hoiustamine](tasks/deposit-customer-payments.md).

