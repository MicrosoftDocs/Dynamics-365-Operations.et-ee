---
title: Pakkumiskutse loomine
description: Selles protseduuris kirjeldatakse, kuidas luua pakkumiskutset.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aed08083d83a47d914ecd6c9421825163c5c467a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673827"
---
# <a name="create-a-request-for-quotation"></a>Pakkumiskutse loomine

[!include [banner](../../includes/banner.md)]

Selles protseduuris kirjeldatakse, kuidas luua pakkumiskutset. Seda teeb tavaliselt ostuagent. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades. Enne alustamist peavad olema seadistatud kutsetüübid. Kui olete selle ülesande lõpule viinud ning loonud ja saatnud pakkumiskutse, saate sisestada vastused hankija kohta, neid võrrelda ning määrata lepingu.


## <a name="prepare-a-new-rfq"></a>Uue pakkumiskutse ettevalmistamine
1. Minge **navigeerimispaanile> Moodulid> Hange ja hankimine> Pakkumistaotlused> Kõik hinnapakkumistaotlused**.
2. Klõpsake valikut **Uus**.
    Saadaval on järgmised ostu tüübid. Ostutellimus (see on vaikesäte): dokument, mis kinnitab toodete ostmise pakkumise, või makse asemel toodete müümise pakkumise aktsepteerimine. Ostutaotlus: see tüüp valitakse automaatselt, kui loote pakkumiskutse otse ostutaotlusest. Kui valite selle suvandi käsitsi, kuvatakse tõrge. Ostuleping: lepe osta aja jooksul teatud koguses või väärtuses tooteid. Kui valite selle suvandi, peate valima ostulepingule kehtiva kuupäevavahemiku.  
3. **Tippige väljale Dokumendi pealkiri väärtus.**
4. **Sisestage või valige väljal Kutse tüüp väärtus.**
    + Kui hindamismeetod on seostatud kutse tüübiga, on see loodava pakkumiskutse vaikehindamismeetod. Hiljem on võimalik hindamismeetodit muuta.  
    + **Sisestage kuupäev väljale Tarnekuupäev.**  
    + Valige kuupäev, millal soovite kaubad saada.  
    + **Sisestage väljale Aegumiskuupäev ja -kellaaeg kuupäev ja kellaaeg.**  
    + Määrake kuupäev ja kellaaeg, mis ajaks peavad hankijad pakkumiskutsele vastama.  
5. Sisestage või valige väärtus väljale **Ladu**. Tarneaadress on vaikimisi lao aadress.  
6. Klõpsake valikut **OK**.

## <a name="add-lines"></a>Lisa read

Pärast pakkumiskutse põhiteabe määramist saate määrata kaubad või teenused, mille kohta soovite hankijatelt pakkumisi saada. Kaup on rea vaiketüüp.

1. Sisestage või valige väärtus väljale **Kauba kood**. Kui kasutate USMF-i, saate teha valiku T0020.  
2. Sisestage arv väljale **Kogus**.
3. Klõpsake käsku **Lisa rida**.
4. **Valige väljal Rea tüüp suvand Kategooria.** Võite kasutada rea tüüpi Kategooria, et luua pakkumiskutseid mittelaokaupade või teenuste kohta. Teil tuleb valida kaupade või teenuste tüüp hankekategooriate hierarhiast.  
5. **Sisestage või valige väärtus väljal Hanke kategooria.**
6. Sisestage väärtus väljale **Toote nimi**.
7. Sisestage arv väljale **Kogus**.
8. Sisestage või valige väärtus väljal **Ühik**.

## <a name="add-vendors"></a>Hankijate lisamine
1. Klõpsake **Päist**, et lülituda reavaatelt päisevaatele. 
2. **Laiendage üksuse Hankija jaotist.**
3. **Klõpsake suvandit Hankijate automaatne lisamine.** Saate hankijaid taotletud kaupade hankekategooria põhjal pakkumiskutsele automaatselt lisada. Kui ridadele lisatud kategooriate puhul pole kinnitatud hankijaid, saate lisada hankijad käsitsi.  
4. Klõpsake käsku **Lisa**.
5. **Sisestage väärtus väljale Hankija konto või valige see.**
6. Klõpsake käsku **Lisa**.
7. Sisestage või valige väärtus väljale **Hankija konto**. Kui olete hankija valinud, on olek Loodud. See tähendab, et hankija andmed on salvestatud pakkumiskutsesse, kuid te pole pakkumiskutset hankijale saatnud. Hankija saate lisada pakkumiskutsesse hankija olekust sõltumata.  

## <a name="send-the-rfq-to-vendors"></a>Pakkumiskutse saatmine hankijatele
1. Klõpsake paanil **Toimingupaan** nuppu **Saada**. Kontrollige lehel Pakkumiskutse saatmine, kas loendis on hankijad, kellele soovite pakkumiskutse saata.  
2. Klõpsake **Prindi**. See dialoog võimaldab teil pakkumiskutset printida. Kui soovite printida vastuselehe, määratletakse selle sisu hankeparameetrites. Valimaks, kuidas vastuselehti printida, klõpsake pärast dialoogi Prindi avamist suvandit Täpsemad prindisuvandid. Iga hankija kohta prinditakse üks pakkumiskutse, mis sisaldab ridu olekus Loodud või Saadetud. Tühistatud ridu ja registreeritud vastustega ridu ei prindita.   
3. Klõpsake **Tühista**.
4. Klõpsake valikut **OK**.
5. Sulgege leht.
6. Sulgege leht.

## <a name="view-the-rfq-journal"></a>Pakkumiskutse töölehe kuvamine
1. Avage **Hanked > Pakkumiskutsed > Pakkumiskutsete järeltoimingud > Pakkumiskutse töölehed**.
2. **Klõpsake suvandit Eelvaade/prindi.**
3. **Klõpsake suvandit Algne eelvaade.**
4. Sulgege leht.
5. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]