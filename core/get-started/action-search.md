---
title: Tegevuse otsing
description: "Selles artiklis kirjeldatakse Microsoft Dynamics 365 operatsioonide tegevuse allalaadimisfunktsioon. Toimingu Otsi abil saate leida ja käivitada tegevusi lehele."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 689d8f9fb0501c5007db21d41f126737af77b89e
ms.lasthandoff: 03/31/2017


---

# <a name="action-search"></a>Tegevuse otsing

Selles artiklis kirjeldatakse Microsoft Dynamics 365 operatsioonide tegevuse allalaadimisfunktsioon. Toimingu Otsi abil saate leida ja käivitada tegevusi lehele.

<a name="introduction"></a>Sissejuhatus
------------

Leheküljed Microsoft Dynamics 365 operatsioonide paljastada peamiselt tegevus paane, standard Updatehagi paani, mis kuvatakse lehe ülaosas ja tööriistaribad, mis esinevad erinevate osade lehekülje käske. Varasemas versioonis klahvinäpunäideteks funktsiooni abil saate kiiresti avada Updatehagi paani nupule vajutades muuteklahvi (Alt) ja seejärel tähed. 

[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png) Dynamics 365 operatsioonide praeguses versioonis klahvinäpunäideteks enam kuid asendus tegevus otsingufunktsiooni. See uus funktsioon võimaldab kiiret otsingut ja nupu käivitamist mis tahes nähtavalt tegevuspaanilt.

## <a name="using-action-search"></a>Tegevus otsingu kasutamine
Tegevuse otsingu funktsiooni kasutamiseks toimige järgmiselt.

1.  Klõpsake tegevuspaani välja **tegevuse otsing**. (Väli **Tegevuse otsing** sisaldab suurendusklaasi ikooni.)
2.  Tippige või nuppu, mida soovite käivitada nime. Võite ka otsida kasutades sõnu nupu "tee." (Lisateabe saamiseks vt käesoleva artikli järgmises osas). Tavaliselt nupp ilmub tulemuste nimekirja tipus pärast sisestatud kaks kuni neli märki.
3.  Otsige nupp tulemuste loendist üles ja käivitage see (kasutades hiirt ja klaviatuuri).

Pärast nupu käivitamist naaseb fookus lehe viimasesse asukohta ja saate tööd jätkata. 

[![välja-tegevus-Otsi](./media/action-search-field.png)](./media/action-search-field.png)

Saate tegevuste otsingu käivitada ka, vajutades klahve Ctrl+/ või Alt+Q. Vajutage uuesti kiirklahvi, et fookus naaseks teie viimasele lehe asukohale.

## <a name="understanding-the-results-list"></a>Tulemuste loendi mõistmine
Sageli Dynamics 365 toiminguteks, peab teadma nii asukoha kui ka nupp täielikult mõista seda nuppu eesmärk seoses. Seetõttu täiendavat teavet kuvatakse tulemite loendis iga kauba aitab teil mõista täpselt mis nupud kuvatakse loendis. Eriti kuvatakse nupu tee. Tee võib vajaduse korral hõlmata järgmiste kasutajaliidese elementide silte.

-   Toimingupaani vahekaart
-   Nupu grupp
-   Menüünupp (kui nupp on menüünupu sees)
-   Menüü eraldaja (kui nupp on menüünupu sees nimega grupis)
-   Grupp või vahekaart lehel (näiteks kiirkaardi nimi)

Tippisite väljale **Tegevuse otsing** näiteks tähed **kog** ja uurite nüüd tulemuste loendit. Esimene kanne, nupp, mille nimi on **kokku**, on esile tõstetud. Nuppu tee **Müügitellimus**&gt;**View** on samuti esitatud. On **Müügitellimus** tee osa vastab selle **Müügitellimus** Updatehagi paani vahekaarti ja **View** tee osa vastab selle **View** rühm sellele kaardile. Samamoodi tee selle **lõppallahindluse** nuppu (**müüa**&gt;**Arvuta**) annab teada, et see nupp asub selle **Arvuta** rühma kohta ning **müüa** Updatehagi paani vahekaarti. Seetõttu, see teave aitab teil mõista täpselt ei millist nuppu Käivita toimingu Otsi (kui selle nupu klõpsamist tulemuste loendis). 

[![Action-Otsi--koos-andmete](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png) 

Eelmises näites näitas tegevuse otsing tulemusi standardselt toimingupaanilt lehe ülaosas. Kuid tegevuse otsing näitab ka tulemusi nähtamatutelt tööriistaribadelt, mis asuvad lehe muudes kohtades. Näiteks otsite selle **vaba kaubavaru** nuppu, mis asub selle **müügitellimuse read** FastTab. Antud juhul tulemuste loendis nuppu tee (**müügitellimuse read**&gt;**varude**&gt;**View**) annab teada, et see nupp asub selle **View** päise kohta on **varude** nuppu ning **müügitellimuse read** FastTab. 

[![linna vaba kaubavaru](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)

## <a name="action-search-vs-navigation-search"></a>Tegevuse otsing vs navigeerimisotsing
Meetmete otsingu eesmärk on leida ja käivitada tegevusi lehele, seal on eraldi mehhanism leida ja kasutada lehekülge Dynamics 365 toiminguteks. Selle funktsiooni kohta lisateabe saamiseks vt ka [Navigation otsing](navigation-search.md) artikli.


