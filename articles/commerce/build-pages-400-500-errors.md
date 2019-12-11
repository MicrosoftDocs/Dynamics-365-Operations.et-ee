---
title: 4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine
description: Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697102"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.

## <a name="overview"></a>Ülevaade

Kui taotlus ei ole edukas, väljastab server HTTP olekukoodi tõrkevastused. Kui lehte ei leita, hõivatakse ja tagastatakse olekukood 404, ning serveritõrke ilmnemisel hõivatakse ja tagastatakse olekukood 500. Rakenduses Dynamics 365 Commerce saavad rakenduse kasutajad luua kohandatud olekukoodi tõrkevastuse lehti, mis kuvatakse nende olekukoodi tõrkevastuste kasutajatele.

## <a name="build-a-status-code-error-response-page"></a>Olekukoodi tõrkevastuse lehe loomine

Olekukoodi tõrkevastuse lehe loomise alustamiseks toimige järgmiselt.

1. Logige oma eelistatud veebibrauseris rakendusse Dynamics 365 Commerce sisse. 
1. Valige sait, mille jaoks soovite 4xx/5xx olekukoodi tõrkevastuse lehe luua.

### <a name="build-the-template"></a>Malli loomine

Olekukoodi tõrkevastuse lehe malli loomiseks toimige järgmiselt.

1. Avage **Mallid \> Uus mall**.
1. Andke uuele mallile nimi.
1. Looge mall põhinedes struktuuril, mille soovite, et olekukoodi tõrkevastuse lehel olemas oleks.
1. Registreerige mall ja avaldage see.

### <a name="build-the-status-code-error-response-page"></a>Olekukoodi tõrkevastuse lehe loomine

Olekukoodi tõrkevastuse lehe loomiseks toimige järgmiselt.

1. Avage **Lehed \> Uus leht**.
1. Andke olekukoodi tõrkevastuse lehele nimi, kuid **ärge** määrake välja **URL**.
1. Looge leht.
1. Registreerige leht ja avaldage see.

> [!NOTE]
> 4xx ja 5xx olekukoodi tõrgete jaoks saate luua eraldi olekukoodi tõrkevastuse lehed. Teise võimalusena saate mõlema tõrkekategooria puhul kasutada sama üldist olekukoodi tõrkevastuse lehte.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Olekukoodi tõrkevastuse lehe ümbersuunamise määramine

Olekukoodi tõrkevastuse lehe ümbersuunamise määramiseks toimige järgmiselt.

1. Avage **URL-id \> Uus \> Uus pseudonüüm** ja valige varem loodud olekukoodi tõrkevastuse leht.
1. Väljale **Pseudonüüm** sisestage kas **vaikimisi 4xx** või **vaikimisi 5xx**, olenevalt olekukoodi tõrkevastuse lehest, mille ümbersuunamise jaoks määrate. Need pseudonüümid tuleb avaldada. Vastasel korral ümbersuunamine ei tööta.
1. Linkimise kinnitamiseks valige **OK**.

> [!NOTE]
> Kui kasutate mõlema tõrkekategooria jaoks ühte olekukoodi tõrkevastuse lehte, korrake seda protseduuri samale lehele teise tõrkekategooria pseudonüümi linkimiseks.

## <a name="additional-resources"></a>Lisaressursid

[Mallidega töötamine](work-with-templates.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehe URL-i loomine](create-page-url.md)
