---
title: Dynamics 365 Human Resources infrastruktuuri ühendamise ülevaade
description: See artikkel kirjeldab Microsofti infrastruktuuri Dynamics 365 Human Resources ühendamist.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f79ef3ed5db7583eb44b99e49c010778ce8524d1
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732762"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources infrastruktuuri ühendamine 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamicsi inimressursid 365

Microsoft Dynamics 365 Human Resources pakub tööriistu, mis aitavad inimressursside töörühmadel organisatsioonilist alandust suurendada, töötajakogemust muuta ja optimeerida inimressursside programme, et luua töökoha, kus inimesed ja ettevõte saavad areneda. Lisateavet vt Dynamics 365 Human Resources teemast [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Saate töötajakogemust muuta.** Säilitage tipptöötajad, volitades juhatajaid ja töötajaid ühendatud iseteeninduskogemuste kaudu, mis juhtida kaasamist ja kasvu.
- **Optimeerige inimressursside programme.** Aidata vähendada tegevuskulusid ja luua töötajate ajalisi puhkusi ja puudumisi, aega, soodustusi ja kompensatsiooni halduskavasid.
- **Organisatsioonilise alandsuse suurendamine.** Lubage inimressurssidel töötada arukusega, mida ettevõte vajab inimeste andmete Dataverse Microsoft Power Platform abil ja tsentraliseerituks ning laiendada hõlpsasti Dynamics 365 Human Resources.
- **Saate avastada tööjõuülevaated.** Saate andmepõhiste otsuste langetada läbi võime analüüsida ja visualiseerida mis tahes seadmes salvestatud rikaste armatuurlaudade andmeid.

## <a name="human-resources-infrastructure-merge"></a>Inimressursside infrastruktuuri ühendamine

Dynamics 365 Human Resources on eraldi rakendus, mis kasutab praegu erinevat infrastruktuuri kui teised finantside ja toimingute rakendused, nt Dynamics 365 Finance või Dynamics 365 Supply Chain Management. Infrastruktuuri ühendamine toob kaasa Dynamics 365 Human Resources samasse infrastruktuuri kui teised finantside ja toimingute rakendused.

Lisateavet Inimressursside infrastruktuuri ühendamise kohta vt inimressursside [pakkumiste ühendamine](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Vastuseid korduma kippuvatele küsimustele vt Inimressursside [infrastruktuuri ühendamise KKK-st](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Kliendi migreerimine vs kliendi ühendamine

Osana infrastruktuuri ühendamisest on kõik Inimressursside rakenduse võimalused tehtud kättesaadavaks finants- ja toimingute keskkondades. Kliendid saavad oma inimressursside keskkondi üle kanda elutsükli teenustes saadaoleva siirdetööriista Microsoft Dynamics abil. Soovi korral saavad nad oma andmeid ühendada olemasoleva finants- ja operatsioonikeskkonnaga. 

Kliendi migreerimine ja klientide ühendamine on üksteisest erinev:

- **Kliendi** migratsioon – automatiseeritud migreerimise tööriista kasutatakse kliendi andmebaasi "tõstmise ja vahetuse migreerimise" (liikumise) sooritamiseks Inimressursside infrastruktuurist finantside ja toimingute infrastruktuuri. Tulemuseks on uus finants- ja toimingute keskkond, mis kasutab kliendi Inimressursside andmebaasi. 
- **Kliendi ühendamine** – See lisasamm pole Microsoft nõutav. Seda tehakse kliendi valikul ja kliendi oma ajaskaalal. Selle sammu jooksul teisaldatakse kliendi andmed olemasolevasse keskkonda, nt finants- või projektioperatsioonide keskkonda. Enamasti käsitsi ja seda saab teha andmehalduse raamistiku (DMF) andmeüksuste abil. 

## <a name="planning-a-human-resources-environment-migration"></a>Inimressursside keskkonna migreerimise plaanimine

Osana infrastruktuuri ühendamisest nõutakse kõikidelt klientidelt olemasolevate inimressursside keskkonna migreerimist eraldi infrastruktuurist. Protsessi aitamiseks soovitame kasutada automatiseeritud migreerimistööriista elutsükli teenustes, et teisaldada oma praegused keskkonnad uude infrastruktuuri. 

Järgmised jaotised annavad üksikasjalikumat teavet selle kohta, kuidas kasutada elutsükli teenuste tööriistu eraldi inimressursside keskkonna migreerimiseks. 

Migreerimist planeerivad kliendid võivad saada järgmised ootused:

- Enne tootmiskeskkonna ülekandmist on kõigilt klientidelt nõutavboxi keskkonna migreerimine. 
- Migreerimise tööriista abil saab kasutada ainultbox-to-boxi ja tootmise tootmisse siirdamist. Seetõttu määrab teie keskkonna tüüp, millist keskkonda saab sobivalt siirata. 
- Kliendid saavad migreerida nii palju kaustasid, kui vaja, enne kui nad oma tootmiskeskkonda üle kannavad, eeldusel, et sihtkausta pesa on saadaval. Kliendid saavad kustutada migreeritud kausta ja teha seda mitu korda uuesti. 
- Kui siirde töö nurjub või kui soovite uuesti alustada, saate kustutada finantside ja toimingute infrastruktuuri keskkonna ja migratsiooni samast keskkonnast.
- Inimressursside keskkonna URL on pärast migreerimist erinevad.
- Planeerige tootmiskeskkonna siirdamiseks sobiv hulk töötunde. Hinnanguline automatiseeritud migreerimisprotsessi lõpetamise ajavahemik on kolm kuni neli tundi. Ajavahemik on organisatsiooni andmetest sõltuvalt erinev. Peate kinnitama aja hulga, mis on vajalik teie sisendkausta keskkondade siirdamiseks, ja lubama aega mis tahes täiendavatele käsitsi sooritatavale tööülesannetele, mis tuleb lõpule viia.

> [!IMPORTANT] 
> Kui tootmiskeskkond on edukalt finantside ja toimingute infrastruktuuri üle kandnud, kustutatakse allika eraldi tootmiskeskkond automaatselt. Ülekantud tootmiskeskkonda ei tohiks kustutada. 

Migreerimise protsess on enamasti automaatne. Kuid teie ärikasutajad peavad pärast migreerimist sooritama mõned käsitsi sammud ja kinnitamise.

Järgmised käsitsi sammud peavad olema lõpule viidud:

- Looge migreerimiseks uus elutsükli teenuste projekt.
- Vaadake kõik oma vanas keskkonnas olevad integratsioonid üle uude keskkonda, suunates integratsiooni uuele URL-ile/lõpp-punktile, põhinedes igal integratsiooni konfiguratsioonil.
- Värskendage manustatud aruannete andmesalve Power BI.
- Värskendage andmeüksuse loendit DMF-tööruumist.
- Linkige spikri jaoks elutsükli teenustega.
- Saate luua rahanduskalendrid.

Automaatse protsessi ajal viiakse lõpule järgmised tegevused ja need tuleb kinnitada:

- Andmete:

    - Konfiguratsioonid
    - Turberollid (sh kohandatud rollid)
    - Töövood
    - Isikupärastamised ja salvestatud vaated
    - Kanded
    - Kohandatud väljad
    - Manused

- Andmehaldus – tooge oma andmebaas (BYOD).
- Funktsioonihaldus – lubatud/keelatud funktsioonid.
- Manustatud Power Apps.
- Power Platform halduskeskusega seotud keskkond (ainult tootmine).
- Pakett-tööd.
- Igale juriidilisele isikule luuakse tühi pearaamat. Seadistatakse vahetuskursi vaiketüüp ja iga pearaamatu arvestusvaluuta.
- Iga juriidilise isiku pearaamatulehe jaoks luuakse ja **lingitakse** automaatselt uus kontoplaan. Teie Inimressursside keskkonnas konfigureeritud finantsdimensioonid lisatakse automaatselt uude konto struktuuri ja seotakse pearaamatuga. 

> [!NOTE]
> Pearaamat on vajalik finantside ja toimingute infrastruktuuris Dynamics 365 finantstoote osana. Eraldi rakenduses olnud kohandatud dimensioonikontroller Dynamics 365 Human Resources ei ole saadaval. Inimressursside ühendatud infrastruktuur sõltub finantsloogikast, et näidata finantsdimensioone inimressursside **moodulis**. Kontoplaani ja finantsdimensioonide kohta leiate lisateavet [siit](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Kaalutlused

- Siirded keskkondadele on alati uusim üldiselt saadaval (GA) versioon. Sõltuvalt migreerimis- ja testimisplaanist, kui teie siirde kinnitamine sisendkausta keskkondades oli teises versioonis, on soovitatav kontrollida sisendkausta migreerimist tootmiskeskkonnaga samas versioonis. 
- Migreerimise ajal paigutatakse ülekantud keskkonnad samasse piirkonda kui allikas eraldiseisev Inimressursid keskkonnad.

## <a name="licensing"></a>Litsentsimine

Litsentsimises ei ole järgmistes Dynamics 365 Human Resources valdkondades muudatusi: 

- **Minimaalne litsentsi ostunõue**
- **Tootmise litsentsid** ja sisendkausta keskkond – kui teil on olemas autonoomsed inimressursside litsentsid, mis annab abi ühele tootmiskeskkonnale ja ühele kaustakeskkonnale, on finantside ja toimingute infrastruktuuris saadaval sama litsentside arv lisakuluta.
- **Lisainfolitsentsid** – kui olete ostnud autonoomse inimressursid rakenduse jaoks täiendavaid ruutlitsentsisid, on standardne kinnitamiskatse (box) keskkonnas finantside ja toimingute infrastruktuuris saadaval sama arv sisendkausta litsentse lisakuluta. 
