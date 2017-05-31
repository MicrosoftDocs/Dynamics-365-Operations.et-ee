---
title: Projekti eest arve esitamine
description: "Selles artiklis antakse ülevaade aja- ja materjalikulu ning fikseeritud hinnaga projektide arveldamise kohta. See sisaldab teavet arvesoovituste (esialgsed arved), arvekontrolli, ettemaksuarvelduse, hankija arvete ja kreeditarvete kohta."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 91b8fa9dc09359c59b806ac3d296e53503f7ed1a
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="project-invoicing"></a>Projekti eest arve esitamine

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade aja- ja materjalikulu ning fikseeritud hinnaga projektide arveldamise kohta. See sisaldab teavet arvesoovituste (esialgsed arved), arvekontrolli, ettemaksuarvelduse, hankija arvete ja kreeditarvete kohta.

Projekti tüüp määratleb, millise arveldusprotseduuri rakendatakse. Arvet saab esitada ainult kahe välise projektitüübi eest: Aeg ja materjal ning Fikseeritud hind. Aja- ja materjalikulu projektid ning fikseeritud hinnaga projektid on alati seotud projektilepinguga.

-   **Fikseeritud hinnaga projektid** – kliendiarve summa põhineb arve maksegraafikutel. Arveldamine toimub ettemaksuseadistuse kaudu, mida nimetatakse ka maksegraafikuks. Fikseeritud hinnaga projektide eest saab esitada arve projekti või projektilepingu kohta.
-   **Aja- ja materjalikulu projektid** – kliendiarve summa põhineb projektidele sisestatud kanderidadel. Kandeid saab arveldada nii projekti kui projektilepingu kaupa.

Aja- ja materjalikulu projekte ning fikseeritud hinnaga projekte saab arveprojektidega siduda kolmel viisil.

-   **Ettemaksuarveldus** – aja- ja materjalikulu projekte ja fikseeritud hinnaga projekte saab arveldada ettemaksuna. Vaja on kahte tüüpi konto seadistust, ühte igale projekti tüübile.
-   **Arveldamine jaotises Perioodiline** – perioodilise funktsiooni abil saate arveldada kõigi projektide kandeid. Perioodilised funktsioonid pakuvad ülevaadet arveldatavatest kannetest.
-   **Kreeditarvete kasutamine arveldamisel** – kreeditarve saab luua nii aja- ja materjalikulu kui ka fikseeritud hinnaga projektide puhul.

## <a name="invoice-proposals"></a>Arvesoovitused
Enne kui loote projekti jaoks kliendiarve, saate luua esialgse arve või arvesoovituse. Arvesoovituses saate valida projekti arvele lisatavad projekti kanded. Seejärel saate vaadata üle arve üksikasjad enne projekti arve sisestamist ja selle saatmist kliendile või muule rahastamise allikale.

### <a name="creating-invoice-proposals"></a>Arvesoovituste loomine

Võite arvesoovituste loomiseks valida kanded kindla projekti kannete loendist käsitsi. Samuti saate häälestada arveldusreeglid, mis määravad, millal luuakse arvesoovitus automaatselt. Näiteks saate luua arveldusreegli, mille kohaselt luuakse arve soovitus, kui projekt on 25, 50, 75 ja 100 protsenti valmis. 

Arvesoovitusi saab luua järgmistele kannetele.

-   Tunnid, kulud ja muud projektikanded
-   Summad, mille kliendid on kinni pidanud varasematel projektiarvetel
-   Kreeditarved
-   Summad, mille klient tasub teile enne projekti alustamist

Saate luua arvesoovituses tasukandeid. Samuti saate muuta müügihinda tunni-, kulu-, kauba- ja tasukannetes. Arvesoovituse sisestamisel lisatakse värskendatud hinnad ja kanded projekti aruannetesse ja kannete ajalukku. 

Projekti kohta mitme kliendiarve koostamiseks peate looma iga arve kohta arvesoovituse. Näiteks saate luua arveid kande tüübi alusel. Kui soovite määrata ühel kliendiarvel tunnid ja teisel kaubad, tuleb teil luua tunnikannete ja tasukannete kohta eraldi arvesoovitused. 

Kui projektil on mitu rahastamise allikat, saate luua eraldi arvesoovituse igale allikale. Lehel **Rahastamisreegli eraldamised** saate määratleda kandesumma protsendi igale rahastamise allikale eraldamiseks ja allika, millele ümardamise erinevused sisestada.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Arvesoovitustest kliendiarvete loomine

Pärast arvesoovituse loomist ja sisestamist luuakse automaatselt kliendiarve arvesoovituses olevate kannete kohta. 

Enne arvesoovituse sisestamist saate sellele kandeid lisada või sellelt kandeid kustutada. Näiteks saate eemaldada kulukanded, mis sisestati projekti, kuid mille eest ei võeta kliendilt tasu. 

Kui teie organisatsioon nõuab arvesoovituste ülevaatamist enne nende sisestamist, võib olla vaja kinnitada arvesoovitus enne sisestamist töövooga Projekti arvesoovituste läbivaatamine.

## <a name="on-account-invoicing"></a>Ettemaksu arveldus
Ettemaksuarvele projekti kohta sisestatav summa põhineb ajastusel, valmimisprotsendil ja muudel seotud projektilepingus sätestatud arveldustingimustel. Summat ei arvutata tundide, kaupade, kulude ega projektile sisestatud tasude põhjal. 

Peate esmalt looma ettemaksukande aja- ja materjaliprojektidele või fikseeritud hinnaga projektidele. Seejärel saate lisada ettemaksukande projekti arvele. Sisestage ettemaksukandele kliendile esitatava arve summa. Summa kohta projekti arve loomiseks looge esialgne arve (arvesoovitus). Valige arvesoovituses ettemaksukanne. Saate vaadata arvesoovituses ettemaksuteavet, enne kui sellele projekti arve loote.

### <a name="fixed-price-projects"></a>Fikseeritud hinnaga projektid

Fikseeritud hinnaga projektide puhul põhinevad ettemaksukanded kokkulepitud vahe-eesmärgil, tarneühikul või valmidusastmelise arvelduse korraldusel, mis on määratud projekti lepingus. Igale maksele, mis projekti kliendilt saada tuleb, luuakse üks rida. Mahaarvamised pole vajalikud.

### <a name="time-and-material-projects"></a>Aja- ja materjalikulu projektid

Aja- ja materjaliprojektide puhul saate kliendi või muu rahastamise allikaga arveldada ettemakse summa, kasutades ettemaksuarve soovitust. Sisestage ettemaksukanded ühe reana. Soovi korral saate sisestada lisaridu mahaarvamistena, et tasakaalustada ettemakseid, mille klient on juba teinud. Mahaarvamise ridade loomiseks pange summa ette miinusmärk.

## <a name="invoice-control"></a>Arvekontroll
Saate kasutada arve juhtelementi nii arveldatud kui ka arveldamata kannete jälgimiseks ja nende kannete analüüsimiseks pakkumiste suhtes, et saada projektidest terviklik ülevaade, alates pakkumise etapist kuni lõpuleviimiseni. Näete, milliste kannete eest on konkreetse projekti juurde tasud arvestatud ja milliste ridade eest on arve esitatud. Saate vaadata ka eraldi kandeid, nii et teil on võimalik neid pärast sisestamist kohandada.

## <a name="invoicing-fixed-price-projects"></a>Fikseeritud hinnaga projektide arveldamine
Fikseeritud hinnaga projektide arveldamiseks peate määratlema maksegraafiku ja läbima arveldamise protseduuri.

### <a name="billing-schedule"></a>Maksegraafik

Saate arveldada fikseeritud hinnaga projekte maksegraafikul. Maksegraafik määratletakse ühe või mitme projekti etapi vahe-eesmärgi põhjal. Iga vahe-eesmärgi kohta saate määrata konkreetse kuupäeva, müügivaluuta, müügihinna ja tegevuse. 

Näiteks saate seadistada järgmist tüüpi maksegraafiku.

-   20% projektilepingu allkirjastamisel
-   30% esimesel tarnel
-   15% teisel tarnel
-   35% lõplikul tarnimisel

### <a name="invoicing-procedure"></a>Arveldusprotseduurid

Kui vahetähtaja maksed on arve esitamiseks valmis, kasutage ettemaksesummade arveldusprotseduuri.

## <a name="vendor-invoicing"></a>Hankija arve koostamine
Kui tellite hankijalt kauba ja määrate selle kauba projektile, määrab reaatribuut, mille selle kauba ostutellimuse reale valite, kas ostetud kauba eest esitatakse kliendile arve. Kui seadistate rea vaikeatribuudid, kuvatakse need kaubale ostutellimuse real (Rea üksikasjad &gt; Projekt &gt; Rea atribuut). On kaks võimalust rea atribuuti muuta.

-   Projekti kliendile kauba eest arve esitamine: määrake kauba reaatribuudiks arveldatav väärtus ostutellimusel ja esitage siis kliendile arve, kasutades õiget projekti arveldusmeetodit.
-   Projekti kliendile kauba eest arve mitte-esitamine: ärge valige selle kauba ostutellimuse real reaatribuuti **Arveldatav**. Siis saate ostutellimuse eest arve esitada ja rohkem pole midagi vaja teha.

## <a name="credit-notes"></a>Kreeditarved
Kui kliendiarve summa väärtus on negatiivne, klassifitseeritakse arve kreeditarveks. Dokumendi printimisel on selle pealkiri Kreeditarve. 

Kui te loote eelnevalt arveldatud summa krediteerimiseks kreeditarve, tuleb teil kõigepealt valida arveldatud summa krediteerimiseks. Seejärel loote kreeditarve sama protseduuri abil, mida te kasutaksite tavalise kliendiarve loomisel. Teisisõnu valite kliendiarvele sisestatud kanded ja seejärel sisestate kreeditarve soovituse. 

Sama dokument võib sisaldada krediteerimiseks, krediitkanneteks valitud kandeid ja sisestatud kandeid. Dokument klassifitseeritakse siis kas arve või kreeditarvena, sõltuvalt sellest, kas lõppsumma on positiivne või negatiivne. 

Arveldatud summa krediteerimiseks tuleb kõigepealt valida arveldatud summa krediteerimiseks ja koostada siis kreeditarve. Kreeditarve koostatakse sama protseduuri abil, mida kasutate kliendiarve koostamisel. 

Saate koostada negatiivse summaga arve, mis klassifitseeritakse kreeditarveks. Kreeditarve loomiseks ja printimiseks tuleb valida kliendiarvele sisestatud kanded ning seejärel kandeid muuta. Kui juriidilise isiku peamine aadress pole Saksamaal, on arve pealkiri Korrigeeriv arve.




