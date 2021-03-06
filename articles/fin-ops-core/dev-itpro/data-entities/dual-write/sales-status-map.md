---
title: Müügitellimuse olekuveergude vastendamise seadistamine
description: Selles teemas selgitatakse, kuidas seadistada müügitellimuse olekuveerge topeltkirjutamiseks.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 9afa64df73aa17e7a15a0ee4f4529ac74bcd3c67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750710"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Müügitellimuse olekuveergude vastendamise seadistamine

[!include [banner](../../includes/banner.md)]

Müügitellimuse olekut näitavatel veergudel on rakendustes Microsoft Dynamics 365 Supply Chain Management ja Dynamics 365 Sales erinevad loetelu väärtused. Nende veergude vastendamiseks topeltkirjutamises on vajalik lisaseadistus.

## <a name="columns-in-supply-chain-management"></a>veerud rakenduses Supply Chain Management

Rakenduses Supply Chain Management näitavad müügitellimuse olekut kaks veergu. Veerud, mida peate vastendama, on **Olek** ja **Dokumendi olek**.

Loetelu **Olek** näitab tellimuse üldist olekut. See olek kuvatakse tellimuse päises.

Loetelul **Olek** on järgmised väärtused.

- Avatud tellimus
- Tarnitud
- Arveldatud
- Cancelled

Loetelu **Dokumendi olek** täpsustab kõige hiljutisemat tellimuse jaoks loodud dokumenti. Näiteks kui tellimus on kinnitatud, on see dokument müügitellimuse kinnitus. Kui müügitellimus on osaliselt arveldatud ja seejärel kinnitatakse järelejäänud rida, jääb dokumendi olekuks **Arve**, kuna arve luuakse protsessis hiljem.

Loetelul **Dokumendi olek** on järgmised väärtused.

- Kinnitus
- Komplekteerimisleht
- Saateleht
- Arve

## <a name="columns-in-sales"></a>veerud rakenduses Sales

Rakenduses Sales näitavad tellimuse olekut kaks veergu. Veerud, mida peate vastendama, on **Olek** ja **Töötlemise olek**.

Loetelu **Olek** näitab tellimuse üldist olekut. Sellel on järgmised väärtused.

- Aktiivne
- Edastatud
- Täidetud
- Arveldatud
- Cancelled

Loetelu **Töötlemise olek** võeti kasutusele, et olekut saaks rakendusega Supply Chain Management täpsemini vastendada.

Järgmises tabelis on toodud suvandi **Töötlemise olek** vastendus rakenduses Supply Chain Management.

| Töötlemise olek   | Olek rakenduses Supply Chain Management | Dokumendi olek rakenduses Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Aktiivne              | Avatud tellimus                        | None                                       |
| Kinnitatud           | Avatud tellimus                        | Kinnitus                               |
| Valitud              | Avatud tellimus                        | Komplekteerimisleht                               |
| Osaliselt tarnitud | Avatud tellimus                        | Saateleht                               |
| Tarnitud           | Tarnitud                         | Saateleht                               |
| Osaliselt arvele kantud  | Tarnitud                         | Arve                                    |
| Arveldatud            | Arveldatud                          | Arve                                    |
| Cancelled           | Cancelled                         | Pole kohaldatav                             |

Järgmises tabelis on toodud suvandi **Töötlemise olek** vastendus rakendustes Sales ja Supply Chain Management.

| Töötlemise olek   | Olek rakenduses Sales | Olek rakenduses Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Aktiivne              | Aktiivne          | Avatud tellimus                        |
| Kinnitatud           | Edastatud       | Avatud tellimus                        |
| Valitud              | Edastatud       | Avatud tellimus                        |
| Osaliselt tarnitud | Aktiivne          | Avatud tellimus                        |
| Osaliselt arvele kantud  | Aktiivne          | Avatud tellimus                        |
| Osaliselt arvele kantud  | Täidetud       | Tarnitud                         |
| Arveldatud            | Arveldatud        | Arveldatud                          |
| Cancelled           | Cancelled       | Cancelled                         |

## <a name="setup"></a>Seadistus

Müügitellimuse olekuveergude vastendamise seadistamiseks peate lubama atribuudid **IsSOPIntegrationEnabled** ja **isIntegrationUser**.

Atribuudi **IsSOPIntegrationEnabled** lubamiseks tehke järgmist.

1. Avage brauseris leht `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Asendage **\<test-name\>** oma ettevõtte rakenduse Sales lingiga.
2. Otsige avatud lehel üles **organizationid** ja kirjutage selle väärtus üles.

    ![Väärtuse organizationid leidmine](media/sales-map-orgid.png)

3. Avage rakenduses Sales brauserikonsool ja käivitage järgmine skript. Kasutage sammust 2 pärit üksuse **organizationid** väärtust.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScripti kood brauserikonsoolis](media/sales-map-script.png)

4. Veenduge, et suvandi **IsSOPIntegrationEnabled** väärtuseks oleks seatud **tõene**. Kasutage väärtuse kontrollimiseks sammust 1 pärit URL-i.

    ![Tõeseks seatud IsSOPIntegrationEnabled](media/sales-map-integration-enabled.png)

Atribuudi **isIntegrationUser** lubamiseks tehke järgmist.

1. Valige rakenduses Sales **Sätted \> Kohandamine \> Kohanda süsteemi**, valige **Kasutaja tabel** ja seejärel avage **Vorm \> Kasutaja**.

    ![Kasutaja vormi avamine](media/sales-map-user.png)

2. Leidke väljauurijas üles **Integratsiooni kasutaja režiim** ja topeltklõpsake sellel, et lisada see vormile. Salvestage muudatus.

    ![Integratsiooni kasutaja režiimi veeru lisamine vormile](media/sales-map-field-explorer.png)

3. Valige rakenduses Sales **Sätted \> Turve \> Kasutajad** ja muutke vaade väärtuselt **Lubatud kasutajad** väärtusele **Rakenduse kasutajad**.

    ![Vaate muutmine lubatud kasutajatelt rakenduse kasutajatele](media/sales-map-enabled-users.png)

4. Valige kaks kirjet nimega **DualWrite IntegrationUser**.

    ![Rakenduse kasutajate loend](media/sales-map-user-mode.png)

5. Muutke veeru **Integratsiooni kasutaja režiim** väärtuseks **Jah**.

    ![Integratsiooni kasutaja režiimi veeru väärtuse muutmine](media/sales-map-user-mode-yes.png)

Teie müügitellimused on nüüd vastendatud.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]