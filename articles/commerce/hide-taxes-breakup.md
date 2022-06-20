---
title: Maksude jaotuse teabe peitmine tellimuse kokkuvõtetes
description: See artikkel kirjeldab, kuidas peita maksu katkestusteavet tellimuse kokkuvõtetes ostukorvis, väljaregistreerimises, tellimuse kinnituses ja tellimuse üksikasjade lehtedes Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: fe1f6c5875444f4f91ee1dfb01b3fdaa527c52e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881786"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Maksude jaotuse teabe peitmine tellimuse kokkuvõtetes

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See artikkel kirjeldab, kuidas peita maksu katkestusteavet tellimuse kokkuvõtetes ostukorvis, väljaregistreerimises, tellimuse kinnituses ja tellimuse üksikasjade lehtedes Microsoft Dynamics 365 Commerce.

Vaikimisi näitab maksu Dynamics 365 Commerce katkestusteavet tellimuse kokkuvõtetes ostukorvis, väljaregistreerimise, tellimuse kinnituse ja tellimuse üksikasjade lehtedel. Commerce'i versiooni 10.0.27 vabastamisel sisaldab Commerce'i saidi koostaja valikut, mis võimaldab teil peita maksu katkestusteabe tellimuse kokkuvõtetes.

Järgmine näide annab näite kahest tellimuse kokkuvõttest. Esimene näitab maksujaotusteavet ja teine peidab selle.

![Ostukorvide näited, kus kuvatakse ja on peidetud maksu katkestuse teave.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Maksueridumisteabe peitmise suvand on saadaval vaid siis, kui e-äri **kanali** suvand Hinnad sisaldavad käibemaksu on häälestatud valikule Jah äri peakontoris, **·** **\>\> kaupluses ja ärikanalites.\>** 
> - Vaikimisi on suvand **Kuva maksude katkestus tellimuse kokkuvõttes** saidikonstruktoris lubatud.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Maksude jaotuse teabe peitmine tellimuse kokkuvõtetes

Et peita maksu katkestuse teave tellimuse kokkuvõtetes, järgige neid samme.

1. Minge Commerce'i saidi koostaja saidile, mida soovite värskendada.
1. Avage **Saidi sätted \> Laiendused**.
1. Tühjendage **ruut Kuva maksude katkestus tellimuse kokkuvõtte** märkeruudus.

Maksupiiri teabe näitamiseks tellimusekokkuvõtetes märkige **ruut Kuva maksude katkestus tellimuse kokkuvõttes**.  

Järgmine näide näitab maksude katkestuse **näitamist tellimuse kokkuvõtte märkeruudus**, mis on esile tõstetud ja saidikonstruktoris valitud.

![Kuva maksude katkestused saidikonstruktori tellimuse kokkuvõtte suvandis.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

> [!NOTE]
> Kui olete kohandanud tellimuse kokkuvõtte mooduleid ja ei soovi pärida äriversiooni 10.0.27 või uuema versiooni funktsiooni "Peida maksu katkestusteave", [ei sisalda tellimuse kokkuvõtte vahesumma tasumakse, kui kasutate kohandatud tellimuse kokkuvõttemoodulit](troubleshoot/summary-taxes-custom-modules-10.0.27.md#resolution).

## <a name="additional-resources"></a>Lisaressursid

[Käibemaksu ülevaade](/finance/general-ledger/indirect-taxes-overview)

[Käibemaksu konfigureerimine veebitellimuste jaoks](sales-tax-config.md)

[Tõrkeotsing: võrgutellimuste maksud on valesti arvutatud.](troubleshoot/tax-miscalculated-online-order.md)
