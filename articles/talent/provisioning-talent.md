---
title: Rakenduse Microsoft Dynamics 365 for Talent ettevalmistamine
description: See teema selgitab uue keskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 for Talent jaoks.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 343e372ad9e29372649e975a5bee16e8913b66c8
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Rakenduse Microsoft Dynamics 365 for Talent ettevalmistamine

[!include [banner](includes/banner.md)]

See teema selgitab uue tootmiskeskkonna ettevalmistuse protsessi rakenduse Microsoft Dynamics 365 for Talent jaoks. See teema eeldab, et olete ostnud rakenduse Talent pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuur (AE) kaudu. Kui teil on lahenduse Microsoft Dynamics 365 litsents, mis juba sisaldab rakenduse Talent teenuseplaani ja te ei saa selles teemas olevaid etappe läbida, võtke ühendust toega.

Alustuseks peab üldadministraator [Microsoft Dynamicsi teenusesse Lifecycle Services](http://lcs.dynamics.com) (LCS) sisse logima ja looma uue Talenti projekti. Välja arvatud juhul, kui litsentsimisega seotud probleem takistab teil Talenti kasutuselevõtmist, pole klienditoe või Dynamicsi tehnikaosakonna meeskonna esindajate abi vaja.

## <a name="create-an-lcs-project"></a>LCS-i projekti loomine
Selleks, et kasutada oma Talenti keskkondade haldamiseks LCS-i, peate esmalt looma LCS-i projekti.

1. Logige [LCS-i](https://lcs.dynamics.com/Logon/Index) sisse, kasutades kontot, mida kasutasite Talenti tellimiseks.
2. Valige projekti loomiseks plussmärk (**+**).
3. Valige toote nimeks ja versiooniks **Microsoft Dynamics 365 for Talent**.
4. Valige metoodika **Dynamics 365 for Talent**.
5. Valige **Loo**.

Lisateavet selle kohta, kuidas Talenti kasutamist alustada, leiate **Talent**i metoodikast, mille lõite oma uues projektis. Kui olete projekti loomise lõpule viinud, viige oma Talenti keskkonna ettevalmistamiseks läbi järgmine protseduur.

## <a name="provision-a-talent-project"></a>Talenti projekti ettevalmistamine
Pärast LCS-i projekti loomist saate Talenti ette valmistada keskkonnas.

1. Valige oma LCS-i projektis paan **Talenti rakendusehaldus**.
2. Talent on alati ette valmistatud Microsoft PowerAppsi keskkonnana, et lubada PowerAppsi integreerimine ja laiendatavus. Enne jätkamist lugege selle teema jaotist „PowerAppsi keskkonna valimine”. 
3. Kui teil pole veel PowerAppsi keskkonda, järgige enne jätkamist selle teema jaotises „Uue PowerAppsi keskkonna loomine (vajaduse korral)” olevaid etappe.

    > [!NOTE]
    > Olemasolevate keskkondade vaatamiseks või uute keskkondade loomiseks peab Talenti ettevalmistavale rentnikuadministraatorile olema määratud PowerApps P2 litsents. Kui teie organisatsioonil ei ole PowerApps P2 litsentsi, saate selle oma CSP-lt või [PowerAppsi hinnakujunduse lehelt](https://powerapps.microsoft.com/en-us/pricing/).

4. Valige **Lisa** ja seejärel valige keskkond, milles Talenti ette valmistada.
5. Kui soovite, et keskkonnas kasutataks samu demoandmete kogumit, mida kasutati Talenti proovikeskkonnas, siis valige suvand Kaasa demoandmed.  See on kasulik pikaajalistes demo- või koolituskeskkondades, kuid seda ei tohiks kunagi tootmiskeskkondade jaoks kasutada.  Pange tähele, et see suvand tuleb valida algsel juurutusel ja hiljem ei saa olemasolevat juurutust värskendada.
6. Valige **Jah**, et nõustuda tingimustega ja alustada juurutamist.

    Teie uus keskkond kuvatakse vasakul oleval navigeerimispaanil asuvas keskkondade loendis. Kuid te ei saa keskkonda kasutada enne, kui juurutuse olekuks on värskendatud **Juurutatud**. See protsess võtab tavaliselt paar minutit aega. Kui ettevalmistuse protsess ei õnnestu, peate võtma ühendust toega.

7. Valige oma uue keskkonna kasutamiseks suvand **Logi Talentisse sisse**.

> [!NOTE]
> Kui te pole veel lõplikke nõudeid kinnitanud, saate projektis juurutada Talenti testeksemplari. Seejärel saate oma lahenduse testimiseks kuni kinnitamiseni kasutada seda testeksemplari. Kui kasutate oma uut keskkonda testimiseks, peate tootmiskeskkonna loomiseks seda protseduuri kordama.

> [!NOTE]
> Kuna Talendi kordustellimuse puhul on lubatud ainult kaks LCS-i keskkonda, võite kaaluda ka tasuta 60-päevase [Talenti proovikeskkonna](https://dynamics.microsoft.com/en-us/talent/overview/) kasutamist. Kuigi proovikeskkonna omanikuks on kasutaja, kes seda taotles, saab sinna kutsuda teisi kasutajaid läbi Core HR-i süsteemiadministratsiooni kogemuse. Proovikeskkonnad sisaldavad fiktiivseid andmeid, mis võimaldavad programmiga turvaliselt tutvuda. Need pole mõeldud kasutamiseks tootmiskeskkonnana. Pange tähele, et proovikeskkonna aegumisel 60 päeva möödudes kustutatakse kõik selles sisalduvad andmed ning neid ei saa taastada. Pärast olemasoleva keskkonna aegumist saate registreerida uue proovikeskkonna kasutamisele.

## <a name="select-a-powerapps-environment"></a>PowerAppsi keskkonna valimine

Talenti ja PowerAppsi keskkondade integratsioon võimaldab teil Talenti andmeid integreerida ja nende kasutust laiendada, kasutades PowerAppsi tööriistu. PowerAppsi keskkondade eesmärkide mõistmine aitab teil luua rakendusi Talenti laiendamiseks ja võib lihtsustada ka Talenti ettevalmistamisel õige keskkonna valimist. Teavet PowerAppsi keskkondade, sh keskkonna ulatuse, keskkonnale juurdepääsu ning keskkonna loomise ja valimise kohta vaadaketeemat [Tutvustame PowerAppsi keskkondi](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Kasutage järgmisi juhiseid, kui otsustate, millisesse PowerAppsi keskkonda Talenti juurutada. 
1. LCS-is valige suvand Keskkondade haldamine või minge otse PowerAppsi administreerimiskeskusse, kus saate vaadata olemasolevaid keskkondi ja luua uusi keskkondi.
2. Üks Talenti keskkond on vastendatud ühe PowerAppsi keskkonnaga.
3. PowerAppsi keskkond sisaldab Talenti rakendust koos vastavate PowerAppsi, Flow ja CDS-i rakendustega. Kui PowerAppsi keskkond kustutatakse, kustutatakse ka selles olevad rakendused.
4. Arvestada tuleks andmete integreerimis- ja testimisstrateegiatega, näiteks: liivakast, UAT, tootmine. Seetõttu soovitame kaaluda juurutamise erinevaid mõjusid, kuna hiljem ei ole lihtne muuta, milline Talenti keskkond PowerAppsi keskkonnaga vastendatakse.
5. Järgmisi PowerAppsi keskkondasid ei saa Talenti jaoks kasutada ja need filtreeritakse LCS-is valikuloendist välja.
 
    **CDS 2.0 keskkonnad** CDS 2.0 on avalikult saadaval alates 21. märtsist 2018; kuid Talent ei toeta veel versiooni CDS 2.0. Saate PowerAppsi halduskeskuses vaadata ja luua CDS 2.0 andmebaase, kuid neid ei saa Talentis kasutada. Võimalus kasutada CDS 2.0 keskkondi Talenti juurutustes on saadaval edaspidi.
   
   > [!Note]
   > Administreerimisportaalis CDS 1.0 ja 2.0 keskkondade eristamiseks valige keskkond ja vaadake selle **üksikasju**. Kõik CDS 2.0 keskkonnad viitavad asjaolule, et „Saate neid sätteid hallata rakenduse Dynamics 365 halduskeskuses”, osutavad eksemplari versioonile ning neil puudub vahekaart Andmebaas. 
 
   **PowerAppsi vaikekeskkonnad** Kuigi iga rentniku jaoks on automaatselt ette valmistatud PowerAppsi vaikekeskkond, ei soovita me neid keskkondi Talentis kasutada, sest kõigil rentniku kasutajatel on juurdepääs PowerAppsi keskkonnale ja nad võivad tahtmatult tootmisandmeid rikkuda, kui nad katsetavad ja tutvuvad PowerAppsi või Flow integratsioonidega.
   
   <strong>Proovikeskkonnad</strong> Keskkonnad nimega, nagu „TestDrive – alias@domain” luuakse 60-päevase aegumisperioodiga, pärast mida need aeguvad ja teie keskkond eemaldatakse automaatselt.
   
   **Toetamata piirkonnad** Praegu toetatakse Talentit ainult järgmistes piirkondades: Ameerika Ühendriigid, Euroopa või Austraalia.
  
6. Kui olete määratlenud kasutatava keskkonna, ei saa ühtegi konkreetset tegevust enam teha. Jätkake ettevalmistamise protsessi. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Uue PowerAppsi keskkonna loomine (vajaduse korral)

Käivitage PowerShelli skript, et luua Talenti jaoks uus PowerAppsi keskkond, eeldusel, et rentniku administraatoril on PowerAppsi plaani 2 litsents. Skript automatiseerib järgmised sammud:


 + PowerAppsi keskkonna loomine;
 + CDS 1.0 andmebaasi loomine;
 + CDS 1.0 andmebaasi näidisandmete kustutamine.


Skripti käivitamiseks tehke järgmist.

1. Laadige järgmisest asukohast alla fail ProvisionCDSEnvironment.zip: [ProvisionCDSEnvironmenti skriptid](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Paremklõpsake allalaadimise kaustas äsja allalaaditud faili ProvisionCDSEnvironment.zip ja valige **Atribuudid**.  Kui dialoogi allosas on turvamärge „See fail on pärit teisest arvutist ja võib olla arvuti kaitsmiseks blokeeritud”, märkige ruut **Tühista blokeerimine**, seejärel klõpsake valikut **Rakenda** ja siis **OK**.

3. Pakkige kogu faili ProvisionCDSEnviroinment.zip sisu lahti mõnda muusse kausta kui juurkaust.

4. Käivitage administraatorina programm Windows PowerShell või Windows PowerShell ISE.

   Vaadake teemat [Käivitamispoliitika häälestamine](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6), et saada lisateavet skriptide käitamist võimaldava käivitamispoliitika häälestamise kohta. Soovitame kasutada järgmist „Komplekt – ExecutionPolicy – ExecutionPolicy piiramatu – protsessi ulatus”, kuid veenduge, et järgiksite oma ettevõtte turbepoliitikaid ja sulgeksite lõpetamisel PowerShelli akna. 
  
5. PowerShellis liikuge kausta, kuhu pakkisite faili lahti, ja käivitage järgmine käsk, asendades väärtused, nagu on näidatud allpool.
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** tuleb asendada teie keskkonna nimega. See nimi kuvatakse LCS-is ja see on nähtav, kui kasutajad valivad, millist Talenti keskkonda kasutada. 

   **YourLocation** tuleb asendada ühega Talenti toetavatest piirkondadest: Ameerika Ühendriigid, Euroopa, Austraalia. 

   **-Verbose** on valikuline ja edastab üksikasjaliku teabe, mis saata probleemide ilmnemisel tugimeeskonnale.

6. Jätkake ettevalmistamise protsessi.
 

## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine
Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Rakenduse teistele kasutajatele tuleb juurdepääs anda eraldi. Juurdepääsu andmiseks tuleb Core HR-i keskkonnas [lisada kasutajaid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [määrata neile sobivad rollid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). Lähtestamise lõpetamiseks ja teistele rentiku kasutajatele juurdepääsu lubamiseks peaks Talenti keskkonna juurutanud üldadministraator käivitama ka mõlemad rakendused Attract ja Onboard.  Kuni seda pole tehtud, pole teistel kasutajatel juurdepääsu rakendustele Attract ja Onboard ning nad saavad juurdepääsuõiguste rikkumise tõrkeid.


