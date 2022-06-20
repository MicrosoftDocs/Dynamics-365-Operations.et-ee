---
title: Kuidas seadistada tasakaalustavad finantsdimensioonid?
description: See artikkel kirjeldab valikuid Tasakaalustava finantsdimensiooni funktsiooni seadistamiseks ja kasutamiseks.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: dd859629b0eb9f14fa4907699613382f3897d21d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878008"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Kuidas seadistada tasakaalustavad finantsdimensioonid?

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab valikuid Tasakaalustava finantsdimensiooni funktsiooni seadistamiseks ja kasutamiseks.

## <a name="symptom"></a>Sümptom

Tasakaalustava finantsdimensioonide seadistamiseks on kaks võimalust. Esimene valik on kasutada **Tasakaalustav finantsdimensioon** välja **pearaamatu** seadistuslehel (**Pearaamatu \> pearaamatu häälestus \> Pearaamat**). Teine võimalus on kasutada **Nõudke, et mõõde oleks tasakaalus** väljal **Finantsdimensioonid** lehel (**Pearaamat > Kontoplaan \> Dimensioonid \> Finantsdimensioonikogumid**). See artikkel selgitab erinevust nende kahe valiku vahel.

## <a name="resolution"></a>Lahendus

Organisatsioonid kasutavad tavaliselt tasakaalustamisdimensioone, et luua bilanss, mis on finantsdimensiooni tasemel tasakaalus. Mõlema funktsiooni lubamine ei too sisestatud tasakaalustamata dimensioone saldosse. Enne kummagi funktsiooni lubamist peate korrigeerivad kanded sisestama käsitsi, et viia bilanss saldosse.

Need kaks võimalust ei ole teineteist välistavad. Valik, mida teie organisatsioon kasutab, peaks põhinema teie ärinõuetel. Sageli ootame neid kliente, kes määratlevad tasakaalustava dimensiooni nii pearaamatu seadistuses kui ka finantsdimensioonide seadistuses, ning seejärel lõpetage osa või kõik vajalikud lisaseadistused. Kuid neid ei saa siiski sisestada, kuna finantsdimensiooni tase ei ole tasakaalustuatud.

Järgmistes jaotistes kirjeldatakse kahte valikut ja selgitatakse nende seadistamist.

### <a name="ledger--balancing-financial-dimension"></a>Pearaamat - Tasakaalustav finantsdimensioon

Tasakaalustamisdimensiooni **Pearaamatu** seadistuslehel kasutatakse ettevõttesisese raamatupidamise lubamiseks. Funktsionaalsuse sisselülitamiseks järgige neid samme.

1. Määrake, milline finantsdimensioon on tasakaalustav dimensioon.

    - See funktsioon võimaldab tasakaalustusdimensiooniks valida ainult ühe finantsdimensiooni.
    - Ärge valige dimensiooni **Pearaamatu** seadistuse lehel.
    - Kontrollige, et teie bilanss oleks valitud finantsdimensiooni jaoks juba tasakaalustatud.

2. Saate uuendada tasakaalustava finantsdimensiooni konto struktuuri.

    - Peate valima tasakaalustava finantsdimensiooni, mis on kaasatud kõikidesse pearaamatusse määratud kontostruktuuridesse.
    - Finantsdimensioon ei tohi konto struktuuris tühje summasid lubada. See piirang tagab, et iga Pearaamatusse sisestatud raamatupidamiskirje sisaldab finantsdimensiooni väärtust. Tühi dimensioon ei kehti tasakaalustusdimensioonide kasutamisel.

3. **Automaatsete kannete kontode** lehel (**Pearaamatu \> Sisestamise seadistus \> automaatsete kannete kontod**) määratlege kontsernisisesed deebet- ja kreediti põhikontod.
4. **Pearaamat** seadistuse lehel (**Pearaamat \> Pearaamatu seadistus \> Pearaamat**), **Tasakaalustav finantsdimensioon** väljal valige finantsdimensioon, et seda kasutada tasakaalustamiseks.

Kui valitud finantsdimensioon ei ole kannete sisestamisel ja postitamisel tasakaalus, lisab süsteem automaatselt deebet- või kreeditkirjed, mis on vajalikud raamatupidamiskirje tasakaalustamiseks sisestamise ajal. Kontsernisisese kande deebet- ja kreeditkontod kuvatakse pearaamatus sisestatud kandel. Neid siiski ei kuvata töölehtedel ega lähtedokumentidel, mille kohta raamatupidamiskirjed sisestati.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Finantsdimensioonid – dimensiooni tasakaalustamise nõudmine

Kuigi tasakaalustusdimensiooni leheküljel **Finantsdimensioonid** kasutavad tavaliselt avaliku sektori ettevõtted, ei ole funktsioon seotud ühegi avaliku sektori konfiguratsioonivõtmega. Kuna süsteemis puudub piirang, saate seda funktsiooni kasutada ka siis, kui teie organisatsioon ei ole avaliku sektori üksus.

Seda funktsiooni kasutatakse tavaliselt avaliku sektori kliendibaasis, sest see nõuab sisestamisdefinitsioonide kasutamist iga kande automaatseks tasakaalustamiseks. See ei kasuta konto **Kontod automaatsete kannete** jaoks määratletud üksustevahelisi deebet- ja kreeditkontosid raamatupidamiskirjete automaatseks tasakaalustamiseks. Kui raamatupidamiskirje ei ole pärast sisestamisdefinitsioonide rakendamist dimensioonitasemel tasakaalus, siis kannet ei sisestata isegi juhul, kui on määratud ettevõttesisesed deebet- ja kreeditkontod.

Sageli ootame neid kliente, kes määravad tasakaalustava dimensiooni nii pearaamatu seadistuses kui ka finantsdimensiooni seadistuses. Sel juhul kasutab süsteem finantsdimensioonide funktsiooni. Tasakaalustamisdimensioonide seadistus finantsdimensiooni tasemel on sisestamisel eelistatud. Sisestamine nurjub, kui sisestamisdefinitsioon ei loo tasakaalustatud raamatupidamiskirjet finantsdimensiooni tasemel.

Järgige neid samme tasakaalustava dimensiooni kasutamise sisse lülitamiseks finantsdimensiooni tasemel.

1. Määrake, milline finantsdimensioon on tasakaalustav dimensioon.

    - Tasakaalustusdimensiooniks saate seada rohkem kui ühe finantsdimensiooni.
    - Ärge määrake veel finantsdimensioone, mis on vajalikud kande tasakaalustamiseks lehel **Finantsdimensioonid**.

2. Määratlege sisestamisdefinitsioonid iga töölehe või lähtedokumendi tüübi jaoks, mida teie organisatsioon kasutab. Sisestamisdefinitsioonid tarbivad pearaamatukontosid sisestamata töölehelt või lähtedokumendist kui ‘vastendamiskriteeriumid‘. Sisestamisdefinitsioon tagastab siis ‘loodud kirjed‘, millest saab raamatupidamiskirje. Kui sisestamisdefinitsioon on õigesti seadistatud, sisaldab loodud kirje pearaamatu vastendamiskriteeriumi kontosid ja lisakontosid raamatupidamiskirje tasakaalustamiseks dimensioonitasemel. Lisateavet vaadake teemast [Sisestamisdefinitsioonid](posting-definitions.md). 
   
   Sisestamisdefinitsioone ei toetata iga kandetüübi puhul. Näiteks ei saa sisestamisdefinitsioone määratleda kannetele, mis on sisestatud Üldise töölehe või Põhivara töölehe kaudu. Kui sisestamisdefinitsiooni ei saa töölehe või lähtedokumendi jaoks määratleda, tuleb kanne finantsdimensiooni väärtuses käsitsi tasakaalustada. Näiteks kui tehakse päevalehe kanne ja osakonna dimensioon on tasakaalustav dimensioon, peate tagama, et iga osakonna väärtus on tasakaalus.  Kui dimensioon ei ole iga osakonna väärtuse puhul tasakaalus, ei sisestata kannet enne, kui tasakaalustamatust parandatakse, lisades kandele käsitsi kontsernisisese deebeti või kreediti. 

    > [!IMPORTANT]
    > Kui üleliigne arv kandeid tuleb käsitsi tasakaalustada, **ei** tohiks te kasutada tasakaalustava dimensiooni funktsiooni lehel **Finantsdimensioonid**. Selle asemel kasutage tasakaalustava dimensiooni funktsiooni **Pearaamatu** seadistuslehel.

3. Pärast sisestamisdefinitsioonide määratlemist saab finantsdimensioonid märkida tasakaalustamiseks nõutavaks.

Kannete sisestamisel ja sisestamisel kutsutakse sisestusdefinitsioonid sisestamise ajal raamatupidamiskirjete määratlemiseks. Kui finantsdimensioonid on tasakaalus, toimub kinnitamine pärast raamatupidamiskirjete määratlemist. Kui finantsdimensioonid pole tasakaalus, siis kannet ei sisestata ja te saate sõnumi, mis näitab, et deebetid ei võrdu kindla dimensiooni kreeditsummadega.
