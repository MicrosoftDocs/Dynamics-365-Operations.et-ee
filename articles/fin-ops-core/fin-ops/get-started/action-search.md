---
title: Tegevuse otsing
description: Selles artiklis kirjeldatakse tegevuse otsingu funktsiooni. Tegevuste otsing aitab teil leida ka käitada lehel tegevusi.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb268c2643b45f6797793dbc5b7cc2e33d5218d9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564210"
---
# <a name="action-search"></a>Tegevuse otsing

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse tegevuse otsingu funktsiooni. Tegevuste otsing aitab teil leida ka käitada lehel tegevusi.

## <a name="introduction"></a>Sissejuhatus

Lehed kuvavad käsklusi peamiselt toimingupaanidel – nii standardsel toimingupaanil, mis kuvatakse lehe ülaosas, kui ka tööriistaribadel, mis kuvatakse lehe erinevates jaotistes. Varasemates versioonides võimaldas klahvinäpunäidete funktsioon teil toimingupaani mis tahes nupule kiiresti juurde pääseda, vajutades Alt-klahvi ja seejärel tähejada.

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)

Tegevuse otsingu funktsioon asendab näpunäited, mis pole enam saadaval. See uus funktsioon võimaldab kiiret otsingut ja nupu käivitamist mis tahes nähtavalt tegevuspaanilt.

## <a name="using-action-search"></a>Tegevus otsingu kasutamine

Tegevuse otsingu funktsiooni kasutamiseks toimige järgmiselt.

1. Klõpsake tegevuspaani välja **tegevuse otsing**. (Väli **Tegevuse otsing** sisaldab suurendusklaasi ikooni.)
2. Tippige osaliselt või täielikult nupu nimi, mille soovite käivitada. Saate otsimiseks kasutada ka nupu „tees” olevaid sõnu, (Lisateavet vt selle artikli järgmisest teemast.) Tavaliselt ilmub nupp tulemuste loendi lähedale pärast kahe kuni nelja tähemärgi tippimist.
3. Otsige nupp tulemuste loendist üles ja käivitage see (kasutades hiirt ja klaviatuuri).

Pärast nupu käivitamist naaseb fookus lehe viimasesse asukohta ja saate tööd jätkata.

[![tegevuse-otsinguväli](./media/action-search-field.png)](./media/action-search-field.png)

Saate tegevuste otsingu käivitada ka, vajutades klahve Ctrl+/ või Alt+Q. Vajutage uuesti kiirklahvi, et fookus naaseks teie viimasele lehe asukohale.

## <a name="understanding-the-results-list"></a>Tulemuste loendi mõistmine

Sageli peate teadma nupu otstarbe mõistmiseks nii nupu asukohta kui ka konteksti. Seetõttu kuvatakse tulemuste loendis lisateave, et saaksite täpselt aru, millised nupud loendis kuvatakse. Eriti kuvatakse nupu tee. Tee võib vajaduse korral hõlmata järgmiste kasutajaliidese elementide silte.

- Toimingupaani vahekaart
- Nupu grupp
- Menüünupp (kui nupp on menüünupu sees)
- Menüü eraldaja (kui nupp on menüünupu sees nimega grupis)
- Grupp või vahekaart lehel (näiteks kiirkaardi nimi)

Tippisite väljale **Tegevuse otsing** näiteks tähed **kog** ja uurite nüüd tulemuste loendit. Esimene kirje (nupp **Kogusummad**) on esile tõstetud. Kuvatakse ka nupu tee **Müügitellimus** &gt; **Vaade**. Tee osa **Müügitellimus** vastab tegumiriba vahekaardile **Müügitellimus** ja tee osa **Vaade** vastab selle vahekaardi rühmale **Vaade**. Samamoodi annab nupu **Koguallahindlus** tee (**Müü** &gt; **Arvuta**) teile teada, et see nupp asub tegumiriba vahekaardi **Müü** grupis **Arvuta**. Seetõttu aitab see teave teil täpselt aru saada, milline nupp tegevuseotsinguga käivitatakse (kui valite selle nupu tulemuste loendist).

[![tegevuste-otsinguväli-koos-andmetega](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)

Eelmises näites näitas tegevuse otsing tulemusi standardselt toimingupaanilt lehe ülaosas. Kuid tegevuse otsing näitab ka tulemusi nähtamatutelt tööriistaribadelt lehe muudes kohtades. Näiteks otsite nuppu **Vaba kaubavaru**, mis on kiirkaardil **Müügitellimuse read**. Sellisel juhul teavitab nupu tee tulemuste loendis (**Müügitellimuse read** &gt; **Varud** &gt; **Vaade**), et see nupp on kiirkaardil **Müügitellimuse read** menüünupu **Varud** päise **Vaade** all.

[![vaba-kaubavaru](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

> [!NOTE]
> Osa nuppe tegevuse otsingus ei kuvata. Need hõlmavad kukutatava dialoogi nuppe ja alamvormide nuppe. 

## <a name="action-search-vs-navigation-search"></a>Tegevuse otsing vs navigeerimisotsing

Kui tegevuseotsing on mõeldud tegevuste otsimiseks ja käivitamiseks lehel, siis lehtede otsimiseks ja neil navigeerimiseks on eraldi otsingumehhanism. Lisateavet selle funktsiooni kohta vt artiklist [Navigeerimisotsing](navigation-search.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]