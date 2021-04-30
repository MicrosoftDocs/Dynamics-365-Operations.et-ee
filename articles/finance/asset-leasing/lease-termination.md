---
title: Rendilepingu lõpetamise ettepanek
description: See teema selgitab, kuidas teha rendilepingu lõppemise ettepanekut.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseTerminateLeaseListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6b32f9e8f80827e04269ac8cb6a4fbb5a13af8bc
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881104"
---
# <a name="propose-a-lease-for-termination"></a>Rendilepingu lõpetamise ettepanek

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Kui rendileping lõpetati vara, saab Vara rentimine kirjendada lõpetamise töölehe kirje, et kanda rendikohustus, kasutusõiguse (ROU) esemeks olev vara ja akumuleeritud kulum maha ja kirjendada kasum või kahjum. Varajane lõpetamisprotsess lõpetab rendilepingu ja sellega seotud rendiraamatud. See ei lõpeta individuaalseid rendiraamatuid. Selles teemas kirjeldatakse funktsioone, mis võimaldab teil teha rendilepingu lõpetamise ettepanek ja töödelda rendilepingu lõpetamise töölehes sisestust.

Kui rent ei ole klassifitseeritud edasilükatud rendina ja see ei ole seotud põhivaraga, loob Vara rentimine järgmise lõpetamise töölehe kande.

| Kanne                           | Deebet (Dr.) | Krediit (Cr.) |
|---------------------------------------|-------------|--------------|
| Dr. Rendikohustis                   | X           |              |
| Dr. Kogunenud kulum          | X           |              |
| Dr. Rendi muutmise kasum (kahjum) | X           |              |
| Cr. Rendivara                       |             | X            |
| Cr. Rendi muutmise kasum (kahjum) |             | X            |

Kui rendiraamat klassifitseeritakse edasilükatud rendi raamatuks, siis kirje kannab maha edasilükatud rendi saldo enne lõpetamist kasumi või kahjumi kontole, nagu siin näidatud.

| Kanne                           | Deebet (Dr.) | Krediit (Cr.) | 
|---------------------------------------|-------------|--------------|
| Dr. Edasilükatud rent                     | X           |              |
| Cr. Rendi muutmise kasum (kahjum) |             | X            |
| Cr. Edasilükatud rent                     |             | X            |
| Dr. Rendi muutmise kasum (kahjum) | X           |              |

Kui rendiraamat on seotud põhivaraga, võetakse kasutusõiguse esemeks olev vara arvele põhivarades. See raamatupidamine hõlmab varajaste lõpetamiste raamatupidamist. Vara rentimine loob järgmise töölehekirje rendikohustise mahakandmiseks.

| Kanne                           | Deebet (Dr.) | Krediit (Cr.) |
|---------------------------------------|-------------|--------------|
| Dr. Rendikohustis                   | X           |              |
| Cr. Rendi muutmise kasum (kahjum) |             | X            |

Teavet kasutamisõiguse esemeks olevast varast vabanemiseks leiate jaotisest [Põhivara likvideerimine praagina](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Rendilepingu lõpetamise ettepanek

1. Minge lõpetatava rendi juurde ja siis valige toimingupaanilt suvand **Lõpetamise ettepanek**.

    > [!NOTE]
    > Nupp **Lõpetamise ettepanek** ei ole saadaval, kui esineb sisestamata töölehekandeid mistahes raamatu kohta. Enne rendilepingu lõpetamist peate sisestama või kustutama kõik töölehe kirjed, mis on rendi suhtes loodud.

2. Kuvatavas dialoogiboksis seadistage lõpetamise töölehe kande väljad **Kehtivuse algus** ja **Sisestuskuupäev**.
3. Rendilepingu lõpetamise ettepaneku tegmiseks valige **Lõpetamise ettepanek**.
4. Valige **Sisesta rendilepingu lõpetamine**, et sisestadda rendilepingu lõpetamise töölehe kirje automaatselt.
5. Valige lehel **Rendilepingu lõpetamised** selle rendilepingu ID, mille lõpetamise ettepaneku tegite, et vaadata lõpetamise ridu. Lepingu lõpetamise ridadel kuvatakse kasutamisõiguse esemeks oleva vara, rendikohustise, akumuleerunud kulumi, edasilükatud rendi (kui on kohaldatav) ning kasumi või kahjumi väärtused, mis tuleb rendilepingu lõpetamisel tuvastada.

Rendileping on nüüd lõpetamiseks valmis. Rendiraamatu välja **Lõpetamise olek** väärtus on muudetud väärtuseks **Lõpetamiseks valmis**. Nüüd ei saa te enam sisestada rendiga seotud töölehe kirjeid, seda korrigeerida või väärtust langetada. 

## <a name="process-leases-that-are-ready-for-termination"></a>Lõpetamiseks valmis rendilepingute töötlemine

Lõpetamiseks valmis olevate rendilepingute töötlemiseks ja lõpetamise töölehekirje sisestamiseks toimige järgmiselt.

1. Valige lehel **Rendilepingute lõpetamised** töödeldav rendileping ja seejärel valige **Lõpeta**.
2. Kuvatavas dialoogiboksis tehke valik **OK**.

Süsteem sisestab lõpetamise töölehe kirje. Rendiraamatu väli **Rendi olek** määratakse olekule **Lõpetatud** ja välja **Lõpetamisettepaneku olek** väärtus seadistatakse olekusse **Lõpetatud**.

## <a name="reverse-a-lease-termination"></a>Liisingulepingu lõpetamise tagasipööramine

Liisingu lõpetamise töölehe kande tühistamiseks ja lõpetatud rendi avamiseks järgige seda juhist.

- Valige lehel **Rendilepingute lõpetamised** tagasipööratav lõpetatud rendileping ja seejärel valige **Lõpetamise tagasipööramine**.

Süsteem tühistab lõpetamise töölehe kirje. Rendiraamatu väli **Rendi olek** seadistatakse olekule **Avatud**. Renti ei kuvata enam lehel **Rendilepingu lõpetamised** ja selle kohta saab teha uue lõpetamise ettepaneku.

## <a name="example-of-a-lease-termination"></a>Rendilepingu lõpetamise näide

Selles näites on rendileping seotud mitte-spetsialiseeritud varaga, mis ei loovuta vara omandiõigust ega anna rentnikule võimalust vara osta.

### <a name="setup"></a>Seadistus

Järgmistes tabelites on toodud väärtused, mis on määratud vahekaartidel **Üldine** ja **Maksegraafiku read** rendi jaoks, mida selles näites kasutatakse.

**Vahekaart Üldine**

| Field                      | Väärtus            |
|----------------------------|------------------|
| Vara õiglane väärtus    | 600,000          |
| Currency                   | USA dollar              |
| Esmased otsekulutused       | 1000            |
| Alternatiivne laenuintressimäär | 7%               |
| Liitmisintervall       | Kord aastas         |
| Vara kasulik tööiga (kuudes) | 600              |
| Annuiteedi tüüp               | Harilik annuiteet |
| Alguskuupäev          | 1.1.2019         |

**Maksegraafiku ridade vahekaart**

| Field             | Väärtus      |
|-------------------|------------|
| Alguskuupäev        | 1.1.2019   |
| Perioodi intervall   | Kord kuus    |
| Perioodid           | 120        |
| Lõppkuupäev          | 31.12.2028 |
| Makse sagedus | Kord aastas   |
| Maksesumma    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Rendilepingu lõpetamise etapid

1. Pärast rendi selle teemas varasemalt kirjeldatud viisil loomist avage rendiraamat ja kinnitage maksegraafil. Seejärel sisestage esialgne tuvastuse töölehe kirje. Esialgne kasutamisõiguse esemeks olev vara on 71 235.81 USD ja rendikohustis peaks olema 70 235.81 USD. Selle näite puhul liigitati rent kasutusrendiks Raamatupidamisstandardite kodeerimise teema 842 (ASC 842) alusel.
2. Käitage pakett-töölehe protsessi kolm korda, et simuleerida rendimaksete, intressikulu ja amortisatsioonikulu jaoks kolme aasta möödumine.
3. Pärast kõigi kolme pakett-töö käitamise lõpetamist minge tagasi rendiraamatusse ning avage kohustuse ja vara kannete tabelid, et vaadata kasutamisõiguse esemeks oleva vara ja rendikohustise praegust bilansiväärtust. Kolme aasta pärast peaks kohustise väärtus olema umbes –53 893.00 USD ja vara väärtus peaks olema ligikaudu 54 593.00 USD.

    Pärast kolme aasta möödumist lepivad ettevõte ja rendileandja ühiselt kokku rendilepingu lõpetamises. Seepärast peate nüüd rendi lõpetama.

4. Minge lõpetatava rendi juurde ja siis valige toimingupaanilt suvand **Lõpetamise ettepanek**. 
5. Sisestage kuvatava dialoogiboksi väljadele **Kehtivuse algus** ja **Sisestuskuupäev** väärtus **1/1/2021**.
6. Rendilepingu lõpetamise ettepaneku tegmiseks valige **Lõpetamise ettepanek**.

    Kuvatakse leht **Rendilepingu lõpetamine** ja kuvatakse lõpetatav rendileping.

7. Valige selle rendilepingu ID, mille lõpetamise ettepaneku tegite, et vaadata lõpetamise ridu. Lepingu lõpetamise read näitavad rendi bilansiväärtusi. Järgnev tabel näitab, millised need väärtused selle näite puhul peaksid olema. 

    | Field                                                 | Väärtus      |
    |-------------------------------------------------------|------------|
    | Kohustuse bilansiline saldo kandevaluutas | 53 892.89 USD |
    | Kasutamisõiguse aluseks olev vara kandevaluutas            | 71 235.81 USD |
    | Akumuleeritud kulum kandevaluutas      | 16 642.92 USD |
    | Kasum (kahjum) kandevaluutas                   | - 700.00 USD   |

8. Lõpetamise töölehe kirje sisestamiseks valige rendileping lehel **Rendilepingute lõpetamised** ja valige **Lõpeta**.
9. Kuvatavas dialoogiboksis tehke valik **OK**.
10. Loodud ja sisestatud lõpetamise töölehe kande vaatamiseks minge vara tööraamatu vara rentimise töölehele. Järgnev tabel näitab, millised need väärtused selle näite puhul peaksid olema.

    | Kanne                           | Deebet (Dr.) | Krediit (Cr.) |
    |---------------------------------------|-------------|--------------|
    | Dr. Rendikohustis                   | 53,892.89   |              |
    | Dr. Kogunenud kulum          | 16,642.92   |              |
    | Dr. Rendi muutmise kasum (kahjum) | 700.00      |              |
    | Cr. Rendivara                       |             | 71,235.81    |

11. Lepingu lõpetamise netomõju vaatamiseks, kus kasutamisõiguse esemeks oleva vara ja rendikohustise väärtuseks on 0 (null), avage kohustuste ja varade kannete tabelid.

Rendi olek peaks nüüd olema **Lõpetatud**. Selle rendi suhtes ei sisestata rohkem töölehe kirjeid, välja arvatud juhul, kui lõpetamine tühistatakse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
