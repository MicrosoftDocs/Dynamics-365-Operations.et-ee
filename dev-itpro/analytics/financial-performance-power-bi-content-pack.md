---
title: Majandusliku tulemuslikkuse Power BI sisu
description: "Selles teemas kirjeldatakse Microsoft Dynamics 365 tegevuse tulemuslikkuse sisu pakendi Microsoft Power BI. See kirjeldab armatuurlaua ja aruanded, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Majandusliku tulemuslikkuse Power BI sisu

Selles teemas kirjeldatakse Microsoft Dynamics 365 tegevuse tulemuslikkuse sisu pakendi Microsoft Power BI. See kirjeldab armatuurlaua ja aruanded, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet.

<a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
--------------------------

Kaks versiooni tulemuslikkuse sisu pack on saadaval. Üks versioon on saadaval alates Microsoft Dynamics elutsükli teenused (LCS) ja teine on saadaval PowerBI.com.

-   **Versioon on saadaval LCS:** The tulemuslikkuse sisu pack, mis on saadud LCS toetab Microsoft Dynamics 365 toiminguid versiooni 1611. Sisu pack leiad jagatud varade kogu lcs. Lae sisu pakendi ja ühendada oma Microsoft Dynamics 365 toimingute andmete kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).
-   **Versioon on saadaval: PowerBI.com:** The tulemuslikkuse sisu pack, mis on saadud PowerBI.com toetab Microsoft Dynamics AX-i versiooni 7.0 kui 7.0.1. Kuidas ühendada ja laadida oma Dynamics 365 toimingute andmete kohta lisateabe saamiseks vaadake [juurdepääsu Power BI sisu: PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Peamine konto seadistamine
Sest organisatsioonide kohustuste ja tulude summad kuvada aruannetes positiivsete summadena, tema asjaomase Dynamics 365 operatsioonide seadistamine on oluline. Nende peamine kontode esitatud positiivsete summadena, peamine konto tüüp peab olema seatud **kohustuste** või **tulu**. Kontotüübi kasutamisel tagasikäigu märgid ja positiivseks summade kaudu Microsoft Power BI.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Armatuurlaua ja aruanded, mis on kaasatud sisu pack
Pärast sisupaketi ühendamist Dynamics 365 for Operationsi andmetega näitavad armatuurlaud ja aruanded teie finantsandmeid. Kui te pole varem Power BI enne, saab õppida rohkem sellest on [juhindub õppe lehekülg Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Armatuurlaud sisaldab aluseks olevatel aruannetel põhinevate andmete kokkuvõtlikke paane. Iga paan sisaldab kõigi organisatsiooni ettevõtete jooksva aasta kohta kokkuvõtlikku teavet. Siin on mõned kaardid:

-   Sularaha
-   Kogu tulu sellel aastal
-   Kogu kulud sellel aastal
-   Netotulu sel aastal
-   Likviidsuskordaja
-   Kogukulud sellel aastal konto kategooria järgi
-   Lühiajalise kohustuse kattekordaja
-   Võlgnevus varadele kokku
-   Tegelik vs eelarvestatud tulu
-   Arveldatud tulu sellel aastal
-   Tegevuskulude suhe sellel aastal
-   Kasumi määr sellel aastal
-   Tegelikud vs eelarvelised kulud – kõik ettevõtted

Iga plaat on tagatud täiendava lühiaruande. Need aruanded sisaldavad nii teavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                      | Teave, mida aruanne sisaldab                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sularaha analüüs               | Juriidilise isiku, kvartali sularaha, kokku raha ja raha kontolt raha **Märkus:** selle **raha kvartali alusel** aruanne ei sisalda algusest kaalud kogumahus korda. See kuvatakse uusi kandeid, mis sisestatakse iga kvartali kogusumma.                                                                                |
| Lühiajalise kohustuse kattekordaja analüüs      | Lühiajalise kohustuse kattekordaja juriidilise isiku järgi, lühiajalise kohustuse kattekordaja kvartali järgi ning käibevara ja lühiajaliste kohustuste saldod.                                                                                                                                                                                                                              |
| Likviidsuskordaja analüüs        | Maksevõime kordaja juriidilise isiku poolt, likviidsuskordaja kvartali ja raha, saldosid moodustab müügi- ja praegused kohustused                                                                                                                                                                                                                      |
| Tuletusreegli analüüs | Tuletusreegel (COGS) juriidilise isiku järgi, COGS sellel aastal ja eelmisel aastal kvartali järgi, COGS müügile juriidilise isiku järgi, kogu COGS ja COGS müügiprotsendile                                                                                                                                                                                   |
| Käibekapitali analüüs    | Käibekapital juriidilise isiku järgi, käibekapital kvartali järgi, käibevara, lühiajalised kohustused ja kogu käibekapital                                                                                                                                                                                                                   |
| Vara ja võla analüüs     | Tagastus kogumaksumuselt ja võlgnevus varadele kokku juriidilise isiku järgi, võlgnevus varadele kokku ja tagastus kogumaksumuselt kvartalis praeguse kuupäevani, varad ja kohustused.                                                                                                                                                                                     |
| Kasumimarginaali analüüs      | Tegelik ja eelarve kasumimarginaal juriidilise isiku järgi, kasumimarginaal kvartali järgi, kasumimarginaali protsent ja kasumimarginaal                                                                                                                                                                                                                       |
| Netotulu analüüs         | Tegelik ja eelarveline netotulu juriidilise isiku järgi, netotulu sellel aastal ja eelmisel aastal ning kulud netotulu protsendile                                                                                                                                                                                                                       |
| Tulude analüüs           | Tegelikud ja eelarvelised tulud enne intressi ja makse (EBIT) juriidilise isiku järgi, EBIT sellel aastal ja eelmise aastal, kulud tulu suhtes protsent ning tegelikud ja eelarvelised kulud tulu suhtes                                                                                                                                                          |
| Tulu analüüs            | Kogutulu, tegelik ja eelarveline kogutulu juriidilise isiku järgi, kogutulu sellel ja eelmisel aastal, tulueelarve hälve juriidilise isiku järgi ning kogutulu sellel ja eelmisel perioodil                                                                                                                                                 |
| Kuluanalüüs            | Kogukulud, tegelikud eelarveliste kogukulude suhtes juriidilise isiku järgi, tegelik ja eelarveline kogukulu kvartali järgi, kogukulud konto kategooria järgi ning tegevuskulude suhe                                                                                                                                                                 |
| Arveldatud tulu analüüs     | Kokku, kokku laekumata arved juriidilise isiku poolt, debitoorne võlgnevus kvartali alusel ja saldod kontode debitoorse **Märkus:** aruanded ei sisalda, algab saadaolevad pearaamatu kontode algsaldod. Nad näitavad uusi kandeid, mis on sisestatud kontodele saadaolevad kokku. |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Power BI-s filtreerimise ja kinnitamise kohta lisateabe saamiseks vaadake teemat [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Andmed, mida asustab armatuurlaua ja aruanded tulemuslikkuse sisu Pack on Dynamics 365 toimingute andmed. Sisu pack aluseks olid järgmised üksused: **koondab andmed üksused**

-   **GeneralLedgerActivities** – selle olemi koondab pearaamatu saldod, konto järgi.
-   **BudgetActivities** – selle olemi koondab eelarvesaldod konto järgi.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Pearaamatud
-   ChartofAccounts

Need üksused olid saab luua arvutatud mõõtmeid andmemudel. Arvutatud mõõtmeid, kasutatakse tulemuslikkuse võtmenäitajate (KPI) ja aruanded, mida kasutatakse sisu Pack. Vaikimisi toob sisupakett sisse viimase kolme aasta ja ühe tulevase aasta andmed. Aruannetesse ja armatuurlauale lisaarvutuste kaasamiseks saate muuta [Microsoft Exceli töövihikut](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). See töövihik on vaikimisi andmemudel, mida kasutati sisupaketi loomiseks. Kui olete lõpetanud muudatuste tegemise, saate luua organisatsioonilise sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)



