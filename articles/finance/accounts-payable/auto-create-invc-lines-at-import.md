---
title: Arveridade loomine hankija arvete importimisel
description: Selles teemas kirjeldatakse arvete importimisel hankija arvetele arveridade automaatse loomise funktsiooni.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 87dec3c142ae296975ab98432421be4548085c80
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647883"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Arveridade loomine hankija arvete importimisel

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas kirjeldatakse arvete importimisel hankija arvetele arveridade automaatse loomise funktsiooni.

Mõnikord sisaldavad hankija arved piiratud teavet, nt saaja teavet ja vahesummasid. Need ei sisalda aga reaüksuste teavet. Arvete importimisel saab süsteem vastava ostutellimuse teabe põhjal arveread automaatselt luua.

Arveridade automaatse loomise lubamiseks järgige neid samme.

1.  Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
2.  Vahekaardil **Hankija arve automatiseerimine** jaotises **Automaatne rea loomine imporditud arvete jaoks** seadke **Automaatselt arveridade loomine** väärtusele **Jah**. 
4.  Väljal **Valige vaikimisi arveridade automaatseks loomiseks** valige kogus, mida süsteem peaks kasutama arveridade automaatseks kasutamiseks:

    - **Tellitud kogus** – süsteem loob read ostutellimuse ridadest. See on väärtus on vaikeväärtus.
    - **Toote sissetuleku kogus** – süsteem kasutab ostutellimuste numbreid vastavate toote sissetulekute leidmiseks. Seejärel kasutab see arve ridade loomiseks toote sissetuleku koguseid.

## <a name="data-entity-changes"></a>Andmeüksuse muudatused

Selles teemas kirjeldatud funktsioonide toetamiseks on täiustatud **hankija arve päise** andmeüksust. Lisatud on kolm välja:

- **HeaderOnlyImport** – arve päiste ridade loomiseks peab süsteem olema seatud väärtusele **Jah**.
- **PurchIdRange** – ostutellimuste numbrite loend. Arvenumbrid võivad olla vahemikus nagu näiteks **INV0001..INV0009** (kus kaks punkti eraldavad vahemiku algust ja lõppu) või diskreetsed väärtused, nagu näiteks **INV0001, INV0003, INV0006**. Kõik ostutellimused peavad kuuluma arve päises samale hankijakontole. Vastasel juhul kuvatakse järgmine tõrketeade: "Arveridade loomine nurjus. Ostutellimustel on erinevad hankijakontod."
- **PackingslipRange** – toote sissetuleku numbrite loend. Hankija arve ridu saab luua toote sissetulekutest. Toote sissetuleku numbreid pole hankija arvetel tavaliselt kaasatud. Sisestage toote sissetuleku numbrid sellele väljale ainult siis, kui saate selgelt määratleda, millised toote sissetulekud on milliste konkreetsete arvete jaoks. Arve ridu saab luua toote laekumiste põhjal. Ja selle välja kasutamisel ignoreeritakse **Vali vaikekogus automaatse arve ridade** välja seadeid **ostureskontro parameetrite** lehel. 

**Piirang**: kui sisestate mitu toote sissetuleku numbrit, luuakse mitu ootel hankija arvet sama arvenumbriga. Enne arve edasi töötlemist peate need käsitsi konsolideerima. Tulevastes väljalasetes plaanime lubada süsteemil arveid automaatselt konsolideerida, nii et piirang eemaldatakse.

Kõik otoote laekumised peavad kuuluma arve päises samale hankijakontole.

## <a name="result"></a>Tulemus

Kui süsteem loob read edukalt, logitakse hankija arve automatiseerimise ajaloos järgmine teade: "Arveridade automaatne loomine: õnnestus."

Kui süsteemil ebaõnnestub ridade loomine, logitakse järgmine tõrketeade: "Arveridade automaatne loomine nurjus."
