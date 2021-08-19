---
title: Tarnehnna päringud
description: See teema selgitab, kuidas leida ja kasutada erinevat tüüpi päringuid, mis on saadaval tarnehinna moodulis.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLine, ITMItemTracking, ITMContainerActivityTracking, ITMContainerTracking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 0b712e7869c592150a408834855bb1f4fa20277ca26182f0d065b8f3cd77296a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762934"
---
# <a name="landed-cost-inquiries"></a>Tarnehinna päringud

[!include [banner](../../includes/banner.md)]

## <a name="voyage-line-inquiries"></a>Reisiliini päringud

**Reisiliini** päringus kuvatakse kõik reisiliini vastavalt varudele. Päringut saab kasutada filtrina abistamaks kauba, ostutellimuse või muu kasuliku teabe otsimisel. Samuti saab seda kasutada eeldatava tarnekuupäeva tuvastamiseks kaubal, mis võib olla ühel või enamal reisil. Sel viisil aitab see hallata varude eeldatavat vastuvõttu.

Päringu avamiseks minge **Tarnehind \> Päringud \> Reisiliinid**.

### <a name="overview-tab"></a>vahekaart Ülevaade

Vahekaart **Ülevaade** **Reisiliinide** päringulehle sisaldab ruudustikku, mis näitab iga asjakohase reisiliini põhiteavet. Järgmises tabelis kirjeldatakse ruudustiku veergusid.

| Veerg | Kirjeldus |
|---|---|
| **Kaubakood** | Reisiliini kaup. |
| **Viide** | Tellimuse tüüp (ostutellimus või üleviimistellimus). |
| **Arv** | Ostutellimuse number või üleviimistellimuse number. |
| **Foolio** | Leht, mis on seotud reisiliiniga. |
| **Saatmiskonteiner** | Saadetise konteiner, mis on seotud reisiliiniga. |
| **Reis** | Reis, mis on seotud reisiliiniga. |
| **Kogus** | Reisiliini kauba kogus. |
| (Muud mõõtmed) | Vajaduse korral saate võrgustikus kuvada täiendavate mõõtmete veerge. Nende mõõtmete hulka kuuluvad partii number, varude olek ja ladu. Tegevuspaanil valige **Varud \> Kuva dimensioonid**, et avada dialoogiboks, kus saate valida kaasamiseks dimensioonid. |

### <a name="general-tab"></a>Vahekaart Üldine

Valige **Üldine** vahekaart, et vaadata praegu valitud rea kohta lisateavet vahekaardil **Ülevaade**.

### <a name="dimensions-tab"></a>Vahekaart Mõõtmed

Valige **Mõõtmed** vahekaart, et näha võimalike mõõtmete väärtusi reale, mis on valitud **Ülevaade** vahekaardil, olenemata sellest, millised mõõtmed olete seal kuvamiseks valinud.

## <a name="cost-estimate-inquiries"></a>Kuluhinnangu päringud

Iga kord kuluhinnangu loomisel lisatakse hinnang päringulehele **Kuluhinnangud**. Täielikku teavet selle kohta, kuidas luua, vaadata ja töötada kuluhinnangutega (sh päringulehel olevad hinnangud), vt [Hinda ja halda tarnehinda](estimate-manage-landed-costs.md).

## <a name="item-tracking"></a>Kauba jälgimine

Kasutage lehte **Kauba jälgimine** avatud ostutellimuste ridade ja nende praeguse oleku vaatamiseks. Ridu ei pea reisiga seostama, et siin näha. Kui kaup on siiski seotud reisiga, kuvatakse kauba jälgimiskirje real reisi ID.

Selle lehe avamiseks minge **Tarnehind \> Päringud \> Jälgimine \> Kauba jälgimine**.

Kuna teie süsteem sisaldab tõenäoliselt väga suurt hulka ostutellimuse ridu, siis **kauba jälgimise** leht ei näita algset ühtegi kirjet. Alustage, kasutades filtri välju lehekülje ülaosas, et määrata otsite ostutellimuse ridade komplekti. Seejärel valige **Uuenda** tegevuspaanil, et luua nimekiri. Võite kasutada tärni (\*) igal filtriväljal metamärgina. Näiteks, et leida kõik ostutellimuse read kaupadele, mille nimes on sõna "DVD", seadke väljale **Tüüp** väärtus **Toote nimi** ja sisestage väärtus *\*DVD\** väljale **Välja väärtus**.

> [!NOTE]
> Praegu sisaldavad järeltellimused ainult müügitellimusi. Müügipakkumine ei ole kuvatud ega võetus arvesse järeltellimustes.

Järgmine tabel kirjeldab veerud ruudustikus **Kauba jälgimise** lehel.

| Veerg | Kirjeldus |
|---|---|
| **Sihtsadam** | Lõppsihtkoht. |
| **Kinnitatud** | Ostutellimuse rea kinnituskuupäev. |
| **Tarnekuupäev** | Ostutellimuse rea tarnekuupäev. |
| **Reis** | Kui rida on seotud reisiga, reisi-ID. |
| **Saatmiskonteiner** | Kui rida on lisatud saadetise konteinerile, siis konteineri ID. |
| **Saatmissadam** | Praegune sadam, mis põhineb jälgimisvormi esimesel etapil, kus ostutellimuse reaga seotud saatmiskonteinerile pole tegelikku kuupäeva seatud. |
| **Tegevus** | Praegune tegevus, mis põhineb jälgimisvormi esimesel etapil, kus ostutellimuse reaga seotud saatmiskonteinerile pole tegelikku kuupäeva seatud. |
| **Eeldatav lõppkuupäev** | Kuupäev, mil reis peaks olema sihtlaos vastu võetud. |
| **Nimi** | Tarnija nimi. |
| **Reisi olek** | Saadetise staatus, mis ons seotud ostu tellimusreaga. |
| **Kaubakood** | Ostutellimuse rea kauba number. |
| **Väline** | Hankija kauba nimi. |
| **Toote nimi** | Kauba nimi ostutellimuse rea jaoks. |
| **Kogus** | Ostutellimuse rea kogus ostutellimuse reale. |
| **Üksus** | Ostutellimuse rea mõõtühik. |
| **Viide** | Tellimuse tüüp (ostutellimus või üleviimistellimus) |
| **Viitenumber** | Ostutellimuse number või üleviimistellimuse number. |
| **Järeltellimus** | Sümbol näitab, et kaubal on müügi järeltellimusi. |
| (Muud mõõtmed) | Vajaduse korral saate võrgustikus kuvada täiendavate mõõtmete veerge. Nende mõõtmete hulka kuuluvad partii number, varude olek ja ladu. Tegevuspaanil valige **Kuva mõõtmed**, et avada dialoogiboks, kus saate valida kaasamiseks dimensioonid. |

### <a name="related-information-about-backorders"></a>Järeltellimustega seotud teave

Järeltellimuste kohta lisateabe vaatamiseks valige lehe paremal pool vahekaart **Seotud teave** ja seejärel valige **Järeltellimused**. Konkreetse järeltellimuse kohta lisateabe saamiseks valige selle jaoks rida ja seejärel valige link **Veel**.

## <a name="individual-shipping-container-tracking"></a>Individuaalse saatmiskonteineri jälgimine

**Üksikute konteinerite jälgimise** päring sisaldab filtrit, mis võimaldab teil leida saatmiskonteineri ja seejärel tuvastada kõik selle konteineri reisiliinid.

Selle päringu avamiseks minge **Tarnehind \> Päringud \> Jälgimine \> Individuaalne kaubakonteineri jälgimine**.

## <a name="multiple-shipping-container-tracking"></a>Mitme saatmiskonteineri jälgimine

**Mitme konteineri jälgimise** päring sisaldab filtrit, mis võimaldab teil leida saatmiskonteinerite hulga ja seejärel tuvastada kõik nende konteinerite reisiliinid.

Selle päringu avamiseks minge **Tarnehind \> Päringud \> Jälgimine \> Mitme kaubakonteineri jälgimine**.
