---
title: "Finantsjõudluse Power BI sisu"
description: Selles teemas kirjeldatakse finantstulemuste Power BI sisu.
author: kweekley
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 83ea868e7612f30afa1b99f374878f4ba415113f
ms.contentlocale: et-ee
ms.lasthandoff: 12/19/2017

---

# <a name="financial-performance-power-bi-content"></a>Finantsjõudluse Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **finantstulemuste** Microsoft Power BI sisu. See kirjeldab armatuurlauda ja selles sisalduvaid aruandeid ning annab teavet sisu loomiseks kasutatud andmemudeli ja üksuste kohta.

## <a name="main-account-setup"></a>Põhikonto seadistus
Kuna organisatsioonid soovivad kuvada kohustused ja tulusummad aruannetel positiivsete summadena, on põhikontode seadistus oluline. Selleks, et need põhikontod kuvataks positiivsete summadena, peab põhikonto tüübiks olema määratud **Kohustus** või **Tulu**. Kui kasutatakse neid kontotüüpe, pööratakse aruande koostamisel Power BI kaudu märgid ümber ja näidatakse summasid positiivsena.

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad armatuurlaud ja aruanded
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
| Sularaha analüüs               | Sularaha juriidilise üksuse järgi, sularaha kvartali järgi, kogu sularaha ja sularaha konto järgi<blockquote>[!NOTE]<br>Kvartalipõhise sularaha andmed ei sisalda esimese kvartali algsaldode kogusummat. Sellel on näha igas kvartalis sisestatud uute kannete koondsumma.</blockquote> |
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
| Arveldatud tulu analüüs     | Kogu müügireskontro, kogu müügireskontro juriidilise isiku järgi, kogu müügireskontro kvartali järgi ja müügireskontro kontode saldod<blockquote>[!NOTE]<br>Teave ei sisalda müügireskontro pearaamatukontode algsaldosid. See näitab müügireskontrosse sisestatud uute kannete koondsummat.</blockquote> |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Power BI-s filtreerimise ja kinnitamise kohta lisateabe saamiseks vaadake teemat [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
**Finantstulemuste** Power BI sisu alusena kasutati järgmisi üksuseid:

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

