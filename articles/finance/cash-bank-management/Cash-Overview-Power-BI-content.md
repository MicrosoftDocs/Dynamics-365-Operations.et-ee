---
title: Sularaha ülevaate Power BI sisu
description: See artikkel kirjeldab kassa ülevaate Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.
author: angelad116
ms.date: 07/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a255afac3aa68f3a48b21e4d2fbfb046a9de603c
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151995"
---
# <a name="cash-overview-power-bi-content"></a>Sularaha ülevaate Power BI sisu

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab kassa **ülevaate** Microsoft Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.

## <a name="overview"></a>Ülevaade

**Kassa ülevaate** Power BI sisu loodi inimeste jaoks, kes vastutavad oma organisatsioonis sularaha eest. **Kassa ülevaate** Power BI sisu annab ülevaate rahavoogudest. Samuti pakub see prognoose, mis aitavad teil teha paremaid otsuseid ja parandavad seeläbi teie rahavoogude seisundit. Saate analüüsida sularaha juriidilise isiku, valuuta ja pangakonto järgi, et ülejääke ja puudujääke paremini mõista.

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI sisu vaatamiseks on vajalik häälestus

Järgmine seadistus tuleb lõpule viia, et kuvada andmeid **Sularaha ülevaade** ja **Panga juhtkond** Power BI visuaalides.

1. Avage **Süsteemihaldus > Seadistamine > Süsteemi parameetrid**, et määrata **Süsteemi valuuta** ja **Süsteemi vahetuskurss**.
2. Avage jaotis **Pearaamat > Kalendrid > Rahanduskalendrid**, et kinnitada aktiivsele ajavahemikule määratud rahanduskalendri kuupäevad.
3. Avage **Üldine pearaamat > Seadistus > Pearaamat**, et seadistada **Raamatupidamise valuutat** ja **Vahetuskursi tüüpi**.
4. Määratlege vahetuskursid kannete valuutade ja arvestusvaluuta, raamatupidamise valuuta ja süsteemi valuuta ning raamatupidamise valuuta ja panga valuutade vahel. Selleks avage **Pearaamat > Valuutad > Valuutakursid**.
5. Konfigureerige ja käivitage likviidsuse planeerimine. Lisainfo saamiseks likviidsuse planeerimise kohta vt [Likviidsuse planeerimine](./cash-flow-forecasting.md). 
6. Avage **Süsteemihaldus > Seadistamine > Üksuse kauplus**, et värskendada **LedgerCovLiquidityMeasurement** koondmõõtmist.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

Aruanded **kassa ülevaate** Power BI sisust kuvatakse tööruumides **Kassa ülevaade** ja **Pangahaldus**.

Likviidsuse plaanimise aruannete kuvamiseks koos andmetega peate esmalt käivitama prognoosiarvutusprotsessi, kasutades funktsiooni **Likviidsuse plaanimiste arvutamine** alal Sularaha- ja pangahaldus. Seda tuleb teha iga prognoosi kaasatava ettevõtte puhul.  Seejärel peate värskendama atribuudi LedgerCovLiquidityMeasurement koondmõõtmist lehel **Üksuse kauplus**.  

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
