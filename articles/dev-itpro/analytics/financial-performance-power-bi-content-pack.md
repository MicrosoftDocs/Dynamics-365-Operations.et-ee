---
title: "Finantsjõudluse Power BI sisu"
description: "Selles teemas kirjeldatakse finantstulemuste Power BI sisu. See kirjeldab armatuurlauda ja selles sisalduvaid aruandeid ning annab teavet sisu loomiseks kasutatud andmemudeli ja üksuste kohta."
author: kweekley
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a501fcb851f1c201e03b59bb3ea951684c6e552
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="financial-performance-power-bi-content"></a>Finantsjõudluse Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **finantstulemuste** Microsoft Power BI sisu. See kirjeldab armatuurlauda ja selles sisalduvaid aruandeid ning annab teavet sisu loomiseks kasutatud andmemudeli ja üksuste kohta.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

**Finantstulemuste** Power BI-le pääsete juurde teenusest Microsoft Dynamics Lifecycle Services (LCS) ja lehelt PowerBI.com.

### <a name="available-from-lcs"></a>Kättesaadav LCS-ist
**Finantstulemuste** Power BI sisu, mis on LCS-ist saadaval, toetab järgmisi versioone.

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017)
- Microsoft Dynamics 365 for Operationsi versioon 1611 

Power BI sisu leiate LCS-i ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

### <a name="available-from-powerbicom"></a>Kättesaadav lehelt PowerBI.com
Power.BI.com-ist kättesaadav **finantstulemuste** Power BI sisu toetab rakenduse Microsoft Dynamics AX versioone 7.0 ja 7.0.1. Lisateavet Dynamics AX-i andmete ühendamise ja laadimise kohta vt jaotisest [Juurdepääs Power BI sisule saidilt PowerBI.com](power-bi-home-page.md).

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

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Arvutatud mõõtusid kasutatakse sisus kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Vaikimisi toob sisu sisse viimase kolme aasta ja ühe tulevase aasta andmed. Aruannetesse ja armatuurlauale lisaarvutuste kaasamiseks saate muuta [Microsoft Exceli töövihikut](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). See töövihik on vaikimisi andmemudel, mida kasutati sisu loomiseks. Kui olete lõpetanud muudatuste tegemise, saate luua organisatsioonilise sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

