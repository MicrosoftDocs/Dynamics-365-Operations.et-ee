---
title: Eelarve plaanimise ülevaade
description: Selles teemas tutvustatakse eelarve plaanimist. See teema sisaldab teavet, mis aitab teil eelarve planeerimist konfigureerida ja eelarve planeerimise protsesse seadistada.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ed56920ca1b4f2ac1313f7025b7a3c7245e9913
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5898206"
---
# <a name="budget-planning-overview"></a>Eelarve plaanimise ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse eelarve plaanimist. See teema sisaldab teavet, mis aitab teil eelarve planeerimist konfigureerida ja eelarve planeerimise protsesse seadistada.

## <a name="overview-of-budget-planning"></a>Eelarve plaanimise ülevaade

Organisatsioon saab eelarve plaanimise konfigureerida ja seejärel seadistada eelarve plaanimise protsessid, et need vastaksid eelarve ettevalmistamise poliitikatele, protseduuridele ja nõuetele. Kui mõistate Microsoft Dynamics 365 Finance-is kasutatavaid mõisteid ja terminoloogiat, on teil lihtsam oma organisatsioonis eelarve plaanimist rakendada.

### <a name="key-terms"></a>Põhimõisted

- **Eelarve plaanimise protsessid** – eelarve plaanimise protsessid määravad, kuidas saab eelarveplaane värskendada, töödelda, läbi vaadata ja kinnitada eelarveorganisatsiooni hierarhias. Eelarve plaanimise protsess on seotud eelarvetsükliga ja organisatsiooniga juriidilise isiku kaudu.
- **Eelarveplaanid** – eelarveplaanid sisaldavad eelarvetsükli eelarve andmeid. Teil võib olla mitu eri eesmärkidel kasutatavat eelarveplaani. Näiteks saate kasutada eelarveplaane, et luua eelarvesummasid erinevatele organisatsiooniüksustele. Saate neid kasutada ka võrdluste tegemiseks ja teadlike otsuste langetamiseks.
- **Eelarveplaani stsenaariumid** – eelarveplaani stsenaariumid määratlevad eelarveplaanide andmete kategooriad. Määrake eelarveplaani stsenaariumid, mis toetavad valuutaklasse ja muid mõõdikuklasse, nt koguseid. Valuuta eelarveplaani stsenaariumide näidete hulka kuuluvad "Osakonna eelmine aasta" ja "Osakonna nõuded". Koguseid kasutavate eelarveplaani stsenaariumide näidete hulka kuulub "Eelmise aasta tugikõned" ja "Täiskoha ekvivalentide arv".
- **Eelarve plaanimise etapid** – Eelarve plaanimise etapid määratlevad astmed, mida eelarveplaan järgib selle algusest kuni lõpliku kinnitamiseni. Eelarve planeerimise etapid korraldatakse eelarve planeerimise töövoogudes.
- **Eelarve plaanimise töövood** – eelarve plaanimise töövood koosnevad eelarve plaanimise etappidest ja määravad need. Eelarve plaanimise töövood on seotud eelarvestuse töövoogudega. Eelarvestuse töövood on automatiseeritud ja käsitsi protsessid, mis liigutavad eelarveplaane läbi eelarve plaanimise etappide.

[![Eelarve plaanimise terminoloogia](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Tavalised ülesanded

Eelarve plaanimise abil saate täita järgmisi ülesandeid.

- Eelarveplaanide loomine eelarvetsükli oodatavate tulude ja kulude määramiseks.
- Eelarveplaanide analüüsimine ja värskendamine mitme stsenaariumi puhul.
- Eelarveplaanide automaatne saatmine koos töölehtede, põhjendusdokumentide ja muude manustega ülevaatamiseks ja kinnitamiseks.
- Mitme eelarveplaani konsolideerimine organisatsiooni madalamalt tasemelt üheks emaeelarveplaaniks organisatsiooni kõrgemal tasemel. Saate ka välja arendada ühe eelarveplaani organisatsiooni kõrgemal tasemel ja eraldada eelarve organisatsiooni madalamatele tasemetele.

Eelarve plaanimine on integreeritud teiste moodulitega. Nii saate kaasata teavet eelmistest eelarvetest, tegelikest kuludest, põhivaradest ja inimressurssidest. Kuna eelarve plaanimine on integreeritud ka rakendustega Microsoft Excel ja Microsoft Word, saate nende programmidega kasutada eelarve plaanimise andmeid. Näiteks saab eelarvehaldur eksportida mõne osakonna eelarvetaotluse eelarveplaani stsenaariumist Exceli töölehele. Andmeid saab seejäral analüüsida, värskendada ja kanda graafikuna töölehele ning seejärel kanda tagasi eelarveplaani ridadele.

## <a name="configuring-budget-planning"></a>Eelarve planeerimise konfigureerimine

Funktsionaalsus, mis oli juurutatud Dynamics 365 Finance versiooni 10.0.9 (aprill 2020), sisaldab funktsiooni, mis aitab parandada toimimist, kui kasutate Exceli kirjete värskendamiseks nuppu **Avalda** ja seejärel saadate need kliendile tagasi. See funktsioon kiirendab värskendusprotsessi ja aitab ka vähendada tõenäosust, et värskendus blokeeritakse, kui värskendate üheaegselt palju kirjeid. Selle funktsionaalsuse lubamiseks minge tööruumi **Funktsioonide haldus** ja lülitage sisse funktsioon **Eelarve planeerimise päringu toimimise optimeerimine** jaotises **Eelarve koostamine**. Soovitame selle funktsiooni sisse lülitada.

Leht **Eelarve plaanimise konfiguratsioon** sisaldab enamikku sätteid, mida vajate eelarve plaanimise seadistamiseks. Järgmistes jaotistes kirjeldatakse mõnd põhitegurit, millega peaksite eelarve plaanimise konfigureerimisel arvestama. Pärast konfigureerimise lõpetamist saate eelarve plaanimise protsessid seadistada.

### <a name="budget-planning-schema-optional"></a>Eelarve plaanimise skeem (valikuline)

Valikuline, kuid soovitatav esimene etapp on skeemi loomine, mis näitab teie organisatsiooni eelarve koostamise protseduuri. Saate selle skeemi loomiseks kasutada mis tahes meetodit.

Järgmisel joonisel on toodud üldine näide, kus organisatsiooni eri tasemete puhul luuakse eraldi eelarve plaanimise töövood. Etapid on määratletud igas töövoos ja igas etapis on määratud konkreetsed stsenaariumid eelarveandmete hoidmiseks. Täidetakse ülesandeid andmete edastamiseks ühest etapist järgmisse. Näiteks saate summad eraldada või liita eri kontodele, kinnitustele või muudele ülevaatustele. Selles näites viitab kursiivkirjas tekst stsenaariumile, mis pole etapi käigus muudetav või andmetele, mis on ajaloolised või kinnitatud varasemas etapis ja mida ei tohi seega muuta.

[![Eelarve plaanimise üldine skeem](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

Järgmises näites hindab ettevõtte peakorter algse eelarve lähtesummasid ja jaotab need müügiosakondade vahel. Müügiosakonnad hindavad ja esitavad seejärel oma prognoosi uuesti peakorterile, kus eelarvehaldur prognoosi koondab ja kohandab. Lõpuks saadab eelarvehaldur kohandatud eelarvesummad peafinantsdirektorile (CFO) ülevaatamiseks, lõplikuks korrigeerimiseks ja kinnitamiseks.

[![Eelarve plaanimise skeemi näide](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Organisatsiooni hierarhia eelarve plaanimiseks

Lehel **Organisatsiooni hierarhia** saate määrata organisatsiooni hierarhia eelarve plaanimise hierarhiaks iga eelarve plaanimise protsessi puhul. Eelarve plaanimise hierarhia ei pea ühtima muul otstarbel kasutatava standardse organisatsiooni hierarhiaga. Kuna seda hierarhiat kasutatakse andmete kogumiseks ja jagamiseks, võite soovida, et sellel oleks teistsugune struktuur. Näidisskeemis on Müügiosakonnad peakorteri taseme all, mis sisaldab Eelarve- ja Finantsosakondi. See struktuur tõenäoliselt erineb struktuurist, mida kasutatakse Müügiosakondade toimingute haldamiseks. Igale eelarve plaanimise protsessile saab määrata vaid ühe organisatsiooni hierarhia.

Lisateabe saamiseks vt jaotist [Organisatsioonid ja organisatsiooni hierarhiad](../../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md).

### <a name="user-security"></a>Kasutaja turvalisus

Eelarve plaanimine saab kasutajaõiguste määramiseks jälgida ühte kahest turvamudelist. Turvamudeli määramiseks seadistate eelarve plaanimise parameetri lehel **Eelarve plaanimise konfiguratsioon**.

### <a name="budget-planning-workflows-stages"></a>Eelarve plaanimise töövoogude etapid

Eelarve plaanimise töövooge kasutatakse koos eelarvestuse töövoogudega eelarveplaanide loomise ja arendamise haldamiseks.

Eelarve planeerimise töövoog koosneb järjestatud etappidest, mille eelarveplaan läbib. Iga eelarve plaanimise töövoog on seotud eelarvestuse töövooga. Eelarvestuse töövood on töövoo tüüp, mida kasutatakse läbi kogu Dynamics 365 Finance. Eelarvestuse töövood suunavad eelarveplaanid koos töölehtede, põhjenduste ja manustega organisatsioonile ülevaatamiseks ja kinnitamiseks.

Saate luua eelarve plaanimise töövoo jaotises **Töövooetapid** lehel **Eelarve plaanimise konfiguratsioon** . Seal saate valida etapid ja kasutatava eelarvestamise töövoo ja konfigureerida täiendavad sätted.

Hea tava on luua eelarve plaanimise töövoog eelarvestamise hierarhia igal tasandil. Seejärel määrake eelarvestamise töövoog, mis sisaldab eelarve plaanimise töövoo etappidele vastavaid elemente. Selle näite varem kuvatud näidisskeemis luuakse üks eelarve plaanimise töövoog Müügiosakondadele ja teine peakorterile. Eelarvestuse töövoog teisaldab eelarveplaane etappide kaupa.

Saate luua eelarvestamise töövoo eelarve plaanimiseks lehel **Eelarvestuse töövood**. Protsess sarnaneb muude töövoogude loomise protsessiga. Järgmisel joonisel on toodud peakorteri töövoo näide.

[![Eelarvestuse töövoog eelarve plaanimiseks](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

Töövoog sisaldab järgmisi elemente:

- Edastamine Müügiosakondadele ja nende panuse liitmine
- Eelarvehalduri ülevaade
- CFO kinnitus
- Eelarve planeerimise töövoo kõigi etappide vahelised etapiedastused

Saate määrata eelarvestamise töövoo igale eelarve plaanimise töövoole jaotises **Töövooetapid** lehel **Eelarve plaanimise konfiguratsioon**.

### <a name="parameters-scenarios-and-stages"></a>Parameetrid, stsenaariumid ja etapid

Lehe **Eelarve plaanimise konfiguratsioon** algsätted võimaldavad luua mõne koosteüksuse hilisemateks konfiguratsioonietappideks.

- **Parameetrid** – Parameetrid määratlevad turbereeglid, mida soovite rakendada eelarveplaanide puhul ja vaikimisi finantsdimensioonid, mida tuleb kasutada, kui kasutajad uurivad süvitsi eelarveplaani stsenaariumi summasid.
- **Stsenaariumid** – stsenaariumid hõlmavad eelarveplaanide puhul soovitavaid andmete kategooriaid. Määrake eelarveplaani stsenaariumid, mis toetavad valuutaklasse ja muid mõõdikuklasse, nt koguseid. Eelarveplaanis tähistavad stsenaariumid eelarve plaanimise andmete ühte versiooni. Valuuta eelarveplaani stsenaariumide näidete hulka kuuluvad "Eelmise aasta müük" ja "Allkirjastatud lepingud." Koguseid kasutavate stsenaariumide näidete hulka kuuluvad "Müügikõnede arv" ja "Täiskohaekvivalentide (FTE) arv".
- **Etapid** – Etapid määravad astmed, mida eelarveplaan järgib algusest kuni lõpliku kinnitamiseni. Eelarve plaanimise etappide näidete hulka kuuluvad "Peakorteri ümberarvestus", "CFO ülevaade" ja "Lõplik".

### <a name="allocation-schedules"></a>Eraldamisgraafikud

Eelarve plaanimisel saate eraldada eelarveplaani ridade summad või kogused ühest stsenaariumist teise või isegi samasse stsenaariumi. Näiteks võite eraldada summad või kogused samale stsenaariumile, kui soovite muudatusi rakendada finantsdimensioonidele või selle stsenaariumi summade kuupäevadele. Eraldada saab eelarveplaani piires või ühest eelarveplaanist teise.

Eraldamisgraafikud eraldavad automaatselt töövoo töötlemise ajal eelarveplaani read. Saate teha eraldisi, kasutades loendi **Eraldamismeetod** mis tahes järgmist meetodit.

- **Eralda perioodide lõikes** – saate kasutada perioodi eraldamisvõtit eelarveplaani ridade eraldamiseks algsest eelarveplaani stsenaariumist sihtstsenaariumi perioodide lõikes.

    > [!NOTE]
    > Enne eraldamist perioodide lõikes peate seadistama perioodi eraldusvõtmed lehel **Perioodi eraldamise kategooriad** .

- **Eralda dimensioonidele** – eelarveplaani read eraldatakse algsest eelarveplaani stsenaariumist sihtstsenaariumi finantsdimensioonide lõikes.

    > [!NOTE]
    > Enne dimensioonidele eraldamist peate seadistama eelarve eraldustingimused lehel **Eelarve eraldustingimused** .

- **Koonda** – eelarveplaani read koondatakse seostatud eelarveplaanide algsest eelarveplaani stsenaariumist eelarve emaplaani sihtstsenaariumisse.
- **Jaota** – eelarveplaani read jaotatakse eelarve emaplaani algse eelarveplaani stsenaariumist seostatud eelarveplaanide sihtstsenaariumisse.
- **Kasuta pearaamatu eraldamisreegleid** – eelarveplaani read jaotatakse algse eelarveplaani stsenaariumist sihtstsenaariumisse valitud pearaamatu eraldamisreegli põhjal.
- **Kopeeri eelarveplaanist** – saate valida eraldamise allikana kasutamiseks teise eelarveplaani.

### <a name="stage-allocations"></a>Etapi eraldamised

Etapi eraldamisi kasutatakse töövoo töötlemise ajal eelarveplaani ridade automaatseks eraldamiseks. Etapi eraldiste kasutamisel saab sihtstsenaariumi eelarveplaani ridu luua ja muuta ilma eelarveplaani ettevalmistaja või ülevaataja sekkumiseta.

Etapi eraldamise seadistamisel seostage eelarve planeerimise töövoog ja etapp eraldamisgraafikuga. Eelarve plaanimise töövoog tuleb seostada eelarvestuse töövooga, mis kasutab automatiseeritud töövoo ülesannet **Eelarve plaanimise etapi eraldamine** . Kui töövoog jõuab määratud etappi, toimub eraldamine automaatselt. Seda automatiseeritud ülesannet saab kasutada uues stsenaariumis eelarveplaani ridade loomiseks.

Selles teema all varem kuvatud näidisskeemis tehakse eraldamine eelarveplaani summade ja peakorteri etapi "Alus"stsenaariumide üleviimiseks teise eelarveplaani ja stsenaariumidesse Müügiosakondade etapis "Hinnang". Järgmisel joonisel kuvatakse näidisskeemi asjakohane jaotis.

[![Etapi eraldamine](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Lisaks tehakse näidisskeemis liitmine Müügiosakondade etapis "Edastatud" eelarveplaanidest ja stsenaariumidest peakorteri etapi "Ümberarvestus" emaplaani. Järgmisel joonisel kuvatakse näidisskeemi asjakohane jaotis.

[![Liitmine](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteedid

Soovi korral saate eelarveplaani prioriteete kasutada seadistatud eelarveplaanide kategooriate ja eesmärkide määramiseks. Ühtlasi saate kasutada prioriteete mitme eelarveplaani organiseerimiseks, klassifitseerimiseks ja hindamiseks. Näiteks saate luua eelarve plaanimise prioriteedi tervise ja ohutuse jaoks ning hinnata seejärel sellele prioriteedile määratud eelarveplaane. Saate ka määrata oma eelarveplaanile arvu, et näidata pingerida.

### <a name="columns-and-layouts"></a>Veerud ja paigutused

Eelarveplaanis kuvatakse eelarvenäitajad ridades ja veergudes. Esmalt peate määratlema veerud ja seejärel saate luua nende veergude esitluse määratlemiseks paigutuse.

Valige veeru määratlemiseks eelarveplaani stsenaarium. Selle stsenaariumi rea summasid näidatakse eelarveplaanis. Saate summa filtrimiseks valida perioodi ja ühtlasi saate rakendada pearaamatukontol põhinevaid filtreid.

Paigutuse määratlemisel valige pearaamatu dimensioonikogum eelarveplaani ridade loomiseks, mida soovite kuvada, ja valige paigutuselementidena veerud. Saate luua mitu paigutust, nii et eelarveplaan kuvab andmeid, mida soovite eelarve plaanimise protsessi eri etappides.

Lisaks eelarvesummade veergudele saate määratleda veerud projekti, pakutava projekti, vara ja pakutavate vara väljade puhul eelarveplaanist. Saate määratleda ka eelarvestatud ametikohtade veeru. See suvand on väga kasulik, kui peate analüüsima personali eelarveid.

Näidisskeemi puhul võite soovida luua veerge stsenaariumitele "PY müük", "Lepingud" ja "Prognoos". (Järgnev kujutis näitab skeemi vastavat sektsiooni.) Seejärel saate jaotada ühe või kõik neist stsenaariumidest eraldi veergudesse rahandusaasta kvartalite kaupa nii, et Müügiosakonna juhataja saab täpselt sisestada iga perioodi prognoositavad summad.

[![Veergude lisamise skeemi jaotiste joonis](./media/columns.png)](./media/columns.png)

Saate ka määrata iga paigutuselemendi (veeru) redigeeritavuse ja selle, kas veerg on saadaval igas selleks paigutuseks loodud töölehe mallis. Näidisskeemi puhul on etapis "Hinnang" kasutatud paigutuses veerud "Eelarve" redigeeritavad, samas kui veerud "PY müük" ja "Lepingud" on kirjutuskaitstud.

> [!NOTE]
> Vaikimisi on teie veergude arv piiratud 36-ga, välja arvatud juhul, kui laiendate eelarve plaanimist etappidega jaotisest [Laienda eelarve plaanimise paigutust](./extending-budget-planning-layout.md).

### <a name="templates"></a>Mallid

Jaotises **Paigutused** lehel **Eelarve plaanimise konfiguratsioon** saate ka moodustada, vaadata või üles laadida Exceli malle igale paigutusele. Need mallid on iga eelarveplaaniga seotud töövihikud täiendava analüüsi, diagrammide ja andmesisestusvõimaluste pakkumiseks.

Malli loomisel paigutus lukustatakse ja seda ei saa redigeerida. See lukustamine aitab tagada, et malli vorming ühtib eelarveplaani paigutusega ja sisaldab samu andmeid. Pärast malli loomist saab seda vaadata ja redigeerida. Näiteks saate malli diagramme lisada või selle ilmet täiendavalt kohandada.

> [!NOTE]
> Mall tuleks salvestada kohta, kuhu kasutajal on juurdepääs, nii et selle saaks pärast redigeerimise lõpetamist paigutusse üles laadida. Nii saab malli kasutada paigutust rakendavates eelarveplaanides.

### <a name="descriptions"></a>Kirjeldused

Kirjeldusi, mille saate määrata jaotises **Paigutused**, kasutatakse paigutusse kaasatud finantsdimensiooni nime kuvamiseks. Näiteks võib organisatsioon soovida näidata põhikonto nime, mis asub eelarveplaani põhikonto numbri kõrval. Kuid see võib soovida jätta välja teiste finantsdimensioonide nimed, et vältida ekraani ülekuhjamist.

## <a name="setting-up-budget-planning-processes"></a>Eelarve planeerimise protsesside seadistamine

Kui olete eelarve plaanimise konfigureerimise lõpetanud, saate seadistada eelarve plaanimise protsessid lehel **Eelarve plaanimise protsess**. Eelarve plaanimise protsessid on reeglistikud, mis määravad, kuidas saab eelarveplaane värskendada, töödelda, läbi vaadata ja kinnitada eelarveorganisatsiooni hierarhias.

Valite iga eelarve plaanimise protsessi puhul esmalt eelarvetsükli ja pearaamatu. Iga eelarve plaanimise protsess on seotud ainult ühe eelarvetsükli ja pearaamatuga. Seejärel valige kiirkaardil **Eelarve plaanimise protsessi haldus** eelarveorganisatsiooni hierarhia ja määrake eelarve plaanimise töövoog kõikidele organisatsiooni vastutuskeskustele ruudustikus.

Sarnastele vastutuskeskustele eelarve plaanimise töövoo määramiseks või selle muutmiseks valige **Määra töövoog** ja valige seejärel sihitava organisatsiooni tüüp ning kasutatav eelarve plaanimise töövoog. Iga eelarve plaanimise töövooga seostatud eelarvestuse töövoo ID lisatakse ruudustikku automaatselt.

Kui määrate kiirkaardil **Eelarve plaanimise etapi reeglid ja paigutused** etapi reeglid ja mallid, saate määrata igale eelarve plaanimise etapile erinevad reeglistikud ja vaikepaigutused. Näiteks võimaldab Müügiosakondade etapp "Hinnang" kasutajatel eelarveplaani ridu muuta, kuid keelab kasutajatel ridade lisamise. Etapp "Esitatud" võimaldab kasutajatel ridu vaadata, kuid mitte neid lisada või muuta, kuna töö on selles etapis lõpetatud ja eelarveplaanide muudatusi tuleb vältida. Eelarveplaanide paigutuste valimiseks klõpsake suvandit **Alternatiivsed paigutused**.

Võite valida eelarve plaanimise prioriteedid ka kiirkaardilt **Eelarveplaani prioriteedi piirangud**. Prioriteete saab seejärel eelarveplaanidel valida.

Viimane samm on aktiveerida eelarve planeerimise protsess kasutades menüüd **Toimingud** . Eelarve planeerimise protsessi ei saa kasutada enne, kui see on aktiveeritud.

Menüüs **Toimingud** saate luua ka uue protsessi, kopeerides olemasoleva protsessi. See funktsioon on kasulik organisatsioonidele, mis järgivad igal eelarvetsüklil sama protsessivoogu ja teevad vähe muudatusi või mitte ühtegi muudatust.

Teine kasulik käsk menüüs **Tegevused** on **Kuva eelarve protsessi olekut**. See käsk kuvab graafiliselt protsessi eelarveplaanid koos asjakohaste andmetega, nagu plaanide töövoo olek, kokkuvõtted summa ja ühiku järgi ja ühe klõpsuga navigeerimise eelarveplaanidele.

[![Eelarve plaanimise protsessi olek](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
