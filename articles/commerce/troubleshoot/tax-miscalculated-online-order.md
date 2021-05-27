---
title: Võrgutellimuste maksud on valesti arvutatud
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui võrgutellimuste maksud on valesti arvutatud või kui müügirea maksugrupp pole õigesti seatud.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021099"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Võrgutellimuste maksud on valesti arvutatud

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui võrgutellimuste maksud on valesti arvutatud või kui müügirea maksugrupp pole õigesti seatud.

## <a name="description"></a>Kirjeldus

Kui e-äri tellimus on esitatud, siis on maksud valesti arvutatud või on müügirea maksugrupp valesti seatud.

## <a name="resolution"></a>Eraldusvõime

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Commerce Headquartersi kaupluse käibemaksu konfigureerimine

Commerce Headquarters`i kaupluse käibemaksu konfigureerimine, järgige järgmisi samme.

1. Minge jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kõik kauplused**.
1. Valige kauplus, mille jaoks käibemaksu konfigureerida.
1. Jaotise **Üldine** **Käibemaks** kiirkaardil konfigureerige kaupluse käibemaksuteavet.

> [!NOTE]
> Toote kauplust peale võttes, tuleb maksugrupp kauplusest, mis on valitud peale võtmiseks. Lisateavet vt jaotisest [Kaupluste muude maksuvalikute häälestamine](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Commerce Headquarters`i kaupluse käibemaksu konfigureerimine

Commerce Headquarters`i kaupluse käibemaksu konfigureerimine, järgige järgmisi samme.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Valige klient, kelle jaoks müügitellimus luua.
1. Valige **Aadressi** kiirkaardil aadress, mille jaoks käibemaks konfigureerida, valige suvand **Veel suvandeid** ja seejärel **Täpsem**.
1. Valige vahekaardil **Üldine** kiirkaart **Maksu grupp**.
1. Valige väljal **Käibemaks** sobiv väärtus.

> [!NOTE]
> Lähetamise puhul, mis hõlmab käibemaksu kliendi aadressil, määrab rea tarneaadress rea maksugrupi. Kui klient lähetab olemasolevale aadressile, kus on juba konfigureeritud maksugrupp, kasutatakse olemasolevat maksugruppi. Vaikimisi ei ole aadressidel loomisel maksugruppi.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Üldiste käibemaksugruppide konfigureerimine Commerce Headquartersis

Commerce headquarters`is kannete redigeerimiseks toimige järgmiselt.

1. Avage **Maks \> Kaudsed maksud \> Käibemaks \> Käibemaksu grupid**.
1. Valige vasakul navigeerimisl konfigureeritav maksugrupp.
1. Konfigureerige **Jaemüügipõhine maks** kiirvahekaardil maksud grupile käibemaks.

> [!NOTE]
> Lähetamiseks, mis ei sisalda kliendi aadressi käibemaksu, määratlege maksugrupp rea tarneaadress ja maksugrupi jaoks konfigureeritud sihtkohapõhised maksud. Lisateavet vt teemast [Seadista maksud veebipoodidele vastavalt asukohale](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Lisaressursid

[Käibemaksu konfigureerimine veebitellimuste jaoks](../sales-tax-config.md)