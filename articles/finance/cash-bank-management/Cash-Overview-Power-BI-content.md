---
title: Kassa ülevaate Power BI sisu
description: Selles teemas kirjeldatakse kassa ülevaate Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.
author: saraschi2
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 553a4a5d25e126923576569b48414c46aab991ec
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177380"
---
# <a name="cash-overview-power-bi-content"></a>Kassa ülevaate Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse **kassa ülevaate** Microsoft Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.

## <a name="overview"></a>Ülevaade

**Kassa ülevaate** Power BI sisu loodi inimeste jaoks, kes vastutavad oma organisatsioonis sularaha eest. **Kassa ülevaate** Power BI sisu annab ülevaate rahavoogudest. Samuti pakub see prognoose, mis aitavad teil teha paremaid otsuseid ja parandavad seeläbi teie rahavoogude seisundit. Saate analüüsida sularaha juriidilise isiku, valuuta ja pangakonto järgi, et ülejääke ja puudujääke paremini mõista.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI sisu vaatamiseks on vajalik häälestus

Järgmine seadistus tuleb lõpule viia, et kuvada andmeid **Sularaha ülevaade** ja **Panga juhtkond** Power BI visuaalides.

1. Avage **Süsteemihaldus > Seadistamine > Süsteemi parameetrid**, et määrata **Süsteemi valuuta** ja **Süsteemi vahetuskurss**.
2. Avage **Üldine pearaamat > Seadistus > Pearaamat**, et seadistada **Raamatupidamise valuutat** ja **Vahetuskursi tüüpi**.
2. Määratlege vahetuskursid kannete valuutade ja arvestusvaluuta, raamatupidamise valuuta ja süsteemi valuuta ning raamatupidamise valuuta ja panga valuutade vahel. Selleks avage **Pearaamat > Valuutad > Valuutakursid**.
3. Konfigureerige ja käivitage likviidsuse planeerimine. Lisainfo saamiseks likviidsuse planeerimise kohta vt <a href="https://docs.microsoft.com/dynamics365/unified-operations/financials/cash-bank-management/cash-flow-forecasting
">Likviidsuse planeerimine</a>. 
4. Avage **Süsteemihaldus > Seadistamine > Üksuse kauplus**, et värskendada **LedgerCovLiquidityMeasurement** koondmõõtmist.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

Aruanded **kassa ülevaate** Power BI sisust kuvatakse tööruumides **Kassa ülevaade** ja **Pangahaldus**.

Likviidsuse plaanimise aruannete kuvamiseks koos andmetega peate esmalt käivitama prognoosiarvutusprotsessi, kasutades funktsiooni **Likviidsuse plaanimiste arvutamine** alal Sularaha- ja pangahaldus.  Seda tuleb teha iga prognoosi kaasatava ettevõtte puhul.  Seejärel peate värskendama atribuudi LedgerCovLiquidityMeasurement koondmõõtmist lehel **Üksuse kauplus**.  

Demoeesmärgil saate lisada likviidsuse plaanimise demoandmed, kasutades mooduli Demoandmed lehte **Andmete loomine**.  See skript sisestab andmed likviidsuse plaanimise tabelitesse, et aruannete jaoks vajalikku teavet kiiresti sisestada.  See moodul on saadaval ainult siis, kui teie keskkonnas on juurutatud demoandmete komplekti moodul. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad aruanded

Järgmises tabelis on üksikasjad **kassa ülevaate** Power BI sisu igal aruandelehel leiduvate mõõdikute kohta.

| Aruanne                                | Sisu |
|---------------------------------------|----------|
| Kassa ülevaade – kõik ettevõtted         | <ul><li>Sissetulekud ja väljaminekud süsteemi valuutas</li><li>Prognoositud valuutasaldod</li><li>Kogu pangasaldo süsteemi valuutas</li><li>Saldo juriidilise isiku järgi</li><li>Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</li></ul> |
| Kassa ülevaade – praegune ettevõte       | <ul><li>Sissetulekud ja väljaminekud arvestusvaluutas</li><li>Prognoositud valuutasaldod</li><li>Kogu pangasaldo arvestusvaluutas</li><li>Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</li></ul> |
| Likviidsuse plaanimine – kõik ettevõtted    | <ul><li>Sissetulekud ja väljaminekud süsteemi valuutas</li><li>Päevaprognoosi kokkuvõte</li><li>Prognoosi andmed</li></ul> |
| Likviidsuse plaanimine – ettevõtte valuuta | <ul><li>Sissetulekud ja väljaminekud arvestusvaluutas</li><li>Päevaprognoosi kokkuvõte</li><li>Prognoosi andmed</li></ul> |
| Valuutaprognoos                     | <ul><li>Prognoositud valuutasaldod</li><li>Igapäevane valuuta kokkuvõte</li><li>Prognoosi andmed</li></ul> |
| Pangasaldod                         | <ul><li>Kogu pangasaldo süsteemi valuutas</li><li>Saldo juriidilise isiku järgi</li><li>Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</li><li>Saldo pangakonto järgi</li><li>Saldo valuuta järgi</li></ul> |


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
