---
title: Peida maksu katkestusteave tellimuse kokkuvõtetes
description: See teema kirjeldab, kuidas peita maksu katkestusteavet tellimuse kokkuvõtetes ostukorvis, väljaregistreerimises, tellimuse kinnituses ja tellimuse üksikasjade lehtedes Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: 9890b5cd92f8c07e6feabb26f4fdd076cb7a02bc
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648132"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Peida maksu katkestusteave tellimuse kokkuvõtetes

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema kirjeldab, kuidas peita maksu katkestusteavet tellimuse kokkuvõtetes ostukorvis, väljaregistreerimises, tellimuse kinnituses ja tellimuse üksikasjade lehtedes Microsoft Dynamics 365 Commerce.

Vaikimisi näitab maksu Dynamics 365 Commerce katkestusteavet tellimuse kokkuvõtetes ostukorvis, väljaregistreerimise, tellimuse kinnituse ja tellimuse üksikasjade lehtedel. Commerce'i versiooni 10.0.27 vabastamisel sisaldab Commerce'i saidi koostaja valikut, mis võimaldab teil peita maksu katkestusteabe tellimuse kokkuvõtetes.

Järgmine näide annab näite kahest tellimuse kokkuvõttest. Esimene näitab maksujaotusteavet ja teine peidab selle.

![Ostukorvide näited, kus kuvatakse ja on peidetud maksu katkestuse teave.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Maksueridumisteabe peitmise suvand on saadaval vaid siis, kui e-äri **kanali** suvand Hinnad sisaldavad käibemaksu on häälestatud valikule Jah äri peakontoris, **·** **\>\> kaupluses ja ärikanalites.\>** 
> - Vaikimisi on suvand **Kuva maksude katkestus tellimuse kokkuvõttes** saidikonstruktoris lubatud.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Peida maksu katkestusteave tellimuse kokkuvõtetes

Et peita maksu katkestuse teave tellimuse kokkuvõtetes, järgige neid samme.

1. Minge Commerce'i saidi koostaja saidile, mida soovite värskendada.
1. Avage **Saidi sätted \> Laiendused**.
1. Tühjendage **ruut Kuva maksude katkestus tellimuse kokkuvõtte** märkeruudus.

Maksupiiri teabe näitamiseks tellimusekokkuvõtetes märkige **ruut Kuva maksude katkestus tellimuse kokkuvõttes**.  

Järgmine näide näitab maksude katkestuse **näitamist tellimuse kokkuvõtte märkeruudus**, mis on esile tõstetud ja saidikonstruktoris valitud.

![Kuva maksude katkestused saidikonstruktori tellimuse kokkuvõtte suvandis.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

## <a name="additional-resources"></a>Lisaressursid

[Käibemaksu ülevaade](/finance/general-ledger/indirect-taxes-overview)

[Käibemaksu konfigureerimine veebitellimuste jaoks](sales-tax-config.md)

[Tõrkeotsing: võrgutellimuste maksud on valesti arvutatud.](troubleshoot/tax-miscalculated-online-order.md)
