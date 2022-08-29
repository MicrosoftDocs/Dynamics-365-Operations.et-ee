---
title: Grupeeri kirjed ja koonda kalkulatsioonid GROUPBY andmeallikate abil
description: See artikkel selgitab GROUPBY-tüüpi andmeallikate kasutamist elektroonilises aruandluses (ER).
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 0e520705d2441ead5a68ec3284db74999b3d90b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277568"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Grupeeri kirjed ja koonda kalkulatsioonid GROUPBY andmeallikate abil

[!include[banner](../includes/banner.md)]

Elektroonilise aruandluse [(ER)](general-electronic-reporting.md) mudeli vastenduste või vormingute konfigureerimisel saate [lisada](#AddMmDataSource2) nõutavad andmeallikad tüübiga **GroupBy**.

Kujunduse ajal konfigureeritakse **andmeallikas GroupBy**, et tuvastada järgmised elemendid:

- Alusandmeallikas [...](#BaseDataSource), mis sisaldab käitusajal grupeeritud kirjeid
- [Põhiandmeallika](#GroupingFields) grupeerimisväljad, mida kasutatakse kirjete grupeerimiseks käitusajal
- [Liitfunktsioonid](#AggregateFunctions), mis määravad agregaatarvutused, mida tehakse iga avastatu grupi jaoks käitusajal

Käitusajal konfigureeritud **GroupBy andmeallikagruppide** kirjed, mis on grupeerimisväljadel samad väärtused ja seejärel tagastab kirjete loendi. Iga kirje tähistab ühte gruppi. Iga grupi puhul näitab andmeallikas väljaväärtusi, mille alusel esialgsed kirjed grupeeriti, arvutatud agregaaside funktsioonide väärtusi ja gruppi kuuluva alusandmeallika kirjete loendit.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Agregaalifunktsioonid

Käitusajal tehakse iga kokkuvõtte arvutus iga kirjegrupi kohta. Arvutused tehakse **üksiku välja või avaldise väärtuse abil andmeallika kirjetes, mis valiti grupeerimiseks tüübiGa GroupBy redigeeritavas andmeallikas**. Praegu toetatakse järgmisi kokkuvõttefunktsioone:

- **AVG** – see funktsioon tagastab grupi väärtuste keskmise. Seda saab kasutada ainult numbriväljade puhul.
- **COUNT** – see funktsioon tagastab grupis leitud kaupade arvu.
- **Miinimum** – see funktsioon tagastab grupi väärtuste miinimumväärtuse.
- **Maksimum** – see funktsioon tagastab grupi väärtuste maksimaalse väärtuse.
- **SUM** – see funktsioon tagastab grupi kõikide väärtuste summa. Seda saab kasutada ainult numbriväljade puhul.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Täitmise asukoht

Kui redigeerite **andmeallikat GroupBy** ja määrate alusandmeallika, [...](#ExecutionLocation)**mis sisaldab rühmitatud kirjeid, tuvastab süsteem automaatselt kõige tõhusama asukoha selle GroupBy** andmeallika käivitamiseks. Kui alusandmeallikas on [küsitav](er-functions-list-filter.md#usage-notes) (st kui seda saab käivitada andmebaasi tasemel), **määratakse ka rakenduse andmebaas redigeeritava groupBy** andmeallika käivitamisasukohaks. Muul juhul määratakse käivitamisasukohaks rakendusserveri mälu.

Automaatselt tuvastatud käivitamise asukoha saate käsitsi muuta, valides asukoha, mis on rakendatav konfigureeritud andmeallikale. Kui valitud täitmisasukoht ei kehti, ilmneb [konstruktsiooni](er-components-inspections.md#i5) ajal valideerimistõrge.

> [!TIP]
> Soovitame kasutada andmebaasi asukohta suure kirjete arvuga andmeallikate grupeerimiseks.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Mälu tarbimine

Vaikimisi, kui **groupBy** andmeallikas on mälus käitatud, kasutatakse rakendusserveri mälu põhiandmeallika kirjete salvestamiseks igasse avastatud gruppi ühe grupi kirjetena. Mälutarbimise vähendamiseks saate blokeerida groupBy **andmeallikate kirjesalvestuse,** kui need on konfigureeritud arvutama ainult liidetud funktsioone ja nende grupi kirjeid käitusajal ei kasutata. Mälu tarbimise vähendamiseks sel viisil lubage mälukasutuse vähendamine ER-is, **kui kirjete grupeerimist kasutatakse ainult funktsioonihalduse tööruumis** **liitmise funktsiooni arvutamiseks**.

## <a name="alternatives"></a><a name="Alternatives"></a> Alternatiive

Sarnaseid kogumeid saab arvutada erinevat [tüüpi](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) andmeallikate või ER-i sisseehitatud funktsioonide abil.

Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Näide: groupBY andmeallika kasutamine koondarvutuste ja kirjete grupeerimise jaoks

See näide näitab, kuidas kasutaja süsteemiadministraatoris või elektroonilise aruandluse funktsiooninõustaja rollis saab konfigureerida ER-mudeli **vastendamist, mille andmeallikal GROUPBY** on agregaatorfunktsioonid ja grupikirjed. Mudeli vastendamist kasutatakse kontrollaruande printimiseks Intrastat-deklaratsiooni loomisel. Selle aruandega saate vaadata üle teatatud Intrastati kanded.

Selle näite protseduurid saab DEMF-ettevõttes **lõpule** viia Microsoft Dynamics 365 Finantsid. 

### <a name="prepare-sample-data"></a>Näidisandmete ettevalmistamine

Kontrollige, kas Intrastat-kanded on Intrastati lehel aruandluseks **ette** kanded. Teil peavad olema kanded erinevate transpordikoodide jaoks, sest teie grupeerite kanded **selles näites** välja Transport alusel.

![Intrastati kannete ettevalmistamine Intrastati lehel.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-raamistiku kasutamist ER-mudeli vastendamise loomiseks peate selle häälestuse lõpule viima.

### <a name="import-the-standard-er-format-configuration"></a>Standardse ER‑vormingu konfiguratsiooni importimine

Järgige standardse ER-vormingu [konfiguratsiooni importimise etappe](er-quick-start2-customize-report.md#ImportERSolution1), et lisada praegusele Dynamics 365 Finance’i eksemplarile standardsed ER-konfiguratsioonid. Saate intrastati mudelikonfiguratsiooni **versiooni** 1 hoidlast importida.

### <a name="create-a-custom-data-model-configuration"></a>Kohandatud andmemudeli konfiguratsiooni loomine

Järgige kohandatud [andmemudeli](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration)**konfiguratsiooni lisamise samme, et lisada käsitsi uus Intrastat-mudeli (Litware)** ER-i andmemudeli konfiguratsioon, mille tuletate imporditud **Intrastat-mudeli konfiguratsioonist**.

### <a name="configure-a-custom-data-model-component"></a>Kohandatud andmemudeli komponendi konfigureerimine

Järgige neid samme **, et teha nõutavad muudatused tuletatud Intrastati mudelis (Litware)** andmemudelis, nii et seda saab kasutada nõutavate üksikasjadega transpordikoodide astenduseks.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Konfiguratsioonipuu **lehel** valige konfiguratsioonipuus **Intrastati mudel (Litware**).
3. Valige **Kujundaja**.
4. Valige andmemudelikujundaja **lehel** mudelipuus **Intrastat**.
5. Valige **uus**, et lisada valitud Intrastat-sõlmele **uus pesastatud** sõlm. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Väljale Nimi **sisestage** transport **·**.
    2. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
    3. Uue sõlme lisamiseks valige **Lisa**.

6. Valige **uus**, et lisada äsja lisatud transpordisõlme **jaoks** uus pesastatud sõlm. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Väljale Nimi **sisestage** **kood**.
    2. Valige väljalt **Üksuse tüüp** suvand **String**.
    3. Uue sõlme lisamiseks valige **Lisa**.

7. Transpordisõlme **jaoks** uue pesastatud sõlme lisamiseks valige **väärtus** Uus. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Sisestage **väljale Nimi** väärtus **TotalInvoicedAmount**.
    2. Väljal **Üksuse tüüp** valige **Tegelik**.
    3. Uue sõlme lisamiseks valige **Lisa**.

8. Transpordisõlme **jaoks** uue pesastatud sõlme lisamiseks valige **väärtus** Uus. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. **Väljale Nimi sisestage** NumberOfTransactions **·**.
    2. Valige väljalt **Kauba tüüp** suvand **Integer**.
    3. Uue sõlme lisamiseks valige **Lisa**.

9. Transpordisõlme **jaoks** uue pesastatud sõlme lisamiseks valige **väärtus** Uus. Järgige andmemudeli sõlme lisamise rippdialoogiboksis järgmiseid juhiseid.

    1. Väljale Nimi **sisestage** kanne **·**.
    2. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
    3. Uue sõlme lisamiseks valige **Lisa**.

10. Äsja lisatud **kandesõlme** jaoks valige sõlme **kiirkaardil** Kauba lülituse **viide**.
11. Valige andmemudelipuus **kauba** viite lülituse dialoogiaknas **suvand CommodityRecord**. Seejärel valige **OK**.

![Konfigureeritud andmemudel ER-i andmemudeli kujundajas.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Kohandatud andmemudeli kujunduse lõpule viimine

Tuletatud Intrastat-mudeli [...](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) (Litware) andmemudeli kujundamise lõpuleviimiseks järgige andmemudeli "Vii andmemudeli kujundus lõpule"**toodud etappe.**

### <a name="create-a-new-model-mapping-configuration"></a>Uue mudelivastenduse konfiguratsiooni loomine

Järgige uue mudeli [vastendamise](er-quick-start1-new-solution.md#CreateModelMapping)**konfiguratsiooni loomise samme, et lisada käsitsi uus Intrastati** näidisvastenduse ER-mudeli **vastendamise konfiguratsioon tuletatud Intrastat-mudeli (Litware) konfiguratsioonile.**

### <a name="add-a-new-model-mapping-component"></a>Uue mudeli vastendamise komponendi lisamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage **konfiguratsioonipuu** lehel Konfiguratsioonid Intrastati mudeli **konfiguratsiooni**.
3. Valige Intrastati **vastendamise näidiskonfiguratsioon**.
4. Valige **Kujundaja**, et avada vastenduste loend.
5. Olemasoleva **vastendamiskomponendi** eemaldamiseks valige käsk Kustuta.
6. Valige **uue vastendamiskomponendi** lisamiseks uus.
7. Valige intrastat **väljal** Definitsioon **·**.
8. Sisestage väljale **Nimi Intrastati** vastendamine **·**.
9. Valige **uue vastendamise** konfigureerimiseks kujundaja.

### <a name="design-the-added-model-mapping-component"></a>Lisatud mudeli vastendamise komponendi kujundamine

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Andmeallika lisamine rakenduse tabelile juurdepääsuks

Konfigureerige andmeallikas, et pääseda juurde rakenduse tabelitele, mis sisaldavad Intrastati kannete üksikasju.

1. Valige lehel **Mudelivastenduse kujundaja** paanil **Andmeallika tüübid** suvand **Dynamics 365 for Operations\\Tabeli kirjed**.
2. Valige andmeallikate paanil **suvand** Lisa **juur, et lisada uus andmeallikas, mida kasutatakse Intrastat-tabelile** **juurdepääsemiseks.** Intrastati tabeli iga **kirje** tähistab ühte Intrastati kannet.
3. Sisestage **dialoogiboksi Andmeallika** atribuudid väljale **Nimi** väärtus **Kanne**.
4. Sisestage **Intrastat** väljale **Tabel**.
5. Uue andmeallika lisamiseks valige **OK**.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Andmeallika lisamine Intrastati kannete grupeerimiseks

Saate konfigureerida andmeallika **GroupBy Intrastati** kannete grupeerimiseks ja liitfunktsioonide arvutamiseks.

1. Valige mudeli **vastendamise** kujundaja lehe paanil **Andmeallika tüübid** **suvand Funktsioonid\\grupp**.
2. Valige andmeallikate **paanil** suvand **Lisa** juur, et lisada uus andmeallikas, mida kasutatakse Intrastati kannete grupeerimiseks ja liitfunktsioonide arvutamiseks.
3. Sisestage **dialoogiboksi Andmeallika** atribuudid väljale **Nimi** väärtus **TransportRecord**.
4. Grupeerimistingimuste **konfigureerimiseks** valige käsk Redigeeri gruppi.
5. Parempoolse paani **andmeallikate loendi** **lehel** Redigeeri "Grupeerimisast" valige andmeallikas ja laiendage seda.
6. Valige **suvand Lisa väli \> Gruppi,** et **näidata**, et <a name="BaseDataSource">kande andmeallikas</a> on valitud konfigureeritud **GroupBy** andmeallika põhiandmeallikaks. Grupeeritakse **kande** andmeallika kirjed ja selle andmeallika väljaväärtusi kasutatakse agregaatfunktsioonide arvutustes.
7. Valige **Tehing\Transport** välja ja seejärel valige  **Lisa väli \> Grupeeritud väli** näitamaks, et **Transport** baasandmeallika väli on valitud kui <a name="GroupingFields">rühmitamise kriteerium</a> konfigureeritud jaoks **GroupBy** andmeallikas. See tähendab, et kande andmeallika **kirjed** grupeeritakse transpordivälja väärtuse **alusel**. Iga konfigureeritud **GroupBy andmeallika** kirje esindab ühte transpordikoodi, mis on leitud põhiandmeallika kirjetes.
8. Valige väli **Transaction\AmountMST** ja seejärel järgige neid samme:

    1. Valige **liitväljadele \> lisa väli,** mis näitab, et <a name="AggregateFunctions">selle välja</a> jaoks arvutatakse agregatfunktsioon.
    2. **Valige paani Liitmised kirjes**,**·** **mis on lisatud väljale Kanne\AmountMST** väljal Meetod, summeerimisfunktsioon.**·**
    3. Väljale Nimi **valikuline** sisestage **TotalInvoicedAmount**.

    Need sätted määravad, et arvutada arvutatakse iga transpordigrupi **välja Transaction\AmountMST** kogusumma.

9. Valige väli **Transaction\RecId** ja seejärel järgige neid samme:

    1. Valige **liitväljadele \> lisa väli,** mis näitab, et selle välja jaoks arvutatakse agregatfunktsioon.
    2. **Valige paani Liitmised kirjes** **,** mis on lisatud väljale Transaction\RecId **väljal Meetod**, loenduse **funktsioon**.
    3. Väljale Nime **valikuline** sisestage **NumberOfTransactions**.

    Need sätted määravad, et iga transpordigrupi puhul arvutatakse kannete arv grupis.

10. Valige käsk **Salvesta**.
11. Vaadake üle <a name="ExecutionLocation">redigeeritava</a> andmeallika käivitamise parameetrid. Pange tähele **, et väljal** Täitmiskoht on **valitud** **automaatselt automaatne täitmine ja välja Täitmine** väärtus on **SQL.** Need sätted määravad, et valitud **kande** alusandmeallikas on praegu päringus ja te saate **käivitada redigeeritava GroupBy** andmeallika andmebaasi tasemel.
12. Avage otsing täitmisasukoha **välja** jaoks, et üle vaadata vabade väärtuste loend. Pange tähele, et saate **valida** **·** **päringu või mälus, et see groupBy** andmeallikas töötaks andmebaasi tasemel või rakendusserveri mälus.
13. Valige **salvestamine** ja sulgege **leht Grupeerimis alusel parameetrite** redigeerimine.
14. Valige **OK** GroupBy **andmeallika sätete** lõpuleviimiseks.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> GroupBy andmeallika sidumine andmemudeli väljadega

Siduge konfigureeritud andmeallikas andmemudeli väljadega, et määrata, kuidas andmemudel käitusajal rakendusandmed täidetakse.

1. Mudeli vastendamise **kujundaja** lehel andmemudeli **paanil** laiendage **transpordisõlme**.
2. Andmeallikate **paanil** laiendage **andmeallikat TransportRecord**.
3. Lisage sidumine, et saada kätte avastatud transpordigruppide loend:

    1. Valige andmemudeli paanil **transpordiüksus** **.**
    2. Valige andmeallikate **paanil** **andmeallikas TransportRecord**.
    3. Valige **Seo**.

4. Lisage sidumine, et muuta iga leitud transpordigrupi transpordikood kohustuslikuks:

    1. Valige transport.koodi **andmemudeli** kaup.
    2. Valige väli **TransportRecord.grouped.TransportMode** grupeeritud.
    3. Valige **Seo**.

5. Lisage sidumine, et saada kätte arvutatud agregaaside funktsioonide väärtused iga avastatud transpordigrupi puhul:

    1. Valige üksuse **Transport.NumberOfTransactions** andmemudeli kaup.
    2. Valige väli **TransportRecord.aggregated.NumberOfTransactions** agregaatväli.
    3. Valige **Seo**.
    4. Valige andmemudeli **kaup Transport.TotalInvoicedAmount**.
    5. Valige väli **TransportRecord.aggregated.TotalInvoicedAmount** aggregated.
    6. Valige **Seo**.

6. Lisage sidumine, et lisada igale avastatud transpordigrupile kuuluvad kandekirjed:

    1. Valige transport.Kande **andmemudeli** kaup.
    2. Valige väli **TransportRecord.lines**.
    3. Valige **Seo**.

    Transpordi pesastatud üksuste sidumiste konfigureerimist saate jätkata.Kande **andmemudeli** kaup ja andmeallika väli TransportRecord.**Ridade andmeallika väli, et käitusajal** kuvada Intrastati kannete üksikasjad, mis kuuluvad iga avastatu transpordigrupi juurde.

![Konfigureeritud mudelivastendus ER-i mudelivastenduse kujundajas.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Lisatud mudeli vastendamise komponendi silumine

Kasutage konfigureeritud [mudelivastenduse testimiseks](er-debug-data-sources.md) ER-andmeallika silurit.

1. Valige mudeli **vastendamise** kujundaja lehel suvand **Alusta silumist**.
2. **Vasakpoolsel paanil oleval silumisandmeallika** **lehel valige andmeallikas TransportRecord** ja seejärel valige suvand **Loe kõik kirjed**.
3. Laiendage **andmeallikat TransportRecord** ja järgige seejärel neid samme.

    1. Valige andmeallikas **TransportRecord.grouped.TransportMode**.
    2. Valige **Too väärtus**.
    3. Valige andmeallikas **TransportRecord.grouped.NumberOfTransactions**.
    4. Valige **Too väärtus**.
    5. Valige andmeallikas **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Valige **Too väärtus**.

4. Valige parempoolsel paanil suvand **Laienda kõik**.

Andmeallikas **TransportRecord** esitab kaks kirjet ja sisaldab kahte transpordikoodi. Iga transpordikoodi puhul arvutatakse kannete arv ja kogu arveldatud summa.

> [!NOTE]
> "Suuna lugemise" lähenemist kasutatakse, kui **GroupBy andmeallikat** kutsutakse andmebaasikutsete optimeerimiseks. Seetõttu arvutatakse mõned GroupBy **andmeallika** väljaväärtused ER-i andmeallika siluris ainult siis, kui need on seotud andmemudeliväljadega.

![Andmeallika silumise tulemused silumise lehel Andmeallikate silumine.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Kas grupi kogusummade arvutamisel saab arvutada kogusummasid?

Jah. Kogusummade arvutamiseks konfigureerige teine GroupBy **andmeallikas**, **kus eelnevalt konfigureeritud andmeallikat GroupBy** kasutatakse alusandmeallikana. Järgmine näide **näitab** **tüübi GroupBy andmeallikat Kogusummad, mida kasutatakse** **tüübi** GroupBy **·** **andmeallika TransportRecord** **andmeallika SUM-liitmisel põhineva liitmise funktsiooni Liitmise arvutamiseks tüübiga GroupBy.**

![Kogusummade andmeallikas ER-mudeli vastendamise kujundajas](./media/er-groupby-data-sources-configure-model-mapping2.png)

Järgmine näide näitab kogusummade andmeallika **silumise** tulemusi.

![Kogusummade andmeallika silumise tulemused lehel Silumine andmeallikad](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks](er-debug-data-sources.md)
- [Kasuta elektroonilise aruandluse vormingutes ANDMEKOGUMI andmeallikaid](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
