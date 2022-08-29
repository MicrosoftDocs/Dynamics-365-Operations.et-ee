---
title: Pildi loendi moodul
description: See artikkel hõlmab pildiloendi mooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: e89624a98d3cbdd861391e994386ae57d2c38aa0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269831"
---
# <a name="image-list-module"></a>Pildi loendi moodul

[!include [banner](includes/banner.md)]

See artikkel hõlmab pildiloendi mooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Pildiloendi moodulit saab kasutada pildikogumi (massiiv) lihtsaks lisamiseks saidi lehtedele. Iga massiivi pilti saab konfigureerida lõigu teksti ja lingi URL-dega. Pildiloendi moodul sobib kõige paremini logode või logosid sisaldavad loendi kuvamiseks.

> [!IMPORTANT]
> - Tellimismoodul on saadaval Commerce'i mooduli teegis Dynamics 365 Commerce 10.0.20 väljalaske versioonis.
> - Pildiloendi moodul kuvatakse Adventure Works teemas.

Järgnev illustratsioon näitab näidet, kus pildiloendi moodul kuvab tekstiloendi, mis sisaldab logosid ettevõtte ja tarbija (B2C) ettevõtte ja ettevõtte(B2C) saidi lehel.

![Näide pildiloendi moodulist, kus on kuvatud logosid sisaldavad tekstiloendid](./media/Image_list.PNG)

Järgnev illustratsioon näitab näidet, kus pildiloendi moodul kuvab tekstiloendi, mis sisaldab brändi logosid Adventure Works ettevõtte ja ettevõtte (B2B) saidi lehel.

![Kaubamärgi logosid kuvava pildiloendi mooduli näide](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Pildiloendi mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Päis       | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Pildi mooduli tekstipäis. |
| Pildiloend    | Pildid, tekst ja URL-id | Iga massiivi üksus on pilt, millele on lisatud lõigu tekst ja URL. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Aktiivse pildimooduli lisamine uuele leheküljele

Pildiloendi mooduli uuele lehele lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Minge **mallidesse** ja avage oma saidi avalehe turundusmall (või looge uus turundusmall).
1. **Vaikelehe** põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige pildiloendi **moodul** ja seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge **lehekülgedele** ja avage saidi avaleht (või looge uus avaleht, kasutades turundusmalli).
1. Vaikelehe põhipesas valige kolmikpunkti nupp (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige pildiloend **ja** seejärel valige **OK**.
1. Lisage pildiloendi mooduli atribuudipaanile pealkiri (nt **Meie kaubamärgid**).
1. Saate lisada pildiloendi üksuse ning määrata pildi, mõne lõigu teksti ja ümbersuunamise URL-i.
1. Lisage ja konfigureerige pildimooduleid vastavalt vajadusele.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Adventure Works teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
