---
title: Kontrollige topeltkirjutuse konfiguratsiooni Finance and Operationsi rakendustes ja Dataverse’is
description: Selles teemas selgitatakse, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakendustes ja Dataverse'is.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 361d6555b60e02832c337b6f416b2b3627b6d365
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129303"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Kontrollige topeltkirjutuse konfiguratsiooni Finance and Operationsi rakendustes ja Dataverse’is

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige selgitab see, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakendustes ja Dataverse'is.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Kontrollimine, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakenduses

Selleks, et teha kindlaks, kas ridade värskenduse salvestamisel kuvatavad tõrketeated on põhjustatud topeltkirjutusest, kontrollige esmalt, kas topeltkirjutus on konfigureeritud.

+ Kui teil on administraatori privileegid rakenduses Finance and Operations, avage jaotis **Tööruumid \> Andmehaldus** ja valige paan **Topeltkirjutus**. Kui kuvatakse lingitud keskkondade üksikasjad ja kasutatava tabeli vastenduste loend, konfigureeritakse topeltkirjutus.

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide korral](media/verify_fin_ops_1.png)

+ Kui teil ei ole administraatori privileege, kuvatakse tõrketeade *Andmeid ei saa kirjutada üksusele \<entity name\>*. Järgmises näites kirjeldatakse, et rakenduses Finance and Operations ei saa kliendi rida luua, sest topeltkirjutus on konfigureeritud, kuid kliendigruppi ja maksetingimuste viiteandmeid pole teenuses Dataverse olemas.

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide puudumise korral](media/verify_fin_ops_2.png)

Lisateavet selle kohta, kuidas lahendada probleeme rakenduses Finance and Operations andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Kontrollimine, kas topeltkirjutus on konfigureeritud Dataverse'is

Kui andmete loomisel kuvatakse Dataverse’i lehtedel veerg **Ettevõte**, on topeltkirjutus konfigureeritud.

![Dataverse'i ühenduse kontrollimine](media/verify_cds.png)

Lisateavet selle kohta, kuidas lahendada probleeme Dataverse'is andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).

Lisateavet selle kohta, kuidas vaadata tõrke üksikasju, kui Dataverse'is andmete loomisel ilmneb tõrkeid, vaadake teemast [Dataverse'is lisandmooduli jälituslogi lubamine ja kuvamine tõrke üksikasjade vaatamiseks](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]