---
title: TDS-i arvutamine arvetel
description: Selles teemas antakse viide kannetele, mille puhul arvestatakse mahamakstud maks allikas (TDS) arve tasemel.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: faf381458fec27e3140579486485d89bb81dfd4c2eae2d60f906c69491009f4c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780358"
---
# <a name="tds-calculation-on-invoices"></a>TDS-i arvutamine arvetel

[!include [banner](../includes/banner.md)]

Selles teemas antakse viide kannetele, mille puhul arvestatakse mahamakstud maks allikas (TDS) arve tasemel.

| Seerianumber | Kande tüüp                                 | Kandesumma | Lehe nimi ja valiku tee                                 | Konto tüüp ja vastaskonto tüüp                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Ost on tehtud hankijalt / kirjendamiskulud   | Deebet või kreedit  | Üldiste töölehtede leht (Pearaamat > Töölehe kirjed > Üldised töölehed), Arvete kinnitamise töölehe leht (Ostureskontro > Arved > Arve kinnitamine), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Pearaamat (Dr) Hankija (Kr.).  Kinnipeetav maks arvutatakse hankija-pearaamatu kombinatsiooni puhul ainult juhul, kui pearaamatukonto sisestustüüp **Ost** **Sulara**. |
| 2.            | Ost on tehtud hankijalt / kirjendamiskulud | Deebet või kreedit  | Pearaamatute leht (Pearaamat > Töölehe sisestused > Üldised töölehed), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Pearaamat (Dr) Klient (Kr.)                                 |
| 3.            | Põhivara ost hankijalt              | Deebet või kreedit  | Üldiste töölehtede leht (Pearaamat > Töölehe kirjed > Üldised töölehed), Arvete kinnitamise töölehe leht (Ostureskontro > Arved > Arve kinnitamine), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Põhivarad (Dr) Hankija (Kr.)                             |
| 4.            | Põhivara ost kliendilt            | Deebet või kreedit  | Pearaamatute leht (Pearaamat > Töölehe sisestused > Üldised töölehed), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Põhivarad (Dr) Klient (Kr.)                           |
| 5.            | Ostuarve (TDS-i kohustus)                  |                    | Ostuarve leht (Maksekontod > Ostutellimused > Kõik ostutellimused) |                                                              |
| 6.            | Müügiarve (TDS-i saadaolev)                  |                    | Müügitellimuse leht (Müügireskontro > Tellimused > Kõik müügitellimused), Vabas vormis arve leht (Müügireskontro > Arved > Kõik vabas vormis arved) |                                                              |
