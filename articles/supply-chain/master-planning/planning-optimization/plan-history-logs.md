---
title: Plaani ajaloo ja plaanimise logide vaatamine
description: Selles teemas selgitatakse, kuidas vaadata planeerimistööde ajalugu, mille on käivitanud planeerimise optimeerimise funktsioon.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 757d2103bd629c0107a3f29599196a56ea56d431a66cf1e69c7b3cf3d817c087
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724816"
---
# <a name="view-plan-history-and-planning-logs"></a>Plaani ajaloo ja plaanimise logide vaatamine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas vaadata planeerimistööde ajalugu, mille on käivitanud planeerimise optimeerimise funktsioon rakenduses Microsoft Dynamics 365 Supply Chain Management-.

Plaani ajaloo vaatamiseks avage plaan, avades **Koonplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid** ja valides suvandi **Ajalugu**. Ajaloos loetletakse kõik valitud plaani tööd. Loend sisaldab lõpetatud ja aktiivseid töid.

Plaanimise optimeerimise koondplaneerimise tööde ajalugu töötab ainult kuni 60 kirjet koondplaani kohta. Kui käivitate uue koondplaneerimise arvutuse, kustutatakse selle plaani varaseim ajalookirje.

Lisaks tööde algusaja ja oleku nägemisele saate vaadata konkreetse töö logi. Logi sisaldab täiendavat teavet ja hoiatusi. Kõikidel töödel ei ole logi. Töö logi vaatamiseks valige **Logi**. Logikirjeid säilitatakse ainult 30 päeva jooksul pärast töö lõpetamiskuupäeva, pärast mida need automaatselt kustutatakse.

Kui **Pakettkäsitlus** suvand kiirkaardil **Käivita taustal** lubati põhiplaani töötlemise seadistamisel, kuvatakse partiitöö logis lisateavet üldplaneeringu ajal loodud hoiatuste ja vigade kohta. Näiteks fikseeritakse automaatse fikseerimise vead ainult partii töölogis. Neid ei kuvata **ajaloo** leheküljel logides.

Koondplaneerimise käivitamisel ilmnenud automaatse täitmise tõrgete ja teiste hoiatuste või tõrgete vaatamiseks järgige neid samme.

1. Avage **Süsteemihaldus \> Päringud \> Pakett-tööd**.
1. Leidke ja valige kirje, mis esindab teid huvitavat üldplaneeringu jooksu. (Näiteks välja **Töö kirjelduse** väärtus võib alata *koondplaneerimisega* .)
1. Järgige üht järgmistest sammudest, sõltuvalt sellest, kas kasutate **partiitööde** lehe puhul *täiustatud vormi* või *pärandi (muutmata) vormi*.

    - Kui kasutate täiustatud vormi: valige tegevuspaanil **Partiitöö ajalugu**. Seejärel valige **Partiitöö ajalugu** lehel tegevuspaanil **Logi**.
    - Kui kasutate pärandvormi: valige tegevuspaani vahekaardil **Partiitöö** **Logi**.

1. Valige **Teate üksikasjad**, et avada **Teate üksikasjade** paan, kus saate vaadata kõiki hoiatusi ja tõrkeid, mis talletati töötlemise ajal.

## <a name="related-resources"></a>Seotud ressursid

- [Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)
- [Planeerimise optimeerimise kasutamise alustamine](get-started.md)
- [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)
- [Plaanile filtrite rakendamine](plan-filters.md)
- [Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
