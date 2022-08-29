---
title: RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine
description: See artikkel kirjeldab, kuidas luua uus aruandekonfiguratsioon, mis sisaldab rakenduse metaandmeid.
author: kfend
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: a9ccbb120be43eaf7a8ae8b5bf8eaafb4850b199
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289970"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine
[!include [banner](../../includes/banner.md)]

Järgnevad juhised selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab rakenduse metaandmeid, et kujundada elektroonilise aruandluse mudelivastenduse konfiguratsioone teenuses Regulatory configuration service (RCS). Seda konfiguratsiooni kasutatakse elektroonilise mudelivastenduse näite konfiguratsiooni kujundamiseks väliskaubanduse kannetele juurdepääsemiseks. Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes. Nende sammude lõpuleviimiseks peate esmalt täitma artikli sammud, [looma konfiguratsiooni pakkujad ja märkima need aktiivseks](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Eeltingimused
1.    Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**. 
2.    Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised. 
3.    Klõpsake valikut **Metaandmete konfiguratsioonid**. 
4.    Oletame, et RCS-i kasutatakse rakenduse Finance and Operation ER-lahenduse kujundamiseks, mis loob elektroonilisi dokumente, mis sisaldavad väliskaubanduse äritegevuse domeeni teavet. ER-i andmemudeli ja nõutavate andmete allikate vahelise vastendamise määramiseks peab meil RCS-is olema ligipääs rakenduse Finance and Operation metaandmetele. Seega konfigureerime ER-lahenduse projekteerimise osana uue ER-i metaandmete konfiguratsiooni, mis sisaldab kõiki metaandmeid, mis on valitud äridomeeni ER-aruannete genereerimiseks praegu nõutavad. 

## <a name="add-metadata-configuration"></a>Metaandmete konfigureerimise lisamine 
1.    Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog. 
2.    Sisestage väljale **Nimi** "Väliskaubanduse metaandmed". 
3.    Klõpsake **Loo konfiguratsioon**. 
4.    Klõpsake valikut **Kujundaja**. 
5.    Klõpsake käsku **Lisa**. 
  
> [!NOTE]
> Saate valida kogu rakenduse või valitud mudeli või valitud mooduli metaandmed. Arvestage, et sel juhul lisatakse automaatselt järgmised metaandmed: kirjete tabelid, loetelud ja laiendatud andmetüübid. Kui on vaja täiendavaid metaandmete tüüpe, tuleb need lisada käsitsi. 
 
Meil on mõned väliskaubanduse kannetega seotud metaandmed, valides metaandmete üksused käsitsi. 
  
6.    Klõpsake suvandit **Andmeallika lisamine**. 
7.    Klõpsake suvandit **Tabeli kirjed**. 
8.    Kasutage kiirfiltrit, et filtreerida **Nime** välja väärtusega "Intrastat". 
9.    Valige tabeli kirje **Intrastat**. 
10.    Klõpsake valikut **OK**.
  
Lisasime Intrastati kirjetabeli metaandmete teabe. 
  
11.    Laiendage puul valikut **Table records Intrastat**\>**Relations**. 
12.    Tehke puul valik **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.     
13.    Klõpsake käsku **Lisa metaandmeid**. 
  
> [!NOTE]
> Valitud kirjetabeli nõutavate seoste metaandmed tuleb lisada käsitsi. 
  
16.    Klõpsake suvandit **Andmeallika lisamine**. 
17.    Klõpsake valikut **Loetelu**. 
18.    Kasutage kiirfiltrit, et filtreerida **Nime** välja väärtusega "IntrastatDirection". 
19.    Valige **IntrastatDirectioni loetelu** kirje. 
20.    Klõpsake valikut **OK**. 
21.    Klõpsake valikut **Salvesta**.  
22.    Sulgege leht. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Täitke metaandmete konfiguratsiooni mustandversioon
1.    Klõpsake valikut **Muuda olekut**. 
2.    Klõpsake valikut **Vii lõpule**. 
3.    Klõpsake valikut **OK**. 
4.    Valige lõpule viidud versioon **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Eksportige metaandmete konfiguratsiooni lõpule viidud versioon rakendusest XML-failina
1.    Klõpsake valikut **Vahetus**. 
2.    Klõpsake **Ekspordi XML-failina**. 
3.    Klõpsake valikut **OK**. 
    
Loodud ER-i metaandmete konfiguratsioon salvestati XML-failina, mida saab importida RCS-i ja kasutada väliskaubanduse äritegevuse domeeni metaandmete teabe allikana. Selle teabe põhjal saame määratleda vastendamise rakenduse metaandmete ja ER-i andmemudeli vahel.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
