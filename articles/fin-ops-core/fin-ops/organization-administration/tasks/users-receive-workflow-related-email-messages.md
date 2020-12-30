---
title: Luba kasutajatel töövooga seotud e-kirju vastu võtta
description: Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b7a953ea54286a7e48b392728d2cc9bb2902072
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692814"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Luba kasutajatel töövooga seotud e-kirju vastu võtta

[!include [banner](../../includes/banner.md)]

Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel. Näiteks e-kirju saab saata kasutajatele kui dokumendid on neile määratud kinnitamiseks. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

1. Avage **Navigeerimispaan > Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake **Toimingupaneelil** valikut **Kasutajavalikud**.
4. Klõpsake vahekaarti **Töövoog** . Veenduge, et jaotis **Teatised** on laiendatud. Jaotises **Teatisted** saate määrata, kuidas soovite, et kasutajat teavitatakse töövooga seotud sündmustest.  
5. Valige suvand väljal **Rea kauba töövoo teavitustüüp**.
    - Grupeeritud – reakaupade teatised grupeeritakse üheks meilisõnumiks.
    - Üksik – meilisõnum saadetakse iga rea kauba puhul.  
    - Kui soovite, et kasutaja saaks klientrakenduses teatisi, märkige ruut **Teatiste saatmine meiliga**.  
6. Klõpsake valikut **Salvesta**.
7. Sulgege leht.

> [!NOTE]
> Töövoo meilimallid hangitakse süsteemi meilimallidest või organisatsiooni meilimallidest, sõltuvalt sellest, kas tegemist on süsteemitasandi (mitte ettevõttepõhise) või organisatsioonitasandi (ettevõttepõhise) töövooga.
