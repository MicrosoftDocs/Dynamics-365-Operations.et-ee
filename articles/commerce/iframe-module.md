---
title: IFrame-moodul
description: See artikkel katab IFrame’i mooduli ja kirjeldab, kuidas lisada see saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 248da5132d1a2c6dcf8f246628f969c8a200b26c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269891"
---
# <a name="iframe-module"></a>IFrame-moodul

[!include [banner](includes/banner.md)]

See artikkel katab IFrame’i mooduli ja kirjeldab, kuidas lisada see saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

IFrame-moodul tagab iFrame'i (tekstisisene raam), mis majutab saidil välissisu. Näiteks saab seda kasutada YouTube'i video või PDF-faili vaaturi majutamiseks ükskõik millisel saidilehel. 

IFrame-mooduli jaoks on vaja siht-URL-i. Seejärel majutab see sihtlehe sisu HTML-i **iFrame'i** elemendi sees. Välised URL-id peavad olema saidi sisu turbepoliitika (CSP) direktiivide põhjal lubatud URL-ide loendis. IFrame'i sisu jaoks peavad URL-id olema lubatud direktiivi **frame-ancestor** kaudu. Lisateavet leiate teemast [Sisu turbepoliitika (CSP) haldamine](manage-csp.md).

> [!NOTE]
> IFrame-moodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.13.

Järgmisel pildil on näited iFrame-moodulitest, mis näitavad saidilehtedel väliseid videoid.

![IFrame-moodulite näide, milles on näha välised videod.](./media/ecommerce-iframe.PNG)

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
1. Dialoogiboksis Uus **mall** sisestage malli nime **all** turundusmall **ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiboksi Uue **lehe loomine jaotises** Lehe nimi sisestage **turundusleht** **ja** seejärel valige **järgmine**.
1. Valige **valiku Vali mall** all loodud **turundusmall** ja seejärel **edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**. 
1. Uue lehekülje põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige **iframe’i** moodul ja seejärel valige **OK**.
1. Seadke mooduli atribuutide paanil suvandi **Siht-URL** väärtuseks video väline URL.
1. Määrake vajaduse järgi muud atribuudid, näiteks **Pealkiri** ja **Kõrgus**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge oma saidil turunduslehele. Peaksite nägema iFrame-moodulis renderdatavat videot.

> [!NOTE]
> Kuna IFrame’i moodul hostib välist sisu, peavad saidi autorid tagama, et iframe’i moodulis majutatud sisu ei riku sisupiirangu poliitikaid vastaval turul. Kui iframe-moodulit kasutav lehekülg sisaldab sisu rikkumise, saab saidi autor iFrame’i mooduli eemaldada, avades saidikonstruktoris lehe, **valides** iframe-moodulis suvandi Eemalda moodul ning salvestades ja avaldades seejärel uuesti.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Sisu turbepoliitika (CSP) haldamine](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
