---
title: Algse kontsernisisese müügitellimuse muutmine või kustutamine
description: See artikkel selgitab algse müügitellimuse funktsiooni muutmist ja kustutamist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6ff7eeb00fec7c1b9fa1dc08fa231669f728ed3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859073"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Algse kontsernisisese müügitellimuse muutmine või kustutamine

[!include [banner](../../includes/banner.md)]

Müügitellimust muutes teie muudatused sünkroonitakse automaatselt kontsernisisese ostutellimuse ja müügitellimusega.

> [!NOTE]
> Muudatused ei mõjuta välishankijate ostutellimusi, samuti pole algsed müügiread seotud välishankijate ostutellimuse ridadega.

Järgmises tabelis võetakse kokku muudatused, mida saate teha ja eeldatavad tulemused.

| Toiming | Tulemus |
|---|---|
| Algse&nbsp;&nbsp;&nbsp;müügitellimuse &nbsp;kustutamine. | Samuti kustutatakse seonduv kontsernisisene ostu- ja müügitellimus. Müügitellimust ei ole võimalik kustutada, kui tellimuse olek on **Komplekteerimisleht** või kui tellimus on töötlemisel. |
| Algse müügitellimuse rea kustutamine. | Kustutatakse sellega seonduv kontsernisisese ostutellimuse rida ja müügitellimuse rida. Müügitellimuste rida ei ole võimalik kustutada, kui tellimuse olek on **Komplekteerimisleht** või kui tellimus on töötlemisel. |
| Algsele müügitellimusele uue rea lisamine. | Uus müügirida luuakse nii kontsernisisesel ostutellimusel kui ka müügitellimusel. |
| Koguse muutmine algse müügitellimuse real. | Kogus sünkroonitakse kontsernisisese ostu- ja müügitellimuse real oleva kogusega. Netosumma arvutatakse kõigi tellimuste puhul ümber. |
| Otsetarnete keelamine algsel müügitellimusel. | Kui kontsernisisese müügitellimuse rea olekuks on **Komplekteerimisleht**, **Väljaminekuorder** või **Komplekteerimislehe tööleht**, ei saa algsel müügitellimusel **Otsetarne** välja muuta. Kontsernisisese ostutellimuse tarneaadress muudetakse standardseks tarneaadressiks (standardne ostutellimuse tarneaadress). Samuti muudetakse kontsernisisese ostutellimuse read ridade standardseks tarneaadressiks. Mõlemad sünkroonitakse kontsernisisese müügitellimuse ja selle ridadega. Algsel müügitellimusel muudetakse kõigi ridade tarnetüübiks **Pole** ning väli sünkroonitakse kontsernisisese ostutellimuse ja selle ridadega. Välishankijate ostutellimusi ei muudeta ning samuti pole algsed müügiread seotud välishankijate ostutellimuse ridadega. Kontsernisisesel ostutellimusel ja selle ridadel uuendatakse tarnekuupäev ning kontsernisisesel müügitellimusel ja ridadel uuendatakse nõutavad sissetuleku-/lähetuskuupäevad. |
| Otsetarnete lubamine algsel müügitellimusel. | Kui kontsernisisese müügitellimuse rea olekuks on **Komplekteerimisleht**, **Väljaminekuorder** või **Komplekteerimislehe tööleht**, ei saa algsel müügitellimusel **Otsetarne** välja muuta. Kontsernisisese ostutellimuse tarneaadress muudetakse algse müügitellimuse tarneaadressiks ja sünkroonitakse kontsernisisese müügitellimusega. Algsel müügitellimusel muudetakse kõigi ridade tarnetüübiks **Otsetarne** ning väli sünkroonitakse kontsernisisese ostutellimuse ja selle ridadega. Iga algse müügitellimuse rea tarneaadress sünkroonitakse nii kontsernisisese ostutellimuse kui ka müügitellimuse ridadega. Kontsernisisesel ostutellimusel ja selle ridadel uuendatakse tarnekuupäev ning kontsernisisesel müügitellimusel ja ridadel uuendatakse nõutavad sissetuleku-/lähetuskuupäevad. |
| Märkuste lisamine nii algse müügitellimuse päisesse kui ka ridadele. | Märkus kopeeritakse kontsernisisesele ostutellimusele ja müügitellimusele. |
| Märkuste muutmine ja kustutamine. | Märkuse muutmisel või kustutamisel kustutatakse või muudetakse sellele vastav märkus kontsernisisesel ostutellimusel ja müügitellimusel. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
