---
title: Human Resources ettevalmistus
description: See artikkel selgitab uue tootmiskeskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Human Resources jaoks.
author: andreabichsel
manager: AnnBe
ms.date: 04/23/2020
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
ms.openlocfilehash: 88a0be50a9b861190e7ce9b3f56bb4e583b791d1
ms.sourcegitcommit: 33685a5cc37081a189279e917def7f122d3beaef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/24/2020
ms.locfileid: "3285485"
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

2. Näidake, kas see keskkond on rakenduse Human Resources liivakasti- või tootmiseksemplar. Liivakastieksemplaride puhul võivad varase tagasiside ja testimise jaoks saadaval olla eelvaatefunktsioonid.
   
    > [!NOTE]
    > Rakenduse Human Resources eksemplari tüüpi ei saa pärast määramist muuta. Enne jätkamist kontrollige, kas valitud on õige eksemplari tüüp.</br></br>
    > Rakenduse Human Resources eksemplari tüüp eraldi on Microsoft Power Appsi keskkonna eksemplari tüübist, mida seadistate Power Appsi halduskeskuses.
    
3. Kui soovite, et keskkonnas kasutataks sama demoandmete kogumit, mida kasutati Human Resourcesi proovikeskkonnas, siis valige suvand **Kaasa demoandmed**. Demoandmed on kasulikud pikaajalistes demo- või koolituskeskkondades, kuid neid ei tohiks kunagi tootmiskeskkondade jaoks kasutada. See suvand tuleb valida algsel juurutusel. Hiljem ei saa te olemasolevat juurutust värskendada.

4. Human Resources on alati ette valmistatud Microsoft Power Appsi keskkonnana, et lubada Power Appsi integreerimine ja laiendatavus. Enne jätkamist lugege selle artikli jaotist Power Appsi keskkonna valimine. Kui teil ei ole veel Power Appsi keskkonda, valige LCS-is Keskkondade haldamine või navigeerige Power Appsi halduskeskusesse. Seejärel järgige juhseid jaotises [Power Appsi keskkonna loomine](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Valige keskkond, kus Human Resources ette valmistada.

6. Valige **Jah**, et nõustuda tingimustega ja alustada juurutamist.

   Teie uus keskkond kuvatakse vasakul oleval navigeerimispaanil asuvas keskkondade loendis. Kuid te ei saa keskkonda kasutada enne, kui juurutuse olekuks on värskendatud **Juurutatud**. See protsess võtab tavaliselt paar minutit aega. Kui ettevalmistuse protsess ei õnnestu, peate võtma ühendust toega.

7. Valige oma uue keskkonna kasutamiseks suvand **Logi rakendusse Human Resources sisse**.

    > [!NOTE]
    > Kui te pole veel lõplikke nõudeid kinnitanud, saate projektis juurutada Human Resourcesi testeksemplari. Seejärel saate oma lahenduse testimiseks kuni kinnitamiseni kasutada seda testeksemplari. Kui kasutate oma uut keskkonda testimiseks, peate tootmiskeskkonna loomiseks seda protseduuri kordama.

    > Võite kaaluda tasuta 60-päevase [Human Resourcesi prooviversiooni keskkonna](https://go.microsoft.com/fwlink/p/?LinkId=2115962) kasutamist. Kuigi proovikeskkonna omanikuks on kasutaja, kes seda taotles, saab sinna kutsuda teisi kasutajaid läbi rakenduse Human Resources süsteemiadministratsiooni kogemuse. Proovikeskkonnad sisaldavad fiktiivseid andmeid, mis võimaldavad programmiga turvaliselt tutvuda. Need pole mõeldud kasutamiseks tootmiskeskkonnana. Pange tähele, et proovikeskkonna aegumisel 60 päeva möödudes kustutatakse kõik selles sisalduvad andmed ning neid ei saa taastada. Pärast olemasoleva keskkonna aegumist saate registreerida uue proovikeskkonna kasutamisele.

## <a name="select-a-power-apps-environment"></a>Valige Power Appsi keskkond

Rakenduse Power Apps tööriistade abil saate te rakenduse Human Resources andmeid integreerida ja nende kasutamist pikendada. Teavet Power Appsi keskkondade, sh keskkonna ulatuse, keskkonnale juurdepääsu ning keskkonna loomise ja valimise kohta vaadake teemat [Tutvustame Power Appsi keskkondi](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Kasutage järgmisi juhiseid, kui otsustate, millisesse Power Appsi keskkonda rakendus Human Resources juurutada. 

1. Valige LCS-is **Keskkondade haldamine**. Samuti saate minna otse rakenduse Power Apps halduskeskusesse, kus saate vaadata olemasolevaid keskkondi ja luua uusi.

2. Üks Human Resourcesi keskkond on vastendatud ühe Power Appsi keskkonnaga.

3. Power Appsi keskkond sisaldab rakendust Human Resources koos vastavate Power Appsi, Power Automate’i ja Common Data Service’i rakendustega. Kui Power Appsi keskkond kustutatakse, kustutatakse ka selles olevad rakendused. Rakenduse Human Resources keskkonna ettevalmistamisel saab ette valmistada kas **Prooviversiooni** või **Tootmise keskkonna**. Valige keskkonna tüüp keskkonna kasutamisel põhjal. 

4. Arvestada tuleks andmete integreerimis- ja testimisstrateegiatega, nagu liivakast, UAT või tootmine. Soovitame hoolikalt kaaluda juurutamise mõju, kuna hiljem ei ole lihtne muuta, milline rakenduse Human Resources keskkond Power Appsi keskkonnaga vastendatakse.

5. Te ei saa kasutada rakenduse Human Resources jaoks järgmisi Power Appsi keskkondi. Need filtreeritakse LCS-is valikuloendist.
 
    - **Power Appsi vaikekeskkonnad** – kuigi iga rentniku jaoks on automaatselt ette valmistatud Power Appsi vaikekeskkond, ei soovita me neid rakenduses Human Resources kasutada. Kõik rentniku kasutajad pääsevad Power Appsi keskkonnale ligi ja võivad tahtmatult tootmisandmeid rikkuda, kui nad katsetavad Power Appsi või Power Automate'i integratsioone või tutvuvad nendega.
   
    - **Testimiskeskkonnad** – need keskkonnad luuakse aegumiskuupäevaga. Pärast aegumist eemaldatakse teie keskkond ja kõik selles olevad rakenduse Human Resources eksemplarid automaatselt.
   
    - **Toetamata piirkonnad** – praegu toetatakse rakendust Human Resources ainult järgmistes piirkondades: Ameerika Ühendriigid, Euroopa, Ühendkuningriik, Austraalia, Kanada ja Aasia.

    > [!NOTE]
    > Human Resourcesi keskkond valmistatakse ette Power Appsi keskkonnaga samas piirkonnas. Human Resourcesi keskkonna migreerimist mõnda muusse piirkonda ei toetata.

6. Kui olete määratlenud kasutatava keskkonna, saate ettevalmistamise protsessiga jätkata. 
 
## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine

Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Te peate rakenduse teistele kasutajatele konkreetselt juurdepääsu andma. Te peate rakenduse Human Resources keskkonnas kasutajad lisama ja neile sobivad rollid määrama. Lähtestamise lõpetamiseks ja teistele rentiku kasutajatele juurdepääsu lubamiseks peaks Human Resourcesi keskkonna juurutanud üldadministraator käivitama ka mõlemad rakendused Attract ja Onboard. Kuni seda pole tehtud, pole teistel kasutajatel juurdepääsu rakendustele Attract ja Onboard ning nad saavad juurdepääsuõiguste rikkumise tõrkeid. Lisateabe saamiseks vaadake teemasid [Uute kasutajate loomine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Kasutajate määramine turberollidesse](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
