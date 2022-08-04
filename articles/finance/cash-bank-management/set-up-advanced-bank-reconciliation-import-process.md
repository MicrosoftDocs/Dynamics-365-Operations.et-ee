---
title: Täpsema panga vastavusseviimise importimisprotsessi seadistamine
description: Täpsem panga vastavusseviimise funktsioon võimaldab teil importida elektroonilisi pangaväljavõtteid ja viia need automaatselt vastavusse pangakannetega Microsoft Dynamics 365 finantsis. Selles artiklis selgitatakse, kuidas seadistada pangaväljavõtete impordifunktsiooni.
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8d186e6b3e44222410c8be94390d7c58a90e352
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151518"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Täpsema panga vastavusseviimise importimise protsessi häälestus

[!include [banner](../includes/banner.md)]

> [!NOTE]
> See funktsioon on aegunud septembrist 2022, uued kasutajad peaksid kasutama elektroonilist aruandlust. Lisateabe saamiseks vt täpsema panga [vastavusseviimise impordi seadistamist elektroonilise aruandluse abil](../accounts-payable/import-bai2-er.md).


Täpsema panga vastavusseviimise funktsioon võimaldab teil importida elektroonilisi pangaväljavõtteid ja viia need automaatselt vastavusse pangakannetega Dynamics 365 Financeis. Selles artiklis selgitatakse, kuidas seadistada pangaväljavõtete impordifunktsiooni. 

Pangaväljavõtte importimise seadistus erineb, olenevalt teie elektroonilise pangaväljavõtte vormingust. Finance toetab kolme valmis pangaväljavõtte vormingut: ISO20022, MT940 ja BAI2.

## <a name="set-time-zone-preference"></a>Ajavööndi eelistuse seadistamine
Pangaväljavõtte importimise sätete konfigureerimisel võib olla oluline arvestada imporditavate pangaväljavõtte failide kuupäeva-kellaaja ajavööndi andmeid. Vaikimisi eeldatakse, et kõik kuupäeva ja kellaaja väärtused on juba kooskõlastatud maailmaajaga (UTC) ja seetõttu ei rakendata andmeid importimisel ajavööndite konverteerimist. 

Saadaval on suvand andmete importimisel kasutatava ajavööndi määramiseks. See suvand on saadaval väljal **Ajavööndi eelistus** igal **Algandmete vorminduse üksikasjade** lehel (kiirkaart **Andmehalduse tööruum > Lähteandmete konfigureerimine > Andmete vormingu valimine > Piirkondlikud sätted**). Teie sisestatud ajavööndi eelistus rakendub kõigile importimistele, mis kasutab seda lähteandmete vormingut. Saate luua nii palju andmeallika vorminguid kui vaja, et importida andmeid mitmest ajavööndist.  

See ajavöönd ei pruugi olla sama kui kasutaja või ettevõtte ajavöönd, seega selgitage välja, millist ajavööndit kuupäeva ja kellaaja andmed kasutavad. Ajavööndi eelistuse määramisel soovitame arvestada järgmiste punktidega. 

 - Ajavööndi eelistus rakendub kõigile importimistele, mis kasutavad seda lähteandmete vormingut. Saate luua nii palju andmeallika vorminguid kui vaja mitmest ajavööndist andmete importimisega toimetulekuks. 
 
 - Ajavööndi eelistus peaks olema impordifaili kohaliku kuupäeva ja kellaaja andmete ajavöönd. 
 
 - Kuupäeva ja kellaaja andmete ajavöönd ei pruugi olla sama mis kasutaja või ettevõtte ajavöönd.
 
 - Kasutajad saavad oma ajavööndit oma **kasutaja suvandite** abil korrigeerida.

Võtke arvesse, et järgmised tegevused võivad aidata vähendada potentsiaalseid kuupäeva ja kellaaja konflikte pangakonto väljavõtete importimisel. 

 - Vältige ajavööndi eelistuste muutmist kõigi pangakontode puhul, millel on juba imporditud väljavõtteid. Ajavööndi eelistuse muutmine võib ajavööndi korrigeerimise tõttu mõjutada uute väljavõtete tellimist võrreldes olemasolevate väljavõtetega. 
 
 - Vaadake üle kõik impordid, mis kasutavad valitud andmeallika vormingut. Vormingu jaoks määratud ajavööndi eelistus rakendub kõigile seda vormingut kasutavatele impordiprojektidele. Kinnitage, et ajavööndi eelistus on sobiv kõigi seda vormingut kasutavate impordiprojektide jaoks.

## <a name="sample-files"></a>Näidisfailid
Kõigi kolme vormingu puhul peavad teil olema failid, mis teisendavad elektroonilise pangaväljavõtte algsest vormingust sellisesse vormingusse, mida Finance saab kasutada. Vajalikud ressursifailid leiate Microsoft Visual Studio Application Exploreris sõlmest **Ressursid**. Pärast failide leidmist kopeerige need ühte teadaolevasse asukohta, et saaksite need seadistusprotsessi ajal hõlpsamini üles laadida.

| Ressursi nimi                                           | Faili nimi                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest
Allpool on näited täiustatud panga vastavusseviimise impordifaili tehniliste paigutuste määratlustest ja kolmest seotud pangaväljavõtte näidisfailist: [Impodifaili näited](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehnilise paigutuse määratlus                             | Pangaväljavõtte näidisfail          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>ISO20022 pangaväljavõtete impordi seadistamine
Esiteks peate määratlema pangaväljavõtte vormi töötlemisgrupi ISO20022 pangaväljavõtetele, kasutades andmeüksuse raamistikku.

1.  Avage **Tööruumid** &gt; **Andmehaldus**.
2.  Klõpsake nuppu **Impordi**.
3.  Sisestage vormingu nimi, nt **ISO20022**.
4.  Määrake välja **Lähteandmete vorming** väärtuseks **XML-element**.
5.  Määrake väljale **Üksuse nimi** väärtus **Pangaväljavõtted**.
6.  Impordifailide üleslaadimiseks klõpsake valikut **Üleslaadimine** ja minge siis faili **SampleBankCompositeEntity.xml** juurde, mille varem salvestasite.
7.  Pärast pangaväljavõtete olemi üleslaadimist ja vastendamise lõpetamist klõpsake üksuse toimingut **Kuva kaart**.
8.  Pangaväljavõtte üksus on liitüksus, mis koosneb neljast eraldi üksusest. Valige loendist **BankStatementDocumentEntity** ja klõpsake siis toimingut **Kuva kaart**.
9.  Klõpsake vahekaardil **Teisendused** valikut **Uus**.
10. Klõpsake järjekorranumbri 1 puhul valikut **Laadi fail üles** ja valige fail **ISO20022XML-to-Reconciliation.xslt**, mille varem salvestasite. **Märkus.** Teisendusfailid on koostatud standardvormingu jaoks. Kuna pangad kalduvad sellest vormingust sageli kõrvale, tuleb teil vajaduse korral värskendada teisendusfaili teie pangaväljavõtte vorminguga vastendamiseks. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Klõpsake nuppu **Uus**.
12. Järjekorranumbri 2 puhul klõpsake valikut **Laadi fail üles** ja valige fail **BankReconciliation-to-Composite.xslt**, mille varem salvestasite.
13. Klõpsake valikut **Rakenda teisendused**.

Pärast vormingu töötlemise grupi seadistamist on järgmine samm määratleda ISO20022 pangaväljavõtetele vormingureeglid.

1.  Valige **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Pangakonto täpsema vastavusseviimise seadistus** &gt; **Pangaväljavõtte vorming**.
2.  Klõpsake nuppu **Uus**.
3.  Määratlege väljavõtte vorming, nt **ISO20022**.
4.  Sisestage vormingu nimi.
5.  Määrake väljal **Töötlemisgrupp** varem määratletud grupp, nt **ISO20022**.
6.  Märkige ruut **XML-fail**.

Viimane toiming on lubada täpsem panga vastavusseviimine ja määrata pangakontol väljavõtte vorming.

1.  Avage **Sularaha- ja pangahaldus** &gt; **Pangakontod**.
2.  Valige pangakonto ja avage see üksikasjade vaatamiseks.
3.  Määrake vahekaardil **Vastavusseviimine** valiku **Pangakonto täpsem vastavusseviimine** väärtuseks **Jah**.
4.  Määrake väljal **Väljavõtte vorming** varem loodud vorming, nt **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>MT940 pangaväljavõtete impordi seadistamine
Esiteks peate määratlema pangaväljavõtte vormi töötlemisgrupi MT940 pangaväljavõtetele, kasutades andmeüksuse raamistikku.

1.  Avage **Tööruumid** &gt; **Andmehaldus**.
2.  Klõpsake nuppu **Impordi**.
3.  Sisestage vormingu nimi, nt **MT940**.
4.  Määrake välja **Lähteandmete vorming** väärtuseks **XML-element**.
5.  Määrake väljale **Üksuse nimi** väärtus **Pangaväljavõtted**.
6.  Impordifailide üleslaadimiseks klõpsake valikut **Üleslaadimine** ja minge siis faili **SampleBankCompositeEntity.xml** juurde, mille varem salvestasite.
7.  Pärast pangaväljavõtete olemi üleslaadimist ja vastendamise lõpetamist klõpsake üksuse toimingut **Kuva kaart**.
8.  Pangaväljavõtte üksus on liitüksus, mis koosneb neljast eraldi üksusest. Valige loendist **BankStatementDocumentEntity** ja klõpsake siis toimingut **Kuva kaart**.
9.  Klõpsake vahekaardil **Teisendused** valikut **Uus**.
10. Klõpsake järjekorranumbri 1 puhul valikut **Laadi fail üles** ja valige fail **MT940TXT-to-MT940XML.xslt**, mille varem salvestasite.
11. Klõpsake **Uus**.
12. Klõpsake järjekorranumbri 2 puhul valikut **Laadi fail üles** ja valige fail **MT940XML-to-Reconciliation.xslt**, mille varem salvestasite. **Märkus.** Teisendusfailid on koostatud standardvormingu jaoks. Kuna pangad kalduvad sellest vormingust sageli kõrvale, tuleb teil vajaduse korral värskendada teisendusfaili teie pangaväljavõtte vorminguga vastendamiseks. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Klõpsake nuppu **Uus**.
14. Järjekorranumbri 3 puhul klõpsake valikut **Laadi fail üles** ja valige fail **BankReconciliation-to-Composite.xslt**, mille varem salvestasite.
15. Klõpsake valikut **Rakenda teisendused**.

Pärast vormingu töötlemise grupi seadistamist on järgmine samm määratleda MT940 pangaväljavõtetele vormingureeglid.

1.  Valige **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Pangakonto täpsema vastavusseviimise seadistus** &gt; **Pangaväljavõtte vorming**.
2.  Klõpsake nuppu **Uus**.
3.  Määratlege väljavõtte vorming, nt **MT940**.
4.  Sisestage vormingu nimi.
5.  Määrake väljal **Töötlemisgrupp** varem määratletud grupp, nt **MT940**.
6.  Määrake välja **Faili tüüp** väärtuseks **txt**.

Viimane toiming on lubada täpsem panga vastavusseviimine ja määrata pangakontol väljavõtte vorming.

1.  Avage **Sularaha- ja pangahaldus** &gt; **Pangakontod**.
2.  Valige pangakonto ja avage see üksikasjade vaatamiseks.
3.  Määrake vahekaardil **Vastavusseviimine** valiku **Pangakonto täpsem vastavusseviimine** väärtuseks **Jah**.
4.  Kui teil palutakse oma valik kinnitada ja lubada täpsem pangakonto vastavusseviimine, klõpsake **OK**.
5.  Määrake väljal **Väljavõtte vorming** varem loodud vorming, nt **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>BAI2 pangaväljavõtete impordi seadistamine
Esiteks peate määratlema pangaväljavõtte vormi töötlemisgrupi BAI2 pangaväljavõtetele, kasutades andmeüksuse raamistikku.

1.  Avage **Tööruumid** &gt; **Andmehaldus**.
2.  Klõpsake nuppu **Impordi**.
3.  Sisestage vormingu nimi, nt **BAI2**.
4.  Määrake välja **Lähteandmete vorming** väärtuseks **XML-element**.
5.  Määrake väljale **Üksuse nimi** väärtus **Pangaväljavõtted**.
6.  Impordifailide üleslaadimiseks klõpsake valikut **Üleslaadimine** ja minge siis faili **SampleBankCompositeEntity.xml** juurde, mille varem salvestasite.
7.  Pärast pangaväljavõtete olemi üleslaadimist ja vastendamise lõpetamist klõpsake üksuse toimingut **Kuva kaart**.
8.  Pangaväljavõtte üksus on liitüksus, mis koosneb neljast eraldi üksusest. Valige loendist **BankStatementDocumentEntity** ja klõpsake siis toimingut **Kuva kaart**.
9.  Klõpsake vahekaardil **Teisendused** valikut **Uus**.
10. Klõpsake järjekorranumbri 1 puhul valikut **Laadi fail üles** ja valige fail **BAI2CSV-to-BAI2XML.xslt**, mille varem salvestasite.
11. Klõpsake **Uus**.
12. Klõpsake järjekorranumbri 2 puhul valikut **Laadi fail üles** ja valige fail **BAI2XML-to-Reconciliation.xslt**, mille varem salvestasite. **Märkus.** Teisendusfailid on koostatud standardvormingu jaoks. Kuna pangad kalduvad sellest vormingust sageli kõrvale ja teil tuleb vajaduse korral värskendada teisendusfaili teie pangaväljavõtte vorminguga vastendamiseks. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Klõpsake nuppu **Uus**.
14. Järjekorranumbri 3 puhul klõpsake valikut **Laadi fail üles** ja valige fail **BankReconciliation-to-Composite.xslt**, mille varem salvestasite.
15. Klõpsake valikut **Rakenda teisendused**.

Pärast vormingu töötlemise grupi seadistamist on järgmine samm määratleda BAI2 pangaväljavõtetele vormingureeglid.

1.  Valige **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Pangakonto täpsema vastavusseviimise seadistus** &gt; **Pangaväljavõtte vorming**.
2.  Klõpsake nuppu **Uus**.
3.  Määratlege väljavõtte vorming, nt **BAI2**.
4.  Sisestage vormingu nimi.
5.  Määrake väljal **Töötlemisgrupp** varem määratletud grupp, nt **BAI2**.
6.  Määrake välja **Faili tüüp** väärtuseks **txt**.

Viimane toiming on lubada täpsem panga vastavusseviimine ja määrata pangakontol väljavõtte vorming.

1.  Avage **Sularaha- ja pangahaldus** &gt; **Pangakontod**.
2.  Valige pangakonto ja avage see üksikasjade vaatamiseks.
3.  Määrake vahekaardil **Vastavusseviimine** valiku **Pangakonto täpsem vastavusseviimine** väärtuseks **Jah**.
4.  Kui teil palutakse oma valik kinnitada ja lubada täpsem pangakonto vastavusseviimine, klõpsake **OK**.
5.  Määrake väljal **Väljavõtte vorming** varem loodud vorming, nt **BAI2**.

## <a name="test-the-bank-statement-import"></a>Pangaväljavõtte impordi proovimine
Viimane toiming on proovimine, kas saate oma pangaväljavõtte importida.

1.  Avage **Sularaha- ja pangahaldus** &gt; **Pangakontod**.
2.  Valige pangakonto, millel täpsem panga vastavusseviimise funktsioon on lubatud.
3.  Klõpsake vahekaardil **Vii vastavusse** valikut **Pangaväljavõtted**.
4.  Klõpsake lehel **Pangaväljavõte** valikut **Väljavõtte importimine**.
5.  Määrake väljale **Pangakonto** valitud pangakonto. Väli **Väljavõtte vorming** määratakse automaatselt pangakonto seadistuse põhjal.
6.  Klõpsake valikut **Sirvi** ja valige elektroonilise pangaväljavõtte fail.
7.  Klõpsake **Üleslaadimine**.
8.  Klõpsake nupul **OK**.

Kui importimine õnnestub, saate teate, milles on öeldud, et teie väljavõte on imporditud. Kui importimine ei õnnestunud, otsige tööruumist **Andmehaldus** jaotises **Tööde ajalugu** töö üles. Klõpsake töö kohta valikut **Käivitamise üksikasjad** lehe **Käivitamise kokkuvõte** avamiseks ja seejärel klõpsake imporditõrgete kuvamiseks valikut **Kuva käivituslogi**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
