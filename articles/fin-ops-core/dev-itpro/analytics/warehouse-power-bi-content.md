---
title: Laojõudluse Power BI sisu
description: See teema kirjeldab, mida hõlmab laojõudluse Power BI sisu.
author: Mirzaab
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWarehousePerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 272953
ms.assetid: 4e4d4323-78cf-4ffa-8d5a-05e856c33db6
ms.search.region: Global
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b07d4516144accec1c41728876df7f6a64c6bae0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754164"
---
# <a name="warehouse-performance-power-bi-content"></a>Laojõudluse Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **Lao jõudluse** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Laojõudluse** Power BI sisu loodi selleks, et lao- ja toiminguhaldurid saaksid jälgida olulisi sissetulevaid, väljaminevaid ning varude parameetreid. See kasutab laohalduse, toote ja muid kandeandmeid teie süsteemist ning pakub hankijatele, tootegruppidele ja toodetele ning tegevuspaikadele ja ladudele nii laojõudluse koondvaadet kui ka jaotusstruktuuri.

Laohaldurid saavad **laojõudluse** Power BI sisu abil mõõta kolme järgmist valdkonda.

- **Sissetulev jõudlus** – saate mõõta hankija jõudlust kliendi vajaduste suhtes (ehk mõõta tarnejõudlust) ja ladustamisjõudlust, et saaksite tuvastada töötajate või kaupadega teatud perioodil ilmnevaid probleeme. Oluline on teada, kas hankijad tarnivad õigel ajal, vara või hilja, et saaksite välja selgitada, kuidas mõjutab hankija jõudlus üldist ladustamisjõudlust. Hankija, kes tarnib väljaspool kokkulepitud kuupäevi, võib ootamatu töö tõttu seada lao surve alla ja suurendada keskmist ladustamisaega.
- **Lähetamisjõudlus** – saate mõõta, kas teie ladu lähetab klientidele täielikult ja õigel ajal (ehk mõõta väljaminevat lähetamis- ja tarnejõudlust), et saaksite tuvastada tooteid, tegevuskohti või ladusid puudutavaid võimalikke probleeme või asjassepuutuvaid kliente. Kui leiate, et lähetate teatud piirkondadesse või linnadesse hilja, peate ehk pöörama suuremat tähelepanu transpordile või kontohaldusele.
- **Asukoha varude täpsus** – varude täpsus on oluline siselao äriteave (BI). Väga oluline on välja selgitada, kui täpselt te üldiselt arvestate. Siiski on oluline ka välja selgitada, kui täpne te olete kaupade hoidmisel õigetes asukohtades, ja et tõstaksite lahknevusandmed esile,e t saaksite leida kaupade jaoks paremaid asukohti või algatada kindlate kaupade koguinventuuri. (Praegu pakutakse uut kaubapõhist inventuurifunktsiooni kiirparandusena.) Kui kasutate seda Power BI sisu vaba kaubavaru andmete õigsuse kindlaks tegemiseks asukohtade kaupa, saate tuvastada ka vargust oma kauplustes. Samuti saate välja selgitada, kas mõnes asukohas on vaba kaubavaru koguseid, mis erinevad ettevõtte ressursiplaanimise (ERP) andmetest. Need asukohad võivad olla liiga suured või on nende loendamine võimatu. Teise võimalusena võib osa füüsilisest paigutamisest olla halb, nii et üht tüüpi kauba hoidmine sünkroonis vaba kaubavaru andmetega on keeruline.

## <a name="accessing-the-power-bi-content-pack"></a>Juurdepääs Power BI sisupaketile
**Laojõudluse** Power BI sisu kuvatakse lehel **Laojõudlus** (**Laohaldus** \> **Päringud ja aruanded** \> **Tootmise jõudlusanalüüs** \> **Laojõudlus**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud
**Laojõudluse** Power BI sisu hõlmab aruannet. See aruanne koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate **laojõudluse** Power BI sisu visualiseerimistest.

| Aruandeleht                 | Diagrammid                                   | Kirjeldus |
|-----------------------------|------------------------------------------|-------------|
| Sissetulev jõudlus         | Ladustamised kokku                          | Kindlal ajal töödeldavate ladustamise tööridade arv. |
| Sissetulev jõudlus         | Keskmine ladustamisaeg                    | Keskmine aeg tundides kõigi ostutellimuse töödeldud ladustamisridade kohta alates kaupade registreerimisest kuni viimase ladustamise töötlemise lõpuni. |
| Sissetulev jõudlus         | Saadud varakult                           | Vara sissetulnud ostutellimuse ridade arv. |
| Sissetulev jõudlus         | Saadud tähtaegselt                         | Õigel ajal sissetulnud ostutellimuse ridade arv. |
| Sissetulev jõudlus         | Saadud hilinemisega                            | Hilja sissetulnud ostutellimuse ridade arv. |
| Sissetulev jõudlus         | Õigel ajal hankija järgi                        | Hankijalt või hankijagrupilt vara, õigel ajal ja hilja sissetulnud ostutellimuse ridade protsendiline vaade. |
| Sissetulev jõudlus         | Dokist lattu keskmine ladustamisaeg (tundides) | Dokist lattu keskmine ladustamisaeg tundides teatud aja jooksul. |
| Sissetulev jõudlus         | Keskmine ladustamisaeg töötaja järgi               | Keskmine aeg tundides, mis on töötajal kulunud ostutellimuse ridade ladustamistöötluseks. |
| Sissetulev jõudlus         | Keskmine ladustamisaeg hankija järgi          | Keskmine ladustamisaeg tundides hankija või hankijagrupi järgi. |
| Sissetulev jõudlus         | Keskmine ladustamisaeg toote järgi         | Keskmine ladustamisaeg tundides kauba või kaubagrupi järgi. |
| Asukoha varude täpsus | Kogus kokku                              | Kindlal perioodil töödeldavate inventuuri tööridade arv. |
| Asukoha varude täpsus | Lahknevusmäär                         | Lahknevuse kogumäär on kõigi teatud perioodi kohta loendatud ridade protsent. |
| Asukoha varude täpsus | Arv ilma lahknevuseta                | Lahknevuseta töödeldud ridade arv töödeldud inventuuri tööridade koguarvust. |
| Asukoha varude täpsus | Aja jooksul loendatud kaubad                  | Teatud aja jooksul lahknevusega ja lahknevuseta loendatud kaupade protsent. |
| Asukoha varude täpsus | Kaubakoguse suurem lahknevus kui teatud % | Tabelivaate inventuuriridadest, mille lahknevus ületab teatud protsenti. Tabel sisaldab teavet asukohtade, kaupade, keskmise lahknevuse, loendatud inventuuri tööridade koguarvu, asukoha puhul lahknevate inventuuriridade arvu, keskmise loendatud koguse, loendatava eeldatud tervikkoguse ja loendatud kaupade tegelike koguse kohta. |
| Asukoha varude täpsus | Kaupade arv töötaja järgi                     | Töötajate inventuurijõudlus. Jõudlust väljendatakse lahknevusega ja lahknevuseta inventuuri tööridade protsendina. |
| Asukoha varude täpsus | Kaupade arv tegevuskoha/lao järgi           | Inventuurijõudlus töödeldud inventuuritöö lahknevustega ja lahknevusteta ridade arvu järgi tegevuskoha või lao kaupa. |
| Asukoha varude täpsus | Lahknevusmäär toote järgi              | Inventuurijõudluse lahknevusmäär. Määra väljendatakse töödeldud inventuuri tööridade protsendina kauba või kaubagrupi järgi. |
| Lähetusjõudlus        | Lähetatud read                            | Kindlal perioodil lähetatavate lähetusridade koguarv. |
| Lähetusjõudlus        | Varajane                                    | Vara lähetatud lähetusridade protsent. |
| Lähetusjõudlus        | Õigeaegne                                  | Õigel ajal lähetatud lähetusridade protsent. |
| Lähetusjõudlus        | Hilja                                     | Hilja lähetatud lähetusridade protsent. |
| Lähetusjõudlus        | Saadetised teatud aja jooksul                      | Teatud perioodi jooksul õigel ajal, vara või hilja lähetatud lähetusridade protsent. Trendireal kuvatakse õigel ajal lähetatud ridade trend. |
| Lähetusjõudlus        | Hilja lähetatud linna järgi                     | Hilisest lähetamisest mõjutatud linnade ja piirkondade kaardivaade. |
| Lähetusjõudlus        | Lähetatud toote järgi                       | Vara, õigel ajal või hilja lähetatud protsent kauba või kaubagrupi järgi. |
| Lähetusjõudlus        | Lähetatud kliendi järgi                      | Vara, õigel ajal või hilja lähetatud protsent kliendi või kliendigrupi järgi. |
| Lähetusjõudlus        | Lähetatud tegevuskoha/lao järgi              | Vara, õigel ajal või hilja lähetatud protsent tegevuskoha või lao järgi. |

## <a name="understanding-the-data-model-and-calculations"></a>Andmemudeli ja arvutuste põhimõte
Aruandelehtede täitmiseks **laojõudluse** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Power BI integratsioon üksuse kauplusega](power-bi-integration-entity-store.md).

Sisu alusena kasutatakse järgmisi peamisi koondmõõtmisi.

| Aruandeleht                 | Diagrammid                                   | Tabelid                                | Arvutuste kirjeldused |
|-----------------------------|------------------------------------------|---------------------------------------|--------------------------|
| Sissetulev jõudlus         | Ladustamised kokku                          | WHSWorkLine                           | Tööridade arv, mille töötüüp on **panek**. |
| Sissetulev jõudlus         | Keskmine ladustamisaeg                    | WHSWorkLine                           | Tööridade maksimaalse aja summa jagatud tööridade maksimaalse aja arvuga, kus tööridade maksimaalne aeg on maksimaalne vahe töö loomiskuupäeva ja sulgemiskuupäeva vahel. |
| Sissetulev jõudlus         | Saadud varakult                           | WHSWorkLine                           | Tööridade arv, kus töö loomiskuupäev on varasem kui kasutatud tarnekuupäev. Kui tarnekuupäev pole määratud, kasutage vaike-tarnekuupäeva. |
| Sissetulev jõudlus         | Saadud tähtaegselt                         | WHSWorkLine                           | Tööridade arv, kus töö loomiskuupäev on võrdne kasutatud tarnekuupäevaga. Kui tarnekuupäev pole määratud, kasutage vaike-tarnekuupäeva. |
| Sissetulev jõudlus         | Saadud hilinemisega                            | WHSWorkLine                           | Tööridade arv, kus töö loomiskuupäev on hilisem kui kasutatud tarnekuupäev. Kui tarnekuupäev pole määratud, kasutage vaike-tarnekuupäeva. |
| Sissetulev jõudlus         | Õigel ajal hankija järgi                        | WHSWorkLine                           | Vara sissetulnud, Õigel ajal sissetulnud ja Hilja sissetulnud (vt kirjeldusi tabelis eestpoolt). |
| Sissetulev jõudlus         | Dokist lattu keskmine ladustamisaeg (tundides)   | WHSWorkLine                           | Keskmine ladustamisaeg (vt kirjeldust tabelis eestpoolt). |
| Sissetulev jõudlus         | Keskmine ladustamisaeg töötaja järgi               | WHSWorkLine                           | Keskmine ladustamisaeg (vt kirjeldust tabelis eestpoolt). |
| Sissetulev jõudlus         | Keskmine ladustamisaeg hankija järgi          | WHSWorkLine                           | Keskmine ladustamisaeg (vt kirjeldust tabelis eestpoolt). |
| Sissetulev jõudlus         | Keskmine ladustamisaeg toote järgi         | WHSWorkLine                           | Keskmine ladustamisaeg (vt kirjeldust tabelis eestpoolt). |
| Asukoha varude täpsus | Kogus kokku                              | WHSWorkLineCycleCount                 | Tsüklilised inventuurid, kus absoluutse lahknevuse kogus on võrdne või suurem kui 0 (null). |
| Asukoha varude täpsus | Lahknevusmäär                         | WHSWorkLineCycleCount                 | Lahknevustega tsüklilised arvud jagatud koguarvuga. Tsüklilise arvu puhul eeldatakse lahknevusi, kui absoluutse lahknevuse kogus on suurem kui 0 (null). |
| Asukoha varude täpsus | Inventuur ilma lahknevuseta                | WHSWorkLineCycleCount                 | Tsüklilised inventuurid, kus absoluutse lahknevuse kogus on suurem kui 0 (null). |
| Asukoha varude täpsus | Inventuur koos lahknevusega                   | WHSWorkLineCycleCount                 | Tsüklilised inventuurid, kus absoluutse lahknevuse kogus võrdub 0 (null). |
| Asukoha varude täpsus | Aja jooksul loendatud kaubad                  | WHSWorkLineCycleCount                 | Inventuuri ilma lahknevuseta ja inventuur koos lahknevusega (vt kirjeldusi tabelis eestpoolt). |
| Asukoha varude täpsus | Kaubakoguse suurem lahknevus kui teatud % | WHSWorkLineCycleCount                 | Keskmine lahknevus on absoluutse lahknevuse kogus jagatud eeldatud kogusega, kus absoluutse lahknevuse kogus on suurem kui 0 (null). Keskmise lahknevuse kogus on keskmine absoluutse lahknevuse kogus, kus absoluutse lahknevuse kogus on suurem kui 0 (null). Inventuur koos lahknevusega, Koguarv, Eeldatud kogus ja Loendatud kogus, kus täielik kogus on grupeeritud kaupade ja asukohtade järgi (vt kirjeldusi tabelis eestpoolt). |
| Asukoha varude täpsus | Kaupade arv töötaja järgi                     | WHSWorkLineCycleCount                 | Inventuuri ilma lahknevuseta ja inventuur koos lahknevusega (vt kirjeldusi tabelis eestpoolt). |
| Asukoha varude täpsus | Kaupade arv tegevuskoha/lao järgi           | WHSWorkLineCycleCount                 | Inventuuri ilma lahknevuseta ja inventuur koos lahknevusega (vt kirjeldusi tabelis eestpoolt). |
| Asukoha varude täpsus | Lahknevusmäär toote järgi              | WHSWorkLineCycleCount                 | Lahknevusmäär (vt kirjeldust tabelis eestpoolt). |
| Lähetusjõudlus        | Lähetatud read                            | SalesLine               | Lähetatud müügiridade arv. |
| Lähetusjõudlus        | Varajane                                    | CustPackingSlipOnTimeStatus           | Müügiread, mille lähetuskuupäeva olek on **1 (vara)**. „Vara” tähendab, et saatelehe lähetuskuupäev on varasem kui müügirea kinnitatud lähetuskuupäev. Kui kinnitatud lähetuskuupäev pole määratud, kasutage nõutud lähetuskuupäeva. |
| Lähetusjõudlus        | Õigeaegne                                  | CustPackingSlipOnTimeStatus           | Müügiread, mille lähetuskuupäeva olek on **2 (õigel ajal)**. „Õigel ajal” tähendab, et saatelehe lähetuskuupäev on sama mis müügirea kinnitatud lähetuskuupäev. Kui kinnitatud lähetuskuupäev pole määratud, kasutage nõutud lähetuskuupäeva. |
| Lähetusjõudlus        | Hilja                                     | CustPackingSlipOnTimeStatus           | Müügiread, mille lähetuskuupäeva olek on **3 (hilja)**. „Hilja” tähendab, et saatelehe lähetuskuupäev on hilisem kui müügirea kinnitatud lähetuskuupäev. Kui kinnitatud lähetuskuupäev pole määratud, kasutage nõutud lähetuskuupäeva. |
| Lähetusjõudlus        | Saadetised teatud aja jooksul                      | SalesLine CustPackingSlipOnTimeStatus | Täielikult lähetatud tellimused, kus müügirea täielik kogus on lähetatud, pluss Vara, Õigel ajal ja Hilja (vt kirjeldusi tabelis eestpoolt). |
| Lähetusjõudlus        | Hilja lähetatud linna järgi                     | CustPackingSlipOnTimeStatus           | Hilja (vt kirjeldusi tabelis eestpoolt). |
| Lähetusjõudlus        | Lähetatud toote järgi                       | CustPackingSlipOnTimeStatus           | Vara, Õigel ajal ja Hilja (vt kirjeldusi tabelis eestpoolt). |
| Lähetusjõudlus        | Lähetatud kliendi järgi                      | CustPackingSlipOnTimeStatus           | Vara, Õigel ajal ja Hilja (vt kirjeldusi tabelis eestpoolt). |
| Lähetusjõudlus        | Lähetatud tegevuskoha/lao järgi              | CustPackingSlipOnTimeStatus           | Vara, Õigel ajal ja Hilja (vt kirjeldusi tabelis eestpoolt). |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]