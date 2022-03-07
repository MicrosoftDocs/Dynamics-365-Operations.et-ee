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
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714206"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Aruande tühistamine lõpetatuna loob ootamatu avatud kande

KB number: 4612469

## <a name="symptoms"></a>Sümptomid

Märgistusega lõppenud aruandluse tühistamine loob avatud tehingu, kus vastupidisel kogusel on samad varude mõõtmed kui tühistatud tehingul.

## <a name="resolution"></a>Eraldusvõime

Kui tühistate aruande kui lõpetatud toimingu, lähtestatakse tootmisdokumentatsioonist varude mõõde. Seetõttu lähtestatakse partiinumber. Märkimise tõttu pärivad müügitellimuse kanded partiinumbri.

Dimensiooni saab lähtestada, kui sisestatakse lõpetatuna kinnitamine.
