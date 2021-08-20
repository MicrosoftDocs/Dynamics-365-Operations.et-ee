---
title: Tellimise moodul
description: See teema hõlmab tellimise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: c9c0ed18e3d5fd2521d63f8aa5b0ea668979c57d4de738b9d51a05a1cc0b6e72
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730919"
---
# <a name="subscribe-module"></a>Tellimise moodul

[!include [banner](includes/banner.md)]

See teema hõlmab tellimise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

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
1. Valige vaikelehe pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** **Telli** moodul ja klõpsake seejärel **Ok**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Minge **lehekülgedele** ja avage saidi avaleht (või looge uus avaleht, kasutades turundusmalli).
1. Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** **Telli** moodul ja klõpsake seejärel **Ok**.
1. Paaniloendi mooduli atribuudipaanil lisage pealkiri, näiteks **Telli uudiskiri**.
1. Lisage lõigu tekst, nt **Hiljutised trendid, stiilid ja kampaaniahinnad. Kas olete loendis? Tellige ja saate info kuumade pakkumiste kohta!**
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Adventure Works teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
