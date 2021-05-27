---
title: Aruande tühistamine lõpetatuna loob ootamatu avatud kande
description: Märgistusega lõppenud aruandluse tühistamine loob avatud tehingu, kus vastupidisel kogusel on samad varude mõõtmed kui vastupidisel tehingul.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026451"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Aruande tühistamine lõpetatuna loob ootamatu avatud kande

KB number: 4612469

## <a name="symptoms"></a>Sümptomid

Märgistusega lõppenud aruandluse tühistamine loob avatud tehingu, kus vastupidisel kogusel on samad varude mõõtmed kui tühistatud tehingul.

## <a name="resolution"></a>Eraldusvõime

Kui tühistate aruande kui lõpetatud toimingu, lähtestatakse tootmisdokumentatsioonist varude mõõde. Seetõttu lähtestatakse partiinumber. Märkimise tõttu pärivad müügitellimuse kanded partiinumbri.

Dimensiooni saab lähtestada, kui sisestatakse lõpetatuna kinnitamine.
