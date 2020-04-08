---
title: Krediidihalduse parameetrite seadistus
description: See teema kirjeldab suvandeid, mida saate kasutada krediidihalduse konfigureerimiseks teie ettevõtte vajaduste täitmiseks.
author: mikefalkner
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6d4ced14e51dd28d51d2081d8e92891e31eea49d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154524"
---
# <a name="credit-management-parameters-setup"></a>Krediidihalduse parameetrite seadistus

[!include [banner](../includes/banner.md)]

See teema kirjeldab suvandeid, mida saate kasutada krediidihalduse konfigureerimiseks teie ettevõtte vajaduste täitmiseks. Krediidihalduse funktsioonide kasutamiseks seadistage parameetrid lehel **Krediidihalduse ja võlanõuete parameetrid** (**Krediidihaldus ja võlanõuded \> Seadistus \> Krediidihalduse ja võlanõuete parameetrid**).

## <a name="credit-parameters"></a>Krediidi parameetrid

Jaotises **Krediit** on neli kiirkaarti, kus saate muuta parameetreid, mis kontrollivad krediidihaldust: **Krediidihalduse ootelolekud**, **Krediidihalduse kontrollpunkt**, **Krediidihalduse statistika** ja **Krediidilimiidid**. Järgmistes jaotistes kirjeldatakse sätteid, mis on saadaval igal kiirkaardil.

### <a name="credit-holds"></a>Kreediti ootelolekud

- Seadistage suvand **Müügitellimuste väärtuse redigeerimise lubamine pärast tellimuse ooteloleku vabastamist** väärtusele **Jah**, et nõuda sisestamise reeglite uuesti kontrollimist, kui müügitellimuse väärtus (laiendatud hind) on pärast müügitellimuse ootelolekust vabastamist muutunud. .
- Valige väljal **Tühistatud tellimuste põhjused** vabastamise põhjus, mida kasutatakse vaikimisi siis, kui tühistatakse müügitellimus, mis oli krediidihaldusega seotud ooteloendis.
- Seadistage suvand **Kontrolli kliendi krediidigruppide krediidilimiiti** väärtuseks **Jah**, et kontrollida kliendi kreeditigrupi krediidilimiiti, kui müügitellimuse klient kuulub kliendi krediidigruppi. Grupi krediidilimiiti kontrollitakse ja kui see on piisav, kontrollitakse kliendi krediidilimiiti.
- Määrake suvand **Kontrolli krediidilimiiti, kui maksetingimused on suurenenud** väärtusele **Jah**, et kontrollida maksetingimuste reitingut, et teha kindlaks, kas müügitellimuse maksetingimused erinevad kliendi vaikimisi maksetingimustest. Kui uutel maksetingimustel on kõrgem reiting kui algsetel maksetingimustel, pannakse tellimus krediidihaldusega seotult ootele.
- Määrake suvand **Kontrolli krediidilimiiti, kui tasakaalustuse allahindlus on suurenenud** väärtusele **Jah**, et kontrollida tasakaalustuse allahindluse reitingut, et teha kindlaks, kas müügitellimuse skonto erineb kliendi vaikimisi skontost. Kui uuel skontol on kõrgem reiting kui algsel skontol, pannakse tellimus krediidihaldusega seotult ootele.
- Valige väljale **Muudetud tellimuste vabastamise põhjus** vabastamise põhjus, mida kasutatakse vaikimisis siis, kui muudetud tellimused vabastatakse automaatselt krediidihaldusega seotud ootelolekust.
- Seadistage suvand **Ignoreeri krediidiliimid aegunud blokeerimisreeglit, kui aegumiskuupäev on tühi** väärtusele **Jah**, et kontrollida reegli **Krediidilimiit aegunud** käitumist. Kui aegumiskuupäev on tühi, seadistage suvand tellimuse blokeerimiseks väärtusele **Ei**.
- Laohalduse puhul saab koormaid luua müügitellimuse sisestamise ajal. Seadistage suvand **Eemalda blokeeritud koorma read** väärtusele **Ei**, et jääta müügitellimuse read koormale, kui müügitellimus on krediidiga seotult ootel. Koormat ei saa töödelda, kui müügitellimus on ootel. Seadistage suvand väärtusele **Jah**, et eemaldada müügitellimuse read koormalt, kui müügitellimus on krediidiga seotult ootel. Koormat saab seejärel töödelda.
- Müügitellimusi saab krediidihalduse läbivaatusest automaatselt vabastada. Valige väljal **Automaatse vabastamise põhjus** vabastamise põhjus, mida kasutatakse vaikimisi juhul, kui müügitellimus automaatselt vabastatakse.
- Müügitellimusi saab krediidihalduse läbivaatusest automaatselt vabastada. Valige väljal **Vabasta automaatselt** väärtus **Sisestamata**, et vabastada tellimus ootelt. Tellimuse ootele panemise protsessi peate käsitsi käivitama. Valige **Sisestamisega**, et sisestada tellimus kasutades sama sisestamisprotsessi, mida kasutatud müügitellimuse ootele panemisel..

### <a name="credit-management-checkpoint"></a>Krediidihalduse kontrollpunkt

Saate seadistada aja, mida kasutatakse müügitellimuste krediidiprobleemide kontrollimiseks. Kiirkaart **Krediidihalduse kontrollpunkt** tuvastab dokumendi sisestamise protsessid, mis sisaldavad krediidihalduse reeglite töötlemist. Saate kontrollida krediidi reegleid ka siis, kui teete kas müügitellimuse esialgset sisestamist või täielikku sisestamist. Valige märkeruudud, et määratleta sisestusprotsessid, mis peaksid panema tellimuse ootele, kui pärast krediidihalduse blokeerimise reeglite töötlemist leitakse probleem.

Samuti saate määratleda ajapikenduse päevade arvu, enne kui krediidi reegleid uuesti kontrollitakse. Kuigi saate määrata, et kreeditihalduse reegleid kontrollitakse sisestamise ajal, ei kontrollita reegleid määratud arvu ajapikenduse päevade jooksul. Näiteks kinnitate müügitellimuse 1. päeval ja määrate kinnitamise etapiks kaks ajapikenduse päeva. Sel juhul ei kontrollita järgmise sisestamise etapis krediidi reegleid (näiteks saatelehe loomisel või tellimuse arve esitamisel) kuni 4. päevani. 4. päeval või pärast seda kontrollitakse reegleid sisestamisel uuesti ja ajapikenduse päevade arvu muudetakse järgmise sisestamise kontrollpunkti jaoks määratud väärtusele.

Kui te ei määra ajapikenduse päevade arvu, siis kontrollitakse krediidi reegleid igal sisestamise etapil, mis on seadistatud krediidihalduse reegleid käivitama. Kui vabastate müügitellimuse sisestamata ja käitate sama tellimuse töötlemise sammu uuesti, kontrollitakse krediidi reegleid uuesti. Näiteks pannakse tellimus pärast kinnitamist ootele ja te vabastate selle kas sisestamisega või ilma. Sellisel juhul pannakse tellimus uuesti ootele, kui selle uuesti kinnitate. Kasutage ajapikendust, kui tellimus peaks edasi liikuma järgmisesse töötluse etappi, ilma et seda jälle ootele pannakse.

Te ei saa määrata ajapikenduse päevi ainult osadele sisestamise kontrollpunktidele. Peate seadistama kõik sisestamise kontrollpunktid nii, et neil on ajapikenduse päevad, või seadistama need nii, et neil ei ole ajapikenduse päevi.

- Märkige ruut **Sisestamine**, et käitada krediidihalduse reegleid siis kui käivitatakse real näidatud sisestamise kontrollpunkt. Kui te märkeruutu ei märgi, kontrollitakse reegleid ainult üks kord kogu sisestamise protsessi jooksul.
- Kui märgite ruudu **Sisestamine**, määrake ajapikenduse päevade arv, mis peaksid mööduma enne blokeerimise reeglite uuesti kontrollimist. Kui märkeruut **Sisestamine** on tühjendatud, ei saa te ajapikenduse päevi lisada.
- Märkige ruut **Esialgne**, et käitada krediidihalduse reegleid siis kui käivitatakse real näidatud esialgse sisestamise kontrollpunkt. Enamikul juhtudel on müügitellimuse sisestamisel kuvatava dialoogikasti väli **Sisestamine** seadistatud väärtusele **Ei**.
- Kui märgite ruudu **Sisestamine**, määrake ajapikenduse päevade arv, mis peaksid mööduma enne blokeerimise reeglite uuesti kontrollimist. Kui märkeruut **Sisestamine** on tühjendatud, ei saa te ajapikenduse päevi lisada.

### <a name="credit-management-statistics"></a>Krediidihalduse statistika

**Kliendi krediidihalduse statistika** kiirinfo lehel **Klient** sisaldab mitut krediidihalduse statistikat. Peate määrama mitu väärtust, mis on vajalikud nende statistikate arvutamiseks. Sisestage kuude arv, mida kasutatakse järgmiste väärtuste arvutamiseks kiirinfos **Kliendi krediidihalduse statistika**.

1. Laekumata müügi päevad 1
2. Laekumata müügi päevad 2
3. Keskmine saldo 1
4. Keskmine saldo 2
5. Keskmine krediidilimiidi %
6. Keskmine kokkupuute %

### <a name="credit-limits"></a>Krediidilimiidid

- Kreeditihalduses kuvatakse kliendi krediidilimiit kliendi valuutas. Peate määratlema krediidilimiidi vahetuskursi tüübi kliendi valuutas. Väljal **Krediidilimiiti vahetuskursi tüüp** valige vahetuskursi tüüp, mida tuleks kasutada esmase krediidilimiidi teisendamiseks kliendi krediidilimiidiks.
- Seadke suvand **Luba krediidilimiitide käsitsi redigeerimine** väärtusele **Ei** et takistada kasutajatel muuta krediidilimiiti lehel **Klient**. Kui see valik on seadistatud väärtusele **Ei**, saab kliendi krediidilimiidi muudatusi teha ainult krediidilimiidi korrigeerimise kannete sisestamisega.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numbriseeriad ja jagatud numbriseeria parameetrid

Krediidilimiidi korrektsioonide töötlemiseks on vajalik töölehe ID. Peate lisama krediidilimiidi korrigeerimise numbri, mida tuleks kasutada töölehe ID loomiseks.
