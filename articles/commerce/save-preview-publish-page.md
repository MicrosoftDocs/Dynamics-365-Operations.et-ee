---
title: Lehe salvestamine, eelvaade ja avaldamine
description: See teema kirjeldab, kuidas salvestada, vaadata ja avaldada lehte rakenduses Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 68fec8c2ddc05c71394045351cef880361f2e306
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254813"
---
# <a name="save-preview-and-publish-a-page"></a>Lehe salvestamine, eelvaade ja avaldamine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas salvestada, vaadata ja avaldada lehte rakenduses Microsoft Dynamics 365 Commerce.

## <a name="save-a-page"></a>Lehe salvestamine

Lehekülje salvestamiseks peate selle ise registreerima ja avama lehe redaktoris. Lehe kuvamiseks klõpsake tegumiribal käsku **Redigeeri**. Te peaksite salvestama lehe kohe pärast selle redigeerimist, et tagada teie muudatuste salvestamine.

Lehe salvestamisel on muudatused nähtavad ainult teile. Salvestamise toiming on mõeldud peamiselt muudatuste salvestamiseks, kui leht pole veel sisse registreerimiseks valmis. Kui olete lehe muutmise lõpetanud, soovitame selle sisse registreerida, et muudatused oleksid teistele nähtavad. Sel hetkel saavad lehte välja registreerida ka teised kasutajad, kes seda muutma peavad.

## <a name="preview-a-page"></a>Lehe eelvaade

Autorluse tööriist pakub kahte tüüpi eelvaate funktsioone: visuaalne leheehitaja, mis on "mida näete, seda ka saate" (WYSIWYG) eelvaatepaan lehe redaktoris, ja eraldi eelvaate aken.

Kui kasutate lehe redaktorit, kuvatakse keskuse paanil "mida näete, seda ka saate" (WYSIWYG) eelvaade. See eelvaade uuendatakse automaatselt iga kord, kui salvestate lehe. Saate seda ka käsitsi värskendada, valides käsuribal käsu **Värskenda**. Eelvaade muudab lehekülge just nii, nagu saidi kasutajad seda näevad, kuid loojad renderdatakse selle peal.

Kui olete lehe muutmise lõpetanud, võite soovida seda vaadata, et näha, mida klientidele kuvatakse. Lehekülje eelvaate nägemiseks valige käsuribal suvand **Eelvaade**. Eelvaade kuvatakse eraldi brauseri aknas. Eelvaate akna lehekülg renderdatakse nii, nagu saidi kasutaja seda näeb. Saate muuta akna suurust, et veenduda, et reageerivad moodulid on kõikides vaateportides õigesti renderdatud.

> [!NOTE]
> Avaldamata sisu eelvaate jaoks on nõutavad autentimine ja õiged load. Seega, kui jagate eelvaate URL-i kellegagi, peavad sellel isikul olema sisule juurdepääsuks vajaminevad õigused.

## <a name="publish-a-page"></a>Lehe avaldamine

Kui leht on valmis, on järgmiseks sammuks selle avaldamine, et välised kasutajad saaksid sisu vaadata. Enne lehe avaldamist peate selle registreerima, valides käsuribal **Lõpeta redigeerimine**.

Lehti saate avaldada ja tühistada avaldamise kas lehe inspektorist või lehe redaktorist. Lehe inspektor kuvab lehtede loendi ja lubab hulgioperatsioone. Lehe redaktorit saab kasutada ainult ühe avatud lehekülje avaldamiseks või avaldamise tühistamiseks.

Lehe inspektoris ühe või mitme lehekülje avaldamiseks valige leheküljed, veenduge, et need on sisse registreeritud, ja seejärel valige käsuribal käsk **Avalda**. Lehed on avaldatud ja saate teatise toimingu kohta autorluse tööriistas.

Lehe redaktoris ühe lehekülje avaldamiseks on protseduur sarnane. Kui leht on lehe redaktoris avatud, veenduge, et see on sisse registreeritud ja seejärel valige käsuribal käsk **Avalda**. Leht on avaldatud ja saate teatise toimingu kohta.

Lehe avaldamisel avaldatakse ainult lehe sisu. Teie ja teised kasutajad saavad minna lehele ja vaadata seda ainult pärast seda, kui URL on sellega seotud. URL tuleb eraldi avaldada.

> [!IMPORTANT]
> Enne lehe avaldamist tuleb avaldada kõik pildid või fragmendid, millele leht viitab.

## <a name="save-preview-and-publish-a-home-page"></a>Lehe salvestamine, eelvaade ja avaleht

Avalehe salvestamiseks, eelvaateks ja avaldamiseks toimige järgmiselt.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **Lehed**.
1. Leidke ja valige avaleht, et avada see lehe redaktoris.
1. Valige suvand **Redigeeri**.
1. Muutke lehte nii nagu vajate.
1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. Sisestage väljale **Kommentaarid** tehtud muudatuste kohta märkus ja seejärel valige nupp **OK**.
1. Lehe eelvaate kuvamiseks valige suvand **Eelvaade**. Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.
1. Valige **Avalda**.

## <a name="publish-a-url"></a>URL-i avaldamine

URL-i avaldamiseks tehke järgmist.

1. Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).
1. Valige navigeerimispaanilt vasakult suvand **URL-id**.
1. Otsige ja valige avaldatav URL.
1. Klõpsake käsuribal käsk **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)

[Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]