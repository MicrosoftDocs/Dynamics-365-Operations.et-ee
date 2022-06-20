---
title: Telli moodul
description: See artikkel kirjeldab moodulite tellimist ja nende lisamise teavet moodulis saidi lehtedele Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 23b74f5853ffb7f191ea7ee3da0d3238db339d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852689"
---
# <a name="subscribe-module"></a>Telli moodul

[!include [banner](includes/banner.md)]

See artikkel kirjeldab moodulite tellimist ja nende lisamise teavet moodulis saidi lehtedele Microsoft Dynamics 365 Commerce.

Tellimismooduleid saab kasutada saidilehtedel, et hõivata klienditeavet info infolehtede või kampaaniate kohta.

Järgmine näide näitab tellimismooduli jaluse näidet Adventure Worksi kodulehel.

![Näide tellimismooduli jaluse näitest Adventure Worksi kodulehel](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Tellimismoodul on saadaval Commerce'i mooduli teegis Dynamics 365 Commerce 10.0.20 väljalaske versioonis.
> - Tellimismoodul kuvatakse Adventure Works teemas.
> - Tellimismoodul nõuab andmetegevuse laiendust, et töötada mõnede turundusmeilide pakkujatega, nii et pärast klienditeabe salvestamist saab saata ka meililehte või kampaaniameile.

## <a name="subscribe-module-properties"></a>Telli mooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Päis       | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Tellimismooduli tekstipäis, nt **Telli uudistelehte** või **Registreeri 10% allahindluseks** välja. |
| Lõik     | Lõigu tekst | Tellimismoodul toetab lõigu teksti rtftekstina, et pakkuda pealkirjas tegevusele kutsumise kohta täiendavaid üksikasju. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Paaniloendi mooduli lisamine uuele lehele

Paaniloendi mooduli uuele lehele lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Minge **mallidesse** ja avage oma saidi avalehe turundusmall (või looge uus turundusmall).
1. **Vaikelehe** põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige tellimismoodul **ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge **lehekülgedele** ja avage saidi avaleht (või looge uus avaleht, kasutades turundusmalli).
1. Vaikelehe põhipesas valige kolmikpunkti nupp (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige tellimismoodul **ja** seejärel valige **OK**.
1. Paaniloendi mooduli atribuudipaanil lisage pealkiri, näiteks **Telli uudiskiri**.
1. Lisage lõigu tekst, nt **Hiljutised trendid, stiilid ja kampaaniahinnad. Kas olete loendis? Tellige ja saate info kuumade pakkumiste kohta!**
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Adventure Works teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
