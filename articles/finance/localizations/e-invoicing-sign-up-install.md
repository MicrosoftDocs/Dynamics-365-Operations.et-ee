---
title: Registreerige elektroonilise arve teenus ja installige see
description: See artikkel annab teavet selle kohta, kuidas registreerida ja installida elektroonilise arvelduse teenust.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283953"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Registreerige elektroonilise arve teenus ja installige see

[!include [banner](../includes/banner.md)]

See artikkel annab teavet selle kohta, kuidas registreerida ja installida elektroonilise arvelduse teenust. Selles protsessis on neli sammu. Juhised 1–3 on kohustuslikud ja 4. etapp on valikuline.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>1. etapp: regulatiivse konfiguratsiooniteenuse konfigureerimine

Konfiguratsiooniteenus (RCS) pakub konfiguratsiooni ja kujunduskogemust, mida kasutatakse elektroonilise arveldamise konfigureerimiseks. Ressursid, nt keskkonnad ja elektroonilise arveldamise funktsioonid, luuakse, hallatakse ja hallatakse RCS-s. Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse teenuses.

Lisateavet RCS-i kohta vt regulatiivsete [konfiguratsiooniteenuste (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).

RCS-ile registreerumiseks minge lehele Regulatiivse [konfiguratsiooni](https://marketing.configure.global.dynamics.com/) teenus.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>2. etapp: installige lisandmoodulid mikroteenustele elutsükli Microsoft Dynamics teenustes.

Elektroonilise arveldamise teenus on Microsofti andmekeskustes majutatud mikroteenuste kogum. Dynamics 365 Finance’i klientidel Dynamics 365 Supply Chain Management ei ole vaikimisi juurdepääsu elektroonilise arveldamise teenusele. Peate selle installima lisandmoodulina elutsükli Microsoft Dynamics teenustes (LCS). Kui installite lisandmooduli, registreeritakse teie finantside või tarneahela halduskeskkond rakenduste registris, mis võivad ühenduda elektroonilise arveldamise teenusega.

Selle etapi lõpuleviimiseks vt [installige mikroteenuste lisandmoodul elutsükli teenustes](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>3. etapp: RCS-i seadistamine

Peate seadistama integratsiooni RCS-i ja elektroonilise arvelduse teenuse vahel. Samuti peate seadistama põhikomponendid.

Selle etapi lõpuleviimiseks vt Seadistage [regulatiivne konfiguratsiooniteenus (RCS).](e-invoicing-set-up-rcs.md)

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>4. etapp: Microsoft Power Platform lisandmooduli administraatori viide

Mõned stsenaariumid nõuavad integratsiooni Dataverse selle ulatusega Microsoft Power Platform.

Praegu on see seadistus kohustuslik, kui kasutate Elektroonilise arvelduse lahendusi Indoneesia elektroonilise arvelduse stsenaariumite jaoks. Saudi Araabia elektroonilise arvelduse stsenaariumite jaoks on see siiski valikuline. Lisateavet vt jaotisest Elektroonilise [arveldamise funktsioonide saadavus riikide või piirkondade kaupa](e-invoicing-country-specific-availability.md).

Selle sammu lõpuleviimiseks vaadake lisandmooduli [Microsoft Power Platform administraatori viidet](e-invoicing-power-platform-plug-in.md).
