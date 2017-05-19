---
title: Ettemaksuarved Ida-Euroopa puhul
description: "Ettemaksuarve on dokument, mille saate luua kliendile või hankijale. Sellel märgitakse summa, mis tuleb müügitellimuse puhul ette maksta. See teema annab teavet ettemaksuarvete kohta Ida-Euroopa puhul."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Operations, Core
ms.custom: 272643
ms.assetid: 00072155-f3d1-4d09-b848-5c086cac0891
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e794425b42266be49ff059d4bf539cc18fc26496
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="advance-invoices-for-eastern-europe"></a>Ettemaksuarved Ida-Euroopa puhul

[!include[banner](../includes/banner.md)]


Ettemaksuarve on dokument, mille saate luua kliendile või hankijale. Sellel märgitakse summa, mis tuleb müügitellimuse puhul ette maksta. See teema annab teavet ettemaksuarvete kohta Ida-Euroopa puhul.

Ettemaksuarve funktsioon võimalda teha järgmist.

-   Ettemaksuarvete väljastamine klientidele ja nende ettemaksuarvete oleku jälgimine (**Avatud**, **Osaliselt makstud** või **Suletud**).
-   Sisestage ettemaksuarve kanded ja käibemaksukanded (ainult Poola puhul).
-   Looge ettemaksuarve põhjal automaatselt maksetöölehe read.
-   Seostage klientidelt saadud ettemaksud ettemaksuarvetega (enne või pärast ettemaksu sisestamist).
-   Muutke käibemaksusisestust sisestatud ettemaksudtes (st teisendage ettemaksu makseks või makse ettemaksuks või muutke sisestamiskuupäeva, maksumäära või summat).
-   Looge maksudokument käibemaksuga maksustatavale tarnele (ainult Tšehhi Vabariik).

## <a name="advance-invoices-for-poland"></a>Ettemaksuarved Poola puhul
Ettemakse saavad Poola ettevõtted peavad looma kliendi jaoks ettemaksude arve. See ettemaksuarve sisestatakse pearaamatusse ja see on käibemaksu maksueesmärgil kohustuslik dokument. Ettemaksuarvel arvutatav maks tuleb teatada maksuhaldurile. Kaupade lõpliku müügi korral tuleb ettemaksuarve määrata müügiarvel. Müügi kogusumma peab sisaldama ettemakse. Müügiarve sisestamisel tühistatakse tasakaalustatud ettemaksuarve. Esialgne ettemaksuarve tasakaalustatakse koos ettemaksuarve tühistamisega.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Müügireskontro seadistamine ettemaksuarvete puhul
Määrake lehe **Müügireskontro parameetrid** vahekaardil **Värskendamine** järgmised parameetrid.

|Kiirkaart|Parameeter|Kirjeldus|
|------|----------|------------|
|Ettemaksuarve  |Sisestusreeglid|Saate valida sisestusreeglid, mida kasutada ettemaksuarvelduse puhul (ainult Poola). **Oluline.** Tšehhi Vabariigi ja Ungari puhul ei käsitleta ettemaksuarveid raamatupidamis- või maksudokumentidena ja neid ei sisestata pearaamatusse. Seetõttu peaksite selle välja nende riikide puhul tühjaks jätma, et vältida ettemaksuarvete sisestamist pearaamatusse.
|
|Ettemaksuarve  |Vastas-|konto        |Saate valida vaikevastaskonto täiustatud arveldamisega kasutamiseks.|
|Ettemaksuarve  |Käibemaksugrupp        |Saate valida käibemaksugrupi ettemaksuarvelduseks käibemaksu arvutamisel.|
|Ettemaksuarve  |Vastupidiseks muutmine parandusena |Märkige see ruut, kui ettemaksuarve tühistamist tuleb käsitleda parandusena.|
|Ettemaksuarve  |Tühista arvekuupäeval|Märkige see ruut, et tühistada ettemaks arve sisestamise kuupäeval.|
|Makse          |Mitu ettemaksukuupäeva|Tehke üks järgmistest valikutest: **Aktsepteeri**, **Hoiatus** või **Tõrge**.|
|Makse          |Kuupäeva sobimatus          |Tehke üks järgmistest valikutest: **Aktsepteeri**, **Hoiatus** või **Tõrge**.|
|Makse          |Summa sobimatus        |Tehke üks järgmistest valikutest: **Aktsepteeri**, **Hoiatus** või **Tõrge**.|
|Makse          |Sisestatud ettemaksuarvega seostamine|Tehke üks järgmistest valikutest: **Aktsepteeri**, **Hoiatus** või **Tõrge**.|
|Makse          |(CZE), (POL) Ettemaksu käsitlemine|Valige **Täpsem**.|

Seadistage numbriseeriad vahekaardil **Numbriseeriad** järgmiste viidete jaoks.

-   Maksudokument
-   Maksukrediiditeatis
-   Ettemaksuarve
-   Ettemaksuarve kreeditarve
-   Ettemaksuarve vastupidiseks muutmine
-   Ettemaksuarve kanne
-   Ettemaksuarve kreeditarve kanne
-   Ettemaksuarve tühistamiskanne

## <a name="create-a-customer-advance-invoice"></a>Kliendi ettemaksuarve loomine
Klõpsake valikuid **Müügireskontro** &gt; **Üldine** &gt; **Ettemaksuarved** &gt; **Kõik ettemaksuarved**. Uue ettemaksuarve loomiseks klõpsake toimingupaani vahekaardil **Ettemaksuarve** valikut **Ettemaksuarve**. Sisestage vajalik teave ja klõpsake ettemaksuarve sisestamiseks nuppu **Sisesta**. Ettemaksuarvel võib olla üks järgmistest olekutest: **Avatud**, **Osaliselt makstud** või **Suletud**. Sisestatud ettemaksuarve olekut saate käsitsi muuta. Klõpsake valikut **Olek** ja seejärel valige lehel **Ettemaksuarve oleku muutmine** väljal **Uus olek** ettemaksuarve uus olek. **Märkus.** Ettemaksuarve olekut saate muuta igal ajal. Suletud ettemaksuarveid kannetes ei saa töödelda. **Märkus.** Poola puhul luuakse ettemaksuarve kanded siis, kui seadistate jaotises Müügireskontro parameetrid ettemaksuarvete jaoks sisestusreeglid. Sisestatud kannete vaatamiseks klõpsake lehel **Ettemaksuarve** valikut **Kanne**.

## <a name="vat-on-advance-invoices"></a>Käibemaks ettemaksuarvetel
Ettevõtted peavad kirjendama käibemaksu klientide ettemaksudel, isegi kui müük pole veel lõpule viidud. Ettemaksult käibemaksu sisestamiseks saate lisada ettemaksuarvele rea, mis sisaldab käibemaksu spetsifikatsioone. Ettemaksuarvel võib olla mitu rida ja read võivad sisaldada käibemaksu spetsifikatsioone, mis võetakse müügitellimuse ridadelt. Seega saate sisestada käibemaksu ettemaksult täpselt vastavalt müügitellimuse ridadele. **Märkus.** Käibemaksu spetsifikatsioonid kopeeritakse ettemaksuarve ridadele ainult juhul, kui välja **Maksuliik** sätteks lehel **Käibemaksukoodid** on valitud **Standardne käibemaks** või **Vähendatud käibemaks**. Muidu kopeeritakse rida ettemaksuarvele, kui käibemaksusumma on 0 (null).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Ettemaksuarve seostamine müügitellimuse või vabas vormis arvega
Iga ettemaksuarve saab seostada korraga ainult ühe müügitellimuse või vabas vormis arvega. Saate olemasoleva ettemaksuarve ümber määrata teisele müügitellimusele või vabas vormis arvele eeldusel, et ettemaksuarvega pole seostatud ühtki ettemaksu. Ettemaksuarve seostamiseks müügitellimusega valige lehel **Kõik ettemaksuarved** soovitud ettemaksuarve. Klõpsake toimingupaanil valikut **Ettemaksuarve** ja seejärel valikut **Müügitellimus**. Seejärel valige müügitellimus, mille soovite ettemaksuarvega seostada, ja klõpsake **OK**. Ettemaksuarve seostamiseks vabas vormis arvega valige lehel **Kõik ettemaksuarved** soovitud ettemaksuarve. Klõpsake toimingupaanil valikut **Ettemaksuarve** ja seejärel valikut **Vabas vormis arve**. Seejärel valige vabas vormis arve, millega soovite ettemaksuarve seostada, ja klõpsake **OK**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Kliendi ettemaksuarve loomine müügitellimuselt
Looge müügitellimus või valige olemasolev müügitellimus. Klõpsake valikut **Arve** ja seejärel valikuid **Loo** &gt; **Ettemaksuarve**. Määrake lehel **Ettemaksuarve loomine** järgmised väljad.

| Väli                                           | Kirjeldus                                                                                                                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Protsent                                         | Saate määrata müügitellimuse ettemaksu protsendi.                                                                                                                                                                             |
| Vastaskonto                                  | Saate valida vaikevastaskonto täiustatud arveldamisega kasutamiseks.                                                                                                                                                                         |
| Tellimuse värskendamine                                    | Saate teha ühe järgmistest valikutest: **Kõik**, **Tarni kohe**, **Komplekteeritud**, **Saateleht** või **Komplekteeritud kogus ja ladustamata tooted**. Ettemaksuarve summa arvutatakse kaupade müügitellimuse summade põhjal. |
| Sisestage KM                                        | Saate määrata, kas käibemaks tuleb sisestada ettemaksuarve sisestamise ajal.                                                                                                                                                                      |
| Käibemaksu sisestamiskuupäev                                   | Saate määrata käibemaksu sisestamise kuupäeva.                                                                                                                                                                                                         |
| Sisestusreeglid ettemaksu töölehekandega | Saate määrata ettemaksu sisestusreeglid.                                                                                                                                                                                           |
| Loo maksudokument                             | Saate määrata, kas maksudokument tuleb luua.                                                                                                                                                                                         |

> MÄRKUS. Poola puhul luuakse ettemaksuarve kanded siis, kui seadistate jaotises Müügireskontro parameetrid ettemaksuarvete jaoks sisestusreeglid.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Kliendi ettemaksuarve loomine vabas vormis arvelt
Looge vabas vormis arve või valige olemasolev vabas vormis arve Klõpsake vahekaardil **Arve** jaotises **Uus** valikut **Ettemaksuarve**. Seejärel saate luua uue ettemaksuarve, mis seostatakse vabas vormis arvega. **Märkus.** Poola puhul luuakse ettemaksuarve kanded siis, kui seadistate jaotises Müügireskontro parameetrid ettemaksuarvete jaoks sisestusreeglid.

## <a name="print-an-advance-invoice"></a>Ettemaksuarve printimine
Ettemaksuarve printimiseks klõpsake lehel **Ettemaksuarve** valikut **Prindi**. Poola puhul saate printida fiskaaldokumendi ettemaksuarve dokumendi. Saate valida suvandi ettemaksuarve sisestamise ajal. Poola puhul peab müügiarve ja vabas vormis arve dokumentide paigutus sisaldama tasakaalustatava ettemaksuarve kohta järgmist teavet.

-   Ettemaksuarve number
-   Ettemaksuarve kuupäev
-   Summa ilma käibemaksuta, käibemaksusumma, summa koos käibemaksuga ja valuuta
-   Maksuprotsent

Käibemaksusummade kokkuvõte peab sisaldama parameetrit **Maks ettemaksuarvelt**. Tasumata summat tuleb ettemaksuarve summa võrra vähendada.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Maksesoovituse loomine ettemaksuarvelt
Saate luua ettemaksuarve põhjal automaatselt maksetöölehe read. Uue maksetöölehe loomisel valige lehel **Maksetööleht** suvand **Ettemaksu töölehekanne** ja klõpsake valikut **Read**. Lehel **Töölehe kanne** saate ettemaksuarvetelt maksesoovituse loomiseks klõpsata valikuid **Maksesoovitus** &gt; **Maksesoovitus ettemaksuarvelt**. Teave, nagu sisestusreeglid ja käibemaksugrupid, võetakse ettemaksuarvelt. **Märkus.** Uued ettemaksud seostatakse automaatselt ettemaksuarvetega, kui lehel **Maksesoovituse loomine ettemaksuarvetelt** on valitud suvandid **Seosta ettemaksud** ja **Muuda olekut**.

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Ettemaksu seostamine ettemaksuarvega
Ettemaksu seostamiseks ettemaksuarvega maksetöölehelt avage maksetööleht, valige ettemaksuga rida ja seejärel klõpsake valikuid **Funktsioonid** &gt; **Seosta ettemaksuarvetega**. Ettemaksu seostamiseks ettemaksuarvega lehelt **Kliendikanded** klõpsake valikuid **Kõik kliendid** &gt; **Klient** &gt; **Kanded**. Valige maksetööleht, valige ettemaksuga rida ja klõpsake valikuid **Funktsioonid** &gt; **Seosta ettemaksuarvetega**.

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Ettemaksuarve seostamine ettemaksuga
Ettemaksuarve seostamiseks ettemaksureaga valige lehel **Kõik ettemaksuarved** soovitud ettemaksuarve. Klõpsake toimingupaanil valikut **Ettemaksuarve** ja seejärel valikut **Ettemaks**. Seejärel valige ettemaksurida, mille soovite ettemaksuarvega seostada, ja klõpsake **OK**.

## <a name="advance-invoice-credit-note"></a>Ettemaksuarve kreeditarve
-   (POL) Ettemaksuarve tühistamiseks saate luua ettemaksuarve kreeditarve ja sisestada selle pearaamatusse.
-   Kreeditarve loomiseks saate luua uue ettemaksuarve ja seejärel klõpsata valikut **Kreeditarve**. Seejärel saate valida tühistatava ettemaksuarve.
-   Saate luua ka kreeditarve müügiarve kohta, millel on ettemaksuarve tasakaalustus.
-   Ettemaksuarve kreediarvete paigutus sisaldab teavet ridade kohta nii enne kui ka pärast korrigeerimist.
-   (POL) Pearaamatukanded luuakse pärast ettemaksuarve kreeditarve sisestamist.

## <a name="cze-tax-documents"></a>(CZE) Maksudokumendid
Tšehhi Vabariigi puhul saate luua maksudokumendi, mis põhineb käibemaksuga maksustatava tarne ettemaksuteabel. Saate maksudokumendi luua, luua ja kuvada või luua ja printida ettemaksu lehel. Klõpsake valikuid **Funktsioonid** &gt; **Maksudokukment** ja valige üks järgmistest suvanditest. Maksudokument sisaldab käibemaksu kohta üksikasjalikku teavet, nagu käibemaksu tüüp, väärtus ning alus arvestusvaluutas ja kandevaluutas.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Ostureskontro seadistamine ettemaksuarvete puhul
Määrake lehe **Ostureskontro parameetrid** vahekaardil **Numbriseeriad** ettemaksuarvete numbriseeriad.

## <a name="create-a-vendor-advance-invoice"></a>Hankija ettemaksuarve loomine
Saate ettemaksuarve käsitsi luua. Teise võimalusena võib uue ettemaksuarve aluseks võtta olemasoleva ostutellimuse.

## <a name="manually-create-a-vendor-advance-invoice"></a>Hankija ettemaksuarve käsitsi loomine
Klõpsake valikuid **Ostureskontro** &gt; **Üldine** &gt; **Ettemaksuarved** &gt; **Kõik ettemaksuarved**. Uue ettemaksuarve loomiseks klõpsake toimingupaani vahekaardil **Ettemaksuarve** valikut **Ettemaksuarve**. Seejärel sisestage vajalik teave ja klõpsake ettemaksuarve sisestamiseks nuppu **Sisesta**. Ettemaksuarvel võib olla üks järgmistest olekutest: **Avatud**, **Osaliselt makstud** või **Suletud**. Sisestatud ettemaksuarve olekut saate käsitsi muuta. Klõpsake valikut **Olek** ja seejärel valige lehel **Ettemaksuarve oleku muutmine** väljal **Uus olek** ettemaksuarve uus olek. **Märkus.** Ettemaksuarve olekut saate muuta igal ajal. Suletud ettemaksuarveid kannetes ei saa töödelda. **Märkus.** Käibemaksu spetsifikatsioonid kopeeritakse ettemaksuarve ridadele ainult juhul, kui välja **Maksuliik** sätteks lehel **Käibemaksukoodid** on valitud **Standardne käibemaks** või **Vähendatud käibemaks**. Muidu kopeeritakse rida ettemaksuarvele, kui käibemaksusumma on 0 (null).

## <a name="link-an-advance-invoice-to-a-purchase-order"></a>Ettemaksuarve seostamine ostutellimusega
Iga ettemaksuarve saab seostada korraga ainult ühe ostutellimusega. Saate olemasoleva ettemaksuarve ümber määrata teisele ostutellimusele eeldusel, et ettemaksuarvega pole seostatud ühtki ettemaksu. Ettemaksuarve seostamiseks ostutellimusega valige lehel **Kõik ettemaksuarved** soovitud ettemaksuarve. Klõpsake toimingupaanil valikut **Ettemaksuarve** ja seejärel valikut **Ostutellimus**. Seejärel valige ostutellimus, mille soovite ettemaksuarvega seostada, ja klõpsake **OK**.

## <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Hankija ettemaksuarve loomine ostutellimusest
Looge ostutellimus või valige olemasolev ostutellimus. Klõpsake valikut **Arve** ja seejärel valikuid **Loo** &gt; **Ettemaksuarve**. Määrake lehel **Ettemaksuarve loomine** järgmised väljad.

| Väli                                           | Kirjeldus                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Protsent                                         | Saate määrata ostutellimuse ettemaksu protsendi.                                                         |
| Uuenda ostu                                 | Valikud on järgmised. Ettemaksuarve summa arvutatakse kaupade ostutellimuse summa põhjal. |
| Sisestusreeglid ettemaksu töölehekandega | Saate määrata ettemaksu sisestusreeglid.                                                                          |







