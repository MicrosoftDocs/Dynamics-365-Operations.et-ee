---
title: Teenusekeskkonna ja ühendatud rakenduste konfigureerimine
description: See teema annab teavet, kuidas konfigureerida oma teenuse keskkondi ja ühendatud rakendusi.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c3366e75b4a6d3f33a1aac9e444236d9ae57c829
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371864"
---
# <a name="configure-service-environments-and-connected-applications"></a>Teenusekeskkonna ja ühendatud rakenduste konfigureerimine

[!include [banner](../includes/banner.md)]

See teema annab teavet, kuidas konfigureerida oma teenuse keskkondi ja ühendatud rakendusi. Selles protsessis on kolm sammu. 1. etapp on kohustuslik ning sammud 2 ja 3 on valikulised.

## <a name="step-1-create-a-service-environment"></a>1. etapp: teenusekeskkonna loomine

Kui loote oma teenuskeskkonna, määratlege loend kasutajatest, kes saavad juurutada globaliseerimisfunktsioonid. Soovi korral määrake mõne stsenaariumi jaoks väliste rakenduste loend, mis võivad suhelda elektroonilise arveldamise teenusega. Seadistage numbriseeriad, kui kasutate neid oma stsenaariumides.

Selle sammu lõpuleviimiseks vt teenuse [keskkondi](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2. etapp: lisage tunnistused ja saladused

Lisage viide võtme hoidlale Microsoft Azure ja saladustele nende kasutamiseks oma stsenaariumides. See samm on kohustuslik, kui müügivõimaluste töötlemistegevused kasutavad serte ja saladusi digitaalallkirjas kasutamiseks või väliste veebiteenustega suhtlemiseks.

Selle sammu lõpuleviimiseks vt kliendi [serte ja saladusi](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>3. etapp: ühendatud rakenduste konfigureerimine

Kommunikatsiooni Dynamics 365 Finance Dynamics 365 Supply Chain Management ja rakenduste vahelise ja elektroonilise arveldamise häälestamiseks peate konfigureerima finants- või tarneahelahalduse, et koostada kõne elektroonilise arveldamise teenusele ja valmistada äriandmed ette ühtses struktuuris, mida saab nõutud elektroonilisele vormingule edastada. Avaldused peavad teenuse vastused korrektselt töötlema. Selle konfiguratsiooni saate lõpetada otse oma finantside või tarneahela halduskeskkonnas või viia selle lõpule Regulatiivse konfiguratsiooni teenuses (RCS). Kui lõpetate konfiguratsiooni RCS-s, saate selle seejärel juurutada oma finantside või tarneahela haldamise keskkonda. Selles etapis registreerite ühendatud rakenduse parameetri juurutamiseks.

Selle sammu lõpuleviimiseks vaadake ühendatud [rakendusi](e-invoicing-connected-applications.md).
