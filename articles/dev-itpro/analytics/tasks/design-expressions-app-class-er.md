--- 
title: Elektroonilise aruandluse avaldiste kujundamine, millega kutsuda rakendusklasside meetodeid
description: Juhendis kirjeldatakse, kuidas taaskasutada olemasolevat rakendusloogikat elektroonilise aruandluse (ER) konfiguratsioonides, kutsudes ER-i rakendusklasside vajalikke meetodeid.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Elektroonilise aruandluse avaldiste kujundamine, millega kutsuda rakendusklasside meetodeid

[!include [task guide banner](../../includes/task-guide-banner.md)]

Juhendis kirjeldatakse, kuidas taaskasutada olemasolevat rakendusloogikat elektroonilise aruandluse (ER) konfiguratsioonides, kutsudes ER-i rakendusklasside vajalikke meetodeid. Kutsumisklasside argumentide väärtusi saab käitusajal dünaamiliselt määratleda: näiteks sõelumisdokumendis oleva teabe alusel, et tagada selle õigsus. Selle juhise järgi koostate näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. 

Need etapid saab lõpule viia ükskõik millise andmekomplekti abil. Peate ka järgmise faili alla laadima ja kohalikult salvestama: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Etappide lõpuleviimiseks peate esmalt läbima protseduuri „Pakkuja elektroonilise aruandluse konfiguratsiooni loomine ning aktiivseks märkimine” etapid.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” esitatud juhised.   
    * Oletame, et koostate sissetulevate pangaväljavõtete sõelumise protsessi avalduse andmete värskendamiseks. Sissetulevad pangaväljavõtted saadetakse teile TXT-failidena, mis sisaldavad IBAN-koode. Pangaväljavõtte importimise osana peate selle IBAN-koodide õigsust kontrollima loogikaga, mis on juba saadaval rakenduses Dynamics 365 for Finance and Operations.   

## <a name="import-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni importimine
1. Otsige loendist ja valige soovitud kirje.
    * Valige Microsofti pakkuja paan.  
2. Klõpsake valikut Hoidlad.
3. Klõpsake suvandit Näita filtreid.
4. Lisage filtriväli „Tüübi nimi”. Väljale Nimi sisestage väärtus „ressursid”, valige filtri tehtemärk „sisaldab” ja klõpsake käsku Rakenda.
5. Klõpsake valikut Ava.
6. Valige puul väärtus Maksemudel.
    * Kui nupp Impordi kiirkaardil Versioonid ei ole lubatud, olete ER-i konfiguratsiooni „Maksemudel” 1. versiooni juba importinud. Võite alamülesande ülejäänud etapid vahele jätta.   
7. Klõpsake Import.
8. Klõpsake nuppu Jah.
9. Sulgege leht.
10. Sulgege leht.

## <a name="add-a-new-er-format-configuration"></a>Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine
1. Klõpsake valikut Aruandluse konfiguratsioonid.
    * Lisage uus ER-i vorming, et sõeluda TXT-vormingus sissetulevaid pangaväljavõtteid.  
2. Valige puul väärtus Maksemudel.
3. Klõpsake valikut Loo konfiguratsioon, et avada dialoogimenüü.
4. Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.
5. Väljale Nimi tippige „Panga väljavõtte impordivorming (näidis)”.
    * Pangaväljavõtte impordivorming (näide)  
6. Väljal Toetab andmeimporti valige Jah.
7. Klõpsake Loo konfiguratsioon.

## <a name="design-the-er-format-configuration---format"></a>Elektroonilise aruandluse vormingu konfiguratsiooni kujundamine – vorming
1. Klõpsake valikut Kujundaja.
    * Kujundatud vorming tähistab TXT-vormingus välise faili eeldatavat struktuuri.  
2. Klõpsake dialoogimenüü avamiseks suvandit Lisa juur.
3. Valige puult Tekst \ Seeria.
4. Tippige Juur väljale Nimi.
    * Juur  
5. Valige väljal Erimärgid Uus rida – Windows (CR LF).
    * Suvand „Uus rida – Windows (CR LF)” on väljal „Erimärgid” valitud. Selle sätte alusel arvestatakse sõelumisfaili iga rida eraldi kirjena.  
6. Klõpsake nuppu OK.
7. Klõpsake valikut Lisa rippdialoogi avamiseks.
8. Valige puult Tekst \ Seeria.
9. Väljale Nimi tippige „Read”.
    * Read  
10. Valige kordsuse väljal „One many”.
    * Väljal „Mitmekordsus” on valitud suvand „Üks, mitu”. Selle sätte alusel eeldatakse, et sõelumisfailis esitatakse vähemalt üks rida.  
11. Klõpsake nuppu OK.
12. Valige puul väärtus „Juur\Read”.
13. Klõpsake käsku Lisa seeria.
14. Väljale Nimi tippige „Väljad”.
    * Väljad  
15. Valige kordsuse väljal „Exactly one”.
16. Klõpsake nuppu OK.
17. Puul valige „Juur\Read\Väljad”.
18. Klõpsake valikut Lisa rippdialoogi avamiseks.
19. Valige puul suvand Tekst\String.
20. Sisestage väljale Nimi suvand IBAN.
    * IBAN  
21. Klõpsake nuppu OK.
    * See on konfigureeritud nii, et sõelumisfaili iga rida sisaldab ainult IBAN-koodi.  
22. Klõpsake nuppu Salvesta.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>ER-i vormingu konfiguratsiooni loomine – andmemudeliga vastendamine
1. Klõpsake nuppu Vormingu vastendamine mudeliga.
2. Klõpsake valikut Uus.
3. Väljale Definitsioon tippige „BankToCustomerDebitCreditNotificationInitiation”.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges definitsiooni.
5. Sisestage nimeväljale valik „Vastendamine andmemudeliga”.
    * Andmemudeliga vastendamine  
6. Klõpsake nuppu Salvesta.
7. Klõpsake valikut Kujundaja.
8. Valige puul suvand „Dynamics 365 for Operations\Klass“.
9. Klõpsake suvandit Juure lisamine.
    * Lisage uus andmeallikas, et kutsuda olemasolev rakendusloogika IBAN-koodide kontrollimiseks.  
10. Väljale Nimi tippige „check_codes”.
    * check_codes  
11. Väljale Klass tippige „ISO7064”.
    * ISO7064  
12. Klõpsake nuppu OK.
13. Laiendage puul valikut „format”.
14. Laiendage puul valikut „format\Root: Sequence(Root)”.
15. Valige puul „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)”.
16. Klõpsake valikut Seo.
17. Laiendage puul jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)”.
18. Laiendage puu jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)”.
19. Valige puul „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”.
20. Laiendage puul valikut „Payments = format.Root.Rows”.
21. Laiendage puus sõlme „Payments = format.Root.Rows\Creditor Account(CreditorAccount)”.
22. Laiendage puus sõlme „Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification”.
23. Valige puus „Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN”.
24. Klõpsake valikut Seo.
25. Klõpsake vahekaarti Kinnitused.
26. Klõpsake valikut Uus.
    * Lisage uus kinnitamisreegel, mis kuvab sõelumisfailis kehtetut IBAN-koodi sisaldava rea puhul tõrke.  
27. Klõpsake nuppu Muuda tingimust.
28. Laiendage puul suvandit „check_codes”.
29. Valige puul „check_codes\verifyMOD1271_36”.
30. Klõpsake suvandit Andmeallika lisamine.
31. Väljale Valem sisestage „check_codes.verifyMOD1271_36(”.
    * check_codes.verifyMOD1271_36(  
32. Laiendage puul valikut „format”.
33. Laiendage puul valikut „format\Root: Sequence(Root)”.
34. Laiendage puul jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)”.
35. Laiendage puu jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)”.
36. Valige puul „format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”.
37. Klõpsake suvandit Andmeallika lisamine.
38. Väljale Valem sisestage „check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)”.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Klõpsake nuppu Salvesta.
40. Sulgege leht.
    * Kontrollimise tingimus on konfigureeritud nii, et kehtetu IBAN-koodi puhul tagastatakse väärtus VÄÄR, kutsudes rakendusklassi „ISO7064” olemasoleva meetodi „verifyMOD1271_36”. Pange tähele, et IBAN-koodi väärtus määratletakse käitusajal dünaamiliselt kutsumismeetodi argumendina sõelutava TXT-faili sisu alusel.   
41. Klõpsake käsku Redigeeri teadet.
42. Väljale Valem sisestage „CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)”.
    * CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)  
43. Klõpsake nuppu Salvesta.
44. Sulgege leht.
45. Klõpsake nuppu Salvesta.
46. Sulgege leht.

## <a name="run-the-format-mapping"></a>Vormingu vastendamise käitamine
Testimiseks käivitage vorminduse vastendamine allalaaditud failiga SampleIncomingMessage.txt. Loodud väljund hõlmab andmeid, mis imporditakse valitud TXT-failist ja täidetakse reaalsel importimisel kohandatud andmemudeliga.   
1. Klõpsake nuppu Käivita.
    * Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini SampleIncomingMessage.txt.  
2. Klõpsake nuppu OK.
    * Vaadake väljund üle XML-vormingus, mis tähistab valitud failist imporditud ja andmemudelisse porditud andmeid. Pange tähele, et töödeldi imporditud TXT-faili ainult 3 rida. 4. real olev kehtetu IBAN-kood jäeti vahele ja teabelogisse lisatakse tõrketeade.  


