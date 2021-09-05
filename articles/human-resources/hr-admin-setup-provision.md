---
title: Human Resourcesi ettevalmistus
description: See teema selgitab uue tootmiskeskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Human Resources jaoks.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5b0f04f27c95b2498ea2b5ad66c3df19bc8df0d9
ms.sourcegitcommit: 49f7528d3268abe15e40f719956e1ec8696a6f4e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/18/2021
ms.locfileid: "7393519"
---
# <a name="provision-human-resources"></a>Human Resourcesi ettevalmistus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

See teema selgitab uue tootmiskeskkonna ettevalmistamise protsessi rakenduse Microsoft Dynamics 365 Human Resources jaoks. 

## <a name="prerequisites"></a>Eeltingimused

Enne uue tootmiskeskkonna ettevalmistamise alustamist peavad olema täidetud järgmised eeltingimused:

- Olete inimressursse ostnud Cloud Solution Provider pakkuja (CSP) või ettevõtte arhitektuuri (EA) lepingu kaudu. Kui teil on olemasolev Microsoft Dynamics 365 litsents, mis juba sisaldab rakenduse Human Resources teenuseplaani ja te ei saa selles artiklis olevaid etappe läbida, võtke ühendust toega.

- Alustuseks peab üldadministraator sisse logima [Microsoft Dynamics`i teenusesse Lifecycle Services](https://lcs.dynamics.com) (LCS) ja looma uue Human Resourcesi projekti. 

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources proovikeskkonna ettevalmistamine

Enne oma esimese kausta või tootmiskeskkonna ressursi ressursiks saatmist võite soovida Human Resources funktsionaalsuse kinnitamiseks ette võtta [Human Resources proovikeskkonna](https://go.microsoft.com/fwlink/p/?LinkId=2115962). Proovikeskkonnad sisaldavad fiktiivseid andmeid, mis võimaldavad programmiga turvaliselt tutvuda. Kuigi proovikeskkonna omanikuks on kasutaja, kes seda taotles, saab sinna kutsuda teisi kasutajaid läbi rakenduse Human Resources süsteemiadministratsiooni kogemuse. 

Proovikeskkonnad pole mõeldud kasutamiseks tootmiskeskkonnana. Need on piiratud 60-päevase prooviajaga. Proovikeskkonna aegumisel keskkond ja kõik selle sisalduvad andmed kustutatakse ning neid ei saa taastada. Keskkonda ei saa teisendada kasti või tootmiskeskkonda. Pärast olemasoleva keskkonna aegumist saate registreerida uue proovikeskkonna kasutamisele.

## <a name="plan-human-resources-environments"></a>Human Resourcesi keskkondade plaanimine

Enne oma esimese Human Resourcesi keskkonna loomist peaksite hoolikalt planeerima keskkonna vajadused oma projekti jaoks. Human Resourcesi baastellimus sisaldab kahte keskkonda: töökeskkond ja liivakasti keskkond. Sõltuvalt teie projekti keerukusest võib teil projekti tegevuste toetamiseks olla vaja osta täiendavaid liivakastisekkondi. 

Kaalutlused täiendavatele keskkondadele:

- **Andmete migratsioon**: teil võib olla tarvis kaaluda andmete migreerimise tegevuste jaoks lisakeskkonda, et võimaldada liivakastikeskkonna testimiseks kasutamist kogu projekti vältel. Lisakeskkonna omamine võimaldab andmete migreerimise toimingute jätkumist testimisega ja konfigureerimisega samaaegselt teises keskkonnas.
- **Integratsioon**: täiendavaid keskkondi peaksite kaaluma testintegreerimiste konfigureerimiseks. See võib hõlmata põhiintegratsioone, nagu Ceridan Dayforce LinkedIn Anne'i talendikeskuse integratsioonid, või kohandatud integratsioonid, nagu palgaarvestuse, kandidaadi jälgimissüsteemide või soodustussüsteemide ja pakkujate integratsioonid.
- **Koolitus**: teil võib olla vaja eraldi keskkonda, mis on konfigureeritud koolitusandmete komplektiga, et koolitada oma töötajaid uut süsteemi kasutama. 
- **Mitmefaasiline projekt**: teil võib täiendavad keskkonna olla vaja konfiguratsiooni, andmete migratsiooni, testimise või muude tegevuste jaoks projektifaasis, mis on planeeritud pärast esialgset projekti käivitamist.

 > [!IMPORTANT]
 > Keskkonda arvesse kandes soovitame:
 > - Kasutage oma tootmiskeskkonda kogu projekti vältel GOLD -i konfiguratsioonikeskkonnana. See on oluline, kuna te ei saa liivakastikeskkonda töökeskkonda kopeerida. Seetõttu on käivitamisel teie GOLD-keskkond teie töökeskkonnaks ja viite oma üleminekutegevused lõpule selles keskkonnas.</br></br>
 > - Me soovitame kasutada oma liivakasti või muud keskkonda ülemineku mudeldamiseks enne tegelikku kasutuselevõttu. Seda saate teha, kui värskendate oma KULD-konfiguratsiooniga töökeskkonda oma liivakastikeskkonda.</br></br>
 > - Soovitame pidada üksikasjalikku ülemineku kontroll-loendit, mis sisaldab kõiki andmepakette, mida on vaja lõppandmete migreerimiseks töökeskkonda kasutuselevõtuks ülemineku ajal.</br></br>
 > - Kasutage TEST -keskkonnana kogu projekti vältel oma liivakasti keskkonda. Kui vajate täiendavaid keskkondi, saab teie organisatsioon neid lisatasu eest osta.</br></br>

## <a name="create-an-lcs-project"></a>LCS-i projekti loomine

Selleks, et kasutada oma rakenduse Human Resources keskkondade haldamiseks LCS-i, peate esmalt looma LCS-i projekti.

1. Logige [LCS-i](https://lcs.dynamics.com/Logon/Index) sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks.

   > [!NOTE]
   > Eduka ressursimääramise tagamiseks peab konto, mida kasutate Inimressursside keskkonna kasutamiseks, olema määratud kas **süsteemiadministraatori** või **süsteemi kohandaja** rollile Power Apps keskkonnas, mis on seotud inimressursside keskkonnaga. Lisateavet kasutajatele turvarollide määramise kohta vaadake jaotisest [kasutajate turberollide konfigureerimise kohta](/power-platform/admin/database-security) Power Platform-s.

2. Valige projekti loomiseks plussmärk (**+**).

3. Valige toote nimeks ja versiooniks **Microsoft Dynamics 365 Human Resources**.

4. Valige **Dynamics 365 Human Resourcesi** metoodika.

5. Valige **Loo**.

Lisateavet selle kohta, kuidas rakenduse Human Resources kasutamist alustada, leiate **Human Resources** i metoodikast, mille lõite oma uues projektis. Kui olete projekti loomise lõpule viinud, viige oma Human Resourcesi keskkonna ettevalmistamiseks läbi järgmine protseduur.

## <a name="provision-a-human-resources-project"></a>Rakenduse Human Resources projekti ettevalmistamine

Pärast LCS-i projekti loomist saate Human Resourcesi ette valmistada keskkonnas.

1. Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.

2. Näidake, kas see keskkond on rakenduse Human Resources liivakasti- või tootmiseksemplar. Liivakastieksemplaride puhul võivad varase tagasiside ja testimise jaoks saadaval olla eelvaatefunktsioonid.
   
    > [!NOTE]
    > Rakenduse Human Resources eksemplari tüüpi ei saa pärast määramist muuta. Enne jätkamist kontrollige, kas valitud on õige eksemplari tüüp.</br></br>
    > Rakenduse Human Resources eksemplari tüüp eraldi on Microsoft Power Appsi keskkonna eksemplari tüübist, mida seadistate Power Appsi halduskeskuses.
    
3. Kui soovite, et keskkonnas kasutataks sama demoandmete kogumit, mida kasutati Human Resourcesi proovikeskkonnas, siis valige suvand **Kaasa demoandmed**. Demoandmed on kasulikud pikaajalistes demo- või koolituskeskkondades, kuid neid ei tohiks kunagi tootmiskeskkondade jaoks kasutada. See suvand tuleb valida algsel juurutusel. Hiljem ei saa te olemasolevat juurutust värskendada.

4. Human Resources on alati ette valmistatud Microsoft Power Appsi keskkonnana, et lubada Power Appsi integreerimine ja laiendatavus. Enne jätkamist lugege selle artikli jaotist Power Appsi keskkonna valimine. Kui teil ei ole veel Power Appsi keskkonda, valige LCS-is Keskkondade haldamine või navigeerige Power Appsi halduskeskusesse. Seejärel järgige juhseid jaotises [Power Appsi keskkonna loomine](/powerapps/administrator/create-environment).

5. Valige keskkond, kus Human Resources ette valmistada.

6. Valige **Jah**, et nõustuda tingimustega ja alustada juurutamist.

   Teie uus keskkond kuvatakse vasakul oleval navigeerimispaanil asuvas keskkondade loendis. Kuid te ei saa keskkonda kasutada enne, kui juurutuse olekuks on värskendatud **Juurutatud**. See protsess võtab tavaliselt paar minutit aega. Kui ettevalmistuse protsess ei õnnestu, peate võtma ühendust toega.

7. Valige oma uue keskkonna kasutamiseks suvand **Logi rakendusse Human Resources sisse**.

    > [!NOTE]
    > Kui te pole veel lõplikke nõudeid kinnitanud, saate projektis juurutada Human Resourcesi testeksemplari. Seejärel saate oma lahenduse testimiseks kuni kinnitamiseni kasutada seda testeksemplari. Kui kasutate oma uut keskkonda testimiseks, peate tootmiskeskkonna loomiseks seda protseduuri kordama.

## <a name="select-a-power-apps-environment"></a>Valige Power Appsi keskkond

Rakenduse Power Apps tööriistade abil saate te rakenduse Human Resources andmeid integreerida ja nende kasutamist pikendada. Teavet Power Appsi keskkondade, sh keskkonna ulatuse, keskkonnale juurdepääsu ning keskkonna loomise ja valimise kohta vaadake teemat [Tutvustame Power Appsi keskkondi](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Kasutage järgmisi juhiseid, kui otsustate, millisesse Power Appsi keskkonda rakendus Human Resources juurutada. 

1. Valige LCS-is **Keskkondade haldamine**. Samuti saate minna otse rakenduse Power Apps halduskeskusesse, kus saate vaadata olemasolevaid keskkondi ja luua uusi.

2. Üks Human Resourcesi keskkond on vastendatud ühe Power Appsi keskkonnaga.

3. Power Appsi keskkond sisaldab rakendust Human Resources koos vastavate Power Appsi, Power Automate’i ja Dataverse’i rakendustega. Kui Power Appsi keskkond kustutatakse, kustutatakse ka selles olevad rakendused. Rakenduse Human Resources keskkonna ettevalmistamisel saab ette valmistada kas **Prooviversiooni** või **Tootmise keskkonna**. Valige keskkonna tüüp keskkonna kasutamisel põhjal. 

4. Arvestada tuleks andmete integreerimis- ja testimisstrateegiatega, nagu liivakast, UAT või tootmine. Soovitame hoolikalt kaaluda juurutamise mõju, kuna hiljem ei ole lihtne muuta, milline rakenduse Human Resources keskkond Power Appsi keskkonnaga vastendatakse.

5. Te ei saa kasutada rakenduse Human Resources jaoks järgmisi Power Apps`i keskkondi. Need filtreeritakse LCS-is valikuloendist.
 
    - **Power Appsi vaikekeskkonnad** – kuigi iga rentniku jaoks on automaatselt ette valmistatud Power Appsi vaikekeskkond, ei soovita me neid rakenduses Human Resources kasutada. Kõik rentniku kasutajad pääsevad Power Appsi keskkonnale ligi ja võivad tahtmatult tootmisandmeid rikkuda, kui nad katsetavad Power Appsi või Power Automate'i integratsioone või tutvuvad nendega.
   
    - **Testimiskeskkonnad** – need keskkonnad luuakse aegumiskuupäevaga. Pärast aegumist eemaldatakse teie keskkond ja kõik selles olevad rakenduse Human Resources eksemplarid automaatselt.
   
    - **Toetuseta geograafiline asukoht** - keskkond peab olema toetatud geograafiline asukoht. Lisateavet leiate artiklist [Toetatud geograafiad](hr-admin-setup-provision.md#supported-geographies).

6. Kui olete määratlenud kasutatava keskkonna, saate ettevalmistamise protsessiga jätkata. 

### <a name="supported-geographies"></a>Toetatud geograafilised graafikud

Rakendus Human Resources toetab praegu järgmisi geograafiline graafikuid:

- Ameerika Ühendriigid
- Euroopa
- Ühendkuningriik
- Austraalia
- Kanada
- Aasia 

Inimressursside keskkonna loomisel valite keskkonna, Power Apps mida siduda Inimressursside keskkonnaga. Inimressursside keskkond on siis ette valmistatud samas Azure'i geograafias kui valitud Power Apps keskkonnas. Inimressursside keskkonna ja andmebaasi füüsilise asukoha valimiseks valige geograafia inimressursside keskkonnaga seostatud Power Apps loetelu loomisel.

Te saate valida Azure'i  *geograafia*, kus keskkond on ette valmistatud, kuid te ei saa valida konkreetset Azure'i *regiooni*. Automatiseerimine määrab konkreetse regiooni geograafilises piirkonnas, kus keskkond on loodud koormuse tasakaalustamise ja jõudluse optimeerimiseks. Teavet Azure'i geograafiliste piirkondade ja Azure'i regioonide kohta leiate [Azure'i geograafiliste piirkondade](https://azure.microsoft.com/global-infrastructure/geographies) dokumentatsioonist.

Inimressursside keskkonna andmed sisalduvad alati Azure'i geograafilises piirkonnas, kus see luuakse. Ent see ei sisaldu alati samas Azure'i regioonis. Avariijärgse taaste konfiguratsioon otstarbel kopeeritakse andmed nii esmases Azure'i regioonis kui teiseses tõrkesiirde regioonis geograafias.

 > [!NOTE]
 > Inimressursside keskkonna migreerimist mõnda muusse Azure'i georgaafilisse piirkonda ei toetata.

## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine

Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Te peate rakenduse teistele kasutajatele konkreetselt juurdepääsu andma. Te peate rakenduse Human Resources keskkonnas kasutajad lisama ja neile sobivad rollid määrama. Lisateabe saamiseks vaadake teemasid [Uute kasutajate loomine](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ja [Kasutajate määramine turberollidesse](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
