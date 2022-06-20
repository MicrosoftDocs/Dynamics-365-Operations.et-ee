---
title: Ettemaksuarved Ida-Euroopa puhul
description: See artikkel annab teavet ettemaksuarvete kohta Ida-Euroopa jaoks. Ettemaksuarve on dokument, mille saate luua kliendile või hankijale. Sellel märgitakse summa, mis tuleb müügitellimuse puhul ette maksta.
author: EvgenyPopovMBS
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272643
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c722d8215c2b65e24008042c9a4d65bb419ad46a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886287"
---
# <a name="advance-invoices-for-eastern-europe"></a>Ettemaksuarved Ida-Euroopa puhul

[!include [banner](../includes/banner.md)]

See artikkel annab teavet ettemaksuarvete kohta Ida-Euroopa jaoks. Ettemaksuarve on dokument, mille saate luua kliendile või hankijale. Sellel märgitakse summa, mis tuleb müügitellimuse puhul ette maksta. 

> [!NOTE]
> Teise võimalusena saate kasutada ettemaksuarve funktsiooni. Microsoft Dynamics 365 Finantsversiooni 10.0.28 puhul saate seda funktsiooni kasutada, kui kasutate seda funktsiooni, **·** &gt; **·** &gt; **·** &gt; **·** **·** **·** **kui kasutate ostureskontro seadistamise parameetreid Pearaamat ja käibemaks ning seadistate ettemakse arve suvandi Ettemakse arve kiirkaardil valikule Jah.** Lisateavet vt ettemaksuarvete [vs. ettemaksete kohta](../accounts-payable/prepayments-invoices-vs-prepayments.md).

Ettemaksuarve funktsioon võimalda teha järgmist.

- Ettemaksuarvete väljastamine klientidele ja nende ettemaksuarvete oleku jälgimine (**Avatud**, **Osaliselt makstud** või **Suletud**).
- *Ainult Poola puhul:* sisestage ettemaksuarve kanded ja käibemaksu kanded.
- Loo ettemaksuarve põhjal automaatselt maksetöölehe read.
- Seostage klientidelt saadud ettemaksud ettemaksuarvetega (enne või pärast ettemaksu sisestamist).
- Muutke käibemaksusisestust sisestatud ettemaksudtes (st teisendage ettemaksu makseks või makse ettemaksuks või muutke sisestamiskuupäeva, maksumäära või summat).
- *Ainult Tšehhi Vabariigile:* looge käibemaksustatav tarne maksudokument.

## <a name="advance-invoices-for-poland"></a>Ettemaksuarved Poola puhul

Ettemakse saavad Poola ettevõtted peavad looma kliendi jaoks ettemaksude arve. See ettemaksuarve sisestatakse pearaamatusse ja see on käibemaksu maksueesmärgil kohustuslik dokument. Ettemaksuarvel arvutatav maks tuleb teatada maksuhaldurile.

Kaupade lõpliku müügi korral tuleb ettemaksuarve määrata müügiarvel. Müügi kogusumma peab sisaldama ettemakse.

Kui müügiarve on sisestatud, siis tasakaalustatud ettemaksuarve tühistatakse. Algne ettemaksuarve tasakaalustatakse ettemaksuarve tagasipööraga.

## <a name="set-up-accounts-receivable-for-advance-invoices"></a>Müügireskontro seadistamine ettemaksuarvete puhul

1. **Seadke müügireskontro** parameetrite **lehe vahekaardi** Uuendused kiirkaardil **Ettemaksuarve** järgmised väljad.

    | Väli | Kirjeldus |
    |-------|-------------|
    | Sisestusprofiil | <p>*Ainult Poola puhul:* valige ettemaksuarveldusega kasutatav sisestusprofiil.</p><p>**Oluline.** Tšehhi Vabariigi ja Ungari puhul ei käsitleta ettemaksuarveid raamatupidamis- või maksudokumentidena ja neid ei sisestata pearaamatusse. Seega peaksite selle välja nende riikide jaoks tühjaks jätma, et takistada ettemaksuarvete sisestamist pearaamatusse.</p> |
    | Vastaskonto | Valige vastaskonto. |
    | Käibemaksugrupp | Saate valida käibemaksugrupi ettemaksuarvelduseks käibemaksu arvutamisel. |
    | Vastupidiseks muutmine parandusena | Märkige see ruut, kui ettemaksuarve vastupidisekspöördumist tuleks käsitleda parandusena. |
    | Tühista arvekuupäeval | Ettemakse tühistamiseks arve sisestamise kuupäeval märkige see ruut. |

1. Seadke makse **kiirkaardil** järgmised väljad.

    | Väli | Kirjeldus |
    |-------|-------------|
    | Mitu ettemaksukuupäeva | Valige **Aktsepteeri**, **Hoiatus** või **Tõrge**. |
    | Kuupäeva sobimatus | Valige **Aktsepteeri**, **Hoiatus** või **Tõrge**. |
    | Summa sobimatus | Valige **Aktsepteeri**, **Hoiatus** või **Tõrge**. |
    | Sisestatud ettemaksuarvega seostamine | Valige **Aktsepteeri**, **Hoiatus** või **Tõrge**. |
    | (CZE), (POL) Ettemaksu käsitlemine | Valige **Täpsem**. |

1. Seadistage numbriseeriad vahekaardil **Numbriseeriad** järgmiste viidete jaoks.

    - Maksudokument
    - Maksukrediiditeatis
    - Ettemaksuarve
    - Ettemaksuarve kreeditarve
    - Ettemaksuarve vastupidiseks muutmine
    - Ettemaksuarve kanne
    - Ettemaksuarve kreeditarve kanne
    - Ettemaksuarve tühistamiskanne

## <a name="create-a-customer-advance-invoice"></a>Kliendi ettemaksuarve loomine

1. Minge kõikide **ettemaksuarvete** &gt; **·** &gt; **müügireskontro** &gt; **üldarvetele.**
1. Ettemaksuarve loomiseks valige tegevuspaani **vahekaardil** **Ettemaksuarve**.
1. Sisestage nõutav teave ja seejärel valige ettemaksuarve **sisestamiseks** käsk Sisesta.

Ettemaksuarvel võib olla üks järgmistest olekutest: **Avatud**, **Osaliselt makstud** või **Suletud**. Sisestatud ettemaksuarve olekut saate käsitsi muuta. Valige **olek** ja seejärel valige **ettemaksuarve** **lehe** oleku muutmine väljal Uus olek ettemaksuarve uus olek.

> [!NOTE]
> Ettemaksuarve olekut saate igal ajal muuta. Suletud ettemaksuarveid kannetes ei saa töödelda.
> 
> *Ainult Poola puhul:* ettemaksuarve kanded luuakse siis, kui seadistate müügireskontro parameetrites ettemaksuarvete sisestusreegli. Sisestatud kannete vaatamiseks valige ettemaksuarve **lehel** **kanne**.

## <a name="vat-on-advance-invoices"></a>Käibemaks ettemaksuarvetel

Ettevõtted peavad kirjendama käibemaksu klientide ettemaksudel, isegi kui müük pole veel lõpule viidud. Ettemaksult käibemaksu sisestamiseks saate lisada ettemaksuarvele rea, mis sisaldab käibemaksu spetsifikatsioone. Ettemaksuarvel võib olla mitu rida ja need read võivad sisaldada KM-i spetsifikatsioone, mis võetakse müügitellimuse ridadelt. Seetõttu saate käibemaksu sisestada ettemakselt, vastavalt müügitellimuse ridadele.

> [!NOTE]
> KM-spetsifikatsioonid kopeeritakse ettemaksuarve **ridadele** ainult siis, kui käibemaksukoodide lehe maksutüübiks on **seatud** **Standardne KM** või Vähendatud **KM**. Vastasel juhul kopeeritakse need ettemaksuarve ridadele nagu oleks KM-summa 0 (null).

## <a name="link-an-advance-invoice-to-a-sales-order-or-a-free-text-invoice"></a>Ettemaksuarve seostamine müügitellimuse või vabas vormis arvega

Iga ettemaksuarve saab siduda korraga ainult ühe müügitellimuse või vabas vormis arvega. Saate olemasoleva ettemaksuarve ümber määrata teisele müügitellimusele või vabas vormis arvele eeldusel, et ettemaksuarvega pole seostatud ühtki ettemaksu.

Ettemaksuarve seostamiseks müügitellimusega järgige neid samme.

1. Valige leheküljel **Kõik ettemaksuarved** ettemaksuarve.
1. Tegevuspaanil valige **ettemaksuarve** ja seejärel **müügitellimus**.
1. Valige ettemaksuarvega seostamiseks müügitellimus ja seejärel valige **OK**.

Ettemaksuarve seostamiseks vabas vormis arvega järgige neid samme.

1. Valige leheküljel **Kõik ettemaksuarved** ettemaksuarve.
1. Tegevuspaanil valige ettemaksuarve **ja** seejärel vabas **vormis arve**.
1. Valige ettemaksuarvega seostamiseks vabas vormis arve ja seejärel valige **OK**.

## <a name="create-a-customer-advance-invoice-from-a-sales-order"></a>Kliendi ettemaksuarve loomine müügitellimuselt

1. Looge müügitellimus või valige olemasolev müügitellimus.
1. Valige **arve** ja seejärel looge **ettemaksuarve** &gt; **·**.
1. Seadke ettemaksuarve **lehel** järgmised väljad.

    | Väli | Kirjeldus |
    |-------|-------------|
    | Protsent | Saate määrata müügitellimuse ettemaksu protsendi. |
    | Vastaskonto | Saate valida ettemaksuarveldusega kasutatava vaikevastaskonto. |
    | Tellimuse värskendamine | Valige **kõik**, **tarni kohe**, **Komplekteeritud**, **Saateleht** või Komplekteeritud **kogus ja mitte ladustamata tooted**. Ettemaksuarve summa arvutatakse kaupade müügitellimuse summade põhjal. |
    | Sisestage KM | Saate määrata, kas käibemaks tuleb sisestada ettemaksuarve sisestamise ajal. |
    | Käibemaksu sisestamiskuupäev | Saate määrata KM-i sisestamise kuupäeva. |
    | Sisestusreeglid ettemaksu töölehekandega | Saate määrata ettemaksu sisestusreeglid. |
    | Loo maksudokument | Saate määrata, kas maksudokument tuleb luua. |

> [!NOTE]
> *Ainult Poola puhul:* ettemaksuarve kanded luuakse siis, kui seadistate müügireskontro parameetrites ettemaksuarvete sisestusreegli.

## <a name="create-a-customer-advance-invoice-from-a-free-text-invoice"></a>Kliendi ettemaksuarve loomine vabas vormis arvelt

1. Looge vabas vormis arve või valige olemasolev vabas vormis arve
1. Valige vahekaardil **Arve jaotises Uus** **suvand** Ettemaksuarve **.**

    Nüüd saate luua uue ettemaksuarve, mis seotakse vabas vormis arvega.

> [!NOTE]
> *Ainult Poola puhul:* ettemaksuarve kanded luuakse siis, kui seadistate müügireskontro parameetrites ettemaksuarvete sisestusreegli.

## <a name="print-an-advance-invoice"></a>Ettemaksuarve printimine

- Valige lehel **Ettemaksuarve** suvand **Prindi**. 

*Ainult Poola puhul:* saate printida fiskaaldokumendi ettemaksuarve dokumendi. Saate valida suvandi ettemaksuarve sisestamise ajal.

*Ainult Poola puhul:* müügiarve ja vabas vormis arvedokumendid peaksid sisaldama järgmist teavet ettemaksuarve kohta, mis on tasakaalustatud.

- Ettemaksuarve number
- Ettemaksuarve kuupäev
- Summa ilma käibemaksuta, käibemaksusumma, summa koos käibemaksuga ja valuuta
- Maksuprotsent

KM-summade kokkuvõte peaks sisaldama välja **Ettemaksuarvelt pärit** maks. Tasumata summat tuleb ettemaksuarve summa võrra vähendada.

## <a name="create-a-payment-proposal-from-an-advance-invoice"></a>Maksesoovituse loomine ettemaksuarvelt

Uue maksetöölehe loomisel saate ettemaksuarve põhjal luua automaatselt maksetöölehe read.

1. Valige lehel **Maksetööleht** suvand Ettemaksu **töölehe kanne** ja seejärel valige **read**.
1. Ettemaksuarvelt **maksesoovituse** **loomiseks** &gt; **valige** töölehe kande lehel maksesoovitus ettemaksuarvelt. Teave, nagu sisestusreeglid ja käibemaksugrupid, võetakse ettemaksuarvelt.

> [!NOTE]
> Uued ettemaksed seostatakse automaatselt **ettemaksuarvetega** **·**, kui leheküljel Loo ettemaksuarved on **valitud suvand Seosta ettemaksed ja Muuda olekut.**

## <a name="link-a-prepayment-to-an-advance-invoice"></a>Ettemaksu seostamine ettemaksuarvega

Ettemakse seostamiseks ettemaksuarvega makse töölehelt, järgige neid samme.

- Avage maksetööleht, valige rida, mis on ettemaksega ja seejärel valige **Funktsioonid** &gt; **link ettemaksuarvetele.**

Ettemakse seostamiseks ettemaksuarvega kliendi tehingute **leheküljelt** järgige neid samme.

1. Valige **kõik kliendikanded** &gt; **·** &gt; **·**.
1. Valige maksetööleht, valige rida, mis on ettemaksega ja seejärel valige **Funktsioonid** &gt; **link ettemaksuarvetele.**

## <a name="link-an-advance-invoice-to-a-prepayment"></a>Ettemaksuarve seostamine ettemaksuga

Ettemaksuarve seostamiseks ettemaksureaga järgige neid samme.

1. Valige leheküljel **Kõik ettemaksuarved** ettemaksuarve.
1. Tegevuspaanil valige ettemaksuarve **ja** seejärel **ettemakse**.
1. Valige ettemaksuarvega seostamiseks ettemakse rida ja seejärel valige **OK**.

## <a name="advance-invoice-credit-notes"></a>Ettemaksuarve kreeditarved

- *Ainult Poola puhul:* ettemaksuarve tühistamiseks saate luua ettemaksuarve kreeditarve ja sisestada selle pearaamatusse.
- Kreeditarve loomiseks saate luua uue ettemaksuarve ja seejärel valida **kreeditarve**. Seejärel saate valida tühistatava ettemaksuarve.
- Samuti saate luua kreeditarve müügiarve jaoks, mille ettemaksuarve tasakaalustus on.
- Ettemaksuarve kreediarvete paigutus sisaldab teavet ridade kohta nii enne kui ka pärast korrigeerimist.
- *Ainult Poola puhul:* pearaamatukanded luuakse pärast ettemaksuarve kreeditarve sisestamist.

## <a name="tax-documents-for-the-czech-republic"></a>Tšehhi Vabariigi maksudokumendid

Tšehhi Vabariigi puhul saate luua maksudokumendi, mis põhineb käibemaksuga maksustatava tarne ettemaksuteabel. Ettemakse leheküljelt saate luua, luua ja näidata või luua või printida käibemaksudokumenti, **·** &gt; **valides soovitud Funktsioonid maksudokumendi** ja valides seejärel ühe valikutest. Maksudokument sisaldab käibemaksu kohta üksikasjalikku teavet, nagu käibemaksu tüüp, väärtus ning alus arvestusvaluutas ja kandevaluutas.

## <a name="set-up-accounts-payable-for-advance-invoices"></a>Ostureskontro seadistamine ettemaksuarvete puhul

- Määrake lehe **Ostureskontro parameetrid** vahekaardil **Numbriseeriad** ettemaksuarvete numbriseeriad.

## <a name="create-a-vendor-advance-invoice"></a>Hankija ettemaksuarve loomine

Saate ettemaksuarve käsitsi luua. Teise võimalusena võib uue ettemaksuarve aluseks võtta olemasoleva ostutellimuse.

### <a name="manually-create-a-vendor-advance-invoice"></a>Hankija ettemaksuarve käsitsi loomine

1. Minge **ostureskontro** &gt; **üld** &gt; **ettemaksuarvetele** &gt; **Kõik ettemaksuarved.**
1. Ettemaksuarve loomiseks valige tegevuspaani **vahekaardil** **Ettemaksuarve**.
1. Sisestage nõutav teave ja seejärel valige ettemaksuarve **sisestamiseks** käsk Sisesta.

Ettemaksuarvel võib olla üks järgmistest olekutest: **Avatud**, **Osaliselt makstud** või **Suletud**. Sisestatud ettemaksuarve olekut saate käsitsi muuta. Valige **olek** ja seejärel valige **ettemaksuarve** **lehe** oleku muutmine väljal Uus olek ettemaksuarve uus olek.

> [!NOTE]
> Ettemaksuarve olekut saate igal ajal muuta. Suletud ettemaksuarveid kannetes ei saa töödelda.
>
> KM-spetsifikatsioonid kopeeritakse ettemaksuarve **ridadele** ainult siis, kui käibemaksukoodide lehe maksutüübiks on **seatud** **Standardne KM** või Vähendatud **KM**. Vastasel juhul kopeeritakse need ettemaksuarve ridadele nagu oleks KM-summa 0 (null).

### <a name="link-an-advance-invoice-to-a-purchase-order"></a>Ettemaksuarve seostamine ostutellimusega

Iga ettemaksuarve saab korraga seostada ainult ühe ostutellimusega. Saate olemasoleva ettemaksuarve ümber määrata teisele ostutellimusele eeldusel, et ettemaksuarvega pole seostatud ühtki ettemaksu.

Ettemaksuarve seostamiseks ostutellimusega järgige neid samme.

1. Valige leheküljel **Kõik ettemaksuarved** ettemaksuarve.
1. Tegevuspaanil valige **ettemaksuarve** ja seejärel **ostutellimus**.
1. Valige ettemaksuarvega seostamiseks ostutellimus ja seejärel valige **OK**.

### <a name="create-a-vendor-advance-invoice-from-a-purchase-order"></a>Hankija ettemaksuarve loomine ostutellimusest

1. Looge ostutellimus või valige olemasolev ostutellimus.
1. Valige **arve** ja seejärel looge **ettemaksuarve** &gt; **·**.
1. Seadke ettemaksuarve **lehel** järgmised väljad.

    | Väli | Kirjeldus |
    |-------|-------------|
    | Protsent | Saate määrata ostutellimuse ettemaksu protsendi. |
    | Uuenda ostu | Tehke valik. Ettemaksuarve summa arvutatakse kaupade ostutellimuse summa alusel. |
    | Sisestusreeglid ettemaksu töölehekandega | Saate määrata ettemaksu sisestusreeglid. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
