---
title: Ettemaksuarved vs ettemaksed
description: "See artikkel kirjeldab ja vastandab kahte meetodit, mida organisatsioonid saavad avansimaksete (ettemaksete) puhul kasutada. Ühe meetodi puhul peate looma ostutellimusega seotud ettemaksuarve. Teise meetodi puhul luuakse ettemaksu töölehekanded, luues töölehekanded ja märkides need ettemaksu töölehekanneteks."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="prepayment-invoices-vs-prepayments"></a>Ettemaksuarved vs ettemaksed

[!include[banner](../includes/banner.md)]


See artikkel kirjeldab ja vastandab kahte meetodit, mida organisatsioonid saavad avansimaksete (ettemaksete) puhul kasutada. Ühe meetodi puhul peate looma ostutellimusega seotud ettemaksuarve. Teise meetodi puhul luuakse ettemaksu töölehekanded, luues töölehekanded ja märkides need ettemaksu töölehekanneteks.

Organisatsioonid võivad väljastada hankijatele ettemakseid kaupade või teenuste eest enne nende täitmist. Hankijatele ettemaksete väljastamiseks on kaks võimalust. Riski vähendamiseks saate ettemakseid jälgida, määratledes ettemakse ostutellimusel. Selle meetodi puhul peate looma ostutellimusega seotud ettemaksuarve. Seda meetodit nimetatakse ettemaksuarvelduseks. Organisatsioonid, mis ei soovi ettemakseid nii täpselt jälgida või ei saa hankijalt ettemaksearvet, saavad ettemaksuarvelduse meetodi asemel kasutada ettemakse töölehekandeid. Ettemakse töölehekannete loomiseks looge töölehekanded ja märkige need ettemakse töölehekanneteks. Selle meetodi puhul ei saa te jälgida, millised hankija ettemaksed milliste ostutellimustega on seotud. Siiski saate märkida sisestatud makse tasakaalustamiseks ostutellimuse suhtes.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Ettemaksuarvelduse vs ettemaksete kasutamine
| Ettemaksearveldus                                                                | Ettemaksed                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Määratlege ostutellimusel ettemakse väärtus.                                    | Määratlege ostutellimusel ettemakse väärtus.                    |
| Võti: sisestada tuleb ettemaksuarve ja lõplik arve.                       | Ettemaksuarvet ei tule sisestada.                                    |
| Ettemaksukohustus on ettemaksukontol, mitte AP-kontol. | Ettemaksukohustus on AP-kontol.                  |
| Hankija saldo ei kajasta ettemakse väärtust protsessi käigus.     | Hankija saldo kajastab ettemakse väärtust protsessi käigus. |
| Ettemaksuarveldus on saadaval ainult jaotises Ostureskontro.                         | Ettemaksed on saadaval nii jaotises Ostureskontro kui ka Müügireskontro.    |

## <a name="overview-of-the-prepayment-process"></a>Ettemakseprotsessi ülevaade
Paljude riikide/piirkondade raamatupidamistava nõuab, et ettemakseid klientidelt või ettemakseid hankijatele ei sisestataks tavalistele klientide või hankijate koondkontodele. Selle asemel sisestatakse need ettemaksed pearaamatu kindlatele ettemaksukontodele. Müügi- või ostutellimuse loomisel väljastatakse kliendile või hankijalt arve. Arve maksmisel tühistatakse ettemakse pearaamatukontodel ettemakse ja käibemaksu ettemaksekanne ning arve summad sisestatakse automaatselt tavalistele koondkontodele. Toimige makse loomiseks järgmiselt.

1.  Seadistage maksete jaoks sisestusreeglid.
2.  Valige suvandites Müügireskontro parameetrid ja Ostureskontro parameetrid jaotises **Pearaamat ja käibemaks** uus sisestusreegel, kasutades parameetrit **Ettemaksega maksetöölehe sisestusreegel**.
3.  Looge maksetööleht ja seejärel uus makse.
4.  Saate tähistada makse ettemaksena. Kui makse on tähistatud ettemaksena, sisestatakse makse etappides 1 ja 2 seadistatud sisestusreeglis määratletud pearaamatukontodele. Kui makse on tähistatud ettemaksena, arvutatakse ka maksud. Mõnes riigis on nõutav, et maksud tuleb tasuda ettemakse registreerimisel, isegi kui arve puudub.
5.  Sisestage ettemakse.
6.  Valikuline: saate enne arve loomist makse ostutellimuse või müügitellimuse suhtes tasakaalustada. Kasutage müügitellimuse või ostutellimuse lehe tegevuspaanil valikut **Kannete tasakaalustamine**.
7.  Kui hankija on kaubad või teenused tarninud, registreerige arve. Kui tasakaalustasite ettemakse 6. etapis ostutellimuse või müügitellimuse suhtes, tasakaalustatakse ettemakse automaatselt teie loodud arve suhtes. Kui te ettemakset ostutellimuse või müügitellimuse suhtes ei tasakaalsutanud, saate selle arve suhtes käsitsi tasakaalustada, kasutades kliendi või hankija lehel jaotist **Kannete tasakaalustamine**. Ettemakse summa tühistatakse ajutiselt AP-/AR-pearaamatukontolt. Peale selle tühistatakse ka maksud, kui need on arvutatud, kuna arvel on tegelikud maksud.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Ettemaksuarvelduse protsessi ülevaade
Ettemaksuarved on levinud äritava. Hankija väljastab ettemaksuarved, et nõuda ostule deposiiti enne ostutellimuse täitmist. Näiteks võib mõni hankija nõuda ettemakset kohandatud kaupade või teenuste puhul. Kui hankija väljastab ettemakset nõudva arve, saate kasutada ettemaksuarvelduse funktsiooni. Ettemakse väärtuse saab määratleda ostutellimusel, siis registreeritakse ja tasutakse ettemaksuarve ja seejärel rakendatakse ettemaksuarve lõplikule arvele. Toimige makse loomiseks järgmiselt.

1.  Ostuagent loob, kinnitab ja seejärel edastab ostutellimuse, mille puhul nõudis hankija ettemakset. Ettemakse väärtus määratletakse ostutellimusel leppe osana.
2.  Hankija esitab ettemaksuarve.
3.  Ostureskontro koordinaator registreerib ettemaksuarve ostutellimuse suhtes ja seejärel tasutakse ettemaksuarve.
4.  Kui hankija on kaubad või teenused tarninud ja seotud hankijaarved on vastu võetud, rakendab ostureskontro koordinaator ettemaksesumma, mis on arve järgi juba tasutud.
5.  Ostureskontro koordinaator tasub ja tasakaalustab arve jääksumma.




