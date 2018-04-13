--- 
title: "Palga/hüvituse struktuuri ja plaanide arendamine"
description: "Selles tegevuse juhises näitlikustatakse, kuidas luua põhitasuplaani ning sobivuse reegleid kasutades lubada töötajate registreerimine plaani."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63a02a64ff28531bae950f1b61d9167eaa0b0373
ms.openlocfilehash: 7fd32467cfbc8c30b398659d16b268f183b6b3d3
ms.contentlocale: et-ee
ms.lasthandoff: 11/01/2017

---
# <a name="develop-salarycompensation-structure-and-plans"></a>Palga/hüvituse struktuuri ja plaanide arendamine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Selles tegevuse juhises näitlikustatakse, kuidas luua põhitasuplaani ning sobivuse reegleid kasutades lubada töötajate registreerimine plaani. Selles ülesandes on kasutatud näidisettevõtte USMF-i andmeid ning ülesanne on mõeldud hüvitise ja eeliste halduritele.


## <a name="create-fixed-compensation-plan"></a>Põhipalgaplaani loomine
1. Klõpsake valikut Tasuhaldus.
2. Klõpsake valikut Põhipalga plaanid.
3. Klõpsake valikut Uus.
4. Sisestage väärtus väljale Plaan.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Sisestage kuupäev väljale Jõustumiskuupäev.
7. Väljal Tüüp valige, kas põhipalgaplaan on rea-, klassi- või etapiplaan.
8. Märkeruut Soovitamine lubatud toimib protsessi sündmusena plaani lisatud mistahes tegevuse vaikeväärtusena.  Tasu töötlemisel saate soovituste lubamisega tühistada arvutatud juhise summa.
9. Vahemikust väljajäämise tolerants võimaldab määrata, kuidas käsitletakse tasusummasid, mis ei kuulu antud tasemel määratletud tasustruktuuri vahemikku.  Valik Vahemikust väljajäämise tolerantsi pole võimaldab kasutada mistahes tasusummat.  Valik Väike kõikumine hoiatab kasutajat, kui tasusumma on väiksem kui taseme minimaalne viitepunkti summa või suurem kui taseme maksimaalne summa. Kasutaja võib hoiatust ignoreerida ja jätkata.  Valik Suur kõikumine annab tõrketeate, kui töötaja tasu jääb väljapoole taseme minimaalset või maksimaalset viitepunkti ning töötaja tasu korrigeeritakse automaatselt määratud vahemikku.
10. Välja Palkamise reegel kasutatakse, kui töötaja tasu arvutamiseks käitatakse tasuprotsessi sündmust.  Palkamise reegel protsent arvutab tõusu, mis jaotub proportsionaalselt töötaja töötamise ajale.
11. Sisestage väärtus väljale Valuuta.
12. Sisestage või valige väärtus väljal Palgamäära teisendamine.
13. Laiendage jaotist Palgavahemiku kasutusastme maatriks.
    * Valikuliselt saate lisada palgavahemiku kasutusastme kirjed, et töötajad jõuaksid kiiremini keskpunkti ja aeglasemalt maksimaalsesse vahemikku.  
14. Siinkohal tuleb teil salvestada põhitasuplaan, et lubada nupp Häälesta tasu ja jätkata plaani tasustruktuuri määratlemist.  Klõpsake nuppu Salvesta.
15. Klõpsa nuppu Häälesta tasu.
    * Tasustruktuuri loomiseks on kolm võimalust. 1. Täiesti uue struktuuri loomiseks valige viitepunktide komplekt ja lisage tasemed. 2. Uue plaani võite luua ka olemasolevast plaanist tasustruktuuri kopeerides ja seda oma plaani loomisel lähtekohana kasutades. 3. Võite valida olemasoleva tasuruudustiku. Kui tasuruudustik on juba kasutusel mõnes muus plaanis, kajastuvad ruudustikus tehtud muudatused ka teises plaanis.  
16. Valige suvand Loo uus olemasolevast tasumaatriksist.
17. Sisestage või valige väärtus väljal Kopeeri ruudustikust.
    * Alternatiivina saate valitud ruudustikule uut nime andes luua selle koopiana uue tasuruudustiku.  
18. Klõpsake nuppu OK.
19. Klõpsake valikut Massmuudatus.
    * Massmuudatust kasutades saate säilitada tasumaatriksi summad, tõstes üht või mitut taset ja/või viitepunkti protsendi või kindla summa võrra.  
20. Sisestage arv väljale Korrigeerimissumma.
21. Märkige või tühjendage loendis kõik read.
22. Klõpsake käsku Rakenda ruudustikule.
23. Sulgege leht.
    * Tasustruktuuri loomise või valimise järel saate valida, milliseid viitepunkte tuleks kasutada põhipalgaplaani kontrollpunktina.  Kontrollpunkti kasutatakse töötaja võrdlusteguri arvutamiseks.  
24. Sisestage või valige väärtus väljal Kontrollpunkti väli.
25. Sulgege leht.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Uuele põhipalgaplaanile sobivuse reegli loomine
    * Uut põhipalgaplaani ei saa töötajale määrata enne, kui plaani jaoks on määratletud sobivuse reeglid.  
1. Klõpsake valikut Sobivuse reeglid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Sobivus.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage kuupäev väljale Jõustumiskuupäev.
    * Sobivuse reegleid kasutatakse nii põhipalga kui ka tulemustasu plaanide puhul.  Valige väljal Tüüp, mis tüüpi plaani jaoks need sobivuse reeglid on mõeldud.  
6. Valige või sisestage väärtus väljal Plaan.
    * Valige, millistele kriteeriumidele peab tasuplaanile sobiv töötaja vastama. Kriteeriumid võivad hõlmata osakonda, ametiühingut, asukohta (tasupiirkonda), tööd, funktsiooni, töö tüüpi või tasu taset. Töötaja on tasuplaani jaoks sobiv, kui ta vastab kõigile määratud kriteeriumidele. Kui määratud ei ole ühtki kriteeriumi, on kõik töötajad tasuplaani jaoks sobilikud. Kui loote töötajale põhipalga kirjet, kuid töötaja ei vasta kõigile sobivuse reegli kriteeriumidele või tasuplaanile ei ole määratud sobivuse reeglit, ei kuvata tasuplaani otsingus.  
7. Sulgege leht.
8. Sulgege leht.


