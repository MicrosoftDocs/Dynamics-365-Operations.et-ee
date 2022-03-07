---
title: Veebitegevuse sündmuste kogumisest loobumine
description: See teema selgitab, kuidas saate lubada veebisaidi külastajatel loobuda rakenduses Microsoft Dynamics 365 Commerce veebitegevuse sündmuste kogumisest.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d71a184b541f243ccc23914ac2e7c663e5ba61be0a27cf8d41e368fe6a384b9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729826"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Veebitegevuse sündmuste kogumisest loobumine
[!include [banner](includes/banner.md)]

See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce veebitegevuse sündmuste kogumisest.

Dynamics 365 Commerce võimaldab saidi administraatoritel analüüsida oma e-kaubanduse saitide kasutajate tegevust veebis. Seeläbi mõistavad nad paremini, kuidas nende saite kasutatakse ja saavad optimeerida saite, et need pakuksid täiustatud kasutuskogemust ja täidaksid ärieesmärke.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Administraatorite loobumiskogemuse rakendamise viisid

Administraatoritel on loobumiskogemuse rakendamiseks kolm viisi.

### <a name="opt-out-on-behalf-of-users"></a>Kasutajate nimel loobumine

Commerce’i peakontori (HQ) kontohalduses saavad administraatorid loobuda kasutajate nimel.

1. Otsige üles ja valige klient HQ-kliendi lehel **Kõik kliendid**.
1. Määrake kliendi üksikasjade lehe kiirkaardi **Jaemüük** jaotises **Privaatsus** suvandi **Ära jälgi veebitegevust** väärtuseks **Jah**.

    ![Privaatsussätted.](media/Disablepersonalizationpart2.png)

1. Valige **Salvesta** ja sulgege seejärel leht.

### <a name="module-based-opt-out-experience"></a>Moodulipõhine loobumise kogemus

Administraatorid saavad lubada autenditud kasutajatel loobuda ise veebitegevuse sündmuste kogumisest. Selle loobumiskogemuse pakkumiseks lisage kasutaja loobumise moodul konto profiili lehtedele.

### <a name="custom-extensions"></a>Kohandatud laiendid

Administraatorid saavad luua oma laiendid, et hallata kasutajate loobumise kogemust. Lisateavet vt [Jaemüügiserveri API-de kutsumine](e-commerce-extensibility/call-retail-server-apis.md) ja [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
