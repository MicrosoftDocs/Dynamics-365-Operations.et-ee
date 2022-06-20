---
title: 4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine
description: See artikkel kirjeldab, kuidas koostada kohandatud vastuselehti 4xxi ja 5xxi olekukoodi tõrgete jaoks, kasutades moodulis Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0b56d7a58659205ce4483480fd85d1c91ae52a0f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882255"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas koostada kohandatud vastuselehti 4xxi ja 5xxi olekukoodi tõrgete jaoks, kasutades moodulis Microsoft Dynamics 365 Commerce.

Kui taotlus ei ole edukas, väljastab server HTTP olekukoodi tõrkevastused. Kui lehte ei leita, hõivatakse ja tagastatakse olekukood 404, ning serveritõrke ilmnemisel hõivatakse ja tagastatakse olekukood 500. Rakenduses Dynamics 365 Commerce saavad rakenduse kasutajad luua kohandatud olekukoodi tõrkevastuse lehti, mis kuvatakse nende olekukoodi tõrkevastuste kasutajatele.

## <a name="build-a-status-code-error-response-page"></a>Olekukoodi tõrkevastuse lehe loomine

Olekukoodi tõrkevastuse lehe loomise alustamiseks toimige järgmiselt.

1. Logige oma eelistatud veebibrauseris rakendusse Dynamics 365 Commerce sisse. 
1. Valige sait, mille jaoks soovite 4xx/5xx olekukoodi tõrkevastuse lehe luua.

### <a name="build-the-template"></a>Malli loomine

Olekukoodi tõrkevastuse lehe malli loomiseks toimige järgmiselt.

1. Avage **Mallid**.
1. Valige lehe malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all uue malli nimi ja valige seejärel **OK**.
1. Looge mall põhinedes struktuuril, mille soovite, et olekukoodi tõrkevastuse lehel olemas oleks.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 

### <a name="build-the-status-code-error-response-page"></a>Olekukoodi tõrkevastuse lehe loomine

Olekukoodi tõrkevastuse lehe loomiseks toimige järgmiselt.

1. Avage **Lehed**.
1. Valige lehe loomiseks **Uus**.
1. Valige mall dialoogiboksis **Vali mall** ja seejärel sisestage olekukoodi tõrkevastuse lehe pealkiri jaotises **Lehe nimi**. Jätke väli **Lehe URL** tühjaks.
1. Looge leht.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
