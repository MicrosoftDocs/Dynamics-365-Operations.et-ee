---
title: Pangakonto vastavusseviimine
description: See artikkel kirjeldab pangakonto vastavusseviimise võtteid.
author: angelad116
ms.date: 11/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 12de50f26127c54c2f82ace43487de10e7125aea
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804206"
---
# <a name="reconcile-a-bank-account"></a>Pangakonto vastavusseviimine

[!include[banner](../includes/banner.md)]

Pangaväljavõtte saamisel tuleb teil juriidilise isiku pangakanded viia perioodiliselt vastavusse kannetega pangaväljavõttel.

Te ei saa pangaväljavõtet pangakontoga vastavusse viia, kui väljavõttel loetletud mis tahes tšekkide või deposiitkviitungi maksete olek on praegu Ootel **tühistamine**. Pärast seda, kui ülevaataja sisestab või lükkab tagasi tšeki tühistamise või deposiidikviitungi makse tühistamise, pole olek enam **Tühistamise ootel** ja te saate pangakonto vastavusse viia.

1. Minge jaotisse **Sularaha- ja pangahaldus**\>**Pangakontod**\>**Pangakontod**. Valige pangakonto, millega pangaväljavõtet vastavusse viia ja valige **Vii vastavusse** > **Konto vastavusseviimine**.

2. Sisestage teave väljadele **Pangaväljavõtte kuupäev** ja **Pangaväljavõte**. Väljale **Lõppsaldo** sisestage pangakonto saldo, mille leiate pangakonto väljavõttelt.

3. Valige **kanded**, et avada leht **Konto vastavusse viimine**.

4. Iga pangaväljavõttel oleva **kande puhul märkige ruut Cleared** (Tühjendatud), kui Dynamics 365 Finance’i summa vastab pangaväljavõtte summale. Väärtust saate sisestada või muuta ka väljal **Pangakande tüüp**. See on oluline teie pangakannete statistika ja mõnede aruannete jaoks.
    

>[!NOTE]
>Ärge märkige ruutu **Tühjendatud** kannete puhul, mis pole pangaväljavõttes. Need kanded ilmuvad jätkuvalt sellel lehel, kuni on vastavusse viidud tulevase pangaväljavõttega.
>Kui **kande** olek on Ootel tühistamine, pole märkeruut **Tühjendatud saadaval**. Kannetel on see olek juhul, kui Finance on seadistatud nõudele, et tühistamised saadetakse enne sisestamist ülevaatusele. Pärast seda, kui ülevaataja sisestab või lükkab tagasi ümberpööramise või tühistamise, pole olek enam **Tühistamise ootel** ja te saate pangakonto pangaväljavõttega vastavusse viia.


Kui soovite pangaväljavõttel **kuvatavate** tšekkide intervalli puhul märkida ruudu Tühjendatud, **märkige ruut Märgi** tšekiintervall ja määrake intervall.

5.  Kui pangakonto kande summa ei vasta pangaväljavõtte kande summale, **sisestage paranduse summa väljale Parandussumma** .
    

> [!NOTE]
> Kui parandatava kande rahandusperiood on suletud, **ei saa** välja Parandussumma kasutada. Selle asemel looge paranduse jaoks rida, mis on avatud fiskaalperioodis. Sel juhul peate lisama finantsdimensioonid, mida kasutati esialgsel kandel ja samuti vastaskonto põhikonto.



6.  Looge kanded kirjetele (nagu tasud ja intress), mis on pangakonto väljavõttes, kuid mida pole talletatud rakenduses Finance. Sisestage **Pangakande tüüp** ja asjakohased finantsdimensioonid.

7.  Kuna kanded pangakonto väljavõttel on märgitud **Tühjendatud**, siis läheneb summa nullile väljal **Vastavusse viimata**, mida arvutatakse pidevalt uuesti vastavalt teie tehtud muudatustele. Kui see jõuab nullini, klõpsake **Vii konto vastavusse**, et sisestada vastavusseviimine ning kanded ja parandused, mille olete loonud.
    
    Pärast vastavusseviimise sisestamist ei saa kaasatud kandeid muuta ega parandada ning neid ei kuvata tulevase konto vastavusseviimiseks.

8.  Veel vastavusse viimata pangakannete vaatamiseks kasutage aruannet **Vastavusse viimata kanded**. Pangakonto pangaväljavõtte vaatamiseks kasutage aruannet **Pangaväljavõte**.

## <a name="cancel-bank-statement-reconciliation"></a>Tühista pangaväljavõtte vastavusseviimine 

Pangaväljavõtte **vastavusseviimise** tühistamise funktsioon võimaldab pangaväljavõtte vastavusseviimise tühistada. Selle funktsiooni kasutamiseks lubage funktsioon **Loobu pangaväljavõtte vastavusseviimisest** tööruumist **Funktsiooni haldamine**. Samuti peate lubama parameetri **Luba pangaväljavõtte redigeerimine**. Selleks minge jaotisse **Sularaha- ja pangahaldus > Häälestus > Sularaha- ja pangahalduse parameetrid > Panga vastavusseviimine**.
 
Pangaväljavõtte vastavusseviimise saab tühistada ainult selle sisestamise kronoloogilises järjestuses. Kui pangaväljavõtte vastavusseviimine tühistatakse, tühistatakse uued kanded ja parandused ning kõik muud kanded tähistatakse kui vastavusse viimata.
 
Pangaväljavõtte vastavusseviimise tühistamiseks valige pangaväljavõte ja valige **Pangaväljavõte > Tühista panga vastavusseviimine**. Lehel **Tühista panga vastavusseviimine** sisestage **Põhjusekood**, **Põhjuse kommentaar** ja **Tühistamise kuupäev**. Tühistamise alustamiseks valige **OK**. Pange tähele, et pangaväljavõtte tühistamise kuupäev peab olema pangaväljavõtte kuupäeval või pärast seda. Kui pangaväljavõtte vastavusseviimine on tühistatud, **uuendatakse pangaväljavõtte tühistamiskuupäeva väli tühistamiskuupäevaga**  **.**  Klõpsake nuppu **Kanded**, et vaadata kandeid, mille vastavusseviimine tühistati.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
