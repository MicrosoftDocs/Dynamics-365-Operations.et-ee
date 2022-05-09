---
title: Elektroonilise aruandluse konfiguratsioonide kohandamine elektroonilise dokumendi loomiseks
description: Selles teemas selgitatakse, kuidas kohandada Microsofti elektroonilise aruandluse (ER) konfiguratsioone, mida kasutatakse kohandatud elektroonilise dokumendi loomiseks.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7353d7d8149ff1316fbc0adc55b7e1050f443a8
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661654"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Elektroonilise aruandluse konfiguratsioonide kohandamine elektroonilise dokumendi loomiseks

[!include[banner](../includes/banner.md)]

Elektroonilise [aruandluse (ER) raamistik](general-electronic-reporting.md) võimaldab teil laadida üles Microsofti 365 finantseksemplari [pakutavad ER-i](general-electronic-reporting.md#Configuration)Microsoft Dynamics konfiguratsioonid. Sel viisil on Microsofti pakutud konfiguratsioonid ER-i lahenduseks, mida kasutatakse elektrooniliste kliendiarvete (e-arvete) loomiseks. Saate kasutada seda ER-i lahendust oma kohandatud ER-i lahenduse konfigureerimiseks, et pääseda juurde oma kohandatud andmebaasi väljadele ja luua e-arveid, mis vastavad teie konkreetsetele nõuetele, ilma lähtekoodi redigeerimata.

## <a name="overview"></a>Ülevaade

Selles teemas esitatud näites peate määratlema föderaalmaksu ID-koodi uue kohandatud atribuudina iga kliendi kohta, kellele te elektroonilist arvet esitate. Seetõttu peate kohandama praegu kasutusel oleva arve struktuuri, lisades uue üksuse, mis tuleb igas loodud e-arves täita maksukoodiga.

Selle teema protseduurid selgitavad, kuidas süsteemiadministraatori, elektroonilise aruandluse arendaja või elektroonilise aruandluse funktsionaalse konsultanti rolli kasutajad saavad teie Finance'i eksemplaris järgmisi ülesandeid täita.

- [Minimaalsete ER-i parameetrite konfigureerimine, mis on vajalikud ER-i raamistiku kasutamiseks](#ConfigureER).
- [Standardsete ER-i konfiguratsioonide algsete versioonide importimine, mida pakutakse e-arvete loomiseks](#ImportERConfigurations1).
- [Müügireskontro parameetrite konfigureerimine, et hakata kasutama standardseid ER-i konfiguratsioone](#ConfigureAR1).
- [Juriidilise isiku parameetrite konfigureerimine klientidele arvete esitamiseks](#ConfigureLE).
- [Kliendi kirje ettevalmistamine elektroonilise arvelduse jaoks](#ConfigureCustomer1).
- [Kliendi arve lisamine, sisestamine ja saatmine standardsete ER-i konfiguratsioonide abil](#ProcessInvoice1).
- [Kohandatud andmebaasi välja lisamine, et hallata klientide föderaalmaksu ID-koodi](#AddCustomField).
- [ER-i metaandmete värskendamine, et lubada ER-i mudelivastenduse kujundaja andmebaasi muudatusi](#RefreshERMetadata).
- [Kohandatud ER-i konfiguratsioonide kujundamine e-arvete loomiseks, mis sisaldavad uut maksukoodi](#DesignCustomERConfigurations).
- [Müügireskontro parameetrite konfigureerimine, et hakata kasutama kohandatud ER-i konfiguratsioone](#ConfigureAR2).
- [Kliendi kirje värskendamine elektroonilise arvelduse jaoks](#ConfigureCustomer2).
- [Kliendi arve lisamine, sisestamine ja saatmine kohandatud ER-i konfiguratsioonide abil](#ProcessInvoice2).
- [Standardsete ER-i konfiguratsioonide uute versioonide importimine, mida pakutakse e-arvete loomiseks](#ImportERConfigurations2).
- [Standardsete ER-i konfiguratsioonide uute versioonide muudatuste kasutuselevõtmine teie kohandatud ER-i konfiguratsioonides](#RebaseCustomERConfigurations).
- [Kliendi arve lisamine, sisestamine ja saatmine kohandatud ER-i konfiguratsioonide uute versioonide abil](#ProcessInvoice3).

Kõiki neid toiminguid saab lõpule viia ettevõttes **DEMF**.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>ER-raamistiku konfigureerimine

Elektroonilise aruandluse funktsionaalse konsultandi või elektroonilise aruandluse arendaja rolli kasutajana tuleb teil seadistada ER-i parameetrite minimaalne kogum. Seejärel saate hakata kasutama ER-i raamistikku e-arvete loomiseks kasutatava ER-i lahenduse standardsete konfiguratsioonide kohandatud versioonide loomiseks.

### <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokaliseerimise **kavandi lehel** jaotises Seotud lingid **valige** elektroonilise **aruandluse parameetrid**.
3. Valige lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** sätteks **Jah**.
4. Valige vahekaardi **Manused** väljal **Konfiguratsioonid** suvand **Fail**.
5. Valige väljadel **Töö arhiiv**, **Ajutine**, **Alus** ja **Muud** tüüp **Fail**.

Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

Kõigile lisatud ER-konfiguratsioonidele on märgitud omanikuks ER-konfiguratsiooni pakkuja. Sel eesmärgil kasutatakse tööruumis **Elektrooniline aruandlus** aktiveeritud ER-konfiguratsiooni pakkujat. Seega enne ER-konfiguratsioonide lisamist või redigeerimist peate aktiveerima tööruumis **Elektrooniline aruandlus** ER-konfiguratsiooni pakkuja.

> [!NOTE]
> ER-konfiguratsiooni saab redigeerida ainult selle omanik. Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.

#### <a name="review-the-list-of-er-configuration-providers"></a>ER-konfiguratsiooni pakkujate loendi ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokaliseerimise **kavandi lehel**, mis asub jaotises Seotud **lingid**, valige konfiguratsiooni **pakkujad**.
3. Lehel **Konfiguratsioonipakkuja tabel** on igal pakkuja kirjel kordumatu nimi ja URL. Vaadake üle selle lehe sisu. Kui üksuse **Litware, Inc.** (`https://www.litware.com`) kirje on juba olemas, jätke järgmine protseduur vahele [Uue ER-konfiguratsiooni pakkuja lisamine](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Uue ER-konfiguratsiooni pakkuja lisamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokaliseerimise **kavandi lehel**, mis asub jaotises Seotud **lingid**, valige konfiguratsiooni **pakkujad**.
3. Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.
4. Väljale **Nimi** sisestage väärtus **Litware, Inc.**
5. Sisestage väljale **Interneti-aadress** `https://www.litware.com`.
6. Valige käsk **Salvesta**.

#### <a name="activate-an-er-configuration-provider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokaliseerimise **kavandi lehel** jaotises Konfiguratsioonipakkujad **valige** **paani Litware, Inc.** ja seejärel valige käsk **Määra aktiivseks**.

Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Standardsete ER‑i konfiguratsioonide algsete versioonide importimine

Oma praegusesse Finance'i eksemplari standardsete ER-i konfiguratsioonide lisamiseks peate importima need selle eksemplari jaoks konfigureeritud ER-i [hoidlast](general-electronic-reporting.md#Repository).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokaliseerimise **kavandi** lehel jaotises **Konfiguratsioonipakkujad** valige **Microsofti** **paanid** ja seejärel valige hoidlad, et vaadata Microsofti pakkuja hoidlate loendit.
3. Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**. Kui teilt küsitakse autoriseerimist ühenduse loomiseks Regulatory Configuration Service'iga, järgige autoriseerimise juhiseid.
4. Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **PEPPOL-i müügiarve** konfiguratsioon.
5. Kiirkaardil **Versioonid** valige versioon **11.2.2**.
6. Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast.

![Konfiguratsioonihoidla leht.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Kui teil on probleeme [globaalsele hoidlale](er-download-configurations-global-repo.md) juurde pääsemisega, saate selle asemel [laadida konfiguratsioonid alla](download-electronic-reporting-configuration-lcs.md) Microsoft Dynamics Lifecycle Servicesist (LCS).

### <a name="review-the-imported-er-configurations"></a>Imporditud ER-konfiguratsioonide ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lokaliseerimise **kavandi lehel** jaotises Konfiguratsioonid **valige** aruandluse **konfiguratsioonipaan**.
3. Laiendage lehel **Konfiguratsioonid** kiirkaarti **Konfiguratsiooni komponendid**.
4. Laiendage vasakpoolse paani konfiguratsioonipuus suvandit **Arvemudel** ja seejärel laiendage suvandit **UBL-i müügiarve**.

Pange tähele, et lisaks valitud ER-vormingule **PEPPOL-i müügiarve** imporditi teised nõutavad ER-i konfiguratsioonid. Kuna ER-i konfiguratsioonide uusi versioone avaldatakse pidevalt globaalsesse hoidlasse ja LCS-i, et vastavad lahendused oleksid vastavuses uute nõuetega, siis imporditi nõutava andmemudeli konfiguratsiooni ja selle mudeli vastenduse konfiguratsioonide uusimad versioonid.

![Konfiguratsioonide leht.](./media/er-quick-start3-imported-solution1a.png)

Et simuleerida olekut, milles ER-i konfiguratsioonid oleksid praeguses Finance'i eksemplaris, kui impordite **PEPPOL-i müügiarve** ER-vormingu versiooni **11.2.2** minevikus (nt 7. augustil 2019), toimige järgmiselt.

- Valige toimingupaanil **Kustuta**, et kustutada kõik ER-i konfiguratsioonid, mis avaldati pärast 7. augustit 2019. Alles peaksid jääma ainult konfiguratsioonid **Arvemudel**, **Arve mudeli vastendus** (algselt nimega **Kliendi arve mudeli vastendus**), **UBL-i müügiarve** ja **PEPPOL-i müügiarve**.
- Kiirkaardile **Versioonid** alles jäänud ER-i konfiguratsioonide puhul valige **Kustuta**, et kustutada kõik ER-i konfiguratsioonide versioonid, mis avaldati pärast 7. augustit 2019.

Seejärel kinnitage, et konfiguratsioonipuus oleksid saadaval järgmised konfiguratsioonid.

- **Arvemudeli** ER-i andmemudeli konfiguratsioon (algselt nimega **Kliendi arve mudel**).

    - Versioon 11 sisaldab andmemudeli ER-i komponendi versiooni 10, mis tähistab arveldamise äridomeeni andmestruktuuri. See ER-i konfiguratsioon on imporditud importimiseks valitud **PEPPOL-i müügiarve** ER-vormingu eekäijana.
    - Versioon 50 sisaldab andmemudeli ER-i komponendi versiooni 31. See ER-i konfiguratsioon imporditi 7. augusti 2019 **Arve mudeli vastenduse** ER-i mudeli vastenduse konfiguratsiooni versiooni eelkäijana.

    ![Arvemudeli ER-i andmemudeli konfiguratsioon konfiguratsioonide lehel.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Kui teile ei kuvata selle andmemudeli versiooni 50, avage globaalne hoidla ja importige **Arve mudeli vastenduse** ER-i konfiguratsiooni versioon 50.19.

- **Arvemudeli vastenduse** ER-i mudeli vastenduse konfiguratsioon (algselt nimega **Kliendi arve mudeli vastendus**).

    - Versioon 50.19 imporditi **Arvemudeli** ER-i andmemudeli konfiguratsiooni versiooni 50 uusima juurutusena. See sisaldab kahte ER-i komponentide mudeli vastendust, mis kirjeldavad, kuidas rakenduse andmeid sisestatakse andmemudelisse käitusajal.

    ![Arvemudeli vastenduse ER-i mudeli vastenduse konfiguratsioon konfiguratsioonide lehel.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Kui teile ei kuvata selle mudeli vastenduse versiooni 50.19, avage globaalne hoidla ja importige **Arve mudeli vastenduse** ER-i konfiguratsiooni versioon 50.19.

- **UBLi-i müügiarve** ER-vormingu konfiguratsioon.

    - Versioon 11.2 sisaldab vormingut ja vormingu vastenduse ER-i komponente. Vormingu komponent määratleb aruande paigutuse. Vormingu vastenduse komponent sisaldab mudeli andmeallikat ja määratleb, kuidas seda andmeallikat kasutatakse aruande paigutuse täitmiseks käitusajal. See ER-vorming konfigureeriti looma e-arveid vormingus Universal Business Language (UBL). See on imporditud importimiseks valitud **PEPPOL-i müügiarve** ER-vormingu ülemüksusena.

- **PEPPOL-i müügiarve** ER-vormingu konfiguratsioon.

    - Versioon 11.2.2 sisaldab vormingut ja vormingu vastenduse ER-i komponente, mis konfigureeriti looma e-arveid vormingus Pan-European Public Procurement OnLine (PEPPOL).

    ![Peppol-i müügiarve ER-vormingu konfiguratsioon konfiguratsioonide lehel.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Müügireskontro parameetrite konfigureerimine

1. Minge jaotisse **Müügireskontro** \> **Seadistus** \> **Müügireskontro parameetrid**.
2. Valige vahekaardi **Elektroonilised dokumendid** kiirkaardi **Elektrooniline aruandlus** väljal **Müügi- ja vabas vormis arve** suvand **PEPPOL-i müügiarve**.
3. Valige käsk **Salvesta**.

![Elektrooniliste dokumentide vahekaart müügireskontro parameetrite lehel.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Juriidilise isiku parameetrite konfigureerimine

1. Avage **Organisatsiooni haldus** \> **Organisatsioonid** \> **Juriidilised isikud**.
2. Sisestage valitud ettevõtte **DEMF** kiirkaardile **Pangakonto teave** väljale **Marsruudi number** väärtus **1234**.
3. Valige käsk **Salvesta**.
4. Sulgege leht **Juriidilised isikud**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Kliendikirje ettevalmistamine

1. Avage **Müügireskontro** \> **Kliendid** \> **Kõik kliendid**.
2. Valige lehel **Kõik kliendid** kliendi konto link **DE-014**.

### <a name="add-a-customer-contact"></a>Kliendi kontakti lisamine

1. Avage **Müügireskontro** \> **Kliendid** \> **Kõik kliendid**.
2. Valige toimingupaanil vahekaardi **Klient** grupis **Kontod** suvand **Kontaktid**.
3. Valige **Lisa kontaktid**.
4. Avage lehe **Kontaktid** välja **Eesnimi** otsing, valige **Adam Carter** ja seejärel valige **Vali** otsingu sulgemiseks.
5. Valige käsk **Salvesta**.
6. Sulgege leht **Kontaktid**.

### <a name="define-a-primary-contact"></a>Esmase kontakti määratlemine

1. Avage **Müügireskontro** \> **Kliendid** \> **Kõik kliendid**.
2. Valige kiirkaardi **Müügidemograafia** väljal **Esmane kontakt** suvand **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>E-arvete suvandi seadistamine

1. Avage **Müügireskontro** \> **Kliendid** \> **Kõik kliendid**.
2. Määrake kiirkaardi **Arve ja tarne** suvandi **eInvoice** väärtuseks **Jah**.
3. Valige käsk **Salvesta**.
4. Sulgege leht **Kõik kliendid**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Kliendi arve töötlemine standardsete ER-i konfiguratsioonide abil

Nüüd saate kasutada standardseid ER-i konfiguratsioone, mille importisite kliendile vabas vormis elektroonilise arve saatmiseks.

### <a name="add-a-new-invoice"></a>Uue arve lisamine

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige lehel **Vabas vormis arve** suvand **Uus**.
3. Valige kiirkaardi **Vabas vormis arve päis** väljal **Kliendi konto** väärtus **DE-014**.
4. Kiirkaardile **Arve read** lisatakse automaatselt arve rida. Määrake sellel real järgmised väljad.

    - Sisestage väljale **Kirjeldus** väärtus **Märkmik**.
    - Valige väljal **Peamine konto** suvand **401100**.
    - Sisestage väljale **Ühiku hind** väärtus **1000**.

5. Valige käsk **Salvesta**.

![Vabas tekstis arve leht.](./media/er-quick-start3-add-invoice.png)

Lisateabe saamiseks vt [Vabas vormis arve loomine](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Uue arve sisestamine

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige toimingupaani lehel **Vabas vormis arve** suvand **Sisesta**.
3. Valige dialoogiboksis **Vabas vormis arve sisestamine** suvand **OK**.

![Vabas vormis arve üksikasjade leht.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Sisestatud arve saatmine

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige toimingupaani lehe **Vabas vormis arve** grupis **Dokument** suvand **Saada** \> **Algne**.

    ![Algse arve eelvaade.](./media/er-quick-start3-send-invoice.png)

3. Sulgege leht **Vabas vormis arve**.

### <a name="analyze-a-generated-e-invoice"></a>Loodud e-arve analüüsimine

1. Avage **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse tööd**.
2. Valige lehel **Elektroonilise aruandluse tööd** esialgne kirje, mille ülesande kirjeldus on **Saada eInvoice XML-vormingus**.
3. Loodud failide loendi juurde pääsemiseks valige **Kuva failid**.

    ![Elektroonilise aruandluse tööde leht.](./media/er-quick-start3-jobs-list.png)

4. Loodud e-arve XML-faili allalaadimiseks valige **Ava**.
5. Analüüsige e-arve XML-faili. Pange tähele, et kliendi maksuskeemi esindavad praegu XML-i atribuudid **schemeID** ja **schemeAgencyID**. Samuti pange tähele, et XML-i element **cbc:CustomizationID** sisaldab praegu järgmist teksti: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Loodud e-arve XML-faili eelvaade.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Kohandatud andmebaasi välja lisamine

Praegusesse Finance'i eksemplari järgmise kohanduse tegemiseks saate kasutada funktsiooni [Kohandatud väli](../../fin-ops/get-started/user-defined-fields.md).

- Kohandage andmebaasi struktuuri, lisades uue kohandatud andmebaasi välja, mis talletab kõikide klientide föderaalsmaksu ID-koode.
- Kohandage lehte **Klient**, lisades uue andmesisestusvälja, mida saab kasutada maksukoodi väärtuse sisestamiseks uuele kohandatud andmebaasi väljale.

Kohandamise tegemiseks toimige järgmiselt.

1. Avage **Müügireskontrod** \> **Kliendid** \> **Kõik kliendid**.
2. Valige lehel **Kõik kliendid** kliendi konto link **DE-014**.
3. Paremklõpsake kiirkaardil **Üldine** mis tahes tühja ala väljal **Keel** ja seejärel valige **Isikupärasta: UpperGroup**.

    Kiirkaardi **Üldine** sisu tõstetakse esile ja kuvatakse menüü **Isikupärastamine**.

4. Menüüs **Isikupärastamine** valige **Lisa väli**.
5. Dialoogiboksis **Lisa veerud** valige **Loo uus väli**.
6. Dialoogiboksi **Loo uus väli** väljal **Tabeli nimi** valige **Kliendid**.
7. Väljal **Nime eesliide** sisestage **FederalTaxID**.

    > [!NOTE]
    > Kogu välja nimi on automaatselt määratletud kui **FederalTaxID\_Kohandatud**.

8. Väljale **Silt** sisestage **Föderaalmaksu ID**.
9. Väljal **Tüüp** valige **Tekst**.
10. Väljale **Pikkus** sisestage **20**.
11. Valige käsk **Salvesta**.
12. Kuvatavas teateaknas valige **Jah**, et kinnitada, kas soovite luua uue välja kirje **FederalTaxID** tabelisse **Kliendid**.
13. Valige **Sisesta** välja **FederalTaxID\_Kohandatud** <a name="insert_custom_field"></a>lisamiseks praegusele lehele.

    ![Kõikide klientide leht.](./media/er-quick-start3-create-new-field.gif)

14. Sulgege leht **Kõik kliendid**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>ER-i metaandmete värskendamine

Peate värskendama ER-i metaandmed, et muuta lisatud kohandatud väli [nähtavaks](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) ER-i mudeli vastenduse kujundajas.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Tabeliviidete uuesti loomine**.
2. Dialoogiboksis **Andmemudeli värskendamine** valige **OK**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Kohandatud ER-i konfiguratsioonide kujundamine

Saate kasutada Microsofti antud ER-i konfiguratsioone oma kohandatud ER-i konfiguratsioonide kujundamiseks, et luua uut maksukoodi sisaldavaid e-arveid.

### <a name="customize-the-data-model-configuration"></a>Andmemudeli konfiguratsiooni kohandamine

Elektroonilise aruandluse funktsionaalse konsultandi rolli kasutajana saate kujundada oma kohandatud ER-i andmemudeli.

#### <a name="add-a-custom-data-model-configuration"></a>Kohandatud andmemudeli konfiguratsiooni lisamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvand **Kliendi arve mudel**.
3. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
4. Valige dialoogiboksi rippmenüü väljal **Uus** suvand **Tuleta nimest: kliendi arve mudel, Microsoft**, et näidata, et teie uus kohandatud ER-i andmemudeli konfiguratsioon peaks põhinema ER-i andmemudeli konfiguratsioonil.
5. Tippige väljale **Nimi** tekst **Arvemudel (Litware)**.
6. Uue ER-i konfiguratsiooni lisamiseks valige **Loo konfiguratsioon**.

Nüüd saate kasutada ER-i andmemudeli kujundajat **Arvemudeli (Litware)** ER-i konfiguratsiooni versiooni 50.1 redigeerimiseks **Mustandi** [olekus](general-electronic-reporting.md#component-versioning).

![ER-i konfiguratsiooni versioon 50.1 konfiguratsioonide lehel.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Kohandatud andmemudeli konfigureerimine

Peate muutma oma kohandatud andmemudelit, lisades uue välja föderaalmaksu ID-koodi väärtuse sisestamiseks. See kood on kliendiandmete osa igas ER-vormingus, mis kasutab seda andmemudelit andmeallikana.

1. Valige lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvand **Arvemudel (Litware)**.
2. Kiirkaardil **Versioonid** valige valitud ER-i andmemudeli konfiguratsiooni versioon **50.1**, mille olek on **Mustand**.
3. Valige toimingupaanil **Kujundaja** valitud konfiguratsiooni versioonile.
4. Valige lehe **Andmemudeli kujundaja** andmemudeli puus **Kliendi teave (klient)**.
5. Valige suvand **Uus**.
6. Kinnitage dialoogiboksi rippmenüü väljal **Uus sõlm kui** vaikeväärtus **Aktiivse sõlme alamüksus**.
7. Väljal **Nimi** sisestage **FederalTaxID\_Litware**.
8. Kinnitage väljal **Üksuse tüüp** vaikeväärtus **String**.
9. Valige **Lisa** ja seejärel **Salvesta**.

    ![Andmemudeli kujundaja leht.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Väljad **Silt** ja **Kirjeldus** kirjeldavad uue välja otstarvet. Neid välju saate täita mitmes keeles. Lisateavet vt [Mitmekeelsete aruannete kujundamine elektroonilises aruandluses](er-design-multilingual-reports.md).

10. Sulgege leht **Andmemudeli kujundaja**.

#### <a name="complete-a-custom-data-model-configuration"></a>Kohandatud andmemudeli konfiguratsiooni lõpule viimine

Peate töö [lõpule viima](general-electronic-reporting.md#component-versioning) oma kohandatud ER-i andmemudeli konfiguratsiooni versiooniga 50.1, et see oleks saadaval ka muude kohandatud ER-i konfiguratsioonide lisamiseks.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arvemudel** ja seejärel valige **Arvemudel (Litware)**.
3. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 50.1 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 50.2, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-i andmemudeli konfiguratsioonis täiendavate muudatuste tegemiseks.

![Versioon 50.1 on lõpule viidud konfiguratsioonide lehel.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Mudelivastenduse konfiguratsiooni kohandamine

Elektroonilise aruandluse arendaja rolli kasutajana saate kujundada oma kohandatud ER-i mudeli vastenduse.

#### <a name="add-a-custom-model-mapping-configuration"></a>Kohandatud mudelivastenduse konfiguratsiooni lisamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Kliendi arve mudel** ja seejärel valige **Kliendi arve mudeli vastendus**.
3. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
4. Valige dialoogiboksi rippmenüü väljal **Uus** suvand **Tuleta nimest: kliendi arve mudeli vastendus, Microsoft**, et näidata, et teie uus kohandatud ER-i mudeli vastenduse konfiguratsioon peaks põhinema ER-i mudeli vastenduse konfiguratsioonil.
5. Tippige väljale **Nimi** tekst **Arve mudeli vastendus (Litware)**.
6. Väljal **Sihtmudel** valige **Arvemudel (Litware)**.

    > [!IMPORTANT]
    > See etapp on väga oluline. Kui jätate selle välja, ei saa te konfigureeritud mudelivastendusel kasutada kohandatud andmemudelit.

7. Uue ER-i konfiguratsiooni lisamiseks valige **Loo konfiguratsioon**.

![Kohandatud mudelivastenduse konfiguratsiooni lisamine lehel „Konfiguratsioonid”.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Kohandatud mudelivastenduse konfigureerimine

Peate muutma oma kohandatud mudelivastendust ja määratlema, kuidas kohandatud andmemudeli kohandatud välja **FederalTaxID\_Litware** tuleb täita rakenduse andmetega käitusajal.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Kliendi arve mudel** \> **Kliendi arve mudeli vastendus** ja seejärel valige **Arve mudeli vastendus (Litware)**.
3. Valige toimingupaanil valik **Koostaja**.
4. Tehke lehe **Mudelist andmeallikasse vastendamine** valik **Kliendiarve** vastendus.

    ![Leht „Mudelist andmeallikasse vastendamine”.](./media/er-quick-start3-select-customer-mapping.png)

5. Valige **Kujundaja**.
6. Laiendage lehe **Mudelivastenduse kujundaja** paanil **Andmeallikad** andmeallikat **CustInvoiceJour**, mis tähistab rakenduse tabelit **CustInvoiceJour**.
7. Laiendage jaotises **CustInvoiceJour** suvandit **Seosed**, et vaadata läbi mitu-ühele (N:1) tüüpi seoste loend tabeli **CustInvoiceJour** jaoks.
8. Laiendage jaotises **CustInvoiceJour** \> **Seosed** suvandit **Kliendid (CustTable)**, et pääseda juurde tabeli **Kliendid (CustTable)** väljade ja seoste juurde.
9. Valige andmeallika väli **FederalTaxID\_Kohandatud**, mille [eelnevalt](#insert_custom_field) rakendasite.
10. Laiendage paanil **Andmemudel** suvandit **Kliendi teave (klient)** ja valige andmemudeli väli **FederalTaxID\_Litware**.
11. Valige **Seo**.

    ![Mudelivastenduse koostaja leht.](./media/er-quick-start3-customize-model-mapping.gif)

12. Valige käsk **Salvesta**.
13. Sulgege leht **Mudelivastenduse kujundaja**.
14. Sulgege leht **Mudelist andmeallikasse vastendamine**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Kohandatud mudelivastenduse konfiguratsiooni lõpule viimine

Peate töö [lõpule viima](general-electronic-reporting.md#component-versioning) oma kohandatud ER-i mudelivastenduse konfiguratsiooni versiooniga 50.19.1, et teha see kasutamiseks kättesaadavaks.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Kliendi arve mudel** \> **Kliendi arve mudeli vastendus** ja seejärel valige **Arve mudeli vastendus (Litware)**.
3. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 50.19.1 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 50.19.2, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-i mudelivastenduse konfiguratsioonis täiendavate muudatuste tegemiseks.

![Versioon 50.19.1 on lõpule viidud konfiguratsioonide lehel.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Toetatud konfiguratsiooni [elutsükkel](general-electronic-reporting-manage-configuration-lifecycle.md) ei hõlma andmebaasi muudatuste elutsüklit. Kui ekspordite konfiguratsiooni **Arve mudeli vastendus (Litware)** versiooni 50.19.1 praegusest Finance'i eksemplarist ja proovite seda importida teise eksemplari, mille tabel **CustTable** ei sisalda kohandatud välja **FederalTaxID\_Kohandatud**, ilmneb erand. Erand ütleb, et imporditud ER-i konfiguratsioon ei ühildu Finance'i sihteksemplari metaandmetega.

### <a name="customize-the-format-configuration"></a>Vormingu konfiguratsiooni kohandamine

Elektroonilise aruandluse funktsionaalse konsultandi rolli kasutajana saate kujundada oma kohandatud ER-vormingu.

#### <a name="add-a-custom-format-configuration"></a>Kohandatud vormingu konfiguratsiooni lisamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Kliendi arve mudel** \> **UBL-i müügiarve** ja seejärel valige **PEPPOL-i müügiarve**.
3. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
4. Valige dialoogiboksi rippmenüü väljal **Uus** suvand **Tuleta nimest: PEPPOL-i müügiarve, Microsoft**, et näidata, et teie uus kohandatud ER-vormingu konfiguratsioon peaks põhinema ER-vormingu konfiguratsioonil.
5. Tippige väljale **Nimi** tekst **PEPPOL-i müügiarve (Litware)**.
6. Valige väljal **Andmemudel** suvand **Arvemudel (Litware)**, et kasutada oma kohandatud andmemudelit ja mudelivastenduse komponente.

    > [!NOTE]
    > See etapp on väga oluline. Kui jätate selle välja, ei saa te konfigureeritud vormingus kasutada kohandatud andmemudelit.

7. Valige väljal **Andmemudel** juurdefinitsioon **InvoiceCustomer**.
8. Uue ER-i konfiguratsiooni lisamiseks valige **Loo konfiguratsioon**.

![Kohandatud vormingu konfiguratsiooni lisamine konfiguratsioonide lehel.](./media/er-quick-start3-adding-custom-format.png)

Nüüd saate kasutada ER-i toimingute kujundajat **PEPPOL-i müügiarve (Litware)** ER-i konfiguratsiooni versiooni 11.2.2.1 redigeerimiseks **Mustandi** [olekus](general-electronic-reporting.md#component-versioning).

![ER-i konfiguratsiooni versioon 11.2.2.1 konfiguratsioonide lehel.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Kohandatud vormingu konfigureerimine

Peate muutma oma kohandatud vormingut, lisades uue vorminguelemendi arveldatud kliendi föderaalsmaksu ID-koodi väärtus sisestamiseks.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Kliendi arve mudel** \> **UBL-i müügiarve** \> **PEPPOL-i müügiarve** ja seejärel valige **PEPPOL-i müügiarve (Litware)**.
3. Valige toimingupaanil valik **Koostaja**.
4. Laiendage vormingupuus suvandit **XMLHeader** \> **Arve** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** ja valige **cbc:ID**.
5. Valige **Lisa** ja seejärel **XML** \> **Atribuut**.
6. Sisestage dialoogiboksi **Komponendi atribuut** väljale **Nimi** tekst **FederalTaxID**.
7. Valige uue vorminguelemendi lisamiseks **OK**, et luua uus XML-atribuut **FederalTaxID** loodud XML-failis.
8. Valige vormingupuu jaotises **XMLHeader** \> **Arve** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** suvand **FederalTaxID**.
9. Valige **Nihuta üles**.

![Uus vorminguelement vormingukujundaja lehel.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Kohandatud vorminguvastenduse konfigureerimine

1. Lehel **Vormingu koostaja** vahekaardil **Vastendamine** laiendage andmeallikat **Arve**, mille tüüp on **Mudel**.
2. Laiendage jaotises **Arve** suvandit **Kliendi teave (klient)** ja valige **FederalTaxID\_Litware**.
3. Valige **Seo**.

    ![Vormingukujundaja leht.](./media/er-quick-start3-customized-format-mapping.png)

4. Valige andmemudel **Arve**, mille tüüp on **Mudel**, ja seejärel valige **Redigeeri**.
5. Valige väljal **Versioon** oma kohandatud andmemudeli versioon **1** ja seejärel valige **OK**.
6. Valige käsk **Salvesta**.
7. Sulgege **Vormingu kujundaja** leht.

#### <a name="complete-a-custom-format-configuration"></a>Kohandatud vormingu konfiguratsiooni lõpule viimine

Peate töö [lõpule viima](general-electronic-reporting.md#component-versioning) oma kohandatud ER-vormingu konfiguratsiooni versiooniga 11.2.2.1, et teha see kasutamiseks kättesaadavaks.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Kliendi arve mudel** \> **UBL-i müügiarve** \> **PEPPOL-i müügiarve** ja seejärel valige **PEPPOL-i müügiarve (Litware)**.
3. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 11.2.2.1 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 11.2.2.2, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-vormingu konfiguratsioonis täiendavate muudatuste tegemiseks.

![Versioon 11.2.2.1 on lõpule viidud konfiguratsioonide lehel.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Müügireskontro parameetrite konfigureerimine, et hakata kasutama kohandatud ER-i konfiguratsioone

1. Minge jaotisse **Müügireskontro** \> **Seadistus** \> **Müügireskontro parameetrid**.
2. Valige vahekaardi **Elektroonilised dokumendid** kiirkaardi **Elektrooniline aruandlus** väljal **Müügi- ja vabas vormis arve** suvand **PEPPOL-i müügiarve (Litware)**.
3. Valige käsk **Salvesta**.

![Müügireskontro parameetrite leht, Elektrooniliste dokumentide vahekaart, Elektroonilise aruandluse kiirkaart.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Kliendikirje värskendamine föderaalmaksu ID-koodi lisamisega

1. Avage **Müügireskontro** \> **Kliendid** \> **Kõik kliendid**.
2. Valige lehel **Kõik kliendid** kliendi konto link **DE-014**.
3. Sisestage kiirkaardi **Üldine** väljale **Föderaalmaksu ID** väärtus **LITWARE-6789**.
4. Valige käsk **Salvesta**.

    ![DE-014 kliendi üksikasjade leht.](./media/er-quick-start3-added-tax-id-value.png)

5. Sulgege leht **Kõik kliendid**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Kliendi arve töötlemine kohandatud ER-i konfiguratsioonide abil

### <a name="select-and-send-a-posted-invoice"></a>Sisestatud arve valimine ja saatmine

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige lehel **Vabas vormis arve** eelnevalt lisatud ja sisestatud arve.
3. Valige toimingupaani grupis **Dokument** suvand **Saada** \> **Algne**.
4. Sulgege leht **Vabas vormis arve**.

### <a name="analyze-a-generated-e-invoice"></a>Loodud e-arve analüüsimine

1. Avage **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse tööd**.
2. Valige lehel **Elektroonilise aruandluse tööd** uusim kirje, mille ülesande kirjeldus on **Saada eInvoice XML-vormingus**.
3. Loodud failide loendi juurde pääsemiseks valige **Kuva failid**.
4. Loodud e-arve XML-faili allalaadimiseks valige **Ava**.
5. Analüüsige e-arve XML-faili. Pange tähele, et vastavalt teie kohandusele sisaldab kliendi maksuskeem kohandatud XML-atribuuti **FederalTaxID** lisaks XML-atribuutidele **schemeID** ja **schemeAgencyID**. Selle uue XML-atribuudi väärtus määratletakse föderaalmaksu ID **LITWARE-6789** alusel, mis sisestati arveldatud kliendile.

    ![Teie kohandustega loodud e-arve XML-faili eelvaade.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Standardsete ER‑i konfiguratsioonide uusimate versioonide importimine

Selleks, et teie Finance'i eksemplari standardsete ER-i konfiguratsioonide komplekt oleks [ajakohane](general-electronic-reporting-manage-configuration-lifecycle.md), peate importima need uued versioonid, kui need on kättesaadavad selle eksemplari jaoks konfigureeritud ER-i [hoidlas](general-electronic-reporting.md#Repository).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Microsoft** ja seejärel valige pakkuja Microsoft hoidlate loendi kuvamiseks **Hoidlad**.
3. Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**. Kui teilt küsitakse autoriseerimist ühenduse loomiseks Regulatory Configuration Service'iga, järgige autoriseerimise juhiseid.
4. Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **PEPPOL-i müügiarve** konfiguratsioon.
5. Valige kiirkaardil **Versioonid** valitud ER-i konfiguratsiooni versioon **32.6.7**, mis on väljastatud kliendi elektrooniliste arvete toetamiseks vormingus PEPPOL BIS 3. Lisateavet vt [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.

![Valitud versioon 32.6.7 konfiguratsiooni hoidla lehel.](./media/er-quick-start3-import-solution2.png)

Lisateavet selle protsessi automatiseerimisvõimaluse kohta leiate teemast [ER-i konfiguratsioonide värskendatud versioonide importimine](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Imporditud ER-konfiguratsioonide ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Laiendage kiirkaarti **Konfiguratsiooni komponendid**.
4. Laiendage vasakpoolse paani konfiguratsioonipuus suvandit **Arvemudel**. Pange tähele, et ühes imporditud ER-i andmemudeli konfiguratsioonis on nime **Kliendi arve mudel** asemel **Arvemudel**.
5. Laiendage vasakpoolse paani konfiguratsioonipuus suvandit **Arve mudeli vastendus**. Pange tähele, et ühes imporditud ER-i mudelivastenduse konfiguratsioonis on nime **Kliendi arve mudeli vastendus** asemel **Arve mudeli vastendus**.
6. Laiendage suvandit **UBL-i müügiarve** \> **PEPPOL-i müügiarve**.

Pange tähele, et lisaks valitud ER-vormingule **PEPPOL-i müügiarve** imporditi teiste nõutavate ER-i konfiguratsioonide uusimad versioonid. Kuna ER-i konfiguratsioonide uusi versioone avaldatakse pidevalt globaalsesse hoidlasse ja LCS-i, et vastavad ER-i lahendused oleksid vastavuses uute nõuetega, siis imporditi nõutava andmemudeli konfiguratsiooni ja selle mudeli vastenduse konfiguratsioonide uusimad versioonid.

Veenduge, et konfiguratsioonipuus oleksid lõpuks saadaval järgmised ER-i konfiguratsioonid.

- **Arvemudel** ER-i andmemudeli konfiguratsioon.

    - Versioon 206 (või uuem) sisaldab andmemudeli ER-i komponendi versiooni 24 (või uuemat), mis tähistab arveldamise äridomeeni andmestruktuuri. See ER-i konfiguratsioon imporditi **Arve mudeli vastenduse** ER-i mudelivastenduse konfiguratsiooni uusima saadaoleva versiooni eelkäijana.

    ![Versioon 206 konfiguratsioonide lehel.](./media/er-quick-start3-imported-solution2b1.png)

- **Arve mudeli vastendus** ER-i mudelivastenduse konfiguratsioon.

    - Versioon 206.132 (või uuem) imporditi **Arvemudeli** ER-i andmemudeli konfiguratsiooni versiooni 206 uusima juurutusena. See sisaldab mitut ER-i komponentide mudelivastendust, mis kirjeldavad, kuidas rakenduse andmeid sisestatakse andmemudelisse käitusajal.

    ![Versioon 206.132 konfiguratsioonide lehel.](./media/er-quick-start3-imported-solution2b2.png)

- **UBLi-i müügiarve** ER-vormingu konfiguratsioon.

    - Versioon 32.6 sisaldab vormingut ja vormingu vastenduse ER-i komponente. Vormingu komponent määratleb aruande paigutuse. Vormingu vastenduse komponent sisaldab mudeli andmeallikat ja määratleb, kuidas seda andmeallikat kasutatakse aruande paigutuse täitmiseks käitusajal. See ER-vorming konfigureeriti looma e-arveid UBL-vormingus. See on imporditud importimiseks valitud **PEPPOL-i müügiarve** ER-vormingu ülemüksusena.

- **PEPPOL-i müügiarve** ER-vormingu konfiguratsioon.

    - Versioon 32.6.7 sisaldab vormingut ja vormingu vastenduse ER-i komponente, mis konfigureeriti looma e-arveid PEPPOL-vormingus.

    ![Versioon 32.6.7 konfiguratsioonide lehel.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Uute standardsete ER-i konfiguratsioonide muudatuste kasutuselevõtmine teie kohandatud ER-i konfiguratsioonides

### <a name="adopt-your-custom-er-data-model"></a>Kohandatud ER-i andmemudeli kasutuselevõtmine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arvemudel** ja seejärel valige **Arvemudel (Litware)**.
3. Kiirkaardil **Versioonid** valige valitud andmemudeli konfiguratsiooni mustandiversioonile **50.2** suvand **Aluse muutmine**.
4. Kinnitage väljal **Sihtversioon** aluseks oleva ER-i andmemudeli konfiguratsiooni versiooni **206** valik ja seejärel valige **OK**.

    Teie kohandatud ER-i andmemudeli konfiguratsiooni mustandiversiooni numbri **50.2** asemele tuleb **206.2**, mis viitab sellele, et see sisaldab nüüd teie kohandust, mis ühendati uusima aluseks oleva ER-i andmemudeli konfiguratsiooni versiooni (206) muudatustega.

    > [!NOTE]
    > Aluse muutmise tegevus on tühistatav. Selle aluse muutmise tühistamiseks valige kiirkaardil **Versioonid** mudeli **Arvemudel (Litware)** versioon **50.1** ja seejärel valige **Hangi see versioon**. Versiooni 206.2 numbriks pannakse seejärel uuesti **50.2** ja mustandiversiooni 50.2 sisu vastab versiooni 50.1 sisule.

5. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 206.2 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 206.3, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-i andmemudeli konfiguratsioonis täiendavate muudatuste tegemiseks.

![Versioon 206.2 on lõpule viidud konfiguratsioonide lehel.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Kohandatud ER-i mudelivastenduse kasutuselevõtmine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arvemudel** \> **Arve mudeli vastendus** ja seejärel valige **Arve mudeli vastendus (Litware)**.
3. Kiirkaardil **Versioonid** valige valitud mudelivastenduse konfiguratsiooni mustandiversioonile **50.19.2** suvand **Aluse muutmine**.
4. Kinnitage väljal **Sihtversioon** aluseks oleva ER-i mudelivastenduse konfiguratsiooni versiooni **206.132** valik ja seejärel valige **OK**.

    Teie kohandatud ER-i mudelivastenduse konfiguratsiooni mustandiversiooni numbri **50.19.2** asemele tuleb **206.132.2**, mis viitab sellele, et see sisaldab nüüd teie kohandust, mis ühendati uusima aluseks oleva ER-i mudelivastenduse konfiguratsiooni versiooni (206.132) muudatustega.

    Pange tähele, et avastati mõned aluse muutmise konfliktid. Nüüd peate need konfliktid käsitsi lahendama.

    ![Aluse muutmise konflikti teade konfiguratsioonid lehel.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Valige toimingupaanil **Kujundaja** ja seejärel valige vastenduste loendist **Kliendi arve**.
6. Iga aluse muutmise konflikti puhul valige **Säilita oma väärtus**, sest peate säilitama oma kohandatud andmemudeli versiooni numbri igal mainitud komponendil.

    ![Aluse muutmise konfliktid lehel „Mudeli vastenduse koostaja”.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Valige **Salvesta** ja sulgege leht **Mudeli vastenduse koostaja**.
8. Valige vastenduste loendist **Projekti arve**.
9. Iga aluse muutmise konflikti puhul valige **Säilita oma väärtus**, sest peate säilitama oma kohandatud andmemudeli versiooni numbri igal mainitud komponendil.
10. Valige **Salvesta** ja sulgege leht **Mudeli vastendused**.

    > [!NOTE]
    > Aluse muutmise tegevus on tühistatav. Selle aluse muutmise tühistamiseks valige kiirkaardil **Versioonid** mudelivastenduse **Arve mudeli vastendus (Litware)** versioon **50.19.1** ja seejärel valige **Hangi see versioon**. Versiooni 206.132.2 numbriks pannakse seejärel uuesti **50.19.2** ja mustandiversiooni 50.19.2 sisu vastab versiooni 50.19.1 sisule.

11. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 206.132.2 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 206.132.3, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-i mudelivastenduse konfiguratsioonis täiendavate muudatuste tegemiseks.

![Versioon 206.132.2 on lõpule viidud konfiguratsioonide lehel.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Teie kohandatud ER-vormingu kasutuselevõtmine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arvemudel** \> **UBL-i müügiarve** \> **PEPPOL-i müügiarve** ja seejärel valige **PEPPOL-i müügiarve (Litware)**.
3. Kiirkaardil **Versioonid** valige valitud vormingu konfiguratsiooni mustandiversioonile **11.2.2.2** suvand **Aluse muutmine**.
4. Kinnitage versiooni väljal **Siht** aluseks oleva ER-vormingu konfiguratsiooni versiooni **32.6.7** valik ja seejärel valige **OK**.

    Teie kohandatud ER-vormingu konfiguratsiooni mustandiversiooni numbri **11.2.2.2** asemele tuleb **32.6.7.2**, mis viitab sellele, et see sisaldab nüüd teie kohandust, mis ühendati uusima aluseks oleva ER-vormingu konfiguratsiooni versiooni (32.6.7) muudatustega.

    Pange tähele, et avastati mõned aluse muutmise konfliktid. Nüüd peate need konfliktid käsitsi lahendama.

5. Valige toimingupaanil valik **Koostaja**.
6. Iga aluse muutmise konflikti puhul valige **Säilita oma väärtus**, sest peate säilitama oma kohandatud andmemudeli versiooni numbri igal mainitud komponendil.
7. Valige käsk **Salvesta**.
8. Valige vahekaardil **Vastendus** andmemudel **Arve**, mille tüüp on **Mudel**, ja seejärel valige **Redigeeri**.
9. Valige väljal **Versioon** oma kohandatud andmemudeli versioon **2** ja seejärel valige **OK**.
10. Valige käsk **Salvesta**.

    > [!NOTE]
    > Aluse muutmise tegevus on tühistatav. Selle aluse muutmise tühistamiseks valige kiirkaardil **Versioonid** voringu **PEPPOL-i müügiarve (Litware)** versioon **11.2.2.1** ja seejärel valige **Hangi see versioon**. Versiooni 32.6.7.2 numbriks pannakse seejärel uuesti **11.2.2.2** ja mustandiversiooni 11.2.2.2 sisu vastab versiooni 11.2.2.1 sisule.

11. Sulgege **Vormingu kujundaja** leht.
12. Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.

Versiooni 32.6.7.2 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks. Lisatud on uus redigeeritav versioon, 32.6.7.3, ja selle olekuks on **Mustand**. Seda versiooni saate kasutada oma kohandatud ER-vormingu konfiguratsioonis täiendavate muudatuste tegemiseks.

![Versioon 32.6.7.2 on lõpule viidud konfiguratsioonide lehel.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Kliendi arve töötlemine kohandatud ER-i konfiguratsioonide uute versioonide abil

### <a name="select-and-send-a-posted-invoice"></a>Sisestatud arve valimine ja saatmine

1. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
2. Valige lehel **Vabas vormis arve** eelnevalt lisatud ja sisestatud arve.
3. Valige toimingupaani grupis **Dokument** suvand **Saada** \> **Algne**.

    > [!NOTE] 
    > Kuna teil on nüüd kaks ER-vormingu konfiguratsiooni **PEPPOL-i müügiarve (Litware)** versiooni ja kummalgi versioonil pole [jõustumiskuupäeva](general-electronic-reporting.md#component-date-effectivity) väärtust, kasutatakse e-arve loomiseks uusimat versiooni.

4. Sulgege leht **Vabas vormis arve**.

### <a name="analyze-a-generated-e-invoice"></a>Loodud e-arve analüüsimine

1. Avage **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Elektroonilise aruandluse tööd**.
2. Valige lehel **Elektroonilise aruandluse tööd** kõige uuem kirje, mille ülesande kirjeldus on **Saada eInvoice XML-vormingus**.
3. Loodud failide loendi juurde pääsemiseks valige **Kuva failid**.
4. Loodud e-arve XML-faili allalaadimiseks valige **Ava**.
5. Analüüsige e-arve XML-faili. Pange tähele, et vastavalt teie kohandusele sisaldab kliendi maksuskeem endiselt kohandatud XML-atribuuti **FederalTaxID** lisaks XML-atribuutidele **schemeID** ja **schemeAgencyID**. Lisaks, kuna aluseks oleva vormingu **UBL-i müügiarve** uue versiooni muudatused ühendati teie kohandusega, muudeti XML-elemendi **cbc:CustomizationID** teksti `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` asemele `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Kohandustega loodud e-arve XML-faili eelvaade.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [ER-konfiguratsioonide allalaadimine teenusest Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [ER-konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](er-download-configurations-global-repo.md)
- [Vabas vormis arve loomine](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Kohandatud väljade loomine ja nendega töötamine](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
