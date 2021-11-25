---
title: Krediidihalduse seadistamine
description: See teema kirjeldab kreeditihalduseks vajalikku seadistust.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9e756b678786d2c5a8c5bb9e890ce988090c09
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753661"
---
# <a name="credit-management-setup"></a>Krediidihalduse seadistamine 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Krediidihalduse töövood

Krediidilimiidi korrigeerimiste haldamiseks kasutatavate töövoogude määratlemiseks avage **Krediit ja võlanõuded \> Seadistus \> Krediidihalduse töövood**.

- Saate luua töövoo, mis võimaldab teil üheainsa kinnitamisega kinnitada krediidilimiitide korrigeerimiste partii.
- Saate lisada töövoo rea tasemel, nii et krediidilimiidi korrigeerimisi saab kinnitada ükshaaval.
- Saate luua väljalaske töövoo, mis suunab ootelolekud automaatselt töövoo protsessi.

## <a name="blocking-rules"></a>Blokeerimise reeglid

### <a name="ranking-payment-terms"></a>Maksetingimuste hindamine

Saate müügitellimuse ootele panna, kui tellimuse maksetingimused ei vasta kliendi vaikimisi maksetingimustele. Siiski on vahel maksetingimused erinevad, kuid siiski piisavalt sarnased, et te ei soovi tellimust ootele panna. Saate järjestada maksetingimusi nii, et mõnel neist on sama aste, samas kui teistel on kõrgem või madalam aste.

Kui maksetingimuste reitingud on aktiivsed ja tellimuse maksetingimustel on kõrgem aste kui kliendi vaikimisi maksetingimustel, pannakse müügitellimused ootele.

Maksetingimuste järjestuse saate seadistada lehel **Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Maksetingimuste järjestamine**  

### <a name="ranking-settlement-discounts"></a>Tasakaalustuse allahindluste hindamine

Saate müügitellimuse ootele panna, kui tellimuse skonto ei vasta kliendi vaikimisi skontole. Siiski on vahel skontod erinevad, kuid siiski piisavalt sarnased, et te ei soovi tellimust ootele panna. Saate järjestada skontosid nii, et mõnel neist on sama aste, samas kui teistel on kõrgem või madalam aste.

Kui tasakaalustuste allahindlused on aktiivsed ja tellimuse skontol on kõrgem aste kui kliendi vaikimisi skontol, pannakse müügitellimused ootele.

Maksetingimuste järjestuse saate seadistada lehel **Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Tasakaalustuse allahindluste hindamine**  

## <a name="reasons"></a>Põhjused

Krediidihalduses kasutatakse mitut tüüpi põhjuseid.

- Ootelepaneku põhjused näitavad, miks müügitellimus ootele pandi.
- Vabastamise põhjused määratakse tellimusele, kui see ootelt vabastatakse.
- Oleku põhjused näitavad, miks kliendile teatud konto olek määrati.

Põhjuseid saate seadistada lehel **Krediidihalduse põhjused** (**Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Krediidihalduse põhjused**).

1. Valige väljal **Põhjuse tüüp** põhjuse tüüp: **Ootel**, **Vabasta** või **Olek**.
2. Sisestage väljale **Põhjus** põhjuse nimi.
3. Sisestage välja **Kirjeldus** põhjusekoodi kirjeldus.

## <a name="credit-management-groups"></a>Krediidihalduse grupid

Krediidihalduse gruppe kasutatakse nende klientide või kliendigruppide tuvastamiseks, kellel on samad krediidihalduse atribuudid. Näiteks saab krediidihalduse gruppe kasutada klientide blokeerimise ja välistamise krediidihalduse reeglite määratlemiseks.

Krediidihalduse gruppe saate luua lehel **Krediidihalduse grupid** (**Krediit ja võlanõuded \> Seadistus> Krediidihalduse seadistus \> Krediidihalduse grupid**).

1. Valige uue rea loomiseks suvand **Uus**.
2. Sisestage grupi ID. ID-l võib olla kuni 10 tähemärki.
3. Sisestage väljale **Kirjeldus** grupi nimi. Nimes võib olla kuni 60 tähemärki.

Krediidihalduse grupp määratakse kliendile vahekaardil **Krediit ja võlanõuded** lehel **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**).

## <a name="account-statuses"></a>Konto olekud

Saate luua konto olekuid kliendi konto kreediti seisu tuvastamiseks. Saate määrata oleku ja selle mõju arveldamisele ning ootel kättetoimetamise protsessidele. Konto olekuid saab kasutada ka kliendi blokeerimise reeglite määratlemiseks.

Konto olekuid saate luua lehel **Konto olekud** (**Krediit ja võlanõuded \> Seadistus> Krediidihalduse seadistus \> Konto olekud**).

1. Lisage konto olek ja sisestage kirjeldus, mis tähistab kliendi krediidi seisu. Näiteks kasutage **Normaalne**, et näidata, et klient on heas seisus ja avatud tellimustele kehtib standardne krediidihalduse töötlemine.
2. Valige väljadel **Arveldamine** ja **Tarne ootel** ooteloleku tüüp, mis peaks kehtima selle konto olekuga klientide korral. Võite panna ootele kogu töötlemise, panna ootele ainult arve töötlemise või üldse töötlemist ootele mitte panna, kui rakendatakse krediidilimiidi reegleid.

## <a name="scoring-groups"></a>Hindamisgrupid

Saate seada sisse punktigrupid riskifaktorite määratlemiseks ning kriteeriumid nende mõõtmiseks. Kui punktigruppi lisatakse andmeid kliendi kohta, arvutatakse iga riskifaktori kohta punktisumma ja kasutatakse seda kliendi riskigruppi panemiseks. Riskigruppi saab kasutada krediidiriski tuvastamiseks ja automaatsete krediidilimiitide arvutamiseks.

Punktigruppe saate luua lehel **Punktigrupid** (**Krediit ja võlanõuded \> Seadistus \> Krediidhalduse seadistus \> Risk \> Punktigrupid**).

1. Looge punktigrupp ja sisestage sellele nimi.
2. Punktigrupi täiendavaks kirjeldamiseks sisestage kirjeldus.
3. Valige grupi tüüp. On kaheksa eelmääratletud tüüpi. Saate valida ka **Kasutaja määratletud**, et määratleda teie organisatsioonile paremini sobiv grupi tüüp.
4. Valige punktisumma tüüp, et määratleda, kuidas punktgrupp riskiskoori arvutab. Valikud on järgmised:

    - **Vahemik** – kasutage seda valikut punktisumma arvutamiseks kasutatava väärtuste vahemiku määramiseks.
    - **Kasutaja määratletud** – kasutage seda valikut punktisumma juures kasutatavate väärtuste loendi käsitsi määratlemiseks.

5. Kui valisite punktisumma tüübiks **Vahemiku**, lisage read väärtuste vahemiku ja vastavate punktisummade määratlemiseks.

    1. Määrake väljal **Väärtusest** vahemiku madalaim väärtus.
    2. Määrake väljal **Väärtuseni** vahemiku kõrgeim väärtus.
    3. Sisestage väljale **Punktisumma** see punktisumma, mis tuleks määrata siis, kui esitatud väärtus langeb "väärtusest"/"väärtuseni" vahemikku.

    Kui valisite punktisumma tüübiks **Kasutaja määratletud**, lisage read kasutaja määratletud väärtuste ja vastavate punktisummade määratlemiseks.

    1. Sisestage väljale **Väärtus** kasutaja määratud väärtus, mis tuleks kliendi andmetest esitada.
    2. Sisestage väljale **Punktisumma** see punktisumma, mis tuleks määrata siis, kui esitatud väärtus langeb "väärtusest"/"väärtuseni" vahemikku.

## <a name="risk-classification"></a>Riski klassifikatsioon

Saate määratleda riskihindamised, mida saab klientidele nende riskiskoori põhjal määrata. Riskiskoori arvutamiseks võrreldakse kliendi andmeid iga punktigrupiga. Punktiskummad liidetakse kokku ja lõppskoori võrreldakse riskigrupi seadistuse väärtustega, et tuvastada riskigrupp, kuhu klient kuulub. Seejärel kasutatakse riskigrupi punktisummat kliendile krediidihalduse blokeerimise ja välistamise reeglite määramiseks.

Riskigruppe saate seadistada lehel **Riskihindamine** (**Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Risk \> Riskihindamine**).

1. Sisestage riskigrupi ID.
2. Riskigrupi täiendavaks selgitamiseks sisestage kirjeldus.
3. Sisestage see punktisummade vahemik, mida kasutatakse, et määrata, millised kliendid riskigruppi kuuluvad.
4. Valige riskigrupi indikaator, et määratleda riskigruppi tähistav sümbol.

## <a name="guaranteeinsurance-types"></a>Garantii/kindlustuse tüübid

Garantii/kindlustuse tüüpe saate seadistada lehel **Garantii/kindlustuse tüübid** (**Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Kindlustus ja garantiid \> Kindlustuse ja garantii tüübid**).

1. Sisestage garantii või kindlustuse tüüp, mis määratleb käendaja või kindlustusmaakleri nime.
2. Sisestage kirjeldus käendaja/kindlustusmaakleri kirjeldamiseks.

## <a name="coverage-types"></a>Laovarude tüübid

Kindlustuskatte tüüpe saab kasutada kindlustuspoliiside täiendavaks liigitamiseks. Neid ei saa kasutada garantiidega.

Kindlustuskatte tüüpe saate lisada lehel **Kindlustuskatte tüübid** (**Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Kindlustus ja garantiid \> Kindlustuskatte tüübid**).

1. Sisestage kindlustuskatte tüüp, et määratleda kindlustuskatte tüüp, mis tuleks lisada kindlustuse või garantiina.
2. Sisestage kirjeldus kindlustuskatte tüübi kirjeldamiseks.

## <a name="automatic-credit-limits"></a>Automaatselt määratud krediidilimiidid

Automaatsetele krediidilimiitidele saate luua kriteeriumid lehel **Automaatsed krediidilimiidid** (**Krediit ja võlanõuded \> Seadistus \> Krediidihalduse seadistus \> Risk \> Automaatsed krediidilimiidid**).

1. Valige riskigrupp, millele automaatne krediidilimiit tuleb määrata.
2. Valige automaatse krediidilimiidi valuuta. Saate samale riskigrupile luua mitu automaatset krediidilimiiti erinevates valuutades.
3. Sisestage tulu summa, mis tähistab maksimaalset ettevõtte tulu, mida saab selle automaatse krediidilimiidi puhul kasutada. Kui krediidilimiidid on loodud, võrreldakse tulu summat selle tulu väärtusega, mis asub lehel **Finantsid** (**Müügireskontro \> Kõik kliendid \> Kliendi valimine \> Üldine \> Statistika \> Finants**). Süsteem kasutab jaotises **Ülevaade** uusimat väärtust.

Järgige neid samme, et lisada ridu, mis esindavad krediidilimiiti, mis valitud kriteeriumide põhjal luuakse.

1. Valige punktigrupp, mis määratleb kliendi teabe, mida tuleks krediidilimiidi arvutamiseks kasutada.
2. Valige võrdlemise tehtemärk, mis määratleb, kuidas punktigrupi andmeid tuleks hinnata.
3. Sisestage väärtus, mida tuleks võrrelda punktigrupile määratletud väärtusega.
4. Sisestage krediidilimiit, mis tuleb määrata, kui kliendi andmed vastavad punktigrupile määratletud väärtusele. Näiteks loote automaatse krediidilimiidi punktigrupile **Madal**. Kui ettevõtluses tegutsemise aastad on üks punktigruppidest, saate määratleda rea, mis määrab krediidilimiidi 100 000, kui klient on tegutsenud viis aastat ja teise rea, mis määrab krediidilimiidi 200 000, kui klient on tegutsenud 10 aastat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
