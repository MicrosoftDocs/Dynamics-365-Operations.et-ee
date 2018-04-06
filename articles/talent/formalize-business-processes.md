---
title: "Äriprotsesside formaliseerimine"
description: "Äriprotsessi funktsioon võimaldab luua äriprotsessi malli protsesside jaoks, mida teie organisatsioonis läbi viiakse."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: 48f80eac5009e1a241d501b0c4a3a70b78f5d709
ms.contentlocale: et-ee
ms.lasthandoff: 03/23/2018

---
# <a name="formalize-business-processes"></a>Äriprotsesside formaliseerimine
Äriprotsessi funktsioon võimaldab luua äriprotsessi malli protsesside jaoks, mida teie organisatsioonis läbi viiakse. Näiteks võib teie ettevõte igal aastal läbi viia personaliauditi. Saate luua malli, mille abil jälgida kõiki auditi ülesandeid, aidates tagada, et kõik ülesanded tehakse iga kord, kui protsessi läbi viiakse ja vajadusel ka tagada ülesannete õiges järjekorras läbiviimise. Malle saab korduvate protsesside puhul uuesti kasutada või kopeerida kasutamaks neid uute loomise lähtepunktina.

Pärast malli loomist saab protsessi käivitada ja seda jälgida äriprotsessi tööruumis.  Äriprotsessi käivitamisel määratakse ülesannete täitmiseks sobivad inimesed ja tähtaeg. Nendest komponentidest saab üksikasjaliku ülevaate altpoolt.

## <a name="business-process-template"></a>Äriprotsessi mall
Äriprotsessi mallis on loendatud ülesannete grupp, mis moodustab äriprotsessi. Personalijuhid ja assistendid saavad vaikimisi äriprotsesse luua.  Seda saab turbekonfiguratsioonis kohustust Halda üldisi äriprotsesse redigeerides muuta.

Igale protsessile saab määrata protsessi omaniku.  Protsessi omanik näeb kõiki protsessi ülesandeid, saab ülesandeid uuesti määrata või tähtaegu muuta.  Näiteks saab personalidirektor luua äriprotsessi malli eeliste ülevaatamiseks.  Hüvitise ja eeliste halduri saab määrata protsessi omanikuks, nii et tal on ülevaade ülesannetest, mis ülevaatuse käigus täita tuleb.  Protsessi omanik ei saa luua või kustutada aktiivseid äriprotsesse või äriprotsessi malle.

## <a name="task"></a>Ülesanne
Äriprotsess hõlmab sageli mitut ülesannet. Mõnd ülesannet, näiteks ettevõttesiseste kursuste pakkumiste ülevaatamist, saab täita rakenduses Dynamics 365 for Talent[?]. Sel juhul valitakse väljal Ülesande link menüükäsk. Muud ülesanded võivad hõlmata veebisaidi vormide ülevaatamist ja täitmist. URL-i valimine väljal Ülesande link võimaldab veebiaadressi sisestada. Sellel väljal saate sisestada nii välis- kui ka sisesaitide URL-e. Samuti saate luua ülesandeid tegevustele, mida teete käsitsi, näiteks struktuuride juurdepääsetavuse ülevaatamine. Sel juhul pole ülesande link vajalik. Sedasi on võimalik jälgida mitmesuguseid ülesandeid ulatusliku protsessi abil.

Ülesandeid on võimalik määrata kindlale töötajale või ametikohale. Näiteks on hüvitise ja eeliste haldur alati see inimene, kes vaatab üle kindlustusmaksed.   Valige selle ülesande loomisel määramise tüübiks ametikoht ja seejärel valige ametikohtade loendist hüvitise ja eeliste haldur. Protsessi käivitamisel määratakse ülesanne töötajale, kelle ametikohaks on hüvitise ja eeliste haldur. Samuti saate ülesande konkreetsele töötajale määrata, kui valite väljal Määramise tüüp suvandi Töötaja ja seejärel valite sobiva inimese.

Ülesande tähtajad olenevad protsessi alguses sisestatud sihtkuupäevast. Mõni ülesanne tuleb täita enne sihtkuupäeva ja mõne võib täita pärast sihtkuupäeva.  Ülesande määramisel sisestage sihtkuupäevaga seotud tähtaeg väljal Tähtaja nihe sihtkuupäevast alates. Oletame näiteks, et hüvitise ja eeliste haldur peab vaatama kindlustusmaksed üle kümme päeva enne personaliauditi lõppu. Loodud ülesandel on sihtkuupäevaga võrreldes tähtaeg -10. Seetõttu, kui protsess käivitatakse 13. mail, on ülesande tähtajaks 3. mai. Märkus. Tähtaegu saab korrigeerida ka pärast protsessi algust.

Keerukate ülesannete puhul võib vaja olla mitut etappi või lisateavet ülesannet täitvalt töötajalt. Ülesandele on võimalik lisada juhiseid ja neid rikastekstina vormindada. Juhistes saab ülesande täitjale ülesande täitmise kohta täiendavat teavet anda.

Protsessi käivitamine Protsessi saab käivitada äriprotsessi mallis, valides Protsessi käivitamine.  Protsessi käivitamisel luuakse valitud töötajate ja/või ülesannetes määratletud ametikohtadele ülesanded, mis kaasatakse äriprotsessi malli. Igale ülesandele määratakse ka tähtaeg liites või lahutades nihkunud päevade arvu sihtkuupäevast (vaadake nihkunud päevi puudutavat teavet ülesande jaotisest). Aktiivseid äriprotsesse saab vaadata äriprotsesside tööruumis. 

## <a name="employee-self-service"></a>Töötaja iseteenindus
Kui töötajale määratakse ülesanne, saab neile määratud ülesandeid vaadata lehel Töötaja iseteenindus. Töötajad, kellele on määratud äriprotsessi ülesanne, saavad lehel Töötaja iseteenindus vaadata ülesannet, selle kirjeldust, juhiseid ja kontaktisiku nime ning avada seotud Dynamics365 lehe või veebilehe. Ülesandeid saab tähistada kui pooleliolevad, tühistatud või lõpetatud.

## <a name="business-process-workspace"></a>Äriprotsessi tööruum
Personalispetsialistid saavad aktiivseid äriprotsesse vaadata äriprotsessi tööruumis. Tööruumis on loetletud kõik aktiivsed protsessid ja nendega seotud ülesanded. Ulatuslikku ülesandeloendit on võimalik tähtaja põhjal filtrida. Lehel on loetletud ka tähtajast üle läinud ülesanded ja ülesanded, mis on just konkreetselt personalispetsialistile määratud. Samuti saavad nad kõigi ülesannete olekuid värskendada ja vajaduse korral ülesandeid uuesti määrata, et üldine äriprotsess liiguks edasi.

## <a name="my-business-processes-workspace"></a>Minu äriprotsesside tööruum
Protsessi omanikud saavad endale määratud aktiivseid äriprotsesse vaadata Minu äriprotsessi tööruumis. Tööruumis on loetletud kõik kasutaja aktiivsed protsessid ja nendega seotud ülesanded.  Ulatuslikku ülesandeloendit on võimalik tähtaja põhjal filtrida. Lehel loetletakse konkreetselt protsessi omanikule määratud ülesanded. Protsessi omanik saab ka kõigi ülesannete olekut värskendada ja ülesandeid uuesti määrata.

## <a name="navigating-business-processes"></a>Äriprotsesside navigeerimine
1.   Äriprotsessi malli lisamiseks avage Äriprotsessid- lingid – Äriprotsesside haldamine.
 - a.   Suvandiga Uus luuakse uus mall.
 - b.   Suvandiga Mallist kopeerimine kopeeritakse valitud mall uude.
 - c.   Suvandiga Protsessi käivitamine käivitatakse valitud äriprotsess, määratakse ülesanded ja arvutatakse tähtajad.  
2.  Aktiivsete protsesside ja seotud ülesannete vaatamiseks minge äriprotsesside tööruumi.

