---
title: Pilv- ja perimeeterskaalaüksused tootmis- ja laohalduse töökoormuste jaoks
description: Selles teemas antakse teavet tootmis- ja laohalduse töökoormuste pilv- ja perimeeterskaalaüksuste kohta.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fb0d8e0226b11e93503979c202da917de1df6319
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240433"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Pilv- ja perimeeterskaalaüksused tootmis- ja laohalduse töökoormuste jaoks

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pilv- ja perimeeterskaalaüksused võimaldavad tootmisjaoskonna ja täideviidavate laotööde töökoormust erikeskkondade vahel jagada. See funktsioon aitab parandada jõudlust, ennetada teenuse katkestusi ja maksimeerida tööaega. Seda pakuvad järgmised lisandmoodulid.

- Pilvskaalaüksuse lisandmoodul rakenduse Dynamics 365 Supply Chain Management jaoks
- Perimeeterskaalaüksuse lisandmoodul Dynamics 365 Supply Chain Managementi jaoks

Tootmise ja jaotamisega töötavad ettevõtted peavad olema võimelised käivitama olulisi äriprotsesse 24/7, katkestusteta ja nõutud ulatuses. Pilv- ja perimeeterskaalaüksused võimaldavad ettevõtetel käitada peamisi olulise tootmis- ja laoprotsesse ilma katkestusteta, isegi siis kui ilmnevad juhuslikud probleemid internetiühenduse või latentsusega.

## <a name="public-preview-information"></a>Avaliku eelversiooni teave

Eelversioonis on üks keskkond, mis toimib teie Dynamics 365 Supply Chain Managementi keskkonna pilvepõhise keskusena, ja üks keskkond, mis toimib pilvskaalaüksusena.

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a>Eelversiooni saadavus

Pilv- ja perimeeterskaalaüksuste eelversioon muutub olemasolevatele Supply Chain Managementi klientidele kättesaadavaks oktoobris 2020.

Et juurutada oktoobri eelversiooni väljalaset 10.0.15 / platvormi värskendust 39 oma teenuse [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) keskkonnas, peate olema liitunud eelversiooni varajase juurdepääsu programmiga (tuntud ka kui PEAP) rakenduse Supply Chain Management jaoks. Saate liituda PEAPiga, kui olete juba laiema programmi [Dynamics Insider Program](https://experience.dynamics.com/insider) liige. Lihtsalt valige programm, mille nimi on "Finance & Operations: eelversiooni varajase juurdepääsu programm (PEAP)."

> [!IMPORTANT]
> Skaalaüksuse funktsioon rakendusele Supply Chain Management on kättesaadav ainult juhul, kui nõustute [rakendusele Finance and Operations mõeldud pilve ja perimeetri eelversiooni tingimustega](https://Aka.ms/SCMCnETerms).

### <a name="data-processing-for-the-preview"></a>Eelvaate andmete töötlemine

Avaliku eelvaate ajal on mõned halduse teenused majutatud ainult Ameerika Ühendriikides. Kui aga funktsioon muutub üldiselt kättesaadavaks, on need haldusteenused saadaval kõikides geograafilistes kohtades, mida Supply Chain Management toetab. See mõjutab astmiku halduri kasutatava administratiivse teabe siiret ja ladustamist, sealhulgas:

- Teie rentniku nimed ja ID-d
- Teie LCS projekti ID-d
- Administraatori meilid, mida kasutatakse sisselogimiseks
- Keskuse ja mastaabi ühikute keskkonna ID-d
- Töömahu konfiguratsioonid
- Kogutud mõõdikud (nt latentsus ja jõudlus), mis kuvatakse kaardi analüüsimise lehel

Andmed, mis on üle kantud ja talletatud USA andmekeskustesse, kustutatakse, kui teie eelvaate keskkondade sulgemisel.

### <a name="sign-up-for-the-preview"></a>Eelvaatele registreerumine

Rakenduse Supply Chain Management jaoks mõeldud pilve ja perimeetri eelversiooni sisselogimiseks peab teie organisatsioonil juba olema aktiivne rakenduse Supply Chain Management pilvekeskkond.

Skaalaüksuse võimalused on praegu avalikus eelvaates. Kui registreerite end, peate kasutama konkreetse rentniku kasutajakontot. Samuti peate olema projekti omanik või keskkonna administraator LCS Active Dynamics 365 LCS projekti jaoks selles rentniku jaoks.

Kui registreerite eelvaate jaoks, valite üürniku ja läbite registreerimise etapid. Niipea kui Microsoft saab eraldada eelvaate võimsust, saadame teile e-kirja, mis sisaldab ettevalmistuse üksikasju ja kampaania (Promo) koode kahe keskkonna jaoks (keskusr ja skaala ühik) vastava LCS projekti jaoks. Seejärel saate kasutada kahte keskkonda Tier-2-na liivakasti keskkondades. Need keskkonnad kehtivad 60 päeva alates promo koodide loomise kuupäevast. Ära kasuta neid kahte keskkonda enne järgmises lõigus kirjeldatud sammu lõpule viimist.

Pärast Microsoftile kinnitamist, et kaks keskkonda on paigutatud kasutades kampaaniakoode, konfigureeritakse üks keskkondadest tööle keskusena ja teine konfigureeritakse töötama skaalaüksusena. Seejärel saate häälestada skaala üksused ja kasutada valitud laohalduse ja tootmise töömahutusid, kasutades [skaala halduri portaali](https://aka.ms/SCMSUM).

Eelvaate keskkonnad kustutatakse automaatseltt 60 päeva möödumisel. Need võidakse siiski varem kustutada, kui ilmneb, et neid ei kasutata. Kui keskkondade eelvaade on kustutatud, saate registreerida ja võtta uue eelvaate paigutamise järjekorda.

Eelvaate jaoks registreerumiseks minge [Skaala Unit Manageri portaali](https://aka.ms/SCMSUM).

### <a name="limitations-that-apply-during-the-preview-period"></a>Eelvaate perioodi jooksul rakendatavad piirangud

> [!IMPORTANT]
> Selle funktsiooni eelvaate esialgse etapi jaoks toetab Microsoft ainult neid keskuseid, millel on pilve skaala üksused, mitte serva skaala üksused. Edge Scale'i üksused on installitud asutusesiseselt ja eeldatakse, et need muutuvad kättesaadavaks programmi eelseisvas faasi käigus.

Kuna pilve ja perimeeterskaala üksused on eelvaate funktsioon, on nendega seotud teenused praegu saadaval piiratud riikides ja regioonides. Lubades pilv- ja perimeeterskaalaüksused, kinnitate, et saate aru, et mõned pilv- ja perimeeterskaalaüksuste konfiguratsiooni ja töötlemisega seotud andmed võidakse talletada Ameerika Ühendriikides asuvas andmekeskuses. Pilv- ja perimeeterskaalaüksuste lubamisega nõustute ka [rakendusele Finance and Operations mõeldud pilve ja perimeetri eelversiooni tingimustega](https://Aka.ms/SCMCnETerms). Lisateavet pilv- ja perimeeterskaalaüksuste kohta vt [dokumentatsioonist](https://aka.ms/scmcne).

Teie privaatsus on Microsoftile oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://aka.ms/privacy).

> [!IMPORTANT]
> Mõni ettevõtte funktsionaalsus ei ole avalikus eelvaates täielikult toetatud juhul, kui töömaht on kasutusel skaala üksustel. Lisateabe saamiseks funktsionaalse töömahu kohta, vt teema lõpuosas olevaid lõike.

## <a name="scale-units-and-dedicated-workloads"></a>Skaala üksused ja sihtotstarbeline töökoormus

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 koos skaala üksustega":::

Skaalaüksused laiendavad teie keskse rakenduse Supply Chain Management keskuse keskkonda, lisades spetsiaalse töötlemise võimsuse. Skaala üksused võivad töötada pilves. Teise võimalusena saavad nad töötada oma kohaliku asutuse ruumide serval. Skaala üksused saab ajutiselt keskuse keskkonnast lahti ühendada. Kui need on ühendatud, saavad skaala üksused kogu teabe, mis on vajalik määratud töötluse töötlemiseks sihtotstarbelise töömahu jaoks.

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="Skaalaüksuse suvandid avalikus eelvaates":::

Avaliku eelvaate jaoks saate konfigureerida keskuse keskkonna, millel on valitud töökoormus pilve skaala üksuses, kasutades Skaalaüksuse halduri portaali. Kohalike äriandmete (LBD) asutusesisesesse keskkonda juurdepääsu omavate osavõtjate eelversioon võib samuti konfigureerida LBD keskkonna kui perimeeterskaalaüksuse.

Töökoormus on määratletud ärifunktsioonide kogum, mida saab välja arvutada ja delegeerida skaala üksusele. Praegu on eelvaates kaks töökoormuse tüüpi:

- Tootmise käivitamine
- Laohaldus

Saate määrata ühe iga töökoormuse tüübi ühiku kohta. 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Spetsiaalsed tootmise käivitamise töökoormuse võimalused skaala üksuses

Tootmise käitamisel tarnivad pilve ja perimeeterskaala üksused järgmised võimalused, isegi kui perimeeterskaala üksused pole pilvega ühendatud:

- Masina operaatorid ja tööde juhtimise haldurid pääsevad ligi operatiivsele tootmisplaanile.
- Masina operaatorid saavad plaani ajakohasena hoida, töötades eraldi ja menetledes tootmise töid.
- Tööde juhtimise haldur saab tegevuskava korrigeerida.
- Töötajatel on juurdepääs aja ja kohalolekt sisse-ja väljaregistreerimisele serval, et tagada õiglane töötaja tasu arvutamine.

Lisateavet vt [tootmise skaala üksuse töömahu üksikasjad](cloud-edge-workload-manufacturing.md).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Spetsiaalsed laohalduse töökoormuse võimalused skaala üksuses

Laohalduse käitlemisel tarnivad pilve ja perimeeterskaala üksused järgmised võimalused, isegi kui perimeeterskaala üksused pole pilvega ühendatud:

- Valitud voogmeetodite töötlemine on lubatud müügitellimuste ja nõudluse täiendamise puhul.
- Laotöötajad saavad teostada müüki ja nõudluse täiendamise lao tööd, kasutades rakendust warehouse.
- Laotöötajad saavad teha päringuid vaba kaubavaru kohta, kasutades rakendust warehouse.
- Laotöötajad saavad luua ja teostada inventuuri kasutades rakendust warehouse.
- Laotöötajad saavad registreerida ostutellimused ja teha ära eeltöö rakenduse warehouse abil. 

Lisateavet vt [tootmise skaala üksuse töömahu üksikasjad](cloud-edge-workload-warehousing.md).

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a>Kasutuselevõetud skaalaüksused rakenduse Supply Chain Management keskkonnale

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a>Pilv- ja perimeeterskaalaüksuste eelversiooni kasutuselevõtmine

Järgnev illustratsioon näitab pilve skaala ühikute avaliku eelvaate jaoks registreerimise ja ettevalmistamise voogu.

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="Registreerimise sammude eelvaade":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a>LCS-i projekti rentniku valimine ja üksikasjalik eelversiooniprotsess

Avalikus eelvaates näitab [Skaala Unit Manageri portaal](https://aka.ms/SCMSUM) nende üürnike loendit, millesse teie konto kuulub, ja kus olete LCS projekti omanik või keskkonna administraator.

Kui teie otsitavat üürnikku ei ole selles loendis, minge [LCS](https://lcs.dynamics.com/v2)ja veenduge, et olete selle rentniku suhtes kas keskkonna-või LCS projekti omanik. Võtke arvesse, et ainult, Azure Active Directory (Azure AD) valitud rentniku kontodelt on lubatud registreerumise kogemus lõpule viia.

> [!NOTE]
> Pärast LCS muudatuste rakendamist võib üürnike loendi muudatuste kajastamiseks kuluda kuni 30 minutit.

Iga üürniku kohta kuvatakse loendis registreerimise olek.

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="Registreerumise võimalus üürnikule":::

Valige **Klõpsake siin, et registreerida** link, et registreerida oma LCS üürnik osalemiseks eelvaates. Peate tingimustega nõustuma. Peate sisestama ka ettevõtte meiliaadressi, kuhu Microsoft saab saata teateid, mis on seotud eelversiooni registreerimise protsessiga.

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="Registreerumise ettepanek üürnikule":::

Microsoft vaatab teie taotluse läbi ja teavitab teid järgmisest sammudest, saates e-kirja aadressile, kust saatsite registreerimise vormi.

Kui teile on antud juurdepääs eelvaate programmile, saate oma LCS projektile kaks kupongi koodi. Nüüd saate kasutada neid kampaania koode, et kasutada kahte keskkonda LCS. Keskkonnad peavad kasutama PEAP väljalaset 10.0.15 või uuemat versiooni. Kui olete kampaaniakoodide rakendamise lõpetanud, teavitage sellest Microsofti (nagu kästud), et saaksime lõpetada eelvaate funktsioonide keskkondade lubamise. Microsoft annab teile teada, kui see konfiguratsiooni etapp on lõpule viidud.

Nüüd saate alustada oma eelvaate keskkonnas skaala üksuste ja töömahtude konfigureerimist.

> [!IMPORTANT]
> Pilve skaala üksuste konfigureerimisel saate [teha kõiki vajalikke samme skaala Unit Manageri portaalis](#scale-unit-manager-portal).
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Hallake pilve skaala üksuseid ja töömahtei, kasutades Scale Unit Manageri portaali

Avage [Scale Unit Manageri portaal](https://aka.ms/SCMSUM) ja logige sisse oma rentniku konto abil. Lehel **Skaalaüksuste konfigureerimine** saate lisada keskse keskkonna, kui see ei ole juba loetletud. Seejärel saate valida keskuse, mida soovite konfigureerida koos skaala ühikute ja töömahuga.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Skaala üksuse ja töömahu haldamise kogemus":::

Ühe või mitme skaala üksuste lisamiseks, mis on saadaval teie topoloogias, valige **Lisa skaala ühikud**. Eelvaates peaksite nägema pilve skaala üksust, mida on rakendatud ühest kupongi koodidest, mille te olete eelvaate programmi osana saanud.

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

Vahekaardil **Määratletud töömahud** Kasutage **nuppu Loo töökoormus,** et lisada laohalduse või tootmise käivitamise töömaht ühte teie skaalajaotise üksustest. Iga töömahu puhul peate määrama töömahule kuuluvate protsesside konteksti. Laohalduse töökoormuste puhul on kontekst konkreetne ladu kindlas tegevuskohas ja juriidiline üksus. Tootmise käivitamise töömahue puhul on kontekst kindla tegevuskohaga juriidiline üksus.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Töömahu loomine":::

> [!IMPORTANT]
> Scale Unit Manageri portaal ei luba eelvaates töömahtusid skaalaüksustelt eemaldada või tühistada skaalaüksuse määramist keskuses kui määramine on juba teostatud. Kui peate määrangu eemaldama, pöörduge oma kontaktisiku poole programmi halduse eelvaate jaoks.

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]