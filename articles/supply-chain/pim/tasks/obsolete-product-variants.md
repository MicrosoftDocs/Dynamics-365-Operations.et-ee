---
title: Aegunud tootevariantide leidmine
description: Protseduur näitab, kuidas leida aegunud väljastatud tooteid või tootevariante ja kuidas seostada toote elutsükli olek aegunud toodetega.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b212a6b4268776893d4e018cab605e6441080fa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986850"
---
# <a name="find-obsolete-product-variants"></a>Aegunud tootevariantide leidmine 

[!include [banner](../../includes/banner.md)]

Protseduur näitab, kuidas leida aegunud väljastatud tooteid või tootevariante ja kuidas seostada toote elutsükli olek aegunud toodetega. Eelnõue: peate määratlema vähemalt ühe toote elutsükli oleku, mis on planeerimise jaoks passiivne, enne kui saate selle ülesande juhendit esitada.


## <a name="run-a-simulation"></a>Simulatsiooni käivitamine
1. Avage jaotis Tooteteabe haldus > Perioodilised ülesanded > Aegunud toodete elutsükli oleku muutmine.
2. Väljal Uue toote elutsükli olek sisestage või valige väärtus.
3. Valige Jah väljal Simulatsiooni käivitamine toote andmeid värskendamata.
4. Sisestage arv väljale Selle arvu päevade jooksul loodud toodete välistamine.
5. Sisestage arv väljale Kannetes kasutatud toodete välistamine (päevade arv).
6. Jaotise kaasamiseks laiendage kirjeid.
7. Klõpsake käsku Filtreeri.
8. Märkige loendis valitud rida.
9. Sisestage väärtus väljale Kriteeriumid.
10. Klõpsake nuppu OK.
11. Klõpsake nuppu OK.

> [!NOTE]
> Soovitatav on käitada simulatsiooni partiina, kui plaanite otsida suurt hulka tooteid. Veenduge ka, et simulatsiooni ei käitataks ettevõtte kõige aktiivsemal tööajal.  

## <a name="review-the-simulation-results"></a>Simulatsiooni tulemuste ülevaatamine
1. Avage jaotis Tooteteabe haldus > Päringud ja aruanded > Toote elutsükli oleku haldamise ajalugu.
   
> [!NOTE]
> Sellel lehel saate üle vaadata simulatsiooni tulemused ja hinnata, kui palju tooteid ning tootevariante uue toote elutsükli olekuga seostatakse, kui värskendus käivitatakse ilma simulatsioonita.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Aegunud toodete elutsükli oleku värskenduse käitamine
1. Sulgege leht.
2. Avage jaotis Tooteteabe haldus > Perioodilised ülesanded > Aegunud toodete elutsükli oleku muutmine.
3. Jaotise kaasamiseks laiendage kirjeid.

> [!NOTE]
> Pange tähele, et viimane valik on salvestatud.  

4. Valige Ei väljal Simulatsiooni käivitamine toote andmeid värskendamata.
5. Laiendage jaotist Käivita taustal.

> [!NOTE]
> Olenevalt mõjutatud toodete ja tootevariantide arvust kaaluge toimingu käitamist pakett-tööna. Veenduge, et te ei käitaks suurt värskendustööd ettevõtte kõige aktiivsemal tööajal.  

6. Klõpsake nuppu OK.
7. Avage jaotis Tooteteabe haldus > Päringud ja aruanded > Toote elutsükli oleku haldamise ajalugu.

> [!NOTE]
> Vaadake üle muudetud väljastatud tooted ja tootevariandid.  

8. Otsige loendist ja valige soovitud kirje.

