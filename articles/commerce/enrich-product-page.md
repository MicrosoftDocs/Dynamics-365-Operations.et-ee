---
title: Tootelehe rikastamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411598"
---
# <a name="enrich-a-product-page"></a>Tootelehe rikastamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.

## <a name="overview"></a>Ülevaade

Vaikimisi kasutab teie sait toote andmete näitamiseks üldist lehte. See leht sisaldab põhiteavet toote ja selle müümiseks vajalike juhtelementide kohta. Samas saate täiendada kaubanduse skaala üksusest tulevat teavet konkreetse toote täiendavate piltide või tekstiga. See protsess on tuntud kui toote lehe rikastamine.

Paljudel juhtudel soovite oma toodete jaoks kasutada kindlat täiendavat sisu. Kui avate autoriseerimise tööriistal suvandi **Jaemüük ja kaubandus**, näete saidile määratud kanalist pärinevate toodete loendit. Selles loendis näitab veerg **Rikastatud**, kas toote tooteleht on rikastatud. Kui veerus kuvatakse märge, on toote jaoks olemas rikastatud toote leht. Kui ühtegi märget ei kuvata, kasutatakse toote jaoks vaikimisi tootelehte ja sisu. Võite kuvada  nii rikastatud kui ka mitte rikastatud toote lehtede eelvaate, valides loendist toote nime.

## <a name="enrich-a-product-page"></a>Tootelehe rikastamine

Tootelehe rikastamiseks toimige järgmiselt.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **Tooted**.
1. Valige toode, millel pole rikastatud tootelehte.
1. Valige toimingupaanil suvand **Rikastatud tooteleht**.
1. Valige suvand **PDP mall** ja seejärel nupp **OK**.
1. Laiendage vasakul lehe liigendpuus pesa **Peamine**.
1. Valige pesa **Peamine** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige suvand **Konteiner 2** ja seejärel nupp **OK**.
1. Valige suvandi **Konteiner 2** kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.
1. Valige suvand **Funktsioon** ja seejärel nupp **OK**.
1. Parempoolsel atribuutide paanil sisestage väljale **Rikastekst** toote värskendatud kirjeldus.
1. Sisestage väljale **Pealkiri** pealkirja tekst ja seejärel valige **OK**.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Sisestage väljale **Kommentaarid** suvand **Rikastatud suvand** ja valige seejärel **OK**.
1. Rikastatud tootelehe eelvaate kuvamiseks valige suvand **Eelvaade**. Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.
1. Valige **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)
