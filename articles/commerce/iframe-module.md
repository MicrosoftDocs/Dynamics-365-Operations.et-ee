---
title: IFrame-moodul
description: See teema hõlmab iFrame-moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665392"
---
# <a name="iframe-module"></a>IFrame-moodul

[!include [banner](includes/banner.md)]

See teema hõlmab iFrame-moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

IFrame-moodul tagab iFrame'i (tekstisisene raam), mis majutab saidil välissisu. Näiteks saab seda kasutada YouTube'i video või PDF-faili vaaturi majutamiseks ükskõik millisel saidilehel. 

IFrame-mooduli jaoks on vaja siht-URL-i. Seejärel majutab see sihtlehe sisu HTML-i **iFrame'i** elemendi sees. Välised URL-id peavad olema saidi sisu turbepoliitika (CSP) direktiivide põhjal lubatud URL-ide loendis. IFrame'i sisu jaoks peavad URL-id olema lubatud direktiivi **frame-ancestor** kaudu. Lisateavet leiate teemast [Sisu turbepoliitika (CSP) haldamine](manage-csp.md).

> [!NOTE]
> IFrame-moodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.13.

Järgmisel pildil on näited iFrame-moodulitest, mis näitavad saidilehtedel väliseid videoid.

![IFrame-moodulite näide, millel on näha välised videod](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>IFrame-mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Pealkiri | Tekst | Mooduli pealkiri. |
| Siht-URL | URL | Moodulis majutatud URL. |
| Kõrgus | Arv või protsent | Mooduli kõrgus pikslites või protsendina. Näiteks koheldakse väärtust **100** pikslite arvuna ja väärtust **100%** protsendina. |
| Aria-silt | Tekst | Juurdepääsetavuse eesmärgil saab määratleda ARIA-sildi (Accessible Rich Internet Applications). |

## <a name="add-an-iframe-module-to-a-page"></a>Lehele iFrame-mooduli lisamine

Et lisada välise video kuvamiseks lehele iFrame-moodul, toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Turundusmall** ja valige seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** mall **Turundusmall**. Sisestage jaotises **Lehe nimi** väärtus **Turundusleht** ja seejärel valige **OK**.
1. Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **iFrame** ja klõpsake seejärel **OK**.
1. Seadke mooduli atribuutide paanil suvandi **Siht-URL** väärtuseks video väline URL.
1. Määrake vajaduse järgi muud atribuudid, näiteks **Pealkiri** ja **Kõrgus**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge oma saidil turunduslehele. Peaksite nägema iFrame-moodulis renderdatavat videot.
 
## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Sisu turbepoliitika (CSP) haldamine](manage-csp.md)
