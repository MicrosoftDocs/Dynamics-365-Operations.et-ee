---
title: "Kulujuhtimise tööruum"
description: "Teema annab teavet kuluhalduse tööruumi kohta. See tööruum on keskne punkt, kus juhid, kes vastutavad kuluobjekti või kuluobjektide kogumi kontrollimise eest dimensioonis või dimensioonide lõikes, aruannetele juurde pääsevad."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7cc6ba50b8df54eadc9a23990a58d1d37365cb6a
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="cost-control-overview"></a>Kulujuhtimise ülevaade 

[!include[banner](../includes/banner.md)]

**Kulujuhtimise** tööruum on keskne punkt, kus juhid, kes vastutavad kuluobjekti või kuluobjektide kogumi kontrollimise eest dimensioonis või dimensioonide lõikes (nt kulukeskused ja tooterühmad), aruannetele juurde pääsevad. Tööruumis olevaid aruandeid haldavad täielikult kuluarvestajad, et aruandluseks kasutatav paigutus ja andmed oleksid terve organisatsiooni lõikes järjepidevad.

## <a name="cost-control-workspace-configuration"></a>Kulujuhtimise tööruumi konfiguratsioon

Kuluarvestajad võivad määratleda nii palju aruandekonfiguratsioone, kui on soovitud andmete koosseisu või paigutuse jaoks vaja. Aruande konfiguratsioon koosneb kuuest osast, millest igaüks mõjutab kas sihtandmete koosseisu valikut või paigutust.

Kulujuhtimise tööruumi konfigureerimiseks klõpsake valikuid **Kuluarvestus** \> **Seadistus** \> **Kulujuhtimise tööruumi konfigureerimine**.

### <a name="general"></a>Üldine

Kiirkaardil **Üldine** saate luua kordumatu aruandepaigutuse. Aruande nimi on ainuidentifikaator, mille kasutajad **kulujuhtimise** tööruumis ära tunnevad. Saate ka määrata, kas aruannet tuleks jagada või seda tuleks hoida kuluarvestajate sisekasutuseks.

| Väli       | Kirjeldus |
|-------------|-------------|
| Nimi        | Sisestage paigutusele kordumatu nimi. |
| Kirjeldus | Sisestage üksikasjalik kirjeldus. |
| Avaldatud   | Kui määrate sellel väljal väärtuse **Jah**, näeb kasutaja, kellele on määratud üks järgmistest rollidest, aruannet **kulujuhtimise** tööruumis.<ul><li>Kuluarvestuse haldur</li><li>Kuluarvestaja</li><li>Kuluarvestuse ametnik</li><li>Kuluobjekti kontroller</li></ul>Kui määrate sellel väljal väärtuse **Ei**, näevad ainult kasutajad, kellele on määratud üks järgmistest rollidest, aruannet **kulujuhtimise** tööruumis.<ul><li>Kuluarvestuse haldur</li><li>Kuluarvestaja</li><li>Kuluarvestuse ametnik</li></ul> |

### <a name="data-filtering"></a>Andmete filtreerimine

Kiirkaardil **Andmete filtreerimine** saate määratleda aruande alusandmed. Selle aruande kasutajad näevad aruandel olevaid väärtusi pärast lähteandmete töötlemist.

| Väli                                                             | Kirjeldus |
|-------------------------------------------------------------------|-------------|
| Kuluarvestuse pearaamat                                            | **Kuluarvestuse pearaamat**, millel aruanne põhineb. Väärtus tuletatakse väljalt **Kulu juhtimisüksus**. |
| Kulu juhtseade                                                 | Väärtus, mille valite, määrab kuluarvestuse pearaamatu ja kuluobjektid, millel see aruanne põhineb. |
| Statistiline dimensioonihierarhia, kuluelemendi dimensioonihierarhia | **Kulujuhtimise** tööruumi konfiguratsioonikirje saab registreerida mitterahalisi või rahalisi väärtusi, kuid mitte samas paigutuses. Valige väärtus väljalt **Kuluelemendi dimensioonihierarhia** rahaliste väärtuste registreerimiseks. Valige väärtus väljalt **Statistiline dimensioonihierarhia** mitterahaliste väärtuste registreerimiseks. Valitud dimensioonihierarhia kirje määrab aruandluse ja liitmise taseme struktuuri.<blockquote>[!NOTE]<br>Mitterahaliste ja rahaliste väärtuste kõrvuti vaatamiseks võite eksportida Microsoft Power BI sisupaketi andmed Microsoft Excelisse.</blockquote> |
| Kuluobjekti dimensioonihierarhia                                   | Valige määratletava aruandluse eesmärgiga sobiva kuluobjekti dimensiooni dimensioonihierarhia. |
| Eelarve algne versioon                                           | Valige eelarveversiooni ID, mis toimib selle aruande kontekstis algse eelarvena. |
| Eelarve parandatud versioon                                            | Valige eelarveversiooni ID, mis toimib selle aruande kontekstis parandatud eelarvena. |

### <a name="assign-calculation-records"></a>Kalkulatsioonikirjete määramine

Üldkulude arvutus läbib lähteandmetega mitu arvutusetappi, nt kulukäitumise klassifikatsioon, kulude jaotus ja kulude eraldamine. Sama rahandusperioodi kohta saab teha mitu üldkulude arvutust, juhul kui avastatakse puuduvaid lähteandmeid või kui reegleid tuleb muuta. Iga üldkulude arvutus salvestatakse kordumatu ID-ga. Kuluarvestaja saab valida konkreetse üldkulude arvutuse ID. Aruande kasutajad, nt juhid, näevad üldkulu arvutuse tulemusi **kulujuhtimise** tööruumis.

| Väli                  | Kirjeldus |
|------------------------|-------------|
| Rahanduskalendri periood | Valige rahanduskalendri periood, millele määrata üldkulude arvutuse ID.<blockquote>[!NOTE]<br>Sellel väljal loetletud rahandusperioodid pärinevad rahanduskalendrist, mis on seotud kuluarvestuse pearaamatuga.</blockquote> |
| Tegelik versioon         | Valige sobiv üldkulude arvutuse ID. |
| Eelarve versioon         | Valige sobiv üldkulude arvutuse ID. |
| Parandatud eelarve versioon | Valige sobiv üldkulude arvutuse ID. |

### <a name="fiscal-periods-per-column"></a>Rahandusperioode veeru kohta

Kiirkaardil **Rahandusperioodid veeru kohta** otsustab kuluarvestaja, millist rahandusperioodi peaks aruandepaigutuses kuvama.

Valitud veergudes olevaid väärtusi korrutatakse valitud väärtustega kiirkaardil **Rahandusperioode veeru kohta**.

| Väli                | Kirjeldus |
|----------------------|-------------|
| Praegune periood       | Kuvatakse jooksva rahandusaasta saldo.<blockquote>[!NOTE]<br>Vaikimisi määrab jooksva perioodi seansi kuupäev. **Kulujuhtimise** tööruumist saab valida konkreetse rahandusperioodi. Valitud väärtus kajastab siis jooksvat perioodi.</blockquote> |
| Eelmine periood      | Kuvatakse eelmise rahandusaasta saldo. Arvutamisel kasutatakse järgmist valemit:<br>Praegune rahandusperiood – 1<blockquote>[!NOTE]<br>Vaikimisi tuletatakse eelmine periood seansi kuupäevast. **Kulujuhtimise** tööruumist saab valida jooksvaks perioodiks konkreetse rahandusperioodi. **Eelmine periood** arvutatakse siis vastavalt ümber.</blockquote> |
| Aasta lõppkuupäevani         | Kuvatakse jooksev aasta. Arvutamisel kasutatakse järgmist valemit:<br>YearToDate (jooksev rahandusperiood)<blockquote>[!NOTE]<br>Vaikimisi määrab jooksva perioodi seansi kuupäev. **Kulujuhtimise** tööruumist saab valida konkreetse rahandusperioodi. Valitud väärtus kajastab siis jooksvat perioodi ja väärtust **Jooksev aasta** muudetakse vastavalt.</blockquote> |
| Jooksva aasta keskmine | Kuvatakse jooksva aasta keskmine. Arvutamisel kasutatakse järgmist valemit:<br>(YearToDate [praegune rahandusperiood]) ÷ (arv [praegune rahandusperiood])<p><strong>Näide</strong></p><ul><li>**Statistilise dimensiooni liige:** täiskohaga töötajad</li><li>**Praegune kuupäev:** 3-21-2017</li><li>**Periood:** rahandusperiood 1, rahandusperiood 2, rahandusperiood 3</li><li>**Väärtus:** 10, 10, 12</li></ul>Sel juhul **Jooksva aasta keskmine** = (10 + 10 + 12) ÷ 3 = 10,67<p>Väärtuse **Jooksva aasta keskmine** saab arvutada kuluelemendi dimensiooniliikmete ja statistiliste dimensiooniliikmete kohta.</p><blockquote>[!NOTE]<br>Vaikimisi määrab jooksva perioodi seansi kuupäev. **Kulujuhtimise** tööruumist saab valida konkreetse rahandusperioodi. Valitud väärtus kajastab siis jooksvat perioodi ja väärtusi **Jooksev aasta** ning **Jooksva aasta keskmine** muudetakse vastavalt.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Kulude jaoks kuvatavad veerud

Kiirkaardil **Kulude jaoks kuvatavad veerud** määrab kuluarvestaja, milliseid veerge aruande paigutus peaks sisaldama. Kategooriaid on kolm: fikseeritud kulu, muutuv kulu ja liigitamata kulu.

| Väli                 | Kirjeldus |
|-----------------------|-------------|
| Fikseeritud kulu            | Selles veerutüübis kuvatakse fikseeritud kulu valitud üldkulude arvutuse ID põhjal.<blockquote>[!NOTE]<br>Selles veerutüübis kuvatakse saldo ainult siis, kui rahandusperioodi jaoks on valitud üldkulude arvutamise ID.</blockquote> |
| Muutuv kulu         | Selles veerutüübis kuvatakse muutuv kulu valitud üldkulude arvutuse ID põhjal.<blockquote>[!NOTE]<br>Selles veerutüübis kuvatakse saldo ainult siis, kui rahandusperioodi jaoks on valitud üldkulude arvutamise ID.</blockquote> |
| Fikseeritud ja muutuv kulu | Selles veerutüübis kuvatakse fikseeritud kulu ja muutuv kulu valitud üldkulude arvutuse ID põhjal.<blockquote>[!NOTE]<br>Selles veerutüübis kuvatakse saldo ainult siis, kui rahandusperioodi jaoks on valitud üldkulude arvutamise ID.</blockquote> |
| Kogumaksumus            | Selles veerutüübis kuvatakse kogukulu (liigitamata kulu, fikseeritud kulu ja muutuv kulu).<blockquote>[!NOTE]<br>Selles veerutüübis kuvatakse alati saldo.</blockquote> |
| Liigitamata kulu     | Selles veerutüübis kuvatakse liigitamata kulu.<blockquote>[!NOTE]<br>Seda veergu saab kasutada kontrollimiseks, kas kõik kulud on üldkulude arvutuses õigesti liigitatud või tuleb kulukäitumise reegleid korrigeerida.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Eelarvestatud kulude jaoks kuvatavad veerud

Kiirkaardil **Eelarvestatud kulude jaoks kuvatavad veerud** määrab kuluarvestaja, millised veerud tuleks valitud eelarveversioonide puhul kuvada. Algse ja muudetud eelarve jaoks saab teha eraldi valikuid.

> [!NOTE]
> Kuna järgmised väljad käituvad algse ja muudetud eelarve puhul ühtemoodi, selgitatakse neid ainult üks kord.

| Väli                     | Kirjeldus |
|---------------------------|-------------|
| Eelarve                    | Eelarvesaldod kuvatakse valitud veergude kohta.<blockquote>[!NOTE]<br>Saldod põhinevad kiirkaardil **Andmete filtreerimine** valitud eelarveversioonidel.</blockquote> |
| Eelarve hälve           | Arvutage ja kuvage eelarve ning tegelike väärtuste vaheline erinevus. Arvutamisel kasutatakse järgmist valemit:<br>Eelarvesaldo – tegelik saldo |
| Eelarve hälbe %      | Arvutage ja kuvage eelarve ning tegelike väärtuste vaheline erinevus protsentides. Arvutamisel kasutatakse järgmist valemit:<br>(Eelarvesaldo – tegelik saldo) ÷ eelarvesaldo |
| Hälbe perioodi lävi | Määrake jooksva perioodi hälbe piirmäär rahasummana. Piirmäära ületamisel tõstetakse rida **kulujuhtimise** tööruumis punasega esile.<blockquote>[!NOTE]<br>See väli kehtib ainult kulusid kajastavatele kuluelementidele.</blockquote> |
| Hälbe aasta lävi   | Määrake aasta hälbe piirmäär rahasummana. Piirmäära ületamisel tõstetakse rida **kulujuhtimise** tööruumis punasega esile. |
| Hälbe läve %      | Määrake hälbe piirmäär protsentides. Piirmäära ületamisel tõstetakse rida **kulujuhtimise** tööruumis punasega esile.<blockquote>[!NOTE]<br>Sama piirmäära protsent rakendub jooksvale perioodile ning aastale.</blockquote> |

## <a name="cost-control-workspace"></a>Kulujuhtimise tööruum

**Kulujuhtimise** tööruum on loodud veebiaruandena. Seega saab kõigile juhtidele, kes kuluobjekti eest vastutavad, juurdepääsu anda, nagu on kirjeldatud jaotises [Kuluobjekti kontrollijate pääsuõiguste määratlemine](access-rights-cost-object-controller.md).

Kasutajatele (nt juhtidele) kättesaadavate aruannete loendit juhitakse sättega valikus **Avaldatud** lehel **Kulujuhtimise tööruumi konfiguratsioonid**.

![Aruanne, mida kasutajad kulujuhtimise tööruumis näevad](./media/report-cost-control.png)

Juht saab valida kuvamiseks rahanduskalendri perioodi. Jooksva perioodi vaikeväärtuse määramiseks kasutatakse seansi kuupäeva.

Rahanduskalendri perioodi väärtused määratakse aruande nime ja rahanduskalendriga, mis valitakse lehel **Kulujuhtimise tööruumi konfiguratsioonid** aruande nimega seostatud kuluarvestuse pearaamatule.

Kuluobjekti dimensioonihierarhias saavad kasutajad valida saldode kuvamise liitmistaseme. Lubades juurdepääsu turbetaseme, juhite õigusi, nii et kasutajad saavad valida ainult neid hierarhiatasemeid, millele neile on antud juurdepääs. Seega näevad nad ainult koondsaldosid, millele neile on antud juurdepääs.

### <a name="add-or-remove-columns"></a>Lisa või eemalda veerge

Kasutajad saavad kohandada oma vajadustele vastavalt aruande veerge.

### <a name="view-details"></a>Kuva üksikasjad

Kasutajad saavad minna süvitsi tööruumis kuvatavate saldode taga olevatesse andmetesse. Kui kasutajad valivad kuluelemendi dimensioonihierarhia sõlme ja klõpsavad siis valikut **Kuva üksikasjad**, kuvatakse dialoogiboksis **Kuluelemendi üksikasjad** sõlme üksikasjalikud andmed.

Ruudustikus kuvatakse kuluelemendi dimensioonihierarhia sõlme ja selle väärtustega seotud kuluelement. Ruudustikus kuvatavad veerud vastavad tööruumi sätetele.

Kaks diagrammi kuvavad kokkuvõtte tegelikest andmetest võrreldes eelarvega ja eelarve hälbe perioodide kaupa.

![Diagrammid, mis kuvavad kokkuvõtte tegelikest andmetest võrreldes eelarvega ja eelarve hälbe perioodide kaupa](./media/cost-element-details-operations.png)

Kasutajad võivad klõpsata valikut **Kulukirjed** kirje andmetes vajalikul viisil süvitsi minekuks.

![Kulukirjed](./media/cost-entries.png)

Näiteks rent on kulu, mis jagatakse kulukeskuste vahel. Kasutaja, kes soovib mõista oma kulukeskuse rendikulu, saab minna süvitsi, et näha, kuidas rent on arvutatud.

Kui kasutajad klõpsavad valikut **Eraldamisalus** lehel **Kulukirjed**, kuvatakse dialoogiboks. Kasutajad saavad siis määrata reeglile eraldamisaluse ja vaadata vastavaid perioodi kohta registreeritud statistilisi mõõte.

Järgmises näites on eraldamisaluse tüüp **Valemi eraldamisalus** ja on kuvatud valem. Loetletud on valemit määratlevad tegurid. Lisaks on ruudustikus näha kuluobjekti kohta tehtav arvutus.

![Arvutused kuluobjekti kohta](./media/cost-entries-allocation-base.png)

Vt ka 

[Kuluobjekti kontrollijate pääsuõiguste määratlemine](access-rights-cost-object-controller.md)



