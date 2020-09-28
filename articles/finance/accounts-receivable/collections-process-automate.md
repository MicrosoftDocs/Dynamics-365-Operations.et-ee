---
title: Sissenõuete protsessi automatiseerimine
description: Selles teemas kirjeldatakse võlanõudmise protsessi strateegiate seadistamist, mis automaatselt tuvastavad kliendi arved, mille korral on vajalik meilimeeldetuletus, võlanõudmise tegevus (nt telefonikõne) või kliendile saadetav märgukiri.
author: panolte
manager: AnnBe
ms.date: 08/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: db59bad2ed3caf38f22bd4d6059e57747d1d983f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760525"
---
# <a name="collections-process-automation"></a>Sissenõuete protsessi automatiseerimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse võlanõudmise protsessi strateegiate seadistamist, mis automaatselt tuvastavad kliendi arved, mille korral on vajalik meilimeeldetuletus, võlanõudmise tegevus (nt telefonikõne) või kliendile saadetav märgukiri. 

Organisatsioonid kulutavad märkimisväärse aja aegunud saldoaruannete, kliendikontode ja avatud arvete otsimisele, et teha kindlaks, milliste klientidega on vaja avatud arve või konto saldoga seoses ühendust võtta. See uuring vähendab aega, mis kulub inkassaatoril klientidega suhtlemiseks, et sisse nõuda tähtajaks tasumata saldosid, või arvega seotud vaidluste lahendamiseks. Võlanõudmise protsessi automatiseerimine võimaldab teil seadistada oma võlanõudmise protsessile strateegiapõhise lähenemise. See aitab teil võlanõudmise tegevusi järjepidevalt rakendada, pakkudes kohandatud meilimeeldetuletusi või programmeeritud protsessi märgukirjade saatmiseks. 

## <a name="collections-process-setup"></a>Võlanõudmise protsessi töötlemine
Lehe **Võlanõudmise protsessi töötlemine** (**Krediidihaldus ja võlanõuded > Töötlemine > Võlanõudmise protsessi töötlemine**) abil saate luua automatiseeritud võlanõudmise protsessi, mis ajastab tegevusi, saadab meilisõnumeid ning loob ja edastab klientidele mõeldud märgukirju. Protsessi etapid põhinevad uusimal või vanimal avatud arvel. Iga etapp kasutab seda arvet, et määrata, millist suhtlusviisi või mis tegevus peaks konkreetse kliendi korral kasutama.  

### <a name="process-hierarchy"></a>Protsessihierarhia
Iga kliendikausta saab määrata ainult ühele protsessi hierarhiale. Selle etapi hierarhia järk tuvastab, milline protsess on ülimuslik, kui klient on kaasatud mitmesse kausta, millele on määratud protsessihierarhia. Kausta ID määrab, millised kliendid määratakse protsessile. 

Vaikseid päevi kasutatakse selleks, et tagada, et automatiseeritud protsess ei võtaks kliendiga ühendust liiga sageli.  Näiteks kui vaikseteks päevadeks on seatud kaks päeva, ei võta automatiseeritud protsess kliendiga ühendust vähemalt kaks päeva, isegi kui uusim esialgne arve on täielikult tasakaalustatud. 

Kui soovite jätta kliendid protsessi automatiseerimisest välja juhul, kui konto saldo või arve saldo on määratletud väärtusest väiksem, seadke välja **Välista protsessist** väärtuseks **Jah** ja sisestage summa väärtus.

## <a name="process-details"></a>Protsessi üksikasjad
**Kirjeldust** kasutatakse hierarhia etapi eesmärgi või nime tuvastamiseks.

**Tegevuse tüüp** määratleb, kas etapp loob tegevuse, saadab meili või loob märgukirja.

**Äridokument** määratleb malli, mida kasutatakse tegevuse tüübi loomiseks.  See võib olla tegevusemall, meilimall või märgukiri kliendi kohta. 

Tegevuse tüüpe saab luua kas enne või pärast arve tähtaega, võttes aluseks sätte, mis kuvatakse veerus **Arve tähtajaga seotud päevad**.

Kui valite meilitoimingu tüübi, kasutatakse adressaati määratlemaks, kas tegemist on kliendi, müügigrupi või inkassaatori kontaktiga. Väljal **Ärikontakt** olev väärtus määrab seejärel, millise selle kliendi konto kontaktiga suheldakse.

## <a name="business-document-details"></a>Äridokumentide üksikasjad
Äridokumendi üksikasjad sõltuvad protsessi üksikasjades valitud tegevuse tüübist.  Kui tegevuse tüüp on tegevus, kuvatakse tegevusemalli üksikasjad.  Need üksikasjad hõlmavad tegevusemalli nime, loodava tegevuse tüüpi, tegevuse eesmärki, tegevuse lõpetamiseks plaanitud päevade arvu ja tegevuse üksikasju.  See tegevus loob seejärel seose uusima arvega, mis teatab adressaadile tegevuse lõpuleviimiseks vajalikust tegevusest.

Kui tegevuse tüüp on protsessi üksikasjades olev meilisõnum, sisaldab see jaotis kahte kiirkaarti.  Esimest kasutatakse malli ID, meili kirjelduse, vaikekeele, automaatselt saadetavatele meilisõnumitele määratud kasutajanime ja seostuvate saatjate meilaadressi määratlemiseks. Teine võimaldab luua meilisisu pärast väljade **Keel** ja **Teema** väärtuste salvestamist, valides **Redigeeri**.  See avab akna, mis võimaldab üles laadida HTML-sisu. Soovi korral saate käsitsi sisestatud sõnumi tippida ka akna alumisse vasakpoolsesse kasti.  

> [!Note]
> Outlooki meili saab salvestada HTML-vormingus soovitud suhtluse tekstina. Selle saab malli rakendamiseks üles laadida. <br> <br> Kui märgukirja tegevuse tüüp on valitud, siis seadistamise vormil pole äridokumendi üksikasjade jaotist.


## <a name="fasttab-reference"></a>Kiirkaardi viide
Järgmistes tabelites on loetletud leheküljed ja väljad, millele määratud kiirkaartide kaudu saab juurde pääseda, koos sellel vahekaardil oleva teabe kirjeldusega. 

### <a name="process-hierarchy"></a>Protsessihierarhia

|     Lehekülg                                                  |     Field                         |     Kirjeldus                           |
| --------------------------------------------------------  |-------------------------------    |---------------------------------------    |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |                                   |     Saate luua ja hallata kliendikausta määrangutel põhinevaid võlanõudmise protsesse.                                                                                                                             |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |     Hierarhia                     |     Määratleb protsessi automatiseerimise prioriteedi, et määrata klient, kui ta kuulub mitmesse kausta.                                                                                                   |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |     Kausta ID                       |     Päringud, mis määratlevad kliendi kirjete grupi.                                                                                                                                                        |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |     Vaiksed päevad                    |     Saate piirata seda, kui sageli saab protsessi etappi lõpule viia. Näiteks kui kaks vaikset päeva on määratud, ei toimu järgmine protsessi etapp vähemalt kahe päeva jooksul, kui uusim arve muutub.     |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |     Välista töötlemisest        |     Kui valite **Kliendi aegunud saldo on väiksem kui** või **Arve summa on väiksem kui**, välistatakse klient protsessi automatiseerimisest, kui väärtuse kriteeriumid pole täidetud.                                   |

### <a name="process-details"></a>Protsessi üksikasjad
|     Lehekülg                                                  |     Field                                         |      Kirjeldus                  |
|--------------------------------------------------------   |-----------------------------------------------    |----------------------------   |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |                                                   |     Saate määratleda uusimal arvel põhinevad etapid.                                                                                                |
|                                                           |     Kirjeldus                                   |     Etapi nime ja/või kirjelduse esitamiseks kasutatav vabas vormis tekstiväli.                                                                           |
|                                                           |     Tegevuse tüüp                                   |     Tegevus, meil või märgukiri, mis luuakse protsessi etapiga.                                                                     |
|                                                           |     Äridokument                           |     Määratleb protsessi etapi korral kasutatava tegevuse või meilimalli.                                                                        |
|                                                           |     Millal?                                          |     Määratleb, kas protsessi etapp toimub enne või pärast uusima arve tähtaega, ning välja **Arve tähtajaga seotud päevad**.        |
|                                                           |     Arve tähtajaga seotud päevad        |     Välja **Kui** abil tuvastab see protsessi etapi ajastuse.                                                                          |
|                                                           |     Adressaat                                     |     Tuvastab, kas meilisõnum saadetakse kliendi, müügigrupi või inkassaatori kontaktile.                                                   |
|                                                           |     Äriotstarbeline kontakt                    |     Määrab, millist adressaadi meiliaadressi meilisuhtluses kasutatakse.                                                                                 |

### <a name="business-process-activity-template-details"></a>Äriprotsessi tegevuse malli üksikasjad 
|     Lehekülg                                                  |     Field                     |      Kirjeldus                  |
|--------------------------------------------------------   |----------------------------   |-------------------------  |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |                               |     Seadistuse protsessi osa, mis tuvastab tegevuste malli üksikasju.                                                                      |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |     Tegevuse mall       |     Tuvastab tüübi, eesmärgi, lõpule viimiseni jäänud päevade arvu ja esitab üksikasjad tegevuse protsessi etapis loodava tegevuse kohta.       |

### <a name="business-document-email-template-details"></a>Äridokumendi meilimalli üksikasjad 
|     Lehekülg                                                  |     Field     |      Kirjeldus                  |
|--------------------------------------------------------   |-------------- |-----------------------------  |
|     Võlanõudmise protsessi töötlemine <br> Protsessi automatiseerimine       |               |     Tuvastab meili protsessi etapis loodava meili kirjelduse, vaikekeele, saatjate nime ja meiliaadressi.        |


### <a name="collections-history"></a>Sissenõuete ajalugu 
|     Lehekülg                              |     Field     |      Kirjeldus                                                          |
|------------------------------------   |-------------- |---------------------------------------------------------------------  |
|     Võlanõudmise protsessi töötlemine       |               |     Saate vaadata valitud protsessi hierarhia hiljutist ajalugu.     |

### <a name="collection-process-assignment"></a>Võlanõudmise protsessi määramine
|     Lehekülg                              |     Field     |      Kirjeldus                                                  |
|------------------------------------   |-------------- |-----------------------------------------------------------    |
|     Võlanõudmise protsessi töötlemine       |               |     Saate vaadata võlanõudmise protsessile määratud kliente.  
|     Käsitsi määramine               |               |     Saate vaadata kliente, kes on protsessile käsitsi määratud, või valida protsessile määratavad kliendid. |
|     Protsessi määramise eelversioon      |               |     Saate vaadata nende klientide eelvaadet, kes selle käivitamisel strateegiale määratakse.   |
|     Kliendi määramise eelversioon     |               |     Saate vaadata strateegiat, millele konkreetne klient on määratud.    |
 
### <a name="parameters"></a>Parameetrid
|     Lehekülg                                                                  |     Field                                             |      Kirjeldus                              |
|-------------------------------------------------------------------------- |------------------------------------------------------ |-------------------------------------  |
|     Müügireskontro parameetrid > võlanõudmise protsessi automatiseerimine     |     Klientide protsent partiiülesande kohta          |     Säte, mille abil saab määrata pakett-tööde arvu automatiseerimisprotsessi kohta.                                          |
|     Müügireskontro parameetrid > võlanõudmise protsessi automatiseerimine     |     Postita märgukirjad automaatselt           |     Märgukirja tegevuse tüübid postitavad kirja automatiseerimise ajal.                                      |
|     Müügireskontro parameetrid > võlanõudmise protsessi automatiseerimine     |     Automatiseerimise tegevuste loomine                |     Saate luua ja sulgeda tegevusi mitteaktiivsetele tegevuse tüüpide kohta, et vaadata kõiki kontol tehtud automatiseeritud etappe.        |
|     Müügireskontro parameetrid > võlanõudmise protsessi automatiseerimine     |     Võlanõudmise protsessi automatiseerimise säilitamise päevade arv     |     Määratleb päevade arvu, mille jooksul kogumite ajalugu talletatakse.                                                       |
