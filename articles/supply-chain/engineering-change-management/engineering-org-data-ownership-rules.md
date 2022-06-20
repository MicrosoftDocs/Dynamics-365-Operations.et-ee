---
title: Tehnikaettevõtted ja andmete omandiõiguse reeglid
description: See artikkel selgitab, kuidas ühte või enamat tehnikafirmat kasutada, et tagada toodete koondandmete loomine ja haldamine keskselt. Tehnikaettevõte esindab ettevõtet, mis omab tehnilisi tooteid ja tehnilisi andmeid.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47662203669d5dd466990be397c9a4aaf1dd9932
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875535"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Tehnikaettevõtted ja andmete omandiõiguse reeglid

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Tehnikaettevõtted ja operatiivettevõtted

Tagamaks, et toodete koondandmeid luuakse ja hallatakse keskselt, saate kasutada ühte või enamat *tehnikaettevõtet*. Tehnikaettevõte omab tehnilisi tooteid ja nende tehnilisi andmeid. See on alati seotud olemasoleva *juriidilise isikuga*, mis on samuti ettevõte (põhineb sellel). Selle ühenduse kaudu loob süsteem kõigi tehnikaettevõtte tehniliste toodete tehniliste andmete jaoks keskse lähtepunkti. Selles keskses lähtepunktis luuakse tehnilised tooted ja hallatakse tehnilisi andmeid. Sellest väljastatakse tehnilised tooted ja seotud andmed *operatiivettevõtetele*, mis on teised juriidilised isikud. (Lisateavet väljastamise halduse kohta leiate teemast [Tootestruktuuride väljastamine](release-product-structure.md).) Need operatiivettevõtted kasutavad neid tehnilisi andmeid, mille on loonud tehnikaettevõte. Kõiki logistilisi andmeid haldavad kohapeal iga tehnika- ja operatiivettevõte.

Tehnikaettevõtte loomiseks minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Tehnikaorganisatsioonid**. Valige **Uus**, sisestage tehnikaettevõtte nimi ja valige olemasolev ettevõte (juriidiline isik), millel see põhineb.

Kui integreerite väliste toote elutsükli halduse (PLM) süsteemidega, tuleb luua äriüksus (ettevõttetüüp), millest saab väline ettevõte.

## <a name="engineering-product-categories-and-engineering-companies"></a>Tehnilise toote kategooriad ja tehnikaettevõtted

*Tehnilise toote kategooriad* aitavad tagada, et tehnilised tooted luuakse vastavalt teie ettevõtte ärireeglitele ja käituvad vastavalt vajadusele. Lisateavet tehniliste toodete kategooriate kohta leiate teemast [Tehnilised versioonid ja tehniliste toodete kategooriad](engineering-versions-product-category.md).

Iga tehnilise toote kategooria kuulub konkreetsele tehnikaettevõttele ja selle alusel võib luua ainult sellele ettevõtte kuuluvaid tooteid. Tehnilise toote haldamise õigus kuulub samuti ettevõttele, mis on seotud selle toote tehnilise toote kategooriaga.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Andmed, mis kuuluvad tehnikaettevõttele

Kuna tehnikaettevõte omab tehnilisi andmeid, haldab see järgmisi protsesse.

- **Tehniliste toodete loomine:** iga tehnikaettevõte saab luua ainult selliseid uusi tehnilisi tooteid, mis põhinevad tehnilise toote kategoorial, mida ettevõte omab. Mõnel juhul säilitavad operatiivettevõtted oma kohalikke andmeid, mis on seotud selliste toodetega.
- **Tehniliste versioonide loomine:** kui ettevõte loob uue tehnilise toote, loob süsteem automaatselt selle jaoks algse tehnilise versiooni. Ainult omanikust tehnikaettevõte saab luua selle toote uusi versioone.
- **Tehniliste atribuutide loomine ja haldamine:** kui ettevõte loob uue tehnilise toote, lisab süsteem automaatselt sellele tehnilised atribuudid. Ainult omanikust tehnikaettevõte saab luua ja hallata selliste atribuutide väärtusi. Lisateavet tehniliste atribuutide kohta leiate jaotisest [Tehnilised atribuudid ja tehnilise atribuudi otsing](engineering-attributes-and-search.md).
- **Tehniliste versioonidega ühendatud koosluste (BOM-id) loomine ja haldamine:** omanikust tehnikaettevõte saab koosluse ühendada otse iga tehnilise tooteversiooniga. Kui need kooslused suunatakse edasi teistele juriidilistele isikutele, on koosluste tehniliste andmete muudatused piiratud järgmistel viisidel.

    - Operatiivettevõte ei saa väljastatud koosluseridu eemaldada.
    - Koosluseridade tehnilisi välju saab operatiivettevõtte ainult lugeda. Kõik teised väljad on logistilised rakendamisväljad ja neid saab muuta operatiivettevõte.
    - Operatiivettevõte saab lisada koosluseridu samale kooslusele. Sel viisil saab ta lisada kohalikke täiendusi, nt pakkematerjale või määrimisvedelikke.
    - Operatiivettevõte saab lisada täiesti uue kohaliku koosluse. See muudatus võib vajalik olla juhul, kui väljastamise ajal ei määrata kooslust. Operatiivettevõte omab ja haldab neid kohalikke kooslusi. Lisateavet väljastamise haldamise kohta leiate teemast [Tootestruktuuride väljastamine](release-product-structure.md).
    - Kõik kohalikud kooslused ja koosluseread säilitatakse, kui tehnikaettevõte uuendab oma kooslust.

- **Tehniliste versioonidega ühendatud protsesside loomine ja haldamine:** tehnikaettevõte saab protsessi ühendada otse iga tehnilise versiooniga. Kui need protsessid suunatakse edasi teistele juriidilistele isikutele, on protsessi tehniliste andmete muudatused piiratud järgmistel viisidel.

    - Teised juriidilised isikud ei saa eemaldada protsesside tehnilisi andmeid.
    - Teised juriidilised isikud saavad protsessile toiminguid lisada. Sel viisil saavad nad lisada kohalikke protsessietappe.
    - Operatiivettevõtted saavad lisada täiesti uusi kohalikke protsesse. See muudatus võib vajalik olla juhul, kui väljastamise ajal ei kaasatud protsesse. Operatiivettevõtted omavad ja haldavad neid kohalikke protsesse. Lisateavet väljastamise haldamise kohta leiate teemast [Tootestruktuuride väljastamine](release-product-structure.md).
    - Kõik kohalikult tehtud muudatused säilitatakse, kui tehnikaettevõtte värskendused väljastatakse uuesti protsesside jaoks.

- **Tehniliste dokumentide loomine ja haldamine:** tehnikaettevõtte saab lisada tehnilisi dokumente igale tehnilisele versioonile.

    - Kui need dokumendid väljastatakse teistele juriidilistele isikutele, ei saa operatiivettevõte dokumente eemaldada.
    - Teised juriidilised isikud saavad lisada täiesti uusi kohalikke dokumente. Operatiivettevõte omab ja haldab neid kohalikke dokumente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]