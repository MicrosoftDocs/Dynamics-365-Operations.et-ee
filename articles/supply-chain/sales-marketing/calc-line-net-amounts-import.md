---
title: Arvuta müügitellimuste ja pakkumiste importimisel ümber rea netosummad
description: See artikkel kirjeldab, kas ja kuidas süsteem arvutab ümber rea netosummad müügitellimuste ja pakkumiste importimisel. See selgitab ka seda, kuidas saate kontrollida käitumist Microsofti erinevates versioonides Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719330"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Arvuta müügitellimuste ja pakkumiste importimisel ümber rea netosummad

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kas ja kuidas süsteem arvutab ümber rea netosummad müügitellimuste ja pakkumiste importimisel. See selgitab ka seda, kuidas saate kontrollida käitumist Microsofti erinevates versioonides Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Näitab, kuidas rea netosummade uuendusi impordil arvutatakse

Tarneahela halduse versioon 10.0.23 [tutvustas 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). See luks muutis tingimusi, **mille** alusel saab rea netosumma välja uuendada või ümber arvutada, kui imporditakse olemasolevate müügitellimuste ja pakkumiste uuendusi. Versioonis 10.0.29 saate *selle veaparanduse asendada, lülitades sisse impordifunktsiooni arvuta rea netosumma*. Sellel funktsioonil on sarnane mõju, kuid see annab globaalse sätte, mis võimaldab teil vajadusel naasta vana käitumise juurde. Kuigi uus käitumine muudab süsteemi töö intuitiivsemaks, võib see anda ootamatuid tulemusi konkreetsetes stsenaariumides, kus on täidetud kõik järgmised tingimused:

- *Andmeid, mis uuendavad olemasolevaid kirjeid, imporditakse müügitellimuse ridade V2,* müügipakkumise ridade *V2* *või* tagastustellimuse ridade üksuse kaudu, kasutades Open Data Protocoli (OData), kaasa arvatud olukorrad, kus kasutate topeltkirjutust, importimist/eksportimist Excelist ja mõningaid kolmanda osapoole integratsioone.
- [Kaubanduslepingu hindamispoliitikad](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)**·**, mis on sisse määratud, loovad muudatusepoliitika, mis piirab müügitellimuse ridade, müügipakkumise ridade ja/või tagastustellimuse ridade netosumma välja uuendusi. Tagastustellimuse ridade puhul arvutatakse alati netosumma **väli** ja seda ei saa käsitsi seada.
- **Imporditud** andmed hõlmavad ridade netosumma välja muudatusi või muudatusi (nt ühiku hind, kogus või allahindlus), **mis** põhjustab ridade netosumma välja väärtuse ümberarvutamise ühe või mitme olemasoleva rea kirje puhul.

Nendes konkreetsetes stsenaariumides on kaubanduslelepingu **hindamispoliitika mõjuks piirata rea netosumma välja** uuendusi. Seda piirangut nimetatakse muutuse *poliitikaks*. Selle poliitika tõttu, kui kasutate välja redigeerimiseks või ümberarvutamiseks kasutajaliidest, palub süsteem teil kinnitada, kas soovite seda muudatust teha. Kuid kirje importimisel peab süsteem teie eest valiku tegema. Enne versiooni 10.0.23 jätk süsteemi rea netosumma alati muutmata, v.a juhul, kui sissetuleva rea netosumma on 0 (null). Kuid uuemates versioonides uuendab või arvutab süsteem netosumma alati ümber vastavalt vajadusele, v.a juhul, kui seda pole eraldi juhendatud seda tegema. Kuigi uus käitumine on loogilisem, võib see põhjustada probleeme teile, kui juba käitate protsesse või integratsioone, mis eeldavad vanemat käitumist. See artikkel kirjeldab, kuidas taastada vana käitumist, kui peate.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Kontrolli rea netosummade kalkulatsioone versioonides 10.0.29 ja uuemates versioonides

Tarneahela halduse versioonis 10.0.29 *tutvustati funktsiooni nimega Arvuta rea netosumma impordil*. See funktsioon lisab suvandi nimega Arvuta rea **netosumma** müügireskontro **parameetrite lehele**. See valik võimaldab teil valida rea netosummade arvutamiseks importimisel uute ja pärandkäitumiste vahel.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Impordifunktsiooni sisse- või väljalülitamine rea netosumma arvutamise funktsioonis

Versioonile 10.0.29 *uuendamisel lülitatakse importimise funktsiooni rea netosumma arvutamine vaikimisi sisse ja rea netosumma arvutamise uue suvandi väärtuseks on* **algselt** seatud *Jah.* Säte *Jah* vastab uuele standardkäitumisele. See vastab süsteemi käitumisele, kui funktsioon on välja lülitatud, [välja arvatud parameetri CalculateLineAmount](#CalculateLineAmount) funktsioonide korral, nagu kirjeldatakse selles artiklis allpool. Säte *Ei* vasta süsteemi käitumisele enne versiooni 10.0.23 ja seda pakutakse peamiselt pärandintegratsiooni stsenaariumite toetamiseks.

Administraatorid saavad funktsioonifunktsiooni *halduse tööruumi abil sisse ja välja lülitada* funktsiooni arvutamisrea [netosumma](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Rea netosumma arvutamise suvandi seada

Kui impordi *funktsiooni Arvuta rea netosumma* on sisse lülitatud, saate järgmiste **sammude** abil seadistada suvandi Arvuta rea netosumma.

1. Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
1. Seadke vahekaardi **Hinnad** rea **netosumma arvutamiseks integratsiooni** **kiirkaardi kaudu suvand Arvuta rea** netosumma ühele järgmistest väärtustest:

    - *Jah* – süsteem arvutab ja uuendab alati vajaduse korral rea summasid. (Seetõttu ignoreerib see kaubanduslelepingu hindamispoliitikat.)
    - *Ei* – kui iga rea olemasolev või sissetulev netosumma on 0 (null), arvutatakse selle rea väärtus ümber teiste väärtuste (nt ühiku hind, kogus ja allahindlus) põhjal. Kui olemasolev või sissetulev netosumma erineb nullist ja muutuse poliitika on **seatud** rea netosumma väljale, siis seda välja ümber ei arvutata ega uuendata, isegi kui rea hinna, koguse ja/või allahindluse sissetulevad muudatused võivad anda võimaluse rea kogusumma ümber arvutada. Selline käitumine vastab versioonile 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a> Kuidas mõjutab rea netosumma arvutamine impordi funktsioonil parameetrit CalculateLineAmount?

Kui impordi *funktsiooni Arvuta rea netosumma* on sisse lülitatud, `CalculateLineAmount` ei mõjuta selle `SalesLine` ja tabelite `SalesQuotationLine` parameetri väärtus. Selle asemel kontrollib käitumist globaalselt suvand **Arvuta rea netosumma**, mida kirjeldatakse eelmises jaotises. Seega, kui funktsioon on sisse lülitatud, ei tohi te teha mingeid sõltuvusi väärtusest `CalculateLineAmount`.

*Kui impordi funktsiooni Arvuta rea netosumma on* välja lülitatud, `CalculateLineAmount``SalesLine``SalesQuotationLine` töötab ja tabelite parameeter nii, nagu seda teeb tarneahela halduse versioonides 10.0.23 kuni 10.0.28, nagu kirjeldatud järgmises jaotises.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Kontrollrea netosumma arvutused versioonides 10.0.28 ja varasemad

[Kui vigafiksi 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) versiooniga 10.0.23, sai võimalik valida, kuidas iga asjakohane andmeüksus rea netosummat redigeeriti või tuleb muude muudatuste tõttu (nt kauba uuendatud hinna) tõttu uuesti arvutada. Saate juhtida seda käitumist, määrates iga `CalculateLineAmount` rea jaoks uue parameetri ühele järgmistest väärtustest imporditud failis:

- **`CalculateLineAmount` = *1*** – **netosumma** väli real arvutatakse ja uuendatakse alati, sõltumata sellest, kas muudatuse poliitika on väljale seatud, ning sõltumata sissetuleva või olemasoleva rea netosumma väärtusest.
- **`CalculateLineAmount` = *0*** – kui mis tahes rea olemasolev või sissetulev netosumma on 0 (null), arvutatakse selle rea väärtus ümber teiste väärtuste (nt ühiku hind, kogus ja allahindlus) põhjal. Kui olemasolev või sissetulev netosumma erineb nullist ja muutuse poliitika on **seatud** rea netosumma väljale, siis seda välja ümber ei arvutata ega uuendata.  

Süsteemi käitumine sõltub teie tarneahela haldamise versioonist:

- Versioonis 10.0.22 `CalculateLineAmount`*ja varem on süsteemi väljaminek alati 0* ja `CalculateLineAmount`*selle väljaminek pole mingil juhul seatud 1-ks*.
- Versioonides 10.0.23 kuni 10.0.28 häälestab süsteem nii, nagu seatakse kõigi ridade puhul 1`CalculateLineAmount`, kus see pole impordifailis *selgesõnaliselt* seatud 0-ks *.*
