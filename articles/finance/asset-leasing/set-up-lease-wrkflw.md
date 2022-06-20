---
title: Rendi kinnitamise töövoogude seadistamine
description: Artikkel selgitab, kuidas seadistada kinnitamise töövoogu, mida käitatakse uue rendi loomisel.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0162e559f8aaec248cfb9042b0152788536c9fc9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870274"
---
# <a name="set-up-lease-approval-workflows"></a>Rendi kinnitamise töövoogude seadistamine

[!include [banner](../includes/banner.md)]

Artikkel selgitab, kuidas seadistada kinnitamise töövoogu, mida käitatakse uue rendi loomisel. Lisateavet töövoo kasutamise kohta vaadake jaotisest [Rendilepingu kinnitamise töövoogude kasutamine](use-create-lease-wrkflw.md). 

1. Avage **Vara rentimine \> Seadistus \> Rendi töövoog**.
2. Valige lehel **Rendi töövoog** suvand **Uus**.
3. Kuvatavas dialoogiaknas valige jaotises **Töövoo tüüp** link **Rendi töövoog**.

    Rakendus avatakse. Pärast selle käitamist logige sisse rakendusse Azure Active Directory (Azure AD) ja teid suunatakse ümber töövoo rakendamise juurde.

4. Lohistage element **Rendi töövoo kinnitamine** töövoogu.
5. Ühendage üks sõlm üksusest **Algus** üksusega **Rendi töövoo kinnitamine**. Seejärel ühendage **Rendi töövoo kinnitamine** üksusega **Lõpp**.
6. Topeltklõpsake käsku **Rendi töövoo kinnitamine**.
7. Valige **Atribuudid** ja seejärel sisestage jaotises **Põhisätted** töövoole nimi.

    Sellel lehel saate seadistada töövoole ka rohkem parameetreid. Kui olete aktiveerinud **Automaatsed tegevused**, teeb süsteem automaatselt teatud toiminguid. Teatisi saab saata, kui need on määratletud vahekaardil **Teatised**. Vahekaardil **Täpsemad seaded** saate määrata lõpliku kinnitaja, määrata ajalimiidi ja määrata konkreetsed tegevused, mis tuleb lõpule viia.

8. Kui olete töövoo parameetrite määramise lõpetanud, valige käsk **Sule**.
9. Valige **1. etapp** ja seejärel valige **Atribuudid**.
10. Sisestage jaotises **Põhisätted** etapile nimi, looge kinnitamiseks teemarida ja määratlege kinnitamise juhendid.
11. Valige lehel **Määramine** määramise tüüp.
12. Kinnitamisele kindlate kasutajate määramiseks valige **Kasutaja**, valige rentimisi kinnitavad kasutajad ja seejärel valige **Sule**.
13. Töövoo loomiseks valige **Salvesta ja sule**. Seejärel, kui teilt küsitakse, valige **OK**.
14. Valige lehel **Loo töövoog** suvand **Sule**.
14. Valige uus töövoog ja seejärel valige **Versioonid**. Tagamaks, et töövoog oleks aktiivne, valige **Tee aktiivseks**.
15. Valige suvand **Sule**. Kuvatakse uus aktiivne versioon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
