---
title: Otsing varudest kassas
description: Selles teemas kirjeldatakse võimalusi, mis on saadaval varude teabe vaatamiseks kassas.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: f08906c14f80b07368d88d820acae83cf1157e6c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969947"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Otsing varudest kassas

[!include [banner](includes/banner.md)]

Otsing varudest kassas aitab jaemüüjatel reaalajas saavutada kõrget töökvaliteeti ning saada ülevaateid kaupluste, kassa ja varukontori ühendamise teel. See funktsiooni annab täpse reaalajas vaate toote varudest kauplustes ja turustuskeskustes. Samuti aitab see jaemüüjatel suurendada tõhusust ja säästlikkust, tõhustades varude planeerimist reaalajas.

Täpne reaalajas ülevaade varudest kogu organisatsioonis aitab kaupluste töötajatel pakkuda kiiret ja tõhusat klienditeenindust. Kõige tähtsam hetk on see, mil klient on valmis tegema ostuotsust. On tähtis, et kaupluse kassapidajatel oleks varude reaalajas teave käeulatuses, et nad saaksid pakkuda täpseid toote tarne ja komplekteerimise aegu.

Saate avada lehe **Otsing varudest** tööruumist **Retail Modern POS** või tööruumist **Jaemüügi pilvekassa**.

![Varude otsingupaan kassa avalehel](media/POSHomepage.png)

Lehel **Otsing varudest** saate kasutada numbriklaviatuuri tootenumbri sisestamiseks. Saate vaadata laos olevat kogust mitme kaupluse ja lao kohta.

![Standardne varude otsingu leht](media/InventoryLookUp.png)

Iga asukoha kohta kuvatakse ka **reserveeritud** ja **tellitud** kogused.

- **Reserveeritud** – see kogus viitab **füüsiliselt reserveeritud** väärtusele varukontorist määratud tootenumbri kohta asukohas.
- **Tellitud** – see kogus viitab **kokku tellitud** väärtusele varukontorist määratud tootenumbri kohta asukohas.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Asukohad, mille kohta kuvatakse varude saadavuse teave

Asukohtade loend sisaldab kahte järgmist tüüpi üksuseid.

- **Kauplused** – selles loendis kuvatakse kauplused, mille konfigureerimiseks on kasutatud kaupluselokaatori gruppi praeguse kaupluse jaoks komponendis Headquarters.
- **Jaotuskeskused** – rakenduses Commerce saab konfigureerida erinevaid jaotuskeskuseid (nt ladusid). Kuid loendis kuvatakse varude saadavuse teave ainult jaotuskeskuste kohta, mille vaiketüüp on **Standardne**.

    > [!NOTE]
    > Varude saadavuse teavet ei kuvata ladude kohta, mille kassatüüp on **Transiit**, **Vaheladu** ja **Kaubad töötemisel**.

Lehel **Otsing varudest** saate iga kaupluse kohta lisaks praeguse vaba kaubavaru, reserveeritud koguste ja tellitud koguste teabele vaadata ka lubamiseks saadaval (ATP) koguseid. Valige kauplus, mille ATP teavet soovite vaadata, ja seejärel valige **Kaupluse saadavuse kuvamine**.

![ATP-i kogused](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Dimensioonipõhise maatriksvaate avamine kõigi variantide kuvamiseks

Tooteetaloni lehel **Toote üksikasjad** või lehel **Otsing varudest** valige lehe allosas rakenduste realt suvand **Kõigi variantide kuvamine**. Nende lehtede esmasel avamisel avanev vaade **Dimensioonipõhine maatriks** kuvab varude saadavuse teabe toote kõigi variantide kohta praeguses kaupluses.

> [!NOTE]
> Nupp **Kõigi variantide kuvamine** on saadaval ainult kauba tooteetalonide korral, millel on tootevariandid. See pole saadaval eraldiseisvate toodete või komplektide korral.

![Kõigi variantide kuvamise nupp lehel Otsing varudest](media/StandardToMatrix.png)

Valige suvand **Kõigi variantide kuvamine** tooteetaloni lehel **Toote üksikasjad** või lehel **Otsing varudest** ilma asukohta valimata, et avada vaade **Dimensioonipõhine maatriks**, et vaadata varude saadavuse teavet toote kõigi variantide kohta praeguses kaupluses.

![Dimensioonipõhise maatriksi vaade lehel Otsing varudest](media/Matrix.png)

> [!NOTE]
> Eelmises näites on dimensioonide kuvamisjärjestus alfabeetiline, sest dimensioonide kuvamisjärjestust ei konfigureeritud valitud toote jaoks.

Vaates **Dimensioonipõhine maatriks** sisaldavad tootevariantide lahtrid parempoolses allnurgas vaba laoseisu väärtust. Järgmises tabelis selgitatakse erinevate väärtuste tähendust.

| Laoseisu väärtus                            | Kirjeldus |
|------------------------------------------|-------------|
| Numbriline väärtus, mis on suurem kui 0 (null) | Variant on väljastatud valitud asukoha jaoks ja te saate lahtris teha täiendavaid toiminguid. (Neid toiminguid kirjeldatakse üksikasjalikumalt selles teemas allpool.) |
| **0** (null)                             | Variant on väljastatud valitud asukoha jaoks, kuid kaup pole valitud asukohas saadaval. Saate siiski teha lahtris täiendavaid toiminguid. (Neid toiminguid kirjeldatakse üksikasjalikumalt selles teemas allpool.) |
| **p/s** või passiivne lahter              | Varianti pole valitud asukoha jaoks väljastatud ja te ei saa lahtris täiendavaid toiminguid teha. |

Saate muuta ka dimensioonide liigendust, valides kasutamiseks uue dimensiooni.

![Liigenduse muutmine](media/ChangePivot.png)

![Liigendus on muudetud](media/PivotChanged.png)

> [!NOTE]
> Eelmisel illustratsioonidel on valitud toote dimensioonide kuvamisjärjestuse kohandatud (mittealfabeetiline). See põhineb varukontoris määratud dimensioonide kuvamisjärjestusel.

Peale selle saab vaates **Dimensioonipõhine maatriks** teha rohkem toiminguid, et suurendada kaupluse töötaja tööviljakust. Järgmisena on toodud mõned näited.

- Muutke kaupluse asukohta, et vaadata varude saadavust kõigi tootevariantide korral muudes asukohtades. Need asukohad hõlmavad teisi kauplusi kaupluselokaatori grupis ja jaotuskeskuseid vaiketüübiga **Standardne**.
- Müüge üksik tootevariant kliendile, kasutades sularaha, kauplusesse järeletulemist või saatmist aadressile.
- Andke kliendile ATP teave üksiku tootevariandi kohta kindlas asukohas.

![Täiendavad toimingud variandi paanidega](media/VariantActions.png)

> [!NOTE]
> Eelmises näites on dimensioonide kuvamisjärjestus alfabeetiline, sest dimensioonide kuvamisjärjestust ei konfigureeritud valitud toote jaoks.

Järgnevast tabelist leiate lisateavet võimalike lisatoimingute kohta.

| Tegevus               | Kirjeldus |
|----------------------|-------------|
| Müü kohe             | Lisage valitud kaubavariant kandele ja suunake kasutaja kandekuvale. (See toiming pole saadaval, kui valitud asukoht on jaotuskeskus.) |
| Kauplusesse järeletulemine     | Looge klienditellimus tootevariandi jaoks, millele tullakse valitud asukohta järele, ja suunakse kasutaja kandekuvale. (See toiming pole saadaval, kui valitud asukoht on jaotuskeskus.) |
| Toote lähetus         | Looge klienditellimus tootevariandi jaoks, mis saadetakse valitud asukohast, ja suunakse kasutaja kandekuvale. |
| Kättesaadavus         | Näidake ATP teavet valitud variandi kombinatsiooni kohta valitud asukoha jaoks. |
| Kõigi asukohtade kuvamine   | Valige standardne varudest otsimise vaade ja tõstke esile varude saadavuse teave kaubavariandi kohta kõigis kauplustes kaupluselokaatori grupis ja ka jaotuskeskustes, mille tüüp on **Standardne/Vaikimisi**. |
| Kuva toote üksikasjad | Suunake kasutaja seostatud tooteetaloni lehele **Toote üksikasjad**. |
