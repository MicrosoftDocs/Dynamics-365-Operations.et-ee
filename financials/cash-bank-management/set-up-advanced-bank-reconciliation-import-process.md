---
title: "Täpsema panga vastavusseviimise importimisprotsessi seadistamine"
description: "Täpsema panga vastavusseviimise funktsiooni abil saate importida elektroonilisi pangaväljavõtteid ja neid rakenduses Microsoft Dynamics 365 for Operations automaatselt pangakannetega vastavusse viia. Selles artiklis selgitatakse, kuidas seadistada pangaväljavõtete impordifunktsiooni."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eab840b2974f4e9e8cf542c146482ba8e4239079
ms.openlocfilehash: acf7bacf6e95725024ff0a542a059349593d01a0
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Täpsema panga vastavusseviimise importimisprotsessi seadistamine

Täpsema panga vastavusseviimise funktsiooni abil saate importida elektroonilisi pangaväljavõtteid ja neid rakenduses Microsoft Dynamics 365 for Operations automaatselt pangakannetega vastavusse viia. Selles artiklis selgitatakse, kuidas seadistada pangaväljavõtete impordifunktsiooni. 

Pangaväljavõtte importimise seadistus erineb, olenevalt teie elektroonilise pangaväljavõtte vormingust. Microsoft Dynamics 365 toiminguteks toetab kolme panga skeeme karbist: ISO20022, MT940 ja BAI2.

## <a name="sample-files"></a>Näidisfailid
Kõik kolm formaate, peab teil faile, tõlkida elektroonilise panga väljavõtte originaal formaat vormingus, mida Dynamics 365 toiminguteks kasutada. Vajalikud ressursifailid leiate sõlmest **Ressursid** Microsoft Visual Studio Application Exploreris. Pärast failide leidmist kopeerige need ühte teadaolevasse asukohta, et saaksite need seadistusprotsessi ajal hõlpsamini üles laadida.

| Ressursi nimi                                           | Faili nimi                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_et\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_et\_sobitamine\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_et\_kombineeritud\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_et\_sobitamine\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_et\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_et\_sobitamine\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest
Allpool on näited arenenud panga vastavusseviimise impordi fail tehnilise ülesehituse mõisted ja kolm seotud panga väljavõtte näide failid: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Tehnilise paigutuse määratlus                             | Pangaväljavõtte näidisfail          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

## <a name="set-up-the-import-of-iso20022-bank-statements"></a>ISO20022 pangaväljavõtete impordi seadistamine
Esiteks peate määratlema pangaväljavõtte vormi töötlemisgrupi ISO20022 pangaväljavõtetele, kasutades andmeüksuse raamistikku.

1.  Mine **tööruumide**&gt;**andmete haldamiseks**.
2.  Click **Import**.
3.  Sisestage vormingu nimi, nt **ISO20022**.
4.  Määrake välja **Lähteandmete vorming **väärtuseks **XML-element**.
5.  Määrake väljale **Üksuse nimi** väärtus **Pangaväljavõtted**.
6.  Impordifailide üleslaadimiseks klõpsake valikut **Üleslaadimine** ja minge siis faili **SampleBankCompositeEntity.xml** juurde, mille varem salvestasite.
7.  Pärast pangaväljavõtete olemi üleslaadimist ja vastendamise lõpetamist klõpsake üksuse toimingut **Kuva kaart**.
8.  Pangaväljavõtte üksus on liitüksus, mis koosneb neljast eraldi üksusest. Valige loendist **BankStatementDocumentEntity** ja klõpsake siis toimingut **Kuva kaart**.
9.  Klõpsake vahekaardil **Teisendused** valikut **Uus**.
10. Klõpsake järjekorranumbri 1 puhul valikut **Laadi fail üles** ja valige fail** ISO20022XML-to-Reconciliation.xslt**, mille varem salvestasite. **Märkus:** Dynamics 365 tegevuse ümberkujundamise faile on loodud vormi. Kuna pangad sageli kehtivatest selles vormingus, peate vastendamiseks oma panga väljavõtte formaadis ümberkujundamise faili värskendama. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Click **New**.
12. Järjekorranumbri 2 puhul klõpsake valikut **Laadi fail üles** ja valige fail**BankReconciliation-to-Composite.xslt**, mille varem salvestasite.
13. Klõpsake valikut **Rakenda teisendused**.

Pärast vormingu töötlemise grupi seadistamist on järgmine samm määratleda ISO20022 pangaväljavõtetele vormingureeglid.

1.  Mine **raha ja panga juhtimise**&gt;**Setup**&gt;**Täpsem panga vastavusseviimise häälestus**&gt;**panga avalduse vormi**.
2.  Click **New**.
3.  Määratlege väljavõtte vorming, nt **ISO20022**.
4.  Sisestage vormingu nimi.
5.  Määrake väljal **Töötlemisgrupp** varem määratletud grupp, nt **ISO20022**.
6.  Märkige ruut **XML-fail**.

Viimane toiming on lubada täpsem panga vastavusseviimine ja määrata pangakontol väljavõtte vorming.

1.  Mine **raha ja pangakontod juhtimise**&gt;**panga**.
2.  Valige pangakonto ja avage see üksikasjade vaatamiseks.
3.  Määrake vahekaardil **Vastavusseviimine** valiku **Pangakonto täpsem vastavusseviimine **väärtuseks **Jah**.
4.  Määrake väljal **Väljavõtte vorming **varem loodud vorming, nt **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>MT940 pangaväljavõtete impordi seadistamine
Esiteks peate määratlema pangaväljavõtte vormi töötlemisgrupi MT940 pangaväljavõtetele, kasutades andmeüksuse raamistikku.

1.  Mine **tööruumide**&gt;**andmete haldamiseks**.
2.  Click **Import**.
3.  Sisestage vormingu nimi, nt **MT940**.
4.  Määrake välja **Lähteandmete vorming **väärtuseks **XML-element**.
5.  Määrake väljale **Üksuse nimi** väärtus **Pangaväljavõtted**.
6.  Impordifailide üleslaadimiseks klõpsake valikut **Üleslaadimine** ja minge siis faili **SampleBankCompositeEntity.xml** juurde, mille varem salvestasite.
7.  Pärast pangaväljavõtete olemi üleslaadimist ja vastendamise lõpetamist klõpsake üksuse toimingut **Kuva kaart**.
8.  Pangaväljavõtte üksus on liitüksus, mis koosneb neljast eraldi üksusest. Valige loendist **BankStatementDocumentEntity** ja klõpsake siis toimingut **Kuva kaart**.
9.  Klõpsake vahekaardil **Teisendused** valikut **Uus**.
10. Klõpsake järjekorranumbri 1 puhul valikut **Laadi fail üles** ja valige fail **MT940TXT-to-MT940XML.xslt**, mille varem salvestasite.
11. Klõpsake **Uus**.
12. Klõpsake järjekorranumbri 2 puhul valikut **Laadi fail üles** ja valige fail** MT940XML-to-Reconciliation.xslt**, mille varem salvestasite. **Märkus:** Dynamics 365 tegevuse ümberkujundamise faile on loodud vormi. Kuna pangad sageli kehtivatest selles vormingus, peate vastendamiseks oma panga väljavõtte formaadis ümberkujundamise faili värskendama. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Click **New**.
14. Järjekorranumbri 3 puhul klõpsake valikut **Laadi fail üles** ja valige fail**BankReconciliation-to-Composite.xslt**, mille varem salvestasite.
15. Klõpsake valikut **Rakenda teisendused**.

Pärast vormingu töötlemise grupi seadistamist on järgmine samm määratleda MT940 pangaväljavõtetele vormingureeglid.

1.  Mine **raha ja panga juhtimise**&gt;**Setup**&gt;**Täpsem panga vastavusseviimise häälestus**&gt;**panga avalduse vormi**.
2.  Click **New**.
3.  Määratlege väljavõtte vorming, nt **MT940**.
4.  Sisestage vormingu nimi.
5.  Määrake väljal **Töötlemisgrupp** varem määratletud grupp, nt **MT940**.
6.  Määrake välja **Faili tüüp** väärtuseks **txt**.

Viimane toiming on lubada täpsem panga vastavusseviimine ja määrata pangakontol väljavõtte vorming.

1.  Mine **raha ja pangakontod juhtimise**&gt;**panga**.
2.  Valige pangakonto ja avage see üksikasjade vaatamiseks.
3.  Määrake vahekaardil **Vastavusseviimine** valiku **Pangakonto täpsem vastavusseviimine** väärtuseks **Jah**.
4.  Kui teil palutakse oma valik kinnitada ja lubada täpsem pangakonto vastavusseviimine, klõpsake **OK**.
5.  Määrake väljal **Väljavõtte vorming **varem loodud vorming, nt **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>BAI2 pangaväljavõtete impordi seadistamine
Esiteks peate määratlema pangaväljavõtte vormi töötlemisgrupi BAI2 pangaväljavõtetele, kasutades andmeüksuse raamistikku.

1.  Mine **tööruumide**&gt;**andmete haldamiseks**.
2.  Click **Import**.
3.  Sisestage vormingu nimi, nt **BAI2**.
4.  Määrake välja **Lähteandmete vorming **väärtuseks **XML-element**.
5.  Määrake väljale **Üksuse nimi** väärtus **Pangaväljavõtted**.
6.  Impordifailide üleslaadimiseks klõpsake valikut **Üleslaadimine** ja minge siis faili **SampleBankCompositeEntity.xml** juurde, mille varem salvestasite.
7.  Pärast pangaväljavõtete olemi üleslaadimist ja vastendamise lõpetamist klõpsake üksuse toimingut **Kuva kaart**.
8.  Pangaväljavõtte üksus on liitüksus, mis koosneb neljast eraldi üksusest. Valige loendist **BankStatementDocumentEntity** ja klõpsake siis toimingut **Kuva kaart**.
9.  Klõpsake vahekaardil **Teisendused** valikut **Uus**.
10. Klõpsake järjekorranumbri 1 puhul valikut **Laadi fail üles** ja valige fail **BAI2CSV-to-BAI2XML.xslt**, mille varem salvestasite.
11. Klõpsake **Uus**.
12. Klõpsake järjekorranumbri 2 puhul valikut **Laadi fail üles** ja valige fail** BAI2XML-to-Reconciliation.xslt**, mille varem salvestasite. **Märkus:** Dynamics 365 tegevuse ümberkujundamise faile on loodud vormi. Kuna pangad sageli kehtivatest selles vormingus ja pead vastendamiseks oma panga väljavõtte formaadis ümberkujundamise faili värskendada. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Click **New**.
14. Järjekorranumbri 3 puhul klõpsake valikut **Laadi fail üles** ja valige fail**BankReconciliation-to-Composite.xslt**, mille varem salvestasite.
15. Klõpsake valikut **Rakenda teisendused**.

Pärast vormingu töötlemise grupi seadistamist on järgmine samm määratleda BAI2 pangaväljavõtetele vormingureeglid.

1.  Mine **raha ja panga juhtimise**&gt;**Setup**&gt;**Täpsem panga vastavusseviimise häälestus**&gt;**panga avalduse vormi**.
2.  Click **New**.
3.  Määratlege väljavõtte vorming, nt **BAI2**.
4.  Sisestage vormingu nimi.
5.  Määrake väljal **Töötlemisgrupp** varem määratletud grupp, nt **BAI2**.
6.  Määrake välja **Faili tüüp** väärtuseks **txt**.

Viimane toiming on lubada täpsem panga vastavusseviimine ja määrata pangakontol väljavõtte vorming.

1.  Mine **raha ja pangakontod juhtimise**&gt;**panga**.
2.  Valige pangakonto ja avage see üksikasjade vaatamiseks.
3.  Määrake vahekaardil **Vastavusseviimine** valiku **Pangakonto täpsem vastavusseviimine** väärtuseks **Jah**.
4.  Kui teil palutakse oma valik kinnitada ja lubada täpsem pangakonto vastavusseviimine, klõpsake **OK**.
5.  Määrake väljal **Väljavõtte vorming **varem loodud vorming, nt **BAI2**.

## <a name="test-the-bank-statement-import"></a>Pangaväljavõtte impordi proovimine
Viimane toiming on proovimine, kas saate oma pangaväljavõtte importida.

1.  Mine **raha ja pangakontod juhtimise**&gt;**panga**.
2.  Valige pangakonto, millel täpsem panga vastavusseviimise funktsioon on lubatud.
3.  Klõpsake vahekaardil **Vii vastavusse** valikut **Pangaväljavõtted**.
4.  Klõpsake lehel **Pangaväljavõte** valikut **Väljavõtte importimine**.
5.  Määrake väljale **Pangakonto** valitud pangakonto. Väli **Väljavõtte vorming** määratakse automaatselt pangakonto seadistuse põhjal.
6.  Klõpsake valikut **Sirvi** ja valige elektroonilise pangaväljavõtte fail.
7.  Klõpsake **Üleslaadimine**.
8.  Klõpsake nupul **OK**.

Kui importimine õnnestub, saate teate, milles on öeldud, et teie väljavõte on imporditud. Kui importimine ei õnnestunud, otsige tööruumist **Andmehaldus** jaotises **Tööde ajalugu** töö üles. Klõpsake töö kohta valikut **Käivitamise üksikasjad** lehe **Käivitamise kokkuvõte** avamiseks ja seejärel klõpsake imporditõrgete kuvamiseks valikut **Kuva käivituslogi**.


