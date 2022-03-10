---
title: Topeltkasutusega kaubad
description: Selles teemas selgitatakse, kuidas saada ülevaadet topeltkasutusega kaupadest, talletada iga asjakohase toote ja sihtriigi sertifikaadi numbreid ning printida kehtivaid sertifikaadi numbreid vastavatele arvetele, saatelehtedele ja/või müügitellimustele.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 21910c61cc330e0c9292990b7b1914f56bac844c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570749"
---
# <a name="dual-use-goods"></a>Topeltkasutusega kaubad

[!include [banner](../includes/banner.md)]

Topeltkasutusega kaubad on tavaliselt kaubad, mis on nii tsiviil- kui ka militaarkasutusega. Näiteks võib kemikaali kasutada väetise või lõhkeainena. Paljudes riikides on erimäärused, mis kehtivad topeltkasutusega kaupade eksportimisel, importimisel ja transpordil. Seetõttu on oluline, et topeltkasutusega kaupade rahvusvahelise kaubandusega seotud ettevõtted oleksid kursis erinevate poliitikate ja sertifikaatidega.

See topeltkasutuse funktsioon aitab saada ülevaadet topeltkasutusega kaupadest, talletab iga asjakohase toote ja sihtriigi sertifikaadi numbreid ning prindib kehtivaid sertifikaadi numbreid vastavatele arvetele, saatelehtedele ja/või müügitellimustele. See aitab tagada, et teie toodete saatmisel on alati kaasatud ajakohased sertifikaadid.

Kaaluge järgmisi stsenaariume.

1. Teie süsteemi leht **Topeltkasutuse riigi häälestamine** näitab, et Prantsusmaale saatmine nõuab sertifikaati.
2. Toote X-100 leht **Väljastatud toote üksikasjad** näitab, et see on topeltkasutusega toode. Kood, kategooria, grupp ja režiim koos näitavad ekspordi juhtimise klassifikatsiooni, kuhu see toode kuulub.
3. Leht **Topeltkasutuse sertifikaadid** sisaldab toote X-100 sertifikaati, kui see saadetakse Prantsusmaale. See sertifikaat aegub 1. jaanuaril 2020.
4. 17. juunil 2020, loote müügitellimuse Prantsusmaal asuva kliendi ettevõttele ja tellimus sisaldab toodet X-100.
5. Kui salvestate müügitellimuse, määrab süsteem järgmise teabe.

    1. Kas tellimus sisaldab tooteid, mis on topeltkasutusega kaubad?
    2. Kui tellimus sisaldab topeltkasutusega kaupu, kas sihtriik nõuab topeltkasutuse sertifikaate?
    3. Kui riik nõuab topeltkasutuse sertifikaate, kas on olemas kehtiv sertifikaat igale topeltkasutusega kaubale selle sihtriigi jaoks?

6. Tellimus sisaldab toodet X-100, toode saadetakse Prantsusmaale ja toote jaoks on olemas prantsuse sertifikaat. Kuid see sertifikaat on aegunud. Seetõttu kuvatakse teile järgmine hoiatusteade: „Selle müügitellimuse ühe või mitme topeltkasutusega kauba sertifikaat ei kehti. Kas soovite kinnitusega jätkata?”

Selles teemas selgitatakse, kuidas konfigureerida kõiki sätteid, mis on vajalikud topeltkasutusega kaupade seadistamiseks ja selle stsenaariumi toetamiseks.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Kõigi asjakohaste riikide topeltkasutuse nõuete määratlemine

Erinevatel riikidel on topeltkasutusega kaupade puhul erinevad nõuded. Kasutage lehte **Topeltkasutuse riigi häälestamine**, et saada ülevaadet, millised riigid nõuavad sertifikaate ja millised mitte. Siin määratud teavet kontrollitakse müügitellimuste loomisel ja teile tuletatakse meelde nõutavate sertifikaatide lisamist.

Erinevate riikide topeltkasutuse nõuete seadistamiseks toimige järgmiselt.

1. Avage jaotis **Tooteteabe haldus \> Häälestus \> Toote vastavus \> Topeltkasutusega tooted \> Topeltkasutuse riigi häälestamine**.
2. Valige redigeerimiseks olemasolev riigi häälestus või valige toimingupaanilt **Uus** uue riigi häälestuse loomiseks.
3. Määrake valitud või uue riigi häälestuse jaoks järgmised väärtused.

    | Väli | Kirjeldus |
    |---|---|
    | Riik/regioon | Valige riik, mille nõudeid te jälgite. |
    | Sert nõutav | Märkige see ruut riikide puhul, mis nõuavad topeltkasutusega kaupade sertifitseerimist. Tühjendage see riikide puhul, mis seda sertifikaati ei nõua. |

## <a name="create-dual-use-categories"></a>Topeltkasutuse kategooriate loomine

Topeltkasutusega kaubad tuleb sageli liigitada vastavalt nende ekspordikontrolli klassifikatsiooni numbrile (ECCN). ECCN on tähe- ja numbrimärkidest koosnev kood, mis liigitab kaupu selliste tegurite alusel, nagu kaup ja tehnoloogia. Leht **Topeltkasutuse kategooriad** aitab teil koostada aruandluse eesmärgil loendi kasutatavatest kategooriatest.

Topeltkasutuse kategooriate häälestuseks läbige need etapid.

1. Avage jaotis **Tooteteabe haldus \> Häälestus \> Toote vastavus \> Topeltkasutusega tooted \> Topeltkasutuse kategooriad**.
2. Valige redigeerimiseks olemasolev kategooria või valige toimingupaanilt **Uus** uue kategooria loomiseks.
3. Määrake valitud või uue kategooria jaoks järgmised väärtused.

    | Väljad | Kirjeldus |
    |---|---|
    | Topeltkasutusega kood | Sisestage täielik ECCN-kood (nt *3A001*).|
    | Topeltkasutuse kategooria | Sisestage kaubanduse kontroll-loendi (CCL) kategooria osa ECCN-koodist. Näiteks ECCN-koodi *3A001* puhul on see väärtus *3*. |
    | Topeltkasutusega grupp | Sisestage tootegrupi osa ECCN-koodist. Näiteks ECCN-koodi *3A001* puhul on see väärtus *A*. |
    | Topeltkasutuse režiim | Sisestage kauba režiimi kood. See kood määratleb põhjuse, miks kaup on topeltkasutuseks liigitatud. Näiteks ECCN-koodi *3A001* puhul on see väärtus *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Topeltkasutuse kategooriate rakendamine toodetele

Toote tuvastamiseks topeltkasutusega kaubana ja sellele topeltkasutuse kategooria rakendamiseks toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige või looge toode, et avada selle leht **Väljastatud toote üksikasjad**.
1. Määrake kiirkaardi **Väliskaubandus** suvandi **Topeltkasutusega tooted** väärtuseks **Jah**, et tuvastada praegust toodet topeltkasutusega kaubana.
1. Määrake väljale **Topeltkasutuse kood** praegusele tootele kehtiv kood. (Määratlesite selle koodi lehel **Topeltkasutuse kategooriad**.)

Seda seadistust kontrollitakse müügitellimuse loomisel.

## <a name="set-up-dual-use-certificates"></a>Topeltkasutuse sertifikaatide häälestamine

Kasutage lehte **Topeltkasutuse sertifikaadid** iga toote ja riigi jaoks nõutavate topeltkasutuse sertifikaatide häälestamiseks ja haldamiseks. Saate jälgida iga sertifikaadi üksikasju, nt riiki ja kehtivuse kuupäevi. Saate määrata ka suvandeid, mis määratlevad, kuhu see teave tuleks printida. Seda teavet printida näiteks arvele, saatelehele ja/või müügitellimusele. Seda seadistust kontrollitakse müügitellimuse loomisel.

1. Avage jaotis **Tooteteabe haldus \> Häälestus \> Toote vastavus \> Topeltkasutusega tooted \> Topeltkasutuse sertifikaadid**.
2. Valige redigeerimiseks olemasolev sertifikaat või valige toimingupaanilt **Uus** uue sertifikaadi loomiseks.
3. Määrake valitud või uue sertifikaadi jaoks järgmised väärtused.

    | Väli | Kirjeldus |
    |---|---|
    | Kauba number | Valige topeltkasutusega kauba kaubakood, millele see sertifikaat kehtib. |
    | Riik/regioon | Sihtriik või -piirkond, kus peate seda sertifikaati kasutama. |
    | Serdi number | Number, mis kuvatakse hankijale või kliendile väljastatud sertifikaadil. |
    | Jõustunud | Valige praeguse sertifikaadi kehtivuse esimene kuupäev.|
    | Aegumine | Valige praeguse sertifikaadi kehtivuse viimane kuupäev. |
    | Arvele printimine | Märkige see ruut, et printida sertifikaadi number arvetele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul. |
    | Saatelehele printimine | Märkige see ruut, et printida sertifikaadi number saatelehtedele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul. |
    | Müügitellimusele printimine | Märkige see ruut, et printida sertifikaadi number müügitellimustele, mis on adresseeritud määratud riigile kindlal kuupäevavahemikul. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]