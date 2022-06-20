---
title: Töö tükeldamine
description: See artikkel annab teavet töö tükeldamise funktsioonide kohta. See funktsioon võimaldab teil tükeldada suured töötellimused mitmeks väiksemaks töötellimuseks, mille saate määrata mitmele lao töötajale. Sel viisil saab sama tööd üheaegselt komplekteerida mitu lao töötajat.
author: Mirzaab
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 83333f4d8c755bc0ca4b2d141a5591ef43501b64
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857021"
---
# <a name="work-split"></a>Töö tükeldamine

[!include [banner](../includes/banner.md)]

Töö jaotamise funktsioon võimaldab teil tükeldada suured töö ID-d (mitmete ridadega töötellimused) mitmeks väiksemaks töö ID-deks, mille saate määrata mitmele lao töötajale. Sel viisil saab sama töönumbrit üheaegselt komplekteerida mitu lao töötajat.

> [!IMPORTANT]
> Saate tükeldada ainult töötellimusi, mille olek on *Avatud* või *Töös*.

## <a name="turn-on-the-work-split-functionality"></a>Töö tükeldamise funktsioonide sisselülitamine

Enne töö tükeldamise funktsiooni kasutamist peate oma süsteemis sisse lülitama funktsiooni ja selle eeltingimuse funktsiooni. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja vajadusel neid sisse lülitada.

Esmalt lülitage sisse eeltingimuste *Organisatsiooniülene töö blokeerimise* funktsioon, kui see ei ole juba sisse lülitatud. Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon kohustuslik, seega on see vaikimisi sisse lülitatud ja seda ei saa enam välja lülitada. Kuid see funktsioon on siiski funktsioonihalduses [loetletud](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmisel viisil:

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Organisatsiooniülene töö blokeerimine*

> [!NOTE]
> Kui see funktsioon on aktiveeritud, rakendatakse automaatset uuendamist pärast seda, kui funktsioon on kõigis juriidilistes isikutes sisse lülitatud.

Järgmisena lülitage sisse *Töö tükeldamise* funktsioon, mis on loetletud järgmisel viisil:

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Töö tükeldamine*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Töö üksikasjade ja kõigi töölehtede täiustused

Funktsioon *Töö tükeldamine* lisab järgmised kaks nuppu tegumiriba **Töö** vahekaardil **Töö üksikasjade** ja **Kogu töö** lehtedele:

- **Töö tükeldamine** – Tükeldage käesolev töö ID mitmeks väiksemaks töö ID-ks, mida saavad töödelda erinevad töötajad.
- **Tühista töö tükeldamise seanss** – Tühistage töö tükeldamise seanss ja tehke töö töötlemiseks saadaolevaks.

![Töö tükeldamise ja töö tükeldamise seansi tühistamise nupud.](media/Work_split_buttons.png "Töö tükeldamise ja töö tükeldamise seansi tühistamise nupud")

> [!IMPORTANT]
> **Töö tükeldamise** nupp ei ole saadaval, kui on täidetud mõni järgmistest tingimustest:
>
> - Töö olek on midagi muud, kui *Avatud* või *Täitmisel*.
> - Konteineri ID on seotud töö ID-ga. (Konteinerit ei saa süstemaatiliselt tükeldada, kuna see nõuab füüsilisi tegevusi.)
> - Töö on seotud kogumiga.
> - Töö tellimuse tüüp on midagi muud kui üks järgmistest tüüpidest:
>
>    - Müügitellimused
>    - Toormaterjalide komplekteerimine
>    - Edastuse väljaminek
>
> - Töö on hetkel tükeldatud teise kasutaja poolt. Kui proovite avada tükeldamise lehte töö jaoks, mida teine kasutaja juba tükeldab, kuvatakse järgmine tõrketeade: "Töö ID-ga \#\#\#\# on hetkel tükeldatud. Proovige mõne minuti pärast uuesti. Kui saate pidevalt seda teadet, võtke ühendust juhendajaga."

Uus töö blokeerimise põhjus, *Tükeldatud töö*, näitab, millal on töö ID tükeldamise protsessis. See kuvatakse **Töö tükeldamise** lehel kui ka mobiilirakenduses Warehouse Management, kui kasutaja proovib tööd teha. Blokeerimise põhjuste kasutamisel muudetakse **Blokeeritud voo** välja nimi töö ID-lt olekusse **Blokeeritud**.

## <a name="initiate-a-work-split"></a>Alusta töö tükeldamist

Funktsioon lisab uue **Töö tükeldamise** lehe, mis võimaldab kasutajatel tükeldada tööridu töö ID-st. Kui leht avatakse esmakordselt, kuvatakse read, millel on tööolek *Avatud* ja mis on saadaval tükeldamiseks. Valitud töö töötlemiseks valige tegumiribal **Töö tükeldamine**.

Töö tükeldamiseks toimige järgmiselt.

1. Avage üks järgmistest töölehtedest:

    - **Töö üksikasjad** (**Laohaldus \> Töö \> Töö üksikasjad**)
    - **Kogu töö** (**Laohaldus \> Töö \> Kogu töö**)

1. Valige ruudustikus tükeldamiseks töö ID. Välja **Töö tellimuse tüüp** väärtuseks peab olema seatud üks järgmistest väärtustest:

    - Müügitellimused
    - Toormaterjalide komplekteerimine
    - Edastuse väljaminek

1. Valige tegumiribal **Töö** vahekaardil **Töö** grupis olev üksus **Töö tükeldamine**.

    Kuvatakse leht **Töö tükeldamine** ja kuvatakse avatud ja tükeldamiseks saadaolevad tööread. Vaikimisi kuvatakse ainult saadaolevad tööread. Töö ID kõigi ridade vaatamiseks (näiteks read, millel on töö tüüp *Komplekteeri*), märkige ruudustiku kohal olev **Näita kõiki ridu** märkeruut.

    Kuvatakse järgmine teade: "kasutajad ei saa töö ridu töödelda seni, kuni lõpetate selle lehe tükeldamise ja sulgete."

    **Töö blokeerimise põhjuse** väli praeguse töö jaoks seatakse olekusse *Töö tükeldamine* ja töö blokeeritakse.

    ![Blokeerimise põhjus.](media/Blocking_reason.png "Blokeerimise põhjus")

1. Valige praeguse töö ID-lt eemaldatav rida ja lisage uus töö ID. Toimub järgmine:

    - Kui tükeldate töö, tühistatakse valitud rida või read algsest töö ID-lt ja kopeeritakse seejärel uuele töö ID-le.
    - Säilitatakse olemasoleva töömalli struktuur ja pannakse (ja ka tulevaste komplekteerimise/komplekteerimispaari) asukoht. Järgmise töö ID väljade väärtused kopeeritakse algsest tööst uuele tööle:

        - Koorma ID
        - Saadetise ID
        - Töötellimuse tüüp
        - Tellimuse kood
        - Laoala
        - Ladu
        - Töö prioriteet
        - Töökausta ID
        - Voo ID
        - Töö loomise number

    - Järgmisi välju ei kopeerita uuele töö ID-le:

        - **Töö ID** – Uus töö ID luuakse vastavast numbriseeriast.
        - **Töö olek** – Selle välja väärtuseks on seatud *Ava*.
        - **Lukustatud** – Selle välja väärtus on algselt tühi.
        - **Sihtkoha identifitseerimisnumber** – Väli jäetakse tühjaks.
        - **Loomise kuupäev ja kellaaeg** – See väli seatakse praegusele kuupäevale ja kellaajale.
        - **Blokeeritud voog/külmutatud** – See väli arvutatakse ümber algse töö ID ja uue töö ID jaoks.

1. Valige toimingupaanilt suvand **Töö tükeldamine**.

Kui tööd tükeldatakse, kuvatakse järgmine teade: "Töötlemise toiming – Töö tükeldamine". Kui see teade on nähtav, saate toimingu tühistada, kui valite sõnumiaknas **Tühista**.

Kui märkeruut **Kuva kõik read** on tühjendatud, ei kuvata enam ruudustikus tükeldatud ja tühistatud rida. Kui see ruut on märgitud, peaksite nägema, et selle rea **Töö oleku** välja väärtus on muudetud olekusse *Tühistatud*.

Kuvatakse järgmine teatis, mis näitab, et uus töö ID on loodud: "Töö \#\#\#\# on loodud algsest tööst lahutamise teel \#\#\#\#."

Muid tööridu algsest töö ID-st (nt *Asetamise* read) korrigeeritakse vastavalt vajadusele, et kajastada tühistatud töö ridu. Näiteks kui algse töö ID, millel oli *Liigutamise* rida kogusele 15 ja *Komplekteerimise* rea kogumahuga 10, tühistatakse, siis on algse töö *Liigutamise* uus kogus on nüüd 5.

Uut tööd ei määrata kohe ühelegi kasutajale. Saate siiski vastavalt vajadusele määrata selle kasutajale kohe, kasutades lehe **Töö üksikasjade** lehe standardfunktsioone.

> [!IMPORTANT]
> Saate tükeldada ainult töö ID-sid, mis sisaldavad kaht või enamat saadaolevat töörida. Kui valite **Töö tükeldamine**, kui on ainult üks töörida, kuvatakse järgmine tõrketeade: "Vähemalt üks töörida peab jääma algsele tööle." Sel juhul tükeldamist ei toimu.

## <a name="finish-a-work-split"></a>Lõpeta töö tükeldamine

Töö tükeldamise lõpetamiseks tuleb eemaldada *Töö tükeldamise* blokeerimise põhjus. Selle sammu läbimiseks on kaks võimalust:

- Kasutaja, kes tükeldab tööd saab **Töö tükeldamise** lehe sulgeda, klõpsates **Sulge** nuppu (**X**) ülemises parempoolses nurgas. Kui leht on suletud, eemaldatakse *Töö tükeldamise* blokeerimise põhjus. Selle töö *Blokeeritud* olek arvutatakse ümber ja kui selle töö jaoks ei ole järelejäänud blokeerimise põhjusi, siis on töö blokeerimata.
- Iga kasutaja avab töö ID ja valib tegumiribalt **Tühista töö tükeldamise sessioon** nupu. *Töö tükeldamise* blokeerimise põhjus eemaldatakse ja selle töö *Blokeeringu* olek arvutatakse ümber, nagu ka siis, kui **Töö tükeldamise** lehekülg on suletud.

Pärast *Töö tükeldamise* blokeerimise põhjuse eemaldamist saab tööd mobiilsel seadmel käitada tingimusel, et Töö ID **Blokeeritud** olekuks on määratud *Ei*.

## <a name="user-blocking-on-the-warehouse-management-mobile-app"></a>Laohalduse mobiilirakenduse kasutaja blokeerimine

Kui proovite mobiilirakenduses Warehouse Management avada tükeldamise lehte töö ID-ga, mida teine kasutaja juba tükeldab, kuvatakse järgmine tõrketeade: "Töö ID \#\#\#\# on hetkel tükeldatud." Kui kuvatakse järgneb sõnum, vajutage **Tühista**. Seejärel saate jätkata teiste tööde töötlemist.

## <a name="other-blocked-operations"></a>Muud blokeeritud toimingud

Toimingud, mis muudavad tööridu, töö laokandeid või täiendamise linke, mis on seotud tööga, mis on tükeldatud, nurjuvad ja kuvatakse järgmine tõrketeade: "Töö ID-ga \#\#\#\# on praegu tükeldatud."


[!INCLUDE[footer-include](../../includes/footer-banner.md)]