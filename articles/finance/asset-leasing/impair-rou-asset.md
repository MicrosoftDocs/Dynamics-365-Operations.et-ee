---
title: Kasutamisõiguse esemeks olevate varade väärtuse langus
description: See artikkel kirjeldab funktsioone, mis salvestavad kahjustuse, ja kohandab raamatupidamisstandardite kodeerimise teema 842 (ASC 842) kasutusrendi vara kulumigraafikut.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f953b3a351859c6becba10a129bbb17b49be6290
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894109"
---
# <a name="impair-right-of-use-assets"></a>Kasutamisõiguse esemeks olevate varade väärtuse langus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kui kasutamisõiguse esemeks oleva vara bilansiline summa ei ole taastatav, peate võib-olla kontrollima, kas vara väärtus on langenud. Kui teete kindlaks, et vara väärtus on langenud, saab vara rentimine kirjendada väärtuse langust ja korrigeerida vastavalt kulumi graafikut. See artikkel kirjeldab funktsioone, mis salvestavad kahjustuse, ja kohandab raamatupidamisstandardite kodeerimise teema 842 (ASC 842) kasutusrendi kulumigraafikut. Sama meetod kehtib ka rahvusvahelises finantsaruandluse standardis 16 (IFRS 16) rendile.

Kasutamisõiguse esemeks oleva vara järelejäänud saldo amortiseeritakse vastavalt allesjäänud perioodide arvule lineaarselt, sõltumata sellest, kas rent liigitati kapitalirendiks IFRS 16 alusel või kasutusrendiks ASC 842 alusel.

## <a name="impair-an-rou-asset"></a>Kasutamisõiguse esemeks oleva vara väärtuse langus

1. Minge langenud väärtusega rendi juurde ja valige suvand **Raamatud**.
2. Toimingupaanil valige **Väärtuse langus**.
3. Sisestage kuvatavas dialoogiboksis väljale **Väärtuse languse summa** vara väärtuse languse summa. Kasutamisõiguse esemeks oleva vara vähendamiseks sisestage positiivne väärtus.
4. Väljale **Kande kuupäev** sisestage kuupäev, millal väärtuse languse kanne tuleb sisestada.
5. Väljale **Järelejäänud perioodid** sisestage allesjäänud amortiseerumise kuude arv.
6. Seadke suvand **Eelvaade**, et vaadata pakutavat vara saldot ja finantskirjet enne nende loomist või sisestamist.
7. Määrake suvand **Raamatu sulgemine** valikule **Jah**, et sulgeda rendiraamat. Selle tegevuse saate tagasi võtta, kasutades liisingu taasava **olekut**. Suletud rentide puhul ei saa kirjeid sisestada ja suletud rente ei saa muuta. 
8. Kahjustuse **kirje** loomiseks või sisestamiseks valige sisestus.

    > [!NOTE]
    > Pärast kahjustuse kande sisestamist luuakse uus raamatu versioon.

    > Kui rent klassifitseeritakse kasutusrendiks, arvutatakse kahjustusele järgmine igakuine kulum lineeeritud kulumi alusel.

9. Kahjustatud vara kulumigraafiku vaatamiseks avage rendiraamatu vara kulumigraafik. Vara amortiseeritakse nüüd lineaarselt vastavalt kuude arvule, mille sisestasite väljale **Järelejäänud perioodid**.
10. Väärtuse vähenemise töölehe kirje vaatamiseks valige vähenenud väärtusega rendi raamatu tegevuspaanil suvand **Vara rentimise tööleht**. Süsteem loob töölehe kirje, mis debiteerib väärtuse languse kulu sisestamise kontot ja krediteerib rendi vara sisestamise kontot. 
11. Kasutamisõiguse esemeks oleva vara uue bilansilise väärtuse vaatamiseks valige rendiraamatu tegevuspaanil suvand **Vara kanded**.

## <a name="example-of-rou-asset-impairment"></a>Kasutamisõiguse esemeks oleva vara väärtuse languse näide

Selles näites on rendiks mitte-spetsialiseeritud vara, mis ei loovuta omandiõigust ega anna rentnikule võimalust osta.

### <a name="setup"></a>Seadistus

Järgmistes tabelites on toodud väärtused, mis on määratud vahekaartidel **Üldine** ja **Maksegraafiku read** rendi jaoks, mida selles näites kasutatakse.

**Vahekaart Üldine**

| Field                      | Väärtus            |
|----------------------------|------------------|
| Vara õiglane väärtus    | 600,000          |
| Alternatiivne laenuintressimäär | 7%               |
| Liitmisintervall       | Kord aastas         |
| Vara kasulik tööiga (kuudes) | 600              |
| Annuiteedi tüüp               | Harilik annuiteet |
| Alguskuupäev          | 1.1.2019       |

**Maksegraafiku ridade vahekaart**

| Field             | Väärtus      |
|-------------------|------------|
| Alguskuupäev        | 1.1.2019   |
| Perioodi intervall   | Kord kuus    |
| Perioodid           | 120        |
| Lõppkuupäev          | 31.12.2028 |
| Makse sagedus | Kord aastas   |
| Maksesumma    | 10,000     |

### <a name="steps"></a>Etapid

1. Pärast selles artiklis kirjeldatud viisil liisingu loomist minge rendiraamatusse ja kinnitage maksegraafik. Seejärel sisestage esialgne tuvastuse töölehe kirje. Esialgne kasutamisõiguse esemeks olev vara ja rendikohustis peaks olema 70 235,81 eurot. Selle näite puhul liigitati rent kasutusrendiks ASC 842 alusel.
2. Käitage pakett-töölehe protsessi kolm korda, et simuleerida rendimaksete, intressikulu ja amortisatsioonikulu jaoks kolme aasta möödumine.
3. Pärast kõigi kolme pakett-töö käitamise lõpetamist minge tagasi rendiraamatusse ning avage kohustuse ja vara kannete tabelid, et vaadata kasutamisõiguse esemeks oleva vara ja rendikohustise praegust bilansiväärtust. Kolme aasta pärast peaks kohustise väärtus olema umbes –53 893,00 eurot ja vara väärtus peaks olema ligikaudu 53 893,00 eurot. 

    Kolme aasta pärast viib ettevõtte läbi väärtuse languse katsed ja teeb kindlaks kasutamisõiguse esemeks oleva vara väärtuse languse 35 000 eurot. Te peate selle väärtuse languse nüüd kirjendama.
    
4. Avage rendiraamat ja valige seejärel tegevuspaanil suvand **Väärtuse langus**.
5. Sisestage lehel **Väärtuse languse parameeter** järgmised üksikasjad.

    | Field                  | Väärtus    |
    |------------------------|----------|
    | Väärtuse languse summa      | 35,000   |
    | Kande kuupäev       | 1.1.2022 |
    | Järelejäänud perioode      | 84       |
    | Postita                   | Jah      |
    | Eelvaade enne sisestamist | Ei       |
    | Sule raamat             | Ei       |

6. Väärtuse languse kulu töölehe kanne on loodud ja sisestatud. Selle vaatamiseks minge rendiraamatus vara rentimise töölehele. Pange tähele, et väärtuse languse summat on debiteeritud väärtuse languse kulu sisestamise konto suhtes ja kasutamisõiguse esemeks oleva vara sisestamise kontot on krediteeritud.

7. Väärtuse languse netomõju vaatamiseks minge tabelitesse kohustise ja varade kanded. Pange tähele, et väärtuse languse kulu on vähendanud kasutamisõiguse esemeks olevat vara, kuid rendikohustise bilansiline maksumus pole muutunud.

Väärtuse langusel on veel üks mõju, millega peate arvestama. Kuna kasutamisõiguse esemeks oleva vara summa on nüüd rendikohustisest palju väiksem, tuleb summat amortiseerida varasemast erinevalt. Täpsemalt on põhivara nüüd amortiseeritud lineaarselt kogu järelejäänud 84 kuu jooksul, alates kande kuupäevast.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
