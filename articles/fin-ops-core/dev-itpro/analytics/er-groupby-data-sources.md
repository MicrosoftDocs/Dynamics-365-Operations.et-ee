---
title: Kirjete ja koondarvutuste rühmitamine GROUPBY andmeallikate abil
description: Selles teemas selgitatakse, kuidas saate GROUPBY tüüpi andmeallikaid kasutada elektroonilises aruandluses (ER).
author: NickSelin
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a6cdc486c5f799bdedafa38e90be989fd328c96
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075744"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Kirjete ja koondarvutuste rühmitamine GROUPBY andmeallikate abil

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Elektroonilise aruandluse (ER) mudelivastenduste või vormingute konfigureerimisel [saate](general-electronic-reporting.md) lisada [GroupBy](#AddMmDataSource2) tüüpi nõutavaid andmeallikaid **.**

Kujundusajal **on GroupBy** andmeallikas konfigureeritud tuvastama järgmisi elemente.

- Baas [andmeallikas](#BaseDataSource), mis sisaldab kirjeid, mis rühmitatakse käitusajal
- [Põhi andmeallika rühmitamisväljad](#GroupingFields), mida kasutatakse käitusajal kirje grupeerimiseks
- [Liitfunktsioonid](#AggregateFunctions), mis määravad koondarvutused, mis tehakse iga avastatud rühma kohta käitusajal

Käitusajal rühmitab konfigureeritud GroupBy **andmeallikakirjed kirjed**, millel on rühmitamisväljadel samad väärtused, ja tagastab seejärel kirjete loendi. Iga kirje tähistab ühte rühma. Andmeallikas paljastab iga rühma jaoks väljaväärtused, mille alusel algsed kirjed rühmitati, arvutatud koondfunktsioonide väärtused ja rühma kuuluva baas andmeallika kirjete loendi.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Liitfunktsioonid

Käitusajal tehakse iga kirjerühma kohta iga koondarvutus. Selle arvutamiseks kasutatakse ühe välja väärtust või avaldist andmeallika kirjetes, mis valiti groupBy **tüübi redigeeritava andmeallika** rühmitamiseks. Praegu toetatakse järgmisi koondfunktsioone.

- **AVG** – see funktsioon tagastab rühma väärtuste keskmise. Seda saab kasutada ainult numbriliste väljadega.
- **COUNT** – see funktsioon tagastab rühmast leitud kaupade arvu.
- **Min** – see funktsioon tagastab rühma väärtuste miinimumväärtuse.
- **Max** – see funktsioon tagastab rühma väärtuste maksimaalse väärtuse.
- **SUM** – see funktsioon tagastab kõigi grupi väärtuste summa. Seda saab kasutada ainult numbriliste väljadega.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Täitmise asukoht

Kui redigeerite GroupBy andmeallikat **ja määrate põhi andmeallika, mis sisaldab rühmitada vajavaid kirjeid, tuvastab süsteem automaatselt selle GroupBy** andmeallika käivitamiseks [kõige tõhusama](#ExecutionLocation) asukoha **.** Kui baasandmeallikas on [päritav](er-functions-list-filter.md#usage-notes) (st kui seda saab käitada andmebaasi tasemel), määratakse rakenduse andmebaas ka redigeeritava GroupBy **andmeallika täitmiskohaks**. Vastasel juhul määratakse rakenduseserveri mälu täitmiskohaks.

Automaatselt tuvastatud täitmiskoha käsitsi muutmiseks valige konfigureeritud andmeallikale rakendatav asukoht. Kui valitud täitmiskohale ei rakendata, [visatakse kinnitamise tõrge](er-components-inspections.md#i5) kujundusajal.

> [!TIP]
> Soovitame kasutada andmebaasi asukohta, et rühmitada andmeallikad, mis paljastavad suure hulga kirjeid.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Mälu tarbimine

Vaikimisi, kui GroupBy **andmeallikat** käitatakse mälus, kasutatakse rakendusserveri mälu igasse avastatud rühma kuuluva baasandmeallika kirjete salvestamiseks ühe rühma kirjetena. Mälutarbimise vähendamiseks saate GroupBy **andmeallikate** kirjesalvestusruumi alla suruda, kui need on konfigureeritud arvutama ainult liitfunktsioone ja nende rühma kirjeid ei kasutata käitusajal. Mälu tarbimise vähendamiseks lubage **ER-i mälukasutuse vähendamine, kui kirjete rühmitamist kasutatakse ainult funktsioonide halduse** tööruumis agregatsioonide **arvutamiseks**.

## <a name="alternatives"></a><a name="Alternatives"></a> Alternatiive

Sarnaseid liitmisi saab arvutada erinevat [tüüpi andmeallikate või ER-i sisseehitatud funktsioonide abil](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions).

Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Näide: GROUPBY andmeallika kasutamine koondarvutusteks ja kirje grupeerimiseks

Selles näites kirjeldatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsionaalse konsultandi rolli kasutaja saab konfigureerida ER-mudeli vastenduse, millel on **GROUPBY** andmeallikas, mida kasutatakse koondfunktsioonide ja rühmakirjete arvutamiseks. Seda mudelivastendust kasutatakse juhtelemendi aruande printimiseks Intrastati deklaratsiooni loomisel. See aruanne võimaldab teil teatatud Intrastati kanded üle vaadata.

Selle näite protseduurid saab lõpule viia **Microsofti** DEMF-ettevõttes Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Näidisandmete ettevalmistamine

Veenduge, et teil oleks Intrastati lehel aruandluse jaoks Intrastati **kanded**. Teil peavad olema erinevate transporditähiste kanded, sest rühmitate selles näites kanded välja Transport **järgi**.

![Intrastati kannete ettevalmistamine lehel Intrastat.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-i mudelivastenduse kujundamist peate selle seadistuse lõpule viima.

### <a name="import-the-standard-er-format-configuration"></a>Standardse ER‑vormingu konfiguratsiooni importimine

Praegusele eksemplarile [standardse ER-vormingu konfiguratsiooni lisamiseks](er-quick-start2-customize-report.md#ImportERSolution1) järgige standardse ER-vormingu konfiguratsiooni Dynamics 365 Finance samme. Importige intrastati **mudeli** konfiguratsiooni versioon 1 hoidlast.

### <a name="create-a-custom-data-model-configuration"></a>Kohandatud andmemudeli konfiguratsiooni loomine

Järgige juhiseid [Lisage kohandatud andmemudeli konfiguratsioon](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) uue käsitsi lisamiseks **Intrastati mudel (Litware)** ER andmemudeli konfiguratsioon, mille tulete imporditud andmetest **Intrastati mudel** konfiguratsiooni.

### <a name="configure-a-custom-data-model-component"></a>Kohandatud andmemudeli komponendi konfigureerimine

Järgige neid samme, et teha tuletis vajalikke muudatusi **Intrastati mudel (Litware)** andmemudel, et seda saaks kasutada vajalike üksikasjadega transpordikoodide avaldamiseks.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. peal **Konfiguratsioonid** lehel, valige konfiguratsioonipuust **Intrastati mudel (Litware)**.
3. Valige **Kujundaja**.
4. peal **Andmemudeli kujundaja** lehel mudelipuust valige **Intrastat**.
5. Valige **Uus** uue pesastatud sõlme lisamiseks valitud jaoks **Intrastat** sõlm. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Aastal **Nimi** väljale, sisestage **Transport**.
    2. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
    3. Uue sõlme lisamiseks valige **Lisa**.

6. Valige **Uus** uue pesastatud sõlme lisamiseks **Transport** sõlm, mille just lisasite. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Aastal **Nimi** väljale, sisestage **Kood**.
    2. Valige väljalt **Üksuse tüüp** suvand **String**.
    3. Uue sõlme lisamiseks valige **Lisa**.

7. Valige **Uus** teise uue pesastatud sõlme lisamiseks **Transport** sõlm. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Aastal **Nimi** väljale, sisestage **TotalInvoicedAmount**.
    2. Väljal **Üksuse tüüp** valige **Tegelik**.
    3. Uue sõlme lisamiseks valige **Lisa**.

8. Valige **Uus** teise uue pesastatud sõlme lisamiseks **Transport** sõlm. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Aastal **Nimi** väljale, sisestage **Tehingute arv**.
    2. Valige väljalt **Kauba tüüp** suvand **Integer**.
    3. Uue sõlme lisamiseks valige **Lisa**.

9. Valige **Uus** teise uue pesastatud sõlme lisamiseks **Transport** sõlm. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Aastal **Nimi** väljale, sisestage **Tehing**.
    2. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
    3. Uue sõlme lisamiseks valige **Lisa**.

10. Selle eest **Tehing** sõlm, mille just lisasite **Sõlm** FastTab, valige **Vahetage üksuse viidet**.
11. Aastal **Vahetage üksuse viidet** dialoogiboksis andmemudeli puus valige **CommodityRecord**. Seejärel valige **OK**.

![Konfigureeritud andmemudel ER-i andmemudeli kujundajas.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Viige kohandatud andmemudeli kujundamine lõpule

Järgige juhiseid [Viige andmemudeli kujundamine lõpule](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) tuletatud kujunduse lõpuleviimiseks **Intrastati mudel (Litware)** andmemudel.

### <a name="create-a-new-model-mapping-configuration"></a>Uue mudelivastenduse konfiguratsiooni loomine

Järgige juhiseid [Looge uus mudeli vastendamise konfiguratsioon](er-quick-start1-new-solution.md#CreateModelMapping) uue käsitsi lisamiseks **Intrastati näidiskaardistamine** ER mudeli vastendamise konfiguratsioon tuletatud mudeli jaoks **Intrastati mudel (Litware)** konfiguratsiooni.

### <a name="add-a-new-model-mapping-component"></a>Lisage uus mudeli vastendamise komponent

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. peal **Konfiguratsioonid** lehel konfiguratsioonipuus laiendage **Intrastati mudel** konfiguratsiooni.
3. Valige **Intrastati näidiskaardistamine** konfiguratsiooni.
4. Valige **Kujundaja**, et avada vastenduste loend.
5. Valige **Kustuta** olemasoleva kaardistamiskomponendi eemaldamiseks.
6. Valige **Uus** uue kaardistamiskomponendi lisamiseks.
7. Aastal **Definitsioon** väli, valige **Intrastat**.
8. Aastal **Nimi** väljale, sisestage **Intrastati kaardistamine**.
9. Valige **Disainer** uue kaardistuse konfigureerimiseks.

### <a name="design-the-added-model-mapping-component"></a>Kujundage lisatud mudeli kaardistamise komponent

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Rakenduste tabelile juurdepääsuks lisage andmeallikas

Konfigureerige andmeallikas, et pääseda juurde rakendusetabelitele, mis sisaldavad Intrastati tehingute üksikasju.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.
2. Aastal **Andmeallikad** paneel, valige **Lisa juur** et lisada uus andmeallikas, mida kasutatakse juurdepääsuks **Intrastat** laud. Iga rekord **Intrastat** tabel esindab ühte Intrastati tehingut.
3. Aastal **Andmeallika omadused** dialoogiboksis **Nimi** väljale, sisestage **Tehing**.
4. Aastal **Tabel** väljale, sisestage **Intrastat**.
5. Uue andmeallika lisamiseks valige **OK**.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Lisage Intrastati tehingute rühma andmeallikas

Seadistage a **GroupBy** andmeallikas Intrastati tehingute rühmitamiseks ja koondfunktsioonide arvutamiseks.

1. peal **Mudeli kaardistamise disainer** lehel **Andmeallika tüübid** paneel, valige **Funktsioonid\\ Grupeeri**.
2. Aastal **Andmeallikad** paneel, valige **Lisa juur** uue andmeallika lisamiseks, mida kasutatakse Intrastati tehingute rühmitamiseks ja koondfunktsioonide arvutamiseks.
3. Aastal **Andmeallika omadused** dialoogiboksis **Nimi** väljale, sisestage **TransportRecord**.
4. Valige **Grupi muutmise alus** grupeerimistingimuste seadistamiseks.
5. peal **Redigeerige parameetreid "Rühmita".** lehe andmeallikate loendis parempoolsel paanil valige **Tehing** andmeallikas ja laiendage seda.
6. Valige **Lisa väli \> Mida rühmitada** näitamaks, et **Tehing** andmeallikaks on valitud <a name="BaseDataSource">baasandmete allikas</a> konfigureeritud jaoks **GroupBy** andmeallikas. Kirjed **Tehing** andmeallikas rühmitatakse ja selle andmeallika väljaväärtusi kasutatakse koondfunktsioonide arvutuste tegemiseks.
7. Valige **Tehing\Transport** välja ja seejärel valige **Lisa väli \> Grupeeritud väli** näitamaks, et **Transport** baasandmeallika väli on valitud kui <a name="GroupingFields">rühmitamise kriteerium</a> konfigureeritud jaoks **GroupBy** andmeallikas. Teisisõnu, dokumendid **Tehing** andmeallikas rühmitatakse väärtuse alusel **Transport** valdkonnas. Iga konfigureeritud kirje **GroupBy** andmeallikas esindab ühte transpordikoodi, mis on leitud baasandmeallika kirjetest.
8. Valige **Tehing\SummaMST** väljal ja seejärel järgige neid samme:

    1. Valige **Lisa väli \> Koondväljad** näitamaks, et an<a name="AggregateFunctions">koondfunktsioon</a> arvutatakse selle välja jaoks.
    2. Aastal **Agregatsioonid** paanil kirjes, mis on valitud jaoks lisatud **Tehing\SummaMST** väljal **meetod** väljal valige **Summa** funktsiooni.
    3. Aastal **Nimi** valikuline väli, sisestage **TotalInvoicedAmount**.

    Need sätted määravad, et iga transpordirühma jaoks on kogusumma **Tehing\SummaMST** välja arvutatakse.

9. Valige **Tehing\RecId** väljal ja seejärel järgige neid samme:

    1. Valige **Lisa väli \> Koondväljad** näitamaks, et selle välja jaoks arvutatakse koondfunktsioon.
    2. Aastal **Agregatsioonid** paanil kirjes, mis on valitud jaoks lisatud **Tehing\RecId** väljal **meetod** väljal valige **Count** funktsiooni.
    3. Aastal **Nimi** valikuline väli, sisestage **Tehingute arv**.

    Need sätted määravad, et iga transpordigrupi jaoks arvutatakse grupis olevate tehingute arv.

10. Valige käsk **Salvesta**.
11. Vaadake üle<a name="ExecutionLocation">hukkamine</a> redigeeritava andmeallika parameetrid. Märka seda **Automaatne tuvastus** on automaatselt valitud **Täitmise koht** väli ja **Täitmine kl** väli sisaldab väärtust **SQL**. Need sätted määravad, et valitud **Tehing** baasandmeallikas on praegu päringutega ja saate redigeeritava käivitada **GroupBy** andmeallikas andmebaasi tasemel.
12. Avage päring **Täitmise koht** väljale, et vaadata üle saadaolevate väärtuste loend. Pange tähele, et saate valida **Päring** või **Mälestuseks** seda sundida **GroupBy** andmeallikas, mida käitatakse andmebaasi tasemel või rakendusserveri mälus.
13. Valige **Salvesta** ja sulgege **Redigeerige parameetreid "Rühmita".** lehel.
14. Valige **Okei** seadete lõpuleviimiseks **GroupBy** andmeallikas.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> Siduge GroupBy andmeallikas andmemudeli väljadega

Siduge konfigureeritud andmeallikas andmemudeli väljadega, et määrata, kuidas andmemudel täitmise ajal rakenduse andmetega täidetakse.

1. peal **Mudeli kaardistamise disainer** lehel **Andmemudel** paani laiendage **Transport** sõlm.
2. Aastal **Andmeallikad** paani laiendage **TransportRecord** andmeallikas.
3. Avastatud transpordirühmade loendi kuvamiseks lisage sidumine:

    1. Aastal **Andmemudel** paan, valige **Transport** üksus.
    2. Aastal **Andmeallikad** paan, valige **TransportRecord** andmeallikas.
    3. Valige **Seo**.

4. Lisage sidumine, et paljastada iga avastatud transpordirühma transpordikood:

    1. Valige **Transport.Kood** andmemudeli üksus.
    2. Valige **TransportRecord.grouped.TransportMode** rühmitatud väli.
    3. Valige **Seo**.

5. Lisage sidumine, et paljastada iga avastatud transpordirühma arvutatud koondfunktsioonide väärtused:

    1. Valige **Transport.Tehingute arv** andmemudeli üksus.
    2. Valige **TransportRecord.agregated.NumberOfTransactions** koondatud väli.
    3. Valige **Seo**.
    4. Valige **Transport.TotalInvoicedAmount** andmemudeli üksus.
    5. Valige **TransportRecord.aggregated.TotalInvoicedAmount** koondatud väli.
    6. Valige **Seo**.

6. Lisage igasse avastatud transpordirühma kuuluvate tehingukirjete paljastamiseks sidumine:

    1. Valige **Transport.Tehing** andmemudeli üksus.
    2. Valige **TransportRecord.lines** valdkonnas.
    3. Valige **Seo**.

    Saate jätkata pesastatud üksuste sidumiste konfigureerimist **Transport.Tehing** andmemudeli üksus ja **TransportRecord.lines** andmeallika väli, et kuvada käitusajal iga avastatud transpordirühma kuuluvate Intrastati tehingute üksikasjad.

![Konfigureeritud mudelivastendus ER-i mudelivastenduse kujundajas.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Siluge lisatud mudeli vastendamise komponent

Kasuta [ER andmeallika silur](er-debug-data-sources.md) konfigureeritud mudeli vastenduse testimiseks.

1. peal **Mudeli kaardistamise disainer** leht, valige **Alustage silumist**.
2. peal **Andmeallikate silumine** lehel valige vasakpoolsel paanil **TransportRecord** andmeallikas ja seejärel valige **Lugege kõiki kirjeid**.
3. Laiendage **TransportRecord** andmeallikas ja seejärel järgige neid samme.

    1. Valige **TransportRecord.grouped.TransportMode** andmeallikas.
    2. Valige **Too väärtus**.
    3. Valige **TransportRecord.grouped.NumberOfTransactions** andmeallikas.
    4. Valige **Too väärtus**.
    5. Valige **TransportRecord.grouped.TotalInvoicedAmount** andmeallikas.
    6. Valige **Too väärtus**.

4. Paremal paanil valige **Laienda kõik**.

The **TransportRecord** andmeallikas paljastab kaks kirjet ja esitab kaks transpordikoodi. Iga transpordikoodi kohta arvutatakse tehingute arv ja arveldatud kogusumma.

> [!NOTE]
> "Laisa lugemise" lähenemist kasutatakse siis, kui a **GroupBy** andmeallikat kutsutakse andmebaasikõnede optimeerimiseks. Seetõttu on mõned välja väärtused a **GroupBy** andmeallikas arvutatakse ER andmeallika siluris ainult siis, kui need on seotud andmemudeli väljadega.

![Andmeallika silumise tulemused lehel Andmeallikate silumine.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Kas grupi kogusummade arvutamisel on võimalik kuidagi üldsummasid arvutada?

Jah. Üldsummade arvutamiseks konfigureerige teine **GroupBy** andmeallikas, kus **GroupBy** baasandmeallikana kasutatakse varem konfigureeritud andmeallikat. Järgmisel joonisel on kujutatud **Kokkuvõtted** andmeallikas **GroupBy** tüüp, mida kasutatakse agregaadi arvutamiseks **SUMMA** funktsioon, mis põhineb **SUMMA** koondamine **TransportRecord** andmeallikas **GroupBy** tüüp.

![Summeerib andmeallika ER mudeli kaardistamise kujundajas.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Järgmisel illustratsioonil on näidatud tulemused **Kokkuvõtted** andmeallika silumine.

![Andmeallikate silumise tulemused lehel Andmeallikate silumine.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks](er-debug-data-sources.md)
- [Kasuta elektroonilise aruandluse vormingutes ANDMEKOGUMI andmeallikaid](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
