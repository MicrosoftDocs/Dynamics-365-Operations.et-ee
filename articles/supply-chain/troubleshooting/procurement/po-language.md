---
title: Ostutellimustel ei kajastata juriidilise isiku keelesätteid
description: Ostutellimusel kuvatakse toote nimi süsteemikeeles, mitte keeles, mis on määratud juriidilise isiku jaoks, kus ostutellimus loodi
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476109"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Ostutellimustel ei kajastata juriidilise isiku keelesätteid


## <a name="symptoms"></a>Sümptomid

Ostutellimusel kuvatakse toote nimi süsteemikeeles, mitte keeles, mis on määratud juriidilise isiku jaoks, kus ostutellimus loodi.

## <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Seadke süsteemikeeleks *EN-US* (USA inglise keel).
1. Veenduge, et olemas oleks toode, mille nimi on tõlgitud keeltesse *EN-US* ja *DE* (saksa).
1. Muutke juriidilise isiku keeleks *DE*.
1. Looge toodet sisaldav ostutellimus juriidilises isikus, mille keeleks on määratud *DE*.
1. Pange tähele, et toote nimi kuvatakse ikka USA inglise keeles (süsteemikeeles).

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. Ostutellimuste puhul kuvatakse toode alati süsteemikeeles. Ostutellimuse keelt kasutatakse kinnitustöölehe loomisel.
