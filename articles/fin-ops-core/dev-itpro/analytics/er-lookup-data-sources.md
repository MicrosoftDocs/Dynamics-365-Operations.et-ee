---
title: Andmeallikate otsingu konfigureerimine kasutama ER-i rakendusepõhiseid parameetreid
description: See artikkel selgitab, kuidas konfigureerida otsingu andmeallikaid elektroonilise aruandluse (ER) vormingutes, et kasutada ER-i rakendusepõhiseid parameetreid.
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: f3ce5837b1d20860588848a1b518b3d801a05db4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285117"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Andmeallikate otsingu konfigureerimine kasutama ER-i rakendusepõhiseid parameetreid 

[!include[banner](../includes/banner.md)]

[Elektroonse aruandluse (ER)](general-electronic-reporting.md) rakendusepõhiste parameetrite funktsiooniga saab konfigureerida andmete filtreerimist ER-vormingus, nii et see põhineb abstraktsete reeglite kogumil. Seda reeglite kogumit saab konfigureerida ER-vormingus saadaolevate **Otsingu** tüübiga andmeallikate kasutamiseks. Saate määrata reaalseid reegleid väljaspool ER komponentide disainereid, kasutades kasutajaliidest (UI), mis luuakse automaatselt vastava ER-vormingu ja praeguse juriidilise isiku andmete **Otsingu** andmeallika põhjal. Lõpuks pääseb määratud reeglitele juurde ER-vormingu **otsingu** andmeallikas, kui see ER-vorming käivitatakse.

> [!NOTE]
> Redigeeritava ER-vormingu konfigureeritud andmeallikate abil saate määrata, milliseid rakenduse andmeid kasutatakse tegelike reeglite konfigureerimiseks.

[ER-toimingute kujundaja](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) abil saate **otsingu** tüübi andmeallika oma ER-vormingusse tuua. Andmeallikas peab olema konfigureeritud kirjeldama, kuidas teie abstraktsed reeglid välja näevad, sealhulgas järgmist.

   - Teatud andmetüübi parameetrite kogum, mille väärtus esitatakse ühe reegli määramiseks.
   - Teatud andmetüübi väärtusetüüp, mille tagastab üks reegel, kui seda reeglit peetakse muu hulgas kõige sobivamaks.

Sõltuvalt mis tahes konfigureeritud reegli tagastatud väärtuse tüübist saate konfigureerida järgmist tüüpi **otsingu** andmeallikaid:

   - Kasutage mudeli loendiväärtuse tagastamisel tüüpi **Andmemudel\Otsing**.
   - Kasutage **Dynamics 365 Operations\Lookup** tüüpi, kui rakenduse loendi väärtus või rakenduse [laiendatud andmetüübi](../extensibility/extensible-edts.md) väärtus tuleb tagastada.
   - Kasutage vormingu loendiväärtuse tagastamisel tüüpi **Vormingu loend\Otsing**.

Järgmisel joonisel on kujutatud, kuidas vormingulist loendit saab konfigureerida näidis-ER-vormingus.

   ![Vormingu loendi kuvamine konfigureeritud otsingu andmeallika alusena.](./media/er-lookup-data-sources-img1.gif)

Järgmisel joonisel on kujutatud vormingukomponendid, mis on konfigureeritud esitama erinevat tüüpi maksete loodud aruande teises jaotises.

   ![Vormingujaotiste kuvamine erinevat tüüpi maksudest eraldi teatamiseks.](./media/er-lookup-data-sources-img2.png)

Järgmisel joonisel on kujutatud, kuidas ER Operationd kujundaja lubab lisada andmeallika tüübile **Vorming\Otsing**.  Lisatud andmeallikas on konfigureeritud tagastama `List of taxation levels` vormingu loendi väärtust.

   ![Vormingu loendi\otsingutüübi ER-andmeallika lisamine.](./media/er-lookup-data-sources-img3.gif)

Järgmisel joonisel on kujutatud, kuidas lisatud andmeallikas on konfigureeritud kasutama **mudeli** andmeallika loendi **Model.Data.Tax** välja **Kood** parameetrina, mis tuleb määrata iga konfigureeritud reegli jaoks.

![Vormingu loendi\otsingutüübi lisatud andmeallika parameetrite konfigureerimine.](./media/er-lookup-data-sources-img4.gif)

Lisatud `Model.Data.Tax` andmeallikas on konfigureeritud määrama maksukoodi iga konfigureeritud reegli jaoks, pääsedes juurde rakendustabeli **TaxTable** kirjetele.

   ![Vormingu loendi\otsingutüübi üheettevõtte otsingu andmeallika ülevaade.](./media/er-lookup-data-sources-img5.gif)

Saate seadistada valitud ER-vormingu otsingureeglid, kasutades kasutajaliidest, mis joondatakse automaatselt konfigureeritud andmeallika struktuuriga. Praegu nõuab see kasutajaliides, et määraksite iga reegli puhul tagastatud väärtuse `List of taxation levels` nii vormingu loendiväärtuseks kui ka maksukoodi parameetriks.

   ![Saate häälestada konfigureeritud andmeallika reegleid.](./media/er-lookup-data-sources-img6.gif)

Järgmisel joonisel on kujutatud, kuidas tüübiga **Arvutatud väli** `Model.Data.Summary.LevelByLookup` andmeallikat saab konfigureerida kutsuma konfigureeritud **otsingu** andmeallikat, mis pakub vajalikke parameetreid. Kutsungi töötlemiseks käitusajal läbib ER määratletud jada konfigureeritud reeglite loendi, et leida esimene reegel, mis vastab esitatud tingimustele. Näites on see reegel, mis sisaldab esitatud maksukoodile vastavat maksukoodi. Selle tulemusena leitakse kõige sobivam reegel ja leitud reegli jaoks konfigureeritud loendiväärtuse tagastab see andmeallikas.

> [!NOTE]
> Erand visatakse, kui kohaldatavat reeglit ei leita. Nende erandite vältimiseks konfigureerige reeglite loendi lõpus täiendavad reeglid, et käsitleda juhtumeid, kui pole konfigureeritud väärtust või väärtust pole esitatud. Kasutage vastavalt suvandeid **\*Pole tühi**\* ja **\*Tühi**\*.  
>
> ![Andmeallika lisamine konfigureeritud otsingu andmeallika kutsumiseks.](./media/er-lookup-data-sources-img7.png)

Kui seate redigeeritava otsingu andmeallika jaoks **ettevõtteülese** suvandi väärtuseks **Jah**, lisate selle andmeallika parameetrite kogumikku uue nõutava **ettevõtte** parameetri. **Ettevõtte** parameetri väärtus tuleb määrata käitusajal, kui otsingu andmeallikas kutsutakse. Kui ettevõtte kood on määratud käitusajal, kasutatakse selle ettevõtte jaoks konfigureeritud reegleid kõige sobivama reegli leidmiseks ja vastav väärtus tagastatakse. Järgmisel joonisel on kujutatud, kuidas saate seda teha ja kuidas redigeeritava andmeallika parameetrite kogumit muudetakse.

   ![Vormingu loendi\otsingutüübi ettevõtteülese otsingu andmeallika ülevaade.](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Valige iga ettevõte eraldi, et konfigureerida selle redigeeritava ER-vormingu otsingu andmeallika reeglite kogum. Erand visatakse käitusajal, kui kontserniülest otsingut nimetatakse selle ettevõtte koodiga, mille otsingusätet ei viidud lõpule.
>
> Veenduge, et annaksite ettevõtteülese **otsingu** andmeallikaga ER-vormingut käitavale kasutajale õigused juurdepääsuks iga selle andmeallika kohaldamisalasse kuuluva ettevõtte andmetele. Vastasel korral ilmneb erand käitusajal.

Alates versioonist 10.0.19 on saadaval **otsingu** andmeallikate laiendatud võimalused. Kui seate redigeeritava otsingu andmeallika suvandi **Laiendatud** väärtuseks **Jah**, teisendatakse konfigureeritud otsingu andmeallikas struktureeritud andmeallikaks, mis pakub konfigureeritud reeglite kogumi analüüsimiseks täiendavaid võimalusi. Järgmisel illustratsioonil on toodud see transformatsioon.

   ![Vormingu loendi\otsingutüübi struktureeritud otsingu andmeallika ülevaade.](./media/er-lookup-data-sources-img9.gif)

- **Otsingu** alamüksus on loodud funktsioonina, et leida kõige sobivam reegel konfigureeritavate reeglite komplektist, mis põhineb esitatud parameetrite komplektil.
- Alamüksus **IsLookupResultSeton** loodud funktsioonina aktsepteerima põhiloendi andmeallika esitatud väärtust ja tagastama *kahendväärtuse* **Tõene**, kui reeglite kogum sisaldab vähemalt ühte reeglit, mille jaoks esitatud loendiväärtus on konfigureeritud tagastatud väärtusena. See funktsioon tagastab *kahendväärtuse* **Väär**, kui esitatud loendiväärtuse tagastamiseks pole konfigureeritud reegleid.
- Alamüksuse **Seadistamine** on loodud funktsioonina, mis tagastab konfigureeritud reeglite komplekti kirjeloendi kirjetena. Tagastatud väärtused ja konfigureeritud reeglite parameetrite kogum esitatakse igas tagastatud kirjes järgmiste andmetüüpide väljadena.

    - Tagastatud väärtus esitatakse väljana **Otsing tulem**.
    - Konfigureeritud parameetrid esitatakse väljadena, millel on parameetrite nimed (selles näites väli **Kood**).

Lisateavet **otsingu** andmeallika konfigureerimise kohta leiate teemast [ER-vormingute konfigureerimine juriidiliste isikute kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md). Lisateavet otsingureeglite seadmise kohta leiate teemast [ER-vormingu parameetrite seadistamine juriidilise isiku kohta](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Lisaressursid

[ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md)

[Elektroonilise aruandluse vormingu parameetrite häälestus juriidilise isiku kohta](er-app-specific-parameters-set-up.md)
