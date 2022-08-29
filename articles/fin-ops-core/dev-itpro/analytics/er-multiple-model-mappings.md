---
title: Ühe mudeli juure mitme tuletatud vastenduse haldamine
description: See artikkel selgitab, kuidas hallata mitut tuletatud vastendust, mis konfigureeriti ühe mudeli juure jaoks.
author: kfend
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERSolutionTable, ERModelMappingTable
ms.openlocfilehash: 868d47ccfebb9a9753d93344c72b10ae4353b0e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277504"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Ühe mudeli juure mitme tuletatud vastenduse haldamine

[!include [banner](../includes/banner.md)]

Elektroonilise [aruandluse (ER)](general-electronic-reporting.md) andmemudelikomponenti kasutatakse igas konfigureeritud ER-vormingu komponendis andmeallikana väljaminevate dokumentide loomiseks. Ühe äridomeeni kirjeldamiseks konfigureerige andmemudeli komponent, mis sisaldab palju juurdefinitsioone. 

Iga juurdefinitsioon võimaldab teil esindada selle domeeni andmeid viisil, mis sobib kõige paremini konkreetsete aruandluse eesmärkidega. Iga juurdefinitsiooni jaoks saate konfigureerida ER-mudeli vastendamise Microsoft Dynamics komponendi kui oma andmemudeli 365 finantsipõhine rakendamine. Nii saate kirjeldada, kuidas teie andmemudel käitusajal täidetakse.

ER-i mudeli vastendamise komponendid võivad asuda ER-i andmemudeli [konfiguratsioonides](general-electronic-reporting.md#Configuration) ja ER-mudeli vastendamise konfiguratsioonides. Üksik ER-i konfiguratsioon võib sisaldada palju vastendamise komponente, millest igaüks on konfigureeritud ühe juurdefinitsiooni jaoks. Teise võimalusena võib üksik ER-i konfiguratsioon sisaldada ainult ühte vastendamise komponenti, mis on konfigureeritud ühe juurdefinitsiooni jaoks.

Paljud konfiguratsiooni pakkujad võivad pakkuda ER-i mudeli vastendamise konfiguratsioone samale ER-i andmemudelile. Need mudeli vastendamise konfiguratsioonid võivad sisaldada erinevate juurdefinitsioonide vastendamise komponente. Võite kasutada ühe juurdefinitsiooni jaoks ühe [pakkuja](general-electronic-reporting.md#Provider) pakutavat mudeli vastendamist ja teise juurdefinitsiooni jaoks teise pakkuja pakutavat mudeli vastendust.

Selles artikli protseduurides seletatakse, kuidas hallata ER-i andmemudeli mitut ER-mudeli vastendamiskonfiguratsiooni, kui need sisaldavad sama juurdefinitsiooni jaoks konfigureeritud eri mudelivastenduse komponente. 

Selle artikli protseduuride lõpule viimiseks peate olema määratud süsteemiadministraatori või elektroonilise aruandluse arendaja rollile.

Kõiki järgmisi protseduure saab teha ettevõttes USMF. Koodi pole vaja kirjutada.

## <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Elektroonilise aruandluse arendaja rollis kasutajana [konfigureerige minimaalne](er-quick-start2-customize-report.md#ConfigureFramework) ER-i parameetrite kogum, enne kui hakkate kasutama äridokumentide loomiseks ER-i raamistikku.

## <a name="import-the-standard-er-format-configurations"></a>Standardse ER‑vormingu konfiguratsiooni importimine

Oma praegusesse rakenduse Finance eksemplari standardsete ER-i konfiguratsioonide lisamiseks peate importima need selle eksemplari jaoks konfigureeritud ER-i hoidlast. Järgige juhiseid teemas [Elektroonilise aruandluse konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](er-download-configurations-global-repo.md), et importida järgmised ER-vormingu konfiguratsioonid.

- **Vabas vormis arve (Excel)**, versioon 220.106
- **Projekti arve (Excel)**, versioon 226.27

## <a name="review-the-imported-er-configurations"></a>Imporditud ER-konfiguratsioonide ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
3. Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Arve mudel**.

    ![Imporditud konfiguratsioonide konfiguratsioonide lehel läbi vaatamine.](./media/er-multiple-model-mappings-image1.png)

4. Vaadake läbi vorming **Vabas vormis arve (Excel)**:

    1. Valige vasakpoolse paani konfiguratsioonipuus suvand **Vabas vormis arve (Excel)**.
    2. Valige toimingupaanil valik **Koostaja**.
    3. Lehel **Vormingu koostaja** vahekaardil **Vastendamine** valige allikate loendist suvand **Mudel**.
    4. Valige suvand **Kuva**.
    
       Praegune ER-vorming on konfigureeritud kasutama juurdefinitsiooni **InvoiceCustomer** suvandis **Arve mudel**. Kui see vorming käivitatakse ja kutsutakse andmeallikas **Mudel**, kasutatakse rakenduse andmetele juurdepääsuks ja andmemudeli täitmiseks mudeli vastendust, mis on konfigureeritud juurdefinitsiooni **InvoiceCustomer** jaoks.

        ![Mudeli andmeallika läbivaatamine vormingu koostaja lehel.](./media/er-multiple-model-mappings-image2.png)

    6. Sulgege **Vormingu kujundaja** leht.

5. Vaadake läbi konfiguratsiooni **Arve mudeli vastendus** sisu:

    1. Valige vasakpoolse paani konfiguratsioonipuus suvand **Arve mudeli vastendus**.
    2. Valige toimingupaanil valik **Koostaja**.
    3. Pange lehel **Mudelist andmeallikasse vastendamine** tähele, et praegune ER-i mudeli vastendamise konfiguratsioon sisaldab mitut mudeli vastendamise komponenti.

        + Mudelivastendus **Kliendiarve** konfigureeritakse juurdefinitsiooni **InvoiceCustomer** jaoks suvandis **Arve mudel**. Seega saab ER-vormingu **Vabas vormis arve (Excel)** käitamisel valida selle ER-i konfiguratsiooni mudelivastenduse **Kliendiarve**, et pääseda juurde rakenduse andmetele ja täita andmemudel.
        + Mudelivastendus **Projekti arve** konfigureeritakse juurdefinitsiooni **InvoiceProject** jaoks suvandis **Arve mudel**. Seega saab ER-vormingu **Projekti arve (Excel)** käitamisel valida selle ER-i konfiguratsiooni mudelivastenduse **Projekti arve**, et pääseda juurde rakenduse andmetele ja täita andmemudel.

        ![Arve mudeli vastendamine lehel "Mudelist andmeallikasse vastendamine".](./media/er-multiple-model-mappings-image3.png)

    4. Sulgege leht **Mudelist andmeallikasse vastendamine**.
    5. Valige kiirkaardil **Versioonid** suvand **Kustuta**, et kustutada selle ER-i konfiguratsiooni kõik versioonid, mis on hilisemad kui versioon 240.175.

6. Vaadake läbi konfiguratsiooni **Projekti arve mudelivastendus (RDP)** sisu:

    1. Valige vasakpoolse paani konfiguratsioonipuus suvand **Projekti arve mudelivastendus RDP**.
    2. Valige toimingupaanil valik **Koostaja**.
    3. Pange tähele, et lehel **Mudelist andmeallikasse vastendamine** sisaldab praegune ER-i mudelivastenduse konfiguratsioon mudelivastendust **InvoiceProject** ja et see mudelivastendus on konfigureeritud juurdefinitsiooni **InvoiceProject** jaoks suvandis **Arve mudel**. Valige ER-vormingu **Projekti arve (Excel)** käitamise ajal selle ER-i konfiguratsiooni mudelivastendus **InvoiceProject**, et pääseda juurde rakenduse andmetele ja täita andmemudel.

        ![Projekti arve mudeli vastendamine mudelist andmeallikasse vastendamise lehel.](./media/er-multiple-model-mappings-image4.png)

    4. Sulgege leht **Mudelist andmeallikasse vastendamine**.
    5. Valige kiirkaardil **Versioonid** suvand **Kustuta**, et kustutada selle ER-i konfiguratsiooni kõik versioonid, mis on hilisemad kui versioon 226.35.

## <a name="customize-the-imported-er-configurations"></a>Imporditud ER-konfiguratsioonide kohandamine

See jaotis selgitab, kuidas [kohandada](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) Microsofti pakutavaid mudelivastendusi. Näiteks kohandumine võib olla vajalik kohandatud loogika rakendamiseks või puuduvate seoste lisamiseks.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Arve mudeli vastenduse konfiguratsiooni kohandamine

1. Valige lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvand **Arve mudeli vastendamine**.
2. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
3. Valige dialoogiakna ripploendi **Konfiguratsiooni loomine** väljal **Uus** suvand **Tuleta nimest: arve mudeli vastendamine, Microsoft**.
4. Sisestage väljale **Nimi** tekst **Arve mudeli vastendus, Litware**.
5. Valige **Konfiguratsiooni loomine**.
6. [Märkige](er-quick-start2-customize-report.md#MarkFormatRunnable) tuletatud vastenduse [mustand](general-electronic-reporting.md) käitusajal kasutamiseks kättesaadavaks.

    1. Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Täpsemad sätted** valik **Kasutaja parameetrid**.
    2. Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.
    3. Vastavalt vajadusele valige **Redigeeri**, et muuta leht redigeeritavaks.
    4. Konfiguratsiooni **Arve mudeli vastendus, Litware** jaoks, mis on praegu konfiguratsioonipuus valitud, määrake suvandi **Käivita mustand** valikuks **Jah**.

7. Valige tegevuspaanil suvand **Kujundaja**, et vaadata läbi selle konfiguratsiooni mudelivastendused.

    ![Arve mudeli vastenduste läbivaatamine mudelist andmeallikasse vastendamise lehel.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Nüüd saate avada kujundajas kõik selle ER-i konfiguratsiooni ER-mudeli vastendamise komponendid oma kohandatud loogika konfigureerimiseks. Lisateavet vt teemast [Mudelivastenduse konfiguratsiooni kohandamine](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Sulgege leht **Mudelist andmeallikasse vastendamine**.

Nüüd on teil konfiguratsioonid **Arve mudeli vastendus** ja **Arve mudeli vastendus, Litware**, millel kummalgi on mudelivastendus, mis on konfigureeritud juurdefinitsiooni **InvoiceCustomer** jaoks. Määrake üks mudeli vastendustest konkreetselt mudelivastenduseks, mida kasutab mis tahes ER-vorming, nt vorming **Vabas vormis arve (Excel)**, mis sisaldab mudeli andmeallikat, mille juurdefinitsioon on **InvoiceCustomer**. Vastasel juhul ilmneb ühe ER-vormingu käivitamisel, redigeerimisel või valideerimisel järgmine erand teavitamaks, et vaikemudelite vastendamist pole eraldi määratud.
 
> Andmemudelis '\<model name\> (\<root descriptor\>)' konfiguratsioonides \<configuration names separated by commas\> on olemas rohkem kui üks mudeli vastendus. Määrake üks konfiguratsioonides vaikeväärtuseks.

![Vormingu avamine konfiguratsioonide lehel redigeerimiseks.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Projekti arve mudelivastenduse (RDP) konfiguratsiooni kohandamine

1. Valige lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvand **Projekti arve mudelivastendus (RDP)**.
2. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
3. Valige dialoogiakna **Konfiguratsiooni loomine** väljal **Uus** suvand **Tuleta nimest: Projekti arve mudelivastendus (RDP), Microsoft**.
4. Sisestage väljale **Nimi** tekst **Projektiarve mudelivastendus, Litware**.
5. Valige **Konfiguratsiooni loomine**.
6. Konfiguratsiooni **Projekti arve mudelivastendus, Litware** jaoks, mis on praegu konfiguratsioonipuus valitud, määrake suvandi **Käivita mustand** valikuks **Jah**.
7. Valige tegevuspaanil suvand **Kujundaja**, et vaadata läbi selle konfiguratsiooni mudelivastendused.

    ![Kohandatud projekti arve mudelivastenduse läbivaatamine mudelist andmeallikasse vastendamise lehel.](./media/er-multiple-model-mappings-image7.png)

8. Sulgege leht **Mudelist andmeallikasse vastendamine**.

Nüüd on teil konfiguratsioonid **Arve mudeli vastendus**, **Projekti arve mudelivastendus (RDP)** ja **Projekti arve mudelivastendus, Litware**. Igal konfiguratsioonil on juurdefinitsiooni **InvoiceProjecti** jaoks konfigureeritud mudelivastendus. Määrake üks mudelivastendustest konkreetselt vaikemudeli vastenduseks, mida kasutab mis tahes ER-vorming. Näiteks kasutage vormingut **Projekti arve (Excel)**, mis sisaldab mudeli andmeallikat, mille juurdefinitsioon on **InvoiceProject**. Vastasel juhul ilmneb ühe ER-vormingu käivitamisel või redigeerimisel erand teavitamaks, et vaikemudelite vastendamist pole eraldi määratud.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Tuletatud konfiguratsiooni Arve mudeli vastendus, Litware valimine vaikimisi mudelivastendusi sisaldava konfiguratsioonina

1. Valige lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvand **Arve mudeli vastendamine, Litware**.
2. Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.

    ![Mudelivastenduse konfiguratsioonide lehel vaikimisi mudelivastenduseks määramine.](./media/er-multiple-model-mappings-image8.png)

    Selle seadistuse tõttu kasutatakse mudelivastendust **Kliendiarve koopia**, kui käitate suvandit **Vabas vormis arve (Excel)** või kui redigeerite seda või kinnitate selle. Mudelivastendust **Kliendiarve** konfiguratsioonis **Arve mudelivastendus** ignoreeritakse.

    Saate nüüd avada vormingu **Vabas vormis arve (Excel)**, et vaadata vormingu kujundaja üle.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Tuletatud konfiguratsiooni Projekti arve mudeli vastendus, Litware valimine vaikimisi mudelivastendusi sisaldava konfiguratsioonina

1. Valige lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvand **Projekti arve mudeli vastendamine, Litware**.
2. Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.

    Sel juhul, erinevalt eelmises jaotises konfiguratsioonis **Arve mudeli vastendamine, Litware** kirjeldatud juhtumist, ei saa te mudelivastendust **InvoiceProjecti koopia** konfiguratsioonist **Projekti arve mudeli vastendamine, Litware** vastendamiseks kasutama hakata. Kaks konfiguratsiooni, mis sisaldavad mudelivastendust juurdefinitsiooni **InvoiceProject** jaoks, on praegu märgitud vaikekonfiguratsioonina. Seega on neil kasutamiseks võrdne prioriteet. Selle probleemi lahendamiseks viige lõpule selle protseduuri ülejäänud etapid.

3. Valige vasakpoolse paani konfiguratsioonipuus suvand **Arve mudelivastendus, Litware**.
4. Valige toimingupaanil valik **Koostaja**.
5. Valige lehel **Mudelist andmeallikasse vastendamine** suvand **Redigeeri**, et muuta leht vastavalt vajadusele redigeeritavaks.
6. Valige mudelivastendus **Projekti arve koopia** ja seejärel valige selle jaoks märkeruut **On kustutatud**.

    ![Mudelivastenduse virtuaalselt kustutatuks seadmine vaikimisi mudelivastenduseks määramise lehel.](./media/er-multiple-model-mappings-image9.png)

    Selle seadistuse tõttu käsitletakse konfiguratsiooni **Arve mudeli vastendamine, Litware** justkui sellel puuduks juurdefinitsiooni **InvoiceProject** jaoks mudelivastendus. Vaikimisi väljastatud mudelivastendus **InvoiceProjecti koopia**. Konfiguratsioon **Projekti arve mudeli vastendus, Litware**, mis sisaldab seda mudelivastendust, on märgitud vaikimisi konfiguratsiooniks. Kuna see on märgitud vaikeväärtuseks, on sellel kõrgem prioriteet kui mudelivastendus **InvoiceProject** konfiguratsioonist **Projekti arve mudelivastendus (RDP)**.

## <a name="other-considerations"></a>Muud kaalutlused

Mudelivastendus **InvoiceProjecti koopia** konfiguratsioonis **Projekti arve mudeli vastendamine, Litware** on loodud kasutama andmealikat **ReportDataProvider**. Andmeallikas on osa tüübist *Objekt*, mis viitab rakenduse klassile **PsaProjInvoiceDP**. See klass rakendatakse prindihalduse raamistiku projekti arve SQL-serveri aruandlusteenuste (SSRS) aruande andmepakkujana. Valige see andmeallikas ER-i [integreerimispunktiks](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Prindihalduse aruannete praegune ER-i juurutamine arvestab selle seadistusega. Lisateavet vaadake rakenduseklassi **ERPrintMgmtDataProviderReport** lähtekoodist. Käitusajal sunnib andmeallika **ReportDataProvider** määramine mudeli vastendamise integreerimispunktina rakendust Finance käsitlema seda vastendamiskomponenti kõrgema prioriteediga kui vastendamise komponenti **InvoiceProject** konfiguratsioonist **Projekti arve mudelivastendus (RDP)**.

## <a name="see-also"></a>Vt ka

- [Elektroonilise aruandluse (ER) mudelivastenduse haldamine eraldi ER-i konfiguratsioonides](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Riigi kontekstist sõltuva ER-mudeli vastenduste konfigureerimine](er-country-dependent-model-mapping.md)
- [Elektroonilise aruandluse raamistiku API muudatused](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
