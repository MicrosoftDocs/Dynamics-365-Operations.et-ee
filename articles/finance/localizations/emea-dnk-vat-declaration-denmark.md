---
title: KM-deklaratsioon (Taani)
description: See artikkel kirjeldab, kuidas seadistada ja luua Taani jaoks ettemakse käibemaksu (VAT).
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: a47b2b98d86daf50876c783f879362ec1addb579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272136"
---
# <a name="vat-declaration-denmark"></a>KM-deklaratsioon (Taani)

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada Taani käibemaksudeklaratsiooni (VAT) ja selle eelvaadet jaotises Microsoft Excel.

Aruande automaatseks loomiseks looge esmalt piisavalt käibemaksukoode, et säilitada iga boksi jaoks eraldi KM-i arvestuse deklaratsioon. Lisaks seostage käibemaksukoodid elektroonilise aruandluse (ER) rakendusspetsiifilistes parameetrites käibemaksukoodide otsingutulemusega km-deklaratsiooni väljade otsingutulemusega.

Taani puhul peate konfigureerima **aruandevälja otsingu**. Rakendusespetsiifiliste parameetrite kohta lisateabe saamiseks vt selles artiklis [jaotist](#set-up-application-specific-parameters) KM-i deklaratsiooni väljade rakendusespetsiifiliste parameetrite seadistamine.

Järgmises tabelis kuvatakse veerus "Otsingu tulemus" otsingutulemus, mis on eelkonfigureeritud kindla KM-i deklaratsiooni reale KM-deklaratsiooni vormingus. Kasutage seda teavet käibemaksukoodide õigeks seostamiseks otsingutulemusega ja seejärel KM-i deklaratsiooni reaga.

### <a name="vat-declaration-overview"></a>KM-i deklaratsiooni ülevaade

Taani KM-i deklaratsioon sisaldab järgmist teavet.

**VAT tasumine**

| Kirjeldus                                                  | Maksu alus/maksusumma | Otsingutulemus/kogusumma                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arvestatud käibemaks                                                   | Maksusumma          | **OutputVAT**</br> **DomesticVATUseTax** (esitatakse ka boksis Sisendkäibemaksud)                                                                                                                                                                                                                                                                       |
| KAUPADE KM jne. Ostetud välismaalt                           | Maksusumma          | **OstugoodsA välismaa**</br>**PurchaseGoodsAbroadUseTax** (esitatud ka väljal Sisendkäibemaks)</br>**PurchaseGoodsEU** (maksubaasi esitatakse kastis A – kaupade soetamine.)</br>**PurchaseGoodsEUUseTax** (maksusumma esitatakse ka väljal SisendKÄIBEMAKS. Maksubaasi saate esitada kastis A – kaupade soetamine.)                   |
| Välismaal ostetud pöördmaksustatavate teenuste käibemaks | Maksusumma          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (esitatud ka väljal Sisendkäibemaks)</br>**PurchaseServicesEU** (maksubaas on esitatud kastis A – teenuste soetamine.)</br>**PurchaseServicesEUUseTax** (maksusumma esitatakse ka väljal Sisendkäibemaks. Maksubaasi saate esitada väljal "Kast A – teenuste soetamine.) |
| Tasumisele kuuluv kogusumma                                                | Maksusumma          | Eelmise kolme välja kogusumma                                                                                                                                                                                                                                                                                                            |

**Mahaarvamised**

| Kirjeldus                                                                               | Maksu alus/maksusumma | Otsingutulemus/kogusumma                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sisendkäibemaks                                                                                 | Maksusumma          | **InputVAT**</br> **DomesticVATUseTax** (esitatakse ka väljal Toodangu KM)</br>**PurchaseGoodsAbroadUseTax** (esitatud ka jaotises Kaupade käibemaks jne). Ostetud välismaine ruut)</br>**PurchaseServicesAbroadUseTax** (esitatud ka väljal "Välismaal ostetud teenuste KM, mille suhtes kehtib pöördtasu")</br>**PurchaseGoodsEUUseTax** (esitatud ka jaotises Kaupade KÄIBEMAKS jne). Ostetud välismaine ruut)</br> **PurchaseServicesEUUseTax** (esitatud ka väljal "Välismaal ostetud teenuste KM, mille suhtes kehtib pöördtasu") |
| Õli ja balloongaasi maks                                                                  | Maksusumma          | **ÕligagasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Maagaasi ja majapidamisgaasi maks                                                             | Maksusumma          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Süsinikumaks                                                                               | Maksusumma          | **Kadakast**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Co2Duty                                                                                   | Maksusumma          | **Co2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Veetasu                                                                              | Maksusumma          | **Vesitasu**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Mahaarvamiste koguarv                                                                          | Maksusumma          | Eelmise kuue välja kogusumma                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Kohustuste kogusumma (positiivne summa = tasuda, negatiivne summa = saada tagasimakse) | Maksusumma          | Tasumisele kuuluv kogusumma – "Mahaarvamised kokku"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Lisateave**

| Kirjeldus                                                                                                                                                                                                                                | Maksu alus/maksusumma | Otsingutulemus/kogusumma                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Kast A - kaupade soetamine. El-sisese kaupade soetamise väärtus ilma käibemaksuta.                                                                                                                                                   | Maksualus            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Kast A - teenuste soetamine. Euroopa Liidu sisese teenuste soetamise väärtus ilma käibemaksuta.                                                                                                                                             | Maksualus            | **OstuteenusedEU PurchaseServicesEUUseTax** |
| Kast B – kaupade tarned, mis tuleb esitada deklaratsioonile "EL-müük KM-ta" / DK VIES. Euroopa Liidu sisese kaupade tarne väärtus ilma KÄIBEMAKSUta                                                                                                           | Maksualus            | **SalesGoodsEU**                                |
| Kast B – tarned – ei tule esitada aruandele "EL-müük KM-ta" / DK VIES. Euroopa Liidu siseste tarnete (nt installatsiooni, assembleri, kaugmüügi ja uute transpordivahendite) väärtus käibemaksuta mittemaksustavatele isikutele. | Maksualus            | **SalesInstallationAssemblyEeu**              |
| Kast B – teenuste tarne. Euroopa Liidu sisese teenusetarne väärtus, mille eest ostja on kohustatud käibemaksu pöördtasuna maksma, tuleb esitada ka "EL-müük KM-ta" / DK VIES.                          | Maksualus            | **SalesServicesEU**                             |
| Box C – muud varud. Muude kaupade ja teenuste tarne väärtus, mida tarnitakse KM-ta Taani, teiste EL-i liikmesriikide ja kolmandate riikide või kolmandate piirkondade vahel.                                     | Maksualus            | **MuudSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Ostu pöördtasu KM

Kui konfigureerite käibemaksukoode sissetuleva pöördtasu KM-i sisestamiseks kasutusmaksu abil, **seostage** oma käibemaksukoodid otsingutulemusega aruandevälja otsingust, mis sisaldab nimes "UseTax".

Teise võimalusena saate konfigureerida kaks eraldi käibemaksukoodi: üks käibemaksule ja teine käibemaksu mahaarvamiseks. Seejärel seostage iga kood aruandevälja otsingu vastavate **otsingutulemustega**.

Näiteks saate **maksustatavate kogukonnasiseste soetamiste puhul konfigureerida käibemaksukoodi UT_S_EU kasutusmaksuga** **ja seostada selle OstugoodsEUUseTax** **otsingutulemusega aruandeväljalt**. Sel juhul kajastuvad käibemaksukoodi **UT_S_EU** kasutavad maksusummad kaupade käibemaksus jne. Ostetud välismaisest kaubast" ja väljadele "Sisendkäibemaks". Maksubaasid kajastuvad "Box A - kaupade soetamine."

Teise võimalusena konfigureerite kaks käibemaksukoodi:

- **VAT_S_EU**, mille maksumäära väärtus on -25 protsenti
- **InVAT_S_EU**, mille maksumäära väärtus on 25 protsenti

Seejärel seostate koodid aruandevälja **otsingutulemustega** järgmisel viisil:

- Saate **VAT_S_EU** PurchaseGoodsEU **otsingutulemusega**.
- Saate **InVAT_S_EU** InputVAT-i **otsingutulemusega**.

Sel juhul kajastuvad käibemaksukoodi **VAT_S_EU** summad kaupade km-s jne. Ostetud välismaa kasti ja "Box A - kaupade soetamine." Summad, InVAT_S_EU **käibemaksukoodi** kasutatakse väljal Sisendkäibemaks.

Lisateavet pöördtasu KM-i konfigureerimise kohta vt [Pöördtasud](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Süsteemiparameetrite konfigureerimine

KM-i deklaratsiooni loomiseks peate konfigureerima KM-numbri.

1. Avage **Organisatsiooni haldus** > **Organisatsioonid** > **Juriidilised isikud**.
2. Valige juriidiline isik ja seejärel registreerimise **ID-d**.
3. Valige või looge aadress Taanis ja seejärel valige kiirkaardil **Registreerimise ID** suvand **Lisa**.
4. Väljal Registreerimise **tüüp** valige registreerimistüüp, mis on Taanile mõeldud ja mis kasutab **KM ID registreerimiskategooriat**.
5. **Väljale Registreerimisnumber** sisestage maksunumber.
6. **Sisestage** vahekaardi Üldine väljale **Jõustus** kuupäev, millal number jõustub.

Registreerimiskategooriate ja registreerimistüüpide kohta lisateabe saamiseks vt registreerimise [ID-sid](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Km-i deklaratsiooni eelvaate häälestamine Taani jaoks

### <a name="import-er-configurations"></a>Elektroonilise aruandluse konfiguratsioonide importimine

Avage elektroonilise **aruandluse tööruum** ja importige **KM-deklaratsiooni Exceli (DK)** ER-vorming.

Lisateavet leiate teemast [ER konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a> Saate häälestada KM-i deklaratsiooniväljade rakendusspetsiifilisi parameetreid.

> [!NOTE]
> Funktsiooni lubamine on soovitatav kasutada funktsioonihalduse **tööruumis ER-vormingute** eelmiste versioonide rakendusespetsiifilisi **parameetreid**. Kui see funktsioon on lubatud, muutuvad ER-vormingu varasema versiooni jaoks konfigureeritud parameetrid automaatselt sama vormingu hilisemale versioonile. Kui see funktsioon pole lubatud, peate iga vorminguversiooni jaoks rakendusepõhised parameetrid konfigureerima. Funktsiooni **Kasuta rakenduse spetsiifilisi parameetreid ER-vormingute** **eelmistest** versioonidest on saadaval funktsioonihalduse tööruumis, alustades finantsversioonist 10.0.23. Lisateavet selle kohta, kuidas seadistada iga juriidilise isiku jaoks ER-vormingu parameetreid, [vaadake juriidilise isiku ER-vormingu parameetrite seadistamine](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

KM-i deklaratsiooni automaatseks loomiseks seostage käibemaksukoodid rakenduses ja otsingutulemused ER-i konfiguratsioonis.

Järgige neid samme, et määrata, millised käibemaksukoodid loovad millised väljad KM-i deklaratsioonil.

1. Minge tööruumide elektroonilise aruandluse juurde ja **valige aruandluskonfiguratsioonid** > **·**.**·**
2. Valige KM-i **deklaratsiooni Exceli (DK)** konfiguratsioon ja seejärel valige **konfiguratsioonide rakenduse \> parameetrite seadistus**.
3. **Valige rakendusespetsiifiliste** parameetrite lehe otsingu **kiirkaardil** aruandevälja **otsing**.
4. Seadke Kiirkaardil **Tingimused** käibemaksukoodide ja aruandeväljade seostamiseks järgmised väljad.

    | Väli                  | Kirjeldus                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Otsingu tulemus          | Valige aruandevälja väärtus. Lisateavet väärtuste ja nende määramise kohta KM-i deklaratsiooni ridadele vt [selle artikli varasemast KM-i](#vat-declaration-overview) deklaratsiooni ülevaate jaotisest.                                                                                               |
    | Maksukood               | Valige käibemaksukood, mida aruandeväljaga seostada. Valitud käibemaksukoodi kasutavad sisestatud maksukanded kogutakse vastavasse deklaratsiooniboksi. Soovitame käibemaksukoodid eraldada nii, et üks käibemaksukood loob summad ainult ühes deklaratsioonikastis. |
    | Kande liigitaja | Kui olete deklaratsiooniboksi määramiseks loonud piisavalt käibemaksukoode, märkige ruut **\* Mitte tühi\***. Kui te ei loo piisavalt käibemaksukoode, nii et üks käibemaksukood loob summad ainult ühes deklaratsiooniboksis, saate seadistada kande liigitaja. Saadaval on järgmised kandeklassid:</br>-   **Osta**</br>-   **PurchaseExempt** (maksuvaba ost)</br>-   **PurchaseReverseCharge** (ostu pöördtasult saadaolev maks)</br>-   **Müük**</br>-   **SalesExempt** (maksuvaba müük)</br>-   **SalesReverseCharge** (ostu pöördtasult või müügi pöördtasult makstav maks)</br>-   **Kasutusmaks**. </br>Iga kandeklassi jaoks on saadaval ka kreeditarve klassifikaatorid. Näiteks on üks nendest klassifikaatoriist **PurchaseCreditNote** (ostu kreeditarve).</br>Looge kindlasti kaks rida iga käibemaksukoodi kohta: üks, mille kandeklassifikaatori väärtus on ja teine, mille kande klassifikaatoriks on kreeditarve väärtus. |


    > [!NOTE]
    > Saate kõik käibemaksukoodid otsingutulemustega seostada. Kui mõni käibemaksukood ei peaks km-deklaratsioonile väärtusi tekitama, seostage need muu **otsingutulemusega**.

    ![Rakendusekohaste parameetrite leht.](media/7db74920fad66a0db7fad60758698cc0.png)


5. **Muutke välja Olek** väärtuseks **Lõpetatud**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>KM-i aruandluse vormingu häälestamine exceli eelvaatesummade jaoks

1. Funktsioonihalduse **tööruumis** leidke ja valige KM-aruande **vormingu aruanded.** Funktsiooni loendis ja seejärel valige **luba kohe**.
2. Minge pearaamatu **seadistuse** > **pearaamatu** > **parameetritesse**.
3. Valige käibemaksudeklaratsiooni **Exceli** **·** **(DK)** ER-vorming vahekaardi Käibemaksu suvandid kiirkaardil KM-aruande **vormingu** vastendamise väljal.

   See vorming prinditakse tasakaalustusperioodi **käibemaksuaruande käivitamisel**. See prinditakse ka siis, kui **valite** käibemaksu maksete **lehel valiku** Prindi.

4. **Maksuameti lehel** valige maksuamet ja seejärel valige väljal **Aruande paigutus** suvand **Vaikimisi**.

Kui konfigureerite KM-i deklaratsiooni juriidilises isikus, kus on mitu [KM-i registreerimist](emea-reporting-for-multiple-vat-registrations.md), järgige neid samme.

1. Minge pearaamatu **seadistuse** \> **pearaamatu** \> **parameetritesse.**
2. Valige DNK-i **real** käibemaksudeklaratsiooni Exceli (DK) **ER-vorming riikide/** **regioonide elektroonilise aruandluse vahekaardil käibemaksu vahekaardil.** **·**

## <a name="set-up-electronic-messages"></a>Saate häälestada elektroonilisi teateid.

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Laadige alla ja importige andmepakett, mis sisaldab elektrooniliste teadete näitesätteid.

Andmepakett sisaldab elektroonilise sõnumi sätteid, mida kasutatakse KM-i deklaratsiooni eelvaateks Excelis. Saate neid sätteid laiendada või luua ise. Lisateavet selle kohta, kuidas töötada elektroonilise sõnumsidega ja luua oma sätted, vt Elektrooniline [sõnumside](../general-ledger/electronic-messaging.md).

1. Elutsükli [Microsoft Dynamics teenustes (LCS)](https://lcs.dynamics.com/v2)**ühiskasutatava** varateegis valige vara tüübiks andmepakett ja seejärel laadige **alla DK KM-i deklaratsiooni pakett**. Allalaaditud faili nimi on **DK KM-i deklaratsiooni pakett.zip**.
2. Valige finantside halduse **tööruumis** suvand **Impordi**.
3. **Sisestage** töö nimi kiirkaardi **Impordi** kiirkaardi väljale Grupi nimi.
4. Valige kiirsakis **Valitud üksused** suvand **Lisa fail**.
5. Dialoogiboksis Faili **lisamine veenduge**, **·** **et** lähteandmete vormingu väli on seatud valikule Pakett, **valige Üleslaadimine ja lisamine** ning seejärel valige varem alla laaditud sihtfail.
6. Valige suvand **Sule**.
7. Kui andmeüksused on tegevuspaanil üles laaditud, valige käsk **Impordi**.
8. Minge **maksupäringute** > **ja aruannetesse Elektroonilised** > **·** > **teated** ning valideerige imporditud elektroonilise sõnumi töötlemine (**DK KM-i deklaratsioon**).

### <a name="configure-electronic-messages"></a>Elektrooniliste teadete konfigureerimine

1. Minge maksu seadistamise **elektrooniliste** > **teadete** > **asustamiskirjete** > **tegevustele**.
2. Valige DK asusta **käibemaksu tagastuskirjete rida ja** seejärel valige käsk **Redigeeri päringut**.
3. Kasutage filtrit aruandesse kaasamiseks tasakaalustusperioodide määramiseks.
4. Kui peate esitama teise deklaratsioonina aruande teiste tasakaalustusperioodide maksukannetest, looge uus **tegevus Asusta kirjed** ja valige sobivad tasakaalustusperioodid.

## <a name="preview-the-vat-declaration-in-excel"></a>KM-i deklaratsiooni eelvaade Excelis

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a> Käibemaksudeklaratsiooni eelvaade Excelis tasakaalustusperioodi perioodilise ülesande käibemaksuaruandest

1. Minge **tasakaalustusperioodi** > **käibemaksuaruande** > **maksu** > **perioodiliste** > **ülesannete deklaratsioonidele**.
2. **Valige väärtus väljal** Tasakaalustusperiood.
3. **Väljal Käibemaksu makse versioon** valige üks järgmistest väärtustest:

    - **Originaal**: looge aruanne algse käibemaksumakse käibemaksukannete kohta või enne käibemaksu makse loomist.
    - **Parandused**: looge aruanne kõigi järgmiste perioodi käibemaksumaksete käibemaksukannete kohta.
    - **Kokkuvõtteloend**: saate luua aruande perioodi kõigi käibemaksukannete kohta, sh algsed ja kõik parandused.

4. **Valige väljal** Alguskuupäev aruandlusperioodi alguskuupäev.
5. Valige **OK** ja vaadake Exceli aruanne üle.

### <a name="settle-and-post-sales-tax"></a>Käibemaksu tasakaalustamine ja sisestamine

1. Minge maksu **perioodiliste** > **ülesannete deklaratsioonidele** > **käibemaksu** > **tasakaalustamine** > **ja sisestage käibemaks**.
2. **Valige väärtus väljal** Tasakaalustusperiood.
3. **Väljal Käibemaksu makse versioon** valige üks järgmistest väärtustest:

    - **Originaal**: looge tasakaalustusperioodile algne käibemaksumakse.
    - **Hiljutised** parandused: looge parandus käibemaksu makse pärast algse käibemaksu makse loomist tasakaalustusperioodiks.

4. **Valige väljal** Alguskuupäev aruandlusperioodi alguskuupäev.
5. Valige nupp **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Käibemaksumakse KM-i deklaratsiooni eelvaade Excelis

1. Minge **maksupäringute** > **ja aruannetesse** > **Käibemaksupäringud** > **Käibemaksu maksed** ning valige käibemaksu makserida.
2. Valige **prindiaruanne** ja seejärel valige **OK**.
3. Vaadake üle Valitud käibemaksu makserea jaoks loodud Exceli fail.

> [!NOTE]
> Aruanne luuakse ainult käibemaksumakse valitud rea kohta. Kui peate näiteks tekitama korrigeeriva deklaratsiooni, mis sisaldab perioodi kõiki parandusi, või asendusdeklaratsiooni, mis sisaldab algandmeid ja kõiki parandusi, **kasutage** tasakaalustusperioodi perioodiliseks toiminguks käibemaksuaruannet.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>KM-i deklaratsiooni loomine elektroonilistest teadetest

Kui kasutate aruande loomiseks elektroonilisi teateid, saate koguda maksuandmeid mitmelt juriidiliselt isikult. Lisateavet vt jaotisest Mitme [juriidilise isiku KM-i deklaratsiooni käivitamine](#run-vat-declaration) (selles artiklis).

Järgmine protseduur kehtib elektroonilise sõnumitöötluse näite kohta, mille importisite varem LCS-i jagatud varateegist.

1. Minge maksupäringute **ja \> aruannetesse elektrooniliste \> teadete elektroonilised \> teated**.
2. Valige vasakul paanil **DK KM-i deklaratsioon**.
3. Valige kiirkaardil **Teated** **väärtus Uus** ja seejärel valige **dialoogiboksis Käivita töötlemine** **OK**.
4. Valige teaterida, mis on loodud, sisestage kirjeldus ja seejärel määratlege deklaratsiooni algus- ja lõppkuupäevad.

   > [!NOTE]
   > Sammud 5 kuni 7 on valikulised.

5. Valikuline: valige **kiirkaardil** Teated suvand **Andmete kogumine** ja seejärel valige **OK**. Varem loodud käibemaksu maksed lisatakse teatele. Lisateabe saamiseks vt selles artiklis [varasemat jaotist Käibemaksu tasakaalustamine](#settle-and-post-sales-tax) ja postitamine. Kui selle sammu vahelejätte, saate siiski luua KM-i deklaratsiooni, **kasutades** dialoogiboksi Deklaratsioon välja Maksudeklaratsiooni **versioon**.
6. Valikuline: **kiirkaardil** Teateüksused vaadake üle töödeldavad käibemaksumaksed. Vaikimisi kaasatakse kõik valitud perioodi käibemaksu maksed, mida ei kaasatud muusse sama töötlemise teatesse.
7. Valikuline: **valige käibemaksu** maksete ülevaatamiseks algdokument või valige käsk **Kustuta**, et käibemaksu maksed töötlemisest välja jätta. Kui selle sammu vahelejätte, saate siiski luua KM-i deklaratsiooni, **kasutades** dialoogiboksi Deklaratsioon välja Maksudeklaratsiooni **versioon**.
8. Valige kiirkaardil **Teated** suvand **Uuenda olekut**. Dialoogiaknas **Oleku** värskendamine valige suvand **Loomiseks valmis ja** seejärel valige **OK**. Kontrollige, kas teate olekuks on määratud **"Loomiseks valmis"**.
9. Valige **loo aruanne**. KM-i deklaratsiooni summade eelvaateks valige **dialoogiboksis Käivita töötlemine** suvand **Aruande eelvaade** ja seejärel valige **OK**.
10. Seadke elektroonilise **aruandluse parameetrite dialoogiaknas väljad nii,**[nagu on kirjeldatud selles artikli varasemas](#preview-vat-excel) jaotises Käibemaksuaruande perioodilise ülesande käibemaksu aruande Excelis, ning seejärel valige **OK**.
11. Valige lehekülje **ülemises parempoolses** nurgas nupp Manused (paberpildi sümbol) **ja** seejärel valige faili avamiseks suvand Ava. Vaadake summad Exceli dokumendis üle.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a> Mitme juriidilise isiku KM-i deklaratsiooni käitamine

Vormingute kasutamiseks KM-i deklaratsiooni esitamiseks juriidiliste isikute grupile peate esmalt seadistama kõigi nõutavate juriidiliste isikute käibemaksukoodide ER-vormingute rakenduspõhised parameetrid.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Saate häälestada elektroonilisi teateid mitmelt juriidiliselt isikult maksuandmete kogumiseks.

Järgige neid samme, et seadistada elektroonilised teated, et koguda andmeid mitmelt juriidiliselt isikult.

1. Avage tööruumide **funktsioonihaldus** > **·**.
2. Otsige ja valige loendist **asustatud kirjete tegevuste funktsiooni jaoks** ettevõtetevahelised päringud ja seejärel valige luba **kohe**.
3. Minge maksu seadistamise **elektrooniliste** > **teadete** > **asustamiskirjete** > **tegevustele**.
4. **Valige DK asusta** km-i tagastuskirjete **rida lehel Asusta kirjed**.

   Andmeallikate **häälestuse** ruudustikus on **saadaval** uus ettevõtte väli. Olemasolevate kirjete puhul näitab see väli praeguse juriidilise isiku ID-d.

5. Lisage andmeallikate **häälestusruudustikus** rida iga täiendava juriidilise isiku jaoks, kes tuleb aruandlusse kaasata. Seadke iga uue rea jaoks järgmised väljad.

    | Väli                  | Kirjeldus                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Nimi                   | Sisestage väärtus, mis aitab teil mõista, kust see kirje pärineb. Näiteks sisestage allkonto **1 KM-makse**. |
    | Sõnumiüksuse tüüp      | Valige KM-i **tagastus**. See väärtus on ainus väärtus, mis on kättesaadav kõigile kirjetele.                                    |
    | Konto tüüp           | Valige **kõik**.                                                                                                               |
    | Peatabeli nimi      | Määrake **kõigi kirjete jaoks TaxReportVoucher**.                                                                             |
    | Dokumendi numbriväli  | Määrake **kõigi** kirjete jaoks kanne.                                                                                      |
    | Dokumendi kuupäevaväli    | Määrake **transDate** kõigile kirjetele.                                                                                    |
    | Dokumendi kontoväli | Määrake **kõigi kirjete jaoks TaxPeriod**.                                                                                    |
    | Ettevõte                | Valige juriidilise isiku ID.                                                                                            |
    | Kasutaja päring             | See ruut valitakse kriteeriumide määratlemisel automaatselt, valides käsu Redigeeri **päringut**.                                 |

6. Iga uue rea jaoks valige **käsk Redigeeri päringut** **ja määrake rea väljal Ettevõte määratud juriidilise isikuga seotud** tasakaalustusperiood.

Kui seadistus on lõpule viidud, kogub **elektrooniliste** teadete **lehel** andmete kogumise funktsioon käibemaksu makseid kõigilt teie määratud juriidilistelt isikutelt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
