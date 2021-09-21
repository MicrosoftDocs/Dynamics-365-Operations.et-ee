---
title: Lõpetamata täiendustöö tõttu blokeeritud komplekteerimistöö
description: Komplekteerimise töö võib olla blokeeritud sõltuva täiendamistöö tõttu. Lõpetage täiendamise töö ja seejärel töödelge komplekteerimise töö.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476166"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Komplekteerimise töö ei saa olla blokeeritud lõpetamata täiendamistöö tõttu

## <a name="symptoms"></a>Sümptomid

Voo nõudluse tõttu täiendamist kasutades saab komplekteerimistöö sõltuva täiendustöö tõttu blokeerida. Kui kasutate voo nõudluse täiendamist, kui komplekteerimise asukoht tuleb komplekteerida, et täita allika tellimuse nõudlust, loob süsteem nii täiendamise töö kui ka komplekteerimise töö. Kuid see blokeerib komplekteerimistöö seni, kuni täiendustöö on lõpule viidud ja saate järgmise tõrketeate:

> Töö %1 blokeeringut ei saa tühistada, sest selles on lõpetamata täiendustöid.

## <a name="resolution"></a>Lahendus

See käitumine on tahtlik, sest komplekteerimise asukohas ei ole piisavalt varusid, kui täiendamise töö on lõpule viidud. Lõpetage täiendamise töö ja seejärel töödelge komplekteerimise töö.
