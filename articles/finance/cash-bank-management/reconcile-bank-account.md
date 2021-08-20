---
title: Pangakonto vastavusseviimine
description: See teema kirjeldab, kuidas pangakontot vastavusse viia.
author: panolte
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e06a38a19a16a07d77d0c9aceaa4e3206646dd0561996681b417b785058f3938
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739355"
---
# <a name="reconcile-a-bank-account"></a>Pangakonto vastavusseviimine

[!include[banner](../includes/banner.md)]

Pangaväljavõtte saamisel tuleb teil juriidilise isiku pangakanded viia perioodiliselt vastavusse kannetega pangaväljavõttel.

Te ei saa viia pangakonto väljavõtet vastavusse pangakontoga, kui väljavõttel loetletud tšekkidest või deposiidikviitungi maksetest on hetkel olekus **Tühistamise ootel**. Pärast seda, kui ülevaataja sisestab või lükkab tagasi tšeki tühistamise või deposiidikviitungi makse tühistamise, pole olek enam **Tühistamise ootel** ja te saate pangakonto vastavusse viia.

1.  Minge jaotisse **Sularaha- ja pangahaldus**\>**Pangakontod**\>**Pangakontod**. Valige pangakonto, millega pangaväljavõtet vastavusse viia ja valige **Vii vastavusse** > **Konto vastavusseviimine**.

2.  Sisestage teave väljadele **Pangaväljavõtte kuupäev** ja **Pangaväljavõte**. Väljale **Lõppsaldo** sisestage pangakonto saldo, mille leiate pangakonto väljavõttelt.

3.  Valige **kanded**, et avada leht **Konto vastavusse viimine**.

4.  Iga kande puhul, mis kaasatakse pangakonto väljavõttesse, valige märkeuut **Tühjendatud**, kui summa rakenduses Dynamics 365 Finance vastab summale pangaväljavõttel. Väärtust saate sisestada või muuta ka väljal **Pangakande tüüp**. See on oluline teie pangakannete statistika ja mõnede aruannete jaoks.
    

    > [!NOTE]
    > <P>Ärge märkige märkeruutu <STRONG>Tühjendatud</STRONG> kannetel, mis pole pangakonto väljavõttel. Need kanded ilmuvad jätkuvalt sellel lehel, kuni on vastavusse viidud tulevase pangaväljavõttega.</P>
    > <P>Märkeruut <STRONG>Tühjendatud</STRONG> ei ole saadaval, kui kande olek on <STRONG>Tühistamise ootel</STRONG>. Kannetel on see olek juhul, kui Finance on seadistatud nõudele, et tühistamised saadetakse enne sisestamist ülevaatusele. Pärast seda, kui ülevaataja sisestab või lükkab tagasi ümberpööramise või tühistamise, pole olek enam <STRONG>Tühistamise ootel</STRONG> ja te saate pangakonto pangaväljavõttega vastavusse viia.</P>

    
    Märkeruudu **Tasaarvestatud** valimiseks tšekkide intervalli puhul, mis kuvatakse kõik pangaväljavõtte puhul, valige **Märgi tšeki intervall** ja seejärel määrake intervall.

5.  Kui pangakonto kande summa ei vasta pangaväljavõtte kandel olevale summale, sisestage parandussumma väljale **Parandussumma**.
    

    > [!NOTE]
    > <P>Kui parandatava kande fiskaalperiood on suletud, ei saa välja <STRONG>Parandussumma</STRONG> kasutada. Selle asemel looge paranduse jaoks rida, mis on avatud fiskaalperioodis. Sel juhul peate lisama finantsdimensioonid, mida kasutati esialgsel kandel ja samuti vastaskonto põhikonto.</P>



6.  Looge kanded kirjetele (nagu tasud ja intress), mis on pangakonto väljavõttes, kuid mida pole talletatud rakenduses Finance. Sisestage **Pangakande tüüp** ja asjakohased finantsdimensioonid.

7.  Kuna kanded pangakonto väljavõttel on märgitud **Tühjendatud**, siis läheneb summa nullile väljal **Vastavusse viimata**, mida arvutatakse pidevalt uuesti vastavalt teie tehtud muudatustele. Kui see jõuab nullini, klõpsake **Vii konto vastavusse**, et sisestada vastavusseviimine ning kanded ja parandused, mille olete loonud.
    
    Pärast vastavusseviimise sisestamist ei saa kaasatud kandeid rohkem üle vaadata või parandada ja need ei ilmu mitte üheski tulevases konto vastavusseviimises.

8.  Veel vastavusse viimata pangakannete vaatamiseks kasutage aruannet **Vastavusse viimata kanded**. Pangakonto pangaväljavõtte vaatamiseks kasutage aruannet **Pangaväljavõte**.

## <a name="cancel-bank-statement-reconciliation"></a>Tühista pangaväljavõtte vastavusseviimine 

Pangaväljavõtte vastavusse viimise tühistamise funktsioon võimaldab tühistada pangaväljavõtte vastavusse viimise. Selle funktsiooni kasutamiseks lubage funktsioon **Loobu pangaväljavõtte vastavusseviimisest** tööruumist **Funktsiooni haldamine**. Samuti peate lubama parameetri **Luba pangaväljavõtte redigeerimine**. Selleks minge jaotisse **Sularaha- ja pangahaldus > Häälestus > Sularaha- ja pangahalduse parameetrid > Panga vastavusseviimine**.
 
Pangaväljavõtte vastavusseviimise saab tühistada ainult selle sisestamise kronoloogilises järjestuses. Kui pangaväljavõtte vastavusseviimine tühistatakse, tühistatakse uued kanded ja parandused ning kõik muud kanded tähistatakse kui vastavusse viimata.
 
Pangaväljavõtte vastavusseviimise tühistamiseks valige pangaväljavõte ja valige **Pangaväljavõte > Tühista panga vastavusseviimine**. Lehel **Tühista panga vastavusseviimine** sisestage **Põhjusekood**, **Põhjuse kommentaar** ja **Tühistamise kuupäev**. Tühistamise alustamiseks valige **OK**. Pange tähele, et pangaväljavõtte tühistamise kuupäev peab olema pangaväljavõtte kuupäeval või pärast seda. Pärast pangaväljavõtte vastavusseviimise tühistamist uuendatakse välja **Tühistamise kuupäev** panga väljavõtte jaoks sisestatud **Tühistamise kuupäevaga**. Klõpsake nuppu **Kanded**, et vaadata kandeid, mille vastavusseviimine tühistati.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]