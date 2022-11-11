---
title: Plaaniajaloo ja plaanimislogide kuvamine
description: See artikkel selgitab, kuidas vaadata tööde planeerimise ajalugu.
author: t-benebo
ms.date: 06/01/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740927"
---
# <a name="view-plan-history-and-planning-logs"></a>Plaaniajaloo ja plaanimislogide kuvamine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas vaadata Microsofti plaanimistööde ajalugu Dynamics 365 Supply Chain Management.

Plaani ajaloo vaatamiseks avage plaan, avades **Koonplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid** ja valides suvandi **Ajalugu**. Ajaloos loetletakse kõik valitud plaani tööd. Loend sisaldab lõpetatud ja aktiivseid töid.

Süsteem säilitab maksimaalselt 60 ajaloo kirjet koondplaani kohta ja kustutab üle 30 päeva vanemad kirjed. Iga kord kui käivitate uue koondplaneerimise arvutuse, lisab süsteem uue ajaloo kirje ja puhastab seejärel vajaduse järgi vanimad kirjed.

Lisaks tööde algusaja ja oleku nägemisele saate vaadata konkreetse töö logi. Logi sisaldab täiendavat teavet ja hoiatusi. Kõikidel töödel ei ole logi. Töö logi vaatamiseks valige **Logi**. Logikirjeid säilitatakse ainult 30 päeva jooksul pärast töö lõpetamiskuupäeva, pärast mida need automaatselt kustutatakse.

Kui **Pakettkäsitlus** suvand kiirkaardil **Käivita taustal** lubati põhiplaani töötlemise seadistamisel, kuvatakse partiitöö logis lisateavet üldplaneeringu ajal loodud hoiatuste ja vigade kohta. Näiteks fikseeritakse automaatse fikseerimise vead ainult partii töölogis. Neid ei kuvata **ajaloo** leheküljel logides.

Koondplaneerimise käivitamisel ilmnenud automaatse täitmise tõrgete ja teiste hoiatuste või tõrgete vaatamiseks järgige neid samme.

1. Avage **Süsteemihaldus \> Päringud \> Pakett-tööd**.
1. Leidke ja valige kirje, mis esindab teid huvitavat üldplaneeringu jooksu. (Näiteks välja **Töö kirjelduse** väärtus võib alata *koondplaneerimisega* .)
1. Järgige üht järgmistest sammudest, sõltuvalt sellest, kas kasutate **partiitööde** lehe puhul *täiustatud vormi* või *pärandi (muutmata) vormi*.

    - Kui kasutate täiustatud vormi: valige tegevuspaanil **Partiitöö ajalugu**. Seejärel valige **Partiitöö ajalugu** lehel tegevuspaanil **Logi**.
    - Kui kasutate pärandvormi: valige tegevuspaani vahekaardil **Partiitöö** **Logi**.

1. Valige **Teate üksikasjad**, et avada **Teate üksikasjade** paan, kus saate vaadata kõiki hoiatusi ja tõrkeid, mis talletati töötlemise ajal.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
