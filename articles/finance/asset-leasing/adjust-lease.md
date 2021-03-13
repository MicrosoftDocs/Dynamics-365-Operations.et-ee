---
title: Rendikirjete korrigeerimine
description: Teema selgitab, kuidas korrigeerida rendikirjet. Korrigeerimine võib olla vajalik, kui rendiperioodi muudetakse, renti pikendatakse või muud asjaolud muutuvad.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32d99d9e90b65f7cac74176d21fa4b053ae8f62c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130751"
---
# <a name="adjust-leases"></a>Rendikirjete korrigeerimine

[!include [banner](../includes/banner.md)]

Teema selgitab, kuidas korrigeerida rendikirjet. Korrigeerimine võib olla vajalik, kui rendiperioodi muudetakse, renti pikendatakse või muud asjaolud muutuvad. Vara rentimine vastab raamatupidamise standardite kodeerimise teema 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardi 16 (IFRS 16) ette nähtud rendikirje muutmise juhistele. ASC-842-20-15-1 määratleb rendikirje muudatused kui mis tahe lepingutingimuse muudatuse, mis põhjustab rendi ulatuse ja tasu muudatuse. IFRS 16 lõikes 39 on sätestatud, et rentnik peab rendikohustise uuesti hindama, et see vastaks rendimaksete muudatustele.

Organisatsioonide puhul, mis järgivad standardeid ASC 842 või IFRS 16, arvestatakse rent uuesti, et kajastada tulevaste rendimaksete minimaalse eelseatud väärtuse (PVFMLP) muudatus. Kui PVFMLP suureneb, debiteeritakse kasutamisõiguse esemeks oleva vara konto loodav töölehekirje ja krediteeritakse rendikohustise konto erinevus uue PVFMLP ja eelmise PVFMLP vahel. Kui PVFMLP väheneb, debiteeritakse rendikohustise konto töölehekirje ja krediteeritakse kasutusõiguse esemeks olev vara konto erinevus.

Kui korrigeerimine vähendab kasutamisõiguse esemeks olev vara nii, et see möödub nullist (0), krediteeritakse ülejäänud summa liisingu sisestamise kontol, mis on määratud lehel **Rendi sisestamise kontod**. Süsteem arvestab nende kannete ja muude korrigeerimise annetega nt klassifikatsiooni muudatused esmased otsekulutused, rendistiimulid, eelmaksed ja demonteerimiskulud, mis tulenevad rendi muudatustest.

Rendi muutmise tehingute konkreetseteks juhisteks soovitame vaadata IFRS 16 ja ASC 842.

## <a name="lease-adjustment-wizard"></a>Rendi korrigeerimisviisard

Rendi korrigeerimiseks tehke järgmised toimingud. Muudetud andmetega värskendatakse rendigraafikud pärast sisestamist viisardist **Rendi korrigeerimine**. Teil on võimalik igal ajal oma töö salvestada ja viisard sulgeda ning seejärel töö jätkamiseks hiljem naasta.

Viisardi **Rendi korrigeerimine** avamiseks rendi kokkuvõtte jaotisest tehke järgmist.

1. Avage **Vara rentimine \> Rentimised \> Rendi kokkuvõte**. 
2. Valige rent, mida soovite korrigeerida, ja seejärel tehke valik **Korrigeerimisviisard**.
3. Vajalike muudatuste sisestamiseks järgige viisardi viipasid.

Kui soovite avada viisardi **Rendi korrigeerimine** lehelt **Rendi korrigeerimised** juba töötluses oleva korrigeerimise jaoks, tehke järgmist.

1.  Avage jaotis **Rentimine \> Rentimised \> Rendi korrigeerimised**.
2.  Valige rent, mille korrigeerimise olek on **Käimas**, ja seejärel tehke valik **Korrigeerimisviisard**.
3.  Sisestage väljadele **Muutmise alguskuupäev** ja **Sisestuskuupäev** asjakohased kuupäevad.
4.  Valige **Edasi**.

    Rent on nüüd lisatud lehele **Rendi korrigeerimised**, kus saate sisestada selle kohta uue teabe.

    Pärast rendi korrigeerimist rakendatakse sellele kasutusõiguse aluseks olevate kaalutluste väljad. Kui muudetud rendiga ei ole seotud esmaseid otsekulutusi, rendimakseid, ettemakseid ega demonteerimiskulusid, jätke need väljad tühjaks. Algsed summad ei kohaldu värskendatud rendile. 

    Näiteks annab rendileandja rendi pikendamis kokkuleppe eest 1000 eurose soodustuse. Sel juhul, kui korrigeerite renti, et kajastada rendilepingu pikendamist, sisestage väljale **Korrigeerimisest tulenevad rendistiimulid** summa **1000**.

    Maksegraafiku ridadel kuvatakse nüüd kõik selle ja hilisemate kuude maksed väljal **Muutmise alguskuupäev**. Kuna muudatused on potentsiaalsed, ei saa maksegraafiku read alata enne muudatuse algust. Muutmise alguskuupäevale eelnevate maksegraafiku ridade kuvamiseks avage leht **Rendi versiooni ajalugu**.

8.  Valige **Edasi**.

    Järgmisel lehel kuvatakse oodatava rendi korrigeerimise põhiandmed, nagu rendikohustise bilansiline väärtus enne muudatust ja uus eeldatav rendikohustis pärast muudatust. Lehel kuvatakse ka eeldatava rendi korrigeerimise töölehekirje eelvaade.

9.  Kui rendi korrigeerimise töövoog on aktiivne ja korrigeerimist pole veel kinnitatud, tehke rendi korrigeerimise töövoosüsteemi edastamiseks valik **Edasta töövoogu**. Lisateavet rendi korrigeerimise töövoo kasutamise kohta vaadake jaotisest [Rendi korrigeerimise töövoogude kasutamine](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Seejärel arvutab süsteem ümber korrigeerimismuutujad, et kontrollida, et pärast korrigeerimisülevaate ja korrigeerimise töölehekirje esmast arvutamist poleks rendi suhtes sisestatud ühtegi kannet. Kui mõni väärtus muutub, värskendatakse korrigeerimise ülevaateruudustikku ja teil on võimalik teave üle vaadata enne rendi korrigeerimiste uuesti töövoosüsteemi edastamist.

10. Kui töövoog pole aktiivne või kui rendi korrigeerimine on kinnitatud, valige muudatuste töötlemiseks ja korrigeerimise töölehekirje sisestamiseks käsk **Lõpeta**.

    > [!NOTE] 
    > Seejärel arvutab süsteem ümber korrigeerimismuutujad, et kontrollida, et pärast korrigeerimisülevaate ja korrigeerimise töölehekirje esmast arvutamist poleks rendi suhtes sisestatud ühtegi kannet. Kui mõni väärtus muutub, värskendatakse korrigeerimise ülevaateruudustikku ja teil on võimalik enne käsu **Lõpeta** valimist muudatused üle vaadata. Kui töövoog on aktiivne ja rendi korrigeerimine on kinnitatud, põhjustab korrigeerimise ülevaate mis tahes muudatus kinnitusoleku naasmise olekusse **Esitamata**. Sel juhul peate rendi korrigeerimise uuesti töövoosüsteemi esitama.

    Lehel **Rendi korrigeerimised** on korrigeerimise olekuks nüüd määratud **Lõpule viidud**.

    Lehel **Rendi korrigeerimised** saate siiski vaadata kiirkaarte **Korrigeerimiste ülevaade** ja **Korrigeerimiskirje eelvaade**. Rendi üksikasjad ja kuupäevateave kuvatakse selle rendi versiooniajaloos.

    Muudetud teabe alusel luuakse nüüd uus rendiversioon ja uus graafikute kogum. 

13. Uute graafikute kuvamiseks avage rent ja tehke seejärel valik **Raamatud**.
14. Vastloodud maksegraafiku kuvamiseks tehke valik **Maksegraafik**.
15. Uue teabe alusel loodava rendikohustise amortiseerimise graafiku kuvamiseks sulgege leht **Maksegraafik** ja avage leht **Kohustise amortiseerumise graafik**.
16. Vastloodud vara kulumi graafiku vaatamiseks avage leht **Vara kulumi graafik** lehel **Raamatu üksikasjad**.
17. Korrigeerimise töölehekirje kuvamiseks tehke valikud **Töölehed \> Vara rentimise tööleht**.

## <a name="cancel-a-lease-adjustment"></a>Rendi korrigeerimise tühistamine

Poolelioleva rendikorrigeerimise kustutamiseks tehke järgmist.

1.  Avage jaotis **Rentimine \> Rentimised \> Rendi korrigeerimised**.
2.  Valige pooleliolev rendikorrigeerimine, mida soovite tühistada.
3.  Tehke valik **Tühista korrigeerimine**. 
4.  Valige nupp **OK**.

    > [!NOTE] 
    > Kui teete viisardis **Rendi korrigeerimine** valiku **Tühista**, tühistatakse viisardis viimasena lõpule viidud muudatus, kuid ei eemaldata pooleliolevat korrigeerimist.

## <a name="use-the-lease-adjustment-workflow"></a>Rendi korrigeerimise töövoo kasutamine

Selles jaotises selgitatakse, kuidas kasutada rendi korrigeerimise töövoogu. Rendi korrigeerimise töövoog aitab teil hallata rendi korrigeerimisi ühtsel viisil, andes ette kindlad kinnitamistoimingud ja määrates need kindlatele kasutajatele, kes kinnitavad rendi korrigeerimise enne selle lõplikuks saamist. Kui rendi korrigeerimine on töövoos kinnitatud, saate rendi korrigeerimise lõpule viimiseks kasutada viisardit **Rendi korrigeerimine**.

1.  Rendi korrigeerimise kinnitamiseks esitamiseks avage jaotis **Rentimine \> Rentimised \> Rendi korrigeerimised**.
2.  Valige rendi korrigeerimise rendi-ID ja seejärel tehke valik **Korrigeerimisviisard**.
3.  Valige viisardi viimasel lehel käsk **Edasta kinnitamiseks**.
4.  Sisestage kommentaar korrigeerimise kohta ja seejärel tehke valik **OK**.

    Töövoo olekuks määratakse **Kinnitamise ootel** ja kõik viisardi väljad lukustatakse redigeerimiseks.

5.  Rendi korrigeerimise kinnitamiseks avage jaotis **Rentimine \> Rentimised \> Rendi korrigeerimised**.
6.  Valige rendi korrigeerimise rendi-ID ja vaadake üle kiirkaardid **Korrigeerimiste ülevaade** ja **Korrigeerimiskirje eelvaade**.
7.  Tehke valikud **Töövoog \> Kinnitatud**.

    Lehel **Rendi korrigeerimised** on töövoo olekuks nüüd määratud **Kinnitatud**. Nüüd on rendi korrigeerimine valmis korrigeerimise töölehe kirje kaudu sisestamiseks.

8.  Rendi korrigeerimise töötlemise jätkamiseks ja korrigeerimiskirje sisestamiseks avage jaotis **Rentimine \> Rentimised \> Rendi korrigeerimised**.
9.  Valige rendi korrigeerimise rendi-ID ja seejärel tehke valik **Korrigeerimisviisard**.
10. Liikuge nupu **Edasi** abil viisardi viimasele lehele, ja seejärel tehke valik **Lõpeta**.

Süsteem arvutab ümber rendi bilansilise väärtuse, tagamaks, et kinnitatud korrigeerimismuutujad oleksid ajakohased. Muudatuste korral määratakse kinnitusolekuks uuesti **Mustand** ja te peate töövoosüsteemis rendi korrigeerimise uuesti esitama.

## <a name="view-lease-versions"></a>Rendi versioonide vaatamine

Kui rendikirjet on korrigeeritud, saate vaadata selle erinevaid versioone. Lisaks saate vaadata ajaloolisi graafikuid ja varasemate rendikirjete üksikasju.

1. Valige lehel **Rendikokkuvõte** rendikirje ja valige seejärel tegevuspaanil suvand **Rendi versiooni ajalugu**.

    Kui valitud rendikirjet on korrigeeritud, kuvatakse lehel **Rendi versiooni ajalugu** selle erinevad versioonid. Algne rendikirje on sildiga **1** ja järgnevad versioonid on tõusvas numbrilises järjestuses.

    Valitud rendi versiooni puhul saate vaadata finantsdimensioone, lepingu üksikasju, asukohta ja maksegraafiku ridu.

2. Ajalooliste graafikute vaatamiseks avage muudetud rendikirje lehelt **Rendi kokkuvõte**, valige soovitud raamat ja valige seejärel tegevuspaanil suvand **Raamatu versiooni ajalugu**.
3. Valige lehel **Raamatu versioon** versioon ja ajakava, mida kuvada.
