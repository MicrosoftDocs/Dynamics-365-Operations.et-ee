---
title: Üldine tõrkeotsing
description: See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4adc2d83667a05d14a26ace23e5bd8026df4b5f
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380208"
---
# <a name="general-troubleshooting"></a>Üldine tõrkeotsing

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni üldise tõrkeotsingu kohta.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Teenuse Dataverse’i lisandmooduli jälituslogide lubamine ja kuvamine tõrke üksikasjade kuvamiseks

**Jälituslogi sisselülitamiseks ja tõrgete kuvamiseks nõutav roll:** süsteemiadministraator

Jälituslogi sisselülitamiseks toimige järgmiselt.

1. Logige sisse kliendikaasamise rakendusse, avage leht **Seaded** ja valge jaotisest **Süsteem** suvand **Haldus**.
2. Valige lehelt **Haldus** suvand **Süsteemisätted**.
3. Lisandmooduli jälituslogi lubamiseks valige vahekaardil **Kohandamine** veerus **Lisandmooduli ja kohandatud töövoo tegevuse jälgimine** suvand **Kõik**. Kui soovite logida jälituslogisid ainult erandite ilmnemisel, saate teha valiku **Erand**.


Jälituslogi kuvamiseks toimige järgmiselt.

1. Logige sisse kliendikaasamise rakendusse, avage leht **Seaded** ja valge jaotisest **Kohandamine** suvand **Lisandmooduli jälituslogi**.
2. Leiate jälituslogid siis, kui veeru **Tüübi nimi** väärtuseks on seatud **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Täieliku logi vaatamiseks topeltklõpsake üksust ja seejärel vaadake üle kiirkaardil **Käivitamine** tekst **Teateplokk**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Silumisrežiim lubamine tõrkeotsingu reaalajas sünkroonimise probleemide korral Finance and Operationsi rakendustes

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator

Dataverse'ist pärinevaid topeltkirjutuse tõrkeid võidakse kuvada Finance and Operationsi rakenduses. Vigade paljusõnalise logimise lubamiseks toimige järgmiselt:

1. Kõigil Finance and Operations rakenduste projekti konfiguratsioonidel on atribuut **Silumisrežiim** tabelis **TopeltKirjutuseProjektiKonfiguratsioon**.
2. **TopeltKirjutuseProjektiKonfiguratsioon** avamine Exceli lisandmooduliga. Lisandmooduli kasutamiseks lubage kujundusrežiim Finance and Operations Exceli lisandmoodulis ja lisage lehele **TopeltKirjutuseProjektiKonfiguratsioon**. Lisateavet vaata [üksuse andmete kuvamiseks ja värskendamiseks Exceli`ga](../../office-integration/use-excel-add-in.md).
3. Seadke projekti **Silumisrežiim** väärtuseks **Jah**.
4. Käivitage stsenaarium, mis tekitab tõrkeid.
5. Paljusõnalised logid salvestatakse **TopeltKirjutusTõrkeLogi** tabelisse.
6. Tabelibrauseri andmete otsimiseks kasutage järgmist linki: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, asendades `999` vastavalt vajadusele.
7. Uuendage uuesti pärast [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), mis on saadaval platvormi värskendusteks 37 ja uuemad. Kui see parandus on installitud, hõivab silumisrežiim rohkem logisid.  

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

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Kuidas lubada ja salvestada võrgujälgi nii, et jälge saab siduda piletipiletite toega

Tugimeeskond võib mõne probleemi tõrkeotsinguks vajada võrgujälje ülevaatamist. Võrgujälje loomiseks järgige järgmisi samme:

### <a name="chrome"></a>Chrome

1. Avatud vahekaardil vajutage **F12** või valige **arendaja tööriistad** arendaja tööriistade avamiseks.
2. Saate avada **Võrk** vahekaardi ja tippige **integreeri** filtri tekstiboksi.
3. Käivitage stsenaarium ja jälgige sisselogitud taotlusi.
4. Paremklõpsake kirjeid ja valige suvand **Salvesta kõik sisuga HAR-i jaoks**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Avatud vahekaardil vajutage **F12** või valige **arendaja tööriistad** arendaja tööriistade avamiseks.
2. Avage vahekaart **Võrgustik**.
3. Käivitage stsenaarium.
4. Valige **Salvestamine** eksportimiseks HAR-tööna.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
