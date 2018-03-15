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
ms.sourcegitcommit: 8b59ea6a2ac8c1c4e5df6e251fa3390639ff3f30
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: et-ee
ms.lasthandoff: 03/02/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Rakenduse Microsoft Dynamics 365 for Talent ettevalmistamine

[!include[banner](includes/banner.md)]

[!include[banner](includes/banner.md)]

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
2. Talent on alati ette valmistatud Microsoft PowerAppsi keskkonnana, et lubada PowerAppsi integreerimine ja laiendatavus. Kui teil pole veel PowerAppsi keskkonda, järgige enne jätkamist selle teema jaotises „Uue PowerAppsi keskkonna loomine (vajaduse korral)” olevaid etappe.

    > [!NOTE]
    > Olemasolevate keskkondade vaatamiseks või uute keskkondade loomiseks peab Talenti ettevalmistavale rentnikuadministraatorile olema määratud PowerApps P2 litsents. Kui teie organisatsioonil ei ole PowerApps P2 litsentsi, saate selle oma CSP-lt või [PowerAppsi hinnakujunduse lehelt](https://powerapps.microsoft.com/en-us/pricing/).

3. Valige **Lisa** ja seejärel valige keskkond, milles Talenti ette valmistada.
4. Valige **Jah**, et nõustuda tingimustega ja alustada juurutamist.

    Teie uus keskkond kuvatakse vasakul oleval navigeerimispaanil asuvas keskkondade loendis. Kuid te ei saa keskkonda kasutada enne, kui juurutuse olekuks on värskendatud **Juurutatud**. See protsess võtab tavaliselt paar minutit aega. Kui ettevalmistuse protsess ei õnnestu, peate võtma ühendust toega.

6. Valige oma uue keskkonna kasutamiseks suvand **Logi Talentisse sisse**.

> [!NOTE]
> Kui te pole veel lõplikke nõudeid kinnitanud, saate projektis juurutada Talenti testeksemplari. Seejärel saate oma lahenduse testimiseks kuni kinnitamiseni kasutada seda testeksemplari. Kui kasutate oma uut keskkonda testimiseks, peate tootmiskeskkonna loomiseks seda protseduuri kordama.

> [!NOTE]
> Talenti keskkonnad, mille ettevalmistus toimub läbi LCS-i, ei sisalda demoandmed, mis on konfigureeritud inimressursside tegevustele või mis on Talentile omased. Kui vajate demoandmed sisaldavat keskkonda, on soovitatav registreerida tasuta 60-päevasele [Talenti proovikeskkonna](https://dynamics.microsoft.com/en-us/talent/overview/) kasutamisele. Kuigi proovikeskkonna omanikuks on kasutaja, kes seda taotles, saab sinna kutsuda teisi kasutajaid läbi Core HR-i süsteemiadministratsiooni kogemuse. Proovikeskkonnad sisaldavad fiktiivseid andmeid, mis võimaldavad programmiga turvaliselt tutvuda. Need pole mõeldud kasutamiseks tootmiskeskkonnana. Pange tähele, et proovikeskkonna aegumisel 60 päeva möödudes kustutatakse kõik selles sisalduvad andmed ning neid ei saa taastada. Pärast olemasoleva keskkonna aegumist saate registreerida uue proovikeskkonna kasutamisele.

## <a name="create-a-new-powerapps-environment-if-required"></a>Uue PowerAppsi keskkonna loomine (vajaduse korral)
Talenti ja PowerAppsi keskkondade integratsioon võimaldab teil Talenti andmeid integreerida ja nende kasutust laiendada, kasutades PowerAppsi tööriistu. PowerAppsi keskkondade eesmärgi mõistmine aitab teil luua rakendusi, mis vastavad teie Talenti laiendamise vajadustele. Teavet PowerAppsi keskkondade, sh keskkonna ulatuse, keskkonnale juurdepääsu ning keskkonna loomise ja valimise kohta vaadaketeemat [Tutvustame PowerAppsi keskkondi](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Kuigi iga rentnik on automaatselt ettevalmistatud PowerAppsi vaikekeskkonnas, ei pruugi see olla Talenti juurutamise jaoks parim keskkond. Selle etapi puhul tuleks arvestada andmete integreerimis- ja testimisstrateegiatega, mistõttu soovitame kaaluda juurutamist mõjutavaid tegureid, kuna mõndasid otsuseid ei ole hiljem lihtne muuta. 

Kuigi iga rentnik on automaatselt ettevalmistatud PowerAppsi vaikekeskkonnas, ei pruugi see olla Talenti juurutamise jaoks parim keskkond. Selle etapi puhul tuleks arvestada andmete integreerimis- ja testimisstrateegiatega. Seetõttu soovitame kaaluda juurutamise erinevaid mõjusid, kuna PowerAppsi keskkonda ei ole hiljem lihtne muuta.

1. Valige LCS-is **Keskkondade haldamine**. Teid suunatakse [PowerAppsi administreerimiskeskusse](https://preview.admin.powerapps.com/environments), kus saate vaadata olemasolevaid keskkondi ja luua uusi keskkondi.
2. Valige **Uus keskkond**.
3. Sisestage keskkonna jaoks kordumatu nimi ja valige asukoht, kuhu juurutada.

    > [!NOTE]
    > Talent pole kõigis regioonides saadaval. Seetõttu kontrollige kindlasti enne oma uue keskkonna asukoha valimist selle saadavust.

4. Kui teilt küsitakse, kas soovite luua andmebaasi, valige **Loo andmebaas**, et luua Common Data Service’ise (CDS) andmebaas, mis peab hostima osasid teie Talenti andmeid. Andmebaasi loomisel saate PowerAppsi rakendused Talentiga integreerida.
5. Teilt küsitakse juurdepääsu taset, mida andmebaasi jaoks kasutada. Soovitame valida suvandi **Juurdepääsu piiramine**, sest see suvand takistab Talenti kasutajatel otsese juurdepääsu tundlikele andmetele PowerAppsi rakenduse abil.
6. Loodud CDS-i andmebaas sisaldab demoandmed, mis lisavad muu teabe hulgas teie keskkonna kaitsmiseks passiivseid töövõtjaid ja fiktiivseid aadresse. Demoandmete eemaldamiseks järgige pärast CDS-i andmebaasi loomist järgmisi etappe.

    > [!IMPORTANT]
    > Kui lõite CDS-i andmebaasi juba varem ja sisestasite sellesse oma ettevõtte tootmisandmeid, eemaldavad need etapid valitud andmebaasist **kõik** andmed, sealhulgas teie ettevõtte tootmisandmed.

    1. Sisselogimine rakendusse [PowerApps](https://preview.web.powerapps.com/home).
    2. Valige ülemise parempoolse nurga ripploendist keskkond, mille lõite 2. etapis.
    3. Laiendage navigeerimispaani vasakul pool asuvat jaotist **Common Data Service** ja tehke valik**Üksused**.
    4. Valige lehe paremal küljel ellipsi (**…**) nupp ja valige siis **Kustuta kõik andmed**.
    5. Valige **Kustuta andmed**, et kinnitada, et soovite andmed eemaldada. See toiming eemaldab kõik demoandmed, mis lisati CDS-i vaikimisi. See eemaldab ka kõik muud andmed, mis sisestati valitud andmebaasi.

Nüüd saate oma uut keskkonda kasutada.

## <a name="grant-access-to-the-environment"></a>Keskkonnale juurdepääsu andmine
Vaikimisi on keskkonnale juurdepääs ainult selle loonud üldadministraatoril. Rakenduse teistele kasutajatele tuleb juurdepääs anda eraldi. Juurdepääsu andmiseks tuleb Core HR-i keskkonnas [lisada kasutajaid](../dev-itpro/sysadmin/tasks/create-new-users.md) ja [määrata neile sobivad rollid](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md). Lisaks on vaja need kasutajad lisada PowerAppsi keskkonda, nii et nad pääsevad ligi rakendustele Attract ja Onboard. Protseduuri on kirjeldatud siin. Kui vajate etappide lõpetamisel abi, vaadake ajaveebipostitust [PowerAppsi halduskeskuse tutvustamine](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Protseduuri lõpetab Talenti keskkonna juurutanud üldadministraator.

1. Avage [PowerAppsi administreerimiskeskus](https://preview.admin.powerapps.com/environments).
2. Valige sobivad keskkonnad.
3. Lisage vahekaardil **Turve** vajalikele kasutajatele roll  **Keskkonna looja**.

Pange tähele, et see PowerAppsi keskkonda kasutajate käsitsi lisamise viimane etapp on ajutine. Lõpuks, kui kasutajad on Core HR-i lisatud, täidetakse see automaatselt.

