---
title: Hankija osalises summas maksed
description: Mõnikord võite teha hankijale makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2644e0a27eff3e45ddcddb89c9aac9230190788f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318898"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Hankija osalises summas maksed

[!include [banner](../includes/banner.md)]

Mõnikord võite teha hankijale makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist. 

<a name="cash-discount-amounts"></a>Skonto summad
---------------------

Hankija võib pakkuda enne tähtaega tasutud arve puhul skontot. Näiteks sisestate arve summas 100,00 ja sellele on määratud skonto 2%, kui arve tasutakse kümne päeva jooksul. Tähtaeg on 30 päeva. Kui maksesoovitus kasutab arve valimise kriteeriumina sularaha allahindlust ja kui soovitus käivitatakse skonto kuupäeval või enne seda, valitakse arve maksmiseks ja makse luuakse summas 98,00. Skonto saab võtta ka ühekordse käsitsi loodud makse jaoks.

## <a name="partial-payments-with-cash-discounts"></a>Osalised maksed skontodega
Osalise makse tegemisel kavatsete ilmselt teha täiendava osamakse arve täielikuks tasakaalustamiseks. Osalise maksega skonto kasutamiseks valige leheküljel **Ostureskontro parameetrid** jaotise **Arvuta skontod osaliste maksete jaoks** suvand **Jah**. 

Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Arve summas 100,00 on sisestatud. Kui teete 10 päeva jooksul makse 49,00, sisestate maksetöölehele deebeti 49,00. Lehel **Avatud kannete tasakaalustamine** osalise makse tasakaalustamisel ilmub väljale **Skonto summa võtmiseks** väärtus **1,00**. 

> [!NOTE] 
> . Kui sisestate osalise makse ja jätate täieliku arve summa väljale **Tasakaalustatav summa**, arvutatakse väli **Skonto summa võtmiseks** automaatselt ümber, kui kanded sisestate.

## <a name="credit-notes-with-cash-discounts"></a>Skontodega kreeditarved
Võib-olla tagastate osa arvel olevatest kaupadest ja saate kreeditarve. Kui algse arve puhul arvestati skontot, lahutage skonto väärtus ja saate tagasimakse õiges summas. Kui lehekülje **Ostureskontro parameetrid** jaotise **Arvuta skontod kreeditarvete jaoks** suvandi väärtuseks on seatud **Jah**, arvutatakse skonto kreeditarve jaoks automaatselt. 

Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist. Sisestatud on arve summas 100,00. Kui tagastate kaubad ja saate kreeditarve, saate algse arve täissumma jaoks sisestada kreeditarve, mis on 100,00, pluss 2-protsendine skonto, mis määratletakse samuti krediiditeatisel.  Kui vaatate kreeditarvet lehel **Kannete tasakaalustamine**, ilmub **98,00** väljale **Tasakaalustatav summa** ja **–2,00** väljale **Skonto summa**. Allahindluse summa sisestatakse skontokontole.

## <a name="overpaymentunderpayment-amounts"></a>Üle-/alamakse summad
Võib‑olla teete osalise makse, mille puhul tasakaalustamist vajav osa on väga väike. Näiteks, kui hankija arve on summas 1000,00 ja maksate sellest 999,90. Kui järelejäänud summa on väiksem kui summa, mis on määratud üle- või alamaksete puhul leheküljel **Ostureskontro parameetrid**, sisestatakse erinevus automaatselt üle-/alamakse pearaamatukontole.


Lisateabe saamiseks vt [Hankijamaksete ülevaade](../cash-bank-management/tasks/vendor-payment-overview.md).
