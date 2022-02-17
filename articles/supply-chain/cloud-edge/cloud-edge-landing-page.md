---
title: Skaala ühikud jaotatud topoloogias
description: Selles teemas antakse teavet tootmis- ja laohalduse töökoormuste pilv- ja perimeeterskaalaüksuste kohta.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 593331a3f1073edb6a50c9bfc66e0723d222832a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065760"
---
# <a name="scale-units-in-a-distributed-hybrid-topology"></a>Skaala ühikud jaotatud topoloogias

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Microsofti Dynamics 365 Supply Chain Management mastaabiühiku võimalus tehakse teile kättesaadavaks teenuse kasutamist reguleerivate tingimuste alusel. Lisateavet leiate [Microsoft Dynamics'i juriidilise teabest](https://go.microsoft.com/fwlink/?LinkID=290927).
>
> Lubades pilv- ja perimeeterskaalaüksused, palutakse teil kinnitada, et saate aru, et mõned pilv- ja perimeeterskaalaüksuste konfiguratsiooni ja töötlemisega seotud andmed võidakse talletada Ameerika Ühendriikides asuvas andmekeskuses. Lisateavet pilve- ja servaskaalaüksuste andmetöötluse kohta leiate käesoleva teema jaotisest [Andmetöötlus mastaabiühikute haldamisel](#data-processing-management).

## <a name="core-value-proposition-for-a-distributed-hybrid-topology"></a>Jaotatud hübriid-topoloogia põhiväärtuste ettepanekuks

Tootmise ja jaotamisega töötavad ettevõtted peavad olema võimelised käivitama olulisi äriprotsesse 24/7, katkestusteta ja nõutud ulatuses. Jaotatud hübriid-topoloogia võimaldab ettevõtetel käitada peamisi olulise tootmis- ja laoprotsesse ilma katkestusteta, isegi siis, kui ilmnevad juhuslikud probleemid internetiühenduse või latentsusega.

Jaotatud hübriid-topoloogias tutvustatakse *kaaluühikute* mõisteid, mis võimaldavad tööde ja laotäitmiskoormuste jaotamist erinevate keskkondade vahel. See funktsioon aitab parandada jõudlust, ennetada teenuse katkestusi ja maksimeerida tööaega. Mõõtühikud pakutakse Supply Chain Management tellimuse jaoks järgmiste lisandmoodulite kaudu:

- Pilvskaalaüksuse lisandmoodul rakenduse Dynamics 365 Supply Chain Management jaoks
- Perimeeterskaalaüksuse lisandmoodul Dynamics 365 Supply Chain Managementi jaoks

Töökoormuse võimalusi vabastatakse pidevalt astmelise täiustamise kaudu.

## <a name="scale-units-and-dedicated-workloads"></a>Skaala üksused ja sihtotstarbeline töökoormus

Skaalaüksused laiendavad teie keskse rakenduse Supply Chain Management keskuse keskkonda, lisades spetsiaalse töötlemise võimsuse. Skaala üksused võivad töötada pilves. Teise võimalusena saavad nad töötada oma kohaliku asutuse ruumide serval.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Dynamics 365 koos skaala üksustega.":::

Skaalaüksused pakuvad määratud töökoormustele vastupidavust, töökindlust ja skaalat. Servaskaala üksusi saab pilvejaoturi keskkonnast ajutiselt lahti ühendada. Töötajad jätkavad tööd määratud töökoormusega pilveserval.

*Töökoormus* on määratletud ärifunktsioonide kogum, mida saab välja arvutada ja delegeerida skaala üksusele. Kuigi laohalduse töökoormus on vabastatud, on tootmise käivitamise töökoormus endiselt eelvaates.

Saate konfigureerida keskuse keskkonna ja valitud töökoormus pilve skaala üksuses kasutades [Skaalaüksuse halduri portaali](https://sum.dynamics.com). Skaalaühiku kohta saate määrata ka mitu töökoormust. Lisateavet pilveskaala ühikute eeltingimuste ja piirangute kohta praeguses versioonis leiate käesoleva teema jaotisest [Pilveskaala ühikute eeltingimused ja piirangud](#cloud-scale-unit-prerequisites).

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Spetsiaalsed laohalduse töökoormuse võimalused skaala üksuses

Laohalduse töökoormus on skaalaühikute esimene jaotatud töökoormus, mis vabastatakse üldise kättesaadavuse jaoks. See võimaldab teie laotoiminguid isoleeritud hooldusakende abil skaleerida ja töötada vastupidavas keskkonnas. Laohalduse töökoormus toetab enamikku ettevõtterummu laohaldusprotsesse. Lisateavet vt [Laohalduse töökoormused pilv- ja perimeeterskaalaüksuste jaoks](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Spetsiaalsed tootmise käivitamise töökoormuse võimalused skaala üksuses

Tootmiskoormus pakub järgmisi võimalusi.

- Masina operaatorid ja tööde juhtimise haldurid pääsevad ligi operatiivsele tootmisplaanile.
- Masina operaatorid saavad plaani ajakohasena hoida, töötades eraldi ja menetledes tootmise töid.
- Tööde juhtimise haldur saab tegevuskava korrigeerida.
- Töötajatel on juurdepääs aja ja kohalolekt sisse-ja väljaregistreerimisele serval, et tagada õiglane töötaja tasu arvutamine.

Lisateavet vt [Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Kaaluge enne Supply Chain Management hajutatud hübriidtopoloogia lubamist

Lubades hajutatud hübriidtopoloogia, muudate oma Supply Chain Management pilvekeskkonna nii, et see toimiks jaoturina. Lisaks saate seostada täiendavaid keskkondi, mis on konfigureeritud mastaabiühikutena pilves või pilveservas.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Pilviskaala ühikute eeldused ja piirangud

Mastaabiühikute praeguses versioonis pole mõned võimalused veel saadaval, kuid need võidakse aja jooksul lisada astmelistes väljalasetes.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Peate olema Supply Chain Management litsentsitud klient.

Hajutatud topoloogia pardalemiseks peab teil olema Supply Chain Management litsents. Teie olemasolevast pilvekeskkonnast saab teie hübriidtopoloogia keskus. Võite defineerida nii liivakasti keskkonnad kui ka tootmiskeskkonnad jaoturikeskkondadeks ja saate lisada skaalaühikud vastavalt omandatud lisandmoodulitele.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Olemasolevat projekti tuleb hallata LCS-i globaalse äriversiooni kaudu

Olemasolev Microsoft Dynamics Lifecyle Servicesi (LCS) projekt peab vastama järgmistele versiooninõuetele.

- Projekti tuleb hallata LCS-i globaalse äriversiooni kaudu asukohas [lcs.dynamics.com](https://lcs.dynamics.com).
- LCS-i kohalikke versioone (nt [eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) ja [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com)) ei toetata.
- LCS-i valitsuse pilveversioone ei toetata.
- LCS-i Mooncake'i versiooni ei toetata.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Praegune tootmiskeskkond peab olema LCS-is iseteenindustüübiga

Praegune tootmiskeskkond peab olema märgitud LCS-is **iseteenindus** tüübiga. See tüüp näitab, et teie LCS-projekti rentnik on juba teisendatud nii, et see toetab Azure Service Fabric hostimismudelit.

> [!IMPORTANT]
> Keskkonnatüüpe, mis töötavad infrastruktuuri teenusena (IaaS), ei toetata. Need keskkonnad on tavaliselt sildistatud LCS-is tüübiga **Microsofti hallatud**. Kui teil on seda tüüpi keskkondi, tehke oma Microsofti kontaktiga koostööd, et mõista oma **iseteeninduse** tüübile ülemineku migreerumise ajaskaalat.

Microsoft on üle minemas kõigile Supply Chain Management pilvekeskkondadele IaaS-mudelilt topoloogiale, mida majutatakse asukohas Service Fabric. See samm toob kaasa parema skaleeritavuse ja aitab muuta teenusehalduse lihtsamaks. Seetõttu on juurutamine ja hooldustoimingud kiiremad. Lisaks viiakse teenuse komponendid üle mikroteenuste kontseptsioonile ja teenuse hostimise mudel [läheb](/virtualization/windowscontainers/about/containers-vs-vm) virtuaalse masina (VM) mudelilt üle kergele konteinerarhitektuurile.

Lõppkokkuvõttes toidab sama Service Fabricil põhinev konteinerteenuse infrastruktuur nii teenuse pilve- kui ka servaeksemplare, olenemata sellest, kas eksemplar on pilvejagu või mastaabiühik pilves või pilveservas.

Enne mastaabiühikuid toetava hübriidtopoloogia juurutamist tuleb projekti rentnik üle viia Service Fabricu poolt hostitud mudelile. Lisaks tuleb teisendada kõik jaoturina toimivad keskkonnad.

> [!TIP]
> LCS-projekti rentniku oleku kohta päringu tegemiseks otsige [LCS-is](https://lcs.dynamics.com/) üles oma keskkonna tüüp või pöörduge oma partneri või Microsofti kontakti poole.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Kohalikke äriandmeid (kohapealseid) keskkondi ei toetata mastaabiühikute jaoturitena

Kohapealsed keskkonnad ei saa toimida mastaabiühikute jaoturitena. Jaoturikeskkonnad peavad alati olema pilve majutatud.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Mastaabiüksuste haldamise võimalused on piiratud

Juhtimisvõimalused, mis võivad aidata töökoormuse liikumisel, on piiratud. Mõnda haldustoimingut ei toetata iseteeninduses ja võib-olla peate taotlema tuge oma partneri või Microsofti kontakti kaudu. Näiteks mõned töökoormuse liikumised skaalaüksuste vahel ja ajutised ad hoc liikumised katastroofistsenaariumide korral.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Mõõdikud ja mõõtmised pole veel kättesaadavad

Mõõdikud ja mõõtmised, mis võivad aidata teil valida oma mõõtühikutele parima rakenduse, pole veel saadaval. Kõige kasulikuma rakenduse valimiseks tehke koostööd oma Microsofti kontakti või rakenduspartneriga.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Andmetöötlus skaalaühikute haldamise ajal

Kui lubate oma Dynamics 365 keskkonnas toetada pilve- ja servaskaalaüksuste hajutatud hübriidtopoloogiat, majutatakse mõnda haldusteenust ainult Ameerika Ühendriikides (nagu LCS-i puhul). Selline käitumine mõjutab mõne haldus- ja konfiguratsiooniteabe edastamist ja talletamist, mida kasutab [portaali Scale Unit Manager](https://sum.dynamics.com). Järgmisena on toodud mõned näited.

- Teie rentniku nimed ja ID-d
- Teie LCS projekti ID-d
- Sisselogimiseks kasutatavad administraatori ja projekti omaniku meiliaadressid
- Keskuse ja mastaabi ühikute keskkonna ID-d
- Töökoormuse konfiguratsioonid, sealhulgas juriidiliste isikute ja rajatiste nimed ja füüsilised aadressid, et teie topoloogiat saaks näidata geograafilisel kaardil
- Kogutud mõõdikud (nt latentsus ja läbilaskevõime), mis kuvatakse kaardi analüüsilehel, et aidata teil valida skaalaühikute kõige kasulikum kasutus

USA andmekeskustesse edastatud ja neis talletatud andmed kustutatakse vastavalt Microsofti andmete säilitamise poliitikatele. Teie privaatsus on Microsoftile oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://go.microsoft.com/fwlink/?LinkId=521839).

## <a name="onboarding-in-two-stages"></a>Juurutamine kahes etapis

Hajutatud hübriidtopoloogia juurutamise protsessil on kaks etappi. Esimeses etapis peate kinnitama kohandused, et tagada nende töö hajutatud topoloogias, millel on skaalaühikud. Liivakasti ja tootmiskeskkondi liigutatakse ainult teises etapis.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>1. etapp: kohanduste hindamine ühe lahendusega arenduskeskkondades

Enne liivakasti või tootmiskeskkondade juuritamist soovitame teil uurida mastaabiühikuid arendusseadistuses (nt ühe lahendusega keskkonnas (tuntud ka kui esimese astme keskkond)), et saaksite protsesse, kohandusi ja lahendusi valideerida. Selles etapis rakendatakse andmed ja kohandused ühe lahendusega keskkondadele. Üks keskkond võtab jaoturi rolli ja teine võtab skaalaüksuse rolli. See häälestus on parim viis probleemide tuvastamiseks ja lahendamiseks. Antud etapi lõpuleviimiseks saab kasutada ka uusimat varajase juurdepääsu (PEAP) ehitust.

1. etapi puhul peaksite kasutama [skaalaüksuse juurutustööriistu ühe lahendusega arenduskeskkondadele](https://github.com/microsoft/SCMScaleUnitDevTools). Nende tööriistade abil saate konfigureerida jaoturi ja mastaabiühikud ühes või kahes eraldi ühekastilises keskkonnas. Tööriistad on saadaval binaarse väljalaskena ja lähtekoodina GitHubis. Uurige projekti wiki-lehte, mis sisaldab [samm-sammulistkasutusjuhendit](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), mis kirjeldab tööriistade kasutamist.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>2. etapp: hankige lisandmoodulid ja lisage need oma liivakasti ja tootmiskeskkondadesse

Uude topoloogiase mõne liivakasti või tootmiskeskkonna juurutamiseks peate hankima lisandmoodulid ühe või mitme pilveskaala ühiku jaoks (ja tulevikus servaskaala ühikute jaoks). Lisandmoodulid annavad [LCS-is](https://lcs.dynamics.com/) vastavad projekti- ja keskkonnapesad, et mastaabiühiku keskkondi saaks juurutada.

> [!NOTE]
> Mastaabiühiku lisandmoodulid ei ole seotud piiratud arvu kasutajatega, kuid neid saab kasutada iga olemasoleva tellimuse kasutaja, tuginedes administraatori määratud rollidele.

Mastaabiühikuid pakutakse mitmes laohoiuühikus (SKU) ja hinnakujundusvõimalustes. Seetõttu saate valida suvandi, mis vastab kõige paremini teie plaanitud igakuiste tehingute mahu- ja jõudlusnõuetele.

Algtaseme SKU on tuntud kui *Peamine* ja jõulisem SKU on tuntud kui *Standardne*. Iga SKU on eellaaditud kindla arvu igakuiste tehingutega. Siiski saate igakuist kandeeelarvet suurendada, lisades iga SKU jaoks ülekulu lisandmoodulid.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Pilvskaalaüksuse lisandmoodulid.":::

> [!TIP]
> Teie vajadustele kõige paremini vastava suuruse tuvastamiseks tehke koostööd oma partneri ja Microsoftiga, et mõista igakuist tehingumahtu, mida vajate.

Iga skaalaühiku lisandmooduli ostmine mitte ainult ei anna teile igakuist tehingute mahtu, vaid annab teile ka õiguse teatud arvule keskkonnateenindusaegadele LCS-is. Iga Cloud Scale Unit Add-in lisandmooduli puhul on teil õigus ühele uuele tootmispesale ja ühele uuele liivakastipesale. Juurutamise käigus lisatakse uus LCS-projekt, millel on need pesad. Pesade kasutusõigused on seotud nii, et neid tuleb kasutada mastaabiühikutena, millel on pilvejaotur.

Ülekulu lisandmoodulid ei anna teile uusi keskkonnapesasid.

Kui soovite omandada rohkem liivakasti keskkondi, saate osta täiendavaid tavalisi liivakastipesasid. Microsoft saab seejärel aidata teil lubada need teenindusajad hübriidtopoloogia liivakasti skaala ühikutena.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Supply Chain Management hajutatud hübriitopoloogia juurutamine

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>LCS-i projekti rentniku valimine ja üksikasjalik juurutusprotsess

Pärast seda, kui olete lõpetanud plaanimise, kuidas saate levitatud hübriidtopoloogiaga Supply Chain Management jaoks juurutada, kasutaga juurutusprotsessi alustamiseks [portaali Scale Unit Manager](https://aka.ms/SCMSUM). Portaalis valige vahekaart **Dynamics 365 rentnikud**. Vahekaart kuvab nende üürnike loendit, millesse teie konto kuulub, ja kus olete LCS projekti omanik või keskkonna administraator.

Kui teie otsitavat üürnikku ei ole loendis, minge [LCS](https://lcs.dynamics.com/v2)ja veenduge, et olete selle rentniku suhtes kas keskkonna-või LCS projekti omanik. Ainult, Azure Active Directory (Azure AD) valitud rentniku kontodelt on lubatud registreerumise kogemus lõpule viia.

> [!NOTE]
> Pärast LCS muudatuste rakendamist võib üürnike loendi muudatuste kajastamiseks kuluda kuni 30 minutit.

Iga üürniku kohta kuvatakse loendis juurutamise olek.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Rentnike loend vahekaardil Dynamics 365 Tenants.":::

LCS-rentniku juurutamise taotlemiseks valige suvand **Alustamiseks klõpsake siin**. Peate tingimustega nõustuma. Peate sisestama ka ettevõtte meiliaadressi, kuhu Microsoft saab saata teateid, mis on seotud juurutamise protsessiga.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Registreerumise ettepanek üürnikule.":::

Microsoft vaatab teie taotluse läbi ja teavitab teid järgmisest sammudest, saates e-kirja aadressile, kust saatsite registreerimise vormi. Microsoft teeb teiega tihedat koostööd, et lubada äristsenaariumi hübriidtopoloogias skaalaühikud.

Kui juurutamine on lõpule jõudnud, saate pordi abil konfigureerida mastaabiühikuid ja töökoormusi.

### <a name="manage-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a> Skaalaühikute ja töökoormuse haldamine skaala ühikuhalduri portaali abil

Avage [Scale Unit Manageri portaal](https://aka.ms/SCMSUM) ja logige sisse oma rentniku konto abil. Lehel **Skaalaüksuste konfigureerimine** saate lisada keskse keskkonna, kui see ei ole juba loetletud. Seejärel saate valida keskuse, mida soovite konfigureerida koos skaala ühikute ja töömahuga.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Skaala ühikuhalduri portaal, skaalaühikute konfigureerimise leht.":::

Ühe või mitme skaala üksuste lisamiseks, mis on saadaval teie tellimustel, valige **Lisa skaala ühikud**.

Vahekaardil **Määratletud töömahud** Kasutage **nuppu Loo töökoormus,** et lisada laohalduse töömaht ühte teie skaalajaotise üksustest. Iga töömahu puhul peate määrama töömahule kuuluvate protsesside konteksti. Laohalduse töökoormuste puhul on kontekst konkreetne ladu kindlas tegevuskohas ja juriidiline üksus.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="Töökoormuse dialoogi määratlemine.":::

#### <a name="manage-workloads"></a>Töökoormuse haldamine

Kui üks või mitme töökoormus on lubatud, kasutage **suvandi Töökoormuse haldamine,** et algatada ja hallata selliseid protsesse nagu need, mis on loetletud järgmises tabelis.

| Töötle | Kirjeldus |
|---|---|
| Skaalaüksuse suhtluse peatamine | Peatage konveierisõnumid jaoturi ja skaalaüksuse vahel. See protsess peatab suhtluse ja tühjendab andmetorustiku jaoturi ja skaalaüksuste vahel. Enne tarneahela halduse teenindustoimingu käivitamist kas jaoturis või skaalaüksuses peate selle protsessi käivitama, kuid võite seda kasutada ka muudes olukordades. |
| Skaalaüksuse kommunikatsiooni jätkamine | Jätkake konveieri sõnumeid jaoturi ja skaalaüksuse vahel. Võimalik, et peate seda protsessi kasutama näiteks pärast tarneahela halduse teenindustoimingu käivitamist kas jaoturis või skaalaüksuses. |
| Töökoormuse täiendamine | Sünkroonige uus funktsioon jaoturi ja skaalaühiku töökoormuse vahel. Võimalik, et peate seda protsessi kasutama näiteks siis, kui teenindus on põhjustanud andmevahetuspäringute muutumise ja/või lisanud töökoormusele uued tabelid või väljad. |
| Töökoormuse ülekandmine skaalaühikusse | Plaanige töökoormus, mis praegu töötab jaoturis, et teisaldada skaalaühikusse. Kui see protsess käivitatakse, voolab andmete sünkroonimine ning nii jaotur kui ka skaalaüksus seatakse töökoormuse omandiõiguse muutmiseks. |
| Skaalaüksuse ülekandmine jaoturisse | Plaanige töökoormus, mis töötab praegu jaoturisse teisaldatavate skaalaühikuga. Kui see protsess käivitatakse, voolab andmete sünkroonimine ning nii jaotur kui ka skaalaüksus seatakse töökoormuse omandiõiguse muutmiseks.
| Erakorraline üleminek keskusele | <p>Viige olemasolev töökoormus kohe jaoturisse. *See protsess muudab ainult praegu jaoturis saadaolevate andmete omandiõigust.*</p><p><strong>Hoiatus:</strong> see protsess võib põhjustada andmekadu sünkroonimata andmetele ja ettevõtte töötlemise nurjumist. Seetõttu tuleks seda kasutada ainult hädaolukordades, kus äriprotsesse tuleb töödelda jaoturis, sest skaalaüksusel on katkestus, mida ei saa mõistliku aja jooksul leevendada.</p> |
| Likvideerige hajutatud topoloogia | Eemaldage skaalaüksuse juurutamine ja käivitage ainult jaoturis ilma töökoormuse töötlemiseta. |

:::image type="content" source="media/sum-manage-workloads.png" alt-text="Skaala üksuse ja töömahu haldamise kogemus.":::

> [!TIP]
> Aja jooksul lisatakse skaala üksusehalduri kogemusele astmelised täiustused, mis aitavad elutsükli haldamise toiminguid lihtsustada. Praeguse väljalaske konkreetsed võimalused on dokumenteeritud juurutamise käsiraamatus, mis on saadaval klientidele, kes on käimas Supply Chain Management hajutatud hübriidtopoloogia juurutamisega. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
