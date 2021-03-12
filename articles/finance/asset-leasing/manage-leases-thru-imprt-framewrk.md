---
title: Rendilepingute haldamine rendilepingu importimise raamistiku kaudu
description: Selles teemas selgitatakse, kuidas kasutada rendilepingu importimise raamistikku, et korrigeerida mitut rendilepingut samaaegselt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
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
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d7a7d2afd8f352bc167ec8c0a354ee4ac0a9e77b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442570"
---
# <a name="manage-leases-through-the-lease-import-framework"></a>Rendilepingute haldamine rendilepingu importimise raamistiku kaudu

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas kasutada rendilepingu importimise raamistikku, et korrigeerida mitut rendilepingut ühe etapina. Seda võimalust kasutades saate säästa aega ja samuti saate tagada täpsemaid korrigeerimisi, vähendades inimliku vea tõenäosust. Lisaks saab see võimalus ühendada Microsoft Dynamics 365 Finance'i väliste andmete üksustega, et andmeid tõhusalt üles laadida.

Vara rentimise integreerimiseks väliste süsteemidega saab kasutada järgmisi andmeüksusi.

- Rendi ajastamine
- Makselepingu ajastamine
- Täitelepingu ajastamine

Saate kasutada impordi protsessi, et korrigeerida rendilepingut, värskendada mitte-finantsteavet või lisada uusi rendilepinguid. Enne importimist saate rendilepingu andmeid vaadata ja redigeerida.

Süsteem võib rendilepingu importimise komplekti kaudu käivitada järgmised kolm protsessi.

| Protsessi tüüp  | Kirjeldus |
|---------------|-------------|
| Lisa kirje    | Selle protsessi tüübiga migreeritud rendilepingud loovad süsteemis rendilepingu. Maksegraafik tuleb käsitsi kinnitada ja algse tuvastuse töölehe kirje tuleb pärast migreerimist käsitsi sisestada. |
| Uuenda kirje | Selle protsessitüübiga migreeritud rendilepingud uuendavad süsteemis juba olemas oleva rendilepingu väärtuseid. Uuendatakse ainult väljad, mis on valitud lehel **Uuenda väljade valikut**. Soovitatav on valida mitte-finantsilised väljad lehel **Uuenda väljade valikut**, kuna see protsessi tüüp ei korrigeeri üürilepingut. |
| Kirje korrigeerimine | Selle protsessitüübiga migreeritud rendilepingud korrigeerivad rendilepingut. See korrigeerimine põhjustab rendilepingu kapitalirendi muutumise. Pärast rendilepingu töötlemist loob süsteem uue maksegraafiku, kasutades uusi andmeid rendilepingu importimise komplektist. Süsteem ei kinnita maksegraafikut ega sisesta korrigeerimise töölehe kirjet. |

Kui andmed on tööruumi **Andmehaldus** kaudu üles laaditud, avage leht **Impordi päis** (**Vara rentimine \> Rendilepingu importimise raamistik \> Impordi päis**). Sellel lehel loetletakse kõik varem loetletud kolme andmeüksuse impordid.

Rendilepingu ajastamise andmete vaatamiseks enne töötluse käitamist valige **Ajastamise andmed**.

Võrdlemise funktsioon võimaldab teil võrrelda kirjet, mida impordite vastava kirjega, mis on juba teie süsteemis olemas. Üksiku rendilepingu kirje võrdlemiseks valige rendileping ja seejärel valige **Võrdle**. See etapp tuleks **Erinevuste** aruande loomiseks lõpule viia enne rendilepingu kirjete migreerimist. Võrdlemise funktsioon võrdle ajastamise andmete väärtusi praegu süsteemis olevate rendilepingute väärtustega.

> [!NOTE]
> Võrdlemise funktsioon ei toimi rendilepingute korral, millel on protsessitüübiks **Lisa kirje**, sest seda rendilepingut pole millegagi võrrelda.
>
> Mitme rendilepingu üheaegseks võrdlemiseks minge jaotisse **Vara rentimine \> Rendilepingu importi raamistik \> Perioodiline \> Võrdlemine** ja valige **Võrdle**.

Iga üksuse puhul saate vaadata praegu süsteemis olemasoleva ja ajastamise tabelites oleva erinevusi. Iga ajastamise tabelites oleva üksuse kohta valige **Vaata erinevusi**. Kuvatavas dialoogiaknas on näha praegune väärtus ja pakutav ajastamise väärtus.

Saate ajastamise väärtust uuendada nii, et vahetate selle veerus **Uus väärtus** ja valite käsu **Uuenda ajastamine**.

Saate rendilepinguid valideerida, veendumaks, et kirjed saab ilma vigu tekitamata süsteemi tuua. Enne rendilepingu kirje migreerimist käitab süsteem mitu valideerimist, et tagada kirje edukas importimine. Üksiku rendilepingu valideerimiseks valige käsk **Valideeri**.

> [!NOTE]
> Mitme rendilepingu üheaegseks valideerimiseks minge jaotisse **Vara rentimine \> Rendilepingu importi raamistik \> Perioodiline \> Valideerimine** ja valige **Võrdle**.

Üksiku rendilepingu töötlemiseks valige käsk **Migreeri rendilepingu kirjed** lehel **Impordi päis**. Kui rendileping on migreeritud, teostab süsteem toimingu, mis on määratletud väljal **Protsessi tüüp**.

> [!NOTE]
> Mitme rendilepingu üheaegseks valideerimiseks minge jaotisse **Vara rentimine \> Rendilepingu importi raamistik \> Perioodiline \> Valideerimine** ja valige **Võrdle**.

Pärast rendilepingute võrdlemist saate käitada aruannet, et vaadata iga impordi ID-s sisalduva rendilepingu erinevusi. Ühe rendilepingu kohta aruande loomiseks valige see rendileping ajastamise andmetest ja seejärel avage jaotis **Võrdle ja kuva aruanne \> Erinevuste aruanne**.

> [!NOTE]
> Mitme rendilepingu üheaegseks valideerimiseks minge jaotisse **Vara rentimine \> Päringud ja aruanded \> Erinevuste aruanne** ja valige **Võrdle**.

## <a name="set-up-update-fields"></a>Uuendusväljade seadistamine

Kui kasutate rendilepingute uuendamiseks rendilepingute importimise raamistikku ja protsessi tüübiks on **Uuenda kirje**, saate valida uuendamiseks kindlad väljad.

1. Avage **Vara rentimine \> Rendilepingu importimise raamistik \> Seadistus \> Uuendatava välja valik**.
2. Valige kuvataval leheküljel väljad, mida uuendada, ja seejärel valige roheline nool, et teisaldada need loendisse **Valitud väljad**. Ainult loendis **Valitud väljad** olevaid välju saab rendilepingu importimise komplektiga uuendada.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]