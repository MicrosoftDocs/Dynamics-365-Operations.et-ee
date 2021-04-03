---
title: Elektroonilise arvelduse lisandmooduli kasutamise alustamine Egiptuses
description: Sellest teemast leiate teabe, mis aitab teil Egiptuse elektroonilise arvelduse lisandmoodulit finantshaldamise ja Supply Chain Managementi alal kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592594"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Elektroonilise arvelduse lisandmooduli kasutamise alustamine Egiptuses

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Sellest teemast leiate teabe, mis aitab teil Egiptuse elektroonilise arvelduse lisandmoodulit kasutama hakata. Selle teema protseduurid juhendavad teid riigist sõltuvate konfiguratsioonietappide osas Regulatory Configuration Services (RCS) ja täiendavad teemas kirjeldatud samme, [Alustage elektroonilise arveldamise lisandmooduliga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Egiptuse elektroonilise arveldamise (EG) funktsiooni riigispetsiifiline konfiguratsioon

Egiptuse elektroonilise arve (EG) elektroonilise arvelduse funktsiooni konfigureerimiseks on mõned sammud selle lõpuleviimiseks. Mõned konfiguratsioonide parameetrid avaldatakse vaikeväärtustega, nii et need tuleb läbi vaadata ja uuendada, et teie äritoimingut paremini sobida.

### <a name="prerequisites"></a>Eeltingimused

Enne selle protseduuri lõpetamist, tuleb:

- Looge digitaalserdi saladus, nagu on kirjeldatud **Digitaalse serdi sala loomine** jaotises [Alustage elektroonilise arveldamise lisandmooduli teenuse administratsiooniga](e-invoicing-get-started-service-administration.md). Testimiseks annab Egiptuse maksuamet kindlad testi digitaalsed sertifikaadid, mida tuleb kasutada ainult testimise ja lahenduse valideerimise faasides. Lisateabe saamiseks vaadake Egiptuse maksuameti veebisaiti, kasutades linki [Egiptuse e-arve SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Enne selle jaotise protseduuri sooritamist looge oma ettevõttele Egiptuse elektrooniline arve (EG), nagu on kirjeldatud teemas **"Loo elektroonilise arveldamise funktsiooni oma organisatsiooni pakkuja all** jaotises [Alustage Elektroonilise arveldamise lisandmooduliga](e-invoicing-get-started.md).

1. RCS-is **Funktsioonid** jaotisest **Globaliseerimisfunktsioonid** tööruum valige **Elektroonilise arvelduse lisandmoodul** plaan.
2. Lehel **Elektroonilise arveldamise lisateenused** veenduge, et **Egiptuse elektrooniline arve (EG)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
4. Valige **Häälestus** vahekaardil, ruudustikus **Müügiarve** funktsioon häälestus.
5. Valige **Redigeeri** ja vahekaardil **Tegevused** väljagrupist **Tegevused**, valige **Allkirjasta json Egiptuse maksudokument**.
6. Väljagrupis **Parameetrid** valige parameeter **Serdi nimi** ja valige elektronarvelduse funktsiooniga kasutamiseks loodud nimi elektroonilise arve funktsioonis.
7. Väljagrupis **Tegevused** valige **integreerimine Egiptuse ETA teenusega**. Korrake seda sammu toimingu kahe esinemiskorra puhul.
8. Valige **Parameetrid** väljagrupis **Veebiteenuse URL** ja **Sisselogimise teenuse URL** ning vajadusel vaadake üle URL-i parameetrid. Lisateabe saamiseks vaadake Egiptuse maksuameti veebisaiti, kasutades linki [Egiptuse e-arve SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Valige **Salvesta** ja sulgege leht.
10. Rakenduse häälestuse konfigureerimiseks vt [Alustamine elektroonilise arvelduse lisandmooduliga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Egiptuse elektroonilise arveldamise (EG) funktsiooni riigispetsiifiline konfiguratsioon

**Egiptuse elektroonilise arveldamise (EG)** funktsiooni riigispetsiifiline konfiguratsioon nõuab järgmiste sammude teostamist. Viige need sammud lõpule enne, kui juurutate oma elektroonilise arveldamise funktsiooni oma elektroonilise arvelduse lisandmooduli teenuse keskkonnas.

### <a name="prerequisites"></a>Eeltingimused

Enne selle jaotise protseduuri sooritamist looge oma **Egiptuse elektroonilise arve (EG)** elektroonilise arvelduse funktsioon, et konfigureerida rakenduse **Egiptuse elektrooniline arve (EG)** elektroonilise arveldamise funktsiooni, nagu on kirjeldatud **Konfigureerige rakenduse sätteid** jaotises [Alustage Elektroonilise arveldamise lisandmooduliga](e-invoicing-get-started.md).

1. RCS-is **Funktsioonid** jaotisest **Globaliseerimisfunktsioonid** tööruum valige **Elektroonilise arvelduse lisandmoodul** plaan.
2. Lehel **Elektroonilise arveldamise lisateenused** veenduge, et **Egiptuse elektrooniline arve (EG)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
4. Vahekaardil **Seadistused** valige **rakenduse häälestus** ja **Ühendatud rakendus** väljal, valige rakendus, kuhu soovite juurutada.
5. Kontrollige **Tabeli nimi** väljal, et kliendiarve tööleht on valitud.
6. Valige **Vastuse tüübid** ja seejärel **Uus**.
7. Väljale **Vastuse tüüp** sisestage "Vastus" fikseeritud väärtusena ja väljale **Kirjeldus** sisestage "Kirjeldus".
8. Valige väljal **Edastuse olek** suvand **Ootel**.
9. Väljal **Mudeli kaardistamine** valige **Mudeli vastendamine vastusesõnumist** koos **(Eelvaade) Vastuse sõnumi impordivorming** ja siis valige **Salvesta**.
10. Valige **Uus** ja sisestage siis väljale **Vastusetüüp** väärtus "Vastuse andmed" fikseeritud väärtusena. Väljale **Kirjeldus** sisestage "kirjeldus".
11. Valige väljal **Edastuse olek** suvand **Ootel**.
12. Väljal **andmeüksuse nimi** valige **müügiarve päised V2**.
13. Väljal **Mudeli kaardistamine** valige **Egiptuse vastuse andmete import** koos **(Eelvaade) Egiptuse vastuse andmed** ja siis valige **Salvesta**.
14. Elektroonilise arveldamise funktsiooni juurutamiseks vt [Alustage elektroonilise arvelduse lisandmooduliga](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Privaatsusavaldus

Lubades **Egiptuse elektroonilise arvelduse (EG)** lisandmoodul võib vajada piiratud andmete saatmist, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID. See info edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega. Administraator saab lubada ja keelata funktsiooni avades **Organisatsiooni haldus** > **Seadistus** > **Elektroonilise dokumendi parameetrid**. Valige **Funktsioonid** vahekaart, valige read, mis sisaldavad **Egiptuse elektroonilise arve (EG)** lisandmoodul ning seejärel tehke sobiv valik. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse lisandmooduli ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md)
- [Kliendi elektroonilised arved Egiptuses](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
