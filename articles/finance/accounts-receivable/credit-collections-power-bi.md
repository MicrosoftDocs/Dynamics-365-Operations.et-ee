---
title: Krediidi ja võlanõuete halduse Power BI sisu
description: See teema kirjeldab, mida hõlmab krediidi ja võlanõuete halduse Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.
author: ShivamPandey-msft
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 65423f49ba106a152f58c92533c4f1a16d47a318982cfe69bb23f9091fa09846
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763210"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Krediidi ja võlanõuete halduse Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **krediidi ja võlanõuete halduse** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Krediidi ja võlanõuete halduse** Power BI sisu on mõeldud krediidi ja võlanõuete juhtidele ning võlanõuetega tegelevatele ametnikele. Selles antakse peamised krediidi ja võlanõuete mõõdikud, nt laekumata müügi päevad, laekumata saldo, krediidi maht ja kliendid, kes on krediidilimiidi ületanud. See kasutab kandeandmeid ja annab koondvaated krediidist ja võlanõuetest kõigi ettevõtete lõikes. Samuti pakub see andmete jaotust ettevõtete, kliendigruppide ja klientide lõikes.

See Power BI sisu koosneb 10 aruandelehest.

- Kaks ülevaatelehte (üks leht krediidiülevaate ja üks leht sissenõuete ülevaate jaoks).
- Kaheksa andmelehte, millel on üksikasjad krediidi ja võlanõuete mõõdikute kohta, mis on mitmesuguste dimensioonide lõikes osadeks jagatud.

Kõik summad on näidatud süsteemivaluutas. Süsteemi valuuta saab seadistada lehel **Süsteemi parameetrid**.

Vaikimisi kuvatakse praeguse ettevõtte krediidi ja võlanõuete andmed. Andmete vaatamiseks kõigi ettevõtete lõikes määrake rollile kohustus **CustCollectionsBICrossCompany**.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI sisu vaatamiseks on vajalik häälestus

**Klientide krediidihaldus ja võlanõuded** Power BI visuaalide kuvamiseks tuleb teha järgmine seadistus.

1. Avage **Süsteemihaldus > Seadistamine > Süsteemi parameetrid**, et määrata **Süsteemi valuuta** ja **Süsteemi vahetuskurss**.
2. Avage jaotis **Pearaamat > Kalendrid > Rahanduskalendrid**, et kinnitada aktiivsele ajavahemikule määratud rahanduskalendri kuupäevad.
3. Avage **Üldine pearaamat > Seadistus > Pearaamat** ja määrake **Raamatupidamise valuutat** ja **Vahetuskursi tüüpi**.
4. Määratlege vahetuskursid kannete valuutade ja arvestusvaluuta, raamatupidamise valuuta ja süsteemi valuuta vahel. Selleks avage **Pearaamat > Valuutad > Valuutakursid**.
5. Avage **Süsteemihaldus > Seadistamine > Üksuse kauplus**, et värskendada **CustCollectionsBIMeasurementsV2** koondmõõtmist.

>[!NOTE] 
> Ajalise jaotuse perioodi määratlused tuleb seadistada jaotises **Müügireskontro parameetrid > Kogumid > Kogumite vaikeväärtused**, et lubada ajalise jaotuse andmed Power BI sisus.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

**Krediidi ja võlanõuete halduse** Power BI sisu kuvatakse tööruumis **Klientide krediidihaldus ja võlanõuded**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad aruanded

**CustCollectionsBICrossCompany** Power BI sisu sisaldab aruannet, mis koosneb mõõdikute kogumist. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate **CustCollectionsBICrossCompany** Power BI sisu visualiseerimistest.

| Aruandeleht                 | Visualiseering |
|-----------------------------|---------------|
| Võlanõuete ülevaade        | <ul><li>Tähtaja ületanud kliendid</li><li>Krediidilimiiti ületavad kliendid</li><li>DSO 30 päeva</li><li>Avatud juhtumid</li><li>Keskmine päevade arv teenindusjuhtumi sulgemiseni</li><li>Avatud tegevused</li><li>Keskmine päevade arv tegevuste sulgemiseni</li><li>Avatud viivisearved</li><li>Avatud märgukirjad</li><li>Ootel klient</li><li>Ootel müük</li><li>Aegunud saldod</li><li>Võlanõuete oleku summad</li><li>Võlanõuete koodi summad</li><li>Mahakandmine põhjusega</li><li>Tähtajaline saldo regiooniti</li><li>Eeldatavad maksed</li></ul> |
| Krediidi ülevaade             | <ul><li>Tähtaja ületanud kliendid</li><li>Krediidilimiit võrreldes deebetsaldoga</li><li>Krediidilimiiti ületavate klientide tabel</li><li>Krediidilimiiti ületavad kliendid ettevõtte kohta</li><li>Kasutatud krediit võrreldes kogu krediidilimiidiga</li><li>Krediidilimiit võrreldes regiooniti kasutatud krediidiga</li><li>Kliendid krediidireitingu kohta</li></ul> |
| Krediidilimiit                | <ul><li>Krediidilimiit</li><li>Krediidilimiidi üksikasjad</li><li>Krediidilimiit kliendi kohta</li><li>Krediidilimiit kliendigrupi kohta</li><li>Krediidilimiit ettevõtte krediidireitingu kohta</li><li>Krediidilimiit vs. regiooniti kasutatud krediit</li></ul> |
| Krediidilimiiti ületavad kliendid | <ul><li>Krediidilimiiti ületavad kliendid</li><li>Krediidilimiiti ületavate klientide üksikasjad</li><li>Krediidilimiiti ületavad kliendid ettevõtte kohta</li><li>Krediidilimiiti ületavad kliendid kliendigrupi kohta</li><li>Krediidilimiiti ületavad kliendid regiooniti</li></ul> |
| Tähtaja ületanud kliendid          | <ul><li>Tähtaja ületanud kliendid</li><li>Tähtaja ületanud kliendi üksikasjad</li><li>Tähtaja ületanud kliendid ettevõtte kohta</li><li>Tähtaja ületanud kliendid kliendigrupi kohta</li><li>Tähtaja ületanud kliendid regiooniti</li></ul> |
| Aegunud saldod               | <ul><li>Aegunud saldod</li><li>Aegunud saldode üksikasjad</li><li>Aegunud saldod ettevõtte kohta</li><li>Aegunud saldod kliendigrupi kohta</li></ul> |
| Eeldatavad maksed           | <ul><li>Eeldatavad maksed</li><li>Eeldatavate maksete üksikasjad</li><li>Eeldatavad maksed ettevõtte kohta</li><li>Eeldatavad maksed kliendigrupi kohta</li><li>Eeldatavad maksed regiooniti</li></ul> |
| Mahakandmised                  | <ul><li>Mahakandmised regiooniti</li><li>Mahakandmiste üksikasjad</li><li>Mahakandmised põhikonto järgi</li><li>Mahakandmised ettevõtte järgi</li><li>Mahakandmised kliendigrupi kohta</li><li>Mahakandmised regiooniti</li></ul> |
| Sissenõuete olek          | <ul><li>Vaidlustatud</li><li>Makselubadust on murtud</li><li>Makselubadus</li><li>Võlanõuete oleku üksikasjad</li><li>Võlanõuete oleku summad</li><li>Avatud juhtumid</li><li>Avatud tegevused</li></ul> |
| Märgukirjad         | <ul><li>Sissenõude koodi summad</li><li>Võlanõude koodi summa üksikasjad</li><li>Märgukirja summa ettevõtte kohta</li><li>Märgukirja summa kliendigrupi kohta</li><li>Märgukirja summa regiooniti</li></ul> |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Visualisatsioonis summeeritud alusandmete eksportimiseks saab kasutada ka alusandmete eksportimise funktsiooni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]