---
title: Krediidihalduse parameetrite seadistus
description: See artikkel kirjeldab valikuid, mida saab kasutada krediidihalduse konfigureerimiseks nii, et see vastaks teie äritegevuse nõuetele.
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8955518e7b5c0200d3827c1c22b7d150a09be244
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799541"
---
# <a name="credit-management-parameters-setup"></a>Krediidihalduse parameetrite seadistus

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab valikuid, mida saab kasutada krediidihalduse konfigureerimiseks nii, et see vastaks teie äritegevuse nõuetele. Krediidihalduse funktsioonide kasutamiseks seadistage parameetrid lehel **Krediidihalduse ja võlanõuete parameetrid** (**Krediidihaldus ja võlanõuded \> Seadistus \> Krediidihalduse ja võlanõuete parameetrid**).

## <a name="credit-parameters"></a>Krediidi parameetrid

Jaotises **Krediit** on neli kiirkaarti, kus saate muuta parameetreid, mis kontrollivad krediidihaldust: **Krediidihalduse ootelolekud**, **Krediidihalduse kontrollpunkt**, **Krediidihalduse statistika** ja **Krediidilimiidid**. Järgmistes jaotistes kirjeldatakse sätteid, mis on saadaval igal kiirkaardil.

### <a name="credit-holds"></a>Kreediti ootelolekud

- Seadistage suvand **Müügitellimuste väärtuse redigeerimise lubamine pärast tellimuse ooteloleku vabastamist** väärtusele **Ei**, et nõuda sisestamise reeglite uuesti kontrollimist, kui müügitellimuse väärtus (laiendatud hind) on pärast müügitellimuse ootelolekust vabastamist tõusnud.
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

Saate seadistada aja, mida kasutatakse müügitellimuste krediidiprobleemide kontrollimiseks. Kiirkaart **Krediidihalduse kontrollpunkt** tuvastab dokumendi sisestamise protsessid, mis sisaldavad krediidihalduse reeglite töötlemist. Saate kontrollida krediidi reegleid ka siis, kui teete kas müügitellimuse esialgset sisestamist või täielikku sisestamist. Märkige ruudud, et määrata sisestusprotsessid, mis peaksid tellimuse ootele panema, kui pärast krediidihalduse blokeerimisreeglite töötlemist leitakse probleem.

Samuti saate määratleda ajapikenduse päevade arvu, enne kui krediidi reegleid uuesti kontrollitakse. Kuigi saate määrata, et kreeditihalduse reegleid kontrollitakse sisestamise ajal, ei kontrollita reegleid määratud arvu ajapikenduse päevade jooksul. Näiteks kinnitate müügitellimuse ühel päeval ja määrate kinnitussammide jaoks kaks ajapikenduspäeva. Sel juhul ei kontrollita kreeditreeglit järgmisel sisestussampäeval (nt saatelehe loomine või tellimuse arveldamine) kuni nelja päevani. Neljal või päeval pärast seda kontrollitakse reegleid sisestamisel uuesti ja ajapikenduspäevade arv muudetakse väärtuseks, mis on määratud järgmisele sisestuse kontrollpunktile.

Kui te ei määra ajapikenduse päevade arvu, siis kontrollitakse krediidi reegleid igal sisestamise etapil, mis on seadistatud krediidihalduse reegleid käivitama. Kui vabastate müügitellimuse sisestamata ja käitate sama tellimuse töötlemise sammu uuesti, kontrollitakse krediidi reegleid uuesti. Näiteks pannakse tellimus pärast kinnitamist ootele ja te vabastate selle kas sisestamisega või ilma. Sellisel juhul pannakse tellimus uuesti ootele, kui selle uuesti kinnitate. Kasutage ajapikendust, kui tellimus peaks edasi liikuma järgmisesse töötluse etappi, ilma et seda jälle ootele pannakse.

> [!Note]
> Kui ühele sisestuse kontrollpunktile on sisestatud ajapikenduse päev, peavad kõigil sisestamiseks märgitud kontrollpunktidel olema ajapikenduspäevad.

- Krediidihalduse **reeglite** käivitamiseks real kuvatava sisestuskontrollipunkti käivitamisel märkige ruut Sisestamine. Kui te ruutu ei märgi, kontrollitakse reegleid ainult üks kord kogu sisestusprotsessi jooksul.
- Kui märgite ruudu **Sisestamine**, määrake ajapikenduspäevade arv, mis peab mööduma enne blokeerimisreeglite uuesti kontrollimist. Kui märkeruut Sisestamine on tühjendatud, ei saa ajapikenduspäevi **lisada**.
- Krediidihalduse **reeglite käivitamiseks rea soovitud pro forma kontrollpunkti käivitamisel märkige ruut Pro forma** . Enamikul juhtudel on müügitellimuse sisestamisel kuvatava dialoogikasti väli **Sisestamine** seadistatud väärtusele **Ei**.
- Kui märgite ruudu **Sisestamine**, määrake ajapikenduspäevade arv, mis peab mööduma enne blokeerimisreeglite uuesti kontrollimist. Kui märkeruut Sisestamine on tühjendatud, ei saa ajapikenduspäevi **lisada**.

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
- Kui krediidihalduse **blokeerimisreeglid on** märgitud, **eirake** varude reserveeringute ignoreerimiseks varude reserveeringuid. Sel juhul kontrollitakse koguseid ja lubatakse kontrollpunkti ajapikendusperioodid, sõltumata laovarude reserveeringu kogusest.
- Kui krediidihaldus on lubatud, kasutatakse **krediidilimiidi** ületamisel teate sätet ainult vabas vormis arvete töötlemiseks. Kuigi teated lisatakse müügitellimustele alles siis, kui kliendid on ületanud krediidilimiidi, ei blokeeri nende teadete olemasolu kinnitust, komplekteerimislehtede ja saatelehtede printimist või arvete sisestamist.

    Krediidihaldus on vaikimisi lubatud, kuid te saate selle keelata. Kui see on lubatud, kasutate krediidihalduse blokeerimisreeglit ja kontrollpunkte, et tuvastada, millal kliendid on ületanud krediidilimiiti. Kui see on keelatud, saavad teated, mis lisatakse müügitellimustele krediidilimiidi ületamisel teate sätte põhjal, aidata teil tuvastada, kui kliendid on **ületanud** oma krediidilimiiti.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numbriseeriad ja jagatud numbriseeria parameetrid

Krediidilimiidi korrektsioonide töötlemiseks on vajalik töölehe ID. Peate lisama krediidilimiidi korrigeerimise numbri, mida tuleks kasutada töölehe ID loomiseks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
