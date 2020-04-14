---
title: Üldine tõrkeotsing
description: See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172687"
---
# <a name="general-troubleshooting"></a>Üldine tõrkeotsing

[!include [banner](../../includes/banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.

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
4. Käivitage **PackageDeployer.exe** Common Data Service'i keskkonna valimiseks ja lahenduste installimiseks.

    ![Kausta Tööriistad sisu](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a>Common Data Service'i lisandmooduli jälituslogide lubamine ja kuvamine tõrke üksikasjade kuvamiseks

**Jälituslogi sisselülitamiseks ja tõrgete kuvamiseks nõutav roll:** süsteemiadministraator

Jälituslogi sisselülitamiseks toimige järgmiselt.

1. Logige sisse rakendusse Finance and Operations, avage leht **Seaded** ja valge jaotisest **Süsteem** suvand **Haldus**.
2. Valige lehelt **Haldus** suvand **Süsteemisätted**.
3. Lisandmooduli jälituslogi lubamiseks valige vahekaardil **Kohandamine** väljal **Lisandmooduli ja kohandatud töövoo tegevuse jälgimine** suvand **Kõik**. Kui soovite logida jälituslogisid ainult erandite ilmnemisel, saate teha valiku **Erand**.


Jälituslogi kuvamiseks toimige järgmiselt.

1. Logige sisse rakendusse Finance and Operations, avage leht **Seaded** ja valge jaotisest **Kohandamine** suvand **Lisandmooduli jälituslogi**.
2. Leiate jälituslogid siis, kui välja **Tüübi nimi** väärtuseks on seatud **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.
3. Täieliku logi vaatamiseks topeltklõpsake üksust ja seejärel vaadake üle kiirkaardil **Käivitamine** tekst **Teateplokk**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Silumisrežiim lubamine tõrkeotsingu reaalajas sünkroonimise probleemide korral Finance and Operationsi rakendustes

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator

Common Data Service'ist pärinevaid topeltkirjutuse tõrkeid võidakse kuvada Finance and Operationsi rakenduses. Mõnel juhul ei ole tõrketeate täistekst saadaval, kuna sõnum on liiga pikk või sisaldab tuvastamist võimaldavaid andmeid (PII). Verbose tõrgete logimise saate sisse lülitada järgmiste juhiste abil.

1. Kõigil Finance and Operationsi rakenduste projekti konfiguratsioonidel on atribuut **IsDebugMode** üksusel **DualWriteProjectConfiguration**. Üksuse **DualWriteProjectConfiguration** avamine Exceli lisandmooduliga.

    > [!TIP]
    > Kõige lihtsam on üksust avada režiimi **Kujundus** sisselülitamisel Exceli lisandmoodulis ja seejärel lisada töölehele üksus **DualWriteProjectConfigurationEntity**. Lisateabe saamiseks vt [Üksuse andmete avamine Excelis ja andmete värskendamine Exceli lisandmooduliga](../../office-integration/use-excel-add-in.md).

2. Seadke projekti atribuudi **IsDebugMode** väärtuseks **Jah**.
3. Käivitage stsenaarium, mis tekitab tõrkeid.
4. Verbose logid on saadaval tabelis DualWriteErrorLog. Tabeli brauseris andmete otsimiseks kasutage järgmist URL-i (asendage **XXX** vastavalt vajadusele):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Rakenduse Finance and Operations virtuaalarvuti sünkroonimistõrgete kontrollimine

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator

1. Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.
2. Avage LCS-i projekt, mille valisite topeltkirjutamise testimiseks.
3. Valige paan **Pilve majutatud keskkonnad**.
4. Kasutage rakenduse Finance and Operations virtuaalarvutisse (VM) sisselogimiseks kaugtöölauda. Kasutage LCS-is kuvatud kohalikku kontot.
5. Avage sündmusevaatur.
6. Valige **Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> AX-DualWriteSync \> Toiming**.
7. Vaadake läbi hiljutiste tõrgete loend.

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a>Linkimise tühistamine ja teise Common Data Service'i keskkonna linkimine Finance and Operationsi rakendusest

**Keskkonna linkimise tühistamiseks nõutav mandaat:** Azure AD rentniku admin

1. Logige rakendusse Finance and Operations sisse.
2. Avage **Tööruumid \>Andmehaldus** ja valige paan **Topeltkirjutus**.
3. Valige kõik töötavad vastendused ja valige **Peata**.
4. Valige nupp **Tühista keskkonna link**.
5. Toimingu kinnitamiseks valige **Jah**.

Nüüd saate linkida uue keskkonna.
