---
title: Kliendi poolimine arveldusgraafikutes
description: See artikkel kirjeldab, kuidas tükeldada klienti, kui kasutatakse kordustellimuse arveldust.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746330"
---
# <a name="customer-split-on-billing-schedules"></a>Kliendi poolimine arveldusgraafikutes

Arveldusgraafikus on maksja *klient*, kes saab müügitellimuse arve, et nad saaksid arve tasuda. Mõnes stsenaariumis saab arvet maksta mitu klienti. Kliendi **tükeldamise** funktsioon võimaldab teil lisada rohkem kliente, kellele saab arve esitada sama arveldusgraafiku alusel. Selle funktsiooni lubamiseks minge korduvtellimuse arvelduse korduva **\>\>\> lepingu arvelduse häälestuse** korduva lepingu arvelduse parameetritesse ja seadke kliendi **tükeldamise suvandi** väärtuseks **Jah.**

## <a name="customer-split-on-the-billing-schedule-header"></a>Kliendi tükeldamine arveldusgraafiku päises

Pärast arveldusgraafiku loomist saab lisakliendid lisada arveldusgraafiku päisesse.

Kliendi lisamiseks järgige neid samme.

1. Valige vahekaardil **Arveldusgraafik** suvand Kliendi **tükeldamine**. Ülaosas **olevad** kliendi **konto ja kliendi** konto nimeväljad määravad kliendi, kes on määratud arveldusgraafiku **kliendiks**.

    > [!NOTE]
    > Lisate kliendi konto ei saa olla sama mis arve konto.

2. Valige vahekaardil **Kliendi tükeldatud** read suvand **Lisa rida**.
3. Valige klient ja seejärel sisestage selle kliendi iga arve protsent.
4. Vaikimisi kasutatakse algus- ja lõppkuupäevi arveldusgraafikus algus- ja lõppkuupäevana. Sisestage erinevad algus- ja lõppkuupäevad, kui uus klient maksab määratud protsendi ainult osa arveldusgraafikust. Näiteks kui arveldusgraafiku alguskuupäev on 1. jaanuar ja lõppkuupäev 31. detsember ning uuele kliendile arveldatakse esimese üheksa kuu eest 40 protsenti, määrake alguskuupäevaks 1. jaanuar ja lõppkuupäevaks 30. september ning **sisestage protsendiks 40,00**.

Saate kliendi tükeldatud ridadele lisada mitu klienti. Sellisel juhul ei tohi sisestatud koguprotsent ületada 100 protsenti. Sisestage kliendiviide ja kliendi ostutellimus teabeväljadeks, mida näidatakse müügitellimuse real arve loomise **protsessi** käigus.

Rea üksikasjad näitavad lisatud klientide kontaktteavet, tarneaadressi, maksja aadressi ja makse üksikasju. Seda teavet näidatakse ka klientide müügitellimustel.

Kui lisate kliendi tükeldatud teabe arveldusgraafiku päisele, kui arveldusgraafikus on arveldamata arveldusgraafiku ridu, saate järgmise teate, mis palub teil muudatused tagasi võtta: "Kas soovite muudatuse päisest ridadele tagasi võtta? Muudatused uuendavad ainult arveldamata arveldusgraafiku ridu." Valige **Jah**, et värskendada kliendi tükeldamisteavet arveldusgraafiku real. Muudatusi ei värskendata, kui arveldusgraafiku rea eest on arve juba välja antud.

Kui arveldusgraafik luuakse kopeerimisgraafiku valikut **kasutades**, sisestatakse vaiketeave kliendi tükeldatud päiseridadele. See ei saa olla sama mis kliendi konto.

Kui arve **loomise** protsess on lõpetatud, luuakse mitu müügitellimust. (Automaatse sisestamise kasutamisel luuakse ka mitu müügiarvet.) Neid müügitellimusi ja müügiarveid saab vaadata arve **vahekaardil lehe** **Kuva** arvelduse üksikasjad kiirkaardil Rea üksikasjad.**·** **Mitu** on kuvatud arvelduse üksikasja real, näitamaks, et loodud on mitu müügitellimust ja müügiarvet.

## <a name="customer-split-on-billing-schedule-lines"></a>Kliendi poolitatud arveldusgraafiku ridades

Kliendi tükeldamise saab lisada üksikutele arveldusgraafiku ridadele, kui soovite tükeldada ainult kindlad arveldusgraafiku read. Märkige real **ruut Kliendi tükeldamine** **ja** seejärel valige arveldusgraafiku rea uuendamiseks või kliendi tükeldamise teabe sisestamiseks menüüks Kliendi tükeldamine.

Auditi teavet värskendatakse, kui arveldusgraafik on juba arveldatud, kuid siis protsenti muudeti arveldusgraafiku real. Kõik pärast seda muudatust arveldatud read kasutavad uut protsenti.

> [!NOTE]
> - Kliendi tükeldamissuvandi ei saa kasutada ladustatavate toodetega.
> - Kui on **märgitud ruut Jaotamata** tulu, ei **saa kliendi tükeldatud** märkeruutu valida.
> - Kui kasutate ainult **valikut Tulu tükeldamine**, on emareal **suvand Kliendi tükeldamine**, kuid tütarrea kaubad seda ei tee.
