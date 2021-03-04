---
title: Vara rentimise aruanded
description: Selles teemas loetletakse ja kirjeldatakse lühidalt vara rentimises saadaolevaid aruandeid.
author: moaamer
manager: Ann Beebe
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bab2b0b2b021266e50d6f4a1fad1cc4a1c1ae56e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442569"
---
# <a name="asset-leasing-reports"></a>Vara rentimise aruanded

[!include [banner](../includes/banner.md)]

Selles teemas loetletakse ja kirjeldatakse lühidalt vara rentimises saadaolevaid aruandeid. Enamik aruandeid kuvatakse, täites need sammud või sammud, mis on väga sarnased, nagu on märgitud. 

- Enamiku varade rentimise aruannete vaatamiseks avage suvand **Vara rentimine > Päringud ja aruanded > Rendiaruanded** ja valige vaatamiseks aruanne. Erinevat valimise teed vajavate aruannete puhul on aruande avamise sammud lisatud selle aruande kirjeldusse. 
- Kui valite aruande printimiseks, avaneb parameetrite leht, mis võimaldab teil aruandesse kaasatavat teavet filtreerida. Sisestage filtreerimise kriteeriumid ja klõpsake seejärel aruande loomiseks nuppu **OK**. Loodud aruandes kuvatakse teave, mis kuulub teie määratud filtrite alla.

## <a name="asset-movement"></a>Vara liigutamine
Vara liikumise aruanne toimib edasiarvestuse aruandena iga rendikirje kasutusõiguse esemeks oleva vara saldo jaoks. See aruanne võimaldab vaadata rentimise vara kandeid konkreetse perioodi jooksul. Aruanne sisaldab järgmisi välju. 

|     Aruande väljad                  |     Kirjeldus                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Alguskuupäev              |     Rentimise varaseima versiooni alguskuupäev.                     |   
|     Rendiperiood                     |     Rentimise varaseima versiooni rendiperiood.                            |
|     Lühiajaline rendileping               |     Kui rendikirje liigitub lühiajaliseks rendilepinguks, on seal kuvatud **Jah**.         |
|     Väikese väärtusega rent                |     Kui rendikirje liigitub väikese väärtusega rendiks, on seal kuvatud **Jah**.          |
|     Esialgse kasutamisõiguse esemeks olev vara     |     Kasutamisõiguse esemeks oleva vara algväärtus esialgse tuvastamise töölehe kirjes.      |
|     Algsaldo              |     Kasutamisõiguse esemeks olev vara raamatupidamislik netoväärtus alates **alguskuupäevast**.                         |
|     Perioodi kulumi kulu    |     Aruande jaoks määratletud kuupäevavahemiku jooksul võetud kulumi kulusumma.        |
|     Akumuleeritud kulum       |     Akumuleeritud kulumi summa alates **alguskuupäevast**.                               |
|     Väärtuse langus                     |     Summa, mille võrra vara väärtus aruandes määratletud kuupäevavahemiku jooksul vähenes.               |
|     Muudatused                  |     Korrigeerimiste summa vara kasutamise õiguseks kuupäeva parameetrite vahel.                            |
|     Arvestuslik jääkväärtus                 |     Vara kasutusõiguse lõplik raamatupidamislik netoväärtus, mis on akumuleerunud kulumi netosumma **lõpukuupäeval**.    |

## <a name="differences-report"></a>Erinevuste aruanne
Erinevuste aruanne näitab rentimise importimise raamistikku laaditud teabe ja praegu süsteemis oleva teabe erinevusi. See võimaldab teil võrrelda seda, mida korrigeeriti, uuendati või lisati rentimise importimise raamistiku kaudu.  

Aruande väärtused varieeruvad valitud rendikirje alusel. Aruanne näitab ainult neid välju, mis erinevad hetkel süsteemis olevatest ja mis on koondamistabelites. Vana väärtus on see, mis on praegu süsteemis või mis oli varem süsteemis, sõltuvalt sellest, kas importimistoiming on käivitatud. Uus väärtus näitab koondamistabelis olevat väärtust, mis asendab vana väärtuse.

## <a name="five-years-undiscounted-payment-forecast"></a>Viie aasta diskonteerimata maksete prognoos
Viie aasta diskonteerimata maksete prognoosi aruanne näitab projitseeritud diskonteerimata rendimakseid, mis tuleb maksta järgmise viie aasta jooksul alates aruande parameetrites määratud kuupäevast. Aruanne sisaldab järgmisi välju. 

|     Aruande väljad         |     Kirjeldus                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Rendi kirjeldus     |     Rendi kirjeldus rendipäisest.                                                      |
|     Rendi ID              |     Unikaalne rendi ID.                                                                              |
|     Reserveerimine                  |     Raamatu ID-ga seotud rendi raamat.                                                         |
|     Klassifikatsioon        |     Rendikirje klassifikatsioon.                                                                  |
|     Sisestamiskiht         |     Rendi sisestamise kiht.                                                         |
|     Currency              |     Rendikirje valuuta.                                                                        |
|     Praegune               |     Kõigi järgmise 12 kuu jooksul tasumisele kuuluvate rendimaksete summa aruandluse kuupäevast.          |
|     13–24 kuud          |     Kõigi järgmise 13–24 kuu jooksul tasumisele kuuluvate rendimaksete summa aruandluse kuupäevast.           |
|     25–36 kuud          |     Kõigi järgmise 25–36 kuu jooksul tasumisele kuuluvate rendimaksete summa aruandluse kuupäevast.           |
|     37–48 kuud          |     Kõigi järgmise 37–48 kuu jooksul tasumisele kuuluvate rendimaksete summa aruandluse kuupäevast.           |
|     49–60 kuud          |     Kõigi järgmise 49–60 kuu jooksul tasumisele kuuluvate rendimaksete summa aruandluse kuupäevast.           |
|     Hilisem            |     Kõigi alates 61. kuust ja hiljem tasumisele kuuluvate rendimaksete summa aruandluse kuupäevast.              |

## <a name="gaap-cash-flows-report"></a>GAAP-i sularaha voo aruanne
GAAP-i teabe avalikustamise aruanne vastab USA raamatupidamispõhimõtete teabe avalikustamise nõudele, mis on määratud 842-20-50-4 punkti g lõikes 1. Selle aruande vaatamiseks minge jaotisse **Vara rentimised > Päringud ja aruanded > Avalikustamised > GAAP – rahavood**. 

|     Aruande väljad                                 |     Kirjeldus                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Alates kuupäevast <br> Lõppkuupäev                        |     Määrab kuupäevade vahemiku, mida kasutatakse aruandes sisalduva teabe piiritlemiseks.      |
|     Juriidiline isik                                  |     Rendikirjetega seotud juriidiline isik.                                      |
|     Rendi tüüp                                    |     Rendi klassifikatsioon, kas finantseerimine või tegevusega seotud.           |
|     Rendi ID                                      |     Unikaalne rendi ID.                                                      |
|     Rendi kirjeldus                             |     Rendi kirjeldus rendipäisest.                              |
|     Rendi raamat                                    |     Rendi raamat, millele rida viitab.                        |
|     Sisestamiskiht                                 |     Iga põhivaraga seotud raamat seadistatakse kindla sisestuskihi jaoks, millel on üldine kulumieesmärk.                          |
|     Rendigrupp                                   |     Grupp, millega rent on seotud.                                     |
|     Currency                                      |     Tehingus kasutatava valuuta lühend. Kõik aruanded teisendavad ülekande valuuta aruandevaluutaks.                      |
|     Kapitalirent – kasutuse rahavood         |     Sisestatud muutuvate maksete kogusumma ja amortiseerumise graafikust sisestatud intressimaksete kogusumma kuupäeva parameetrite vahel.        |
|     Kapitalirent – kapitali rahavood           |     Põhimaksete kogusumma alates amortiseerumise graafikust kuupäeva parameetrite vahel.       |
|     Kasutusrent – kasutuse rahavood       |     Kõigi sisestatud rendimaksete ja sisestatud muutuvate maksete summa kuupäeva parameetrite vahel.            |

## <a name="lease-balances-forecast"></a>Rendisaldode prognoos
Rendikirje saldode prognoos loetleb teabe otse kohustise amortiseerimise graafikust ja vara kulumi graafikust. Aruanne kuvab prognoositud rendikohustise ja ajavahemikus kasutamisõiguse esemeks oleva vara prognoositud summad, sh kõik nende rendikirjete planeeritud kulud. Aruanne sisaldab järgmisi välju.

|     Aruande väljad                 |     Kirjeldus                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Algsaldo             |     Aruande alguskuupäeva sisaldava perioodi rendi amortiseerumise graafiku algsaldo.            |
|     Esialgne tuvastamine           |     Kui rendi alguskuupäev jääb aruande jaoks määratletud kuupäevavahemikku, kuvatakse selles veerus algse tuvastamise töölehe kirje kohustise konto väärtus.      |
|     Maksed                      |     Rendimaksete summa, mis jääb aruande jaoks määratletud kuupäevavahemikku.                               |
|     Viivis                      |     Rendi intressimaksete summa, mis jääb aruande jaoks määratletud kuupäevavahemikku.                    |
|     Ending balance                |     Rendi kohustise saldo **lõpukuupäeva** seisuga.                                                             |
|     Lühiajaline kohustis          |     Lühiajalise kohustise summa rendi amortiseerimise graafikus **lõpukuupäeva** seisuga.                           |
|     Pikaajaline kohustis           |     Pikaajalise kohustise summa rendi amortiseerimise graafikus **lõpukuupäeva** seisuga.                            |
|     Algne raamatupidamislik netoväärtus      |     Aruande alguskuupäeva sisaldava perioodi rendi vara kulumise graafiku algne raamatupidamislik netoväärtus      |
|     Esialgne tuvastamine           |     Kui rendi alguskuupäev jääb aruande kuupäeva parameetrite vahemikku, kuvatakse selles veerus algse tuvastamise töölehe kirje vara konto väärtus.            |
|     Kulumi kulu          |     Rendi kulumi kulude summa, mis jääb aruande jaoks määratletud kuupäevavahemikku.                  |
|     Ending balance                |     Rendi vara saldo **lõpukuupäeva** seisuga.                                                              |
|     Omakapitali korrigeerimine             |     Algsaldo miinus algne raamatupidamislik netoväärtus.                                                             |

## <a name="lease-commencements-report"></a>Rendi alguse aruanne
Rendi alguse aruanne näitab kõik rendikirjeid, mis on konkreetsel kuupäeva vahemikul alanud, sealhulgas algsed kohustised ja kasutamisõiguse esemeks oleva vara saldod. Aruanne sisaldab järgmisi välju. 

|     Aruande väljad                 |     Kirjeldus                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Alguskuupäev             |     Selle rendi versiooni jaoks sisestatud algse tuvastamise töölehe kirje kuupäev.         |
|     Esialgne rendisumma      |     Algse tuvastamise töölehe kirje kohustise summa.                                  |
|     Algne rendisumma          |     Algse tuvastamise töölehe kirje vara summa.                                      |

## <a name="lease-modification-report"></a>Rendi muutmise aruanne
Rendi muutmise aruandes kuvatakse kõik rendikirjed, mida on määratud kuupäevavahemiku jooksul muudetud. Aruandes kuvatakse ka rendikirjet korrigeerinud kasutaja ja korrigeeritud kohustiste kogusumma. Aruanne sisaldab järgmisi välju. 

|     Aruande väljad                 |     Kirjeldus           |
|---------------------------------  |-------------------------  |
|     Korrigeerinud                   |     Rendikirjed korrigeerinud isiku kasutajanimi.                                |
|     Korrektsiooni tulem               |     Korrigeerimise töölehe kirje sisestamise kuupäev.                        |
|     Korrigeerimised                   |     Mis tahes korrigeerimise töölehe kirje summa, mis sisestati rendikohustise kontole kuupäeva parameetrite ajavahemikul. Krediteerimised ilmuvad positiivsetena, samas kui debiteerimised on negatiivsed.       |
|     Kasumi (kahjumi) summa            |     Mis tahes korrigeerimise töölehe kirje summa, mis sisestati rendi kasumi/kahjumi kontole kuupäeva parameetrite ajavahemikul. Krediteerimised ilmuvad positiivsetena, samas kui debiteerimised on negatiivsed.       |
|     Jaotamata kasum             |     Mis tahes korrigeerimise töölehe kirje summa, mis sisestati rendi jaotamata kasumi kontole kuupäeva parameetrite ajavahemikul.      |
|     Kohustise lõppsaldo      |     Rendi korrigeerimise kuupäeval tulemiks oleva kohustise saldo.           |

## <a name="lease-movement-report"></a>Rendi liikumisaruanne
Rendi liikumisaruanne toimib edasiarvestuse aruandena iga rendikirje rendikohustise saldo jaoks. See aruanne võimaldab kasutajal vaadata rendi kohustise tehinguid konkreetse perioodi jooksul.

|     Aruande väljad             |     Kirjeldus                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Alguskuupäev         |     Rentimise varaseima versiooni alguskuupäev.    |
|     Rendiperiood                |     Rentimise varaseima versiooni rendiperiood.           |
|     Järelejäänud makseid        |     Rendi jaoks veel sisestamata maksete arv.                       |
|     Algsaldo         |     Kõikide kannete summa, mis mõjutavad enne aruande kuupäeva rendikohustist.             |
|     Esialgne tuvastamine       |     Mis tahes esialgse tuvastamise tehingu summa rendi jaoks, mis sisestati aruandes määratletud kuupäevavahemikus.     |
|     Maksed                  |     Rendimaksete kannete summa, mis sisestati aruande jaoks määratletud kuupäevavahemikus. Selle veeru väärtused kuvatakse negatiivsete summadena, kuna maksed vähendavad rendikohustise saldot.  |
|     Viivis                  |     Intressi laekumiste summa, mis on sisestatud seosest rendiga aruande jaoks määratletud kuupäevavahemikus.            |
|     Korrigeerimised               |     Rendi sisestatud korrigeerimise tehingute summa, mis jääb aruande jaoks määratletud kuupäevavahemikku.                               |
|     Ending balance            |     Kõigi rendikohustiste tehingute saldo, mis on sisestatud aruande **lõpukuupäevaks**.                  |

## <a name="lease-transactions-report"></a>Rendkannete aruanne
Rendikannete päring kuvab kõik töölehe kirjed, mis on vara rentimise poolt loodud. Iga töölehe kirje on lingitud raamatu ID-ga, millest see pärineb. See võimaldab teil hõlpsalt seostada töölehe kirje vastava rendikirjega. Rendikannete päring toimib viisil, mis sarnaneb pearaamatu lehele **Kande tehingud**.

## <a name="weighted-average-discount-rate-report"></a>Kaalutud keskmise allahindluse määra aruanne
Kaalutud keskmise allahindluse määra aruanne vastab USA raamatupidamispõhimõtete teabe avalikustamise nõudele, mis on kaalutud keskmise allahindlusmäära jaoks määratletud ASC 842-20-50-4 punkti g lõikes 4. Selle aruande vaatamiseks minge jaotisse **Vara rentimised > Päringud ja aruanded > Kaalutud keskmise allahindluse määr**. Aruanne sisaldab järgmisi välju. 

|     Aruande väljad                     |     Kirjeldus                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Alates kuupäevast                        |     See aruanne sisaldab kõiki rendikirjeid, mis on alanud **alates** kuupäeva parameetril või enne seda. Seda aruannet tuleks käitada avaldatava perioodi viimasel päeval.      |
|     Juriidiline isik                      |     Rendikirjega seotud juriidiline isik.                           |
|     Rendi ID                          |     Unikaalne rendi ID.                                                  |
|     Rendi kirjeldus                 |     Rendi kirjeldus rendipäisest.                          |
|     Reserveerimine                              |     Kuvatud rendi konkreetne raamatu tüüp.                                                                                                                                            |
|     Sisestamiskiht                     |     Iga põhivaraga seotud raamat seadistatakse kindla sisestuskihi jaoks, millel on üldine kulumieesmärk.      |
|     Rendigrupp                       |     Rühm, kuhu rent kuulub.                                 |
|     Allahindluse määr                     |     Rendimaksete allahindamiseks kasutatud määr.                             |
|     Currency                          |     Tehingus kasutatava valuuta lühend. Kõik aruanded teisendavad ülekande valuuta aruandevaluutaks.  |
|     Järelejäänud rendimaksed          |     Maksegraafikus olevate tasumisele kuuluvate rendimaksete kogusumma **alates** kuupäevast.            |
|     Järelejäänud kaalutud maksed       |     Allesjäänud rendimaksed korrutatud kasutatud allahindluse määraga.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]