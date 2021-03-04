---
title: Hüvitise struktuuri arendamine
description: See artikkel annab ülevaate põhipalga plaani loomisest ja sobivusreeglite abil töötajate plaani lisamisest.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418182"
---
# <a name="develop-a-compensation-structure"></a>Hüvitise struktuuri arendamine

See artikkel annab ülevaate põhipalga plaani loomisest ja sobivusreeglite abil töötajate plaani lisamisest. See artikkel kasutab USMF-i demoandmeid ja kehtib hüvitise ja soodustuste halduritele.

## <a name="create-a-fixed-compensation-plan"></a>Põhipalga plaani loomine

1. Valige suvand **Hüvituste haldus**.

2. Valige suvand **Põhipalga plaanid**.

3. Valige suvand **Uus**.

4. Sisestage väärtus väljale **Plaan**.

5. Sisestage väärtus väljal **Kirjeldus**.

6. Väljale **Jõustumiskuupäev** sisestage kuupäev.

7. Väljal **Tüüp** valige, kas põhipalgaplaan on **rea-**, **klassi-** või **etapiplaan**.

8. Märkeruut **Soovitamine lubatud** toimib protsessi sündmusena plaani lisatud mistahes tegevuse vaikeväärtusena. Tasu töötlemisel saate soovituste lubamisega tühistada arvutatud juhise summa.

9. Väli **Vahemikust väljajäämise tolerants** võimaldab määrata, kuidas käsitletakse tasusummasid, mis ei kuulu antud tasemel määratletud tasustruktuuri vahemikku. Välja **Vahemikust väljajäämise tolerants** määramine suvandile **Puudub** võimaldab kasutada mis tahes hüvitise summat. Suvand **Paindlik tolerants** hoiatab kasutajaid, kui hüvitise summa on selle taseme viitepunkti summade miinimumist väiksem või maksimumist suurem. Kasutajad võivad hoiatust ignoreerida ja jätkata. Valik **Jäik tolerants** annab tõrketeate, kui töötaja tasu jääb väljapoole taseme minimaalset või maksimaalset viitepunkti ning töötaja tasu korrigeeritakse automaatselt määratud vahemikku.

10. Väli **Palkamise reegel** arvutab protsessi sündmuse ajal töötaja hüvitise. Suvandi **Palkamise reegel** valik **Protsent** arvutab tõusu, mis jaotub proportsionaalselt töötaja töötamise ajale.

11. Sisestage väärtus väljale **Valuuta**.

12. Sisestage või valige väärtus väljal **Palgamäära teisendamine**.

13. Laiendage jaotist **Palgavahemiku kasutusastme maatriks**. Valikuliselt saate lisada palgavahemiku kasutusastme kirjed, et töötajad jõuaksid kiiremini keskpunkti ja aeglasemalt maksimaalsesse vahemikku.

14. Valige käsk **Salvesta**. See aktiveerib nupu **Hüvitise seadistamine** nupu ja võimaldab jätkata plaani hüvitise struktuuri määratlemisega.

15. Valige suvand **Hüvitise seadistamine**. Saate luua hüvitise struktuuri kasutades üht järgmise kolme viisi seast.

    - Looge täiesti uus struktuur, valides viitepunktide komplekti ja lisades tasemed, et luua oma struktuur.
    - Kopeerige hüvitise struktuur olemasolevast plaanist lähtepunktina kasutamiseks ja muutke seda uue plaani jaoks.
    - Valige olemasolev hüvitise ruudustik. Kui mõni muu plaan juba kasutab hüvitise ruudustikku, kajastuvad kõik ruudustikus tehtud muudatused ka teises plaanis.

16. Valige suvand **Loo uus olemasolevast tasumaatriksist**.

17. Sisestage või valige väärtus väljal **Kopeeri ruudustikust**. Teise võimalusena saate muuta uue hüvitise ruudustiku nime, mille valitud ruudustiku kopeerimisega lõite.

18. Valige nupp **OK**.

19. Valige suvand **Massmuudatus**. **Massmuudatus** võimaldab teil säilitada hüvitise maatriksi summad, tõstes üht või mitut taset ja/või viitepunkti protsendi või kindla summa võrra.

20. Sisestage arv väljale **Korrigeerimissumma**.

21. Märkige või tühjendage loendis kõik read.

22. Klõpsake käsku **Rakenda ruudustikule**.

23. Sulgege leht. Pärast hüvitise struktuuri loomist saate valida, milliseid viitepunkte põhipalgaplaani kontrollpunktina kasutada. Kontrollpunkti kasutatakse töötaja võrdlusteguri arvutamiseks.

24. Sisestage või valige väärtus väljal **Kontrollpunkt**.

25. Sulgege leht.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Põhipalgaplaanile sobivuse reegli loomine

Te ei saa põhipalgaplaani töötajale määrata enne, kui määratlete plaani jaoks on sobivuse reeglid.  

1. Valige suvand **Sobivuse reeglid**.

2. Valige suvand **Uus**.

3. Sisestage väärtus väljal **Sobivus**.

4. Sisestage väärtus väljal **Kirjeldus**.

5. Väljale **Jõustumiskuupäev** sisestage kuupäev. Nii põhipalga kui ka tulemustasu plaanid kasutavad sobivuse reegleid. Valige plaani tüüp väljal **Tüüp**.

6. Sisestage või valige väärtus väljal **Plaan**. Valige, millistele kriteeriumidele peab tasuplaanile sobiv töötaja vastama. Kriteeriumid võivad hõlmata järgmist.

    - **Osakond**
    - **Ametiühing**
    - **Asukoht** (**Hüvituspiirkond**)
    - **Töö**
    - **Funktsioon**
    - **Töö tüüp**
    - **Hüvituse tase**
    
    Töötaja on tasuplaani jaoks sobiv, kui ta vastab kõigile määratud kriteeriumidele. Kui te ühtegi kriteeriumit ei määra, on kõik töötajad hüvitusplaani jaoks sobilikud. Kui töötaja ei vasta sobivuse reeglis määratletud kriteeriumitele või sobivuse reeglit ei ole hüvitusplaani jaoks määratletud, siis töötaja jaoks põhipalga kirje loomisel ei kuvata hüvitusplaani otsingus.

7. Sulgege leht.

8. Sulgege leht.



[!INCLUDE[footer-include](../includes/footer-banner.md)]