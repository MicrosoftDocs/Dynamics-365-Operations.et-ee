---
title: Impordi- ja ekspordimaksude arvutused
description: Selles teemas antakse teavet maksuarvestuse teenuse impordi ja ekspordi kohta.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 02ad47b5f350969b4935a8f383ddf26a7ce7a46a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690886"
---
# <a name="import-and-export-tax-calculations"></a>Impordi- ja ekspordimaksude arvutused

Selles teemas antakse teavet maksuarvestuse teenuse impordi ja ekspordi kohta. See funktsioon aitab tagada paindliku ja tõhusa konfiguratsioonikogemuse.

## <a name="import-and-export-tax-codes"></a>Impordi ja ekspordi maksukoodid

### <a name="export-templates"></a>Ekspordi mallid

1. Logige sisse regulatiivsesse [konfiguratsiooniteenusesse (RCS)](https://marketing.configure.global.dynamics.com/).
2. Globaliseerimisfunktsiooni **tööruumis** valige **Funktsioonid ja** seejärel maksu arvutamise **paani**.
3. Valige olemasolev funktsioon või [looge uus funktsioon](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Versioonide ruudustikus **valige** käsk **Redigeeri**.
5. Seadke maksu **arvutamise** funktsiooni lehel konfiguratsiooni [versioon](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Vahekaardil Maksukoodid **valige** Käsk **Impordi**.
7. Valige **maksukoodi malli eksportimine**, et laadida **alla fail TaxCodesTemplate.zip**.
8. Eemalda TaxCodesTemplate.zip **·**. Maksukoodi mallid tihendatakse eraldi vastavalt arvutuse **päritolu väärtusele**.
9. Eemaldage fail **netosumma.zip abil**, et saada järgmised komaga eraldatud väärtuste (CSV) failid:

    - **TaxCode.csv** – sisestage maksukoodid.
    - **TaxLimit.csv** – sisestage maksulimiidid igale maksukoodile.
    - **TaxRate.csv** – sisestage maksumäärad igale maksukoodile.

> [!NOTE]
> Vaikimisi on näidismaksu koodi **kirjed** mallides saadaval. Kui näidismaksukoodi **ei** eemaldata CSV-failidest, imporditakse see funktsiooni.

### <a name="import-tax-codes"></a>Impordi maksukoodid

Järgige neid samme mallis maksu **näidiskoodi** importimiseks oma maksuarvestuse funktsiooni.

1. Valige RCS-i **maksuarvutuse** funktsiooni lehel vahekaardil **Maksukoodid** suvand **Impordi**.
2. Valige sirvimis-, otsimis- **ja valige fail TaxCode.csv** **ning seejärel valige sihttabeli** väljal **Maksukood**.**·**
3. Valige **maksukoodi importimiseks OK**.
4. Otsige ja valige **fail TaxRate.csv** ning seejärel valige **maksumäär väljalt** Sihttabel **·**.
5. Valige **impordimaksumäära importimiseks OK**.
6. Otsige ja valige **Fail TaxLimit.csv** ning seejärel valige **väljalt** Sihttabel suvand **Maksupiirang**.
7. Maksulimiidi **importimiseks valige OK**.

Saate importida ka otse sihtfaili, mis sisaldab kõiki kolme CSV-faili. Sel viisil saate importi kiiresti ja hõlpsasti lõpule viia.

1. Valige RCS-i **maksuarvutuse** funktsiooni lehel vahekaardil **Maksukoodid** suvand **Impordi**.
2. Valige **sirvimine**, leidke ja valige **fail Netosumma.zip** ning seejärel valige **OK**.

### <a name="export-tax-codes"></a>Ekspordi maksukoodid

1. Valige RCS-i **maksuarvutuse** funktsiooni lehel vahekaardil **Maksukoodid** suvand **Ekspordi**.

    Nupp **Ekspordi** on saadaval, kui maksukoodide ruudustikus on vähemalt **üks maksukood**.

2. Valige **OK**, et eksportida kõik sihtfaili funktsiooni maksukoodid.

> [!NOTE]
> Kasutage eksporditud faili mallina, et importida maksukoodid vastavasse funktsiooni.

## <a name="import-and-export-applicability-rules"></a>Impordi ja ekspordi kohaldatavusreeglid

### <a name="export-applicability-rules"></a>Ekspordi kohaldatavusreeglid

1. Logige teenusesse [RCS](https://marketing.configure.global.dynamics.com/) sisse.
2. Globaliseerimisfunktsiooni **tööruumis** valige **Funktsioonid ja** seejärel maksu arvutamise **paani**.
3. Valige olemasolev funktsioon või [looge uus funktsioon](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Versioonide ruudustikus **valige** käsk **Redigeeri**.
5. Seadke maksu **arvutamise** funktsiooni lehel konfiguratsiooni [versioon](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Vahekaardil Maksugrupi **kohaldatavus** valige read maksugrupi kohaldatavusruudustikus **Häälesta**.
7. Valige nupp **Ava ja Microsoft Office** seejärel valige maksuteenuse dünaamilise **kohaldatavusmaatriks**.

    [![Kohaldatavusreeglite eksportimine Microsoft Excel maksuarvestuse funktsiooni lehel](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Valige **laadi** alla, et eksportida valitud read töölehele Microsoft Excel.

### <a name="import-applicability-rules"></a>Impordi kohaldatavusreeglid

Allalaaditud Exceli tööleht sisaldab maksugrupi kohaldatavusruudustiku **häälestamise struktuuri**. Uusi reegleid saate lisada otse töölehele. Kui olete lõpetanud, järgige neid samme uute reeglite tagasi importimiseks maksugrupi **kohaldatavusruudustikku**.

1. Valige ja kopeerige Exceli töölehel impordivad read.
2. Valige RCS-i maksuarvutuse funktsiooni lehel vahekaardil Maksugrupi kohaldatavus suvand **Lisa**, **et lisada tühi kirje maksugrupi kohaldatavusruudustiku allosas**.**·** **·**
3. Kopeeritud **ridade kleepimiseks ruudustikku valige klahv Ctrl+V**.
4. Valige käsk **Salvesta**.
