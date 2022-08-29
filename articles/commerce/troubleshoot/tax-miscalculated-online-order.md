---
title: Võrgutellimuste maksud on valesti arvutatud
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui võrgutellimuste maksud on valesti arvutatud või kui müügirea maksugrupp pole õigesti seatud.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: a85b03cb6245c7c2e3622abc61a7887030927432
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285574"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Võrgutellimuste maksud on valesti arvutatud

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui võrgutellimuste maksud on valesti arvutatud või kui müügirea maksugrupp pole õigesti seatud.

## <a name="description"></a>Kirjeldus

Kui e-äri tellimus on esitatud, siis on maksud valesti arvutatud või on müügirea maksugrupp valesti seatud.

## <a name="resolution"></a>Lahendus

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Üldiste käibemaksugruppide konfigureerimine Commerce Headquartersis

Commerce headquarters`is kannete redigeerimiseks toimige järgmiselt.

1. Avage **Maks \> Kaudsed maksud \> Käibemaks \> Käibemaksu grupid**.
1. Valige vasakul navigeerimispaanil konfigureeritav maksugrupp.
1. Konfigureerige **Jaemüügipõhine maks** kiirvahekaardil maksud grupile käibemaks.

> [!NOTE]
> Lähetamiseks, mis ei sisalda kliendi aadressiga määratletud käibemaksu, määravad maksugrupile rea tarneaadress ja maksugrupi jaoks konfigureeritud sihtkohapõhised maksud. Lisateavet vt teemast [Seadista maksud veebipoodidele vastavalt asukohale](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

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

## <a name="additional-resources"></a>Lisaressursid

[Käibemaksu konfigureerimine veebitellimuste jaoks](../sales-tax-config.md)
