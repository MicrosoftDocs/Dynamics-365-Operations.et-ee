---
title: Ettemaksuarved vs. ettemaksed
description: See teema kirjeldab ja vastandab kahte meetodit, mida organisatsioonid saavad avansimaksete (ettemaksete) puhul kasutada.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a99e2d52aae925441fbe29ab712944f11317b3e3688c9a1913176a43dd8b5a37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737303"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Ettemaksuarved vs. ettemaksed

[!include [banner](../includes/banner.md)]

See teema kirjeldab ja vastandab kahte meetodit, mida organisatsioonid saavad avansimaksete (ettemaksete) puhul kasutada. Üks meetod loob ostutellimusega seotud ettemaksuarve. Teine meetod loob ettemaksu töölehekanded, luues töölehekanded ja märkides need ettemaksu töölehekanneteks.

Organisatsioonid võivad väljastada hankijatele ettemakseid kaupade või teenuste eest enne nende täitmist. Hankijatele ettemaksete väljastamiseks on kaks võimalust. Riski vähendamiseks saate ettemakseid jälgida, määratledes ettemakse ostutellimusel. Selle meetodi puhul peate looma ostutellimusega seotud ettemaksuarve. Seda meetodit nimetatakse ettemaksuarvelduseks. Organisatsioonid, mis ei soovi ettemakseid nii täpselt jälgida või ei saa hankijalt ettemaksearvet, saavad ettemaksuarvelduse meetodi asemel kasutada ettemakse töölehekandeid. Ettemakse töölehekannete loomiseks looge töölehekanded ja märkige need ettemakse töölehekanneteks. Selle meetodi puhul ei saa te jälgida, millised hankija ettemaksed milliste ostutellimustega on seotud. Siiski saate märkida sisestatud makse tasakaalustamiseks ostutellimuse suhtes.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Ettemaksuarvelduse vs ettemaksete kasutamine

| Ettemaksearveldus                                                                | Ettemaksed                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Määratlege ostutellimusel ettemakse väärtus.                                    | Määratlege ostutellimusel ettemakse väärtus.                    |
| Sisestada tuleb ettemaksuarve ja lõplik arve.                       | Ettemaksuarvet ei tule sisestada.                                    |
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
4.  Hankija saadab maksenõude, mida nimetatakse standardseks hankijaarveks. Kui hankija on kaubad või teenused tarninud ja seotud standardsed hankijaarved on vastu võetud, rakendab ostureskontro koordinaator ettemaksesumma, mis on standardarve järgi juba tasutud.
5.  Ostureskontro koordinaator tasub ja tasakaalustab standardarve jääksumma.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Häälestab parameetreid ettemakse arveldamisprotsessi lubamiseks.
Ettemaksekonto peab olema määratletud vahekaardil **Ostutellimus** lehel **Varude sisestamine** (**Laohaldus \> Seadistus \> Sisestamine\> Sisestamine**). Ettemaksukontot uuendatakse (tavaliselt debiteeritakse) ettemaksuarve sisestamisel. Ettemaksukonto saldo tühistatakse, kui sisestatakse ettemaksuarvele rakendatav standardarve. Kui te ei tasakaalusta ettemaksuarvet makseks enne ettemaksuarve rakendamist standardarvele, tühistatakse sisestatud ettemaksuarve raamatupidamiskirjed standardarve sisestamisel.

Poolelioleva koondkonto ostureskontro määratletakse profiilil **Hankija sisestus**. Vaike-sisestusreeglite määratlemiseks klõpsake suvandit **Ostureskonto \>Seadistus \> Ostureskonto parameetrid \>Pearaamat ja müügi vahekaart \> Sisestusreeglid ettemakse hankijaarvega**.

**Ettemakse rakenduse poliitika** näitab, kas süsteem rakendab tasakaalustatud ettemaksuarved automaatselt käsitsi loodud lõpparvele. Andmeüksust kasutades loodud arved ei viita **Ettemakse rakenduse poliitikale**. Peate käsitsi rakendama tasakaalustatud ettemaksuarvet arvetel, mis loodi andmeüksust kasutades. Poliitika määratlemiseks minge jaotisesse **Ostureskontro \>Seadistus \> Ostureskontro parameetrid \> Pearaamat ja müügi vahekaart  \> Ettemakse rakenduspoliitika**. Kui väli **Ettemakse rakenduspoliitika** on seatud väärtusele **Automaatne**, märgitakse ettemaksuarve automaatselt lõpliku arvega tasakaalustamiseks. Kui väli on seatud olekusse **Teavitus**, kuvatakse lõpliku arve loomisel visuaalne viide, et ettemaksuarve on rakenduse jaoks saadaval.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Ettemaksuarve teavet sisaldava ostutellimuse loomine
Kui hankija ütleb teile, et nad nõuavad ettemakset ostutellimuses sisalduvate kaupade ja teenuste eest, peate määratlema nendega seotud ostutellimuse ettemakse väärtuse. Avage **Ostureskontro \> Üldine \> Ostutellimus \> Kõik ostutellimused** ja otsige üles hankija ostutellimus. Valige toimingupaanil vahekaart **Ost** ja seejärel valige **Ettemakse**. Sisestage ettemakse teave, sh kirjeldus, ettemakse väärtus, kas ettemakse on fikseeritud summa või protsent ning ettemakse kategooria ID. 

Pange tähele, et ostutellimusele pole mitu ettemaksemääratlust lubatud. Kui teil on vaja lubada ostutellimusele mitu ettemakset, sisestage maksed, kasutades ettemaksuarve asemel maksetöölehte.

Ettemakse võib ostutellimuselt eemaldada, kui te ei ole juba makset sisestatud ettemaksuarve suhtes tasakaalustanud või sisestanud standardarve. Ettemakseteabe eemaldamiseks ostutellimusest valige **Ostureskonto \> Üldine \> Ostutellimused \> Kõik ostutellimused** ja otsige üles hankija ostutellimus. Valige toimingupaanil vahekaart **Ost** ja seejärel valige **Eemalda ettemakse**.

## <a name="create-and-post-a-prepayment-invoice"></a>Ettemaksuarve loomine ja sisestamine
Hankija ettemaksuarve kirjendamiseks minge **Hankija arve** lehele, valides suvandi **Ettemaksuarve** lehel **Ostutellimused** (**Ostureskonto \> Üldine \> Ostutellimused \> Kõik ostutellimused \> Vahekaart Arve \> Ettemaksuarve**). Sisestage ettemaksuarve teave, sh arve number. Ettemaksuarve puhul ei saa koguseid muuta. Kui hankija on arveldanud ostutellimusel määratletud ettemakse väärtuse osalise summa, saate ühikuhinda värskendada, et see kajastaks osaväärtust.

Hankija saldot ja ettemaksukontot uuendatakse (tavaliselt debiteeritakse) ettemaksuarve sisestamisel. Uuendatakse ka ostutellimuse ettemakse määratluses sisalduvat **Ettemakse avalduse** väärtust. Sisestatud ettemakse kande finantsdimensiooni vaikekirjed võetakse ostutellimuse päiseteabest.

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Ettemaksuarve maksete sisestamine ja tasakaalustamine
Järgmisena makstakse ettemaksuarve **Maksetöölehelt**. Maksetöölehtedele juurdepääsemiseks klõpsake **Ostureskonto \> Töölehted \> Maksed \> Maksetööleht**. Pärast makse tasakaalustuse sisestamist ettemaksuarvele uuendatakse ostutellimuse **Järelejäänud ettemakse avalduse** väärtus.

Enne ettemaksuarve standardarve sisestamist saate tühistada makse tasakaalustuse ettemaksuarvelt. Kuid pärast standardarve rakendamist ettemaksuarvele ei saa tühistada makse tasakaalustust ettemaksuarvelt.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Sisestage standardne hankijaarve ostutellimusele ja rakendage ettemaksuarve standardarvele
Kirjendage hankijalt saadud standardarve. Selle protsessi osana saate rakendada tasakaalustatud ettemaksuarvet hankijaarvele nii, et arve väärtust vähendatakse juba makstud summa võrra. Ettemaksearve rakendamine hankijaarvele tagab, et ettemaksuarve raamatupidamiskirjed tühistatakse.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Ettemaksuarve rakendamine pärast standardarve sisestamist
Kui unustate hankijaarve sisestamise ajal rakendada ettemakset standardsele hankijaarvele, on tasakaalustatud ettemakse saadaval kõigile selle hankija arvetele rakendamiseks lehel **Hankijad** (**Ostureskonto \> Üldine \> Hankijad \> Kõik hankijad \> Arve vahekaart \> Rakenda**).

## <a name="reversal-of-the-prepayment-application-process"></a>Ettemakse avalduse protsessi tühistamine
Kui peate ettemaksearve rakendamise standardarve osas tasakaalustuse tühistama või üldse tühistama, valige **Tühistamine** lehelt **Hankijad** (**Ostureskontro \> Üldine \> Hankijad \> Kõik hankijad \> Arve vahekaart \> Tühista**). Kui ettemaksutaotlus on tühistatud, saate ettemakset rakendada teisel standardarvel. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]