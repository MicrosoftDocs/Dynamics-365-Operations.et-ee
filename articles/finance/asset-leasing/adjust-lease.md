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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442578"
---
# <a name="adjust-leases"></a>Rendikirjete korrigeerimine

[!include [banner](../includes/banner.md)]

Teema selgitab, kuidas korrigeerida rendikirjet. Korrigeerimine võib olla vajalik, kui rendiperioodi muudetakse, renti pikendatakse või muud asjaolud muutuvad. Vara rentimine vastab raamatupidamise standardite kodeerimise teema 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardi 16 (IFRS 16) ette nähtud rendikirje muutmise juhistele. ASC-842-20-15-1 määratleb rendikirje muudatused kui mis tahe lepingutingimuse muudatuse, mis põhjustab rendi ulatuse ja tasu muudatuse. IFRS 16 lõikes 39 on sätestatud, et rentnik peab rendikohustise uuesti hindama, et see vastaks rendimaksete muudatustele.

Organisatsioonide puhul, mis järgivad standardeid ASC 842 või IFRS 16, arvestatakse rent uuesti, et kajastada tulevaste rendimaksete minimaalse eelseatud väärtuse (PVFMLP) muudatus. Kui PVFMLP suureneb, debiteeritakse loodav töölehe kirje kasutamisõiguse esemeks oleva vara ja krediteeritakse rendikohustise erinevust uue PVFMLP ja eelmise PVFMLP vahel. Kui PVFMLP väheneb, debiteeritakse rendikohustise töölehe kirje ja krediteeritakse kasutusõiguse esemeks olev vara erinevus.

Kui korrigeerimine vähendab kasutamisõiguse esemeks olev vara nii, et see möödub nullist (0), krediteeritakse ülejäänud summa liisingu sisestamise kontol, mis on määratud lehel **Rendi sisestamise kontod**. Süsteem arvestab nende kannete ja muude korrigeerimise annetega nt klassifikatsiooni muudatused esmased otsekulutused, rendistiimulid, eelmaksed ja demonteerimiskulud, mis tulenevad rendi muudatustest.

Rendi muutmise tehingute konkreetseteks juhisteks soovitame vaadata IFRS 16 ja ASC 842.

Rendi muutmiseks tehke järgmist. Muudetud andmed värskendatakse rendigraafikutes pärast toimingu Loo graafik käivitamist.

1. Avage **Vara rentimine \> Rentimised \> Rendi kokkuvõte**.
2. Valige lehel **Rendi kokkuvõte** korrigeerimiseks rendikirje ja valige seejärel **Rendikirje korrigeerimine**.
3. Lehel **Rendikirje korrigeerimine** sisestage korrigeeritud rendikirje jaoks uus teave.

    Pange tähele, et leht **Rendikirje korrigeerimine** sarnaneb lehele **Rendikirje lisamine**. Lisaks sarnaselt rendikirje lisamisel määratletav alguskuupäev teeb kindlaks uue rendi alguse, määratleb väli **Muutmise kuupäev** lehel **Rendikirje korrigeerimine** muudetud rendiperioodi algusaja. Seda kuupäev ei saa määrata hilisemaks kui maksegraafiku rea alguskuupäev.

    > [!NOTE]
    > Rendi korrigeerimistele rakenduvad väljad **Kasutusõiguse aluseks olevad kaalutlused**. Kui muudetud rendiga ei ole seotud esmaseid otsekulutusi, rendimakseid, ettemakseid ega demonteerimiskulusid, jätke need väljad tühjaks. Algsed summad ei kohaldu värskendatud rendile. Kõik lisakulud, mis rendi muutmise ajal tekivad, tuleb sisestada lehel **Rendikirje korrigeerimine**.
    > 
    > Näiteks annab rendileandja rendi pikendamis kokkuleppe eest 1000 eurose soodustuse. Sel juhul, kui korrigeerite renti pikendamise konto jaoks, sisestate väljale **Rendistiimulid** summa **1000**. Kui rendi korrigeerimisega ei seostata ühtegi stiimulit, peate tühjendama mis tahes eelnevalt sellele väljale sisestatud väärtuse. Sama loogikat rakendatakse teistele kasutusõiguse aluseks olevatele kaalutlustele.

    Korrigeeritud rendi maksegraafiku read tuleb luua potentsiaalsuse alusel. Potentsiaalsuse alusel loodavad maksegraafiku read ei saa alata enne rendi korrigeerimiste jõustumist.

    Järgmised sammud on peaaegu identsed rendi algse tuvastamise etappidega.

4. Kohandatud maksegraafiku loomiseks valige käsk **Loo graafikud**. Teile kuvatakse teade, mis teatab, et rendikirje jaoks on loodud maksegraafik.

    > [!IMPORTANT]
    > Enne suvandi **Loo graafikud** valimist veenduge, et muutmiskuupäeva ja maksegraafiku read oleks täpsed. Veenduge ka selles, et kõik esmased otsekulutused, rendistiimulid, ettemaksed või demonteerimiskulud vastaksid ainult korrigeerimise käigus tekkivatele kuludele.

5. Vastloodud maksegraafiku vaatamiseks valige suvand **Raamatud** ja avage leht **Maksegraafik**.
6. Lehel **Maksegraafik** saate muuta korrigeeritud maksesummasid enne, kui maksegraafiku kinnitate. Graafiku kinnitamiseks valige **Kinnita graafik**.

    Kui maksegraafik on kinnitatud, luuakse uus vara kulum ja uus rendikohustise graafik.

7. Uue rendikohustise amortiseerimise graafiku vaatamiseks, mis luuakse uutest sisenditest, sulgege leht **Maksegraafik** ja avage leht **Kohustise amortiseerumise graafik**.
8. Vastloodud vara kulumi graafiku vaatamiseks avage leht **Vara kulumi graafik** lehel **Raamatu üksikasjad**.
9. Korrigeerimise töölehe kirje loomiseks valige **Funktsioon \>Rendi korrigeerimine**. Teile kuvatakse teade, et korrigeerimise töölehe kirje on loodud. 
10. Töölehe kirje vaatamiseks valige **Töölehed \> Vara rentimise tööleht**.
11. Töölehe kirje sisestamiseks valige rida ja valige seejärel käsk **Sisesta**.

## <a name="view-lease-versions"></a>Rendi versioonide vaatamine

Kui rendikirjet on muudetud, saate vaadata selle erinevaid versioone. Lisaks saate vaadata ajaloolisi graafikuid ja varasemate rendikirjete üksikasju.

1. Valige lehel **Rendikokkuvõte** rendikirje ja valige seejärel tegevuspaanil suvand **Rendi versiooni ajalugu**.

    Kui valitud rendikirjet on korrigeeritud, kuvatakse lehel **Rendi versiooni ajalugu** selle erinevad versioonid. Algne rendikirje on sildiga **1** ja järgnevad versioonid on tõusvas numbrilises järjestuses.

    Valitud rendi versiooni puhul saate vaadata finantsdimensioone, lepingu üksikasju, asukohta ja maksegraafiku ridu.

2. Ajalooliste graafikute vaatamiseks avage muudetud rendikirje lehelt **Rendi kokkuvõte**, valige soovitud raamat ja valige seejärel tegevuspaanil suvand **Raamatu versiooni ajalugu**.
3. Valige lehel **Raamatu versioon** vaatamiseks soovitud versioon ja soovitud ajakava.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]