---
title: "Kassa ülevaate Power BI sisu"
description: "Selles teemas kirjeldatakse kassa ülevaate Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati."
author: saraschi2
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e969c2033463d565ce782c7dc8cfc4b458349289
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017

---

# <a name="cash-overview-power-bi-content"></a>Kassa ülevaate Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **kassa ülevaate** Microsoft Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.

## <a name="overview"></a>Ülevaade

**Kassa ülevaate** Power BI sisu loodi inimeste jaoks, kes vastutavad oma organisatsioonis sularaha eest. **Kassa ülevaate** Power BI sisu annab ülevaate rahavoogudest. Samuti pakub see prognoose, mis aitavad teil teha paremaid otsuseid ja parandavad seeläbi teie rahavoogude seisundit. Saate analüüsida sularaha juriidilise isiku, valuuta ja pangakonto järgi, et ülejääke ja puudujääke paremini mõista.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

Kui kasutate rakenduse Dynamics 365 for Finance and Operations, Enterprise edition, 2017. aasta juuli värskendust, kuvatakse **kassa ülevaate** Power BI sisu aruanded tööruumides **Kassa ülevaade** ja **Pangahaldus**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded
Järgmises tabelis on üksikasjad **kassa ülevaate** Power BI sisu igal aruandelehel leiduvate mõõdikute kohta.

| Aruanne                                | Sisu |
|---------------------------------------|----------|
| Kassa ülevaade – kõik ettevõtted         | <ul><li>Sissetulekud ja väljaminekud süsteemi valuutas</li><li>Prognoositud valuutasaldod</li><li>Kogu pangasaldo süsteemi valuutas</li><li>Saldo juriidilise isiku järgi</li><li>Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</li></ul> |
| Kassa ülevaade – praegune ettevõte       | <ul><li>Sissetulekud ja väljaminekud arvestusvaluutas</li><li>Prognoositud valuutasaldod</li><li>Kogu pangasaldo arvestusvaluutas</li><li>Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</li></ul> |
| Likviidsuse plaanimine – kõik ettevõtted    | <ul><li>Sissetulekud ja väljaminekud süsteemi valuutas</li><li>Päevaprognoosi kokkuvõte</li><li>Prognoosi andmed</li></ul> |
| Likviidsuse plaanimine – ettevõtte valuuta | <ul><li>Sissetulekud ja väljaminekud arvestusvaluutas</li><li>Päevaprognoosi kokkuvõte</li><li>Prognoosi andmed</li></ul> |
| Valuutaprognoos                     | <ul><li>Prognoositud valuutasaldod</li><li>Igapäevane valuuta kokkuvõte</li><li>Prognoosi andmed</li></ul> |
| Pangasaldod                         | <ul><li>Kogu pangasaldo süsteemi valuutas</li><li>Saldo juriidilise isiku järgi</li><li>Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</li><li>Saldo pangakonto järgi</li><li>Saldo valuuta järgi</li></ul> |

## <a name="extending-the-power-bi-content"></a>Power BI sisu laiendamine
Saate pakkuda suurepärast analüüsi inimestele, kes ei logi Dynamics 365, kasutades teenuses Lifecycle Services (LCS) olevaid sisupakette. Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada siis analüüsimiseks Power BI.com-i rentnikus. 

**Kassa ülevaate** Power BI sisu leiate LCS-i ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

Järgmises tabelis on näidatud üksused, millel **kassa ülevaate** Power BI sisu põhineb.

| Üksus                                                                          | Sisu |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_ettevõte                                          | Ettevõtted, mille alusel aruandeid filtreerida |
| LedgerCovLiquidityMeasurement\_Kuupäev                                             | Kuupäevad, mille alusel aruandeid filtreerida |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Tegelikud pangasaldod vs viimati prognoositud pangasaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Prognoositud kande üksikasjad |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Summeeritud sularaha sissetulekud ja väljaminekud, kasutades iga ettevõtte arvestusvaluutat |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Summeeritud sularaha sissetulekud ja väljaminekud, kasutades kõigi ettevõtete puhul süsteemivaluutat |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Summeeritud kande netosumma ja valuutade saldo, kasutades kandevaluutat |

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Seejärel kasutatakse neid arvutatud mõõte **kassa ülevaate** Power BI sisus kasutatavate diagrammide ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida Power BI faili LCS-ist alla ja seda muuta. See fail on vaikeandmemudel, mida kasutati sisu loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisu ja armatuurlauad, mis sisaldavad teie lisatud teavet.


