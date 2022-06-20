---
title: Arveridade loomine hankija arvete importimisel
description: See artikkel kirjeldab arvete importimisel hankija arvetele arveridade automaatse loomise funktsiooni.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e745ab1fb39edf69fabd147e46e1da8cc98ba6e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903503"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Arveridade loomine hankija arvete importimisel

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel kirjeldab arvete importimisel hankija arvetele arveridade automaatse loomise funktsiooni.

Mõnikord sisaldavad hankija arved piiratud teavet, nt saaja teavet ja vahesummasid. Need ei sisalda aga reaüksuste teavet. Arvete importimisel luuakse arveread automaatselt vastava ostutellimuse teabe alusel.

Arveridade automaatse loomise lubamiseks järgige neid samme.

1.  Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
2.  Vahekaardil **Hankija arve automatiseerimine** jaotises **Automaatne rea loomine imporditud arvete jaoks** seadke **Automaatselt arveridade loomine** väärtusele **Jah**. 
4.  **Väljal Vali arveridade loomise vaikekogus** valige kogus, mida tuleks kasutada arveridade automaatseks loomiseks.

    - **Tellitud kogus** – read luuakse ostutellimuse ridadest. See on väärtus on vaikeväärtus.
    - **Toote sissetuleku kogus** – ostutellimuste numbrit kasutatakse vastavate toote sissetulekute leidmiseks. Seejärel kasutab see arve ridade loomiseks toote sissetuleku koguseid.

## <a name="data-entity-changes"></a>Andmeüksuse muudatused

Selles artiklis kirjeldatud funktsioonide toetamiseks on hankija **arve päise andmeüksus** täiustatud. Lisatud on kolm välja:

- **HeaderOnlyImport** – arve päiste ridade loomiseks **tuleb** selle välja väärtuseks seada Jah.
- **PurchIdRange** – ostutellimuste numbrite loend. Arvenumbrid võivad olla vahemikus nagu näiteks **INV0001..INV0009** (kus kaks punkti eraldavad vahemiku algust ja lõppu) või diskreetsed väärtused, nagu näiteks **INV0001, INV0003, INV0006**. Kõik ostutellimused peavad kuuluma arve päises samale hankijakontole. Vastasel juhul kuvatakse järgmine tõrketeade: "Arveridade loomine nurjus. Ostutellimustel on erinevad hankijakontod."
- **PackingslipRange** – toote sissetuleku numbrite loend. Hankija arve ridu saab luua toote sissetulekutest. Toote sissetuleku numbreid pole hankija arvetel tavaliselt kaasatud. Sisestage toote sissetuleku numbrid sellele väljale ainult siis, kui saate selgelt määratleda, millised toote sissetulekud on milliste konkreetsete arvete jaoks. Arve ridu saab luua toote laekumiste põhjal. Selle välja kasutamisel ignoreeritakse **ostureskontro** **parameetrite lehel välja Vali vaikekogus** automaatse arve ridade loomiseks. 

**Piirang**: kui sisestate mitu toote sissetuleku numbrit, luuakse mitu ootel hankija arvet sama arvenumbriga. Enne arve edasi töötlemist peate need käsitsi konsolideerima. Tulevastes väljalasetes plaanime arveid automaatselt konsolideerida, nii et piirang eemaldatakse.

Kõik otoote laekumised peavad kuuluma arve päises samale hankijakontole.

## <a name="result"></a>Tulemus

Kui read on edukalt loodud, logitakse hankija arve automatiseerimise ajaloos järgmine teade: "Arveridade automaatne loomine: õnnestus."

Kui ridu ei loo, logitakse järgmine tõrketeade: "Arveridade automaatne loomine nurjus."
