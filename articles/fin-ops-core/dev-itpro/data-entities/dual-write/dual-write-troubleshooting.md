---
title: Üldine tõrkeotsing
description: See artikkel annab üldist tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f263e331d23ce0ddf60a4abc2467513aa342445
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112360"
---
# <a name="general-troubleshooting"></a>Üldine tõrkeotsing

[!include [banner](../../includes/banner.md)]



See artikkel annab üldist tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning Dataverse.

> [!IMPORTANT]
> Mõned küsimused, mida see artikkel käsitleb, võivad nõuda kas süsteemiadministraatori rolli või Microsofti Azure Active Directory (Azure AD) rentniku administraatori mandaate. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Teenuse Dataverse’i lisandmooduli jälituslogide lubamine ja kuvamine tõrke üksikasjade kuvamiseks

Jälituslogid võivad olla kasulikud, kui finantside &toimingute ja vahel on topeltkirjutustega otsesünkroonimisprobleemide tõrkeotsinguks Dataverse. Logid võivad anda dynamics 365 jaoks tehnilise ja tehnika toe meeskondadele kindlaid üksikasju. See artikkel käsitleb jälituslogide lubamist ja nende vaatamist. Jälituslogisid hallatakse Dynamics 365 sätete lehel ja need vajavad muutmiseks ja vaatamiseks administraatori taseme privileege. 

**Jälituslogi sisselülitamiseks ja tõrgete kuvamiseks nõutav roll:** süsteemiadministraator

### <a name="turn-on-the-trace-log"></a>Lülita jälituslogi sisse
Jälituslogi sisselülitamiseks toimige järgmiselt.

1.  Logige rakendusse Dynamics 365 sisse ja valige ülemisel **navigeerimisribal** sätted. Klõpsake lehel Systems (Süsteemides) käsku **Administration (Haldus)**.
2.  Klõpsake halduslehel valikut **Süsteemisätted**.
3.  Valige vahekaart **Kohandamine** ja lisandmoodulid ning seejärel muutke kohandatud töövoo tegevuse jälituse jaotises ripploend valikule **Kõik**. See jälitab kõiki tegevusi ja pakub põhjalikku andmekomplekti meeskondadele, kes peavad potentsiaalseid probleeme üle vaatama.

> [!NOTE]
> Ripploendist Erand seadmine **annab** jälitusteavet ainult erandite (tõrgete) ilmnemisel.

Kui see on lubatud, kogutakse lisandmooduli jälgimislogisid seni, kuni need lülitatakse käsitsi välja, pöördudes tagasi selle asukoha juurde ja valides suvandi **Välja**.

### <a name="view-the-trace-log"></a>Kuva jälituslogi
Jälituslogi kuvamiseks toimige järgmiselt.

1. Valige Dynamics 365 sätete lehel ülemisel **navigeerimisribal** sätted. 
2. Valige **lehe jaotises Kohandused** **suvand** Trace Log.
3. Jälgimislogide loendist leiate sisestusi tüübi nime ja/või teate nime alusel.
4. Täislogi vaatamiseks avage soovitud kirje. Jaotises Käivitamine teateblokk annab lisandmooduli kohta saadaolevat teavet. Võimaluse korral antakse ka erandi üksikasjad. 

Saate kopeerida jälituslogide sisu ja kleepida need teise rakendusse nagu Notepad või teised tööriistad logide ja tekstifailide vaatamiseks, et kogu sisu oleks lihtsam näha. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Silumisrežiimi lubamine reaalajas sünkroonimisprobleemide tõrkeotsinguks finantside ja toimingute rakendustes

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator

Topeltkirjutuse tõrked, mis pärinevad Dataverse, võivad ilmuda finantside ja toimingute rakenduses. Vigade paljusõnalise logimise lubamiseks toimige järgmiselt:

1. Kõigil finantsi ja toimingute rakenduse projektikonfiguratsioonidel **on lipp IsDebugMode** tabelis **DualWriteProjectConfiguration**.
2. **TopeltKirjutuseProjektiKonfiguratsioon** avamine Exceli lisandmooduliga. Lisandmooduli kasutamiseks lubage kujundusrežiim finantside **ja toimingute Exceli lisandmoodulis ja lisage lehele DualWriteProjectConfiguration**. Lisateavet vaata [üksuse andmete kuvamiseks ja värskendamiseks Exceli`ga](../../office-integration/use-excel-add-in.md).
3. Seadke projekti **Silumisrežiim** väärtuseks **Jah**.
4. Käivitage stsenaarium, mis tekitab tõrkeid.
5. Paljusõnalised logid salvestatakse **TopeltKirjutusTõrkeLogi** tabelisse.
6. Tabelibrauseri andmete otsimiseks kasutage järgmist linki: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, asendades `999` vastavalt vajadusele.
7. Uuendage uuesti pärast [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), mis on saadaval platvormi värskendusteks 37 ja uuemad. Kui see parandus on installitud, hõivab silumisrežiim rohkem logisid.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontrolli virtuaalmasina sünkroonimistõrkeid finantside ja toimingute rakenduse puhul

**Tõrgete vaatamiseks nõutav roll:** süsteemiadministraator

1. Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.
2. Avage LCS-i projekt, mille valisite topeltkirjutamise testimiseks.
3. Valige paan **Pilve majutatud keskkonnad**.
4. Kasutage kaugtöölaua abil finantside ja toimingute rakenduse sisselogimiseks virtuaalmasinasse (VM). Kasutage LCS-is kuvatud kohalikku kontot.
5. Avage sündmusevaatur.
6. Valige **Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> AX-DualWriteSync \> Toiming**.
7. Vaadake läbi hiljutiste tõrgete loend.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Topeltkirjutuse kasutajaliidese dokument, mis kuvatakse tühjana
Kui avate topeltkirjutuslehe Microsoft Edge brauseris või Chrome'i brauseris, ei laadita kodulehte ja te näete tühja lehekülge või tõrketeadet, nagu näiteks "Midagi läks valesti".
Devtoolis näete viga konsoollogides:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: atribuudi sessionStorage lugemine nurjus asukohast Window: selle dokumendi jaoks ei ole võimalik juurde pääseda. t.storeInSessionStorage'is (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860) uuel t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103)https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115 at Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728) juures jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191) juures Nr (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692) või (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076) Ss ( ) juures, kell vs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750 https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130) Hsis (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151)

Kasutajaliides kasutab brauserit "seansi talletus", et talletada mõned atribuudiväärtused avalehe laadimiseks. Selleks peavad saidi brauseris olema lubatud kolmanda osapoole küpsised. Tõrge näitab, et kasutajaliides ei pääse seansi talletuse juurde. Selle probleemi ilmnemisel võib olla kaks stsenaariumi:

1.  Te avate UI incotoolto režiimis Edge/Kroomitud ja kolmanda osapoole küpsised incokoostos on blokeeritud.
2.  Te olete blokeerinud kolmanda osapoole küpsised kokku Edge'is/Kroomitud.

### <a name="mitigation"></a>Vähendamine
Kolmanda osapoole küpsiste kasutamine brauseri sätetes peab olema lubatud.

### <a name="google-chrome-browser"></a>Veebilehitseja <a0/&amp
1. valik:
1.  Minge säteteni, chrome://settings/ aadressiribale ja seejärel avage Privaatsus ja Turvalisus -> Küpsised ja muud saidi andmed.
2.  Valige "Luba kõik küpsised". Kui te ei soovi seda teha, kasutage teist valikut.

2. Valik:
1.  Minge säteteni, chrome://settings/ aadressiribale ja seejärel avage Privaatsus ja Turvalisus -> Küpsised ja muud saidi andmed.
2.  Kui valitud on valik "Blokeeri kolmanda osapoole küpsised Incotoolis" või "Blokeeri kolmanda osapoole küpsisted", minge "Saidid, mis saavad alati küpsiseid kasutada" ja klõpsake käsku **Lisa**. 
3.  Lisage oma finants& toimingute rakenduste saidi nimi – https://<your_FinOp_instance>.cloudax.dynamics.com. Veenduge, et märgite ruudu "Kõik küpsised" puhul ainult sellel saidil. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge brauser
1.  Liikuge sätetes –> saidiload –> ja saidi andmed.
2.  Lülitage välja "Blokeeri kolmanda osapoole küpsisted".  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Mõne muu keskkonna linkimine ja Dataverse linkimine finantside ja toimingute rakendusest

**Nõutav roll keskkonna linkimise tagasi tegemiseks: süsteemiadministraatori** jaoks: finantside ja toimingute rakendus või Dataverse.

1. Logige sisse finantside ja toimingute rakendusse.
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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Kuidas tagada andmete integratsioon kasutab kõige praegust finantside ja toimingute skeemi?

Võite oma andmete integreerimisel esineda andmeprobleeme, kui ajalist skeemi ei kasutata. Järgmised sammud aitavad teil värskendada üksuste loendit finantside ja toimingute rakendustes ning andmete integraatori üksustes.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Üksuseloendi värskendamine finants- ja toimingutekeskkonnas
1.  Logige sisse oma finants- ja toimingute keskkonda.
2.  Valige **andmehaldus**.
3.  Valige andmete halduse sees raamistiku **parameetrid**.
4.  Valige andmete **importimise/eksportimise raamistiku parameetrite lehel** vahekaart **Üksuse sätted ja** valige üksuseloendi **värskendamine**. Sõltuvalt kaasatud üksuste arvust võib värskendamiseks aega võtta üle 30 minuti.
5.  Liikuge andmehaldusele **ja** valige **andmeüksused, et** kontrollida, kas eeldatud üksused on loendis. Kui eeldatud üksusi loendis ei ole, kontrollige, et üksused ilmuvad teie finantside ja toimingute keskkonnas ning taastage puuduvad üksused vastavalt vajadusele.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Kui värskendus ei suuda probleemi lahendada, kustutage ja lisage üksused uuesti.

> [!NOTE]
> Teil võib tekkida vajadus peatada mis tahes töötlemisgrupid, mis kasutavad neid üksusi enne kustutamist aktiivselt.

1.  Valige **andmehaldus** oma finants- ja toimingute keskkonnas ja valige **Andmeüksused**.
2.  Otsige üksuseid, kellel on probleeme, ja tehke märkus sihtüksusele, paigutamistabelile, üksuse nimele ja muudele sätetele. Kustutage üksus või üksused loendist.
3.  Valige **uus** ja lisage üksus või üksused uuesti, kasutades andmeid sammust 2. 

#### <a name="refresh-entities-in-data-integrator"></a>Värskenda üksuseid andmete integraatoris
Logige halduskeskusesse Power Platform sisse ja valige andmete **integratsioon**. Avage projekt, kus probleemid esinevad, ja valige värskenda **üksused**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Kuidas lubada ja salvestada võrgujälgi nii, et jälge saab siduda piletipiletite toega

Tugimeeskond võib mõne probleemi tõrkeotsinguks vajada võrgujälje ülevaatamist. Võrgujälje loomiseks järgige järgmisi samme:

### <a name="google-chrome-browser"></a>Veebilehitseja <a0/&amp

1. Avatud vahekaardil vajutage **F12** või valige **arendaja tööriistad** arendaja tööriistade avamiseks.
2. Saate avada **Võrk** vahekaardi ja tippige **integreeri** filtri tekstiboksi.
3. Käivitage stsenaarium ja jälgige sisselogitud taotlusi.
4. Paremklõpsake kirjeid ja valige suvand **Salvesta kõik sisuga HAR-i jaoks**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge brauser

1. Avatud vahekaardil vajutage **F12** või valige **arendaja tööriistad** arendaja tööriistade avamiseks.
2. Avage vahekaart **Võrgustik**.
3. Käivitage stsenaarium.
4. Valige **Salvestamine** eksportimiseks HAR-tööna.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

