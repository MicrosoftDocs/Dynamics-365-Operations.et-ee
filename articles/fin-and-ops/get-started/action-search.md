---
title: Tegevuse otsing
description: "See artikkel kirjeldab tegevuste otsingu funktsioone rakenduses Microsoft Dynamics 365 for Finance and Operations. Tegevuste otsing aitab teil leida ka käitada lehel tegevusi."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b9bb0acc6f0dc1722c916f133eed766ffdd4cc8
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="action-search"></a>Tegevuse otsing

[!include[banner](../includes/banner.md)]


See artikkel kirjeldab tegevuste otsingu funktsioone rakenduses Microsoft Dynamics 365 for Finance and Operations. Tegevuste otsing aitab teil leida ka käitada lehel tegevusi.

<a name="introduction"></a>Sissejuhatus
------------

Microsoft Dynamics 365 for Finance and Operationsi lehed kuvavad käsklusi peamiselt toimingupaanidel, nii standardsel toimingupaanil, mis kuvatakse lehe ülaosas, kui ka tööriistaribadel, mis kuvatakse lehe erinevates jaotistes. Varasemates versioonides võimaldas klahvinäpunäidete funktsioon teil toimingupaani mis tahes nupule kiiresti juurde pääseda, vajutades Alt-klahvi ja seejärel tähejada. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Finance and Operationsi praeguses versioonis pole klahvinäpunäited aga enam saadaval, kuid need on asendatud tegevuse otsimise funktsiooniga. See uus funktsioon võimaldab kiiret otsingut ja nupu käivitamist mis tahes nähtavalt tegevuspaanilt.

## <a name="using-action-search"></a>Tegevus otsingu kasutamine
Tegevuse otsingu funktsiooni kasutamiseks toimige järgmiselt.

1.  Klõpsake tegevuspaani välja **tegevuse otsing**. (Väli **Tegevuse otsing** sisaldab suurendusklaasi ikooni.)
2.  Tippige osaliselt või täielikult nupu nimi, mille soovite käivitada. Saate otsimiseks kasutada ka nupu „tees” olevaid sõnu, (Lisateavet vt selle artikli järgmisest teemast.) Tavaliselt ilmub nupp tulemuste loendi lähedale pärast kahe kuni nelja tähemärgi tippimist.
3.  Otsige nupp tulemuste loendist üles ja käivitage see (kasutades hiirt ja klaviatuuri).

Pärast nupu käivitamist naaseb fookus lehe viimasesse asukohta ja saate tööd jätkata. 

[![tegevuse-otsinguväli](./media/action-search-field.png)](./media/action-search-field.png)

Saate tegevuste otsingu käivitada ka, vajutades klahve Ctrl+/ või Alt+Q. Vajutage uuesti kiirklahvi, et fookus naaseks teie viimasele lehe asukohale.

## <a name="understanding-the-results-list"></a>Tulemuste loendi mõistmine
Sageli peate Finance and Operationsis teadma nupu otstarbe mõistmiseks nii nupu asukohta kui ka konteksti. Seetõttu kuvatakse tulemuste loendis iga üksuse puhul lisateave, et saaksite täpselt aru, millised nupud loendis kuvatakse. Eriti kuvatakse nupu tee. Tee võib vajaduse korral hõlmata järgmiste kasutajaliidese elementide silte.

-   Toimingupaani vahekaart
-   Nupu grupp
-   Menüünupp (kui nupp on menüünupu sees)
-   Menüü eraldaja (kui nupp on menüünupu sees nimega grupis)
-   Grupp või vahekaart lehel (näiteks kiirkaardi nimi)

Tippisite väljale **Tegevuse otsing** näiteks tähed **kog** ja uurite nüüd tulemuste loendit. Esimene kirje (nupp **Kogusummad**) on esile tõstetud. Kuvatakse ka nupu tee **Müügitellimus** &gt; **Vaade**. Tee osa **Müügitellimus** vastab tegumiriba vahekaardile **Müügitellimus** ja tee osa **Vaade** vastab selle vahekaardi rühmale **Vaade**. Samamoodi annab nupu **Koguallahindlus** tee (**Müü** &gt; **Arvuta**) teile teada, et see nupp asub tegumiriba vahekaardi **Müü** grupis **Arvuta**. Seetõttu aitab see teave teil täpselt aru saada, milline nupp tegevuseotsinguga käivitatakse (kui valite selle nupu tulemuste loendist). 

[![tegevuste-otsinguväli-koos-andmetega](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Eelmises näites näitas tegevuse otsing tulemusi standardselt toimingupaanilt lehe ülaosas. Kuid tegevuse otsing näitab ka tulemusi nähtamatutelt tööriistaribadelt, mis asuvad lehe muudes kohtades. Näiteks otsite nuppu **Vaba kaubavaru**, mis asub kiirkaardil **Müügitellimuse read**. Sellisel juhul teavitab nupu tee tulemuste loendis (**Müügitellimuse read** &gt; **Varud** &gt; **Vaade**), et see nupp asub kiirkaardil **Müügitellimuse read** menüünupu **Varud** päise **Vaade** all. 

[![vaba-kaubavaru](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Tegevuse otsing vs navigeerimisotsing
Kui tegevuseotsing on mõeldud tegevuste otsimiseks ja käivitamiseks lehel, siis lehtede otsimiseks ja neil navigeerimiseks on Finance and Operationsis eraldi otsingumehhanism. Lisateavet selle funktsiooni kohta vt artiklist [Navigeerimisotsing](navigation-search.md).




