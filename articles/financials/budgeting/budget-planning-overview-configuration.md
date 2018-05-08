---
title: "Eelarve plaanimise ülevaade"
description: Selles artiklis tutvustatakse eelarve plaanimist ja see sisaldab teavet, mis aitab teil eelarve plaanimise konfigureerida ning selle protsesse seadistada.
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b008e70c7d834c6aacad7aef4987e60b12ed8a6d
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="budget-planning-overview"></a>Eelarve plaanimise ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis tutvustatakse eelarve plaanimist ja see sisaldab teavet, mis aitab teil eelarve plaanimise konfigureerida ning selle protsesse seadistada.

<a name="overview-of-budget-planning"></a>Eelarve plaanimise ülevaade
---------------------------

Plaanite eelarvet organisatsiooni juurutatavate eelarvete ettevalmistamisel. Organisatsioon saab eelarve plaanimise konfigureerida ja seejärel seadistada eelarve plaanimise protsessid, et need vastaksid eelarve ettevalmistamise poliitikatele, protseduuridele ja nõuetele. 

Kui mõistate Microsoft Dynamics 365 for Finance and Operationsis kasutatavaid mõisteid ja terminoloogiat, on teil lihtsam oma organisatsioonis eelarve plaanimist rakendada.

### <a name="key-terms"></a>Põhimõisted

-   **Eelarve plaanimise protsessid** – eelarve plaanimise protsessid määravad, kuidas saab eelarveplaane värskendada, töödelda, läbi vaadata ja kinnitada eelarveorganisatsiooni hierarhias. Eelarve plaanimise protsess on seotud eelarvetsükliga organisatsiooniga juriidilise isiku kaudu.
-   **Eelarveplaanid** – eelarveplaanid sisaldavad eelarvetsükli eelarve andmeid. Teil võib olla mitu eri eesmärkidel kasutatavat eelarveplaani. Näiteks saab eelarveplaane kasutada eelarvesummade loomiseks eri organisatsiooniüksustes või need võivad aidata teil võrrelda ja otsuseid vastu võtta.
-   **Eelarveplaani stsenaariumid** – eelarveplaani stsenaariumid määratlevad eelarveplaanide andmete kategooriad. Määrake eelarveplaani stsenaariumid, et toetada valuutat ja muid mõõtühikute klasse, nagu kogus. Valuuta eelarveplaani stsenaariumide näidete hulka kuulub Osakonna eelmine aasta ja Osakonna nõuded. Koguseid kasutavate eelarveplaani stsenaariumide näidete hulka kuulub Eelmise aasta toe kõned ja Täiskohaga töötajate arv.
-   **Eelarve plaanimise etapid** – eelarve plaanimise etapid määratlevad etapid, mida eelarveplaan jõustumisest kuni lõpliku kinnitamiseni järgib. Eelarve planeerimise etapid korraldatakse eelarve planeerimise töövoogudes.
-   **Eelarve plaanimise töövood** – eelarve plaanimise töövood koosnevad eelarve plaanimise etappidest ja määravad need. Eelarve plaanimise töövood on seotud eelarvestuse töövoogudega. Eelarvestuse töövood on automatiseeritud ja käsitsi protsessid, mis liigutavad eelarveplaane läbi eelarve plaanimise etappide.

[![Eelarve plaanimise terminoloogia](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Üldised ülesanded

Eelarve plaanimise abil saate täita järgmisi ülesandeid.

-   Eelarveplaanide loomine eelarvetsükli oodatavate tulude ja kulude määramiseks.
-   Eelarveplaanide analüüsimine ja värskendamine mitme stsenaariumi puhul.
-   Eelarveplaanide automaatne saatmine koos töölehtede, põhjendusdokumentide ja muude manustega ülevaatamiseks ja kinnitamiseks.
-   Mitme eelarveplaani konsolideerimine organisatsiooni madalamalt tasemelt ühte pea-eelarveplaani organisatsiooni kõrgemal tasemel. Saate ka välja arendada üksiku eelarveplaani organisatsiooni kõrgemal tasemel eraldada eelarve organisatsiooni madalamatele tasemetele.

Eelarve plaanimine on integreeritud teiste Microsoft Dynamics 365 for Finance and Operationsi moodulitega. Seetõttu saab teavet tuua eelmistest eelarvetest, tegelikest kuludest, põhivaradest ja inimressurssidest. Kuna eelarve plaanimine on integreeritud ka Microsoft Excelisse ja Microsoft Wordi, saate neid programme kasutada eelarve plaanimise andmetega töötamiseks. Näiteks saab eelarvehaldur eksportida mõne osakonna eelarvetaotluse eelarveplaani stsenaariumist Exceli töölehele. Andmeid saab analüüsida, värskendada ja kanda diagrammina töölehele ning seejärel avaldada tagasi eelarveplaani ridadele.

## <a name="configuring-budget-planning"></a>Eelarve planeerimise konfigureerimine
Leht **Eelarve plaanimise konfiguratsioon** sisaldab enamikku sätteid, mida vajate eelarve plaanimise seadistamiseks. Järgmistes jaotistes kirjeldatakse mõnd põhitegurit, millega peaksite eelarve plaanimise konfigureerimisel arvestama. Pärast konfiguratsiooni lõpetamist saate eelarve plaanimise protsessid seadistada.

### <a name="create-a-budget-planning-schema"></a>Eelarve plaanimise skeemi loomine

Valikuline, kuid soovitatav esimene etapp on skeemi loomine, mis näitab teie organisatsiooni protseduuri eelarve koostamiseks. Saate selle skeemi loomiseks kasutada mis tahes meetodit. Järgmisel joonisel on toodud üldine näide, kus organisatsiooni eri tasemete puhul luuakse eraldi eelarve plaanimise töövood. Etapid on määratletud igas töövoos ja konkreetsed stsenaariumid on määratud eelarveandmete hoidmiseks igale etapile. Ülesandeid täidetakse andmete teisaldamiseks ühest etapist järgmisse. Näiteks saate summad eraldada või liita eri kontodele, kinnitustele või muudele ülevaatustele. Selles näites viitab kursiivkirjas tekst stsenaariumile, mis pole etapi käigus muudetav või andmetele, mis on ajaloolised või etapis varem kinnitatud ja mida ei tohiks seega muuta. 

[![Eelarve plaanimise üldine skeem](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Järgmises näites hindab ettevõtte peakontor algse eelarve lähtesummasid ja jaotab need müügiosakondade vahel. Müügiosakonnad hindavad ja esitavad seejärel oma prognoosi uuesti peakorteritele, kus eelarve haldur prognoosi koondab ja seda kohandab. Lõpuks saadab eelarve haldur kohandatud eelarvesummad CFO-le ülevaatamiseks, lõplikuks korrigeerimiseks ja kinnitamiseks. 

[![Eelarve plaanimise skeemi näide](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Organisatsiooni hierarhia eelarve plaanimiseks

Lehel **Organisatsiooni hierarhia** saate määrata organisatsiooni hierarhia eelarve plaanimise hierarhiana iga eelarve plaanimise protsessi puhul. Eelarve plaanimise hierarhia ei pea ühtima muul otstarbel kasutatava standardse organisatsiooni hierarhiaga. Kuna seda hierarhiat kasutatakse andmete kogumiseks ja jagamiseks, võite soovida, et sellel oleks teistsugune struktuur. Näiteskeemis on müügiosakonnad peakorterite taseme all, mis sisaldab eelarvet ja finantsosakondi. See struktuur erineb tõenäoliselt struktuurist, mida kasutatakse müügiosakondade toimingute haldamiseks. Igale eelarve plaanimise protsessile saab määrata vaid ühe organisatsiooni hierarhia. 

Lisateabe saamiseks vt jaotist [Organisatsioonid ja organisatsiooni hierarhiad](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Kasutaja turvalisus

Eelarve plaanimine saab kasutajaõiguste määramiseks jälgida ühte kahest turvamudelist. Turvamudeli määramiseks seadistate eelarve plaanimise parameetri lehel **Eelarve plaanimise konfiguratsioon**.

### <a name="budget-planning-workflows-stages"></a>Eelarve plaanimise töövoogude etapid

Eelarve plaanimise töövooge kasutatakse koos eelarvestuse töövoogudega eelarveplaanide loomise ja aredamise haldamiseks.

Eelarve planeerimise töövoog koosneb järjestatud etappidest, mille eelarveplaan läbib. Iga eelarve plaanimise töövoog on seotud eelarvestuse töövooga. Eelarvestuse töövood on töövoo tüüp, mida kasutatakse kogu Finance and Operationsis. Eelarvestuse töövoog suunab eelarveplaani koos töölehtede, põhjenduste ja manustega organisatsioonile ülevaatamiseks ja kinnitamiseks. 

Saate luua eelarve plaanimise töövoo jaotises **Töövooetapid** lehel **Eelarve plaanimise konfiguratsioon**. Seal saate valida etapid ja kasutatava eelarvestamise töövoo ja konfigureerida täiendavad sätted. 

Hea tava on luua eelarve plaanimise töövoog eelarvestamise hierarhia igal tasandil. Seejärel määrake eelarvestamise töövoog, mis sisaldab eelarve plaanimise töövoo etappidele vastavaid elemente. Selles artiklis varem kuvatud näidisskeemis luuakse üks eelarve plaanimise töövoog müügiosakondade puhul ja teine peakorterite puhul. Eelarvestuse töövoog teisaldab eelarveplaane etappide kaudu. 

Saate luua eelarvestamise töövoo eelarve plaanimise puhul lehel **Eelarvestuse töövood**. Protsess sarnaneb Finance and Operationsis muude töövoogude loomise protsessiga. Järgmisel joonisel on toodud peakorteri töövoo näide. 

[![Eelarvestuse töövoog eelarve plaanimiseks](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Töövoog sisaldab elemente müügiosakondadele eraldamiseks ja nende esitamiste koondamiseks, eelarvehalduri ülevaatust, CFO heakskiitu ja etapi üleminekuid iga etapi vahel. 

Saate määrata eelarvestamise töövoo igale eelarve plaanimise töövoole jaotises **Töövooetapid** lehel **Eelarve plaanimise konfiguratsioon**.

### <a name="parameters-scenarios-and-stages"></a>Parameetrid, stsenaariumid ja etapid

Lehe **Eelarve plaanimise konfiguratsioon** algsätted võimaldavad luua mõne koosteüksuse hilisemateks konfiguratsioonietappideks.

-   **Parameetrid** – parameetrid määratlevad turbereeglid, mida soovite rakendada eelarveplaanide puhul ja vaikimisi finantsdimensioonid, mida tuleks kasutada, kui kasutajad lähevad eelarveplaani stsenaariumi summadesse süvitsi.
-   **Stsenaariumid** – stsenaariumid hõlmavad eelarveplaanide puhul soovitavaid andmete kategooriaid. Määrake eelarveplaani stsenaariumid, et toetada valuutat ja muid mõõtühikute klasse, nagu kogus. Eelarveplaanis tähistavad stsenaariumid eelarve plaanimise andmete ühte versiooni. Valuuta eelarveplaani stsenaariumide näidete hulka kuulub Eelmise aasta müük ja Allkirjastatud lepingud. Koguseid kasutavate stsenaariumide näidete hulka kuulub Müügikõnede arv ja Täiskohaga töötajate arv.
-   **Etapid** – etapid määravad etapid, mida eelarveplaan jõustumisest kuni lõpliku kinnitamiseni järgib. Eelarve plaanimise etappide näidete hulka kuulub Peakorteri ümberarvestus, CFO ülevaade ja Lõplik.

### <a name="allocation-schedules"></a>Eraldamisgraafikud

Eelarve plaanimisel saate eraldada eelarveplaani ridade summad või kogused ühest stsenaariumist teise või isegi samasse stsenaariumi. Näiteks võite eraldada samasse stsenaariumi, kui soovite muudatusi rakendada finantsdimensioonidele või selle stsenaariumi summade kuupäevadele. Eraldada saab eelarveplaani piires või ühest eelarveplaanist teise. 

Eraldamisgraafikud eraldavad automaatselt töövoo töötlemise ajal eelarveplaani read. Saate eraldada, kasutades loendi **Eraldamismeetod** mis tahes järgmist meetodit.

- <strong>Eralda perioodide lõikes</strong> – saate kasutada perioodi eraldamisvõtit eelarveplaani ridade eraldamiseks algsest eelarveplaani stsenaariumist sihtstsenaariumi perioodide lõikes. <strong>Märkus.</strong> Enne perioodide lõikes eraldamist peate seadistama perioodi eraldusvõtmed lehel *<strong><em>Perioodi eraldamise kategooriad</em></strong>*.
- <strong>Eralda dimensioonidele</strong> – eelarveplaani read eraldatakse algsest eelarveplaani stsenaariumist sihtstsenaariumi finantsdimensioonide lõikes. <strong>Märkus.</strong> Enne dimensioonidele eraldamist peate seadistama eelarve eraldustingimused lehel *<strong><em>Eelarve eraldustingimused</em></strong>*.
- **Koonda** – eelarveplaani read koondatakse seostatud eelarveplaanide algsest eelarveplaani stsenaariumist eelarve emaplaani sihtstsenaariumisse.
- **Jaota** – eelarveplaani read jaotatakse eelarve emaplaani algse eelarveplaani stsenaariumist seostatud eelarveplaanide sihtstsenaariumisse.
- **Kasuta pearaamatu eraldamisreegleid** – eelarveplaani read jaotatakse algse eelarveplaani stsenaariumist sihtstsenaariumisse valitud pearaamatu eraldamisreegli põhjal.
- **Kopeeri eelarveplaanist** – saate valida eraldamise allikana kasutamiseks teise eelarveplaani.

### <a name="stage-allocations"></a>Etapi eraldamised

Etapi eraldamisi kasutatakse töövoo töötlemise ajal eelarveplaani ridade automaatseks eraldamiseks. Etapi eraldamiste kasutamisel saab sihtstsenaariumi eelarveplaani ridu luua ja muuta ilma eelarveplaani ettevalmistaja või ülevaataja sekkumiseta.

Etapi eraldamise seadistamisel seostage eelarve planeerimise töövoog ja etapp eraldamisgraafikuga. Eelarve plaanimise töövoog tuleb seostada eelarvestuse töövooga, mis kasutab automatiseeritud töövoo ülesannet *<strong><em>Eelarve plaanimise etapi eraldamine</em></strong>*. Kui töövoog jõuab määratud etappi, toimub eraldamine automaatselt. Seda automatiseeritud ülesannet saab kasutada uues stsenaariumis eelarveplaani ridade loomiseks. 

Selles artiklis varem kuvatud näidisskeemis tehakse eraldamine eelarveplaani summade ja peakorterite alusetapi stsenaariumide üleviimiseks teise eelarveplaani ja stsenaariumidesse müügiosakonna hinnangu etapis. Järgmisel joonisel kuvatakse näidisskeemi asjakohane jaotis.

[![Etapi eraldamine](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Peale selle tehakse näidisskeemis koondamine müügiosakonna edastatud etapi eelarveplaanidest ja stsenaariumidest peakontori ümberarvestuse etapi emaplaani. Järgmisel joonisel kuvatakse näidisskeemi asjakohane jaotis.

[![Liitmine](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteedid

Soovi korral saate eelarveplaani prioriteete kasutada seadistatud eelarveplaanide kategooriate ja eesmärkide määramiseks. Ühtlasi saate kasutada prioriteete mitme eelarveplaani organiseerimiseks, klassifitseerimiseks ja hindamiseks. Näiteks saate luua eelarve plaanimise prioriteedi tervise ja ohutuse jaoks ning hinnata seejärel sellele prioriteedile määratud eelarveplaane. Samuti saate määrata numbri eelarveplaanide järjestamiseks kõikide eelarveplaanide lõikes.

### <a name="columns-and-layouts"></a>Veerud ja paigutused

Eelarvenäitajad kuvatakse eelarveplaanil ridades ja veergudes. Esmalt peate määratlema veerud ja seejärel saate luua veergude esitluse määratlemiseks paigutuse. 

Valige veeru määratlemiseks eelarveplaani stsenaarium. Selle stsenaariumi rea summasid näidatakse eelarveplaanil. Saate summa filtrimiseks valida perioodi ja ühtlasi saate rakendada pearaamatukontol põhinevaid filtreid. 

Paigutuse määratlemisel valige pearaamatu dimensioonikogum eelarveplaani ridade loomiseks, mida soovite kuvada, ja valige paigutuselementidena veerud. Saate luua mitu paigutust, nii et eelarveplaan kuvab andmeid, mida soovite eelarve plaanimise protsessi eri etappides. 

Lisaks eelarvesummade veergudele saate määratleda veerud projekti, pakutava projekti, vara ja pakutavate vara väljade puhul eelarveplaanist. Saate määratleda ka eelarvestatud ametikohtade veeru. See suvand on väga kasulik, kui peate analüüsima töötajate eelarveid. 

Näidisskeemi puhul võite soovida luua veerge PY müügi, lepingute ja prognoosi stsenaariumide puhul (järgmisel joonisel on kujutatud skeemi asjakohane jaotis). Seejärel saate jaotada ühe või kõik neist stsenaariumidest eraldi veergudesse rahandusaasta kvartalite kaupa nii, et müügiosakonna juhataja saab iga perioodi eelarvesummad täpselt sisestada.

[![Veerud](./media/columns.png)](./media/columns.png) 

Saate ka määrata iga paigutuselemendi (veeru) redigeeritavuse ja selle, kas veerg on saadaval igas selle paigutuse puhul loodud töölehe mallis. Näidisskeemi puhul on hinnangu etapi puhul kasutatud paigutuses eelarve veerud redigeeritavad, samas kui PY müügi ja lepingute veerud on kirjutuskaitstud.

### <a name="templates"></a>Mallid

Jaotises **Paigutused** lehel **Eelarve plaanimise konfiguratsioon** saate ka luua, vaadata või üles laadida Exceli malle. Need mallid on iga eelarveplaaniga seotud töövihikud täiendava analüüsi, diagrammide ja andmesisestusvõimaluste pakkumiseks. 

Saate malli luua, seda vaadata või üles laadida iga paigutuse puhul. Malli loomisel paigutus lukustatakse ja seda ei saa redigeerida. See lukustamine aitab tagada, et malli vorming ühtib eelarveplaani paigutusega ja sisaldab samu andmeid. Pärast malli loomist saab seda vaadata ja redigeerida. Näiteks saate malli diagramme lisada või selle ilmet täiendavalt kohandada.

> [!NOTE] 
> Mall tuleks salvestada asukohta, kuhu kasutajal on juurdepääs, nii et selle saaks pärast redigeerimise lõpetamist paigutusse üles laadida. Nii kasutatakse malli paigutust kasutavates eelarveplaanides.

### <a name="descriptions"></a>Kirjeldused

Kirjeldusi, mille saate määrata jaotises **Paigutused**, kasutatakse paigutusse kaasatud finantsdimensiooni nime kuvamiseks. Näiteks võib organisatsioon soovida põhikonto nime kuvamist eelarveplaanis põhikonto numbri kõrval, kuid jätta kuva risustamise vältimiseks välja muude finantsdimensioonide nimed.

## <a name="setting-up-budget-planning-processes"></a>Eelarve planeerimise protsesside seadistamine

Kui olete eelarve plaanimise konfigureerimise lõpetanud, saate seadistada eelarve plaanimise protsessid lehel **Eelarve plaanimise protsess**. Eelarve plaanimise protsessid on reeglistikud, mis määravad, kuidas saab eelarveplaane värskendada, töödelda, läbi vaadata ja kinnitada eelarveorganisatsiooni hierarhias. 

Valite iga eelarve plaanimise protsessi puhul esmalt eelarvetsükli ja pearaamatu. Iga eelarve plaanimise protsess on seotud ainult ühe eelarvetsükli ja pearaamatuga. Seejärel valige kiirkaardilt **Eelarve plaanimise protsessi haldus** eelarveorganisatsiooni hierarhia ja määrake eelarve plaanimise töövoog kõikidele ruudustikus olevatele organisatsiooni vastutuskeskustele. 

Sarnastele vastutuskeskustele eelarve plaanimise töövoo määramiseks või selle muutmiseks klõpsake valikut **Määra töövoog** ja valige seejärel sihitav organisatsiooni tüüp ning kasutatav eelarve plaanimise töövoog. Iga eelarve plaanimise töövooga seostatud eelarvestuse töövoo ID lisatakse ruudustikku automaatselt. 

Kui määrate kiirkaardil **Eelarve plaanimise etapi reeglid ja paigutused** etapi reeglid ja mallid, saate määrata igale eelarve plaanimise etapile erinevad reeglistikud ja vaikepaigutused. Näiteks võimaldab müügiosakonna hinnangu etapp kasutajatel eelarveplaani ridu muuta, kuid keelab kasutajatel ridade lisamise. Esitatud etapp võimaldab kasutajatel ridu vaadata, kuid mitte neid lisada või muuta, kuna töö on selles etapis lõpetatud ja eelarveplaanide muudatusi tuleb vältida. Eelarveplaanide puhul saadaolevate paigutuste valimiseks klõpsake suvandit **Alternatiivsed paigutused**. 

Võite valida eelarve plaanimise prioriteedid ka kiirkaardilt **Eelarveplaani prioriteedi piirangud**. Prioriteete saab seejärel eelarveplaanidel valida. 

Viimane etapp on eelarve plaanimise protsessi aktiveerimine menüü **Tegevused** kaudu. Eelarve plaanimise protsessi ei saa kasutada enne, kui see on aktiveeritud. 

Menüüs **Tegevused** saate luua ka uue protsessi, kopeerides olemasoleva protsessi. See funktsioon on kasulik organisatsioonidele, mis järgivad igal eelarvetsüklil sama protsessivoogu ja teevad vähe muudatusi või mitte ühtegi muudatust. 

Teine kasulik käsk menüüs **Tegevused** on **Kuva eelarve protsessi olekut**. See käsk kuvab graafiliselt protsessi eelarveplaanid koos asjakohaste andmetega, nagu plaani töövoo olek, kokkuvõtted summa ja ühiku järgi ja ühe klõpsuga navigeerimine eelarveplaanidele.

[![Eelarve plaanimise protsessi olek](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)




