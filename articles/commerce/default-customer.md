---
title: Vaikekliendi loomine
description: See teema kirjeldab, kuidas luua vaikeklienti, mida Microsoft Dynamics 365 Commerce'is kanali loomisel kasutada.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993396"
---
# <a name="create-a-default-customer"></a>Vaikekliendi loomine


[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua vaikeklienti, mida Microsoft Dynamics 365 Commerce'is kanali loomisel kasutada.

## <a name="overview"></a>Ülevaade

Kanali loomisel peate sisestama vaikekliendi. Vaikeklienti on lihtne luua pärast kliendigrupi ja kliendi aadressiraamatu loomist.

## <a name="create-a-customer-group"></a>Kliendigrupi loomine

Kui ühtegi kliendigruppi pole veel olemas, saate selle luua. Näiteks võib tuua erinevaid kliendigruppe esindavad grupid, nagu näiteks hulgimüük, jaemüük, internet, töötajad, jne.

Kliendigrupi loomiseks tehke järgmist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kliendid \> Kliendigrupid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Kliendigrupp** kliendigrupi ID.
1. Sisestage väljale **Kirjeldus** sobiv kirjeldus.
1. Sisestage väljale **Maksetingimused** sobiv väärtus.
1. Sisestage väljale **Aeg arve tähtaja ja maksekuupäeva vahel** sobiv väärtus.
1. Sisestage väljale **Vaikemaksugrupp** maksugrupp, kui see on kohaldatav.
1. Valige märkeruut **Hinnad sisaldavad käibemaksu**, kui see on kohaldatav.
1. Sisestage väljale **Vaikimisi mahakandmise põhjus** sobiv väärtus, kui see on kohaldatav.

Järgmine pilt näitab mitmeid konfigureeritud kliendigruppe.

![Kliendigrupid](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Kliendi aadressiraamatu loomine

Klient peab olema aadressiraamatuga seotud. Kui seda pole veel loodud, peate selle looma.

Kliendi aadressiraamatu loomiseks toimige järgmiselt.

1. Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Aadressiraamatud**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage nimi väljale **Nimi**.
1. Sisestage kirjeldus väljale **Kirjeldus**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab aadressiraamatu näidet.

![Aadressiraamat](media/address-book.png)

## <a name="create-a-default-customer"></a>Vaikekliendi loomine

Vaikekliendi loomiseks tehke järgmist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kliendid \> Kõik kliendid**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige ripploendist **Tüüp** valik "Isik".
1. Valige ripploendist **Kliendi konto** või sisestage sinna kontonumber (näiteks "100001").
1. Valige ripploendist **Eesnimi** nimi või sisestage see (näiteks "Vaikimisi").
1. Valige ripploendist **Teine eesnimi**, või sisestage see (näiteks "Jaemüük").
1. Valige ripploendist **Perekonnanimi** nimi, või sisestage see (näiteks "Klient").
1. Valige või sisestage ripploendisse **Valuuta** valuuta (näiteks "USD").
1. Valige ripploendist **Valuuta** eelnevalt loodud kliendigrupp.
1. Valige ripploendist **Aadressiraamatud** olemasolev kliendi aadressiraamat.
1. Valige **Salvesta**, et salvestada ja naasta kliendi üksikasjade ekraanile uue kliendi jaoks.

> [!NOTE]
> Vaikekliendile ei ole vaja aadressi lisada.

Järgmine pilt näitab kliendi loomise näidet.

![Vaikekliendi loomine](media/default-customer-creation.png)

Järgmine pilt näitab vaikekliendi konfiguratsiooni.

![Kliendi konfiguratsiooni näide](media/default-customer-configuration1.png)

Enamik kliendiandmete kuva vaikeväärtusi võib jääda, kuid muuta tuleb kaht väärtust.

1. Laiendage kliendiandmete kuval jaotist **Müügitellimuse vaikesätteid**.
1. Valige või sisestage ripploendis **Sait** eelkonfigureeritud sait.
1. Valige või sisestage ripploendis **Ladu** eelkonfigureeritud ladu.

Järgmine pilt näitab kliendi konfiguratsiooni näidet.

![Kliendi konfiguratsiooni näide](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)
