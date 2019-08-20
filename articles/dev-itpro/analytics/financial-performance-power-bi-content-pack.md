---
title: Finantstulemuste PowerBI.com’i lahendus
description: Selles teemas kirjeldatakse finantstulemuste PowerBI.com’i lahendust.
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35db2b51274afa6dae4cb5f75b4ba5390b167a49
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849577"
---
# <a name="financial-performance-powerbicom-solution"></a>Finantstulemuste PowerBI.com’i lahendus

[!include [banner](../includes/banner.md)]

> [!NOTE]
> See PowerBI.com’i lahendus on aegunud, nagu on kirjas dokumendis [AppSource’is saadaolevad Power BI sisupaketid](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource)’i

Selles teemas kirjeldatakse **finantstulemuste** PowerBI.com’i lahendust. See kirjeldab armatuurlauda ja selles sisalduvaid aruandeid ning annab teavet lahenduse loomiseks kasutatud andmemudeli ja üksuste kohta.

## <a name="main-account-setup"></a>Põhikonto seadistus
Kuna organisatsioonid soovivad kuvada kohustused ja tulusummad aruannetel positiivsete summadena, on põhikontode seadistus oluline. Selleks, et need põhikontod kuvataks positiivsete summadena, peab põhikonto tüübiks olema määratud **Kohustus** või **Tulu**. Kui kasutatakse neid kontotüüpe, pööratakse aruande koostamisel Power BI kaudu märgid ümber ja näidatakse summasid positiivsena.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>PowerBI.com’i lahendusse kuuluvad armatuurlaud ja aruanded
Armatuurlaud sisaldab aluseks olevatel aruannetel põhinevate andmete kokkuvõtlikke paane. Iga paan sisaldab kõigi organisatsiooni ettevõtete jooksva aasta kohta kokkuvõtlikku teavet. Siin on mõned neist paanidest.

- Sularaha
- Kogu tulu sellel aastal
- Kogu kulud sellel aastal
- Netotulu sel aastal
- Likviidsuskordaja
- Kogukulud sellel aastal konto kategooria järgi
- Lühiajalise kohustuse kattekordaja
- Võlgnevus varadele kokku
- Tegelik vs eelarvestatud tulu
- Arveldatud tulu sellel aastal
- Tegevuskulude suhe sellel aastal
- Kasumi määr sellel aastal
- Tegelikud vs eelarvelised kulud – kõik ettevõtted

Iga paan on varustatud toetava aruandega. Need aruanded sisaldavad nii teavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                      | Teave, mida aruanne sisaldab |
|-----------------------------|--------------------------------------|
| Sularaha analüüs               | Sularaha juriidilise üksuse järgi, sularaha kvartali järgi, kogu sularaha ja sularaha konto järgi<blockquote>[!NOTE] Kvartalipõhise sularaha andmed ei sisalda esimese kvartali algsaldode kogusummat. Sellel on näha igas kvartalis sisestatud uute kannete koondsumma.</blockquote> |
| Lühiajalise kohustuse kattekordaja analüüs      | Lühiajalise kohustuse kattekordaja juriidilise isiku järgi, lühiajalise kohustuse kattekordaja kvartali järgi ning käibevara ja lühiajaliste kohustuste saldod. |
| Likviidsuskordaja analüüs        | Likviidsuskordaja juriidilise isiku järgi, likviidsuskordaja kvartali järgi ja sularaha, müügireskontro ja lühiajaliste kohustuste saldod |
| Tuletusreegli analüüs | Tuletusreegel (COGS) juriidilise isiku järgi, COGS sellel aastal ja eelmisel aastal kvartali järgi, COGS müügile juriidilise isiku järgi, kogu COGS ja COGS müügiprotsendile |
| Käibekapitali analüüs    | Käibekapital juriidilise isiku järgi, käibekapital kvartali järgi, käibevara, lühiajalised kohustused ja kogu käibekapital |
| Vara ja võla analüüs     | Tagastus kogumaksumuselt ja võlgnevus varadele kokku juriidilise isiku järgi, võlgnevus varadele kokku ja tagastus kogumaksumuselt kvartalis praeguse kuupäevani, varad ja kohustused. |
| Kasumimarginaali analüüs      | Tegelik ja eelarve kasumimarginaal juriidilise isiku järgi, kasumimarginaal kvartali järgi, kasumimarginaali protsent ja kasumimarginaal |
| Netotulu analüüs         | Tegelik ja eelarveline netotulu juriidilise isiku järgi, netotulu sellel aastal ja eelmisel aastal ning kulud netotulu protsendile |
| Tulude analüüs           | Tegelikud ja eelarvelised tulud enne intressi ja makse (EBIT) juriidilise isiku järgi, EBIT sellel aastal ja eelmise aastal, kulud tulu suhtes protsent ning tegelikud ja eelarvelised kulud tulu suhtes |
| Tulu analüüs            | Kogutulu, tegelik ja eelarveline kogutulu juriidilise isiku järgi, kogutulu sellel ja eelmisel aastal, tulueelarve hälve juriidilise isiku järgi ning kogutulu sellel ja eelmisel perioodil |
| Kuluanalüüs            | Kogukulud, tegelikud eelarveliste kogukulude suhtes juriidilise isiku järgi, tegelik ja eelarveline kogukulu kvartali järgi, kogukulud konto kategooria järgi ning tegevuskulude suhe |
| Arveldatud tulu analüüs     | Kogu müügireskontro, kogu müügireskontro juriidilise isiku järgi, kogu müügireskontro kvartali järgi ja müügireskontro kontode saldod<blockquote>[!NOTE] Teave ei sisalda müügireskontro pearaamatukontode algsaldosid. See näitab müügireskontrosse sisestatud uute kannete koondsummat.</blockquote> |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
**Finantstulemuste** PowerBI.com’i lahenduse alusena kasutati järgmisi üksusi.

**Koondandmete üksused**

- **GeneralLedgerActivities** – see üksus koondab pearaamatu saldod konto kategooria järgi.
- **BudgetActivities** – see üksus koondab eelarvesaldod konto kategooria järgi.

**Andmeüksused**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Pearaamatud
- ChartofAccounts

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Arvutatud mõõtusid kasutatakse sisus kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Vaikimisi toob sisu sisse viimase kolme aasta ja ühe tulevase aasta andmed. Aruannetesse ja armatuurlauale lisaarvutuste kaasamiseks saate muuta [Microsoft Exceli töövihikut](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). See töövihik on vaikimisi andmemudel, mida kasutati sisu loomiseks.
