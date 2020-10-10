---
title: Tõrke haldamine
description: Selles teemas kirjeldatakse varahalduse tõrke haldust.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 72d6c8d750a5a0903017b4c77b3ce5d9521cf99b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889357"
---
# <a name="fault-management"></a>Tõrke haldamine

[!include [banner](../../includes/banner.md)]

 

Varahalduses saate vara tüüpides seadistada tõrke sümptomeid, tõrke valdkondi ja tõrke tüüpe tõrke kujundajaga. Nii saate hallata varades tuvastatavaid tõrkeid. Lisaks saab tõrgete põhjuseid ja nende lahendamissoovitusi registreerida töökäsus.

Tõrke registreerimine ja haldamine sisaldab neid etappe.

1. Looge loend vara tüüpides esineda võivatest tõrke sümptomitest, tõrke valdkondadest ja tõrke tüüpidest.
2. Tõrke kujundajas seadistage tõrke sümptomeid, tõrke valdkondi ja tõrke tüüpe.

Siin on paar näidet, mis aitavad eristada tõrke sümptomeid, tõrke valdkondi ja tõrke tüüpe.

**Tõrke sümptomid:**

- tasakaalustamata pinged;
- lühis;
- Müra
- leke;
- vibratsioonid.

**Tõrke valdkonnad:**

- elektriline;
- mehhaaniline;
- hüdrauliline;
- pneumaatiline.

**Tõrke tüübid:**

- vigane üldstaatori mähis;
- vigane diood;
- mustad mähised;
- vigane generaator;
- vigane andur.

## <a name="create-fault-symptoms"></a>Looge rikkesümptomid

Järgige neid etappe, et luua loend tõrke kujundajas kasutatavatest sümptomitest.

1. Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke sümptomid**.
2. Valige **Uus**, et luua uus kirje.
3. Sisestage välja **Tõrke sümptom** tõrke sümptomi nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige käsk **Salvesta**.

## <a name="create-fault-areas"></a>Looge rikkevaldkonnad

Järgige neid etappe, et luua loend tõrke kujundajas kasutatavatest valdkondadest või asukohtadest.

1. Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke valdkonnad**.
2. Valige **Uus**, et luua uus kirje.
3. Sisestage välja **Tõrke valdkond** tõrke valdkonna nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige käsk **Salvesta**.

## <a name="create-fault-types"></a>Looge tõrke tüübid

Järgige neid etappe, et luua loend tõrke kujundajas kasutatavatest tõrke tüüpidest.

1. Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke tüüpidest**.
2. Valige **Uus**, et luua uus kirje.
3. Sisestage välja **Tõrke tüüp** tõrke tüübi nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige käsk **Salvesta**.

## <a name="set-up-the-fault-designer"></a>Seadistage tõrke kujundaja

Tõrke kujundajas seadistate vara tüüpide tõrke andmed.

1. Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke kujundaja**.
2. Valige vasakus paanis vara tüüp, et seadistada selle tõrke kannet.
3. Kiirkaardil **Tõrke sümptom** valige **Lisa rida** ja seejärel valige väljas **Tõrke sümptom** tõrke sümptom.
4. Kiirkaardil **Tõrke valdkond** valige **Lisa rida** ja seejärel valige väljas **Tõrke valdkond** tõrke valdkond.
5. Kiirkaardil **Tõrke tüüp** valige **Lisa rida** ja seejärel valige väljas **Tõrke tüüp** tõrke tüüp.
6. Valitud vara tüübi kõikide olemasolevate tõrke sümptomite, valdkondade ja tüüpide kombinatsioonide kiireks loomiseks valige **Looge tõrke kombinatsioonid**. Sellest on kasu siis, kui olete lisanud palju tõrke sümptomeid, valdkondi ja tüüpe. Lihtsam on kustutada vara tüübiga mitte seotud mistahes kombinatsioonide ridu kui luua ise uusi ridu.

    > [!NOTE]
    > Tõrke sümptomite, valdkondade ja tüüpide seadete kopeerimiseks ühest vara tüübist valitud vara tüüpi valige **Kopeeri vara tüübist**.

7. Oma muudatuste salvestamiseks valige **Salvesta**.

![Tõrke kujundaja leht](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a>Looge tõrke põhjused

Järgige neid etappe, et luua loend teadaolevatest tõrke põhjustest, mida saab lisada töökäsku või hooldusnõudesse.

1. Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke põhjused**.
2. Valige **Uus**, et luua uus kirje.
3. Sisestage välja **Tõrke põhjus** tõrke põhjuse nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige käsk **Salvesta**.

## <a name="create-fault-remedies"></a>Looge tõrkelahendusi

Järgige neid etappe, et luua loend lahenduse ja paranduse soovitustest, mida saab lisada töökäsku või hooldusnõudesse.

1. Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke lahendused**.
2. Valige **Uus**, et luua uus kirje.
3. Sisestage välja **Tõrke lahendus** tõrke lahenduse nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige käsk **Salvesta**.

> [!NOTE]
> Saate vajadusel muuta tõrke sümptomite, valdkondade, tüüpide, põhjuste ja lahenduste nimesid. Nime muutused kajastuvad automaatselt vastavates tõrke registreerimistes.
