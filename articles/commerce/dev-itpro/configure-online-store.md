---
title: Konfigureeri e-poode
description: See artikkel sisaldab linke teemadele, mis aitavad teil võrgupoodi keskselt konfigureerida ja hallata.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cf7adf76cb547ffbf516ce475380ddafaca1dfc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215458"
---
# <a name="configure-online-stores"></a>Konfigureeri e-poode

[!include [banner](../includes/banner.md)]

See artikkel sisaldab linke teemadele, mis aitavad teil võrgupoodi keskselt konfigureerida ja hallata.

Järgmises tabelis loetletud teemad aitavad teil kaubanduse komponente ja jaemüügi võrgupoodi kliendis konfigureerida.

## <a name="configure-an-online-store"></a>E-poe konfigureerimine

| Ülesanne                                                | Üksikasjad                                                                                                                                                                                                                                                                                                                                                   | Teema                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Komponentide konfigureerimine.                        | Saate seadistada ja hallata kaubandustoimingute teavet. See teave hõlmab poode, makse, tooteid, kinkekaarte, soodustusi ja allahindlusi.                                                                                                                                                                                                          | [Retaili seadistamine ja haldamine](https://technet.microsoft.com/library/hh597201.aspx) (TechNeti sisu Microsoft Dynamics AX 2012 kohta)                                                                                                                                                                                                                                                                                          |
| Kanali navigeerimishierarhia konfigureerimine.    | Saate luua kanali navigeerimiskategooria hierarhia, mida saab kasutada kategooriastruktuuri seadistamiseks teie võrgupoe kaudu pakutavatele toodetele. Saate määratleda kategooriahierarhia ning määrata kategooriatesse tooted, tooteatribuutide grupid ja atribuudiväärtused. Seejärel saate määrata võrgupoele kategooriahierarhia.                            | [Jaemüügihierarhia häälestus](https://technet.microsoft.com/library/hh580593.aspx)</br> (TechNet sisu AX 2012 jaoks)</br> [Atribuutide ja atribuudi tüüpide seadistamine](https://technet.microsoft.com/library/hh227548.aspx) (TechNet sisu AX 2012 jaoks)</br> [Jaemüügi atribuutide gruppide seadistamine](https://technet.microsoft.com/library/jj728713.aspx) (TechNet sisu AX 2012 jaoks) |
| Võrgupoe lisamine organisatsioonihierarhiasse. | Enne kui saate määrata loodud võrgupoe jaoks tootesortimendid või täita tellimusi või luua selle võrgupoe andmeid sisaldavaid aruandeid, peate määrama poe ühte või mitmesse organisatsioonihierarhiasse. Peate e-poe määrama vähemalt organisatsioonihierarhiale, mis sisaldab tootesortimente. | [Võrgupoe seadistamine](https://technet.microsoft.com/library/jj682095.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                                                                                                                                                                                                     |
| Võrgupoele tarneviiside lisamine.          | Saate lisada tarneviisid, mida võrgupood pakub.                                                                                                                                                                                                                                                                                                 | [Võrgupoe seadistamine](https://technet.microsoft.com/library/jj682095.aspx) (TechNeti sisu Microsoft AX 2012 kohta)                                                                                                                                                                                                                                                                                                     |
| Atribuutide vastendamine ja metaandmete lisamine.                   | Saate valida suvandid, mis näitavad, kuidas iga kategooria või kanali toote atribuudid peavad Microsoft SharePointi saidi võrgupoes käituma.                                                                                                                                                                                              | [Võrgupoe seadistamine](https://technet.microsoft.com/library/jj682095.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Võrgupoe toodete konfigureerimine

| Ülesanne                                 | Üksikasjad                                                                                                                                           | Teema                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Võrgupoele sordimentide lisamine. | Saate lisada sortimendid, mis sisaldavad teie võrgupoes pakutavaid tooteid.                                                                  | [Võrgupoe seadistamine](https://technet.microsoft.com/library/jj682095.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                                              |
| Kataloogide haldamine.                     | Saate kasutada tootekatalooge, et tuvastada tooteid, mida soovite oma kauplustes pakkuda.                                                              | [Peamised ülesanded: jaemüügi tootekataloogide loomine](https://technet.microsoft.com/library/jj728712.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                           |
| Hindade haldamine.                       | Saate seadistada ja kasutada hinnagruppe, mis on keskseks lingiks hindade ja allahindluste vahel, ning kanaleid, katalooge, filiaale ja püsikliendiprogramme. | [Hindade seadistamine hinnagruppide abil](https://technet.microsoft.com/library/hh597169.aspx) (TechNet sisu AX 2012 jaoks)</br> [Maksude seadistamine](https://technet.microsoft.com/library/hh580571.aspx) (TechNet sisu AX 2012 jaoks) |
| Allahindluste haldamine.                    | Saate seadistada ja hallata hinna korrigeerimisi ning nelja tüüpi allahindlusi.                                                                                  | [Hinna korrigeerimiste ja allahindluste seadistamine](https://technet.microsoft.com/library/hh597114.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                          |
| Saatekulude haldamine.             | Saate seadistada ja hallata võrgupoele kohaseid saatekulusid.                                                                     | [Võrgupoodide jaoks saatekulude seadistamine](https://technet.microsoft.com/library/jj728714.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                           |
| Tarneviiside haldamine.            | Saate hallata võrgupoe pakutavaid tarneviise.                                                                                        | [Tarneviiside seadistamine](https://technet.microsoft.com/library/jj728719.aspx) (TechNeti sisu AX 2012 kohta)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Saate seadistada andmevahetuse Commerce'i ja võrgupoe vahel

| Ülesanne                                 | Üksikasjad                                                                                                                               | Teema                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kanali integratsiooniprofiilide seadistamine. | Profiilid võimaldavad komponentidel üksteisega suhelda. Saate seadistada profiilid enne andmevahetuse sätete konfigureerimist. | [Reaalajas teenuse profiili seadistamine](https://technet.microsoft.com/library/hh580631.aspx) (TechNet sisu AX 2012 jaoks)</br> [Kanali profiili seadistamine](https://technet.microsoft.com/library/jj677402.aspx) (TechNet sisu AX 2012 jaoks) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]