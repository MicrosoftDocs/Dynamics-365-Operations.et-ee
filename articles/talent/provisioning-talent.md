---
title: Talenti ettevalmistamine
description: See teema selgitab uue keskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Talent jaoks.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d7c4a8174007384370ae320b3874e104c04b71a5
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124700"
---
# <a name="provision-talent"></a>Talenti ettevalmistamine

See teema selgitab uue tootmiskeskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Talent jaoks. See teema eeldab, et olete ostnud rakenduse Talent pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuur (AE) kaudu. Kui teil on lahenduse Microsoft Dynamics 365 litsents, mis juba sisaldab rakenduse Talent teenuseplaani ja te ei saa selles teemas olevaid etappe läbida, võtke ühendust toega.

Alustuseks peab üldadministraator sisse logima [Microsoft Dynamicsi teenusesse Lifecycle Services](https://lcs.dynamics.com) (LCS) ja looma uue Talenti projekti. Välja arvatud juhul, kui litsentsimisega seotud probleem takistab teil Talenti kasutuselevõtmist, pole klienditoe või Dynamicsi tehnikaosakonna meeskonna esindajate abi vaja.

## <a name="create-an-lcs-project"></a>LCS-i projekti loomine
Selleks, et kasutada oma Talenti keskkondade haldamiseks LCS-i, peate esmalt looma LCS-i projekti.

1. Logige [LCS-i](https://lcs.dynamics.com/Logon/Index) sisse, kasutades kontot, mida kasutasite Talenti tellimiseks.

2. Valige projekti loomiseks plussmärk (**+**).

3. Valige toote nimeks ja versiooniks **Microsoft Dynamics 365 Talent**.

4. Valige **Dynamics 365 Talenti** metoodika.

5. Valige **Loo**. 

Lisateavet selle kohta, kuidas Talenti kasutamist alustada, leiate **Talent**i metoodikast, mille lõite oma uues projektis. Kui olete projekti loomise lõpule viinud, viige oma Talenti keskkonna ettevalmistamiseks läbi järgmine protseduur.

## <a name="provision-a-talent-project"></a>Talenti projekti ettevalmistamine

Pärast LCS-i projekti loomist saate Talenti ette valmistada keskkonnas.

1. Valige oma LCS-i projektis paan **Talenti rakendusehaldus**.

2. Näidake, kas see on Talenti liivakasti- või tootmiseksemplar. Liivakastieksemplaride puhul võivad varase tagasiside ja testimise jaoks saadaval olla eelvaatefunktsioonid. 

    > [!NOTE]
    > Talenti eksemplari tüüpi ei saa pärast määramist muuta. Enne jätkamist kontrollige, kas valitud on õige eksemplari tüüp.

    > [!NOTE]
    > Talenti eksemplari tüüp on eraldi Microsoft Power Apps keskkonnas eksemplari tüübist, mida seate Power Apps halduskeskuses.

3. Kui soovite, et keskkonnas kasutataks samu demoandmete kogumit, mida kasutati Talenti proovikeskkonnas, siis valige suvand **Kaasa demoandmed**. See on kasulik pikaajalistes demo- või koolituskeskkondades, kuid seda ei tohiks kunagi tootmiskeskkondade jaoks kasutada.  Pange tähele, et see suvand tuleb valida algsel juurutusel. Hiljem ei saa olemasolevat juurutust värskendada.

4. Talent on alati ette valmistatud Microsoft Power Appsi keskkonnana, et lubada Power Appsi integreerimine ja laiendatavus. Enne jätkamist lugege selle teema jaotist Power Appsi keskkonna valimine. Kui teil ei ole veel Power Appsi keskkonda, valige LCS-is Keskkondade haldamine või navigeerige Power Appsi halduskeskusesse. Seejärel järgige juhseid jaotises [Power Appsi keskkonna loomine](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Valige keskkond, kus Talenti ette valmistada.

6. Valige **Jah**, et nõustuda tingimustega ja alustada juurutamist.

    Teie uus keskkond kuvatakse vasakul oleval navigeerimispaanil asuvas keskkondade loendis. Kuid te ei saa keskkonda kasutada enne, kui juurutuse olekuks on värskendatud **Juurutatud**. See protsess võtab tavaliselt paar minutit aega. Kui ettevalmistuse protsess ei õnnestu, peate võtma ühendust toega.

7. Valige oma uue keskkonna kasutamiseks suvand **Logi Talentisse sisse**.

    > [!NOTE]
    > Kui te pole veel lõplikke nõudeid kinnitanud, saate projektis juurutada Talenti testeksemplari. Seejärel saate oma lahenduse testimiseks kuni kinnitamiseni kasutada seda testeksemplari. Kui kasutate oma uut keskkonda testimiseks, peate tootmiskeskkonna loomiseks seda protseduuri kordama.

    > Kuna Talendi kordustellimuse puhul on lubatud ainult kaks LCS-i keskkonda, võite kaaluda tasuta 60-päevase [Talenti proovikeskkonna](https://dynamics.microsoft.com/talent/overview/) kasutamist. Kuigi proovikeskkonna omanikuks on kasutaja, kes seda taotles, saab sinna kutsuda teisi kasutajaid läbi rakenduse Human Resources süsteemiadministratsiooni kogemuse. Proovikeskkonnad sisaldavad fiktiivseid andmeid, mis võimaldavad programmiga turvaliselt tutvuda. Need pole mõeldud kasutamiseks tootmiskeskkonnana. Pange tähele, et proovikeskkonna aegumisel 60 päeva möödudes kustutatakse kõik selles sisalduvad andmed ning neid ei saa taastada. Pärast olemasoleva keskkonna aegumist saate registreerida uue proovikeskkonna kasutamisele.

## <a name="select-a-power-apps-environment"></a>Valige Power Appsi keskkond

Talenti ja Power Appsi keskkondade integratsioon võimaldab teil Talenti andmeid integreerida ja nende kasutust laiendada, kasutades Power Appsi tööriistu. Power Appsi keskkondade eesmärkide mõistmine aitab teil luua rakendusi Talenti laiendamiseks ja lihtsustab ka Talenti ettevalmistamisel õige keskkonna valimist. Teavet Power Appsi keskkondade, sh keskkonna ulatuse, keskkonnale juurdepääsu ning keskkonna loomise ja valimise kohta vaadake teemat [Tutvustame Power Appsi keskkondi](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Kasutage järgmisi juhiseid, kui otsustate, millisesse Power Appsi keskkonda Talenti juurutada. 

1. LCS-is valige suvand **Keskkondade haldamine** või minge otse Power Appsi administreerimiskeskusse, kus saate vaadata olemasolevaid keskkondi ja luua uusi keskkondi.

2. Üks Talenti keskkond on vastendatud ühe Power Appsi keskkonnaga.

3. Power Appsi keskkond sisaldab Talenti rakendust koos vastavate Power Appsi, Power Automate’i ja Common Data Service’i rakendustega. Kui Power Appsi keskkond kustutatakse, kustutatakse ka selles olevad rakendused. Talenti keskkonna ettevalmistamisel saab ette valmistada kas **Prooviversiooni** või **Tootmise keskkonna**. Valige keskkonna tüüp keskkonna kasutamisel põhjal. 

4. Arvestada tuleks andmete integreerimis- ja testimisstrateegiatega, nagu liivakast, UAT või tootmine. Soovitame kaaluda juurutamise erinevaid mõjusid, kuna hiljem ei ole lihtne muuta, milline Talenti keskkond Power Appsi keskkonnaga vastendatakse.

5. Järgmisi Power Appsi keskkondasid ei saa Talenti jaoks kasutada ja need filtreeritakse LCS-is valikuloendist välja.
 
    - **Power Appsi vaikekeskkonnad** – kuigi iga rentniku jaoks on automaatselt ette valmistatud Power Appsi vaikekeskkond, ei soovita me neid keskkondi Talentis kasutada, sest kõigil rentniku kasutajatel on juurdepääs Power Appsi keskkonnale ja nad võivad tahtmatult tootmisandmeid rikkuda, kui nad katsetavad ja tutvuvad Power Appsi või Power Automate’i integratsioonidega.
   
    - **Proovikeskkonnad** – need keskkonnad luuakse aegumisperioodiga, pärast mida need aeguvad, misjärel teie keskkond ja selles sisalduvad Talenti eksemplarid eemaldatakse automaatselt.
   
    - **Toetamata piirkonnad** – praegu toetatakse Talenti ainult järgmistes piirkondades: Ameerika Ühendriigid, Euroopa, Ühendkuningriik, Austraalia, Kanada ja Aasia.
  
6. Kui olete määratlenud kasutatava keskkonna, saate ettevalmistamise protsessiga jätkata. 
 
## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine

Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Rakenduse teistele kasutajatele tuleb juurdepääs anda eraldi. Juurdepääsu andmiseks tuleb Human Resourcesi keskkonnas lisada kasutajaid ja määrata neile sobivad rollid. Lähtestamise lõpetamiseks ja teistele rentiku kasutajatele juurdepääsu lubamiseks peaks Talenti keskkonna juurutanud üldadministraator käivitama ka mõlemad rakendused Attract ja Onboard.  Kuni seda pole tehtud, pole teistel kasutajatel juurdepääsu rakendustele Attract ja Onboard ning nad saavad juurdepääsuõiguste rikkumise tõrkeid. Lisateabe saamiseks vaadake teemasid [Uute kasutajate loomine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Kasutajate määramine turberollidesse](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
