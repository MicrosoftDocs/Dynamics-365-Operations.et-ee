---
title: KM-i deklaratsioon (Saksamaa)
description: See teema kirjeldab, kuidas seadistada ja luua Saksamaa ettemakse käibemaksu deklaratsioon ametlikus XML-vormingus.
author: anasyash
ms.date: 11/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 29c04e1034c05b4672f3657ce0b7bc9d5f6d7c9c
ms.sourcegitcommit: 8c17717b800c2649af573851ab640368af299981
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7860865"
---
# <a name="vat-declaration-germany"></a>KM-i deklaratsioon (Saksamaa)

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada ja luua Saksamaa ettemakse käibemaksu deklaratsioon ametlikus XML-vormingus. See teema selgitab ka, kuidas KM-i deklaratsiooni eelvaadet vaadata Microsoft Excel.

Aruande automaatseks loomiseks looge piisavalt käibemaksukoode, et hoida eraldi KM-i raamatupidamine iga välja puhul käibemaksu ettemaksu deklaratsioonis. Lisaks seostage käibemaksukoodid elektroonilise aruandluse (ER) rakendusspetsiifilistes parameetrites käibemaksukoodide otsingutulemusega km-deklaratsiooni väljade otsingutulemusega.

Saksamaa puhul peate konfigureerima **aruandevälja otsingu**. Rakendusespetsiifiliste parameetrite seadistuse kohta lisateabe saamiseks vt selles teemas jaotist KM-i deklaratsiooni väljade rakendusespetsiifiliste parameetrite [seadistamine](#set-up-application-specific-parameters-for-vat-declaration-fields).

Järgmises tabelis kuvatakse veerus "Otsingu tulemus" otsingutulemus, mis on eelkonfigureeritud kindla KM-i deklaratsiooni reale KM-deklaratsiooni vormingus. Kasutage seda teavet käibemaksukoodide õigeks seostamiseks otsingutulemusega ja seejärel KM-i deklaratsiooni reaga.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a> KM-i deklaratsiooni ülevaade

Saksamaa käibemaksu ettemaksu deklaratsioon sisaldab järgmist teavet.

**JAOTIS – TARNED JA MUUD TEENUSED**

**Maksustatav müük**

| Rida | Kast – maksubaas | Kast – maksusumma | Kirjeldus                                                                                                                                      | Otsingu tulemus                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Koodita     | Maksustatav müük maksumääraga 19 protsenti.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – miinusmärgiga             |
| 21  | 86             | Koodita     | Maksustatav müük maksumääraga 7 protsenti.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – miinusmärgiga               |
| 22  | 35             | 36               | Maksustatav müük muude maksumääraga.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – miinusmärgiga      |
| 23  | 77             | *Maksusumma puudub*  | Vastavalt Saksa käibemaksuseaduse (UStG) 24 .24-le on toiduainete- ja toiduaineteettevõtte tarned käibemaksu ID-numbriga klientidele. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – miinusmärgiga |
| 24  | 76             | 80               | Müük, mille eest tuleb tasuda maks vastavalt UStG-le (24 UStG-d ksaanitooted, joogid ja lisalikviited).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Maksuvaba müük sisendkäibemaksu mahaarvamisega**

| Rida | Kast – maksubaas | Kast – maksusumma | Kirjeldus                                                                       | Otsingu tulemus                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Maksusumma puudub*  | Euroopa Liidu sisesed tarned klientidele, mille KM-i ID on.                       | 26-EUSales                          |
| 27  | 44             | *Maksusumma puudub*  | ELi-sisesed uute sõidukite tarned ostjatele, tal ei ole KM-i ID-d.    | 27-EUSalesNewVehiopia               |
| 28  | 49             | *Maksusumma puudub*  | ELi-sisesed uute sõidukite tarned väljaspool ettevõtet.                     | 28-EUSalesNewVehikestusOutsideCompany |
| 29  | 43             | *Maksusumma puudub*  | Muu maksuvaba müük, mille puhul sisendmaksu mahaarvamine, nt ekspordi tarned. | 29-ExportOtherTaxFreeSales          |

**Maksuvaba müük sisendkäibemaksu mahaarvamiseta**

| Rida | Kast – maksubaas | Kast – maksusumma | Kirjeldus                                            | Otsingu tulemus                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Maksusumma puudub*  | Maksuvaba müük, mis ei oma sisendmaksu mahaarvamist. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**ÜHENDUSEsisesed soetamised**

| Rida | Kast – maksubaas | Kast – maksusumma | Kirjeldus                                                                                                                   | Otsingu tulemus                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Maksusumma puudub*  | Maksuvabad kogukonnasisesed mõne objekti soetus ja kuldinvesteeringud.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Koodita     | Maksustatavad EL-sisesed soetamised maksumääraga 19 protsenti.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Koodita     | Maksustatavad EL-sisesed soetamised maksumääraga 7 protsenti.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Maksustatavad EL-sisesed soetamised muude maksumääradega.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Maksustatavad uute sõidukite ühendusesisesed soetamised hankijalt, tal ei ole käibemaksu ID-numbrit üldises maksumääras. | 37-EUPurchaseVehitool</br>37-UseTaxEUPurchaseVehitool (94/96/61)     |

**JAOTIS – KASUSAAJA MAKSUDEEBITI**

| Rida | Kast – maksubaas | Kast – maksusumma | Kirjeldus                                                                        | Otsingu tulemus                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Muud kogukonna teenused, mis põhinevad ülejäänud ühenduse alal.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Paragrahvi 13b (2) nr all kuuluvad müügid. 3 UStG- st.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Muud teenused, mis kuuluvad paragrahvi 13b (2) nr alla. 1, 2 ja 4 kuni 12 UStG-st. | 42-KasusaajaTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**JAOTIS – LISATEAVE MÜÜGI KOHTA**

| Rida | Kast – maksubaas  | Kast – maksusumma | Kirjeldus                                                                                                | Otsingu tulemus                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Maksusumma puudub*  | Tarned esimese kliendi poolt EL-sisese kolmnurkkande puhul.                   | 48-tarnedFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Maksusumma puudub*  | Selle teenuse saaja maksustatav müügisumma, mille alusel teenuse saaja maksu võlgneb. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Maksusumma puudub*  | Muud mittemaksustavad teenused.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Maksusumma puudub*  | Muu mittemaksustatav müük, kui jõudluse koht ei ole Saksamaal.                                    | 51-MuudSalesNonTaxable                                                                          |
| 52  | *Maksusumma puudub* | *Maksusumma puudub*  | KM.                                                                                                       | Rida 20 + Rida 21 + Rida 22 + Rida 4 + Rida 34 + Rida 35 + Rida 36 + Rida 37 + Rida 40 + Rida 41 + Rida 42 |

**JAOTIS – MAHAARVATAV SISENDMAKS**

| Rida | Kast – maksusumma | Kirjeldus                                                                                                | Otsingu tulemus                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Sisendarve maksusummad teistelt ettevõtetelt, teenustelt ja KOGUKONNAsisestelt kolmnurkkannetelt.     | 55-InputTax 40-UseTaxBenefaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – miinusmärgiga                                                                   |
| 56  | 61               | Sisendmaksu summad ühendusesisesest kaupade soetamisest.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehitool (94/96/61) |
| 57  | 62               | Tekkinud impordi käibemaks.                                                                                 | 57-inputTaxImport                                                                                                                                                            |
| 58  | 67               | Sisendmaksu summad teenustelt UStG -13b mõistes.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Sisendmaksu summad, mis arvutatakse üldiste keskmiste määrade alusel.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – miinusmärgiga                                                                                    |
| 60  | 59               | Sisendmaksu mahaarvamine ühendusesiseste tarnete puhul uute sõidukite puhul väljaspool ettevõtet ja väikeettevõtteid. | 60-InputTaxEUPurchaseNewVehitool</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehitool (59/37) – miinusmärgiga                                                                  |
| 61  | 64               | Sisendmaksu mahaarvamise parandamine.                                                                     | 61-inputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Ülejäänud summa.                                                                                      | 52. rida – 55. rida – rida 56 – rida 57 – 58. rida – 60. rida – rida 61                                                                                                        |

**SEKTSIOON – MUUD MAKSUSUMMAD**

| Rida | Kast – maksusumma | Kirjeldus                                                                                                                                                                                                                                                         | Otsingu tulemus                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Maks maksustamise ja täiendava maksu kaudu maksustatud maksetelt muutuse tõttu maksumääras.                                                                                                                                        | 64-täiendavtaxDueChangeTaxRate              |
| 65  | 69               | Arvetel kuvatavad valed või osamaksusummad ja arvetel kuvatavad maksusummad, mis on võlgnetavad vastavalt 2. peatüki 6a (4) lausele, paragrahvile 17 (1) lausele 7 või UStG paragrahvile 25b (2) või mida võlgneb allhankiv ettevõte või laopidaja. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Püsiva laiendi fikseeritud erimakse mahaarvamine. Sellele reale sisestatakse tavaliselt ainult maksuperioodi viimane etteteatis.                                                                                                  | Kasutaja sisestusparameeter aruande dialoogiboksis |
| 68  | 83               | Järelejäänud ettemakse käibemaksu makse ja järelejäänud ülejääk. Saate summa ette kaasata miinuslogi.                                                                                                                                                          | 62. rida + 64. rida – rida 65 – rida 66             |

**JAOTIS – LISATEAVE VÄHENDAMISTE KOHTA**

| Rida | Kast – maksubaas | Kast – maksusumma | Kirjeldus                                                            | Otsingu tulemus                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Ridadel 20–24 oleva maksubaasi vähendamine.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Mahaarvatavate sisendmaksu summade vähendamine ridadel 55, 59 ja 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehitool (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Ostu pöördtasu KM

Kui konfigureerite käibemaksukoode sissetuleva pöördtasu KM-i sisestamiseks kasutusmaksu abil, seostage oma käibemaksukoodid otsingutulemusega aruandevälja otsingust, mis sisaldab **nimes** "UseTax".

Teise võimalusena saate konfigureerida kaks eraldi käibemaksukoodi: üks käibemaksule ja teine käibemaksu mahaarvamiseks. Seejärel seostage iga kood aruandevälja otsingu **vastavate otsingutulemustega.**

Näiteks standardse määraga maksustatavate kogukonnasiseste soetamiste puhul peate konfigureerima käibemaksukoodi UT_S_EU kasutusmaksuga ja seostama **selle** **34-UseTaxEUPurchaseStandardi otsingutulemusega** **Aruandeväli**. Sel juhul kajastuvad käibemaksukoodi kasutavad UT_S_EU väljadele **089** ja 061 (read 34 ja 56).

Teise võimalusena konfigureerite kaks käibemaksukoodi:

  - **VAT_S_EU,** mille maksumäära väärtus on -19 protsenti
  - **InVAT_S_EU,** mille maksumäära väärtus on 19 protsenti

Seejärel seostate koodid **aruandevälja** otsingutulemustega järgmisel viisil:

  - Saate **VAT_S_EU** **34-EUPurchaseStandard** otsingutulemusega.
  - Saate **InVAT_S_EU** **56-InputTaxEUPurchase** otsingutulemusega.

Sel juhul kajastuvad käibemaksukoodi VAT_S_EU summad **kastis** 089 (rida 34). Summad, **mida InVAT_S_EU** käibemaksukoodi puhul, kajastuvad ka kastis 061 (rida 56).

Lisateavet pöördtasu KM konfigureerimise kohta vt [Pöördtasud](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Süsteemiparameetrite konfigureerimine

KM-i deklaratsiooni loomiseks peate konfigureerima oma organisatsiooni maksukoodi (Steuernummer).

1. Avage **Organisatsiooni haldus** > **Organisatsioonid** > **Juriidilised isikud**.
2. Valige juriidiline isik ja seejärel registreerimise **ID-d.**
3. Valige või looge aadress Saksamaal ja seejärel valige **kiirkaardil Registreerimise ID** suvand **Lisa**.
4. Väljal Registreerimise tüüp valige registreerimistüüp, mis on mõeldud Saksamaale ja mis kasutab **Ettevõtte** **ID -d (COID)** registreerimiskategooriat.
5. Väljale **Registreerimisnumber** sisestage maksunumber.
6. Sisestage **vahekaardi** Üldine väljale **Jõustus** kuupäev, millal number jõustub.

Registreerimiskategooriate ja registreerimistüüpide kohta lisateabe saamiseks vt registreerimise [ID-sid.](emea-registration-ids.md)

## <a name="set-up-a-vat-declaration-for-germany"></a>Saksamaa KM-i deklaratsiooni seadistamine

### <a name="import-er-configurations"></a>Elektroonilise aruandluse konfiguratsioonide importimine

Avage elektroonilise **aruandluse** tööruum ja importige järgmised või hilisemad neist ER-vormingutest:

   - KM-deklaratsiooni Excel (DE).version.101.16.12.xml
   - KM-deklaratsiooni XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a> Saate häälestada KM-i deklaratsiooniväljade rakendusspetsiifilisi parameetreid.

KM-i deklaratsiooni automaatseks loomiseks seostage käibemaksukoodid rakenduses ja otsingutulemused ER-i konfiguratsioonis.

Järgige neid samme, et määrata, millised käibemaksukoodid loovad millised väljad KM-i deklaratsioonil.

1. Minge **tööruumide elektroonilise** > **aruandluse juurde ja valige aruandluse** **konfiguratsioonid.**
2. Valige **KM-deklaratsiooni XML-i (DE)** konfiguratsioon ja seejärel **konfiguratsioonide rakenduse kindlate parameetrite \>** seadistus.
3. Valige **rakendusespetsiifiliste** parameetrite lehe otsingu **kiirkaardil** **aruandevälja** otsing.
4. Seadke **Kiirkaardil** Tingimused käibemaksukoodide ja aruandeväljade seostamiseks järgmised väljad.

    | Field                  | Kirjeldus                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Otsingu tulemus          | Valige aruandevälja väärtus. Lisateavet väärtuste ja nende määramise kohta KM-i deklaratsiooni ridadele vt selle teema [varasemast KM-i](#vat-declaration-overview) deklaratsiooni ülevaate jaotisest.                                                                                               |
    | Maksukood               | Valige käibemaksukood, mida aruandeväljaga seostada. Valitud käibemaksukoodi kasutavad sisestatud maksukanded kogutakse vastavasse deklaratsiooniboksi. Soovitame käibemaksukoodid eraldada nii, et üks käibemaksukood loob summad ainult ühes deklaratsioonikastis. |
    | Kande liigitaja | Kui lõite deklaratsiooniboksi määramiseks piisavalt käibemaksukoode, valige **\* suvand Mitte \*** tühi. Kui te ei loo piisavalt käibemaksukoode, nii et üks käibemaksukood loob summad ainult ühes deklaratsiooniboksis, saate seadistada kande liigitaja. Saadaval on järgmised kandeklassid:</br>-   **Ost**</br>-   **PurchaseExempt** (maksuvaba ost)</br>-   **PurchaseReverseCharge** (ostu pöördtasult saadaolev maks)</br>-   **Müük**</br>-   **SalesExempt** (maksuvaba müük)</br>-   **SalesReverseCharge** (ostu pöördtasult või müügi pöördtasult makstav maks)</br>-   **Kasutusmaks**. </br>Iga kandeklassi jaoks on saadaval ka kreeditarve klassifikaatorid. Näiteks on üks nendest klassifikaatoriist **PurchaseCreditNote** (ostu kreeditarve).</br>Looge kindlasti kaks rida iga käibemaksukoodi kohta: üks, mille kandeklassifikaatori väärtus on ja teine, mille kande klassifikaatoriks on kreeditarve väärtus. |

    > [!NOTE]
    > Saate kõik käibemaksukoodid otsingutulemustega seostada. Kui mõni käibemaksukood ei peaks km-deklaratsioonile väärtusi tekitama, seostage need muu **otsingutulemusega**.

    ![Rakendusekohaste parameetrite leht](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. Muutke **välja** Olek väärtuseks **Lõpetatud**.
6. Tegevuspaanil valige **ekspordi**, et eksportida rakendusespetsiifiliste parameetrite sätted.
7. Valige KM-i deklaratsiooni Exceli (DE) konfiguratsioon ja seejärel valige toimingupaanil suvand Impordi, et importida parameetrid, mis te konfigureerinud **KM**-deklaratsiooni **·** **XML-i (DE)** jaoks.
8. Valige väljalt **Olek** suvand **Lõpule viidud**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>KM-i aruandluse vormingu häälestamine exceli eelvaatesummade jaoks

1. Funktsioonihalduse **tööruumis** leidke ja lubage KM-aruande **vormingu aruannete** funktsioon.
2. Minge **pearaamatu** > **seadistuse** > **pearaamatu** parameetritesse.
3. Valige käibemaksu vahekaardi Maksusuvandite kiirkaardil KM-aruande vormingu vastendamise **väljal** **·** **·** **KM-i deklaratsiooni Excel** (DE).

   See vorming prinditakse **tasakaalustusperioodi käibemaksuaruande** käivitamisel. See prinditakse ka siis, kui **valite** käibemaksu **maksete lehel** valiku Prindi.

4. Maksuameti lehel valige maksuamet ja seejärel valige väljal **Aruande** **paigutus suvand** **Vaikimisi**.

Kui konfigureerite KM-i deklaratsiooni juriidilises isikus, kus on [mitu KM-i](emea-reporting-for-multiple-vat-registrations.md) registreerimist, järgige neid samme.

1. Minge **pearaamatu** > **seadistuse** > **pearaamatu** parameetritesse.
2. Valige **käibemaksudeklaratsiooni Exceli** **·** **·** **(DE) ER-vorming deu real riikide/regioonide elektroonilise aruande** kiirkaardil käibemaksu vahekaardil.

## <a name="set-up-electronic-messages"></a>Saate häälestada elektroonilisi teateid.

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Laadige alla ja importige andmepakett, mis sisaldab elektrooniliste teadete näitesätteid.

Andmepakett sisaldab elektroonilise sõnumi sätteid, mida kasutatakse KM-i deklaratsiooni loomiseks XML-vormingus ja seejärel selle eelvaadet Excelis. Saate neid sätteid laiendada või luua ise. Lisateavet selle kohta, kuidas töötada elektroonilise sõnumsidega ja luua oma sätted, vt [elektrooniline](../general-ledger/electronic-messaging.md) sõnumside.

1. Elutsükli teenustes (LCS) valige ühiskasutusega varateegis varatüübiks andmepakett ja seejärel laadige alla [Microsoft Dynamics](https://lcs.dynamics.com/v2) DE **·** **KM-i deklaratsioon EM** pakett. Allalaaditud faili nimi **on DE KM-i deklaratsiooni EM** pakett.
2. Valige Dynamics 365 Finance andmehalduse **tööruumis** käsk **Impordi**.
3. Sisestage töö nimi kiirkaardi Impordi kiirkaardi väljale **Grupi** **nimi**.
4. Valige kiirsakis **Valitud üksused** suvand **Lisa fail**.
5. Dialoogiboksis Faili lisamine veenduge, et lähteandmete vormingu välja väärtuseks on seatud Pakett, valige Üleslaadimine ja lisa ning seejärel valige varem **alla** **·** **·** **laaditud** sihtfail.
6. Valige suvand **Sule**.
7. Kui andmeüksused on tegevuspaanil üles laaditud, valige **käsk** Impordi.
8. Minge **·** > **maksupäringute ja aruannetesse** > **Elektroonilised** > **teated ning** valideerige imporditud elektroonilise teate töötlemine.

### <a name="configure-electronic-messages"></a>Elektrooniliste teadete konfigureerimine

1. Minge maksu seadistamise **elektrooniliste** > **teadete** > **·** > **asustamiskirjete** tegevustele.
2. Valige de asusta **käibemaksu tagastuskirjete rida** ja seejärel valige käsk Redigeeri **päringut**.
3. Kasutage filtrit aruandesse kaasamiseks tasakaalustusperioodide määramiseks.
4. Kui peate esitama teise deklaratsioonina aruande teiste tasakaalustusperioodide maksukannetest, looge uus tegevus Asusta **kirjed ja valige sobivad** tasakaalustusperioodid.

## <a name="preview-the-vat-declaration-in-excel"></a>KM-i deklaratsiooni eelvaade Excelis

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Käibemaksudeklaratsiooni eelvaade Excelis tasakaalustusperioodi perioodilise ülesande käibemaksuaruandest

1. Minge **·** > **tasakaalustusperioodi** > **käibemaksuaruande maksu** > **·** > **perioodiliste ülesannete** deklaratsioonidele.
2. Valige **väärtus** väljal Tasakaalustusperiood.
3. Väljal **Käibemaksu makse** versioon valige üks järgmistest väärtustest:

    - **Originaal : saate luua aruande algse käibemaksumakse või enne käibemaksumakse loomist** käibemaksukannete kohta.
    - **Parandused**: looge aruanne kõigi järgmiste perioodi käibemaksumaksete käibemaksukannete kohta.
    - **Kogusummaloend** – saate luua aruande perioodi kõigi käibemaksukannete kohta (sh algsed ja kõik parandused).

4. Valige **väljal** Alguskuupäev aruandlusperioodi alguskuupäev.
5. Valige **OK ja vaadake Exceli aruanne** üle.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Käibemaksu tasakaalustamine ja sisestamine

1. Minge **maksu** > **perioodiliste ülesannete** > **deklaratsioonidele** > **käibemaksu** > **tasakaalustamine ja sisestage** käibemaks.
2. Valige **väärtus** väljal Tasakaalustusperiood.
3. Väljal **Käibemaksu makse** versioon valige üks järgmistest väärtustest:

    - **Originaal** – saate luua tasakaalustusperioodi algse käibemaksumakse.
    - **Hiljutised parandused: looge parandus käibemaksu makse pärast algse käibemaksu makse loomist** tasakaalustusperioodiks.

4. Valige **väljal** Alguskuupäev aruandlusperioodi alguskuupäev.
5. Valige nupp **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Käibemaksumakse KM-i deklaratsiooni eelvaade Excelis

1. Minge **·** > **maksupäringute ja** > **aruannetesse** > **Käibemaksupäringud Käibemaksu maksed ning valige käibemaksu** makserida.
2. Valige **prindiaruanne** ja seejärel valige **OK**.
3. Vaadake üle Valitud käibemaksu makserea jaoks loodud Exceli fail.

    > [!NOTE]
    > Aruanne luuakse ainult käibemaksumakse valitud rea kohta. Kui soovite luua näiteks parandusdeklaratsiooni, mis sisaldab perioodi kõiki parandusi, või asendusdeklaratsiooni, mis sisaldab algandmeid ja kõiki parandusi, kasutage tasakaalustusperioodi perioodiliseks toiminguks **käibemaksuaruannet**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>KM-i deklaratsiooni loomine elektroonilistest teadetest

Kui kasutate aruande loomiseks elektroonilisi teateid, saate koguda maksuandmeid mitmelt juriidiliselt isikult. Lisateavet vt jaotisest [Mitme juriidilise isiku KM-i deklaratsiooni](#run-a-vat-declaration-for-multiple-legal-entities) käivitamine (selles teemas hiljem).

Järgmine protseduur kehtib elektroonilise sõnumitöötluse näite kohta, mille impordite LCS-i jagatud varateegist.

1. Minge **maksupäringute** > **ja aruannetesse Elektrooniliste** > **teadete** > **elektroonilised** teated.
2. Valige vasakul paanil **DE KM-i** deklaratsioon.
3. Valige **kiirkaardil** Teated **väärtus Uus ja seejärel valige dialoogiboksis Käivita töötlemine** **·** **OK**.
4. Valige teaterida, mis on loodud, sisestage kirjeldus ja seejärel määratlege deklaratsiooni algus- ja lõppkuupäevad.

    > [!NOTE]
    > Sammud 5 kuni 7 on valikulised.

5. Valikuline: valige **kiirkaardil** Teated suvand **Andmete** kogumine ja seejärel valige **OK**. Varem loodud käibemaksu maksed lisatakse teatele. Lisateabe saamiseks vt selles [teemas varasemat jaotist Käibemaksu](#settle-and-post-sales-tax) tasakaalustamine ja postitamine. Kui selle sammu vahelejätte, saate siiski luua KM-i deklaratsiooni, kasutades dialoogiboksi Deklaratsioon **välja** **Maksudeklaratsiooni** versioon.
6. Valikuline: **kiirkaardil** Teateüksused vaadake üle töödeldavad käibemaksumaksed. Vaikimisi kaasatakse kõik valitud perioodi käibemaksu maksed, mida ei kaasatud muusse sama töötlemise teatesse.
7. Valikuline: **valige käibemaksu maksete ülevaatamiseks algdokument või valige käsk** **Kustuta, et käibemaksu maksed** töötlemisest välja jätta. Kui selle sammu vahelejätte, saate siiski luua KM-i deklaratsiooni, kasutades dialoogiboksi Deklaratsioon **välja** **Maksudeklaratsiooni** versioon.
8. Valige **kiirkaardil** Teated olek **Uuenda**. Valige dialoogiboksis **Oleku** värskendamine suvand **Loomiseks valmis ja seejärel valige** **OK**. Kontrollige, kas teate olekuks on määratud **"Loomiseks** valmis".
9. Valige **käsk Loo** aruanne. KM-i deklaratsiooni summade eelvaateks valige **dialoogiboksis Käivita töötlemine suvand Aruande eelvaade ja seejärel valige** **·** **OK**.
10. **Dialoogiaknas Elektroonilise aruandluse** parameetrid seadke järgmised väljad ja seejärel valige **OK**.

    | **Field**                                   | **Kirjeldus**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Tasakaalustusperiood                           | Valige tasakaalustusperiood. Kui valisite **sammus** 5 valiku Andmete kogumine, võite selle välja tühjaks jätta. Aruanne luuakse käibemaksukannete kohta, mis sisalduvad kogutud käibemaksu maksetes. |
    | Maksudeklaratsiooni versioon                     | Valige üks järgmistest väärtustest.</br>-   **Originaal – saate luua aruande algse käibemaksumakse või enne käibemaksumakse loomist** käibemaksukannete kohta.</br>-   **Parandused** – saate luua aruande kõigi järgmiste perioodi käibemaksumaksete käibemaksukannetest.</br>-   **Kogusummade** loend – saate luua aruande perioodi kõigi käibemaksukannete kohta, sh algsed ja kõik parandused.|
    | Maksuesindaja | Valige osapool, kes on KM-i deklaratsiooni maksuesindaja, kui see on olemas. Valitud osapoole teave eksporditakse **DatenLieferant** XML-elementi. |
    | Kontaktisik | Valige isik organisatsioonis, kes on andmetarnija. Teave valitud isiku kohta eksporditakse **DatenLieferant** XML-elementi. |
    | Parandav tagastus | Valige **Jah**, kui see on korrigeeriv KM-i deklaratsioon. Sel juhul on XML-elemendi KZ10 väärtus **1**.|
    | Toetavad dokumendid | Kui **saadate** ka toetavad dokumendid, valige Jah. Sel juhul on XML-elemendi KZ22 väärtus **1**.|
    | SEPA otsekorralduskäsk tühistatakse erandina| Valige **Jah**, kui SEPA otsekorralduse luba tühistatakse selle eelregistreerimisperioodi erandina. Näiteks taotluste lähtestamise tõttu. Kõik järelejäänud saldod tuleb tasuda eraldi. Sel juhul on XML-elemendi KZ26 väärtus **1**. |
    | Soovitud väljamaksesumma lähtestamine | Valige **Jah**, kui soovitud korvamissummat lähtestatakse või kui korvamissumma on määratud. Sel juhul on XML-elemendi KZ29 väärtus **1**. |
    | Ettemakse eri püsilaiend | Sisestage fikseeritud erimakse mahaarvatatav summa jäädav laienduse puhul. See mahaarvamissumma lõpetatakse tavaliselt ainult maksuperioodi viimases eelregistreerimises. Summa eksporditakse käibemaksudeklaratsiooni real 67 (ruut 39) ja XML-elemendis KZ39. |

11. Valige **manused** lehekülje ülemises parempoolses nurgas ja seejärel valige **Ava**.
12. Vaadake summad Exceli dokumendis üle ja valige käsk **Loo** aruanne.
13. KM-i deklaratsiooni XML-vormingus loomiseks valige dialoogiaknas Käivita töötlemine suvand **Loo aruanne ja seejärel valige** **·** **OK**.
14. Seadke elektroonilise **aruandluse parameetrite dialoogiboksis** väljad nii, nagu on kirjeldatud sammus 10.
15. Valige **lehekülje** ülemises parempoolses nurgas manused, laadige fail alla ja kasutage seda maksuametile esitamiseks.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a> Mitme juriidilise isiku KM-i deklaratsiooni käitamine

Vormingute kasutamiseks KM-i deklaratsiooni esitamiseks juriidiliste isikute grupile peate esmalt seadistama kõigi nõutavate juriidiliste isikute käibemaksukoodide ER-vormingute rakenduspõhised parameetrid.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Saate häälestada elektroonilisi teateid mitmelt juriidiliselt isikult maksuandmete kogumiseks.

Järgige neid samme, et seadistada elektroonilised teated, mis koguvad andmeid mitmelt juriidiliselt isikult.

1. Avage **tööruumide** > **funktsioonihaldus**.
2. Otsige ja valige **loendist asustatud kirjete tegevuste funktsiooni jaoks** ettevõtetevahelised päringud ja seejärel valige **luba kohe**.
3. Minge maksu seadistamise **elektrooniliste** > **teadete** > **\> asustamiskirjete tegevustele**.
4. Valige **tegevuslehel** Asusta kirjed rida **DE Asusta KM-i tagastuskirjete** jaoks.

   Andmeallikate **häälestuse** ruudustikus **on saadaval uus ettevõtte** väli. Olemasolevate kirjete puhul näitab see väli praeguse juriidilise isiku ID-d.

5. Lisage **andmeallikate** häälestusruudustikus rida iga täiendava juriidilise isiku jaoks, kes tuleb aruandlusse kaasata. Seadke iga uue rea jaoks järgmised väljad.

    | Field                  | Kirjeldus                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nimi                   | Sisestage väärtus, mis aitab teil mõista, kust see kirje pärineb. Näiteks sisestage **allkonto 1** KM-makse. |
    | Sõnumiüksuse tüüp      | Valige **KM-i** tagastus. See väärtus on ainus väärtus, mis on kättesaadav kõigile kirjetele.                                    |
    | Konto tüüp           | Valige **kõik**.                                                                                                               |
    | Peatabeli nimi      | Määrake **kõigi kirjete jaoks TaxReportVoucher.**                                                                             |
    | Dokumendi numbriväli  | Määrake **kõigi kirjete jaoks** kanne.                                                                                      |
    | Dokumendi kuupäevaväli    | Määrake **transDate** kõigile kirjetele.                                                                                    |
    | Dokumendi kontoväli | Määrake **kõigi kirjete jaoks TaxPeriod.**                                                                                    |
    | Ettevõte                | Valige juriidilise isiku ID.                                                                                            |
    | Kasutaja päring             | See ruut valitakse kriteeriumide määratlemisel automaatselt, valides käsu **Redigeeri** päringut.                                 |

6. Iga uue rea jaoks valige käsk Redigeeri päringut ja määrake rea väljal Ettevõte määratud **juriidilise** **isikuga** seotud tasakaalustusperiood.

Kui seadistus on lõpule viidud, kogub elektrooniliste teadete lehel andmete kogumise funktsioon käibemaksu makseid kõigilt **teie** määratud **juriidilistelt** isikutelt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
