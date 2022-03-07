---
title: Sissenõuete protsessi automatiseerimine
description: Selles teemas kirjeldatakse võlanõudmise protsessi strateegiate seadistamist, mis automaatselt tuvastavad kliendi arved, mille korral on vajalik meilimeeldetuletus, võlanõudmise tegevus (nt telefonikõne) või kliendile saadetav märgukiri.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486865"
---
# <a name="collections-process-automation"></a>Sissenõuete protsessi automatiseerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse võlanõudmise protsessi strateegiate seadistamist, mis automaatselt tuvastavad kliendi arved, mille korral on vajalik meilimeeldetuletus, võlanõudmise tegevus (nt telefonikõne) või kliendile saadetav märgukiri. 

Organisatsioonid kulutavad tihti märkimisväärse aja aegunud saldoaruannete, kliendikontode ja avatud arvete otsimisele, et teha kindlaks, milliste klientidega on vaja avatud arve või konto saldoga seoses ühendust võtta. See uuring vähendab aega, mis kulub inkassaatoril klientidega suhtlemiseks, et sisse nõuda tähtajaks tasumata saldosid, või arvega seotud vaidluste lahendamiseks. Võlanõudmise protsessi automatiseerimine võimaldab teil seadistada oma võlanõudmise protsessile strateegiapõhise lähenemise. See aitab teil võlanõudmise tegevusi järjepidevalt rakendada, pakkudes kohandatud meilimeeldetuletusi või programmeeritud protsessi märgukirjade saatmiseks. 

## <a name="collections-process-setup"></a>Võlanõudmise protsessi töötlemine
Lehe **Võlanõudmise protsessi töötlemine** (**Krediidihaldus ja võlanõuded > Töötlemine > Võlanõudmise protsessi töötlemine**) abil saate luua automatiseeritud võlanõudmise protsessi, mis ajastab tegevusi, saadab meilisõnumeid ning loob ja edastab klientidele mõeldud märgukirju. Protsessi etapid põhinevad uusimal või vanimal avatud arvel. Iga etapp kasutab seda arvet, et määrata, millist suhtlusviisi või mis tegevus peaks konkreetse kliendi korral kasutama.  

Inkassomeeskonnad saadavad tavaliselt iga laekumata arvega seotud varajase teatise, et klienti teavitatakse siis, kui arve tähtaeg muutub kindlaks. Valiku **Eellugemine** saab seadistada nii, et iga protsessihierarhia sammuga saaks iga arve puhul tegutseda, kui arve ajastus selle sammuni jõuab.

### <a name="process-hierarchy"></a>Protsessihierarhia
Iga kliendikausta saab määrata ainult ühele protsessi hierarhiale. Selle etapi hierarhia järk tuvastab, milline protsess on ülimuslik, kui klient on kaasatud mitmesse kausta, millele on määratud protsessihierarhia. Kausta ID määrab, millised kliendid määratakse protsessile. Iga seadistatud hierarhiat saab määrata ainult ühele protsessiautomaatikale.

Vaikseid päevi kasutatakse selleks, et tagada, et automatiseeritud protsess ei võtaks kliendiga liiga sageli ühendust. Näiteks kui vaikseteks päevadeks on seatud kaks päeva, ei võta automatiseeritud protsess kliendiga ühendust vähemalt kaks päeva, isegi kui uusim esialgne arve on täielikult tasakaalustatud. 

Klientide väljajätmiseks protsessi automatiseerimisest, kui kliendi vananemise saldo või arve summa on väiksem kui määratud väärtus, valige **Kliendi vananemise saldo alla** või **Arve summa alla** väljal **Välista protsessist** väli ja sisestage summa väärtus.

Märkige **Ennustuse kasutamine** sissenõuete tegevuste loomiseks, kasutades kliendi makseprognoose. Loodud tegevuste puhul kasutatakse tegevuste malli **Makseprognoosid** **Konto saadaolevad parameetrid** lehel, **Kogumisprotsessi automatiseerimine** vahekaardil. 

### <a name="process-details"></a>Protsessi üksikasjad
Klõpsake nuppu **Uus** hierarhiale uue protsessi üksikasja lisamiseks. **Kirjeldust** kasutatakse hierarhia etapi eesmärgi või nime tuvastamiseks. Valige **Tegevuse tüüp**, et määratleda etapp, mis loob tegevuse, saadab meili või loob märgukirja. 

- **Äridokument** määratleb malli, mida kasutatakse tegevuse tüübi loomiseks. See dokument võib olla tegevusemall, meilimall või märgukiri saadetud igale kliendile. Sissenõuete protsessi automatiseerimine loob ainult märgukirju kliendi kohta, sõltumata sellest, kuidas muud sissenõuete parameetrid on seadistatud.
- **Millal** määratleb protsessietapi, mis toimub enne või pärast arve esmast tähtaega ja mida kasutatakse koos numbriga, mis kuvatakse veerus **Päevad seoses arve maksetähtajaga**. 
- Märkige suvand **Eellteade**, et luua tegevus igale arvele protsessihierarhia ühe sammu jooksul. Eelteate toimingud on tavaliselt tasumata arvetega seotud varajane teade, nii et klienti saab teavitada arve tasumise tähtajast. Eelteadet saab märkida ainult ühele tegevusele hierarhia kohta. Kui valite meilitoimingu tüübi, kasutatakse adressaati määratlemaks, kas e-kiri saadetakse kliendi, müügigrupi või inkassaatori kontaktiga. 
- Väljal **Ärikontakt** olev väärtus määrab seejärel, millise selle kliendi konto kontaktiga suheldakse.

### <a name="business-document-details"></a>Äridokumentide üksikasjad
Äridokumendi üksikasjad sõltuvad protsessi üksikasjades valitud tegevuse tüübist. Kui tegevuse tüüp on tegevus, kuvatakse tegevusemalli üksikasjad. Need üksikasjad hõlmavad tegevusemalli nime, loodava tegevuse tüüpi, tegevuse eesmärki, tegevuse lõpetamiseks plaanitud päevade arvu ja tegevuse üksikasju. See tegevus loob seejärel seose uusima arvega, mis teatab adressaadile tegevuse lõpuleviimiseks vajalikust tegevusest.

Kui tegevuse tüüp on protsessi üksikasjades olev meilisõnum, sisaldab see jaotis kahte kiirkaarti. Esimest kasutatakse malli ID, meili kirjelduse, vaikekeele, automaatselt saadetavatele meilisõnumitele määratud kasutajanime ja seostuvate saatjate meilaadressi määratlemiseks. Teine võimaldab luua meilisisu pärast väljade **Keel** ja **Teema** väärtuste salvestamist, valides **Redigeeri**. See avab akna, mis võimaldab üles laadida HTML-sisu. 

> [!Note]
> Saate salvestada Outlooki meilisõnumi, mis sisaldab side kehateksti HTML-vormingus. Seejärel saate malli rakendamiseks teate sisu üles laadida. <br> <br> Kui märgukirja tegevuse tüüp on valitud, siis seadistamise lehel pole äridokumendi üksikasjade jaotist.

Kasutage nuppu **Sissenõuete protsessiajalugu** valitud protsessihierarhia viimase ajaloo vaatamiseks. 

Klõpsake **Sissenõuete protsessi määramine** tegevustel, et vaadata sissenõuete protsessi määratud kliente. Kasutage **Kliendi määramise eelvaadet**, et vaadata hierarhiat, millele konkreetne klient on määratud. Kasutage **Protsessi määrangu eelvaadet** klientide eelvaateks, kes määratakse hierarhiasse selle käivitamisel. Vajutage **Manuaalne ülesanne** peal, et vaadata kliente, kes on protsessile käsitsi määratud, või valida protsessile määratavad kliendid.

Vajutage **Protsessi simulatsioni** peal, et vaadata üle tegevused, mis luuakse siis, kui valitud protsessi automatiseerimine on käitatud. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
