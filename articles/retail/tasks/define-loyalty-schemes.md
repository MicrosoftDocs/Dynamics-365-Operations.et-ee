--- 
title: " Püsikliendiskeemide määratlemine"
description: "See protseduur selgitab, kuidas määratleda boonusskeemi."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f398197566918c571128433c2fba3bf7d7c2fe3d
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="define-loyalty-schemes"></a> Püsikliendiskeemide määratlemine

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

See protseduur selgitab, kuidas määratleda boonusskeemi. Boonusskeemid on püsikliendiprogrammis preemiapunktide teenimise ja lunastamise reeglid. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage Jaemüük ja kaubandus > Kliendid > Püsiklient > Boonusskeemid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Skeemi ID.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
    * Püsikliendiprogrammi jaoks võib olla mitu boonusskeemi. Boonusskeemid võivad kehtida kõigi kanalite või ainult kanalite alamkogumi kohta.  
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake nuppu Salvesta.
9. Klõpsake käsku Lisa rida.
10. Valige suvand väljalt Tegevuse tüüp.
    * Valige suvand Toodete ostmine summa järgi, kui soovite, et kliendid teeniksid preemiapunkte selle põhjal, kui palju nad kulutavad. Valige suvand Toodete ostmine koguse järgi, kui soovite, et kliendid teeniksid preemiapunkte selle põhjal, kui palju tooteid nad ostavad.  Valige suvand Müügikannete loendus kui soovite, et kliendid teeniksid preemiapunkte iga müügikande eest, olenemata ostetud toodetest või kogusest.  
    * Valige kategooria. Kategooria piirab, millistele toodetele see teenimisreegel rakendub.  
    * Kui soovite rakendada teenimisreegli kõigile toodetele, jätke see väli tühjaks.  
11. Sisestage number väljale Tegevuse summa/kogus.
    *  Tegevusetüübi Müügikannete loendus puhul peaksite kasutama alati väärtust 1,0. Tegevusetüüpide Ostmine summa järgi või Ostmine koguse järgi puhul ei käivitata teenimisreeglit, kui kanne on väiksem kui sisestatud väärtus. Näiteks kui tegevusetüüp on Ostmine summa järgi ja sisestate väärtuse 10,00, ei teeni müügikanne väärtuses 9,00 selle teenimisreegli järgi preemiapunkte.  
12. Sisestage väärtus väljale Tegevuse valuuta.
13. Klõpsake väljal Preemiapunkti ID otsingu avamiseks ripploendi nuppu.
14. Klõpsake loendis valitud real olevat linki.
15. Sisestage number väljale Preemiapunktid.
    * Summatüüpi preemiapunktid salvestavad teenitud summad kümnendkohaga. Näiteks kui teenimisreegel määrab iga teenitud Kanada dollari kohta ühe preemiapunkti ja klient kulutab 1,25 Kanada dollarit, teenib klient 1,25 preemiapunkti. Kogusetüüpi preemiapunktid salvestavad teenitud summad täisarvudena. Näiteks kui teenimisreegel määrab iga teenitud Kanada dollari kohta ühe preemiapunkti ja klient kulutab 1,25 Kanada dollarit, teenib klient 1,0 preemiapunkti.  
16. Klõpsake nuppu Salvesta.
17. Klõpsake käsku Lisa rida.
    * Lunastamisreegleid kasutatakse püsikliendi makseviisi kasutamise korral.  
18. Klõpsake väljal Preemiapunkti ID otsingu avamiseks ripploendi nuppu.
    * Kuvatakse ainult lunastatavad preemiapunktid.  
19. Klõpsake loendis valitud real olevat linki.
20. Sisestage number väljale Preemiapunktid.
21. Valige suvand väljal Lunastuse tüüp.
    * Suvandi Makse summa järgi valimisel käsitletakse välja Summa või kogus valuutaväärtusena. Sellisel juhul on makse valuutaühiku kohta kasutatav preemiapunktide summa fikseeritud määr. Suvandi Makse koguse järgi valimisel käsitletakse välja Summa või kogus koguseväärtusena. Sellisel juhul on kauba koguse kohta kasutatav preemiapunktide summa fikseeritud määr, kuid summa valuutas võib erineda, kui kaupade eest preemiapunktidega tasutud hind sama koguse lõikes varieerub. Püsikliendi allahindluse tüüp Lunastamine kehtib ainult siis, kui lubatud on riigi-/piirkonnapõhine konfiguratsioonivõti Venemaa ja kassa funktsiooniprofiilide ISO-koodi sätteks on valitud RU.  
    * Valige kategooria. Kategooria piirab, millistele toodetele see lunastamisreegel rakendub.  
    * Kui soovite rakendada lunastamisreegli kõigile toodetele, jätke see väli tühjaks.  
22. Sisestage number väljale Summa või kogus.
23. Sisestage väärtus väljale Valuuta.
24. Klõpsake nuppu Salvesta.
25. Klõpsake käsku Lisa rida.
    * Valige üks või mitu sõlme loendist Saadaolevad organisatsioonisõlmed ja teisaldage need loendisse Valitud organisatsioonisõlmed, klõpsates loendite vahel olevat noolt.  
26. Klõpsake nuppu OK.
27. Klõpsake nuppu Salvesta.
    * Boonusskeemi kanalite muutmisel peate käivitama boonusskeemide töötlemise. Nii värskendavad boonusskeemid kanaleid.  


