---
title: Kulude halduse Power BI sisu
description: Selles teemas kirjeldatakse, mida hõlmab kulude halduse Power BI sisupakett.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 178a65c44abd0c9c068d4da1f2684a60062da595247560de4cb81d97ab7b6521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769894"
---
# <a name="expense-management-power-bi-content"></a>Kulude halduse Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, mida hõlmab kulude halduse Power BI sisu. 

## <a name="overview"></a>Ülevaade
Versioonis 8.1 ja uuemates versioonides on koos kulude haldusega kasutamiseks saadaval kaks Power BI sisupaketti. 
- Kuluaruandeid esitavate töötajate jaoks on loodud isiklik armatuurlaud. 

  Armatuurlaud on loodud nii, et see annab inimestele põhiteavet esitamata ja esitatud summade kohta ning näitab kulukannete ajalugu ja ülevaateid. Isiklik armatuurlaud on üks lehekülg, mis sisaldab kasutaja jaoks kõige olulisemat teavet.

- Ostureskontro ametnike ja juhtide jaoks on loodud administraatori armatuurlaud. Armatuurlaud on loodud töövõtja kulude jälgimiseks ja aruandluseks. See sisaldab peamisi kulude mõõdikuid, näiteks esitamata kulud, läbisõit ja keskmised kuluaruande summad. See kasutab kandeandmeid ja annab koondvaated kulude haldusest kõigi ettevõtete lõikes. Peale selle esitab see jaotuse töövõtja kohta võimalusega lisada finantsdimensioonide andmeid. Halduskulu analüüsi sisu sisaldab järgmist. 
  - Ülevaate leht põhimõõdikutega kulusummade kohta ja ülevaadetega kuluaruannete mustanditest ning pooleliolevatest ja lõpetatud kuluaruannetest. 
  - Töövõtja statistikaleht töövõtja individuaalsete üksikasjade ülevaatamiseks aja, kulutüübi ja statistikagrupi järgi. 
  - Töövõtja võrdlusleht mitme töövõtja võrdlemiseks aja jooksul. 

Kõik summad on näidatud ettevõtte valuutas. Näidatakse kõikide ettevõtete andmeid, aga vajaduse korral saab lisada ettevõtte filtri. 

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Kulude administraatori Dashboard.pbix-i ja kulude isikliku Dashboard.pbix-i Power BI sisu leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).
Sisu on saadaval kulude halduse tööruumis Power Bi manussisuna. Kulu omanik pääseb ligi enda isiklikele kuludele, kuid ainult ostureskontro ametnikel ja juhtidel on ligipääs administraatori sisule, et näha kõiki kasutaja kuluandmeid.

## <a name="refreshing-the-power-bi-content"></a>Power BI sisu värskendamine
Kulude halduse Power BI sisu jaoks on vaja üksuse kauplusest värskendada mõõdikuid TrvBiExpenseMeasurement ja BudgetActivityMeasure. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud
Sisu hõlmab aruandelehtede komplekti. Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate Power BI sisu visualiseerimistest.

**Isiklike kulude analüüs**

| Aruandeleht | Visualiseering                             |
|-------------|-------------------------------------------|
| Minu kulud | Läbisõidu summa                         |
|             | Pooleliolevad kuluaruanded                |
|             | Nr Esitamata kulude arv               |
|             | Makstavad isiklikud kulud              |
|             | Esitamata summa                        |
|             | Esitatud summa                          |
|             | Korvamist ootav summa             |
|             | Kuluaruanded summade ja olekuga   |
|             | Esitatud, aga kinnitamata kuluaruanded  |
|             | Kulud kulutüübi järgi                     |
|             | Kulud kaupmehe järgi                      |
|             | Kulud töödeldud kulude järgi            |
|             | Kulud projekti järgi                       |
|             | Kande kogusumma aja jooksul        |

**Halduskulude analüüs**

| Aruandeleht         | Visualiseering                           |           
|---------------------|-----------------------------------------|
| Kulude ülevaade    | Kulude mustandi summa                   |
|                     | Kulude mustandi ridade arv           |
|                     | Kulude mustandi read                     |
|                     | Kuluaruande poliitika rikkumised        |
|                     | Laekumata summa                      |
|                     | Esitatud, aga kinnitamata kulud       |
|                     | Kinnitatud kulud                       |
|                     | Kulusumma kokku                    |
|                     | Kuluaruande kokkuvõtted                |
|                     | Kulud kulutüübi järgi                   |
|                     | Kulud kaupmehe järgi                    |
|                     | Kulud töövõtjate järgi                   |
|                     | Kulud vs projekt                     |
| Töövõtja võrdlus | Kulusummad                         |
|                     | Kulusummad aja jooksul töövõtja järgi   |
| Töövõtja statistika | Kuluaruanded kulutüübi järgi            |
|                     | Isiklikud kulud                       |
|                     | Kuluaruanded statistikagrupi järgi     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]