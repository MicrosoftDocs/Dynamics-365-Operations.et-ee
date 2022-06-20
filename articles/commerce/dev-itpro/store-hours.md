---
title: Kaupluse lahtiolekuaegade loomine ja värskendamine
description: Commerce Headquartersis kaupluse tundide loomine ja värskendamine.
author: josaw1
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 99d2f06be959e00656901c6ca8fc79fac32a3a6f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884361"
---
# <a name="create-and-update-store-hours"></a>Kaupluse lahtiolekuaegade loomine ja värskendamine

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Ühest asukohast saavad jaemüüjad luua, hooldada ja hallata erinevate kaupluste lahtiolekuaegu geograafiliste piirkondade lõikes. Kaupluse lahtiolekuajad saab seejärel kuvada müügikoha (POS) terminalis. Sel viisil saavad kassapidajad klientidega jagada kaupluse lahtiolekuaegu ja paremini aidata ostjaid, kes on teistest kaupluste varudest huvitatud. Kaupluse lahtiolekuajad saab printida ka tšekkidele, kui kliendid soovivad hiljem kauplusse naasta.

Erinevate kanalite vahel saab konfigureerida mitu lahtiolekuaega. Need kanalid hõlmavad tellis-ja mördi kauplusi, kõnekeskusi, mobiiliseadmeid ja e-kaubanduse saite.

Kui kliendil on teise kaupluse tellimus, saab kassapidaja valida kuupäevad, millal üleskorje on selles poes saadaval. Kaupluse otsing annab viite kuupäevadele ja kaupluse lahtiolekuaegadele. Kassapidaja saab valida kuupäeva ja asukoha ning printida ka üleskorje kviitungi, mis sisaldab kaupluse lahtiolekuaegu.

See funktsioon on saadaval tarkvara Microsoft Dynamics 365 Retail versioonides 8.1.2 ja uuemad.

## <a name="configure-store-hours"></a>Konfigureeri lahtiolekuaegu

Kaupluse lahtiolekuaegade konfigureerimiseks tehke järgmist.

1. Minge jaotisse **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Lahtiolekuajad**.
2. Valige **Uus**, et luua uus kaupluse lahtiolekuaegade mall. Olemasoleva malli kasutamiseks valige vasakul paneelil mall.
3. Dialoogiaknas **Lisa vahemik** Määratlege kuupäevavahemik, kaupluse lahtiolekuajad ja kõik nõutavad pühad.

    - Kui kaupluse lahtiolekuajad ei muutu, valige **Ei lõpe** väljas **Lõppkuupäev**.
    - Kui kaupluse lahtiolekuajad on kindla kuu, nädala või päeva jaoks, seadke vastavad kuupäevad väljades **Alguskuupäev** ja **Lõppkuupäev**.

    > [!NOTE]
    > Saate luua mitu malli, millel on kattuvad algus-ja lõppkuupäevad. Seetõttu saate erinevate ajavööndite kaupluste lahtiolekuaegu määratleda.

    ![Vahemiku dialoogiakna lisamine.](../dev-itpro/media/Storehours1.png "Vahemiku dialoogiakna lisamine")

4. Seostage kaupluse lahtiolekuaegade mall kauplustega, kus seda kasutatakse. Valige dialoogikastis **Vali organisatsiooni sõlmed** kauplused, regioonid ja organisatsioonid, millega mall peaks seotud olema.

    - Iga kauplusega saab seostada ainult ühe kaupluse lahtiolekuaegade malli.
    - Kasutage noolenuppe, et valida kauplusi, regioone või organisatsioone. Kalender on saadaval kauplustele või kauplusegruppidele ja see on viiteks nähtav kassas.

    ![Organisatsioonisõlmede dialoogiakna valimine.](../dev-itpro/media/Storehours2.png "Organisatsioonisõlmede dialoogiakna valimine")

5. Käivitage lehel **Jaotuse graafik** tööd **1070** ja **1090**, et muuta kaupluse lahtiolekuajad kassas kättesaadavaks.

## <a name="add-store-hours-to-printed-receipts"></a>Kaupluse lahtiolekuaegade lisamine prinditud kviitungitele

Järgige neid samme, et lisada kaupluse lahtiolekuajad prinditud kassa kviitungitele.

1. Avage kviitungi kujundaja.
2. Valige alumises vasakus nurgas **Jalus**.
3. Lohistage element **Kaupluse lahtiolekuajad** vasakul paneelilt jalusesse kviitungi malli allservas.
4. Elemendis saate redigeerida vaikimisi seatud silti **Kaupluse lahtiolekuajad** vastavalt vajadusele.
5. Salvestage kviitung ja sulgege kviitungi kujundaja.
6. Käivitage lehel **Jaotuse graafik** tööd **1070** ja **1090**.
7. Logige kassasse sisse.
8. Lõpetage müük ja valige kviitung printimiseks.

Kassa kviitungid sisaldavad nüüd kaupluse lahtiolekuaegu. Kui malli kaasatakse kõik pühad, kuvatakse need kviitungil.

![Kviitungi näide.](../dev-itpro/media/Storehours3.png "Kviitungi näide")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]