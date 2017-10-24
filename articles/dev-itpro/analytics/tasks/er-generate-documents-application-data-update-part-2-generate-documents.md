--- 
title: Elektroonilise aruandluse (ER) jaoks avalduse andmete uuendamisega dokumentide genereerimine
description: "Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (1. osa – konfiguratsioonide import)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c724ce3c39ed7097a5a842b44a095628dcdfa131
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) jaoks avalduse andmete uuendamisega dokumentide genereerimine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri "ER Avalduse andmete värskendusega dokumentide genereerimine (1.



osa: konfiguratsioonide importimine). Selles protseduuris selgitatakse, kuidas kasutada imporditud näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks.



Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia DEMF-i andmekomplekti abil. 



Enne alustamist asendage DEMF-ettevõtte riigikontekst DEU (Saksamaa) kontekstiga BEL (Belgia). Juriidilise isiku DEMF esmase aadressi riigikoodi värskendamiseks avage Organisatsioonihaldus > Organisatsioonid > Juriidilised isikud. Taaskäivitage avaldus.


## <a name="run-imported-er-format"></a>Imporditud ER-vormingu käivitamine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut „Intrastat (model)".
3. Tehke puul valik „Intrastat (model)\Intrastat (format)".
4. Klõpsake nuppu Käivita.
    * Intrastat-aruande genereerimiseks käivitage elektroonilise aruandluse (ER) vormingu konfiguratsioon.  
5. Sisestage valiku Sisesta fail nimeväljale „intrastat.xml".
    * Määrake faili nimi.  
6. Klõpsake nuppu OK.
    * Vaadake genereeritud XML-fail üle.  
7. Sulgege leht.
8. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.
    * Avage see vorm genereeritud elektroonilisse dokumenti kaasatud Intrastati kannete vaatamiseks.  
9. Klõpsake valikut „Intrastat archive".
    * Kuna käivitatud elektroonilise aruandluse vorming ei sisalda ühtegi avalduse andmete värskenduse sätet, pole lõpule viidud Intrastat-aruande üksikasjad arhiivitud.  
10. Sulgege leht.
11. Sulgege leht.


