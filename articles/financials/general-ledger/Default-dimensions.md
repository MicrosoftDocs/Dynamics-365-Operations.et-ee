---
title: Finantsdimensioonid ja sisestamine
description: "Kontoplaani koostades ja häälestades peate arvestama sellega, kuidas erinevad komponendid dokumendi või tööraamatu sisestamisel koos toimivad. Need komponendid on konto struktuurid, täpsemad reeglid ning tasakaalustavad ja fikseeritud dimensioonid. Selles teemas selgitatakse, mis komponendid on ja kuidas need koos töötavad."
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fa494ab9c3b3f0540ec042f952344c15796845e6
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="financial-dimensions-and-posting"></a>Finantsdimensioonid ja sisestamine 

[!include[banner](../includes/banner.md)]

Kontoplaani koostades ja häälestades peate arvestama sellega, kuidas erinevad komponendid dokumendi või tööraamatu sisestamisel koos toimivad. Need komponendid on konto struktuurid, täpsemad reeglid ning tasakaalustavad ja fikseeritud dimensioonid. Selles teemas selgitatakse, mis komponendid on ja kuidas need koos töötavad.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Kontoplaani ja finantsdimensiooni komponendid

Rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition on põhikontode ja finantsdimensioonide väärtuste kehtivate kombinatsioonide määratlemiseks põhjalik reeglitepõhine süsteem. Selles teemas antakse lühiülevaade iga komponendi funktsioonidest ja sellest, kuidas komponenti leida.

### <a name="account-structures"></a>Konto struktuurid

Pearaamatut luues tuleb valida konto struktuur. Peate määratlema ja aktiveerima vähemalt ühe konto struktuuri ja määrama selle pearaamatule. Konto struktuur peab sisaldama põhikontot. Saate määratleda ettevõtte jaoks kõige sobivama segmentide järjekorra. Pärast põhikonto määratlemist saab süsteem määrata kindlaks kasutatava konto struktuuri. Põhikonto esimeseks või struktuuri alguse lähedale seadmine aitab piirata väärtuseid ja võimaldab süsteemil rakendada kõige hiljutisemat teadaolevat väärtust vaikeväärtusena. Konto struktuuris võib olla kuni 10 täiendavat finantsdimensiooni. Konto struktuur määrab selle, millised dimensiooniväärtused kehtivad koos muude väärtustega. See määratleb ka selle, kas dimensiooniväärtused tuleb sisestada.

### <a name="advanced-rules"></a>Täpsemad reeglid

Kontoplaani häälestamisel saab lisasuvandina kasutada täpsemaid reegleid. Konto struktuurile võite lisada nii palju täpsemaid reegleid, kui soovite. Täpsemaid reegleid kasutatakse sageli siis, kui finantsdimensioone peab kindlate kriteeriumite täitumise korral jälgima. Näiteks reisikulude konto kasutamisel saab jälgida lisainfot (nt üritus, kuhu töötaja sõidab). Kui täpsemaid reegleid on mitu, rakendatakse neid reeglite nimede põhiselt tähestikulises järjestuses. Reegli lisatavaid segmente saab rakendada alles pärast konto struktuuri segmente.

### <a name="balancing-dimension"></a>Tasakaalustusdimensioon

Saate vajadusel määratleda tasakaalustava finantsdimensiooni. Lehel **Pearaamat** saate määratleda tasakaalustamist vajava finantsdimensiooni. See tähendab, et iga kord kui sellesse finantsdimensiooni kandeid sisestatakse, loob ja sisestab süsteem automaatselt kandeid finantsdimensiooni tasakaalustamiseks.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Põhikontosse vaikimisi/fikseeritud finantsdimensioonide sisestamine

Vaikedimensioonid tulevad erinevatest kohtadest, näiteks põhikirjetest (nt kliendi või hankija kirjed), dokumendipäistest ja põhikontolt. Selles teemas käsitletakse põhikonto vaikedimensioone juriidilise isiku alusel. Saate määratleda, kas põhikonto väärtus on **Fikseerimata** või **Fikseeritud** iga finantsdimensiooni puhul, mida kasutatakse kõigis pearaamatu konto struktuurides. Kui finantsdimensioon on **Fikseerimata**, kasutatakse vaikeväärtust, mida saab üle kirjutada. See kehtib süsteemi kõigi, isegi põhikirjetest pärit vaikeväärtuste puhul. Kui finantsdimensiooni väärtus on **Fikseeritud**, rakendatakse alati seda väärtust, olenemata sellest, kas tegemist on mõne vaikeväärtuse või kasutaja poolt sisestatud väärtusega.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Vaikedimensioonide rakendamise järjekord sisestamise ajal

Erinevate komponentide käitamisjärjekord tekitab sageli küsimusi. On oluline mõista, millises järjekorras vaikedimensioone rakendatakse, sest sellest sõltub häälestamisel kasutatav lähenemine.

> [!NOTE]
> See teave kehtib ainult rakenduses vaikedimensioonide rakendamisel. Andmete Microsoft Excelist või rakendusest Data Management Network importimisel rakendamine erineb.

### <a name="example-1"></a>Näide 1

**Konto struktuur**

| Põhikonto            | Äriüksus           | Osakond              | Kulukeskus             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Kõik väärtused on lubatud. | Kõik väärtused on lubatud. | Kõik väärtused on lubatud. | Kõik väärtused on lubatud. |

**Põhikonto**

| Põhikonto | Nimi          | Juriidiline isik | Osakond                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Tootemüük | USMF         | Kinnitatud – 022 Müügi- ja turunduse osakond |

Järgmisel joonisel kujutatakse põhikontole 401100 seadistatud fikseeritud vaikedimensiooni.

[![Vaikimisi finantsdimensioonid](./media/default-dimensions.png)](./media/default-dimensions.png)

Käesolevas lihtsas näiteks sisestatakse üldin tööraamat, mille Osakonna dimensioon on häälestatud kasutama vaikeväärtust **023** (Operatsioonid). Koostatakse ja sisestatakse pearaamatukonto. Järgmisel joonisel kujutatakse vaikimisi finantsdimensiooni pearaamatu päises.

[![Päevaraamatud](./media/general-journal.png)](./media/general-journal.png)

Töölehe päises oleva vaikedimensiooni tõttu rakendatakse müügikonto real vaikimisi osakonda 023. Järgmisel joonisel kujutatakse üldise tööraamatu rida, kus rakendatakse päisest pärit dimensiooni vaikeväärtust **023**.

[![Töölehe kanne](./media/journal-voucher.png)](./media/journal-voucher.png)

Rea sisestamisel kasutatakse siiski fikseeritud dimensiooni ja rida sisestatakse osakonnale 022. Järgmisel joonisel kujutatakse sisestatud kannet, mille puhul rakendatakse müügikontole fikseeritud dimensiooni.

[![Pearaamatu kanded](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Näide 2

See näide kasutab esimesega sama malli. Küll aga on siia lisatud veel üks komponent: Osakonna dimensioon tasakaalustava dimensioonina. Järgmisel joonisel on dimensioon **Osakond** määratletud USMF-i pearaamatu tasakaalustava finantsdimensioonina.

[![Pearaamat](./media/ledger.png)](./media/ledger.png)

Kui kasutada sama töölehe päise seadistust ja sisestada sama kanne, siis rakendatakse esmalt fikseeritud dimensiooni. Sellisel juhul rakendatakse tasakaalustamise loogikat, et igal osakonnal oleks taskaalustatud sissekanne. Järgmisel joonisel kujutatakse kirjekandeid, milles sisaldub pärast fikseeritud dimensiooni rakendamist ka tasakaalustav kirje.

[![Pearaamatu kanded](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Näide 3

Selles näites lisatakse täpsem reegel. Täpsema reegli kohaselt peab süsteem jälgima lisasegmenti nimega Klient, juhul kui kasutatakse müügikontot 401100 ja osakonda 022 (Müük ja turundus).

See näite on järjekorra tõttu oluline. Konto struktuur määratletakse pärast põhikonto sisestamist. Konto struktuuri häälestusele viitamise korral käsitleb süsteem põhikontot, äriüksust, osakonda ja kulukeskust asjakohastena. Praegu ei ole täpsemat reeglit veel rakendatud, sest enne fikseeritud dimensioone rakendatakse tööraamatu kande sisestamisel vaikedimensioone. Järgmises näites puudub segment Klient, sest täpsema reegli kriteeriumid pole täidetud.

[![Pearaamatukonto](./media/drop-down.png)](./media/drop-down.png)

Sisestamine ei õnnestu, sest fikseeritud dimensiooni rakendati protsessi lõpus. Dimensiooni kontrollimise käigus selgub, et põhikonto 401100 ja osakonna 022 korral on nõutav Kliendi segment. Kontrolli käigus leitud tõrke tõttu ei saa sisestamine toimuda. Järgmisel joonisel kujutatakse pärast dimensiooni kontrolli kuvatavat teadet selle kohta, et Klient on nõutud segment.

[![Teate üksikasjad](./media/message.png)](./media/message.png)

Selle näite puhul tuleb vaikeväärtus täpsema reegli käivitamiseks ja segmenti Klient sisestamiseks üle kirjutada. Siiski ei saa seda lahendust alati kasutada ja mõned kasutajad ei teagi midagi sisestamisreeglite kohta. Seetõttu on oluline mõista, millises järjekorras vaikedimensioone kontoplaani häälestamisel rakendatakse.

Selles näites soovitu saavutamiseks saab konfiguratsiooni muuta mitmel viisil. Näiteks saab luua müügikontode jaoks uue konto struktuuri ja lisada struktuurile Kliendi segmendi. Samuti saate lisada ridu olemasolevale konto struktuurile ja määrata põhikonto ja kehtivad osakonnaväärtused. Täiendava kliendistruktuuri puhul võib seejärel olla kasu eraldi konto struktuurist Kliendi segmenti sisaldavate müügikontode jaoks.

## <a name="additional-resources"></a>Lisaressursid 

Mõnedes järgmistest teabematerjalidest viidatakse rakenduse Finance and Operations varasemale väljaandele. Küll aga kehtib suurem osa vaikedimensioonide rakendamise alasest teabest ja kasutatavatest kontseptsioonidest ka varasema väljaande kohta ja viited on endiselt asjakohased.

[Tasakaalustatud töölehed sisekäibe jaoks](example-balanced-journals-interunit-accounting.md)

[Kontoplaanide plaanimine](plan-chart-of-accounts.md) 

[Kontoplaani plaanimine AX 2012 ajaveebis](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – link viib seitsmeosalise seeria esimese osa juurde.

[Dimensiooni vaikeväärtused arvestuse jaotustes](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimensiooni vaikeväärtused dimensiooniraamistikus](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)

