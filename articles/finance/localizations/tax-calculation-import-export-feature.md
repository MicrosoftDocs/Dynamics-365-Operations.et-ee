---
title: Impordi ja ekspordi maksuarvutused
description: Selles teemas antakse teavet maksuarvestuse teenuse impordi ja ekspordi kohta.
author: Kai-Cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 76ea99510455e984d94a93d87ee788fdcf00c376
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891355"
---
# <a name="import-and-export-tax-calculations"></a>Impordi ja ekspordi maksuarvutused

Selles teemas antakse teavet maksuarvestuse teenuse impordi ja ekspordi kohta. See funktsioon aitab tagada paindliku ja tõhusa konfiguratsioonikogemuse.

## <a name="import-and-export-tax-codes"></a>Impordi ja ekspordi maksukoodid

### <a name="export-templates"></a>Ekspordi mallid

1. Logige sisse [regulatiivsesse konfiguratsiooniteenusesse (RCS)](https://marketing.configure.global.dynamics.com/).
2. **Globaliseerimisfunktsiooni** tööruumis valige **Funktsioonid ja seejärel valige maksu arvutamise** **paani**.
3. Valige olemasolev funktsioon või [looge uus](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) funktsioon.
4. Valige **ruudustikus** Versioonid suvand **Redigeeri**.
5. Seadke **maksuarvestuse** funktsiooni lehel [konfiguratsiooni](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) versioon.
6. Valige vahekaardil **Maksukoodid** suvand **Impordi**.
7. Valige **maksukoodi malli** eksportimine, et laadida **alla fail TaxCodesTemplate.zip.**
8. Eemalda **TaxCodesTemplate.zip.** Maksukoodi mallid tihendatakse eraldi vastavalt arvutuse **päritolu** väärtusele.
9. Eemaldage fail **netosumma.zip** abil, et saada järgmised komaga eraldatud väärtuste (CSV) failid:

    - **TaxCode.csv** – sisestage maksukoodid.
    - **TaxLimit.csv** – sisestage maksulimiidid igale maksukoodile.
    - **TaxRate.csv** – sisestage maksumäärad igale maksukoodile.

> [!NOTE]
> Vaikimisi on näidismaksu koodi **kirjed** mallides saadaval. Kui **näidismaksukoodi** ei eemaldata CSV-failidest, imporditakse see funktsiooni.

### <a name="import-tax-codes"></a>Impordi maksukoodid

Järgige neid samme **mallis maksu** näidiskoodi importimiseks oma maksuarvestuse funktsiooni.

1. Valige RCS-i **maksuarvutuse** funktsiooni lehel vahekaardil **Maksukoodid** suvand **Impordi**.
2. Valige **sirvimisfail**, otsige ja valige fail TaxCode.csv ning seejärel **valige** **sihttabeli** väljal **Maksukood**.
3. Valige **maksukoodi** importimiseks OK.
4. Otsige ja valige **fail TaxRate.csv ning seejärel valige sihttabeli väljal** **·** **Maksumäär**.
5. Valige **impordimaksumäära** importimiseks OK.
6. Otsige ja valige **fail TaxLimit.csv** ning seejärel valige **väljalt Sihttabel suvand** **Maksupiirang.**
7. Maksulimiidi **importimiseks** valige OK.

Saate importida ka otse sihtfaili, mis sisaldab kõiki kolme CSV-faili. Sel viisil saate importi kiiresti ja hõlpsasti lõpule viia.

1. Valige RCS-i **maksuarvutuse** funktsiooni lehel vahekaardil **Maksukoodid** suvand **Impordi**.
2. Valige **Sirvi**, leidke ja valige **fail Netosumma.zip** ning seejärel valige **OK**.

### <a name="export-tax-codes"></a>Ekspordi maksukoodid

1. Valige RCS-i **maksuarvutuse** funktsiooni lehel vahekaardil **Maksukoodid** suvand **Ekspordi**.

    Nupp **Ekspordi** on saadaval, kui maksukoodide ruudustikus on **vähemalt üks** maksukood.

2. Valige **OK**, et eksportida kõik sihtfaili funktsiooni maksukoodid.

> [!NOTE]
> Kasutage eksporditud faili mallina, et importida maksukoodid vastavasse funktsiooni.

## <a name="import-and-export-applicability-rules"></a>Impordi ja ekspordi kohaldatavusreeglid

### <a name="export-applicability-rules"></a>Ekspordi kohaldatavusreeglid

1. Logige teenusesse [RCS](https://marketing.configure.global.dynamics.com/) sisse.
2. **Globaliseerimisfunktsiooni** tööruumis valige **Funktsioonid ja seejärel valige maksu arvutamise** **paani**.
3. Valige olemasolev funktsioon või [looge uus](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) funktsioon.
4. Valige **ruudustikus** Versioonid suvand **Redigeeri**.
5. Seadke **maksuarvestuse** funktsiooni lehel [konfiguratsiooni](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs) versioon.
6. Vahekaardil **Maksugrupi kohaldatavus** valige read maksugrupi kohaldatavusruudustikus **Häälesta**.
7. Valige nupp **Ava ja seejärel valige Microsoft Office** maksuteenuse dünaamilise **kohaldatavusmaatriks.**

    [![Kohaldatavusreeglite Microsoft Excel eksportimine maksuarvestuse funktsiooni lehel](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Valige **laadi** alla, et eksportida valitud read Microsoft Excel töölehele.

### <a name="import-applicability-rules"></a>Impordi kohaldatavusreeglid

Allalaaditud Exceli tööleht sisaldab maksugrupi **kohaldatavusruudustiku häälestamise** struktuuri. Uusi reegleid saate lisada otse töölehele. Kui olete lõpetanud, järgige neid samme uute reeglite tagasi importimiseks maksugrupi **kohaldatavusruudustikku.**

1. Valige ja kopeerige Exceli töölehel impordivad read.
2. Valige RCS-i maksuarvutuse funktsiooni lehel vahekaardil Maksugrupi kohaldatavus suvand Lisa, et lisada tühi kirje maksugrupi **kohaldatavusruudustiku** **·** **·** **allosas**.
3. Kopeeritud **ridade** kleepimiseks ruudustikku valige klahv Ctrl+V.
4. Valige käsk **Salvesta**.
