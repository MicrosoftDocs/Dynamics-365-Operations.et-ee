---
title: Tehniliste toodete muudatuste haldamine
description: Teema annab teavet tehnilise muudatuse haldamise kohta. Tehnilise muudatuse haldamine pakub struktureeritud protsesse, et hallata muudatusi tehnilistes toodetes, alates ettepanekute tegemisest, taotlemisest ja muudatuste tegemisest kuni muudatuste läbivaatamiseni ja kinnitamiseni, nende mõju hindamiseni olemasolevatele tehingutele ning nende jälgimiseni.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8ae97d0e6aac1b0961427bd73a37612020231a9f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983796"
---
# <a name="manage-changes-to-engineering-products"></a>Tehniliste toodete muudatuste haldamine

[!include [banner](../includes/banner.md)]

Tehnilise muudatuse haldamine pakub struktureeritud protsesse tehniliste toodete muudatuste haldamiseks. Saate kasutada protsessi *tehnilise muudatuse taotlus*, et teha ettepanekuid ja taotleda muudatusi, ning seejärel kasutada protsessi *tehnilise muudatuste tellimus*, et neid muudatusi tegelikult teha. Kasutajad saavad luua tehnilise muudatuse taotlusi või tellimusi ning seejärel kasutada protsessi nende ülevaatamiseks ja kinnitamiseks, hinnates nende mõju olemasolevatele kannetele ja tehes järeltegevusi.

## <a name="engineering-change-requests"></a>Tehnilise muudatuse taotlused

Tehnilise muudatuse taotluse protsess võimaldab teil talletada kõigi teie ettevõtte asjakohaste osakondade muudatuse taotlusi. See ei ole oluline, kas töötate insenerina või tootmis-, hanke-, lao- või müügiosakonnas – igaüks saab kasutada tehnilise muudatuse taotlust muudatuse taotlemiseks. See muudatus võib olla idee uue toote jaoks, probleem, mis tuvastati olemasoleva tootega töötamise ajal, soovitus olemasoleva toote parandamiseks või midagi muud.

Pärast seda, kui keegi esitab muudatuse taotluse, haldab *läbivaatuse ja kinnitamise* protsessi töövoog, mis tuvastab inimese, kes peab muudatuse kinnitama (nt toote omanik).

Töövoo seadistamiseks tehnilise muudatuse tellimuste või taotluste jaoks minge **Tehnilise muudatuse haldamine \> Tehnilised töövood**. Valige **Uus**, valige, kas töövoogu kasutatakse tehnilise muudatuse tellimuste või taotluste ülevaatamiseks, ja seejärel konfigureerige töövoog.

Lisateavet töövoogudega töötamise kohta leiate teemast [Töövoosüsteemi ülevaade](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md). Lisateavet toote omanike kohta leiate jaotisest [Toote omanikud](product-owner.md).

### <a name="create-a-new-engineering-change-request"></a>Uue tehnilise muudatuse taotluse loomine

Tehnilise muudatuse taotluse loomiseks järgige ühte järgmistest meetoditest.

- Avage **Tehnilise muudatuse haldamine \> Ühine \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse taotlused** ja seejärel valige toimingupaanil suvand **Uus**.
- Avage olemasoleva tehnilise toote leht **Toote üksikasjad**. Seejärel valige toimingupaanil vahekaardil **Projekteerimine** grupis **Tehnilise muudatuse haldamine** suvand **Tehnilise muudatuse taotlus \> Uus tehnilise muudatuse taotlus**.

Luuakse uus muudatuse taotlus. Seejärel saate seadistada iga kiirkaardi väljad nii, nagu on kirjeldatud järgmistes alajaotistes.

#### <a name="general-fasttab"></a>Kiirkaart Üldine

Kiirkaart **Üldine** võimaldab teil lisada muudatuse taotlusele põhikirjelduse. Järgmises tabelis kirjeldatakse selle kiirkaardi välju.

| Väli | Kirjeldus |
|---|---|
| Muudatuse taotlus | Saate sisestada tehnilise muudatuse taotluse nime. |
| Nimetus | Sisestage tekst, mis kirjeldab või tuvastab lühidalt taotluse muudatusi. |
| Prioriteet | Valige väärtus, mis näitab, kui kõrge on muudatuse prioriteet. Saate vastavalt vajadusele kohandada oma ettevõtte jaoks saadaolevaid väärtusi. (Lisateavet leiate teemast [Tehnilise muudatuse haldamise jaoks ühiste väärtuste loomine](engineering-change-management-setup.md).) |
| Kategooria | Valige väärtus, mis kirjeldab teie taotletud muudatuse tüüpi. Saate vastavalt vajadusele kohandada oma ettevõtte jaoks saadaolevaid väärtusi. (Lisateavet leiate teemast [Tehnilise muudatuse haldamise jaoks ühiste väärtuste loomine](engineering-change-management-setup.md).) |
| Raskusaste | Valige väärtus, mis näitab selle probleemi raskusastet, mis tuleb taotluse rakendamise kaudu parandada. Saate vastavalt vajadusele kohandada oma ettevõtte jaoks saadaolevaid väärtusi. (Lisateavet leiate teemast [Tehnilise muudatuse haldamise jaoks ühiste väärtuste loomine](engineering-change-management-setup.md).) |
| Taotleja | Taotluse loonud kasutaja nimi. |
| Kuupäeval | Taotluse loomise kuupäev. |
| Olek | Taotluse olek. Kui taotlus esmalt luuakse, on selle olek *Loodud*. Kui taotlus kinnitatakse, muudetakse selle olekuks *Kinnitatud*. Kui taotluse jaoks on loodud seotud muudatuse tellimus, muudetakse selle olekuks *Hõlmab järeltegevust*. |
| Muudatuse tellimus | Muudatuse tellimuse number, kui muudatuse taotlusele järgnes muudatuse tellimus. |

#### <a name="information-fasttab"></a>Teabe kiirkaart

Kiirkaart **Teave** võimaldab teil lisada taotluse kohta lisateavet.

Rea lisamiseks ruudustikku valige ruudustiku kohal olevalt tööriistaribalt **Uus** ja seejärel valige üks järgmistest valikutest.

- **Fail** – laadige üles fail.
- **Pilt** – laadige üles pildifail.
- **Märge** – sisestage märge otse ruudustikku.
- **URL** – sisestage URL otse ruudustikku.

Järgmises tabelis kirjeldatakse iga rea välju.

| Väli | Kirjeldus |
|---|---|
| Loodud kuupäev ja kellaaeg | Rea loomise kuupäev ja kellaaeg. |
| Tüüp | Teabetüüp, mille jaoks rida loodi (fail, pilt, märge või URL). |
| Kirjeldus | Sisestage rea kirjeldus. |
| Piirang | Väärtus, mis näitab, kas lisatud teave pärineb sise- või välisest allikast. |
| Seotud | Valitud märkeruut näitab, et rida sisaldab manust (fail või pilt). Manuse allalaadimiseks valige rida ja seejärel valige ruudustiku kohal olevalt tööriistaribalt **Ava**. |

#### <a name="products-fasttab"></a>Toodete kiirkaart

Kiirkaardi **Tooted** abil saate loetleda iga toote, mida muudatuse taotlus mõjutab. Saate kasutada tööriistariba nuppe, et lisada tooteid ruudustikku või neid eemaldada.

Sellel loendil on ainult informatiivne eesmärk. Seetõttu saate lisada nii palju seotud tooteid, kui vajalikuks peate. Kui loote muudatuse taotluse lehel **Toote üksikasjad** olemasoleva toote jaoks, peaks see toode olema loetletud kiirkaardil **Tooted** pärast taotlusekirje salvestamist.

#### <a name="source-fasttab"></a>Allika kiirkaart

Kiirkaart **Allikas** võimaldab teil jälgida muudatuse taotluse lähtepunkti. See on kasulik näiteks juhul, kui soovite näha, kas muudatuse taotlus loodi müügitellimuse alusel, kes selle lõi ja millises ettevõttes see loodi.

### <a name="evaluate-the-business-impact-of-a-change-request"></a>Muudatuse taotluse ärimõju hindamine

Kui vaatate muudatuse taotlust läbi, saate otsida sõltuvusi. Sel viisil saate hinnata taotletud muudatuse mõju avatud kannetele, nagu näiteks müügitellimused, tootmistellimused ja vaba kaubavaru.

1. Valige **Tehnilise muudatuse haldamine \> Ühine \> Tehnilise muudatuse haldamine \> Tehnilise muudatuse taotlused**.
1. Avage olemasolev muudatuse taotlus või valige toimingupaanil **Uus**, et luua uus muudatuse taotlus.
1. Valige toimingupaanil vahekaardil **Muudatuse taotlus** grupis **Ärimõju** üks järgmistest nuppudest.

    - **Otsing** – skannib kõiki avatud kandeid ja avab seejärel dialoogiboksi **Ärimõju avatud kannetele**, kus loetletakse kõik kanded, mida muudatus mõjutab.
    - **Kuva eelmine otsing** – avage dialoogiboks **Ärimõju avatud kannetele**, kus loetletakse eelmise otsingu tulemused. (Uut otsingut ei tehta.)

1. Kui probleem, mis nõuab muutmist, leitakse olevat kriitiline, saate avatud kanded blokeerida või teavitada vastutavat kasutajat, kasutades tööriistariba nuppe dialoogiboksis **Ärimõju avatud kannetele**.

### <a name="create-a-change-order-from-a-change-request"></a>Muudatuse tellimuse loomine muudatuse taotluse põhjal

Insener, kes vaatab läbi tehnilise muudatuse taotlust, saab luua tehnilise muudatuse tellimuse otse lehel **Tehnilise muudatuse taotlused**. Valige toimingupaani vahekaardil **Muudatuse taotlus** grupis **Tehnilise muudatuse tellimus** suvand **Kopeeri link ja tooted**.

## <a name="engineering-change-orders"></a>Tehnilise muudatuse tellimused

Tehnilise muudatuse tellimused pakuvad struktureeritud protsessi tehniliste toodete muutmiseks. Muudatusettepanekuid saab teha kopeeritud tehnilisi andmeid kasutades. Tegelikke koondandmete ei mõjutata. Lisateavet tehniliste andmete kohta leiate teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).

Saate luua tehnilise muudatuse tellimuse, mis põhineb kinnitatud tehnilise muudatuse taotlusel. Insenerid saavad luua ka tehnilise muudatuse tellimusi nullist. Saate kaasata mitu toodet ühte tehnilise muudatuse tellimusse, toimides järgmiselt.

- Valige tooted käsitsi.
- Kasutage kooslust (BOM) selliste toodete kaasamiseks, mis on tootestruktuuris allpool (st tütarüksused).
- Kasutage kasutamiskohapõhist otsingut, et kaasata tootestruktuuris ülalpool olevad tooted (st emaüksused).

Kui muudatusettepanek on lõpule viidud, tegeleb läbivaatus- ja kinnitamisprotsessiga töövoog. Saate seadistada erinevaid töövooge prioriteedi ja raskusastme alusel.

Töövoo seadistamiseks tehnilise muudatuse tellimuste või taotluste jaoks minge **Tehnilise muudatuse haldamine \> Tehnilised töövood**. Valige **Uus**, valige, kas töövoogu kasutatakse tehnilise muudatuse tellimuste või taotluste ülevaatamiseks, ja seejärel konfigureerige töövoog.

Lisateavet töövoogudega töötamise kohta vt teemast [Töövoosüsteemi ülevaade](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

Siin on mõned tavalised huvirühmad, kes peavad võib-olla tehnilise muudatuse tellimust kinnitama.

- **Toote omanikud** – lisateavet toote omanike kohta leiate teemast [Toote omanikud](product-owner.md).
- **Vastutav meeskonnajuht** – tehnilise muudatuste tellimuse vaate **Päis** väljal **Insener** kuvatakse insener, kes lõi tehnilise muudatuse tellimuse. Kui tehnik kuulub süsteemi määratud töörühma, kuvatakse väljal **Vastutav isik** selle töörühma juht.
- **Finantsosakond** – finantsosakond peab võib-olla läbi vaatama juhtumid, kus muudatus hõlmab suuri kulusid.

Saate valida, kas tehnilise muudatuse tellimus tuleb töödelda töövoo osana vahetult pärast selle kinnitamist või hiljem käsitsi. Tehnilise muudatuse tellimuse töötlemisel uuendatakse tegeliku toote tehnilisi andmeid.

Kui vaatate muudatuse taotlust läbi, valige toimingupaanil kiirkaardil **Muudatuse taotlus** grupis **Ärimõju** suvand **Otsing**, et hinnata pakutud muudatuse mõju avatud kannetele, nagu näiteks müügitellimused, tootmistellimused ja vaba kaubavaru. Tulemused kuvatakse dialoogiboksis **Ärimõju avatud kannetele**, kus saate valida mõjutatud kanded ja seejärel kasutada tööriistariba käske, et vaadata lisateavet, teavitada vastutavat kasutajat või blokeerida kande.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Tehnilise muudatuse tellimused tehnika- või operatiivettevõtetes

Nagu on kirjeldatud teemas [Tehnikaettevõtted ja andmete omandiõiguse reeglid](engineering-org-data-ownership-rules.md), olenevad redigeeritavad tooteandmed juriidilise isiku tüübist, milles te töötate (tehnikaettevõte vs. operatiivettevõte). Andmete omandiõiguse reegleid rakendatakse ka tehnilise muudatuse tellimuste puhul. Seetõttu, sõltuvalt juriidilisest isikust, kus te loote tehnilise muudatuse tellimuse, saab teha erinevat tüüpi muudatusi. Järgmisena on toodud mõned näited.

- **Operatiivettevõtte** tehnilise muudatuse tellimuste korral saate tehnilisi andmeid vähe muuta. Näiteks saate luua tootele uusi versioone, muuta toote struktuuri koosluse kaudu ja muuta tehnilise atribuudi väärtusi. Iga mõjutatud toote puhul valige väljal **Mõju** üks järgmistest väärtustest.

    - **Pole** – värskendage olemasolevat tooteversiooni (versioonisisene värskendamine).
    - **Uus versioon** – looge uus versioon, mis põhineb valitud tooteversioonil.
    - **Uus toode** – looge täiesti uus toode või tootevariant, mis põhineb valitud tooteversioonil.

- **Operatiivettevõtte** tehnilise muudatuse tellimuste korral saate muuta toote logistilisi andmeid. Näiteks saate rikastada olemasolevat kooslust hankimissätetega, lisada kohalikke protsesse või kohalikke kooslusi ning isegi rikastada kooslust, lisades uusi koosluseridu kohaliku pakkematerjali, määrimisevedelike või kohalikus keeles juhiste jaoks. Rikastamised, mida kasutajad operatiivettevõttes teevad, säilitatakse uute värskenduste saatmisel tehnikaettevõttest. Lisateavet vt teemast [Tehnikaettevõtted ja andmete omandiõiguse reeglid](engineering-org-data-ownership-rules.md).

    Kui tehnilise muudatuse tellimusi töödeldakse tehnikaettevõttes, luuakse ja/või uuendatakse tooted ainult tehnikaettevõttes. Seega, kui toote koondandmeid tuleb värskendada, tuleb tooted ka operatiivettevõtetele väljastada.

- Tooteid saate väljastada otse tehnilise muudatuse tellimustest. Avage muudatuse tellimus ja seejärel valige toimingupaanil vahekaardil **Muudatuse tellimus** grupis **Tooteväljastused** suvand **Väljasta tootestruktuur**. Protsess toimib täpselt nii, nagu see toimib, kui väljastate tooteid lehelt **Väljastatud tooted**. Lisateavet leiate jaotisest [Tootestruktuuride vabastamine](release-product-structure.md).
- Saate lasta tooted automaatselt tehnilise muudatuse tellimustest väljastada järgmiste tegurite alusel.

    - Taasväljastamine ettevõtetele, millele tooted on varem väljastatud. Valige **Otsing**, et skannida kõiki eelmisi väljastamisi ja seejärel valige **Kuva** tulemuste vaatamiseks. Lehel **Kuvamine** kuvatakse eelmised tooteväljastused ja te saate valida, milliseid tooteid soovite uuesti väljastada. Seejärel sulgege leht **Kuvamine** ja valige **Töötle**, et valitud tooted uuesti väljastada.
    - Automaatse väljastamise sätted tehnilise toote kategooria väljastamise juhtimise vahekaardil. Saate väljastada töövoo osana. Kui kasutatakse plokki **väljastamise ettepaneku talletamine**, täidetakse väljastamise ettepanek taasväljastamise ettepanekutega (vt eelmist loendiüksust) ja tooted väljastatakse ettevõtetele, kui märkeruut **Automaatne väljastamine** on valitud tehnilise toote kategooria väljastamise juhtelemendis. Saate valida **Kuva**, et vaadata tulemusi, nagu on kirjeldatud eelmises loendiüksuses. Tooted väljastatakse ka siis, kui kasutatakse plokki **väljastamise ettepaneku töötlemine**. Kui soovite talletada väljastamise ettepanekut ainult töövoo osana, saate väljastamise käsitsi käivitada, valides **Töötle**, nagu on kirjeldatud eelmises loendiüksuses.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Tehnilise muudatuse taotluse järeltegevused tehnilise muudatuse tellimuse kaudu

Nii kui tehnilise muudatuse taotlus on kinnitatud, saate pärast seda luua tehnilise muudatuse tellimuse. Saate kombineerida mitu tehnilise muudatuse taotlust üheks tehnilise muudatuse tellimuseks. Üks tehnilise muudatuse tellimus võib sisaldada isegi mitut toodet. (Tavaliselt kasutate seda meetodit, kui sama muudatus tuleb rakendada mitmele tootele.) Samas ei saa ühe tehnilise muudatuse taotluse põhjal luua mitut tehnilise muudatuse tellimust.

Et luua muudatuse taotluse järeltegevusena muudatuse tellimus, avage muudatuse taotlus ja seejärel valige toimingupaanil vahekaardil **Muudatuse tellimus** grupis **Tehnilise muudatuse tellimus** suvand **Kopeeri link ja tooted**. Seejärel saate valida olemasoleva tehnilise muudatuse tellimuse, millega ühendada muudatuse taotlus, või luua uue tehnilise muudatuse tellimuse selle konkreetse taotluse jaoks.

## <a name="engineering-change-order-report"></a>Tehnilise muudatuse tellimuse aruanne

Tehnilise muudatuse tellimuse aruanded kirjeldavad muudatusi, mis tehti tehnilise muudatuse tellimuse põhjal. Need on kasulikud nii läbivaatus- ja kinnitamisprotsessi ajal kui ka pärast seda.

Et vaadata tehnilise muudatuse tellimuse aruannet, avage asjaomane muudatuse tellimus ja seejärel valige toimingupaanil vahekaardi **Muudatuse tellimus** grupis **Kuvamine** suvand **Tehnilise muudatuse tellimuse aruanne**.

## <a name="fields-on-an-engineering-change-order"></a>Tehnilise muudatuse tellimuse väljad

Suurem osa tehniliste muudatuste tellimuste väljadest on samad, mis on saadaval väljastatud toodetes, tehnilistes versioonides, dokumentides, kooslustes (read) ja protsessides (toimingud). Siiski on järgmise tabeli väljad saadaval ainult muudatuse tellimustes.

| Väli | Kirjeldus |
|---|---|
| Tehnilise muudatuse põhjused | Valige mõjutatud toote muutmise põhjus. |
| Muudatuse kirjeldus | Sisestage muudatuse kirjeldus. |
| Nõutav spetsiaalne tööriist | Määrake, kas muudatuse rakendamiseks on vaja spetsiaalset tööriista. |
| Tehnilise materjali likvideerimine | Valige materjalilikvideerimiskood mis tahes jäätmete jaoks, mida toodetakse muudatuse rakendamisel. |
| Kliendi nõusolek on vajalik | Määrake, kas kliendi nõusolek on vajalik enne muudatuse rakendamist. |
| Saadud kliendi nõusolek | Määrake kliendi nõusoleku olek. |
| Keskkonnatervis ja -ohutus | Määrake, kas muudatuse korral rakendatakse keskkonnatervise ja -ohutuse reegleid. Kui jah, saate valida kohaldatavad reeglid. |

Saate kasutada nuppu **Halda/kopeeri muudatuse teave**, et kopeerida muudatuse teavet mõjutatud toodete vahel.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]