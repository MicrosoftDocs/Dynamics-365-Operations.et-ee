---
title: "Käibemaksu ülevaade"
description: "Selles artiklis antakse ülevaade käibemaksu süsteemist. Selgitatakse käibemaksu seadistamise elemente ja kuidas need koos töötavad."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 1adee145d705f239e0c663d310234286478fead0
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-overview"></a>Käibemaksu ülevaade

Selles artiklis antakse ülevaade käibemaksu süsteemist. Selgitatakse käibemaksu seadistamise elemente ja kuidas need koos töötavad.

<a name="overview"></a>Ülevaade
--------

Käibemaksu raames toetab mitmeid kaudseid makse, näiteks käibemaksu, käibemaks (VAT), kaupade ja teenuste maksu (GST), üksus tasud ja kinnipeetava maksu. Need maksud arvutatakse ja dokumenteeritud ostu-müügi tehingute puhul. Aeg-ajalt peab olema teatatud ja makstava summaga. 

Järgmisel diagrammil on näidatud maksuseadistuse üksused ja nendevahelised seosed.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Iga käibemaksu, mida ettevõte peab moodustama tuleb määratleda käibemaksukood. Käibemaksukood talletab maksumäärad ja käibemaksu arvutamise reeglid. 

Iga käibemaksukood peab olema seotud käibemaksu tasakaalustusperioodiga. Käibemaksu tasakaalustusperioodid määratlevad intervallid, mille tagant käibemaksuaruandeid tuleb koostada ja käibemaksuasutusele tasuda. Iga käibemaksu tasakaalustusperiood tuleb määrata käibemaksuasutusele. Käibemaksuasutus kajastab üksust, millele käibearuandeid esitatakse ja käibemaksu tasutakse. See määratleb ka käibemaksuaruande ülesehituse. Käibemaksuasutused võivad olla seotud hankija kontodega. 

Iga käibemaksukood peab olema seotud ka pearaamatu sisestusgrupiga. Pearaamatu sisestusgrupp määrab põhikontod, millele käibemaksukoodide summad sisestatakse. 

Määratleda saab ka valikulised käibemaksuaruandluse koodid. Neid saab määrata mitmesuguste summatüüpide käibemaksukoodidele, mida käibemaksukoodi puhul arvutatakse. Aruanne **Käibemaksu tasumine koodide lõikes** näitab antud käibemaksu tasakaalustusperioodi ja intervalli kogusummasid käibemaksuaruandluse koodi kohta. 

Igal kandel, mille arvutamine ja sisestamine käibemaksu puhul vajalik on, peab olema käibemaksugrupp ja kauba käibemaksugrupp. Käibemaksugrupid on seotud kande osapoolega (nt kliendi või hankijaga), samas kui kauba käibemaksugrupid on seotud kande ressursiga (nt kauba või hanke kategooriaga). Maksugrupid sisaldavad maksukoodide loendit. Maksukoodid, mis on kande puhul olemas nii käibemaksugrupis kui ka kauba käibemaksugrupis, on sellele kandele kehtivad maksukoodid. 

Järgmises tabelis kirjeldatakse üksusi ja maksu seadistusprotsessi.

| Tegevuste seadistamine                                                  | Kohustuslik/valikuline tegevus ja kirjeldus                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Põhikontode loomine.                                           | Nõutav. Ettevõtte maksude tasumiseks ja registreerimiseks kasutatavad põhikontod peavad olema loodud enne käibemaksufunktsiooni seadistamist.                                                                                                                                                                             |
| Seadistage käibemaksule pearaamatu sisestusgrupid.                     | Nõutav. Pearaamatu sisestamisgrupid määratlevad käibemaksu kajastamise ja tasumise põhikontod.                                                                                                                                                                                                                            |
| Seadistage käibemaksuhaldurid.                                   | Nõutav. Käibemaksuasutused on asutused, millele tuleb maksuaruandeid esitada ja makse tasuda.                                                                                                                                                                                                                                   |
| Saate seadistada käibemaksu tasakaalustusperioode.                            | Nõutav. Käibemaksu tasakaalustusperioodid sisaldavad teavet selle kohra, millal ja kui sageli käibemaksu aruandeid tuleb esitada ja käibemaksu tasuda. Need on seotud käibemaksuasutusega.                                                                                                                                                       |
| Käibemaksuaruandluse koodide seadistamine.                               | Valikuline. Käibemaksuaruandluse koodid saab määrata käibemaksukoodidele mitme käibemaksukoodi summade kohta aruande koostamiseks ühe käibemaksuaruandluse koodi alusel.                                                                                                                                                                 |
| Saate seadistada käibemaksukoode.                                         | Nõutav. Käibemaksukoodid sisaldavad iga käibemaksu määrasid ja arvutusreegleid. Käibemaksukoodid on seotud käibemaksu tasakaalustusperioodi ja pearaamatu sisestusgrupiga.                                                                                                                                        |
| Käibemaksugruppide seadistamine.                                        | Nõutav. Käibemaksugrupid sisaldavad kande osapoolele (kliendile või hankijale) kehtivate käibemaksukoodide loendit. Antud kande puhul määrab käibemaksugruppi kuuluvate käibemaksukoodide ja kauba käibemaksugrupi ühisosa kande puhul kehtivad käibemaksukoodid.                  |
| Saate seadistada kauba käibemaksugruppe.                                   | Nõutav. Kauba käibemaksugrupid sisaldavad kande ressursile (tootele, teenusele jne) kehtivate käibemaksukoodide loendit. Antud kande puhul määrab käibemaksugruppi kuuluvate käibemaksukoodide ja kauba käibemaksugrupi ühisosa kande puhul kehtivad käibemaksukoodid. |
| Saate seadistada käibemaksuparameetrid rakenduse parameetri lehtedel. | Nõutav. Valdkondades nagu pearaamat, müügireskontro ja ostureskontro tuleb seadistada kaudsete maksude õige arvutamise parameetrid. Kuigi enamikul neist parameetritest on vaikeväärtused, tuleb neid iga ettevõtte vajaduste kohaselt muuta.                                          |

## <a name="sales-tax-on-transactions"></a>Käibemaks kannetelt
Iga kande puhul (müügi-/ostudokumendi read, töölehed jne) tuleb sisestada käibemaksu arvutamiseks käibemaksugrupp ja kauba käibemaksugrupp. Vaikegrupid on määratud koondandmetes (nt klient, hankija, kaup ja hankekategooria), kuid saate kande gruppe käsitsi muuta, kui peate seda tegema. Mõlemad grupid sisaldavad käibemaksukoodide loendit ja kahe käibemaksukoodide loendi ühisosa määrab kandele kohaldatavate käibemaksukoodide loendi. 

Iga kande puhul saate vaadata arvutatud käibemaksu, avades lehe **Käibemaksukanne**. Saate vaadata dokumendi rea või kogu dokumendi käibemaksu. Teatud dokumentide (nt hankija arve ja päevaraamatute puhul) saate arvutatud käibemaksu korrigeerida, kui originaaldokumendil on näha erinevad summad.

## <a name="sales-tax-settlement-and-reporting"></a>Käibemaksu tasakaalustamine ja aruandlus
Käibemaksu kohta tuleb esitada aruanne ja maksta see maksuasutustele regulaarsete ajavahemike järel (kord kuus, kord kvartalis jne). Microsoft Dynamics 365 operatsioonide pakub funktsiooni, mis võimaldab maksu Postipangas intervalli ja kompenseerida tulumaksu arvelduskontole vastavalt pearaamatu sisestusgruppide saldod. Seda funktsiooni saab kasutada selle **lahendada ja pärast käibemaksu** lehel. Määrake käibemaksu ütleks puhul käibemaksu tasakaalustusperioodi. 

Pärast käibemaksu tasumist tuleb käibemaksu tasakaalustuskonto saldo tasakaalustada pangakontoga. Kui käibemaksu tasakaalustusperioodile määratud käibemaksuasutus on seotud hankija kontoga, sisestatakse käibemaksusaldo avatud hankija arvena ja selle saab lisada tavalisse maksesoovitusse.

## <a name="conditional-sales-tax"></a>Tingimuslik käibemaks
Tingimuslik käibemaks on käibemaks, mis makstakse proportsionaalselt tegeliku summa, mis makstakse arvele. Seevastu standard arvutatakse kell arveldamise aeg. Tingimuslik käibemaks makstakse maksuameti kui makse on sisestatud, mitte siis, kui arve on sisestatud. Kui arve on sisestatud, tuleb esitada tehingu käibemaksuraamatu aruandesse. Aga tehing arvatakse käibemaksu tasumise aruanne. 

Kui märgite vormil pearaamatu parameetrid tingimuslik käibemaks ruut, saate käibemaksu maha enne arve tasumist. See on juriidiline nõue teatud riikides/regioonides.

> [!NOTE]
> Tingimuslik käibemaks ruut valimisel tuleb seadistada käibemaksu koodiga ja käibemaksugruppide ja ka saate luua, funktsionaalsuse. |

###  <a name="example"></a>Näide

Käibemakse saate tasakaalustada iga kuu. 15. juunil loote kliendile arve 10 000, pluss käibemaks.
-   Käibemaks on 25% või 2500.
-   Arve makse tuleb tasuda 30. juuli.

Tavaliselt teil lahendada ja maksma 2500 talle, kui arve on sisestatud juunis, isegi juhul, kui makse ei ole saanud kliendilt. 

Siiski tingimuslik käibemaks kasutamisel saate tasakaalustada maksuhalduriga kui teile makse kliendi kohta juuli 30.


