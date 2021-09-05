---
title: Taskukohase ravikindlustuse eelnõu (ACA) aruannete koostamine soodustuste halduses
description: Käesolevas teemas kirjeldatakse, kuidas Soodustuste haldus jälgib teavet, mis on esitatud Taskukohase ravikindlustuse eelnõu (ACA) tööandja kohustuse vormidega 1095-B ja 1095-C.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 99ac67795cd3f587e54a84361dd4744b79b4dbbd
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416250"
---
# <a name="generate-aca-reports-in-benefits-management"></a>ACA-aruannete loomine soodustuste halduses

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Soodustuste haldus jälgib teavet, mis on esitatud Taskukohase ravikindlustuse eelnõu (ACA) tööandja kohustuse vormidega 1095-B ja 1095-C. Nagu ka ACA aruandluse võimalused vanas tööruumis **Soodustused**, kehtib see funktsioon ainult USA juriidilistele isikutele.

Selle funktsiooni kasutamiseks peate esmalt lülitama sisse suvandi **Täpsem soodustuste haldus**. Lisateavet, sealhulgas olulisi hoiatusi soodustuste halduse kohta leiate jaotisest [Soodustuste halduse lubamine või keelamine](hr-admin-manage-features.md#enable-or-disable-benefits-management).

> [!IMPORTANT]
> ACA-aruandlust saate kasutada ainult kas tööruumist **Soodustuste haldus** või vanast tööruumist **Eelised**, mitte mõlemast. Näiteks kui lülitasite Soodustuste haldusele, on ACA aruandlus saadaval ainult tööruumis **Soodustuste haldus**, mitte vanas tööruumis **Soodustused**.
>
> Kui lülitute Soodustuste haldusele registreerimisaasta keskel, peate töötajata andmed soodustuste halduses kogu aasta jaoks õigesti konfigureerima. Sedasi tagate, et saate kogu aasta kohta õige aruandeteabe.

## <a name="getting-started"></a>Alustamine

1095-vormide jaoks andmete jälgimiseks looge kõigepealt üks või rohkem ravikindlustusega hõlmatud gruppi. Need grupid näitavad järgmist teavet.

- Töötajale antud kindlustuspakkumine
- Töötaja osa madalaima maksumusega kuumaksest, kui kulu ületab föderaalset vaesuspiiri
- Tööandja kasutatav Safe Harbor, kui see on kohaldatav

Ravikindlustusega hõlmatud grupid aitavad teil hallata neid andmeid mitme töötaja kirjete kohta, millel on samad tingimused. Saate kerge vaevaba määrata gruppe ühele või rohkemale töötajale.

### <a name="create-or-edit-an-affordable-care-coverage-group"></a>Ravikindlustusega hõlmatud grupi loomine või redigeerimine

1. Valige tööruumis **Soodustuste haldus** valik **Ravikindlustusega hõlmatud grupp**.

    ![Ravikindlustusega hõlmatud grupi valimine.](./media/hr-benefits-management-aca-coverage-group.png)

2. Uue ravikindlustusega hõlmatud grupi loomiseks valige **Uus** või olemasoleva grupi redigeerimiseks valige **Redigeeri**.

    ![Uue või Redigeerimise valik.](./media/hr-benefits-management-aca-new.png)

3. Seadistage järgmised väljad.

    | Field | Kirjeldus |
    |---|---|
    | Nimi | Sisestage grupile nimi. |
    | Kirjeldus | Saate sisestada grupi kirjeldus. |
    | Katvuse pakkumine | Töötajatele, nende abikaasale või partnerile ja nende ülalpeetavatele pakutav kindlustuskaitse. |
    | Töötaja kulu osa | Summa, mille eest vastutab töötaja. |
    | Kohaldatav jaotis 4980H Safe Harbor | 4980H Safe Harbori või ülemineku leevenduse kood. |
    | Plaani alguskuu | Valige kalendrikuu, millal teie soodustusplaani aasta algab. |
    | Grupp kehtib alates | Esimene kuupäev, millal see kirje kehtib. |
    | Grupp kehtib kuni | Viimane kuupäev, millal see kirje kehtib. Kui aegumiskuupäev puudub, sisestage **Mitte kunagi**. |

    ![Kindlustuskaitse grupi loomine.](./media/hr-benefits-management-aca-new-group.png)

4. Valige käsk **Salvesta**.

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a>Mitme töötaja määramine ravikindlustusega hõlmatud gruppi

1. Valige tööruumis **Soodustuste haldus** valik **Ravikindlustusega hõlmatud grupp**.
2. Valige grupp, millele töötajaid määrata.
3. Valige **Massiline määramine**.

    ![Massilise määramise valimine.](./media/hr-benefits-management-aca-mass-assignment.png)

4. Valige loendist töötajad ja seejärel valige käsk **Määra**.

    ![Valitud töötajate määramine gruppi.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a>Mitme kindlustuskaitse valiku säilitamine

Saate säilitada mistahes kindlustuskaitse grupist mitu versiooni. Kui teie organisatsioonis või teie pakutavates soodustustes midagi muutub, saate hoida grupi andmed ajakohased ilma, et peaksite looma uue grupi ja määrama töötajad sinna ümber.

Kui olete ravikindlustusega hõlmatud grupid loonud, saate neisse töötajaid hulgi määrata. Saate töötajaid gruppidesse ka ükshaaval määrata ning näidata, kas ACA teavet jälgitakse ja esitatakse.

Kui te ei pea töötaja ACA-teavet jälgima ja esitama, saate määrata suvandi **Kindlustuskaitse aruandlus** väärtuseks **Ei**. Näiteks võivad teil olla osalise tööajaga töötajad, kes ei vaja ACA-aruandlust.

### <a name="override-default-values-for-an-employee"></a>Töötaja vaikeväärtuste alistamine

Töötajate puhul, kes on määratud ravikindlustusega hõlmatud gruppi, saate kõigi kuude jaoks, mis vajavad erinevaid väärtusi, muuta järgmisi suvandeid.

- Katvuse pakkumine
- Töötaja kulu osa
- Kohaldatav jaotis 4980H Safe Harbor

> [!NOTE]
> 2020 ACA-aruannete puhul tuleb vormil 1095-C esitada nii töö kui ka kodu sihtnumbrid. Väärtused täidetakse praeguste aktiivsete asukohtade alusel automaatselt. Kui kumbki asukoht oli aasta mis tahes osal erinev, peate väärtuse alistama. 1095-C aruande väli **Sihtnumber** (rida 17) täidetakse ainult siis, kui kood **Kindlustuspakkumine** sisaldab väärtusi **1L** kuni **1Q** järgmiselt.
>
> - **1L, 1M või 1N:** esmane elukoha sihtnumber
> - **1O, 1P, 1Q:** esmane töökoha sihtnumber

Ravikindlustusega hõlmatud grupi mistahes väärtustele erandite sisestamiseks toimige järgmiselt.

1. Valige tööruumis **Personalihaldus** suvand **Lingid** ja seejärel **Töötajad**.
2. Valige loendist töötaja.
3. Valige vahekaardi **Tööhõive** jaotises **Lisateave** suvand **Ravikindlustuskaitse**.

    ![Ühe töötaja valikute muutmine.](./media/hr-benefits-management-aca-change-single-employee.png)

4. Valige suvand **Redigeeri**.
5. Iga kuu puhul, mis nõuab muudatusi, valige märkeruut **Vaikesätete alistamine** ja seejärel muutke vajadusel muid väärtusi.

    ![Vaikeväärtuste ülekirjutamine.](./media/hr-benefits-management-aca-override-default.png)

6. Valige käsk **Salvesta**.

## <a name="report-health-care-coverage"></a>Tervisekindlustuskaitse aruandlus

Peate jälgima täiskohaga ja osalise tööajaga töötajate mistahes töötaja toetusega töötaja enda kindlustuskaitset. Lisage aruandele 1095-C kõik töötajad ja nende ülalpeetavad nende kuude kohta, millal neil kindlustuskaitse oli.

Et näidata, kas soodustusplaanist tuleb teatada, järgige neid samme.

1. Valige tööruumis **Soodustuste haldus** suvand **Soodustusplaanid**.
2. Valige aruande soodustusplaan.
3. Valige suvand **Redigeeri**.
4. Seadke suvandi **Taskukohase ravikindlustuse eelnõu aruanne** väärtuseks **Jah**.

    ![Tervisekindlustuse registreerimine.](./media/hr-benefits-management-aca-report-coverage.png)

5. Valige käsk **Salvesta**.

Kui töötaja valib ülalpeetavale tervisekindlustuskaitse, määratakse ülalpeetava tervisekindlustuse kaitse periood kuupäeva järgi, millal ülalpeetav liideti või eemaldati. Kindlustuskaitse kuupäevad arvestatakse ülalpeetavatele vastavalt perioodile, millal ülalpeetav oli liitumisaastal plaani jaoks sobiv ja aktiivne.

## <a name="generate-1095-b-and-1095-c-forms"></a>Vormide 1095-B ja 1095-C loomine

Saate luua ka vormid 1095-B ja 1095-C ning jaotada need igale töötajale. Võite vormi 1095-C ja vastavad 1094-C edastusfailid luua ka elektrooniliselt ning saate need IRS-ile.

1. Valige tööruumis **Soodustuste haldus** kas **vorm ACA 1095-B** või **vorm ACA 1095-C**.
2. Muutke parameetreid vastavalt vajadusele ja valige **OK**.

    > [!NOTE]
    > Rohkem kui 500 töötaja 1095-C vormi printimisel saate rohkem kui ühe PDF-faili. Soovitame suurendada välja **Maksimaalne failisuurus megabaitides** väärtust lehel **Dokumendihalduse parameetrid** väärtusele **150**. (Selle lehe kiireks avamiseks kasutage navigeerimisriba otsinguvälja.)
    >
    > ![Maksimaalse failisuuruse muutmine.](./media/hr-benefits-management-aca-maximum-file-size.png)

3. Aruannete oleku kontrollimiseks ja nende vaatamiseks kasutage navigeerimisriba otsinguvälja, et avada leht **Elektroonilise aruandluse tööd**.

    ![Elektroonilise aruandluse tööde lehe otsing.](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. Valige vaatamiseks aruanne ja seejärel klõpsake käsku **Kuva failid**.

    ![Failide kuvamine.](./media/hr-benefits-management-aca-show-files.png)

5. Valige **Avamine**.

    ![Faili avamine.](./media/hr-benefits-management-aca-open-file.png)

6. Avage brauseriakna allosas kuvatav teavitusriba, avage zip-fail ja seejärel valige aruanne. Saate PDF-faili vaadata või printida.

    ![Vormi 1095-C näidis.](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a>ACA kindlustuskaitse teabe vaatamine

Leht **Töötaja ravikindlustuskaitse** kuvab järgmist teavet.

- Igale kindlustuskaitse grupile määratud töötajad
- Töötajad, keda ei pea aruandesse kaasama
- Määramata töötajad

Selle teabe vaatamiseks toimige järgmiselt.

1. Valige tööruumis **Soodustuste haldus** valik **Töötaja ravikindlustuskaitse**.
2. Valige grupp väljal **Grupi nimi**.

    ![ACA kindlustuskaitse vaatamine.](./media/hr-benefits-management-aca-view-coverage.png)

Kui mõni väärtus taskukohase ravikindlustuse grupist on alistatud, kuvatakse muudetud väärtuse kõrval tärn. Kui kõigi 12 kuu väärtused on samad ja neid pole alistatud, kuvatakse väärtus veerus **Kõik 12 kuud**.

Saate vaadata töötajaid, kes on märgitud ACA-aruandele mitte lisatavaks ja kes ei vaja vormi 1095-C. Valige väljal **Filtreerimise alus** suvand **Ei ole ACA-le esitatav**.

Saate vaadata töötajaid, kes pole gruppi määratud või kes on määratud aegunud gruppi. Valige väljal **Filtreerimisalus** valik **Määramata või aegunud grupp**.

### <a name="export-to-excel"></a>Excelisse eksportimine

Loendite eksportimiseks rakendusse Microsoft Excel järgi neid samme.

1. Valige nupp **Ava Microsoft Office'is**.
2. Valige **HCM-i inimressursside ajutine tabel sisemiseks kasutamiseks**.
3. Valige **Laadi alla**.

### <a name="view-aca-reportable-dependents"></a>ACA-aruandele lisatavate ülalpeetavate vaatamine

Kui peate kindlustuskaitsega inimestest teatama, sest pakute isekindlustuskaitset, saate vaadata ülalpeetavaid, kes on soodustusplaanidega kaitstud ja märgitud kui **ACA-aruandele lisatavad**. Valige toimingupaanil nupp **Vaata ülalpeetavate kindlustuskaitset**.

![Ülalpeetavate kindlustuskaitse vaatamine.](./media/hr-benefits-management-aca-view-dependent-coverage.png)

Kuvatakse töötaja ülalpeetavate kindlustuskaitse teave.

![Ülalpeetavate kindlustus.](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> Lehel kuvatakse ainult soodustusplaanid, mis on märgitud kui **ACA-aruandele lisatavad**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
