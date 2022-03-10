---
title: Rendi sisestuskontode seadistamine
description: Selles teemas loetletakse vara rendikannete jaoks nõutavad sisestuskontod ja selgitatakse, kuidas määratleda rendi sisestamise parameetrite lehel sisetuskontod.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ac8dc59a19a489c6a7c4bf6621dd1a316de03ac3af4512d3ed7e55668af801b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770637"
---
# <a name="set-up-lease-posting-accounts"></a>Rendi sisestuskontode seadistamine

[!include [banner](../includes/banner.md)]

Selles teemas loetletakse vara rendikannete jaoks nõutavad sisestuskontod ja selgitatakse, kuidas määratleda lehel **Rendi sisestamise parameetrid** sisetuskontod.

Vastavalt raamatupidamisstandardite kodifitseerimise teemale 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardile 16 (IFRS 16) võib olla vajalik luua oma kontoplaanis kontod. Siiski ei ole kõik kontod, mille vastavalt ASC-i ja IFRS-i standarditele loote, põhivara kontod. ASC 842 kohaselt kirjendatakse kasutamisõiguse esemeks oleva vara nii kapitali- kui kasutusrendi korral. Need rendid on põhivaradest eraldi. (Kasutamisõiguse esemeks olevat vara võite siiski hallata põhivarade abil.)

Lisateavet kontostruktuuride loomise kohta leiate jaotisest [Kontostruktuuride loomine](../general-ledger/tasks/create-account-structures.md). Lisateavet põhikonto loomise kohta leiate jaotisest [Põhikonto loomine](../general-ledger/tasks/create-main-account.md).

Järgmine tabel näitab näiteid kontodest, mis tuleb luua renditud vara kannete jaoks, kui neid ei ole juba loodud. IFRS 16-i kohaselt kasutatakse kasutusrendi seoseid endiselt väikese väärtusega ja lühiajaliste rendilepingute puhul.

| Pearaamatukonto number | Konto tüüp  | Konto nimi                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Vara         | Sõiduki kasutamisõiguse esemeks olev vara                                     |
| 180160                | Vara         | Hoone kasutamisõiguse esemeks olev vara                                    |
| 180250                | Vara         | Kogunenud kulum - sõidukid                   |
| 180260                | Vara         | Kogunenud kulum - hooned                  |
| 222300                | Kohustus     | Lühiajaline kohustus - kapitalirent                |
| 222310                | Bilanss | Lühiajaline kohustus - kasutusrent              |
| 250200                | Kohustus     | Kreditoorne võlgnevus                                         |
| 250601                | Bilanss | Pikaajaline kohustus - kapitalirent                 |
| 250602                | Bilanss | Pikaajaline kohustus - kasutusrent               |
| 250606                | Bilanss | Edasilükatud rent                                         |
| 300160                | Bilanss | Jaotamata kasum                                     |
| 604500                | Expense       | Rendikulu                                         |
| 604501                | Expense       | Sõiduki kasutusrendi kulu – intressi juurdekasv  |
| 604502                | Expense       | Sõiduki kasutusrendi kulu – amortisatsioon        |
| 605200                | Expense       | Hoone kasutusrendi kulu – intressi juurdekasv |
| 605201                | Expense       | Hoone kasutusrendi kulu – amortisatsioon       |
| 607101                | Expense       | Sõiduki rendi amortisatsiooni kulu                    |
| 607102                | Expense       | Hoone rendi amortisatsiooni kulu                   |
| 607103                | Expense       | Väärtuse languse kulu - kapitalirent                   |
| 607104                | Expense       | Väärtuse languse kulu - kasutusrent                 |
| 618910                | Expense       | Rendikulu - kapitalirent                        |
| 618920                | Expense       | Muutuvad maksed - kapitalirent                    |
| 618930                | Expense       | Muutuvad maksed - kasutusrent                  |
| 800600                | Expense       | Sõiduki rendi intressikulu                        |
| 800601                | Expense       | Hoone rendi intressikulu                       |
| 801201                | Bilanss | Kasum ja kahjum - liisingu muutmine                      |

## <a name="configure-posting-accounts"></a>Sisestuskontode konfigureerimine

Loodud rendiraamatutele ja rühmadele kontode määramiseks peate konfigureerima varade rendi parameetrid.

1. Avage **Vara rentimine \> Seadistus \> Rendi sisestamise parameetrid**.
2. Avage vahekaardil **Kontod** kiirkaart **Rendikontod**. Määratlege põhikontod kapitali- ja kasutusrendi jaoks vastavale **Sisestamistüübile**. Eeltoodud tabelis kuvatakse kasutus- ja kapitalirendiga seotud kontod.

    > [!NOTE]
    > See etapp nõuab, et te seadistate eraldi kontod nii kasutus- kui ka kapitalirendile iga sisestamistüübi jaoks, välja arvatud **Rendikulu vastaskonto** ja **Rendi suurenemine/vähenemine**. Ettevõtted, mis järgivad IFRS 16 raamatupidamisraamistikku, peavad lisama kasutusrendi jaoks põhikonto. Kuid süsteem ei kasuta seda kontot, kuigi see on kohustuslik väli, sest kõik IFRS 16-le vastavad rendilepingud liigitatakse kapitalirendina.
    >[!NOTE]
    > **Rendi suurenemist/vähendamist** kasutatakse sisestustüübina varade täiendavate kaalutluste korral, sealhulgas **esmaste otsekulutuste, rendistiimulite, rendi ettemaksete ja demonteerimiskulude** korral, kuid kasutamisõiguse esemeks olev vara sisestatakse põhikontole, mis on vaikimisi **Renditav vara**.        
    
3. Põhikontole vastava rendigrupi valimiseks valige väljal **Konto kood** väärtus **Grupp**. Seejärel valige väljal **Konto/grupi number** põhikontole määratav rendigrupp.
4. Süsteemis seadistatud halduskuludele konto koodide määramiseks valige kulu kiirkaardi **Täitekulu** väljal **Kulu tüüp**. Seejärel määrake igale raamatule kasutamiseks finants- ja kasutusel olevad kontod.

    > [!NOTE]
    > Valitud finants- või kasutusel olev konto debiteeritakse, kui plaanitud kulu arve sisestatakse.
    > **Rendikulu vastaskontot** kasutatakse täitekulude kannete sisestamistüübina, aga sisestatakse määratletud **Vastaskontole** **Täitekulude maksegraafikute ridadel** rendi üksikasjade juures või rendiraamatu vormil.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
