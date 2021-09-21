---
title: Sertimistee tõrge WMS-i uuendamisel või migreerimisel
description: Kui rakendus kuvab WMS-i uuendamisel või migratsioonil tõrge "Sertifikaaditee usaldusankrut ei leitud", kuvatakse sellel lehel teave probleemi lahendamise kohta.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476094"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>WMS-i värskendamisel ja migreerimisel ei leitud sertifikaaditee usaldusankrut

## <a name="symptoms"></a>Sümptomid

Kui proovite täiendatud laohaldust (WMS) värskendada või migreerida, võib Warehouse Management rakendus teile kuvada järgmise tõrketeate:

> java.security.cert.certPathValidatorException: usaldusankru sertifitseerimise teed ei leitud.

## <a name="cause"></a>Põhjus

See toimub, kuna ise allkirjastatud serdid ei ole usaldusväärsed Android 8+ puhul ettevõttesisestes keskkondades.

## <a name="resolution"></a>Lahendus

Kasutage välist (avaliku) sertifitseerimiskeskust (CA). Selle probleemi parandus on saadaval Warehouse Management rakenduse versioonis 1.9.0.0. Lisateavet selle probleemi ja selle parandamiseks vt [rakenduse ühenduse häälestamisel ei leitud sertifitseerimistee usaldusankrut](certification-path-app-connection-error.md).
