---
title: TDS-i arvutamine arvetel
description: See artikkel annab viite kannetele, kus allikas mahaarvatud maks (TDS) arvutatakse arve tasemel.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855359"
---
# <a name="tds-calculation-on-invoices"></a>TDS-i arvutamine arvetel

[!include [banner](../includes/banner.md)]

See artikkel annab viite kannetele, kus allikas mahaarvatud maks (TDS) arvutatakse arve tasemel.

| Seerianumber | Kande tüüp                                 | Kandesumma | Lehe nimi ja valiku tee                                 | Konto tüüp ja vastaskonto tüüp                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Ost on tehtud hankijalt / kirjendamiskulud   | Deebet või kreedit  | Üldiste töölehtede leht (Pearaamat > Töölehe kirjed > Üldised töölehed), Arvete kinnitamise töölehe leht (Ostureskontro > Arved > Arve kinnitamine), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Pearaamat (Dr) Hankija (Kr.).  Kinnipeetav maks arvutatakse hankija-pearaamatu kombinatsiooni puhul ainult juhul, kui pearaamatukonto sisestustüüp **Ost** **Sulara**. |
| 2.            | Ost on tehtud hankijalt / kirjendamiskulud | Deebet või kreedit  | Pearaamatute leht (Pearaamat > Töölehe sisestused > Üldised töölehed), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Pearaamat (Dr) Klient (Kr.)                                 |
| 3.            | Põhivara ost hankijalt              | Deebet või kreedit  | Üldiste töölehtede leht (Pearaamat > Töölehe kirjed > Üldised töölehed), Arvete kinnitamise töölehe leht (Ostureskontro > Arved > Arve kinnitamine), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Põhivarad (Dr) Hankija (Kr.)                             |
| 4.            | Põhivara ost kliendilt            | Deebet või kreedit  | Pearaamatute leht (Pearaamat > Töölehe sisestused > Üldised töölehed), Arve töölehe leht (Ostureskontro > Arved > Arve tööleht) | Põhivarad (Dr) Klient (Kr.)                           |
| 5.            | Ostuarve (TDS-i kohustus)                  |                    | Ostuarve leht (Maksekontod > Ostutellimused > Kõik ostutellimused) |                                                              |
| 6.            | Müügiarve (TDS-i saadaolev)                  |                    | Müügitellimuse leht (Müügireskontro > Tellimused > Kõik müügitellimused), Vabas vormis arve leht (Müügireskontro > Arved > Kõik vabas vormis arved) |                                                              |
