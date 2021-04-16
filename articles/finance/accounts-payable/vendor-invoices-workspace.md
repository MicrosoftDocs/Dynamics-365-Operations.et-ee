---
title: Hankija arve sisestamise tööruum
description: Selles teemas selgitatakse, kuidas seadistada hankija arvetega seotud tööruume, mis kuvavad Microsoft Power BI kaudu saadaolevat teavet.
author: abruer
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bac57056af6d85bb30600e13628279801508741d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837248"
---
# <a name="vendor-invoice-entry-workspace"></a>Hankija arve sisestamise tööruum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas seadistada hankija arvetega seotud tööruume, mis kuvavad Microsoft Power BI kaudu saadaolevat teavet. Selle tööruumi hankija arve teave filtreeritakse kindlatele kasutajatele ja kuvatakse graafikuna.

## <a name="overview"></a>Ülevaade

Tööruumis **Hankija arve sisestamine** kuvatakse teave, mis on seotud hankija arvete töötlemisega. See sisaldab vaadet **Minu töö** ja lehte **Analüüs – kõik ettevõtted**. Vaade **Minu töö** kuvab kokkuvõttepaanid, hankija kannete tabelid ja hankija seonduvad andmed. Leht **Analüüs – kõik ettevõtted** kasutab Power BI võimalusi hankija arvetega seotud visualiseeringute kuvamiseks.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Tööruumi seadistamine Power BI sisu kuvamiseks

Peate selle häälestuse lõpule viima enne, kui andmeid saab kuvada Power BI visualiseeringutes tööruumis **Hankija arve sisestamine**.

1. Filtreerige tööruumi **Funktsioonihaldus** loendit funktsiooni **Hankija arve automatiseerimine** leidmiseks.
3. Valige **Luba kohe**.
4. Tagamaks, et arveid saab töödelda algusest lõpuni ilma käsitsi sekkumata, seadistage hankija arve töövoog. Töövoo seadistamiseks avage **Ostureskontro \> Seadistus \> Ostureskontro töövood**.
5. Avage **Ostureskontro \> Seadistamine \> Ostureskontro parameetrid** ja valige vahekaart **Hankija arve automatiseerimine**. Lisateavet leiate jaotisest [Hankija arve automatiseerimise seadistuse suvandid](vnd-invoice-set-up-options.md).
6. Määrake suvandi **Imporditud arvete automaatne edastamine töövoole** väärtuseks **Jah**.
7. Kui toote sissetulekud tuleb automaatselt vastendada, määrake suvandi **Toote sissetulekute automaatne vastendamine arveridadele** väärtuseks **Jah**.
8. Vaadake läbi ülejäänud valikulised sätted ja konfigureerige need vastavalt oma organisatsiooni vajadustele.
9. Avage **Süsteemihaldus \> Seadistamine \> Süsteemi parameetrid**, et määrata väljad **Süsteemi valuuta** ja **Süsteemi vahetuskurss**.
10. Avage **Pearaamat \> Seadistamine \> Pearaamat** ja määrake väljad **Raamatupidamise valuuta** ja **Vahetuskursi tüüp**.
11. Avage **Pearaamat \> Valuutad \> Valuuta vahetuskursid** ja sisestage kandevaluuta ja arvestusvaluuta ning arvestusvaluuta ja süsteemivaluuta vahelised vahetuskursid.
12. Avage **Süsteemihaldus \> Seadistamine \> Üksuse kauplus** ja otsige üles üksus **Hankija arve automatiseerimise mõõdik**. Valige **Värskenda**.

Tööruumis kuvatava teabe vaatamiseks peab teil olema ostureskontro halduri või ostureskontro ametniku turberoll.

## <a name="my-work-view"></a>Minu töö vaade

### <a name="company-selection"></a>Ettevõtte valimine

Kui funktsioon **Hankija arvete automatiseerimine** on sisse lülitatud, kuvatakse tööruumi ülaosas väli **Ettevõte**. Väljal **Ettevõte** valitud suvand mõjutab kogu tööruumis kuvatavat teavet. Vaikimisi kuvatakse selles vaates teave ettevõtte kohta, kuhu olete sisse loginud. Kui valite väljal **Ettevõte** mõne muu ettevõtte, saate kuvada selle ettevõtte teabe tööruumis. Seejärel saate valida tööruumi paani, et minna valitud ettevõtte seotud lehele.

### <a name="summary-tiles"></a>Kokkuvõttepaanid

Vaate **Minu töö** jaotise **Ootel olevate arvete kokkuvõte** paanid annavad ülevaate hankija arvete olekust. Saate kuvada töölehti, mida pole veel sisestatud ja ootel olevaid arveid. Lisaks on neli paani, mis on seotud hankija arve automatiseerimise funktsiooniga.

- Vajalik on sissetuleku käsitsi vastendamine
- Võrdlemise kinnitamine ei õnnestunud
- Arveid pole edastatud töövoogu
- Arveid pole imporditud

(Need neli paani nõuavad, et hankija arve automatiseerimise funktsioon oleks funktsioonihalduses sisse lülitatud.)

Paani **Hankija arvete taastamine** kasutamiseks peab funktsioon olema ostureskontro parameetrites sisse lülitatud. Avage **Ostureskontro \> Ostureskontro parameetrid** ja seejärel määrake vahekaardil **Arve** suvandi **Luba hankija arve taastamine** väärtuseks **Jah**.

Kui funktsioon on sisse lülitatud, kuvatakse töölehe jaotises **Töölehed** kolm kokku grupeeritud paani. Need paanid on **Töölehed**, **Töölehed – mulle määratud** ja **Arvekaust**. 

Jaotises **Ootel olevate arvete kokkuvõte** kuvatav teave käib ettevõtte kohta, mis on määratud teie vaikeettevõtteks sisselogimisel.

### <a name="creating-new-records"></a>Uute kirjete loomine

Uue arve kirje loomiseks valige **Uus** ja seejärel valige loendist üks järgmistest kirje tüüpidest:

- Hankija arve
- Arve tööleht
- Globaalne arve tööleht
- Arveregister
- Arve kinnitamine

Pange tähele, et teie loodud kirje põhineb ettevõtte filtril, mitte ettevõttel, kuhu olete sisse logitud. Näiteks olete sisse logitud ettevõttesse **UMSF**, kuid ettevõtte filtriks on seatud **GBSI**. Sel juhul, kui valite suvandi **Uus** ja valite seejärel loendist kirje tüübi, luuakse kirje ettevõttes GBSI.

### <a name="documents-not-invoiced-grids"></a>Arveldamata dokumentide ruudustikud

Jaotis **Arveldamata dokumendid** sisaldab ruudustikke, mis kuvavad hankija arveid ootavaid dokumente.

Ruudustikus **Avatud ostutellimused** kuvatakse kõiki ostutellimusi, mida pole veel täielikult arveldatud. Ostutellimusele uue hankija arve loomiseks saate kasutada nuppu **Arvelda kohe**. Ostutellimusele uue ettemaksuarve loomiseks saate kasutada nuppu **Ettemaksuarve kohe**.

Ruudustikus **Toote sissetulekud** kuvatakse kõik vastuvõetud kanded, mida pole veel täielikult arveldatud. Ostutellimusele uue hankija arve loomiseks saate kasutada nuppu **Arvelda kohe**.

Ruudustikus **Ootel olevad hankija arved** kuvatakse kõik hankija arved, mida pole töövoo süsteemi sisestatud. Kindla hankija arve otsimiseks saate kasutada välja **Otsing** ja/või ettevõtte filtrit. Ruudustikus kuvatava kande redigeerimiseks saate kasutada nuppu **Redigeeri**.

Ruudustikus **Ostutellimuse otsimine** saate kasutada välja **Otsing** kindla ostutellimuse otsimiseks.

### <a name="related-information"></a>Seostuv teave

Tööruumi paremas servas olevate linkide abil saate kuvada teavet sisestatud arvete kohta. Nende linkide hulka kuuluvad **Avatud hankija arved**, **Arve tööleht** ja **Arve ajalugu ja võrdlemise üksikasjad**. Jaotises **Hankijad** pääsete juurde filtreeritud loendile, kus kuvatakse kõik ootel olevad hankijad, või saate kasutada linki **Kõik hankijad**. Saadaval on ka lingid **Kõik ostutellimused** ja **Avatud ettemaksud**.

### <a name="analytics--all-companies-page"></a>Analüüs – kõikide ettevõtete leht

Saate kuvada automaatse analüüsi, kui lehel **Ostureskontro parameetrid** on suvandi **Imporditud arvete automaatne edastamine töövoole** väärtuseks seatud **Jah**. Leht **Analüüs – kõik ettevõtted** annab olulisi mõõdikuid, nt hankija arveid, mida kinnitavad kinnitaja ja ettevõte. See leht sisaldab viite aruandelehte. Üks leht annab ülevaate ja ülejäänud lehtedel on ostureskontro automatiseerimise mõõdikute üksikasjad.

Järgmine tabel näitab igal aruandelehel olevaid visualiseeringuid.

| Aruandeleht                    | Visualiseeringud |
|--------------------------------|----------------|
| Hankija arve ülevaade        | <ul><li>Ootel olevad hankija arved automatiseerimisel süsteemi valuutas</li><li>Arved, mille importimine nurjus</li><li>Töövoos olevad arved</li><li>Puudutamata arved viimase 30 päeva jooksul</li><li>Automatiseeritud arveid kokku viimase 30 päeva jooksul</li><li>Avatud arvete saldo süsteemi valuutas</li><li>Nurjumiste põhjused viimaste 30 päeva jooksul</li><li>Sisestatud arvete protsent, mida töödeldi automaatselt</li><li>Arve töötlemiseks kuluv päevade arv</ul></li> |
| Automatiseerimise olek              | <ul><li>Puudutamata arved viimase 30 päeva jooksul</li><li>Puudutamata arved viimase 30 päeva jooksul ettevõtte järgi</li><li>Puudutamata arved viimase 30 päeva jooksul hankija grupi järgi</li><li>Sisestatud arvete protsent, mida töödeldi automaatselt</li><li>Arve töötlemiseks kuluv päevade arv</li></ul> |
| Arved, mille importimine nurjus | <ul><li>Arved, mille importimine nurjus</li><li>Arved, mille importimine nurjus, ettevõtte järgi</li></ul> |
| Automatiseerimise nurjumise põhjused | <ul><li>Nurjunud arved</li><li>Nurjunud arved ettevõtte järgi</li><li>Nurjunud arved hankija grupi järgi</li></ul> |
| Töövoo olek                | <ul><li>Töövoos olevad arved</li><li>Hankija arve töövooeksemplarid</li><li>Määramine kinnitaja kohta</li><li>Hankija arve töövoog ettevõtte kohta</li><li>Keskmine töövoo päevade arv kinnitaja kohta</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]