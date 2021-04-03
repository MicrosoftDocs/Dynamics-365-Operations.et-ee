---
title: Tegevusest sõltuvate ER-i sihtkohtade konfigureerimine
description: Sellest teemast selgitatakse, kuidas konfigureerida tegevusest sõltuvad sihtkohad konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks.
author: NickSelin
manager: AnnBe
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 80624e286fd1300b8de6fd8a7fc67c246cb3a41b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569631"
---
# <a name="configure-action-dependent-er-destinations"></a>Tegevusest sõltuvate ER-i sihtkohtade konfigureerimine

[!include [banner](../includes/banner.md)]

Saate konfigureerida [sihtkohad](electronic-reporting-destinations.md) iga [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [vormingu](general-electronic-reporting.md#FormatComponentOutbound) [konfiguratsiooni](general-electronic-reporting.md#Configuration) väljundi komponendi jaoks, mida kasutatakse väljamineva dokumendi jaoks. Kasutajad, kes kasutavad seda tüüpi ER-vormingut ja kellel on vastavad pääsuõigused, saavad muuta konfigureeritud sihtkoha sätteid ka käitusajal.

Rakenduse Microsoft Dynamics 365 Finance **versioonis 10.0.17 ja uuemas** saab ER-vormingut käitada [valmistades ette](er-apis-app10-0-17.md) tegevuse koodi, mille kasutaja ER-vormingut käitades teeb. Näiteks moodulis **Müügireskontro**, saate prindihalduse sätetes valida ER-vormingu, mis loob kindla äridokumendi, nt vabas vormis arve. Seejärel saate arve eelvaate kuvamiseks valida nupu **Kuva** või printerisse saatmiseks nupu **Prindi**. Kui kasutaja tegevus edastatakse töötavasse ER-vormingusse käitusajal, saate konfigureerida eri kasutaja tegevustele erinevad ER-i sihtkohad. Selles teemas selgitatakse, kuidas konfigureerida ER-i sihtkohti seda tüüpi ER-vormingule.

## <a name="make-action-dependent-er-destinations-available"></a>Tegevusest sõltuvate ER-i sihtkohtade kättesaadavaks tegemine

Praeguses rakenduse Finance eksemplaris tegevusest sõltuvate ER-i sihtkohtade konfigureerimiseks ja [uue](er-apis-app10-0-17.md) ER-i API lubamiseks avage tööruum [Funktsiooni haldus](../../fin-ops/get-started/feature-management/feature-management-overview.md#the-feature-management-workspace) ja lülitage sisse funktsioon **Konkreetsete ER-i sihtkohtade konfigureerimine, mida kasutada erinevate PM-tegevuste jaoks**. Konfigureeritud ER-i sihtkohtade kasutamiseks käitusajal [kindlate](#reports-list-wave1) aruannete jaoks, lubage funktsioon **PM-aruannete väljundi marsruutimine ER-i sihtkohtade põhjal, mis on kasutaja tegevusele spetsiifilised (voog 1)**.

## <a name="configure-action-dependent-er-destinations"></a>Tegevusest sõltuvate ER-i sihtkohtade konfigureerimine

Kui lülitate sisse funktsiooni **Konkreetsete ER-i sihtkohtade konfigureerimine, mida kasutada erinevate PM-tegevuste jaoks**, saate konfigureerida tegevusest sõltuvad ER-i sihtkohad kiirkaardil **Faili sihtkoht** lehel **Elektroonilise aruandluse sihtkoht**. Iga komponendi jaoks saate lisada kirje ja lubada konkreetsed ER-i sihtkohad. Iga kirje jaoks peate määrama dokumendi tüübi, millele konfigureeritud ER-i sihtkohad peaksid olema rakendatud. Valige väljal **Dokumendi tüüp** üks järgmistest väärtustest.

- Valige **Elektrooniline**, et rakendada konfigureeritud sihtkohad, kui käitusajal kasutajategevuse koodi ei esitata.
- Valige **Prindihaldus**, et rakendada konfigureeritud sihtkohad, kui käitusajal esitatakse kasutajategevuse kood.
- Valige **Mis tahes**, et rakendada konfigureeritud sihtkohad alati, olenemata sellest, kas kasutaja tegevus käitusajal esitatakse.

Kui valite dokumenditüübi **Prindihaldus**, peate määrama kasutaja tegevused, mille puhul tuleb konfigureeritud ER-i sihtkohti rakendada. Valige väljal **Prindihalduse tegevus** üks järgmistest väärtustest.

- Valige **Kuva**, et rakendada konfigureeritud sihtkohad, kui käitusajal esitatakse kaustaja tegevus **Kuva**.
- Valige **Prindi**, et rakendada konfigureeritud sihtkohad, kui käitusajal esitatakse kaustaja tegevus **Prindi**.
- Valige **Saada**, et rakendada konfigureeritud sihtkohad, kui käitusajal esitatakse kasutaja tegevus **Saada**.

> [!NOTE]
> Ühe sihtkirje jaoks saab valida mitu tegevust.

Kui valite dokumendi tüübi **Mis tahes**, valitakse suvand **Automaatne tuvastus** väljal **Prindihalduse tegevus** automaatselt kasutaja tegevusena ja toimub järgmine käitumine.

- Kui käitusajal kasutaja tegevuskoodi ei esitata, rakendatakse kõik konfigureeritud ER-i sihtkohad.
- Kui kasutaja tegevuskood käitusajal esitatakse, rakendatakse konkreetse tegevuse jaoks eelmääratletud ER-i sihtkoht, **olenemata sellest, kas see on lubatud**.

    - Kui käitusajal esitatakse tegevus **Kuva**, rakendatakse ER-i sihkoht **Ekraan**.
    - Kui käitusajal esitatakse tegevus **Saada**, rakendatakse ER-i sihkoht **E-post**.
    - Kui käitusajal esitatakse tegevus **Prindi**, rakendatakse ER-i sihkoht **Printer**.

Näiteks saate kasutada ER-vormingut **Vabas vormis arve (Excel)**, et selle sisestamisel printida [vabas vormis arve](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new). Loodud dokumendi marsruutimiseks peate konfigureerima selle ER-vormingu jaoks ER-i sihtkohad. Näiteks peate võib-olla konfigureerima need ER-i sihtkohad, et teha genereeritud dokumendis järgmist.

- Arhiivige dokument, kui ER-vorming on käivitunud, kuid tegevuskoodi pole antud (näiteks dokumendi elektroonilisel saatmisel).
- Kuvage veebibrauseris dokumendi eelvaade, kui kasutaja sooritab tegevuse **Kuva**.
- Arhiivige ja printige dokument, kui kasutaja sooritab tegevuse **Prindi**.
- Arhiivige dokument ja saatke see meiliga väljamineva meilisõnumi manusena, kui kasutaja sooritab tegevuse **Saada**.

Järgmises näites on näidatud, kuidas saavutada seda ER-i sihtkohtade konfigureerimist individuaalsete sihtkoha kirjete komplektina, kui iga kirje konfigureeritakse individuaalse kasutaja tegevuse jaoks.

![Elektroonilise aruandluse sihtleht, kus on tegevusest sõltuvad sihtkoha sätted ER-vormingu jaoks, kui iga sihtkirje on konfigureeritud ühe kasutaja tegevuse jaoks](./media/er-destination-action-dependent-01.png)

Järgmises näites on näidatud, kuidas saavutada samu alternatiivseid ER-i sihtkohtade konfigureerimisi individuaalsete sihtkoha kirjete komplektina, kui iga kirje konfigureeritakse individuaalse sihtkoha jaoks.

![Elektroonilise aruandluse sihtleht, kus on tegevusest sõltuvad sihtkoha sätted ER-vormingu jaoks, kui iga sihtkirje on konfigureeritud ühe sihtkoha jaoks](./media/er-destination-action-dependent-01a.png)

> [!NOTE]
> Kui jooksva ER-vormingu käitamiseks on antud tegevuse kood, kuid selle tegevuskoodi jaoks pole ühtegi sihtkohta konfigureeritud, rakendatakse [vaikimisi](electronic-reporting-destinations.md#default-behavior) sihtkoha käitumist.

## <a name="change-action-dependent-er-destinations-at-runtime"></a>Käitusajal tegevusest sõltuvate ER-i sihtkohtade muutmine

Kui ER-vormingu käitamisel kasutaja tegevused on valmistatud ette kasutaja poolt, kellel on vastavad [õigused](electronic-reporting-destinations.md#security-considerations) konfigureeritud sihtkohasätete muutmiseks käitusajal, kuvatakse dialoogiboks, mis annab võimaluse muuta konfigureeritud sihtkohasätteid. See dialoogiboks on valikuline ja selle ilme sõltub sellest, kuidas on ER-vormingu käitamiseks tehtud ER-ii raamistiku kutsung rakendatud. Selle dialoogiboksi kuvamisel lubatakse ER-i sihtkohad vastavalt esitatud kasutaja tegevusele.

Järgmises näites on toodud dialoogiboksi **Elektroonilise aruandlse vormingu sihtkohad** näide, mis ilmub, kui vabas vomis arve [sisestatakse](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/create-free-text-invoice-new) ja ER-vorming **Vabas vormis arve (Excel)** käitatakse selle dokumendi loomiseks, kui tegevus **Printer** valmistati ette ja ER-i sihtkohad olid selle vormingu jaoks konfigureeritud, nagu varasemalt selles teemas on näidatud.

![Dialoogiboks, mis annab võimaluse muuta täätava ER-vormingu algselt konfigureeritud ER-i sihtkohad](./media/er-destination-action-dependent-02.gif)

> [!NOTE]
> Kui konfigureerisite ER-i sihtkohad mitme töötava ER-vormingu komponendi jaoks, pakutakse valikut eraldi iga ER-vormingu konfigureeritud komponendi jaoks.

## <a name="verify-the-provided-user-action"></a>Esitatud kasutajategevuse kinnitamine

Saate kontrollida, milline kasutaja tegevus (selle olemasolul) käimasoleva ER-vormingu jaoks esitatakse, kui sooritate konkreetse kasutaja tegevuse. See kontroll on oluline, kui peate konfigureerima tegevusest sõltuvaid ER-i sihtkohti, kuid pole kindel, milline on kasutajategevuse kood (kui see on olemas). Näiteks kui hakkate sisestama vabas vormis arvet ja määrate suvandi **Prindi arve** valikule **Jah** dialoogiboksis **Vabas vormis arve sisestamine**, saate määrata suvandi **Kasuta prindihalduse sihtkohta** valikule **Jah** või **Ei**.

Järgige neid samme, et kontrollida esitatud kasutajategevuse koodi.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Dialoogiboksis **Kasutaja parameetrid** [määrake](er-trace-reports-compare-baseline.md#configure-er-parameters-to-use-the-baseline-feature) suvand **Käivita silumisrežiimis** valikule **Jah**.
4. Sooritage kasutaja tegevus ER-vormingut käitades. Pidage meeles, et ER-i kasutaja parameetrid on ettevõttepõhised ja kasutajapõhised.
5. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsiooni silumislogid**.
6. Filtreerige lehel **Konfigureerimise silumislogid** ER-i käitamislogisid, et leida oma ER-vormingu käitamise logi.
7. Vaadake läbi logikirjed, mis peavad sisaldama esitatud kasutajategevuse koodi kirjet, kui ER-vormingu käitamiseks on esitatud mis tahes tegevus.

    ![Elektroonilise aruandluse käitamise logide leht, mis sisaldab teavet kasutajategevuse koodi kohta, mis on esitatud ER-vormingu filtreeritud käituse jaoks](./media/er-destination-action-dependent-03.png)

## <a name=""></a><a name="reports-list-wave1">Äridokumentide loend (voog 1)</a>

Järgmine äridokumentide loend on juhitav funktsiooniga **PM-aruannete väljundi marsruutimine ER-i sihtkohtade põhjal, mis on kasutaja tegevusele spetsiifilised (voog 1)**.

- Kliendiarve (vabas vormis arve)
- Kliendiarve (müügiarve)
- Ostutellimus
- Ostutellimuse ostupäring
- Müügitellimuse kinnitus
- Märgukirjade märkus
- Kliendi kontoväljavõte
- Viivisearve
- Hankija maksesoovitus
- Pakkumiskutse

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)

[Elektroonilise aruandluse raamistiku API muudatused Application update 10.0.17 puhul](er-apis-app10-0-17.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]