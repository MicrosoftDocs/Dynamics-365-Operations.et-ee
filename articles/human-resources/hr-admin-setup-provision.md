---
title: Human Resources ettevalmistus
description: See artikkel selgitab uue tootmiskeskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Human Resources jaoks.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4f2fd2b7bf9f09a61d07e1bc35ad48fe2c5d7383
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138355"
---
# <a name="provision-human-resources"></a>Human Resources ettevalmistus

See artikkel selgitab uue tootmiskeskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Human Resources jaoks. See artikkel eeldab, et olete ostnud rakenduse Human Resources pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu. Kui teil on olemasolev Microsoft Dynamics 365 litsents, mis juba sisaldab rakenduse Human Resources teenuseplaani ja te ei saa selles artiklis olevaid etappe läbida, võtke ühendust toega.

Alustuseks peab üldadministraator sisse logima [Microsoft Dynamicsi teenusesse Lifecycle Services](https://lcs.dynamics.com) (LCS) ja looma uue Human Resourcesi projekti. Välja arvatud juhul, kui litsentsimisega seotud probleem takistab teil rakenduse Human Resources kasutuselevõtmist, pole klienditoe või Dynamicsi tehnikaosakonna meeskonna esindajate abi vaja.

## <a name="create-an-lcs-project"></a>LCS-i projekti loomine

Selleks, et kasutada oma rakenduse Human Resources keskkondade haldamiseks LCS-i, peate esmalt looma LCS-i projekti.

1. Logige [LCS-i](https://lcs.dynamics.com/Logon/Index) sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.

2. Valige projekti loomiseks plussmärk (**+**).

3. Valige toote nimeks ja versiooniks **Microsoft Dynamics 365 Human Resources**.

4. Valige **Dynamics 365 Human Resourcesi** metoodika.

5. Valige **Loo**.

Lisateavet selle kohta, kuidas rakenduse Human Resources kasutamist alustada, leiate **Human Resources**i metoodikast, mille lõite oma uues projektis. Kui olete projekti loomise lõpule viinud, viige oma Human Resourcesi keskkonna ettevalmistamiseks läbi järgmine protseduur.

## <a name="provision-a-human-resources-project"></a>Rakenduse Human Resources projekti ettevalmistamine

Pärast LCS-i projekti loomist saate Human Resourcesi ette valmistada keskkonnas.

1. Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.

2. Näidake, kas see on rakenduse Human Resources liivakasti- või toomiseksemplar. Liivakastieksemplaride puhul võivad varase tagasiside ja testimise jaoks saadaval olla eelvaatefunktsioonid.
   
    > [!NOTE]
    > Rakenduse Human Resources eksemplari tüüpi ei saa pärast määramist muuta. Enne jätkamist kontrollige, kas valitud on õige eksemplari tüüp.</br></br>
    > Rakenduse Human Resources eksemplari tüüp eraldi on Microsoft Power Appsi keskkonna eksemplari tüübist, mida seadistate Power Appsi halduskeskuses.
    
3. Kui soovite, et keskkonnas kasutataks sama demoandmete kogumit, mida kasutati Human Resourcesi proovikeskkonnas, siis valige suvand **Kaasa demoandmed**. See on kasulik pikaajalistes demo- või koolituskeskkondades, kuid seda ei tohiks kunagi tootmiskeskkondade jaoks kasutada.  Pange tähele, et see suvand tuleb valida algsel juurutusel. Hiljem ei saa olemasolevat juurutust värskendada.

4. Human Resources on alati ette valmistatud Microsoft Power Appsi keskkonnana, et lubada Power Appsi integreerimine ja laiendatavus. Enne jätkamist lugege selle artikli jaotist Power Appsi keskkonna valimine. Kui teil ei ole veel Power Appsi keskkonda, valige LCS-is Keskkondade haldamine või navigeerige Power Appsi halduskeskusesse. Seejärel järgige juhseid jaotises [Power Appsi keskkonna loomine](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Valige keskkond, kus Human Resources ette valmistada.

6. Valige **Jah**, et nõustuda tingimustega ja alustada juurutamist.

   Teie uus keskkond kuvatakse vasakul oleval navigeerimispaanil asuvas keskkondade loendis. Kuid te ei saa keskkonda kasutada enne, kui juurutuse olekuks on värskendatud **Juurutatud**. See protsess võtab tavaliselt paar minutit aega. Kui ettevalmistuse protsess ei õnnestu, peate võtma ühendust toega.

7. Valige oma uue keskkonna kasutamiseks suvand **Logi rakendusse Human Resources sisse**.

    > [!NOTE]
    > Kui te pole veel lõplikke nõudeid kinnitanud, saate projektis juurutada Human Resourcesi testeksemplari. Seejärel saate oma lahenduse testimiseks kuni kinnitamiseni kasutada seda testeksemplari. Kui kasutate oma uut keskkonda testimiseks, peate tootmiskeskkonna loomiseks seda protseduuri kordama.

    > Võite kaaluda tasuta 60-päevase [Human Resourcesi prooviversiooni keskkonna](https://dynamics.microsoft.com/talent/overview/) kasutamist. Kuigi proovikeskkonna omanikuks on kasutaja, kes seda taotles, saab sinna kutsuda teisi kasutajaid läbi rakenduse Human Resources süsteemiadministratsiooni kogemuse. Proovikeskkonnad sisaldavad fiktiivseid andmeid, mis võimaldavad programmiga turvaliselt tutvuda. Need pole mõeldud kasutamiseks tootmiskeskkonnana. Pange tähele, et proovikeskkonna aegumisel 60 päeva möödudes kustutatakse kõik selles sisalduvad andmed ning neid ei saa taastada. Pärast olemasoleva keskkonna aegumist saate registreerida uue proovikeskkonna kasutamisele.

## <a name="select-a-power-apps-environment"></a>Valige Power Appsi keskkond

Human Resourcesi ja Power Appsi keskkondade integratsioon võimaldab teil Human Resourcesi andmeid integreerida ja nende kasutust laiendada, kasutades Power Appsi tööriistu. Power Appsi keskkondade eesmärkide mõistmine aitab teil luua rakendusi Human Resourcesi laiendamiseks ja lihtsustab ka Human Resourcesi ettevalmistamisel õige keskkonna valimist. Teavet Power Appsi keskkondade, sh keskkonna ulatuse, keskkonnale juurdepääsu ning keskkonna loomise ja valimise kohta vaadake teemat [Tutvustame Power Appsi keskkondi](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Kasutage järgmisi juhiseid, kui otsustate, millisesse Power Appsi keskkonda rakendus Human Resources juurutada. 

1. LCS-is valige suvand **Keskkondade haldamine** või minge otse Power Appsi administreerimiskeskusse, kus saate vaadata olemasolevaid keskkondi ja luua uusi keskkondi.

2. Üks Human Resourcesi keskkond on vastendatud ühe Power Appsi keskkonnaga.

3. Power Appsi keskkond sisaldab rakendust Human Resources koos vastavate Power Appsi, Power Automate’i ja Common Data Service’i rakendustega. Kui Power Appsi keskkond kustutatakse, kustutatakse ka selles olevad rakendused. Rakenduse Human Resources keskkonna ettevalmistamisel saab ette valmistada kas **Prooviversiooni** või **Tootmise keskkonna**. Valige keskkonna tüüp keskkonna kasutamisel põhjal. 

4. Arvestada tuleks andmete integreerimis- ja testimisstrateegiatega, nagu liivakast, UAT või tootmine. Soovitame kaaluda juurutamise erinevaid mõjusid, kuna hiljem ei ole lihtne muuta, milline Human Resourcess keskkond Power Appsi keskkonnaga vastendatakse.

5. Järgmisi Power Appsi keskkondasid ei saa Human Resourcesi jaoks kasutada ja need filtreeritakse LCS-is valikuloendist välja.
 
    - **Power Appsi vaikekeskkonnad** – kuigi iga rentniku jaoks on automaatselt ette valmistatud Power Appsi vaikekeskkond, ei soovita me neid keskkondi rakenduses Human Resources kasutada, sest kõigil rentniku kasutajatel on juurdepääs Power Appsi keskkonnale ja nad võivad tahtmatult tootmisandmeid rikkuda, kui nad katsetavad ja tutvuvad Power Appsi või Power Automate’i integratsioonidega.
   
    - **Proovikeskkonnad** – need keskkonnad luuakse aegumisperioodiga, pärast mida need aeguvad, misjärel teie keskkond ja selles sisalduvad Human Resourcesi eksemplarid eemaldatakse automaatselt.
   
    - **Toetamata piirkonnad** – praegu toetatakse rakendust Human Resources ainult järgmistes piirkondades: Ameerika Ühendriigid, Euroopa, Ühendkuningriik, Austraalia, Kanada ja Aasia.

    > [!NOTE]
    > Human Resourcesi keskkond valmistatakse ette Power Appsi keskkonnaga samas piirkonnas. Human Resourcesi keskkonna migreerimist mõnda muusse piirkonda ei toetata.

6. Kui olete määratlenud kasutatava keskkonna, saate ettevalmistamise protsessiga jätkata. 
 
## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine

Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Rakenduse teistele kasutajatele tuleb juurdepääs anda eraldi. Juurdepääsu andmiseks tuleb Human Resourcesi keskkonnas lisada kasutajaid ja määrata neile sobivad rollid. Lähtestamise lõpetamiseks ja teistele rentiku kasutajatele juurdepääsu lubamiseks peaks Human Resourcesi keskkonna juurutanud üldadministraator käivitama ka mõlemad rakendused Attract ja Onboard.  Kuni seda pole tehtud, pole teistel kasutajatel juurdepääsu rakendustele Attract ja Onboard ning nad saavad juurdepääsuõiguste rikkumise tõrkeid. Lisateabe saamiseks vaadake teemasid [Uute kasutajate loomine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Kasutajate määramine turberollidesse](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
