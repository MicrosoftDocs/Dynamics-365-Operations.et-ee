---
title: Teenusekeskkondade ja ühendatud rakenduste konfigureerimine
description: See artikkel annab teavet, kuidas konfigureerida oma teenuse keskkondi ja ühendatud rakendusi.
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
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853218"
---
# <a name="configure-service-environments-and-connected-applications"></a>Teenusekeskkondade ja ühendatud rakenduste konfigureerimine

[!include [banner](../includes/banner.md)]

See artikkel annab teavet, kuidas konfigureerida oma teenuse keskkondi ja ühendatud rakendusi. Selles protsessis on kolm sammu. 1. etapp on kohustuslik ning sammud 2 ja 3 on valikulised.

## <a name="step-1-create-a-service-environment"></a>1. etapp: teenusekeskkonna loomine

Kui loote oma teenuskeskkonna, määratlege loend kasutajatest, kes saavad juurutada globaliseerimisfunktsioonid. Soovi korral määrake mõne stsenaariumi jaoks väliste rakenduste loend, mis võivad suhelda elektroonilise arveldamise teenusega. Seadistage numbriseeriad, kui kasutate neid oma stsenaariumides.

Selle sammu lõpuleviimiseks vt teenuse [keskkondi](e-invoicing-service-environments.md).

## <a name="step-2-add-certificates-and-secrets"></a>2. etapp: lisage tunnistused ja saladused

Lisage viide võtme hoidlale Microsoft Azure ja saladustele nende kasutamiseks oma stsenaariumides. See samm on kohustuslik, kui müügivõimaluste töötlemistegevused kasutavad serte ja saladusi digitaalallkirjas kasutamiseks või väliste veebiteenustega suhtlemiseks.

Selle sammu lõpuleviimiseks vt kliendi [serte ja saladusi](e-invoicing-customer-certificates-secrets.md).

## <a name="step-3-configure-connected-applications"></a>3. etapp: ühendatud rakenduste konfigureerimine

Dynamics 365 Dynamics 365 Supply Chain Management Finantside või rakenduste ja elektroonilise arveldamise vahelise kommunikatsiooni häälestamiseks peate konfigureerima finants- või tarneahelahalduse, et koostada kõne elektroonilise arveldamise teenusele ja valmistada äriandmed ette ühtses struktuuris, mida saab ülendada nõutud elektroonilisele vormingule. Avaldused peavad teenuse vastused korrektselt töötlema. Selle konfiguratsiooni saate lõpetada otse oma finantside või tarneahela halduskeskkonnas või viia selle lõpule Regulatiivse konfiguratsiooni teenuses (RCS). Kui lõpetate konfiguratsiooni RCS-s, saate selle seejärel juurutada oma finantside või tarneahela haldamise keskkonda. Selles etapis registreerite ühendatud rakenduse parameetri juurutamiseks.

Selle sammu lõpuleviimiseks vaadake ühendatud [rakendusi](e-invoicing-connected-applications.md).
