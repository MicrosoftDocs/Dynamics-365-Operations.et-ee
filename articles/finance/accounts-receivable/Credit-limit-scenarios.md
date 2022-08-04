---
title: Krediidilimiidi stsenaariumid
description: See artikkel kirjeldab, kuidas kontrollitakse kliendi krediidilimiiti, kui klient kuulub kliendi krediidilimiidi gruppi.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130271"
---
# <a name="credit-limit-scenarios"></a>Krediidilimiidi stsenaariumid

Krediidihalduses saab kliendile klienditasemel määrata krediidilimiidi. Iga kliendi saab määrata kliendi krediidilimiidi *gruppi ja* igal grupil on krediidilimiit. Seetõttu saab krediidilimiiti määrata ka klientidele grupitasemel. Kõigil samale kliendi krediidigrupile määratud klientidel on sama krediidilimiit.

Üldiselt kontrollitakse grupi krediidilimiite enne üksikuid krediidilimiite. Individuaalne krediidilimiit ei alista alati grupi krediidilimiiti.

See artikkel kirjeldab viit stsenaariumi, mis on seotud kliendi krediidigruppide ja individuaalsete krediidilimiitdega.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Kliendigrupi krediidilimiit on suurem kui üksik krediidilimiit

Näiteks on kliendil kliendil individuaalne krediidilimiit $10,000. Klient on määratud kliendi krediidigruppi ja grupi krediidilimiiti $15,000. Sellisel juhul on kliendi "tegelik krediidilimiit" $10,000, sest see summa on väiksem kui grupi limiit. Blokeerimisreeglid kontrollivad esmalt grupi limiiti. Seejärel kontrollivad nad üksikut limiiti. Iga müügitellimused $10,000 blokeeritud.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Individuaalne krediidilimiit on suurem kui kliendigrupi krediidilimiit

Kliendil on näiteks kliendi krediidilimiit $20,000. Klient on määratud kliendi krediidigruppi ja grupi krediidilimiiti $15,000. Sel juhul kehtestatakse kliendi tegelik krediidilimiit $15,000, kuna blokeerimisreeglid kontrollivad alati grupi limiiti esimesena. Kõik üle $15,000 müügitellimused blokeeritakse.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Üksiku krediidilimiidi väärtuseks on seatud 0,00 ja kohustuslikuks krediidilimiidiks on määratud Jah.

**Kui kliendil on individuaalne krediidilimiit, mis on seatud väärtusele 0,00** ja **·** **Kohustusliku** krediidilimiidi valik on Jah, siis on kliendi tegelik krediidilimiit $0.00, isegi kui klient on määratud kliendi krediidigruppi. Sel viisil saab klient gruppi kuuluda, kuid kõik tellimused lähevad krediidihaldusse.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Individuaalseks krediidilimiidiks on seatud 0,00 ja piiramatu krediidilimiit on seatud väärtusele Jah.

Kui kliendil **on individuaalne krediidilimiit, mis on seatud väärtusele 0,00**, **·** **kuid piiramatu krediidilimiidi valik on Jah**, on kliendil piiramatu krediit, isegi kui ta on määratud kliendi krediidigrupile.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Individuaalseks krediidilimiidiks on seatud 0,00 ja klient on osa kliendi krediidigrupist

Näiteks on kliendil individuaalse **krediidilimiidi väärtuseks seatud 0,00**,**·** **piiramatu krediidi valikuks on Määratud Ei** **ja** kohustuslikuks krediidilimiidiks on seatud **Ei.** Klient on määratud kliendi krediidigruppi ja grupi krediidilimiiti $15,000. Sellisel juhul on kliendi tegelik krediidilimiit grupi limiit, $15,000. Seetõttu blokeeritakse kõik seda summat ülevad müügitellimused. Selline käitumine võimaldab krediidilimiiti hallata kliendi krediidigrupi tasemel, mitte kliendi tasemel. Kõigil samasse gruppi määratud klientidel on sama krediidilimiit.
