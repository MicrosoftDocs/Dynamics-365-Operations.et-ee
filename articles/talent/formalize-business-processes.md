---
title: Äriprotsesside formaliseerimine
description: See teema selgitab, kuidas saate kasutada äriprotsessi funktsiooni, et luua äriprotsessi malli protsesside jaoks, mis tuleb teie organisatsioonis läbi viia.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 0f4d2b8e5f78c5815c5ad7e5eae0d13ad7d15c12
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460880"
---
# <a name="formalize-business-processes"></a>Äriprotsesside formaliseerimine

Äriprotsessi funktsioon võimaldab luua äriprotsessi malli äriprotsesside jaoks, mis tuleb teie organisatsioonis läbi viia. Näiteks läbib teie ettevõtte igal aastal inimressursside (HR) auditi. Sel juhul saate luua malli, mis jälgib kõiki ülesanded, millest auditiprotsess koosneb. See mall aitab seejärel tagada, et auditi tegemise ajal on alati kõik ülesanded tehtud. Lisaks, kui ülesanded tuleb lõpule viia kindlas järjekorras, aitab mall tagada, need on tehtud õiges järjekorras.

Malli saab korduvate protsessida jaoks uuesti kasutada. Samuti saab malle kopeerida ja kasutada lähtekohana uute mallide loomiseks.

Pärast äriprotsessi malli loomist saab äriprotsessi käivitada ja seda jälgida tööruumis **Äriprotsess**. Äriprotsessi käivitamisel määratakse ülesannete täitmiseks sobivad inimesed ja tähtaeg.

## <a name="business-process-templates"></a>Äriprotsessi mallid
Äriprotsessi mallis on loendatud ülesannete grupp, mis moodustab äriprotsessi. Vaikimisi saavad personalijuhid ja assistendid äriprotsesse luua. Kuid saate äriprotsess loovaid rolle muuta, muutes turbekonfiguratsioonis kohustust **Halda üldisi äriprotsesse**.

Igale äriprotsessile saate määrata protsessi omaniku. Protsessi omanik näeb kõiki protsessi ülesandeid, saab ülesandeid uuesti määrata või tähtaegu muuta. Näiteks loob personalidirektor äriprotsessi malli eeliste ülevaatamiseks ning määrab hüvitise ja eeliste halduri protsessi omanikuks. Seejärel näeb hüvitise ja eeliste haldur ülesandeid, mis tuleb lõpule viia ülevaatuse osana.

Protsessi omanik ei saa luua uusi äriprotsesse või äriprotsessi malle ega kustutada aktiivseid äriprotsesse või äriprotsessi malle.

## <a name="tasks"></a>Ülesanded
Äriprotsess koosneb sageli mitmest ülesandest. Mõnd ülesannet, näiteks ettevõttesiseste kursuste pakkumiste ülevaatamist, saab lõpule viia rakenduses Microsoft Dynamics 365 Talent. Sel juhul valitakse väljal **Ülesande link** suvand. Muud ülesanded võivad hõlmata veebisaidi lehtede ülevaatamist ja täitmist. Sel juhul valitakse väljal **Ülesande link** **URL**, misjärel saab sisestada veebiaadressi. Saate sisestada nii välis- kui ka sisesaitide URL-e. Samuti saate luua ülesandeid tegevustele, mida teete käsitsi, näiteks struktuuride juurdepääsetavuse ülevaatamine. Sel juhul pole ülesande link vajalik. Sedasi on võimalik jälgida mitmesuguseid ülesandeid ulatusliku protsessi abil.

Ülesandeid on võimalik määrata kas kindlale töötajale või ametikohale. Näiteks on hüvitise ja eeliste haldur alati see inimene, kes vaatab üle kindlustusmaksed. Seetõttu valige selle ülesande loomisel **Ametikoht** väljal **Määramise tüüp** ja seejärel valige **Hüvitise ja eeliste haldur** loendis **Ametikoht**. Äriprotsessi käivitamisel määratakse ülesanne töötajale, kelle ametikohaks on **Hüvitise ja eeliste haldur**. Ülesande määramiseks konkreetsele töötajale valige väljal **Määramise tüüp** suvand **Töötaja** ja seejärel valige sobiv inimene.

Ülesannete tähtajad olenevad äriprotsessi alguses sisestatud sihtkuupäevast. Mõni ülesanne tuleb täita enne sihtkuupäeva ja mõne võib täita pärast sihtkuupäeva. Ülesande määramisel sisestage väljal **Tähtaja nihe sihtkuupäevast alates** sihtkuupäevaga seotud tähtaeg. Hüvitise ja eeliste haldur peab vaatama kindlustusmaksed üle kümme päeva enne personaliauditi lõpule viimist. Sellisel juhul on ülevaatuse jaoks loodud ülesandel valiku **Tähtaja nihe sihtkuupäevast alates** väärtus **–10**. Seetõttu, kui äriprotsess käivitatakse 13. mail, on ülesande tähtajaks 3. mai.

> [!NOTE]
> Tähtaegu saab korrigeerida ka pärast äriprotsessi algust.

Keerukate ülesannete puhul võib vaja olla mitut etappi või ülesandeid täitvad inimesed peavad esitama lisateavet. Nende stsenaariumide korral saate ülesandele lisada juhised. Juhised annavad ülesande täitjale ülesande täitmise kohta täiendavat teavet. Saate juhistesse lisada ka rikasteksti vormingut.

## <a name="starting-a-business-process"></a>Äriprotsessi käivitamine
Äriprotsessi mallis saate käivitada äriprotsessi, vali **Käivita protsess**. Protsessi käivitamisel luuakse valitud töötajate ja/või ülesannetes määratletud ametikohtadele ülesanded, mis kaasatakse malli. Igale ülesandele määratakse ka tähtaeg, liites või lahutades nihkunud päevade arvu sihtkuupäevast, nagu on selgitatud jaotises „Ülesanded”. Aktiivseid äriprotsesse saate vaadata tööruumis **Äriprotsessid**.

## <a name="employee-self-service"></a>Töötaja iseteenindus
Kui ülesanne on määratud töövõtjale, saab ta seda ja kõiki temale määratud ülesandeid vaadata lehel **Töövõtja iseteenindus**. Iga töövõtjale määratud äriprotsessi juures näeb töövõtja ülesande nime ja kirjeldust, selle lõpule viimise juhiseid ja kontaktisiku nime. Lehel **Töövõtja iseteenindus** saab töövõtja ka avada seostatud lehe rakenduses Microsoft Dynamics 365 või seostatud veebilehe ja märkida ülesanded kui pooleliolevad, tühistatud või lõpetatud.

## <a name="business-process-workspace"></a>Äriprotsessi tööruum
Personalispetsialistid saavad aktiivseid äriprotsesse vaadata tööruumis **Äriprotsess**. Selles tööruumis on loetletud kõik aktiivsed protsessid ja nendega seotud ülesanded. Ulatuslikku ülesandeloendit on võimalik tähtaja põhjal filtrida. Tööruumis on loetletud ka tähtajast üle läinud ülesanded ja ülesanded, mis on just konkreetselt personalispetsialistile määratud. Personalispetsialist saab ka kõigi ülesannete olekuid värskendada ja vajaduse korral ülesandeid uuesti määrata, et üldine äriprotsess liiguks edasi.

## <a name="my-business-processes-workspace"></a>Minu äriprotsesside tööruum
Protsessi omanikud saavad endale määratud aktiivseid äriprotsesse vaadata tööruumis **Minu äriprotsess**. Selles tööruumis on loetletud kõik kasutaja aktiivsed protsessid ja nendega seotud ülesanded. Ulatuslikku ülesandeloendit on võimalik tähtaja põhjal filtrida. Tööruumis on loetletud ka ülesanded, mis on just konkreetselt protsessi omanikule määratud. Protsessi omanik saab ka kõigi ülesannete olekut värskendada ja ülesandeid uuesti määrata.

## <a name="navigating-business-processes"></a>Äriprotsesside navigeerimine
Äriprotsessi malli loomiseks või kopeerimiseks või äriprotsessi käivitamiseks avage Äriprotsessid – lingid – Äriprotsesside haldamine. Seejärel saate teha järgmisi toiminguid:

- Valige **Uus**, et luua uus äriprotsessi mall.
- Valige **Kopeeri mallist**, et kopeerida valitud mall uude malli.
- Valige **Käivita protsess**, et käivitada valitud äriprotsess, määrata ülesandeid ja arvutada tähtaegu.

Aktiivsete protsesside ja seotud ülesannete vaatamiseks avage tööruum **Äriprotsessid**.

