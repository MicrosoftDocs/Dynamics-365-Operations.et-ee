---
title: Toote struktuuride vabastamine
description: Selles teemas selgitatakse, kuidas saate vabastada lõpptoote struktuurid lisaks toodete vabastamisele koos nende tehniliste versioonidega. Sel viisil saate tagada, et tehnilise poolega seotud tooteandmeid saab hõlpsasti kasutada erinevates juriidilistes isikutes.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 1134b24aa3f7ada72ba837b525d2cea33b3e6287da0f8611f60152672c1ee6f4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743622"
---
# <a name="release-product-structures"></a>Toote struktuuride vabastamine

[!include [banner](../includes/banner.md)]

Tagamaks, et tehnilise poolega seotud tooteandmeid saab hõlpsalt kasutada erinevates juriidilistes isikutes, saate lisaks toodete tootmisele ja nende tehnilistele versioonidele väljastada ka täielikke toote struktuure. Seetõttu saate ühe väljastamise toiminguga anda koos põhitootega väljastada mitmetasandilise koosluse struktuurid. Sel juhul väljastatakse ka kooslused ja madalama taseme tooted.

Insener-tooteid loovad ja haldavad nende inseneride ettevõte viisil, mis vastab kvaliteedinõuetele, nagu need on kavandatud. Iga ettevõte, mis toodab toodet, vajab sama toodet ja aluseks olevat kooslust. Sõltuvalt tootmisüksusest võib protsessi luua kohalikult. Sel juhul ei väljasta te protsessi koos tootega. Juriidilistel isikutel, kes müüvad tooteid, kuid ei valmista neid, ei pruugi kooslus vajalik olla.

Et muuta protsess tõhusamaks, saab kõiki tehnilisele tegevusele vastavaid andmeid väljastatakse samaaegselt ka teistele ettevõtetele. Need andmed sisaldavad toote struktuuri. Väljastamise protsessi käigus saate valida, millist osa toote teabest tuleks väljastada.

Tehnikaettevõte ja operaatorettevõtete kohta lisateabe saamiseks vt [Tehnikaettevõtted ja andmete omandiõiguse reeglid](engineering-org-data-ownership-rules.md).

Pange tähele, et saate väljastada nii standardseid tooteid kui ka tehnilisi tooteid koos väljastatava toote struktuuriga. Selle protsessi käigus väljastatakse toote väljastavast ettevõttest kogu toote struktuur ning isegi kooslus ja protsess.

Teavet toote väljastamise kohta vt teemast [Tehnilise toote väljastamine kohalikule ettevõttele](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Väljastatud andmed toote kohta, kui kasutatakse väljastatud toote struktuuri

Tehniliste toodete väljastamine sisaldab järgmisi andmeid:

- **Toote andmed** – Luuakse uus väljastatud toode.
- **Tehnilise versiooni andmed** – Tehniline versioon ja selle andmed on loodud või uuendatud. Pidage meeles, et kui väljastate operaatorettevõttele uuesti sama tehnilise versiooni, kirjutatakse tehnilised andmed üle.
- **Tehnilised atribuudid** – Luuakse või uuendatakse tehnilisi atribuute ja nende väärtusi.
- **Tehniline kooslus** – Luuakse või uuendatakse tehnilist kooslust. Lisateavet andmete omandiõiguse kohta leiate lõigust [Toote omanikud](product-owner.md).
- **Tehnilised protsessid** – Luuakse või uuendatakse tehnilisi protsesse ja nende operatsioone. Lisateavet andmete omandiõiguse kohta leiate lõigust [Toote omanikud](product-owner.md).
- **Tehnilised dokumendid** – Luuakse või uuendatakse tehnilisi dokumente, mis on seotud tehnilise versiooniga.

Kui lülitate süsteemil sisse tehniliste muutuste halduse, on saadaval väljastatud toote struktuur. Lisaks sisaldavad standardsed tooted väljastamisel nende kooslust ja protsesse.

## <a name="product-acceptance"></a>Toote aktsepteerimine

**Toote kinnitamine** on võtmeparameeter, mis mõjutab väljastamisprotsessi. Saate seada selle parameetri igale ettevõttele, minnes **Tehniliste muudatuste haldus \> Seadistamine \> Tehniliste muudatuste halduse parameetrid**. Lisateavet vt teemast [Tehniliste muudatuste haldamise parameetrid](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Toote automaatne kinnitamine

Tehniliste toodete iga väljastamine algab siis, kui keegi tehnikaettevõttest valib väljastamiseks toote. Kui **Toote kinnitamine** parameeter on seatud olekusse *Automaatne*, otsustab tehnikaettevõttes asuv kasutaja, milliseid toote andmeid tuleks automaatselt operatiivsetele ettevõtetele väljastada. Seejärel väljastatakse toode automaatselt ettevõtetele, mis on valitud väljastamisviisardis.

### <a name="manual-product-acceptance"></a>Toote käsitsi kinnitamine

Tehniliste toodete iga väljastamine algab siis, kui keegi tehnikaettevõttest valib väljastamiseks toote. Kui **Toote kinnitamine** parameeter on seatud olekusse *Käsitsi*, otsustab tehnikaettevõttes asuv kasutaja, milliseid toote andmeid tuleks operatiivsetele ettevõtetele väljastada. Iga operatiivettevõtte kasutaja vaatab seejärel üle toote andmed ja otsustab, kas lubada väljastamist. Kui andmed on vastu võetud, saab operatiivettevõtte kasutaja seadistada järgmised valikud:

- Kui tooted (uuendused) ei ole operatiivettevõtte puhul asjakohased, saab kasutaja valida selle väljastamist mitte kinnitada.
- Kasutaja saab muuta kauba malli uute toodete jaoks.
- Kasutaja saab valida, kas toode tuleks väljastada koos koosluste ja/või protsessidega ning kas need tuleks väljastada kinnitatud ja aktiivsena.
- Kasutaja saab muuta toodete kehtivuse alguse kuupäevi.

Lisateavet toote kinnitamise kohta vaadake teemast [Toote ülevaatamine ja kinnitamine enne kohalikus ettevõttes väljastamist](engineering-scenarios.md#accept).

> [!NOTE]
> Standardsete toodete puhul saate väljastada mis tahes juriidilisest isikust mis tahes teisele juriidilisele isikule. Tehniliste toodete puhul on ainus juriidiline isik, kust saate väljastada, tehnikaettevõte.

## <a name="release-policies"></a>Väljastamispoliitikad

Kõik operatiivettevõtted ei vaja samu toote andmeid. Üldiselt nõuavad tehnilisi tooteid tootvad operatiivettevõtted kooslusi, samas kui operatiivettevõte, mis tehnilisi tooteid ainult müüb, kooslusi ei vaja. Saate kasutada väljastamispoliitikaid, et luua parameetreid, mida kasutatakse toodete väljastamiseks.

Lisateavet tehniliste toodete kategooriate kohta leiate teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).

Väljastamisprotsessi ajal saate sätteid mõjutada.

## <a name="create-and-manage-product-release-policies"></a>Toote väljastamispoliitikate loomine ja haldamine

Toote väljastamispoliitikatega töötamiseks valige **Tehniliste muutuste haldus \> Häälestus \> Toote väljastamispoliitikad**. Seejärel järgige üht neist sammudest.

- Uue poliitika loomiseks valige tegumiriba nupp **Uus** ja seejärel häälestage väljad, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva poliitika redigeerimiseks valige see loendipaanil, valige tegumiribal nupp **Redigeeri** ja seejärel häälestage väljad nii, nagu on kirjeldatud järgmistes lõikudes.
- Olemasoleva poliitika kustutamiseks valige see loendipaanil, valige tegumiribal käsk **Redigeeri** ja seejärel veenduge, et **Üldine** FastTab-is on suvandi **Aktiivne** valikuks seatud *Ei*. Seejärel valige tegumiribal suvand **Kustuta**.

### <a name="header"></a>Päis

Häälestage järgmised väljad toote väljastamispoliitika päises.

| Field | Kirjeldus |
|---|---|
| Nimi | Sisestage poliitika nimi. |
| Kirjeldus | Sisestage poliitika kirjeldus. |

### <a name="general-fasttab"></a>Kiirkaart Üldine

Seadistage toote väljastamispoliitika **Üldine** FastTab-is järgmised seaded.

| Field | Kirjeldus |
|---|---|
| Toote tüüp | Valige, kas poliitika rakendub *kauba* või *teenuse* tüübi toodetele. Pärast kirje salvestamist ei saa seda sätet muuta. |
| Tootmise tüüp | See valik kuvatakse ainult siis, kui olete süsteemis lubanud [valemi muutmise halduse](manage-formula-changes.md). Valige tootmise tüüp, mille suhtes see tehnika tootekategooria kehtib:<ul><li>**Kaastoode** – kasutage seda väljalaske poliitikat kaastoodete haldamiseks. Kaastooted toodetakse protsessi tootmise ajal ja neid ei ole versioonitud ega tehnika tooteid. Kaastoodete vabastuspoliitikad aitavad kindlustada oluliste sätete nagu **Laoala dimensioonigrupi** ja **Jälgimisdimensiooni grupi** häälestamist väljastatud tootemalli abil, enne kui need ettevõttele lastakse.</li><li>**Kaastoode** – kasutage seda väljalaske poliitikat kaastoodete haldamiseks. Kaastooted toodetakse protsessi tootmise ajal ja neid ei ole versioonitud ega tehnika tooteid. Kaastoodete vabastuspoliitikad aitavad kindlustada oluliste sätete nagu **Laoala dimensioonigrupi** ja **Jälgimisdimensiooni grupi** häälestamist väljastatud tootemalli abil, enne kui need ettevõttele lastakse.</li><li>**Pole** – kasutage seda poliitikat standardsete toodete haldamiseks, mis pole versioonitud või tehnikatooted, kaastooted või by-tooted.</li><li>**Kauba plaanimine** - Kasutage seda väljalaskepoliitikat protsessi tootmise abil toodetud kaupade plaanimise haldamiseks. Plaanimisüksused kasutavad valemeid. Need sarnanevad valemiüksustega, kuid neid kasutatakse ainult kaastoodete ja kaastoodete tootmiseks, lõpetamata toodete tootmiseks.</li><li>**Koostis** - Kasutage seda tehnika kategooriat, et hallata tehnika tooteid, mis ei kasuta valemeid ja sisaldavad tavaliselt (kuid mitte tingimata) koostises.</li><li>**Valem** - Kasutage seda väljalaskepoliitikat protsessi tootmise abil toodetud kaupade plaanimise haldamiseks. Nendel üksustel on valem, kuid mitte BOM.</li></ul> |
| Rakenda mallid | Valige üks järgmistest suvanditest, et määrata, kas ja kuidas tuleks poliitika kasutamise toote väljastamise malle rakendada:<ul><li>**Alati** – Väljastamiseks tuleb alati kasutada väljastatud toote malli. Kui valite selle suvandi, kasutage **Kõikide toodete** FastTab-i, et määrata mall, mida kasutatakse iga ettevõtte puhul, millele te väljastate. Kui te ei määra iga ettevõtte jaoks malli, mis on loetletud **Kõikide toodete** FastTab-is, kuvatakse tõrge, kui püüate poliitikat salvestada.</li><li>**Valikuline** – Kui väljastatud toote mall on määratud ettevõttele, mis on loetletud **Kõikide toodete** FastTab-is, kasutatakse seda malli sellele ettevõttele väljastamisel. Muul juhul malli ei kasutata. Selle suvandi valimisel saate poliitika salvestada kõikidele ettevõtetele malle määramata. (Hoiatust ei kuvata.)</li><li>**Mitte kunagi** – Väljastatud toote malli ei kasutata mitte ühegi ettevõtte puhul, kellele väljastatakse, isegi mitte siis, kui mall on määratud ettevõttele, mis on loetletud **Kõikide toodete** FastTab-is. Malli veerud ei ole saadaval.</li></ul> |
| Aktiivne | Kasutage seda suvandit, et aidata säilitada väljastamispoliitikaid. Seadistage see kõigi kasutatavate väljastamispoliitikate puhul valikule *Jah*. Seadistage see valikule *Ei*, et tähistada väljastamispoliitikat passiivsena, kui seda ei kasutata. Võtke arvesse, et te ei saa aktiveerida väljastamispoliitikat, mis on määratud tehniliste toodete kategooriale, ja saate kustutada ainult passiivse väljastamispoliitika. |

### <a name="all-products-fasttab"></a>Kõikide toodete FastTab

Lisage **Kõikide toodete** FastTab-is rida igale operatiivettevõttele, kellel soovite seda poliitikat kasutada. Kasutage järgmisi nuppe **Kõik tooted** FastTab-is, et lisada ja eemaldada ridu, mida vajate. Iga lisatava rea jaoks määrake järgmised väljad.

> [!NOTE]
> **Kõigi toodete** FastTab-is olevad seaded kehtivad nii tehniliste toodete kui ka standardsete toodete puhul.

| Field | Kirjeldus |
|---|---|
| Ettevõtte ID | Valige ettevõte, millele rida kehtib. Rea parameetreid rakendatakse, kui tooted väljastatakse sellele ettevõttele. |
| Malli väljastatud toode | Toote malli sisestamine. |
| Kopeeri koosluse kinnitus | Valige see märkeruut koosluse kinnitamise oleku kopeerimiseks vastuvõtvale ettevõttele. |
| Kopeeri koosluse aktiveerimistoiming | Valige see märkeruut koosluse aktiveerimise oleku kopeerimiseks vastuvõtvale ettevõttele. |
| Kopeeri protsessi kinnitus | Valige see märkeruut protsessi kinnitamise oleku kopeerimiseks vastuvõtvale ettevõttele.|
| Kopeeri protsessi aktiveerimistoiming | Valige see märkeruut protsessi aktiveerimise oleku kopeerimiseks vastuvõtvale ettevõttele. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Tehniliste toodete FastTab-i valiku parameetrid

Iga kord, kui lisate rea **Kõik tooted** FastTab-i, luuakse samuti sama **Ettevõtte konto ID** väärtusega rida **Tehniliste toodete valiku parameetrite** FastTab-i. Kui te kustutate rea **Kõik tooted** FastTab-ist, kustutatakse samuti sama **Ettevõtte konto ID** väärtusega rida **Tehniliste toodete valiku parameetrite** FastTab-ist.

Iga rea puhul, mis kuvatakse **Tehniliste toodete valiku parameetrid** FastTab-is, määrake järgmised väljad.

> [!NOTE]
> **Tehniliste toodete valiku parameetrid** FastTab-i seaded rakenduvad ainult tehnilistele toodetele.

| Field | Kirjeldus |
|---|---|
| Mallkooslus | Kui väljastatakse kooslusega toode, lisatakse määratud malli koosluse read. See väli on kasulik kohalike komponentide, nt pakendi või juhiste lisamiseks kohalikus keeles. |
| Malli protsess | Kui väljastatakse protsessiga toode, lisatakse määratud malli vastavad read. |
| Koopia kehtivus | Valige, kas kehtivuskuupäevad tuleb toote väljastamisel kopeerida tehnilisest ettevõttest operatiivettevõttesse. |
| Väljastuse soovitusele automaatselt lisamine | Valige see märkeruut toodete puhul, mis tuleks automaatselt väljastada tehniliste muutmise tellimusel. Sel viisil saab tooteid, mis kuuluvad tehniliste toodete kategooriasse, mis kasutavad seda väljastamispoliitikat, automaatselt väljastada operatiivettevõtetele, kus see valik on seadistatud. (Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Kõigi toodete läbivaatamine väljastamisel

Kui väljastatakse koosluste või protsessidega tehnilised tooted, seatakse parameetrite vaikeväärtused, nagu on näidatud väljastamispoliitikas. Kasutajana saate seda käitumist mõjutada, kui kasutate toote struktuuri väljastamist.

**Väljastatud toodete** lehel tehniliste toodete väljastamiseks valige väljastamiseks tooted ja seejärel valige väljastamisviisardi avamiseks **Väljasta toote struktuur**. **Vali väljastamiseks tehnilised tooted** leht näitab tooteid. Valige üks toode ja seejärel valige **Väljastamise üksikasjad**, et vaadata üle toote väljastamise üksikasjad.

**Väljastamise üksikasjad** lehel saate muuta suvandi **Koosluse vastuvõtt** väärtust, **Kopeerida koosluse kinnitust**, **Kopeerida koosluse aktiveerimist**, **Võtta kooslus vastu**, **Kopeerida protsessi kinnitust** ja **Kopeerida protsessi aktiveerimise** välju. Lükka-tõmba stsenaariumi puhul saate muuta samade väljade väärtust vastuvõtval poolel, tingimusel et kooslus ja protsess on väljastatud.

## <a name="product-owners-and-product-releases"></a>Toote omanikud ja toote väljalasked

Kuna toote omanikud teavad, millised juriidilised isikud vajavad nende tooteid, saab toote väljastada ainult selle toote omaniku grupi liikmed. Teised kasutajad ei saa väljastada tooteid, mida nad ei oma.

Selline käitumine rakendub ainult siis, kui toode on otseselt väljastamiseks valitud. Tooteid, mis on mõne teise toote struktuuri osa koosluse kaudu, *saavad* väljastada mitte-omanikust kasutajad, kui nad väljastavad põhitoote.

Näiteks toode X on määratud *Disainkappide* toote omaniku grupile. Toode X on ühtlasi osa toote Y kooslusest, mis on määratud *Disainkõlarid* toote omaniku grupile. Kui tooteomaniku grupi *Disainkõlarid* kasutaja väljastab toote Y ja selle koosluse, väljastatakse toode X koos tootega Y.

Lisateavet vt jaotisest [Toote omanikud](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
