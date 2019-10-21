---
title: Käibemaksu ülevaade
description: Selles teemas antakse ülevaade käibemaksu süsteemist. Selgitatakse käibemaksu seadistamise elemente ja kuidas need koos töötavad.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2741eb51f93f2f0b627dd8676629077b6df0f1b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186459"
---
# <a name="sales-tax-overview"></a>Käibemaksu ülevaade

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Selles teemas antakse ülevaade käibemaksu süsteemist. Selgitatakse käibemaksu seadistamise elemente ja kuidas need koos töötavad.

<a name="overview"></a>Ülevaade
--------

Käibemaksuraamistik toetab mitmeid kaudsete maksude tüüpe, nt müügimaksu, käibemaksu (KM), kaupade ja teenuste maksu (GST), ühikupõhiseid tasusid ja kinnipeetavat maksu. Need maksud arvutatakse ja dokumenteeritakse ostu- ja müügikande tegemise ajal. Nende kohta tuleb regulaarselt aruandeid esitada ja neid maksuametile tasuda. 

Järgmisel diagrammil on näidatud maksuseadistuse üksused ja nendevahelised seosed.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Iga käibemaksu puhul, mille kohta ettevõte peab aru andma, tuleb määratleda käibemaksukood. Käibemaksukood talletab maksumäärad ja käibemaksu arvutamise reeglid. 

Iga käibemaksukood peab olema seotud käibemaksu tasakaalustusperioodiga. Käibemaksu tasakaalustusperioodid määratlevad intervallid, mille tagant käibemaksuaruandeid tuleb koostada ja käibemaksuasutusele tasuda. Iga käibemaksu tasakaalustusperiood tuleb määrata käibemaksuasutusele. Käibemaksuasutus kajastab üksust, millele käibearuandeid esitatakse ja käibemaksu tasutakse. See määratleb ka käibemaksuaruande ülesehituse. Käibemaksuasutused võivad olla seotud hankija kontodega. Lisateavet käibemaksu seadistamise kohta leiate teemast [Käibemaksu tasakaalustusperioodi määramine](tasks/set-up-sales-tax-settlement-periods.md).

Iga käibemaksukood peab olema seotud ka pearaamatu sisestusgrupiga. Pearaamatu sisestusgrupp määrab põhikontod, millele käibemaksukoodide summad sisestatakse. 

Määratleda saab ka valikulised käibemaksuaruandluse koodid. Neid saab määrata mitmesuguste summatüüpide käibemaksukoodidele, mida käibemaksukoodi puhul arvutatakse. Aruanne **Käibemaksu tasumine koodide lõikes** näitab antud käibemaksu tasakaalustusperioodi ja intervalli kogusummasid käibemaksuaruandluse koodi kohta. 

Igal kandel, mille arvutamine ja sisestamine käibemaksu puhul vajalik on, peab olema käibemaksugrupp ja kauba käibemaksugrupp. Käibemaksugrupid on seotud kande osapoolega (nt kliendi või hankijaga), samas kui kauba käibemaksugrupid on seotud kande ressursiga (nt kauba või hanke kategooriaga). Maksugrupid sisaldavad maksukoodide loendit. Maksukoodid, mis on kande puhul olemas nii käibemaksugrupis kui ka kauba käibemaksugrupis, on sellele kandele kehtivad maksukoodid. 

Järgmises tabelis kirjeldatakse üksusi ja maksu seadistusprotsessi.

| Tegevuste seadistamine                                                  | Kohustuslik/valikuline tegevus ja kirjeldus                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Põhikontode loomine.                                           | Nõutav. Ettevõtte maksude tasumiseks ja registreerimiseks kasutatavad põhikontod peavad olema loodud enne käibemaksufunktsiooni seadistamist.                                                                                                                                                                             |
| Seadistage käibemaksule pearaamatu sisestusgrupid.                     | Nõutav. Pearaamatu sisestamisgrupid määratlevad käibemaksu kajastamise ja tasumise põhikontod.   Lisateavet leiate teemast [Käibemaksu jaoks pearaamatu sisestusgruppide seadistamine](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Seadistage käibemaksuhaldurid.                                   | Nõutav. Käibemaksuasutused on asutused, millele tuleb maksuaruandeid esitada ja makse tasuda.    Lisateavet leiate teemast [Käibemaksuasutuste määramine](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Saate seadistada käibemaksu tasakaalustusperioode.                            | Nõutav. Käibemaksu tasakaalustusperioodid sisaldavad teavet selle kohra, millal ja kui sageli käibemaksu aruandeid tuleb esitada ja käibemaksu tasuda. Need on seotud käibemaksuasutusega.                                                                                                                                                       |
| Käibemaksuaruandluse koodide seadistamine.                               | Valikuline. Käibemaksuaruandluse koodid saab määrata käibemaksukoodidele mitme käibemaksukoodi summade kohta aruande koostamiseks ühe käibemaksuaruandluse koodi alusel. Lisateavet leiate teemast [Käibemaksuaruandluse koodide määramine](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Saate seadistada käibemaksukoode.                                         | Nõutav. Käibemaksukoodid sisaldavad iga käibemaksu määrasid ja arvutusreegleid. Käibemaksukoodid on seotud käibemaksu tasakaalustusperioodi ja pearaamatu sisestusgrupiga. Lisateavet leiate teemast [Käibemaksukoodide määramine](tasks/set-up-sales-tax-codes.md).                                |
| Käibemaksugruppide seadistamine.                                        | Nõutav. Käibemaksugrupid sisaldavad kande osapoolele (kliendile või hankijale) kehtivate käibemaksukoodide loendit. Antud kande puhul määrab käibemaksugruppi kuuluvate käibemaksukoodide ja kauba käibemaksugrupi ühisosa kande puhul kehtivad käibemaksukoodid.                  |
| Saate seadistada kauba käibemaksugruppe.                                   | Nõutav. Kauba käibemaksugrupid sisaldavad kande ressursile (tootele, teenusele jne) kehtivate käibemaksukoodide loendit. Antud kande puhul määrab käibemaksugruppi kuuluvate käibemaksukoodide ja kauba käibemaksugrupi ühisosa kande puhul kehtivad käibemaksukoodid. Lisateavet leiate teemast [Käibemaksugruppide ja kauba käibemaksugruppide häälestamine](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Saate seadistada käibemaksuparameetrid rakenduse parameetri lehtedel. | Nõutav. Valdkondades nagu pearaamat, müügireskontro ja ostureskontro tuleb seadistada kaudsete maksude õige arvutamise parameetrid. Kuigi enamikul neist parameetritest on vaikeväärtused, tuleb neid iga ettevõtte vajaduste kohaselt muuta.                                          |

## <a name="sales-tax-on-transactions"></a>Käibemaks kannetelt
Iga kande puhul (müügi-/ostudokumendi read, töölehed jne) tuleb sisestada käibemaksu arvutamiseks käibemaksugrupp ja kauba käibemaksugrupp. Vaikegrupid on määratud koondandmetes (nt klient, hankija, kaup ja hankekategooria), kuid saate kande gruppe käsitsi muuta, kui peate seda tegema. Mõlemad grupid sisaldavad käibemaksukoodide loendit ja kahe käibemaksukoodide loendi ühisosa määrab kandele kohaldatavate käibemaksukoodide loendi. 

Iga kande puhul saate vaadata arvutatud käibemaksu, avades lehe **Käibemaksukanne**. Saate vaadata dokumendi rea või kogu dokumendi käibemaksu. Teatud dokumentide (nt hankija arve ja päevaraamatute puhul) saate arvutatud käibemaksu korrigeerida, kui originaaldokumendil on näha erinevad summad.

## <a name="sales-tax-settlement-and-reporting"></a>Käibemaksu tasakaalustamine ja aruandlus
Käibemaksu kohta tuleb esitada aruanne ja maksta see maksuasutustele regulaarsete ajavahemike järel (kord kuus, kord kvartalis jne). Saate tasakaalustada maksukontosid ajavahemiku kohta, tasakaalustades need käibemaksu tasakaalustuskontoga, nagu on määratud pearaamatu sisestusgruppides. Sellele funktsioonile pääseb juurde lehel **Käibemaksu tasakaalustamine ja sisestamine**. Peate määrama käibemaksu tasakaalustusperioodi, mille eest käibemaks tasakaalustada tuleb. 

Pärast käibemaksu tasumist tuleb käibemaksu tasakaalustuskonto saldo tasakaalustada pangakontoga. Kui käibemaksu tasakaalustusperioodile määratud käibemaksuasutus on seotud hankija kontoga, sisestatakse käibemaksusaldo avatud hankija arvena ja selle saab lisada tavalisse maksesoovitusse.

## <a name="conditional-sales-tax"></a>Tingimuslik käibemaks
Tingimuslikku käibemaksu tuleb maksta proportsionaalselt ainult tegelikult arvel makstud summast. Seevastu tavakäibemaks arvestatakse arve esitamise ajal. Tingimuslikku käibemaksu tuleb tasuda käibemaksuhaldurile makse, mitte arve sisestamise ajal. Arve sisestamisel tuleb kanne registreerida käibemaksuregistri aruandes. Kuid kanne tuleb käibemaksu maksearuandest välja arvata. 

Tingimusliku käibemaksu ruudu märkimisel pearaamatu parameetrite vormil ei saa käibemaksu maha arvata enne, kui olete arve tasunud. Mõnes riigis/regioonis on see seadusjärgne nõue.

> [!NOTE]
> Kui märgite ruudu Tingimuslik käibemaks, peate seadistama käibemaksukoodid ja käibemaksugrupid ning looma pearaamatu sisestusgrupid funktsionaalsuse toetamiseks. |

###  <a name="example"></a>Näide

Tasakaalustate käibemaksud iga kuu. 15. juunil koostate kliendiarve summas 10 000 pluss käibemaks.
-   Käibemaks on 25 protsenti ehk 2500.
-   Arve maksetähtaeg on 30. juuli.

Üldjuhul tuleks tasakaalustada ja maksta maksuhaldurile 2500 arve sisestamise ajal juunis, kuigi te pole kliendilt veel makset saanud. 

Kuid kui kasutate tingimuslikku käibemaksu, siis tasakaalustatakse summa maksuhalduriga siis, kui 30. juulil kliendilt makse saate.


Lisateavet leiate teemast [Kinnipeetava maksu määramine](tasks/set-up-withholding-tax.md).
