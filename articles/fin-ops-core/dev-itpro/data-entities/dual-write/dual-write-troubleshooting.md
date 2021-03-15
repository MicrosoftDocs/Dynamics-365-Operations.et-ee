---
title: Üldine tõrkeotsing
description: See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b01ef3da908739d17f2a03398ae56f35191e8db6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744537"
---
# <a name="general-troubleshooting"></a>Üldine tõrkeotsing

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Kui üritate installida tööriista Package Deployer abil topeltkirjutuse paketti, ei kuvata ühtegi saadaolevat lahendust

Mõni tööriista Package Deployer versioon ei ühildu topeltkirjutuse lahenduse paketiga. Paketi edukaks installimiseks kasutage kindlasti tööriista Package Deployer [versiooni 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) või uuemat.

Pärast tööriista Package Deployer installimist installige lahendusepakett, järgides neid juhiseid.

1. Uusima lahenduse paketi faili saate alla laadida lehelt Yammer.com. Pärast paketi ZIP-faili allalaadimist paremklõpsake seda ja valige **Atribuudid**. Valige märkeruut **Tühista blokeerimine** ja valige seejärel **Rakenda**. Kui märkeruutu **Tühista blokeerimine** ei kuvata, on ZIP-fail juba blokeeritud ja võite selle toimingu vahele jätta.

    ![Atribuutide dialoogiboks](media/unblock_option.png)

2. Ekstraktige paketi ZIP-fail ja kopeerige kõik failid kaustas **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![Kausta Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 sisu](media/extract_package.png)

3. Kleepige kõik kopeeritud failid tööriista Package Deployer kausta **Tööriistad**. 
4. Käivitage **PackageDeployer.exe** Dataverse'i keskkonna valimiseks ja lahenduste installimiseks.

    ![Kausta Tööriistad sisu](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Teenuse Dataverse’i lisandmooduli jälituslogide lubamine ja kuvamine tõrke üksikasjade kuvamiseks

**Jälituslogi sisselülitamiseks ja tõrgete kuvamiseks nõutav roll:** süsteemiadministraator

Jälituslogi sisselülitamiseks toimige järgmiselt.

1. Logige sisse mudelipõhisesse rakendusse Dynamics 365, avage leht **Sätted** ja valige seejärel jaotises **Süsteem** suvand **Haldus**.
2. Valige lehelt **Haldus** suvand **Süsteemisätted**.
3. Lisandmooduli jälituslogi lubamiseks valige vahekaardil **Kohandamine** veerus **Lisandmooduli ja kohandatud töövoo tegevuse jälgimine** suvand **Kõik**. Kui soovite logida jälituslogisid ainult erandite ilmnemisel, saate teha valiku **Erand**.


Jälituslogi kuvamiseks toimige järgmiselt.

1. Logige sisse mudelipõhisesse rakendusse Dynamics 365, avage leht **Sätted** ja valige seejärel jaotises **Kohandamine** suvand **Lisandmooduli jälituslogi**.
2. Leiate jälituslogid siis, kui veeru **Tüübi nimi** väärtuseks on seatud **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Täieliku logi vaatamiseks topeltklõpsake üksust ja seejärel vaadake üle kiirkaardil **Käivitamine** tekst **Teateplokk**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Silumisrežiim lubamine tõrkeotsingu reaalajas sünkroonimise probleemide korral Finance and Operationsi rakendustes

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator. Dataverse'ist pärinevaid topeltkirjutuse tõrkeid võidakse kuvada Finance and Operationsi rakenduses. Mõnel juhul ei ole tõrketeate täistekst saadaval, kuna sõnum on liiga pikk või sisaldab tuvastamist võimaldavaid andmeid (PII). Verbose tõrgete logimise saate sisse lülitada järgmiste juhiste abil.

1. Kõigil Finance and Operationsi rakenduste projekti konfiguratsioonidel on atribuut **IsDebugMode** tabelis **DualWriteProjectConfiguration**. Tabeli **DualWriteProjectConfiguration** avamine Exceli lisandmooduliga.

    > [!TIP]
    > Kõige lihtsam on tabelit avada režiimi **Kujundus** sisselülitamisel Exceli lisandmoodulis ja seejärel lisada töölehele üksus **DualWriteProjectConfigurationEntity**. Lisateabe saamiseks vt [Tabeli andmete avamine Excelis ja andmete värskendamine Exceli lisandmooduliga](../../office-integration/use-excel-add-in.md).

2. Seadke projekti atribuudi **IsDebugMode** väärtuseks **Jah**.
3. Käivitage stsenaarium, mis tekitab tõrkeid.
4. Verbose logid on saadaval tabelis DualWriteErrorLog. Tabeli brauseris andmete otsimiseks kasutage järgmist URL-i (asendage **XXX** vastavalt vajadusele):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Rakenduse Finance and Operations virtuaalarvuti sünkroonimistõrgete kontrollimine

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator

1. Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.
2. Avage LCS-i projekt, mille valisite topeltkirjutamise testimiseks.
3. Valige paan **Pilve majutatud keskkonnad**.
4. Kasutage rakenduse Finance and Operations virtuaalarvutisse (VM) sisselogimiseks kaugtöölauda. Kasutage LCS-is kuvatud kohalikku kontot.
5. Avage sündmusevaatur.
6. Valige **Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> AX-DualWriteSync \> Toiming**.
7. Vaadake läbi hiljutiste tõrgete loend.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Linkimise tühistamine ja teise Dataverse'i keskkonna linkimine Finance and Operationsi rakendusest

**Keskkonna linkimise tühistamiseks nõutav roll:** kas Finance and Operationsi rakenduse või teenuse Dataverse süsteemiadministraator.

1. Logige rakendusse Finance and Operations sisse.
2. Avage **Tööruumid \>Andmehaldus** ja valige paan **Topeltkirjutus**.
3. Valige kõik töötavad vastendused ja valige **Peata**.
4. Valige nupp **Tühista keskkonna link**.
5. Toimingu kinnitamiseks valige **Jah**.

Nüüd saate linkida uue keskkonna.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Müügitellimuse rea teabevormi ei saa kuvada 

Kui loote müügitellimuse rakenduses Dynamics 365 Sales, võib nupu **+ Lisa tooted** klõpsamine suunata teid rakenduse Dynamics 365 Project Operations tellimuserea vormile. Sellel vormil ei saa vaadata müügitellimuse rea vormi **Teave**. Ripploendis ei kuvata suvandi **Uus tellimuse rida** all suvandit **Teave**. See juhtub, kuna teie keskkonnas on installitud rakendus Project Operations.

Vormisuvandi **Teave** uuesti lubamiseks tehke järgmist.
1. Avage tabel **Tellimuse rida**.
2. Leidke vormide sõlme alt vorm **Teave**. 
3. Valige vorm **Teave** ja klõpsake **Luba turberollid**. 
4. Seadke turbesäte väärtusele **Kuva kõigile**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]