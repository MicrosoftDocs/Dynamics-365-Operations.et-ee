---
title: Elektroonilise arvelduse lisandmooduli kasutamise alustamine Egiptuses
description: See teema pakub teavet, mis aitab teil alustada elektroonilise arveldusega Egiptuses Finants ja Supply Chain Management -is.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f6175a50a88d2d636bfafc5988265b8657630758
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840192"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Elektroonilise arvelduse lisandmooduli kasutamise alustamine Egiptuses

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Sellest teemast leiate teabe, mis aitab teil alustada elektroonilise arveldusega Egiptuses. See teema juhatab teid läbi riigist sõltuvate konfiguratsioonietappide Regulatory Configuration Services (RCS) ja täiendab teemas kirjeldatud samme [Alustage elektroonilise arveldamisega](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Egiptuse elektroonilise arveldamise (EG) funktsiooni riigispetsiifiline konfiguratsioon

Mõned parameetrid **Egiptuse elektroonilise arve (EG) Elektroonilise arvelduse funktsioonist** avaldatakse vaikeväärtustega. Vaadake üle ja vajadusel uuendage väärtusi, et need sobiksid paremini teie äritegevuse vajadustega, enne kui juurutate elektroonilise arveldamise funktsiooni teenuse keskkonda.

See jaotis täiendab **Elektroonilise arveldamise riigispetsiifilist funktsiooni** jaotist teemas [Alusta elektroonilise arveldusega](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Eeltingimused

Enne selle protseduuri lõpetamist, tuleb:

- Looge digitaalsertifikaadi saladus, nagu on kirjeldatud **Digitaalse sertifikaadi saladuse loomine** jaotises [Alustage elektroonilise arveldamise lisandmooduli teenuse administratsiooniga](e-invoicing-get-started-service-administration.md). Testimiseks annab Egiptuse maksuamet kindlad testi digitaalsed sertifikaadid, mida tuleb kasutada ainult testimise ja lahenduse valideerimise faasides. Lisateabe saamiseks vaadake Egiptuse maksuameti veebisaiti, kasutades linki [Egiptuse e-arve SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus** .
2. Lehel **Elektroonilise arveldamise lisateenused** veenduge, et **Egiptuse elektrooniline arve (EG)** on valitud loodud elektroonilise arveldamise funktsioon.
3. Vahekaardil **Versioon** kontrollige, et oleks valitud versioon **Mustand**.
4. Valige **Häälestus** vahekaardil, ruudustikus **Müügiarve** funktsioon häälestus.
5. Valige **Redigeeri** ja vahekaardil **Tegevused** väljagrupist **Tegevused**, valige **Allkirjasta json Egiptuse maksudokument**.
6. Väljagrupis **Parameetrid** valige parameeter **Serdi nimi** ja valige elektronarvelduse funktsiooniga kasutamiseks loodud nimi elektroonilise arve funktsioonis.
7. Väljagrupis **Tegevused** valige **integreerimine Egiptuse ETA teenusega**. Korrake seda sammu toimingu kahe esinemiskorra puhul.
8. Valige **Parameetrid** väljagrupis **Veebiteenuse URL** ja **Sisselogimise teenuse URL** ning vajadusel vaadake üle URL-i parameetrid. Lisateabe saamiseks vaadake Egiptuse maksuameti veebisaiti, kasutades linki [Egiptuse e-arve SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Valige **Salvesta** ja sulgege leht.
10. Elektroonilise arveldamise funktsiooni juurutamiseks Teenusse keskkonda vt [Alustage elektroonilise arvelduse lisandmooduliga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Egiptuse elektroonilise arveldamise (EG) funktsiooni riigispetsiifiline konfiguratsioon

Viige need sammud lõpule enne rakenduse häälestuse juurutamist ühendatud finants- või Supply Chain Management rakendusse.

See jaotis täiendab **Rakenduse seadistamise riigispetsiifilist funktsiooni** jaotist teemas [Alusta elektroonilise arveldusega](e-invoicing-get-started.md).

1. RCS-i jaotises **Funktsioonid** tööruumis **Globaliseerimisfunktsioonid** valige paan **Elektrooniline arveldus** .
2. Lehel **Elektroonilise arveldamise Funktsioon** veenduge, et **Egiptuse elektrooniline arve (EG)** on valitud loodud elektroonilise arveldamise funktsioon.
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
14. Rakenduse seadistuse juurutamiseks finants- või Supply Chain Management -iga seotud rakendusse vt [Alustamine elektroonilise arveldamisega](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Privaatsusavaldus

Lubades **Egiptuse elektroonilise arvelduse (EG)** lisandmoodul võib vajada piiratud andmete saatmist, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID. See info edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega. Administraator saab lubada ja keelata funktsiooni avades **Organisatsiooni haldus** > **Seadistus** > **Elektroonilise dokumendi parameetrid**. Valige **Funktsioonid** vahekaart, valige read, mis sisaldavad **Egiptuse elektroonilise arve (EG)** lisandmoodul ning seejärel tehke sobiv valik. Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132). Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise arvelduse ülevaade](e-invoicing-service-overview.md)
- [Elektroonilise arvelduse lisandmooduli teenusehalduse kasutamise alustamine](e-invoicing-get-started-service-administration.md)
- [Elektroonilise arveldusega alustamine](e-invoicing-get-started.md)
- [Kliendi elektroonilised arved Egiptuses](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
