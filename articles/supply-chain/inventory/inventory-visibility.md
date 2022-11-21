---
title: Inventory Visibility lisandmooduli ülevaade
description: See artikkel kirjeldab varude nähtavust ja selle funktsioone.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd790bcaada0c1a05e46b4edacaa31fc4e15be92
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762803"
---
# <a name="inventory-visibility-add-in-overview"></a>Inventory Visibility lisandmooduli ülevaade

[!include [banner](../includes/banner.md)]

Varude nähtavuse lisa (*mida* nimetatakse ka varude nähtavuse teenuseks) pakub iseseisvat ja väga skaleeritavat mikroteenust, mis võimaldab reaalajas vaba kaubavaru muudatuste sisestusi ja nähtavuse jälgimist läbi kõigi andmeallikate ja kanalite. See pakub platvormi, mis võimaldab teil hallata oma globaalset kaubavaru, kasutades funktsioone, mis sisaldavad (kuid ei ole piiratud) järgmist loendit:

- Jälgige kõigi andmeallikate, ladude ja asukohtade viimast varude olekut (nt laoseis, tellitud, ostetud, transiidis, tagastatud ja vahelattu) läbi kõigi andmeallikate, ladude ja asukohtade, ühendades oma hankeahela halduse või kolmanda osapoole logistika andmeallikad (nt tellimuse haldussüsteemid, \[kolmanda osapoole ettevõtte ressursside plaanimise ERP-süsteem\], \[\] müügi kassasüsteem ja laohaldussüsteem) varude nähtavuse teenusega.
- Tehke päring vaba laovaru saadavuse ja puudujäägi kohta ning hankige kohesed vastused, kutsudes otse lao nähtavuse teenuse.
- Vältige ülemüüdamist, eriti siis, kui teie nõudlus pärineb erinevatest kanalitest, tehes reaalaja soft reserveerimised varude nähtavuse teenuses.
- Parem hallake lubatud tellimusi ja kliendi ootusi, pakkudes täpseid praeguseid või järgmiseid saadaolevaid kuupäevi, nii et lubaduse andmiseks saadaolev (ATP) funktsioon saab arvutada eeldatava tellimuse täitmiskuupäevi.

## <a name="extensibility"></a>Laiendatavus

Varude nähtavuse teenus on väga laiendatav, kuna andmete sisestus ja väljund pole piiratud Microsofti rakendustega. Välissüsteemidel on juurdepääs teenusele RESTful-rakenduse programmeerimisliideste (API-d) kaudu. Lisaks boksist väljas vastendustele, mida antakse tarneahela halduse andmeallikale ja dimensioonidele, saate integreerida varude nähtavuse mitme kolmanda osapoole süsteemiga, seadistades täiendavad andmeallikad, varude oleku mõõdud (*mida* nimetatakse füüsilisteks mõõtudeks varude nähtavuse teenuses) ja varude dimensioone konfiguratsioonirakenduse kaudu. Sel viisil saate teha päringuid ja muuta mitmeid andmeallikaid ning eelmääratletud varude dimensioone.

Peale selle saab varude nähtavuse loonud Microsoft Dataverse andmete põhjal luua ja integreerida neid andmetega Power Apps. Samuti saate luua kohandatud Power BI armatuurlaudu, mis vastavad teie äritegevuse vajadustele.

## <a name="scalability"></a>Mastaapsuse

Varude nähtavuse teenust saab sõltuvalt andmemahust kas üles või alla astaabida. Skaleeritavus on enamasti tõrgeteta ja Microsofti platvormi meeskond viib seda läbi kannete andmemahtu automaatse tuvastamise ja hindamise alusel.

Järgmine näide näitab varude nähtavuse ülesehitust.

[<img src="media/inventory-visibility-architecture.png" alt="Inventory Visibility architecture." title=" Varude nähtavuse ülesehitus" width="720" />](media/inventory-visibility-architecture.png)

## <a name="feature-highlights"></a>Esiletõstetud funktsioonid

### <a name="get-a-global-view-of-real-time-inventory"></a>Reaalajas lao globaalvaate saamine

Lao nähtavus tagab selle, et teil on juurdepääs ajakohastele laokogustele kogu aeg, läbi kõigi kanalite, asukohtade ja ladude. Seda kasutatakse kõige rohkem igapäevaste tööteenuste toetamiseks alati, kui peate varude kirjeid saama. Füüsiline vaba kaubavaru, müüdud kogused ja ostetud kogused on kõik boksist saadaval. Samuti saate konfigureerida teisi füüsilise laovaru dimensioone (nt tagastatud, vahelattu ja sisestatud andmed), nagu vajate, et saada need üksikasjad reaalajas. Lao nähtavus saab tõhusalt töödelda miljonites lao muutmise sisestamist. Neid andmeid saab koondada ja kajastada teenuse viimastes laokogusdes kohe, sekundi või minuti kohta, sõltuvalt andmete sisestamisintervallist. Lisateavet vt varude nähtavuse avalikud [API-d](inventory-visibility-api.md).

### <a name="central-inventory-adjustment"></a>Keskkaubavaru korrigeerimine

Varude nähtavus võimaldab välissüsteemidel helistada varude muudatuste sisestamiseks oma API-le. Muudatused jõustuvad varude nähtavuses kohe. Seetõttu arvatakse vaba kaubavaru kohe maha.

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Soft reservation, et vältida ülemüümist kõigis tellimuskanalites

*Spetsiifiline reserveerimine* võimaldab teil määrata või lipuga märgistada kindlad kogused tellimuse või nõudluse täitmiseks. Kerge reserveerimine ei mõjuta füüsilisi laovarusid, *kuid* see arvatakse varude reserveerimiseks saadaolevast kogusest maha ja esitab tulevase tellimuse täitmise jaoks uuendatud koguse. See funktsioon on kasulik, kui müügitaotlused või -tellimused tulevad teie ettevõttesse ühest või enamast kanalist või andmeallikast, mis on väljaspool teie ettevõtte ressursiplaanimise (ERP) süsteemi.

Kui te ei kasuta varude nähtavuse teenuses kergeid reserveeringuid, peate füüsilise laokoguse uuendamiseks ootama, kuni tellimus on sünkroonitud ja seda töötleb. Sellel protsessil on tavaliselt väga suur latentsus. Kuid pehmed reserveerimised jõustuvad müügitaotluse või -tellimuse loomisel müügikanalites iga kord kohe. Seega aitavad need ennetada olukorda, kindlustades, et teie kaubatellimused ei vaja üksteisega, kui nad lõpuks ERP süsteemi jõuab. Softreserveeringud tagavad ka selle, et saate täita kõik lubatud tellimused. Seetõttu aitavad need teil vastata kliendi ootustele ja säilitada kliendi lojaalsust. Lisateavet vt teemast [Varude nähtavuse reserveeringud](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-quantity-and-dates"></a>ATP koguse ja kuupäevade kohene vastus

Nähtavus on teie lähedalasuva kaubavaru (sh pakkumine, nõudlus ja laovaru prognoositud üksikasjad) nähtavus on oluline, sest see aitab teie ettevõttel saavutada järgmised eesmärgid:

- Minimeerige kaubavarude tasemed laohalduse kulude vähendamiseks.
- Hõlbustage tellimuse sisemist töötlemist, et müügiisikud saaksid tellitud toodete saadavusel põhinevalt arvutada saatmis- ja tarnekuupäevi.
- Pakuge kust kliendid võivad eeldada, et laost väljas kaup muutub kättesaadavaks, pakkudes järgmist saadaolevat kuupäeva.

ATP funktsiooni on lihtne oma igapäevase tellimuse täitmisprotsessi vastu võtta. Kõige olulisem - nagu teised varude nähtavuse pakkumistel - on ATP funktsioon globaalne *ja reaalajas*. Seetõttu saate seadistada mitmeid ATP arvutusvalemeid, et saada täielikke varude saadavuspäringuid, mis katavad kõik teie ärikanalid ja andmeallikad. Lisateavet vt varude nähtavuse [vaba kaubavaru muutmise graafikutest ja lubaduse andmiseks saadaval](inventory-visibility-available-to-promise.md).

### <a name="preallocate-your-stock-to-important-channels-or-customers-with-inventory-allocation"></a>Lao eelalloiseeritud olulistesse kanalitesse või klientidesse varude eraldamisega

Varude nähtavuse eraldamise funktsioon võimaldab kaitsta ja koguda oma väärtust vaba kaubavaru oluliste kanalite, kliendigruppide või asukohtade jaoks. Pärast lao eraldamist on varude tarbimine piiratud eraldatud parki ja kogused, mis on salvestatud parki, arvatakse maha reaalajas, et kajastada veel tarbimiseks saadaolevat kogust. Lisateavet vt varude nähtavuse [varude eraldamisest](inventory-visibility-allocation.md).

### <a name="compatibility-with-wms-items"></a>Ühildumine WMS-kaupadega

Microsofti abil saab tagada boksist väljas integratsiooni laohaldusprotsessidega (WMS), et WMS-kliendid saaksid ka ära kasutada varude nähtavuse teenuse soodustusi. 2022 Voo 1 väljalaske kohta (avalik eelvaade märtsis) toetab laoteenus WMS-i kauba vaba kaubavaru päringuid ja ATP-d. Järgmises voos toetatakse WMS-klientide puhul kerget reserveerimise ja eraldamise funktsiooni. Lisateavet vt WMS-kaupade [varude nähtavuse tugi](inventory-visibility-whs-support.md).

Järgmine näide näitab olemasolevate funktsioonide kõrgema taseme kokkuvõtet ja seda, kuidas neid saab andmevoos asetada.

[<img src="media/inventory-visibility-feature-overview.png" alt="Inventory Visibility feature overview." title=" Varude nähtavuse funktsiooni ülevaade" width="720" />](media/inventory-visibility-feature-overview.png)

## <a name="licensing"></a>Litsentsimine

Varude nähtavuse teenus on saadaval järgmistes versioonides.

- **Varude nähtavuse lisandmoodul Microsoftile Dynamics 365 Supply Chain Management** – kehtiva tarneahela halduslitsentsiga ettevõtetele on varude nähtavus saadaval lisatasuta. Kuna varude nähtavus põhineb, sõltub Microsoft Power Platform see ladustamisvõimsusest ja Microsoft Power Platform API-piirangutest. Teie tarneahela haldamise litsents peaks sisaldama ladustamise ja API vaikevõimsust. Kui vajate rohkem talletus- ja API-võimsust, saate osta professionaalse litsentsi. Üksikasju API vaikeeralduse ja kutselitsentsi kohta vt taotluse [limiitide ja eraldamiste ning](/power-platform/admin/api-request-limits-allocations) litsentsimise [ülevaatest Microsoft Power Platform](/power-platform/admin/pricing-billing-skus). Laoala ja API vaikeeralduste puhul saate alustada varude nähtavuse lisandmooduli proovimist täna. Installi üksikasjad leiate jaotisest Varude [nähtavuse installimine ja seadistamine](inventory-visibility-setup.md). Kui teie hinnanguline API ja salvestuskasutus ületavad standarderalduse, võite võtta ühendust oma müügiesindajaga ja paluda neil erandiks võtta ühendust platvormi töörühmaga.
- **Varude nähtavuse teenus IOM-i** komponendina – see versioon on kas nutika tellimusehalduse (IOM) klientidele või ettevõtetele, kes ei kasuta tarneahela haldust oma ERP-süsteemina. Litsents kaasatakse nutika tellimusehalduse kogumisse. Lisateavet vt nutika tellimusehalduse [ülevaatest](/dynamics365/intelligent-order-management/overview).

## <a name="inventory-visibility-terminology"></a>Varude nähtavuse terminoloogia

Varude nähtavuse lisandmooduliga töötamisel on oluline mõista järgmisi mõisteid ja tingimusi:

- **Andmeallikas** – andmeallikas esindab süsteemi, millelt teie andmed pärit on.
- **Dimensioonid** – dimensioonid määravad toote omadused. Need võivad olla ladustamisdimensioonid (nt laoala või ladu) või tootedimensioonid (nt värv, suurus või stiil).
- **Füüsilised** mõõtmised – füüsilised mõõtmised on kogused, millega mõõdetakse erinevaid varude olekuid, nt vaba kaubavaru, ostetud, tellimusel või müüdud.
- **Arvutatud määrad** – arvutatud määrad on kvantitatiivsed meetmed, mis arvutatakse füüsiliste measuresmete komplektist. Näiteks arvutatakse kogu *saadav* arvutatud mõõt väärtuseks *Ostetud vaba kaubavaru* + *·* – *tellimusel* – *müüdud*.
- **Sektsioon** – sektsioon määrab hierarhia, kuidas lao nähtavus vastuvõetud andmeid jaotab. Praegu on vaikesektsiooniks sait ja asukoht.
- **Indekshierarhia** – indeksihierarhia määratleb veelgi enam, kuidas soovite varude kohta päringut teha ja saada tulemusi, mis on granulaarsusega.

Lisateavet nende tingimuste ja mõistete kohta vt Lao nähtavuse [konfigureerimine](inventory-visibility-configuration.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
