---
title: Konteineri kaalu ja mahu lisamine laadimisel
description: See artikkel kirjeldab, kuidas seadistada ja rakendada funktsioone konteineri kaalu ja mahu kaasamiseks koormatele.
author: Weijiesa
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66dc84171f8b175476f37f736489d3d83cacfe57
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897396"
---
# <a name="include-container-weight-and-volume-on-load"></a>Konteineri kaalu ja mahu lisamine laadimisel

[!include [banner](../includes/banner.md)]

Koormatele konteineri kaalu ja mahu lisamise funktsioon kajastab täpselt koormatesse minevate konteinerite ja kaupade kogukaalu ning -mahtu.

Koormas on üks või mitu saadetist ja neis saadetistes on eraldi kaubad, mis kuuluvad ühte või mitmesse müügitellimusse. Kaubad ladustatakse konteinerisse ja konteineris laaditakse koormasse. Ka väljaspool konteinerit olevad kaubad võivad koorma hulka kuuluda. Nende tingimuste põhjal arvutab süsteem koorma kaalu ja mahu väärtused, arvestades nii konteinerite kui ka kaupade kaalu ja mahtu.

Kui arvutatud väärtused ei ole täpsed, saate neid kohandada, sisestades koorma kaalu ja mahu tegelikud väärtused. Kaalu ja mahu väärtusi kasutatakse transpordihalduse protsessides. Näiteks kasutatakse väärtusi määra marsruudi töölaual, kus need aitavad määratleda koormate määra ja marsruudi ning neid kasutatakse ka transpordi maksevahendite ja juhi sisseregistreerimise puhul.

## <a name="where-it-applies"></a>Kus see kehtib

Konteineri kaalu ja mahu lisamine koormale rakendub transpordihalduse protsessides, nt määra marsruudi töölaual, transpordi maksevahendite ja juhi sisseregistreerimise puhul.

## <a name="how-it-is-set-up"></a>Kuidas see seadistatakse

Koorma puhul arvestatav konteinerite arv arvutatakse konteineri kaalu ja mahu ning konteineri kasutamise protsendi alusel.

-   Konteineri kaalu ja mahu määramiseks klõpsake valikuid **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteineritüübid**.

-   Konteineri kasutamise protsendi seadistamiseks klõpsake valikuid **Laohaldus** \> **Seadistus** \> **Konteinerid** \> **Konteinerigrupid** ja sisestage siis väärtus väljale **Konteineri kasutamise protsent**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]