---
title: Avalduse andmetega dokumentide loomine
description: Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (4. osa – vormingu muutmine)“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c474f4bc7940a429ed62870e00302c93581eb9a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569577"
---
# <a name="generate-documents-that-have-application-data"></a>Rakenduse andmetega dokumentide loomine

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (4. osa: vormingu muutmine)“.



Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks. Käesolevas näites kasutate ER vormingu konfiguratsiooni Intrastati aruande loomiseks ja avalduse andmete värskendamiseks arhiivimisdetailide ja aruandlusprotsessi jaoks.



Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia DEMF-i andmekomplekti abil. Enne alustamist veenduge, et ettevõtte DEMF riigikontekst on BEL (Belgia).


## <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine
1. Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.
2. Klõpsake vahekaarti Numbriseeriad.

    Intrastat-aruandlusprotsessi üksikasjade arhiivimiseks tuleb tuvastada iga loodud arhiivi kirjed. Selleks peab olema konfigureeritud spetsiaalne numbriseeria.  

3. Valige viide „Intrastat archive ID”.
4. Tippige väärtus väljale Numbriseeria kood.

    Sisestage või valige väärtus „Fore_2” väljal „Numbriseeria kood”.  

5. Numbriseeria koodi ResolveChanges.
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.

## <a name="run-modified-er-format"></a>Muudetud ER-vormingu käivitamine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut „Intrastat (model)".
3. Tehke puul valik „Intrastat (model)\Intrastat (format)".
4. Klõpsake käsku Käita.
5. Sisestage valiku Sisesta fail nimeväljale „intrastat2.xml".
6. Klõpsake nuppu OK.

## <a name="review-er-format-executions-results"></a>Vaadake üle ER-vormingu käivitamise tulemused
Vaadake genereeritud XML-fail üle.  
1. Sulgege leht.
2. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.

    Avage vorm, mis sisaldab Intrastati kandeid, mis on kaasatud genereeritud elektroonilisse dokumenti.  

3. Klõpsake valikut „Intrastat archive".

    Kuna käivitatud elektroonilise aruandluse vorming sisaldab nüüd avalduse andmete värskenduse sätet, on lõpule viidud Intrastat-aruande üksikasjad arhiivitud. Sellel vormil saate vaadata loodud arhiivi päisekirjet.  

4. Klõpsake käsku Details (Üksikasjad).

    Sellel vormil saate vaadata loodud arhiivi üksikasju.  

5. Sulgege leht.
6. Sulgege leht.
7. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]