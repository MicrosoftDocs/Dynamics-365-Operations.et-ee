---
title: ICMS-DIF-i maksuarvutuste aluse muutus teiste riikide hankijate toodete puhul
description: See teema kirjeldab konfiguratsiooni ICMS-DIF-i maksutüübi arvutuste jaoks, kui fiskaaldokument laekub Brasiilia osariigis Tomati do Sul (RS) või São Mossi (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 63e3cbaaf77456b55f08ea91831ba9d49cb57185
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689152"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>ICMS-DIF-i maksuarvutuste aluse muutus teiste riikide hankijate toodete puhul

See teema kirjeldab **konfiguratsiooni ICMS-DIF-i** maksutüübi arvutuste jaoks, kui fiskaaldokument laekub Brasiilia osariigis Tomati do Sul (RS) või São Mossi (SP).

Vastavalt riikliku seaduse definitsioonile peab kogutav Imposto sobre Toolulação de Mercias e Serviços (ICMS) järgima järgmist reeglit:

*ICMS koguma* = ([(*Toimingu* summa – *ICMS* allikast) ÷ (1 – *ICMS % sisemine*)] × *ICMS % sisemine*) – *ICMS-i summa allikast*

## <a name="example"></a>Näide

Brasiilia ettevõte RS-i osariigis saab finantsdokumendi hankija ostuks SP osariigis. Ettevõte peab koguma ICMS-i protsendierinevuse RS-i osariigi (18 protsenti) ja SP osariigi (12 protsenti) vahel. Alus tuleb siiski arvutada vastavalt eelnevale reeglile.

- **Toimingu summa:** 1000,00 Brasiilia reaali (R$ 1000,00)
- **ICMS-i osariikides:** R$ 120,00
- **ICMS-i protsent RS-i osariigis:** 18 protsenti
- **ICMS-i kogumine RS-i osariigis:** (\[(1000 - 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Lahendus

ICMS-i (ICMS-DIF) arvutamiseks vastavalt RS-i osariigi reeglitele peate seadistama käibemaksukoodid ja käibemaksugrupi järgmisel viisil:

1. Looge käibemaksukood 12-protsendise ICMS-i saamiseks (teise osariigi puhul). Seda koodi kasutatakse hankijalt saadaoleva maksu summa registreerimiseks.
2. Looge käibemaksukood ICMS-DIF-i kogumiseks. Selle käibemaksukoodi protsent peab olema 18 protsenti (teie enda osariigi puhul), et määrata erinevus 18 protsendi ja 12 protsendi vahel. Saate maksutüübiks seada **ICMS-DIF**. See käibemaksukood tuleb arvutamisparameetrites määratleda järgmiselt:

    - Väljal Päritolu **valige** väärtus **Protsent brutosummast**.
    - Väljal Marginaali **alus valige netosumma** rea kohta või **arve** saldo netosumma **.**
    - Määratlege maksustamiskood nii, et selle fiskaalväärtus oleks **3**. Sel viisil luuakse korrigeerimiskanne automaatselt, kui finantsraamatute **moodul** on lubatud.
    - Käibemaksugrupi konfiguratsioonis **valige** **ICMS-DIF-i** käibemaksukoodile valik Kasuta maksu.
