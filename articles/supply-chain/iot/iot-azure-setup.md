---
title: Azure'i ressursside seadistamine IoT iseõppimisvõime jaoks
description: Selles teemas selgitatakse, kuidas luua ja konfigureerida Microsoft Azure'i ressursse, mida vajate IoT iseõppimisvõime jaoks.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 722904aa75a9d95b99c83f39a1d79b9c796714b3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821101"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>Azure'i ressursside seadistamine IoT iseõppimisvõime jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas luua ja konfigureerida Microsoft Azure'i ressursse, mida vajate IoT iseõppimisvõime jaoks.

## <a name="create-azure-resources"></a>Azure'i ressursside loomine

Järgige neid juhiseid, et luua IoT-keskus, Redis-vahemälu ja võtmehoidla, millele pääseb juurde Microsoft Dynamics 365 Supply Chain Managementiga.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Kinnitage, et teie rentnikus on Microsoft Dynamics ERP mikroteenuste esimese osapoole rakenduse ID

Järgige neid juhiseid, et kinnitada, kas teie rentnikus on Microsoft Dynamics ERP mikroteenuste esimese osapoole rakenduse ID.

1. Logige sisse Azure’i portaali lehel<https://portal.azure.com>.
2. Avage **Azure Active Directory**.
3. Avage **Ettevõtte rakendused**.
4. Valige väljal **Rakenduse tüüp** suvand **Microsofti rakendused**.
5. Sisestage otsinguväljale **Microsoft Dynamics ERP mikroteenused**.
6. Kinnitage, et loendis oleksid **Microsoft Dynamics ERP mikroteenused**. Teiste rakenduste nimed on sarnased. Seetõttu veenduge, et leiaksite õige rakenduse. Rakenduse ID on **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Kui rakendust ei ole loendis, peate lisama selle oma rentnikusse.

    1. Valige Azure'i portaali tööriistaribal nupp Azure Cloud Shelli avamiseks.
    2. Käivitage käsk **Install-Module AzureAD**. Sisestage mooduli installimiseks **Y**.
    3. Käivitage käsk **Get-InstalledModule -Name "AzureAD"**, et kinnitada, kas moodul on installitud.
    4. Käivitage käsk **Connect-AzureAD -Confirm** autentimise käivitamiseks.
    5. Käivitage käsk **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Saate nüüd korrata etappe 1–6, et kinnitada, kas rakenduse ID on teie rentnikus.

### <a name="create-a-key-vault-resource"></a>Võtmehoidla ressursi loomine

Võtmehoidla ressursi loomiseks tehke järgmist.

1. Looge või avage ressursi grupp Azure'i portaalis.
2. Valige **Lisa**.
3. Sisestage lehel **Uus** otsinguväljale **Võtmehoidla**. Seejärel valige **Loo**.
4. Sisestage lehel **Võtmehoidla loomine** nimi väljale **Võtmehoidla nimi**.
5. Vaadake vaikeväärtused üle ja seejärel valige **Ülevaatamine ja loomine**.
6. Valige **Loo**.

Võtmehoidla luuakse taustal.

### <a name="create-an-iot-hub-resource"></a>IoT-keskuse ressursi loomine

IoT-keskuse ressursi loomiseks tehke järgmist.

1. Looge või avage ressursigrupp.
2. Valige **Lisa**.
3. Sisestage lehel **Uus** otsinguväljale **IoT-keskus**. Seejärel valige **Loo**.
4. Sisestage nimi väljale **IoT-keskuse nimi**.
5. Vaadake vaikeväärtused üle ja seejärel valige **Ülevaatamine ja loomine**.
6. Valige **Loo**.

IoT-keskus luuakse taustal.

> [!NOTE]
> Soovitame luua ainult ühe IoT-keskuse ressurssi keskkonna kohta.

### <a name="create-a-redis-cache-resource"></a>Redis-vahemälu ressursi loomine

Redis-vahemälu ressursi loomiseks tehke järgmist.

1. Looge või avage ressursigrupp.
2. Valige **Lisa**.
3. Sisestage lehel **Uus** otsinguväljale **Azure'i vahemälu Redise jaoks**. Seejärel valige **Loo**.
4. Väljale **DNS-i nimi** sisestage nimi.
5. Vaadake vaikeväärtused üle ja seejärel valige **Loo**.

Redis-vahemälu luuakse taustal.

> [!NOTE]
> Soovitame luua ainult ühe Redis-vahemälu ressurssi keskkonna kohta.

Kõik ressursid on nüüd loodud.

## <a name="configure-the-azure-resources"></a>Azure'i ressursside konfigureerimine

### <a name="configure-the-iot-hub"></a>IoT-keskuse konfigureerimine

IoT-keskuse konfigureerimiseks tehke järgmist.

1. Valige oma ressurssides IoT-keskuse ressurss.
2. Valige vasakpoolsel navigeerimispaanil **Sisseehitatud lõpp-punktid**.
3. Kleepige jaotisesse **Tarbijagrupid** järgmised tarbijagrupid. Need tarbijagrupid vastavad valmislahenduse stsenaariumidele.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Võtmehoidla konfigureerimine

Võtmehoidla konfigureerimiseks tehke järgmist.

1. Valige oma ressurssides võtmehoidla ressurss.
2. Valige vasakpoolselt navigeerimispaanilt suvand **Juurdepääsupoliitikad**.
3. Valige **Lisa juurdepääsupoliitika**.
4. Valige lehel **Lisa juurdepääsupoliitika** väljal **Salajased load** suvand **Hangi** ja **Loend**.
5. Klõpsake suvandit **Subjekti valimine**.
6. Otsige üles ja valige dialoogiboksis **Subjekt** suvand **Microsoft Dynamics ERP mikroteenused**. Seejärel valige **Vali**.
7. Valige **Lisa**.
8. Valige käsk **Salvesta**.

Rakendusel on nüüd juurdepääs võtmehoidla saladustele.

### <a name="save-the-iot-hub-connection-string-secret"></a>IoT-keskuse ühenduse stringi saladuse salvestamine

IoT-keskuse ühenduse stringi saladuse salvestamiseks toimige järgmiselt.

1. Valige oma ressurssides IoT-keskuse ressurss.
2. Valige vasakpoolsel navigeerimispaanil **Sisseehitatud lõpp-punktid**.
3. Kopeerige väärtus väljale **Sündmuste keskusega ühilduv lõpp-punkt**.
4. Avage võtmehoidla ressurss.
5. Valige vasakpoolsel navigeerimispaanil suvand **Saladused**.
6. Valige **Loo/impordi**.
7. Väljale **Nimi** sisestage nimi.
8. Kleepige väljale **Väärtus** lõpp-punkti väärtus, mille eelnevalt kopeerisite.
9. Valige **Loo**.

### <a name="save-the-redis-cache-connection-string-secret"></a>Redis-vahemälu ühenduse stringi saladuse salvestamine

Redis-vahemälu ühenduse stringi saladuse salvestamiseks toimige järgmiselt.

1. Valige oma ressurssides Redis-vahemälu ressurss.
2. Valige **Juurdepääsuvõtmed**.
3. Kopeerige väärtus väljajalt **Peamine ühenduse string**.
4. Avage võtmehoidla ressurss.
5. Valige vasakpoolsel navigeerimispaanil suvand **Saladused**.
6. Valige **Loo/impordi**.
7. Väljale **Nimi** sisestage nimi.
8. Kleepige väljale **Väärtus** ühenduse string, mille eelnevalt kopeerisite.
9. Valige **Loo**.

> [!NOTE]
> Kui värskendate ühte neist ühenduse stringidest, peate värskendama ka salajasi väärtusi.

Olete nüüd lõpetanud nõutavate Azure'i ressursside ettevalmistamise. Järgmine etapp on [IoT iseõppimisvõime lisandmooduli installimine teenuses Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]