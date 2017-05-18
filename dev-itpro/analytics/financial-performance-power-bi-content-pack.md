---
title: Finantstulemuste Power BI sisu
description: "See teema kirjeldab Microsoft Power BI-le mõeldud Microsoft Dynamics 365 for Operationsi finantstulemuste sisupaketti. See kirjeldab ka sisupaketis sisalduvaid armatuurlauda ja aruandeid ja annab teavet andmemudeli ja üksuste kohta, mida sisupaketi loomiseks kasutati."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: bb9a12dd45e227e86ba47c19f0850a73b77bc735
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="financial-performance-power-bi-content"></a>Finantstulemuste Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab Microsoft Power BI-le mõeldud Microsoft Dynamics 365 for Operationsi finantstulemuste sisupaketti. See kirjeldab ka sisupaketis sisalduvaid armatuurlauda ja aruandeid ja annab teavet andmemudeli ja üksuste kohta, mida sisupaketi loomiseks kasutati.

<a name="accessing-the-content-pack"></a>Juurdepääs sisupaketile
--------------------------

Saadaval on kaks finantstulemuste sisupaketi versiooni. Üks versioon on saadaval teenuste Microsoft Dynamics Lifecycle Services (LCS) kaudu ja teine PowerBI.com-ist.

-   **LCS-ist saadaolev versioon.** LCS-ist saadaolev finantstulemuste sisupakett toetab rakenduse Microsoft Dynamics 365 for Operations versiooni 1611. Sisupaketi leiate LCS-i ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle ühendamise kohta Microsoft Dynamics 365 for Operationsi andmetega vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).
-   **Power.BI.com-ist saadaolev versioon.** Power.BI.com-ist saadaolev finantstulemuste sisupakett toetab rakenduse Microsoft Dynamics AX versioone 7.0 ja 7.0.1. Lisateavet lahenduse Dynamics 365 for Operations andmete ühendamise ja laadimise kohta vt jaotisest [Juurdepääs Power BI sisule saidilt PowerBI.com](power-bi-home-page.md).

## <a name="main-account-setup"></a>Põhikonto seadistus
Kuna organisatsioonid soovivad kuvada kohustused ja tulusummad aruannetel positiivsete summadena, on põhikontode seadistus rakenduses Dynamics 365 for Operations oluline. Selleks, et need põhikontod kuvataks positiivsete summadena, peab põhikonto tüübiks olema määratud **Kohustus** või **Tulu**. Kui kasutatakse neid kontotüüpe, pööratakse aruande koostamisel Microsoft Power BI kaudu märgid ümber ja näidatakse summasid positiivsena.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad töölaud ja aruanded
Pärast sisupaketi ühendamist Dynamics 365 for Operationsi andmetega näitavad armatuurlaud ja aruanded teie finantsandmeid. Kui te pole Power BI-d varem kasutanud, saate selle kohta lisateavet lehelt [Power BI juhendatud õpe](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Armatuurlaud sisaldab aluseks olevatel aruannetel põhinevate andmete kokkuvõtlikke paane. Iga paan sisaldab kõigi organisatsiooni ettevõtete jooksva aasta kohta kokkuvõtlikku teavet. Siin on mõned neist paanidest.

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

Iga paan on varustatud toetava aruandega. Need aruanded sisaldavad nii teavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                      | Teave, mida aruanne sisaldab                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sularaha analüüs               | Sularaha juriidilise isiku järgi, sularaha kvartali järgi, kogu sularaha ja sularaha konto järgi **Märkus:** aruanne **Sularaha kvartali järgi** ei sisalda esimese kvartali koondsummas algsaldosid. Sellel on näha igas kvartalis sisestatud uute kannete koondsumma.                                                                                |
| Lühiajalise kohustuse kattekordaja analüüs      | Lühiajalise kohustuse kattekordaja juriidilise isiku järgi, lühiajalise kohustuse kattekordaja kvartali järgi ning käibevara ja lühiajaliste kohustuste saldod.                                                                                                                                                                                                                              |
| Likviidsuskordaja analüüs        | Likviidsuskordaja juriidilise isiku järgi, likviidsuskordaja kvartali järgi ja sularaha, müügireskontro ja lühiajaliste kohustuste saldod                                                                                                                                                                                                                      |
| Tuletusreegli analüüs | Tuletusreegel (COGS) juriidilise isiku järgi, COGS sellel aastal ja eelmisel aastal kvartali järgi, COGS müügile juriidilise isiku järgi, kogu COGS ja COGS müügiprotsendile                                                                                                                                                                                   |
| Käibekapitali analüüs    | Käibekapital juriidilise isiku järgi, käibekapital kvartali järgi, käibevara, lühiajalised kohustused ja kogu käibekapital                                                                                                                                                                                                                   |
| Vara ja võla analüüs     | Tagastus kogumaksumuselt ja võlgnevus varadele kokku juriidilise isiku järgi, võlgnevus varadele kokku ja tagastus kogumaksumuselt kvartalis praeguse kuupäevani, varad ja kohustused.                                                                                                                                                                                     |
| Kasumimarginaali analüüs      | Tegelik ja eelarve kasumimarginaal juriidilise isiku järgi, kasumimarginaal kvartali järgi, kasumimarginaali protsent ja kasumimarginaal                                                                                                                                                                                                                       |
| Netotulu analüüs         | Tegelik ja eelarveline netotulu juriidilise isiku järgi, netotulu sellel aastal ja eelmisel aastal ning kulud netotulu protsendile                                                                                                                                                                                                                       |
| Tulude analüüs           | Tegelikud ja eelarvelised tulud enne intressi ja makse (EBIT) juriidilise isiku järgi, EBIT sellel aastal ja eelmise aastal, kulud tulu suhtes protsent ning tegelikud ja eelarvelised kulud tulu suhtes                                                                                                                                                          |
| Tulu analüüs            | Kogutulu, tegelik ja eelarveline kogutulu juriidilise isiku järgi, kogutulu sellel ja eelmisel aastal, tulueelarve hälve juriidilise isiku järgi ning kogutulu sellel ja eelmisel perioodil                                                                                                                                                 |
| Kuluanalüüs            | Kogukulud, tegelikud eelarveliste kogukulude suhtes juriidilise isiku järgi, tegelik ja eelarveline kogukulu kvartali järgi, kogukulud konto kategooria järgi ning tegevuskulude suhe                                                                                                                                                                 |
| Arveldatud tulu analüüs     | Kogu müügireskontro, kogu müügireskontro juriidilise isiku järgi, kogu müügireskontro kvartali järgi ja müügireskontro kontode saldod **Märkus:** aruanded ei sisalda müügireskontro pearaamatukontode algsaldosid. Need näitavad müügireskontrosse sisestatud uute kannete koondsummat. |

Kõikidel nendel aruannetel olevaid diagramme ja paane saab filtreerida ja kinnitada armatuurlauale. Power BI-s filtreerimise ja kinnitamise kohta lisateabe saamiseks vaadake teemat [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Andmed, millega armatuurlaud ja aruanded finantstulemuste sisupaketis täidetakse, on Dynamics 365 for Operationsi andmed. Sisupaketi alusena kasutati järgmiseid üksuseid: **Koondandmete üksused**

-   **GeneralLedgerActivities** – see üksus koondab pearaamatu saldod konto kategooria järgi.
-   **BudgetActivities** – see üksus koondab eelarvesaldod konto kategooria järgi.

**Andmeüksused**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Pearaamatud
-   ChartofAccounts

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Arvutatud mõõtusid kasutatakse sisupaketis kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Vaikimisi toob sisupakett sisse viimase kolme aasta ja ühe tulevase aasta andmed. Aruannetesse ja armatuurlauale lisaarvutuste kaasamiseks saate muuta [Microsoft Exceli töövihikut](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi). See töövihik on vaikimisi andmemudel, mida kasutati sisupaketi loomiseks. Kui olete lõpetanud muudatuste tegemise, saate luua organisatsioonilise sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)





