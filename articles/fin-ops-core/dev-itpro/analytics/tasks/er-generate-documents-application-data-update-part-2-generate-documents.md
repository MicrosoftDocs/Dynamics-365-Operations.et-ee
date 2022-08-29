---
title: Konfiguratsioonide loomine rakendusandmetega dokumentide loomiseks
description: See artikkel kirjeldab, kuidas kujundada elektroonilise dokumendi loomiseks elektroonilise aruandluse (ER) konfiguratsioone. (1. osa – konfiguratsioonide importimine).
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290540"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>Konfiguratsioonide loomine rakendusandmetega dokumentide loomiseks

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri "ER Avalduse andmete värskendusega dokumentide genereerimine (1.



Konfiguratsioonipakkuja loomine ja aktiivseks märkimine".) Selles protseduuris selgitatakse, kuidas kasutada imporditud näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks.



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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
