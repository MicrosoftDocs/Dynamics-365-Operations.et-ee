---
title: Regulatory Configuration Services (RCS) – globaliseerimise funktsioonid
description: Selles teemas selgitatakse, kuidas kasutada rakendust Microsoft Regulatory Configuration Services (RCS) ja globaalset hoidlat globaliseerimise funktsioonide loomiseks ja kasutamiseks.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 7faa9a3cf6a29d8ed126cfcb0e2902b2016d03ff
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358142"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) – globaliseerimise funktsioonid

[!include [banner](../includes/banner.md)]

Te saate kasutada rakendust Microsoft Regulatory Configuration Services (RCS) sellise globaliseerimise funktsiooni loomiseks, mida saab kasutada globaliseerimise teenuste raames, nagu näiteks e-arvete teenus. RCS võimaldab teha järgmisi toiminguid.

- Saate määratleda funktsiooniga seotud komponendid.
- Saate funktsiooni oleku kaudu hallata funktsiooni töötsüklit.
- Saate luua määratletud keskkondadele kättesaadava funktsiooni.
- Saate jagada funktsiooni teiste organisatsioonidega.

Järgmised protseduurid selgitavad, kuidas kasutaja saab RCS-is lisada globaliseerimise funktsioone ja seotud komponente, uuendada funktsiooni olekut ja muuta funktsiooni kättesaadavaks, et seda saaks kasutada globaliseerimise teenustes.

Enne protseduuride lõpule viimist peate lõpule viima järgmiste toimingutega seotud etapid.

- Juurdepääs RCS-i eksemplarile.
- Konfiguratsioonipakkuja loomine ja aktiveerimine. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

Toimige Finance and Operations-i rakenduste eksemplaris järgmiselt.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Kui teie ettevõtte jaoks pole RCS-i keskkonda ette valmistatud, valige **Regulatory services – konfiguratsioon** ja seejärel järgige juhised selle ettevalmistamiseks.

> [!NOTE]
> Kui teie ettevõtte jaoks on RCS-i keskkond juba ette valmistatud, kasutage keskkonnale juurde pääsemiseks lehe URL-i, valides sisselogimise suvandi.

## <a name="turn-on-the-globalization-features"></a>Globaliseerimise funktsioonide sisselülitamine

1. Valige oma RCS-i eksemplaris paan **Funktsioonihaldus**.
2. Valige tööruumis **Funktsioonihaldus** loendist suvand **Globaliseerimise funktsioonid** ja seejärel valige **Luba kohe**.

    ![Globaliseerimise funktsioonid funktsioonihalduses.](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globaliseerimisfunktsioonid

Globaliseerimise funktsioonide kasutamiseks peate selle esmalt importima globaalsest hoidlast ja looma sellest enda versiooni. Globaliseerimise funktsioonide lisamiseks on kaks võimalust.

- Saate lisada avaldatud või jagatud olemasoleva funktsiooni alusel tuletatud funktsiooni.
- Saate lisada uue funktsiooni, mille olete loonud nullist.

## <a name="access-globalization-features"></a>Juurdepääs globaliseerimise funktsioonidele

1. Veenduge, et funktsioon **Globaliseerimise funktsioonid** on funktsioonihalduses sisse lülitatud, nagu varasemalt käesolevas teemas kirjeldatud.
2. Avage uus tööruum **Globaliseerimise funktsioonid** ja valige seejärel jaotisest **Funktsioonid** paan **E-arved**.

    ![Globaalsete funktsioonide tööruum.](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    Leht **E-arvete funktsioonid** on avatud.

    ![E-arvete funktsioonide leht.](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Tuletatud globaliseerimise funktsiooni lisamine

Saate lisada uue globaliseerimise funktsiooni, tuletades selle juba avaldatud või jagatud olemasolevast funktsioonist.

1. Valige lehe **Globaalsest hoidlast funktsiooni importimine** avamiseks suvand **Impordi**.

    ![Globaalse hoidla lehelt funktsiooni importimine.](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Uusimate funktsioonide toomiseks valige **Sünkrooni**.

    Sünkroonitud loetelu hõlmab funktsioone, mis on teile saadaval seetõttu, et need avaldati Microsofti poolt, või seetõttu, et neid jagas teiega mõni teine konfiguratsioonipakkuja.

    ![Funktsioonide sünkroonitud loetelu.](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Valige loetelus imporditavad funktsioonid ja seejärel **Impordi**. Te saate teate, kui valitud funktsioonid on edukalt imporditud.

    ![Teade eduka importimise kohta.](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Valige **Lisa** ja seejärel valige dialoogiakna ripploendist suvand **Olemasoleval versioonil põhinev**.
5. Sisestage funktsiooni nimi ja kirjeldus.
6. Valige saadaolevate funktsioonide loetelust funktsiooni alusversioon ja seejärel valige **Loo funktsioon**.

    ![Tuletatud funktsiooni lisamine.](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    Lisatud funktsioon on loodud ja selle olek on **Mustand**.

    ![Mustandi olekuga tuletatud funktsioon.](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Vaadake üle funktsiooni komponendid, et teha kindlaks, kas värskendused on vajalikud.

    - Vaadake üle konfiguratsioonid, juhuks kui peate kohandama elektroonilise aruandluse vorminguid ja nende seotust funktsiooniversiooni vorminguvastendustega.
    - Vaadake seadistused üle, juhuks kui peate kohandama funktsiooniversiooni vahekaarti **Tegevused**, vahekaarti **Rakendatavuse reeglid** või vahekaarti **Muutujad**.

8. Valige vahekaardil **Versioonid** kuupäev **Kehtiv alates** ja sisestage kirjeldus, kui väli **Kirjeldus** on tühi.
9. Valige funktsiooni lõpule viimiseks suvand **Muuda olekut**. Lõpule viidud funktsioonid saab muuta kättesaadavaks konkreetsele keskkonnale, et seda saaks kasutada globaliseerimise teenustes, või neid saab avaldada globaalses hoidlas.

> [!NOTE]
> Funktsioone, mille suvandi **Funktsiooniversiooni olek** on **Avaldatud**, saab jagada väliste organisatsioonidega.

## <a name="add-a-new-globalization-feature"></a>Uue globaliseerimise funktsiooni lisamine

Saate lisada uue globaliseerimise funktsiooni, luues selle nullist.

1. Valige lehel **Globaalsest hoidlast funktsiooni importimine** suvand **Lisa** ja seejärel valige dialoogiakna ripploendis suvand **Uus funktsioon**.
2. Sisestage funktsiooni nimi ja kirjeldus.
3. Valige **Loo funktsioon**.

    ![Uue funktsiooni lisamine.](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Valige vahekaardil **Versioonid** suvandi **Kehtiv alates** kuupäev ja seejärel valige funktsiooni lõpule viimiseks suvand **Muuda olekut**. Lõpule viidud funktsioonid saab muuta kättesaadavaks konkreetsele keskkonnale, et seda saaks kasutada globaliseerimise teenustes, või neid saab avaldada globaalses hoidlas.

> [!NOTE]
> Funktsioone, mille suvandi **Funktsiooniversiooni olek** on **Avaldatud**, saab jagada väliste organisatsioonidega.

## <a name="feature-component-overview"></a>Funktsiooni komponendi ülevaade

Globaliseerimise funktsioonidel on mitu komponenti.

- **Versioon** – see komponent toetab funktsiooni töötsükli haldust ja võimaldab kasutajatel hallata funktsiooni erinevate versioonide olekut.
- **Konfiguratsioonid** – see komponent võimaldab kasutajatel hallata, kuvada ja redigeerida seotud elektroonilise aruandluse vorminguid ja vorminguvastendusi.
- **Seadistused** – see komponent võimaldab globaliseerimise teenuste, nt e-arvete teenus, kasutajatel hallata seotud funktsiooni versiooni seadistusi. Seega toetab see paindlike suhtlemise ja vastuste reeglite ülesehitamist.
- **Keskkond** – see komponent võimaldab globaliseerumise teenuste, nt e-arvete teenus, kasutajatel hallata keskkonda, kus funktsiooni versiooni seadistust kasutatakse, ja annab volituse kasutajatele, kellel saab olema sellele juurdepääs.
- **Organisatsioonid** – see komponent võimaldab kasutajatel jagada funktsiooni väliste organisatsioonidega.

## <a name="configuring-feature-components"></a>Funktsiooni komponentide konfigureerimine

### <a name="version-and-status"></a>Versioon ja olek

Versiooni kasutatakse globaliseerimise funktsiooni töötsükli haldamiseks.

Olekut saab muuta vahekaardi **Versioon** väljal **Olek**. Saadaval on järgmised olekud.

- **Mustand** – funktsiooni saab muuta vaid selles olekus.
- **Lõpule viidud** – funktsioon ja kõik seotud komponendid on lõpetatud (lõpule viidud) ja neid ei saa redigeerida.
- **Avaldatud** – funktsioon ja kõik seotud komponendid on avaldatud globaalses hoidlas.
- **Ühiskasutuses** – funktsioon ja kõik seotud komponendid on ühiskasutuses väliste organisatsioonidega.
- **Lubatud** – funktsioon ja kõik seotud komponendid on globaliseerimise teenuses, nt e-arvete teenus, kasutamiseks lubatud.

> [!NOTE]
> Mõnest olekust peavad funktsioonid järjekorras läbi liikuma. Seega ei pruugi iga olek igas elutsükli etapis saadaval olla.

### <a name="configurations"></a>Konfiguratsioonid

Konfiguratsioonide puhul on saadaval järgmised tegevused.

- **Kuvamine** – saate kuvada aluseks olevaid funktsiooni konfiguratsioone, mis ei vaja uuendamist.
- **Redigeerimine** – saate valitud konfiguratsioonist mustandiversiooni, et saaksite redigeerida vormingut ja vorminguvastendust vormingukujundajas.
- **Kustutamine** – saate kustutada funktsioonist valitud konfiguratsiooni.
- **Aluse muutmine** – saate muuta funktsiooni alust. Lisateabe saamiseks vaadake allpool käesoleva teema jaotises [Tuletatud globaliseerimise funktsioonide aluse muutmine](#rebase).

### <a name="setups"></a>Seadistused

Funktsioonide seadistuste puhul on saadaval järgmised tegevused.

- **Lisamine** – saate luua uue funktsiooni seadistuse. Selle funktsiooni seadistuse saab tuletada olemasolevast funktsiooni seadistusest või luua nullist.
- **Kustutamine** – saate kustutada valitud funktsiooni seadistuse.
- **Kuvamine** – saate kuvada aluseks olevat funktsiooni seadistust, mis ei vaja muudatusi.
- **Redigeerimine** – saate luua, kustutada või muuta funktsiooni seadistuse kolme põhikomponendi atribuute.

    - Tegevused ja nende parameetrid
    - Kohaldatavusreeglid
    - Muutujad

![Funktsiooni versiooni seadistamise leht.](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Keskkonnad

Keskkondade puhul on saadaval järgmised tegevused.

- **Lubamine** – valige valitud funktsiooniversiooni jaoks avaldatud keskkond ja valige **Kehtiv alates** kuupäev, millest alates see peaks olema kättesaadav. Lisateabe saamiseks vaadake allpool käesoleva teema jaotises [Lubamise jaoks keskkondade konfigureerimine](#configureenvironment).
- **Tühistamine** – saate eemaldada funktsiooni seadistuse keskkonna.

### <a name="organizations"></a>Organisatsioonid

Globaliseerimise funktsiooni välisele organisatsioonile ühiskasutuseks andmiseks toimige järgmiselt.

1. Valige lehel **E-arvete funktsioonid** ühiskasutusse antav funktsioon ja funktsiooniversioon.
2. Valige vahekaardil **Organisatsioonid** suvand **Anna ühiskasutusse** ja seejärel sisestage dialoogiakna rippmenüüs organisatsiooni domeeninimi.
3. Valige **Anna ühiskasutusse**.

    ![Funktsiooni organisatsiooni jaoks ühiskasutusse andmine.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

Funktsioon on antud ühiskasutusse valitud organisatsiooniga ja on selle organisatsiooni jaoks globaalses hoidlas kättesaadav. Sealt saab funktsiooni importida kasutamiseks organisatsiooni RCS-i või Dynamics 365 Finance'i eksemplari.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Tuletatud globaliseerimise funktsioonide aluse muutmine

Saate võtta tuletatud globaliseerimise funktsiooni aluseks uue või uuendatud põhifunktsiooni versiooni. Sel moel saab põhiversioonis aset leidnud muutusi automaatselt uuendada. Uuendatud põhifunktsiooni versiooni loob esialgne konfiguratsioonipakkuja ning seejärel see avaldatakse või antakse ühiskasutusse.

![Uuendatud põhifunktsiooni versioon.](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Näiteks kui soovite muuta teie loodud funktsiooni tuletatud versiooni alust, peate esmalt hankima funktsiooni uusima versiooni, importides selle globaalsest hoidlast.

1. Valige lehelt **E-arvete funktsioonid** suvand **Impordi**.
2. Uusimate funktsioonide toomiseks valige **Sünkrooni**.
3. Valige funktsioonide loetelus imporditavad funktsioonid ja seejärel **Impordi**.

    ![Funktsiooni uusima versiooni importimine.](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Valige funktsioonide loetelust funktsioon, mille alust soovite muuta.
5. Valige vahekaardil **Versioon** suvand **Uus**, et luua mustandversioon.

    ![Uus mustandversioon loodud.](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Valige **Aluse muutmine**.
7. Valige dialoogiaknas **Aluse muutmine** funktsiooni uusim versioon, millele vastavalt alust muudetakse.

    ![Dialoogiakna aluse muutmine.](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Valige nupp **OK**.
9. Vaadake üle funktsiooni komponendid ja tehke vajalikud muudatused.
10. Valige funktsiooni, mille alus on muudetud, lõpule viimiseks suvand **Muuda olekut**. Kui aluse muutmine on lõpule viidud, saate teostada täiendavaid toiminguid. Näiteks saate funktsiooni avaldada ja teha selle kasutamise globaliseerimise teenuste raames kättesaadavaks.

    ![Funktsiooni olek on muudetud lõpule viiduks.](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Globaliseerimise funktsioonide jaoks keskkondade konfigureerimine

Globaliseerimise teenuste kasutajad saavad hallata keskkonda, et seadistada globaliseerimise funktsioon ja anda volitus kasutajatele, kes sellele ligi pääsevad.

1. Valige tööruumis **Globaliseerimise funktsioonid** jaotisest **Keskkonnad** paan **E-arved**.

    ![Globaliseerimise funktsioonide tööruum.](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Valige **Võtmehoidla parameetrid** ja seejärel valige **Uus**, et luua Azure'i võtmehoidla saladus.
3. Sisestage võtmehoidla nimi ja kirjeldus ning seejärel sisestage väljal **Võtmehoidla URI** URL, mis tuvastab Azure'is võtmehoidla ressursi.
4. Valige kiirkaardil **Serdid** serdi lisamiseks suvand **Lisa** ja sisestage iga serdi nimi ja kirjeldus.

    ![Sert on lisatud.](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Valige uue keskkonna loomiseks **Uus**.
6. Sisestage nimi, kirjeldus ja salvestamiseks nõutud ühiskasutusele juurdepääsu allkirjaloa saladus.
7. Valige kiirkaardil **Kasutajad** suvand **Uus**, et lisada kasutaja, kellel on juurdepääsuõigus sellele keskkonnale.
8. Sisestage kasutaja ID ja e-posti aadress.
9. Kasutajate lisamiseks korrake samme 7 ja 8.
10. Keskkonna avaldamiseks valige suvand **Avalda**.

    ![Avaldatud keskkond.](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]