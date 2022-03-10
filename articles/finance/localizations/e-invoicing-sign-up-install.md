---
title: Registreerige elektroonilise arve teenus ja installige see
description: See teema annab teavet selle kohta, kuidas registreerida ja installida elektroonilise arvelduse teenust.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ab16652e4a50dd71a5d0b2b49b4dd79e327f7a8
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371869"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Registreerige elektroonilise arve teenus ja installige see

[!include [banner](../includes/banner.md)]

See teema annab teavet selle kohta, kuidas registreerida ja installida elektroonilise arvelduse teenust. Selles protsessis on neli sammu. Juhised 1–3 on kohustuslikud ja 4. etapp on valikuline.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>1. etapp: regulatiivse konfiguratsiooniteenuse konfigureerimine

Konfiguratsiooniteenus (RCS) pakub konfiguratsiooni ja kujunduskogemust, mida kasutatakse elektroonilise arveldamise konfigureerimiseks. Ressursid, nt keskkonnad ja elektroonilise arveldamise funktsioonid, luuakse, hallatakse ja hallatakse RCS-s. Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse teenuses.

Lisateavet RCS-i kohta vt regulatiivsete [konfiguratsiooniteenuste (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).

RCS-ile registreerumiseks minge lehele Regulatiivse [konfiguratsiooni](https://marketing.configure.global.dynamics.com/) teenus.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>2. etapp: installige lisandmoodulid mikroteenustele elutsükli Microsoft Dynamics teenustes.

Elektroonilise arveldamise teenus on Microsofti andmekeskustes majutatud mikroteenuste kogum. Vaikimisi on elektronarvelduse Dynamics 365 Finance Dynamics 365 Supply Chain Management teenusel klientidele ja neil ei ole juurdepääsu sellele. Peate selle installima lisandmoodulina elutsükli Microsoft Dynamics teenustes (LCS). Kui installite lisandmooduli, registreeritakse teie finantside või tarneahela halduskeskkond rakenduste registris, mis võivad ühenduda elektroonilise arveldamise teenusega.

Selle etapi lõpuleviimiseks vt [installige mikroteenuste lisandmoodul elutsükli teenustes](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>3. etapp: RCS-i seadistamine

Peate seadistama integratsiooni RCS-i ja elektroonilise arvelduse teenuse vahel. Samuti peate seadistama põhikomponendid.

Selle etapi lõpuleviimiseks vt Seadistage [regulatiivne konfiguratsiooniteenus (RCS).](e-invoicing-set-up-rcs.md)

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>4. etapp: Microsoft Power Platform lisandmooduli administraatori viide

Mõned stsenaariumid nõuavad integratsiooni Dataverse selle ulatusega Microsoft Power Platform.

Praegu on see seadistus kohustuslik, kui kasutate Elektroonilise arvelduse lahendusi Indoneesia elektroonilise arvelduse stsenaariumite jaoks. Saudi Araabia elektroonilise arvelduse stsenaariumite jaoks on see siiski valikuline. Lisateavet vt jaotisest Elektroonilise [arveldamise funktsioonide saadavus riikide või piirkondade kaupa](e-invoicing-country-specific-availability.md).

Selle sammu lõpuleviimiseks vaadake lisandmooduli [Microsoft Power Platform administraatori viidet](e-invoicing-power-platform-plug-in.md).
