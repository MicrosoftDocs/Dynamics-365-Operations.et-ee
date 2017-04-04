---
title: "Hallata allhanketööde tootmises"
description: "See teema selgitab, kuidas allhangete, juhitakse Microsoft Dynamics 365 toiminguteks. See tähendab, ta selgitab, kuidas tootmistegevusi, mis on eraldatud ressurss haldab hankija."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Hallata allhanketööde tootmises

See teema selgitab, kuidas allhangete, juhitakse Microsoft Dynamics 365 toiminguteks. See tähendab, ta selgitab, kuidas tootmistegevusi, mis on eraldatud ressurss haldab hankija.

Aastal [tootmisprotsesside](production-process-overview.md), tööd saab teha vahendeid, mis kuuluvad või mida haldab müüjad. Tavaliselt hankija ressursse kasutatakse taseme perioodilise liigse nõudluse, mis ületab ettevõtte tootmisvõimsust omavahendid. Samuti võib hankija pakkuda konkreetseid [ressursi võimalusi](resource-capabilities.md)või ressursse ka.  

Sõltuvalt hankija ressursse, mida kasutatakse tootmisprotsessis, on [tee](routes-operations.md) on tihti logistilise lisanõudeid, sest materjal ja pooltooted tuleb vedada esmalt hankija saidi. Seejärel tuleb transportida alltöövõtu tehte tulem, kas asukohta, mis on määratud järgmise operatsiooni või valmistoodang lattu.  

Allhange tegevuse või tegevuste kasutamisel need mõjutavad kõiki etappe tegevuste määratlemisel arvesse toiminguid, mis on vajalikud tootmise, maksavad, prognoosimine, kavandamine ja planeerimine, materjalide, pooltoodete ja valmistoodangu logistika juhtimist. Lõpuks neid vahendeid vaja oma protsesse ja kulude kontrolli.  

Sisemisi ressursse, on tavaliselt fikseeritud kulumäär eraldatavast jooksul. Seevastu alltöövõtu ressursside maksumus põhineb teenistuses ostuhind. Teenust määratletakse kui teise toote ja saab sõita hankimise ja osta protsesside alltöövõtu operatsioon.  

Praegu ei ole selge mõiste pooltoodete Microsoft Dynamics 365 toiminguteks. Tootmistellimuse, mis nõuab mitme toimingu käigus, et muutuda valmis hea tooraine, sisestatakse lõpetatud kauba taas inventari ainult viimane. Pooltöödeldud tooted, millel on eelmiste operatsioonide kajastatakse lõpetamata toodangu (WIP), kuid nad ei ole sisestatud või jälgida laoseisu. Kuigi te võite tükeldada liinidel ja kooslusi (kooslused) mootorrongid väiksem, selline lähenemine toodete kooslusi ja protsesse, mida tuleb hallata hulk suureneb.  

On kaks meetodid modelleerimine alltöövõtu töö tootmiseks. Need meetodid erinevad nii, et allhange protsessi saab modelleerida, nii, et pool on esindatud protsessi, ja nii, et kulude juhtimine.

-   Protsessi operatsioonide tootmistellimuste või partii tellimuste allhanke korras
    -   Toote teenus peab olema varustatud toote ja peab olema osa komplektist.
    -   See meetod toetab esimene, esimene FIFO või standardkulu.
    -   Pooltöödeldud tooted esitatakse toote teenuse protsessi.
    -   Kulude jälgimine eraldab olulist kulude alltöövõtu tööga seotud kulud.
-   Allhanke korras tootmine andmevoo tegevused lean tootmise voolu
    -   Teenus on teenus laos toodet, ja see ei ole osa komplektist.
    -   See meetod kasutab ostulepingud lepingute.
    -   See meetod kasutab tagasivool maksumus.
    -   See meetod võimaldab koondatud ja asünkroonse. (Sisendid ja väljundid ei sõltu hankeprotsessi.)
    -   Kontroll kulude üle eraldab alltöövõtu tööde tsoonis oma kulude jaotus.

## <a name="subcontracting-of-route-operations"></a>Allhanke korras liin
Protsessi operatsioonide tootmiseks või partii tellimuste allhanke korras kasutamiseks tuleb määratleda teenuse toode, mida kasutatakse teenuse hankimiseks teatavat tüüpi on **teenuse** tüüp. Lisaks peab olema kauba tootemudeli grupi, mis on selle **varustatud toote** valikuvõimalus vastavalt **varude poliitika** seatud **Jah**. See valik määrab, kas toode moodustab varuna toote kättesaamisel (**varustatud toode** = **Jah**), või kas toote vahe tulu ja kulu konto (**varustatud toode** = **nr**). Kuigi selline käitumine võib tunduda vastuoluline, on asjaolu, et ainult tooteid, mis on selle poliitika loob laokanded, mida saab kasutada kulude kontrolli arvutab plaanitud ja tegelik kulu kui tootmistellimus on lõpetatud.  

Pidada planeerimise ja kulude arvutamisel, tuleb lisada teenuse kooslusega. Koosluse Real peab olema ka **hankija** tüüp ja kontrollitakse teenuse eraldatakse protsessi operatsioonile. Protsessi operatsioon peab olema maksavad ressurssi ja ressursi nõue, mis osutab ressurss on **hankija** tüüp, mis ühendub vastava hankijakonto operatsiooni ja teenistuses.  

Selle konfiguratsiooni kasutamisel luuakse ostutellimuse teenistuses tootepõhine tootmistellimuse hinnangu. Ostutellimuse teenuse kasutatakse Ankru ning allhangete. Alltöövõtu töö saab hallata selle **allhankeleping töö** loendi lehel tootmisohje. Alltöövõtu töö saab laeva tooraine ning Kokkuvõttes on hankija tegevuse ettevalmistamisel. Seda kasutatakse ka saada lõpptoote alltöövõtu operatsiooni kauba saabumist, kui teenuse toodet kasutatakse tuvastamiseks pooltoote saabumist. Ostutellimuse rea saabumisel tootmise operatsioon uuendatakse lõpuleviiduks.  

Tootmistellimus on palju tegevust ja iga toimingu võib eraldada erineva hankija. Seetõttu võivad otsast-otsani tootmistellimuse käivitada mitu ostutellimused.

## <a name="subcontracting-of-production-flow-activities"></a>Allhanke korras tootmine andmevoo tegevused
Selle [kulusäästlik töötamine](lean-manufacturing-overview.md)lahendus-mudelite ning allhanketööde teenus, mis on seotud tegevuse kohta on [tootmisprotsesside](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (ülesande juhend teema). Seega seda tüüpi allhanked on ka edaspidi [baasil allhankeid.](activity-based-subcontracting.md) Eriline kulu tüüp, **vahetut välistõlgete tellimist**, on kehtestatud, ja allhange teenused ei kuulu komplekti valmistoodet. Kulusäästlik töötamine kasutamisel kõik tegevused on määratletud kanbans, mis võib olla seotud ühe või mitme tootmistegevuse voolu. Siiani, selle selgituse kõlab nagu tootmistellimuste selgitus. Siiski tuleks tootmistellimuste lõppema alati valmis toode, saate luua kanbans varustamiseks pooltoode. Teil pole uue toote ja kooslusetasemel.  

Kuna kanban eeskirjad võib olla väga dünaamiline, võib mudel erinevad variandid sama toote eest linna tootmise voolu. Kui kasutate lahja allhanked, sisendite ja rahaline voog rangelt lahus. Kõik sisendid ja väljundid on esindatud kanban tegevust. Tellimuste teenus toodete ja teenuste tarne sisestuste automatiseerida, vastavalt tootmise voolu kanban tööde oleku. Kanban töö käivitamist ja valmis isegi enne, et ostutellimused loodud. Allhange dokumentide (ostu- ja ostutarne teenuse) saab liita perioodidele ja teenuseid. Seega säilib ostudokumentidel ja ridade arv väike, isegi kui tarnijad pakuvad allhankelepinguid teenuste üheosaline voolus väga korduvaid tegevuses.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Allhanke tootmise voolu modelleerimine

Linnas on [lean tootmise voolu](lean-manufacturing-modeling-lean-organization.md), protsessi tegevuse võib määratleda kui alltöövõtu töö lahtrile (ressursirühma) on ühe müüja ressursside eraldamisel. Kui töö raku allhankeleping, seotud protsess tegevus peab olema seotud aktiivseid hooldusleppe rea, mis sisaldab hooldusüksuse ja teenuse hind. Hooldusleppe tegevuse määratleb toote kogus kanban töö ja saadud teenuse koguse arvutamisel suhe. Saate valida, kas teenuse kogus arvutatakse vastavalt arv töökohti, hea toote kogus, mis on esitatud tööde või toote koguse (kogus kokku ka praagitud tooted).  

Edastamine võib määratleda ka kui allhankelepinguid. See määratlus ilmneb kaudselt nende tegevusele vastutaja saatmiskulud valimisel. Kui valite **saatja** või **vastuvõtja**, kui vastav allikas või eesmärgi ladu on hankija hallatavas ladu, tegevust käsitletakse allhankelepinguid. Kui valite **vedaja**, tegevus on alati allhankelepinguid. Peatuda alltöövõtu protsessidega seotud tegevuste, alltöövõtu üleandmise tegevus peab olema ühendatud teenindusega enne tootmise voolu aktiveerimist.

### <a name="backflush-costing"></a>Omahinna tagasiarvestus

Täielikult integreeritud kuluarvestuse alltöövõtu tööde maksumus kulusäästlik töötamine lahendus (Kuluarvestus tagasivool). Teenuse ostu tellimuse tarne konteerimisel või arvete ilmnemisel, teenuse maksumus on eraldatud tootmise voolu. Tagasivool omahinna arvutamiseks, arvutatakse dispersioon allhankelepinguid teenuste hüvitamise arvutamisel saadud toodete kogused tarnituna ja arveldatuna teenistuses allhange plokk.

## <a name="material-supply-for-subcontracted-operations"></a>Materjali tarnimiseks allhangete
Pooltoodete ja sellega seotud materjalid tuleb viia asukohta, kus töö füüsiliselt toimub. Allhangete ja tegevuste kasutamisel see on sageli seotud transpordi hankija opereeritud saidi. Materjali alltöövõtu operatsioonile koosluses jaotades kinnitad, et materjal peab lavastatud ressursirühmadele jaotatud ressursi sisendi asukohta. Koondplaneerimise või lahja täiendamise seejärel valmistab materjali kohale.  

Mudel nimekiri, mis asub hankija kaudu, on hea tava määrata hankija hallatavas lao tööstuses. Uue loomine ja määramine ning hankija poolt lihtsalt määratleda hankija hallatavas ladu. Et materjali dokumenteerimiseks tuleb viia hankija enne operatsiooni tuleks teha, tuleks määrata hankija hallatavas ressursi hoidvale ressursirühma sisendi lattu lao.  

Laos materjali täiendamiseks kasutage mitmeid strateegiaid.

-   Üleviimistellimused
-   Töölehtede ülekandmine
-   Tagasivõtmine kanbans
-   Otseostmine hankija kohta

Pooltöödeldud tooted on erand sellest reeglist. Kanda pooltoodete, oled piiratud suvanditest:

-   Tootmise ja partii tellimused, pooltoodete ainult ülekandmist loogiliselt: komplekteerimislehe töölehe abil on **allhankeleping töö** loendi lehel. Selle töölehe loob saatelehe dokumendi, mida saab kanda pool ja tooraine hankijale.
-   Jaoks tootmise voolude allhangete, fikseeritakse üleandmise pooltoodete tühistamise või tootmise kanbans müüja asukohas võtta vastu. Mudel on otseselt tegevusele, saab lõpetada tootmise kanban täiendava üleandmist tegevusega.

**Märkus:** ühe tootmistellimuse tootmisprotsessi ei saa ületada mitmes kohas. See reegel kehtib ka alltöövõtu töö. Seega, laod mida esitab hankija hallatavas materjali asukohad tuleb määratleda sisemisi ressursse, mida kasutatakse protsessi samal territooriumil. Kuigi tootmise voolab võib läbida saite, nad ei saa transport pooltoodete ühest töökohast teise, sest selle toimimine eeldab kulu seoses muutus.  

Toodang lattu ja alltöövõtu ressursirühmi asukoht otse tavaliselt eraldatud lao ja asukoha operatsiooni protsessi või tootmise voolu järgmiseks. See seadistus aitab vähendada aruandlus, mis ilmneb töö või number täiendava üleandmist toiminguid, mis tuleb modelleerida.


