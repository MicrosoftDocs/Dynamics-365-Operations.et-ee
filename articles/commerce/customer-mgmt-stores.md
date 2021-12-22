---
title: Kaupluste kliendihaldus
description: See teema kirjeldab, kuidas jaemüüjad saavad müügikohas (POS) lubada Microsoft Dynamics 365 Commerce kliendihaldust.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 29e45419f712e25092b473e34144ac1146e4ed9b
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913622"
---
# <a name="customer-management-in-stores"></a>Kaupluste kliendihaldus

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas jaemüüjad saavad müügikohas (POS) lubada Microsoft Dynamics 365 Commerce kliendihaldust.

On oluline, et kaupluse partnerid saavad müügikohas kliendi kirjeid luua ja redigeerida. Sel viisil saavad nad koguda mis tahes uuendusi klienditeabesse, nt meiliaadressi, telefoninumbrit ja aadressi. See teave on kasulik sellistes allavoolu süsteemides nagu turundus, kuna nende süsteemide efektiivsus sõltub nende kliendiandmete täpsusest.

Müügiseosed võivad käivitada kliendi loomise töövoo kahest kassa sisestuspunktist. Nad saavad valida nupu, mis on vastendatudotsingutulemuste lehel **kliendi lisamine** toiminguga, või nad saavad valida **Loo klient** rakendusribal otsingutulemeste lehel. Mõlemal juhul kuvatakse dialoogiboks **Uus klient** kus müügiesindajad saavad sisestada nõutavaid kliendi üksikasju, nt kliendi nime, meiliaadressi, telefoninumbri, aadressi ja mis tahes muud ettevõttele asjakohast teavet. Selle lisateabe saab koguda kliendi atribuutide abil, mis on kliendiga seostatud. Lisateavet kliendi atribuutide kohta vt kliendi [Kliendi atribuutidest](dev-itpro/customer-attributes.md).

Müügiesindajad saavad hõivata ka teiseseid meiliaadresse ja telefoninumbreid. Lisaks võivad nad hõivata kliendi eelistuse turundusteabe saamise kohta nende teiseste meiliaadresside või telefoninumbrite kaudu. Selle võimaluse lubamiseks peab jaemüüja lülitama sisse valiku **Salvesta mitu e-kirja ja telefoninumbrit** funktsiooni **funktsioonihalduse** Commerce headquarters`i tööruumis (**Süsteemide haldus \> tööruumides \> Funktsioonihaldus**).

## <a name="default-customer-properties"></a>Kliendi vaikimisi omadused

Jaemüüjad saavad kasutada **Kõik kauplused** rakenduse Commerce headquarters lehekülge (**Jaemüügi- ja Ärikanalite \> Kanalid \>Kauplused**), et seostada vaikekliendi iga kauplusega. Seejärel kopeerib Commerce vaikekliendi jaoks määratletud atribuudid kõigisse loodud kliendikirjetesse. Näiteks kuvatakse **Loo klient** dialoogiboksis atribuudid, mis on päritud kauplusega seotud vaikekliendilt. Need atribuudid on **kliendi tüüp**, **kliendigrupp**, **tarne-eelistus**, **vastuvõtja email**, **valuuta** ja **keel**. Kõik **kliendigrupid** (klientide grupeerimised) päritakse ka vaikekliendilt. Siiski, **finantsdimensioonid** on tuletatud vaikekliendiga seotud kliendigrupist, mitte vaikekliendist endast.

> [!NOTE]
> **Kviitungi e-kiri** väärtus kopeeritakse vaikekliendilt ainult juhul, kui kviitungi e-kirja ID-d pole vastloodud klientidele esitatud. See tähendab, et kui kviitungi e-posti ID on vaikekliendil olemas, saavad kõik e-kaubanduse saidilt loodud kliendid sama kviitungi e-posti ID, kuna kliendi kviitungi e-posti ID hõivamiseks puudub kasutajaliides. Soovitame teil hoida **kviitungi e-posti** välja kaupluse vaikekliendi jaoks tühjana ja kasutada seda ainult siis, kui teil on äriline protsess, mis sõltub kviitungi meiliaadressi olemasolust. 

Müügiesindajad saavad hõivata kliendi kohta mitu aadressi. Kliendi nimi ja telefoninumber on päritud iga aadressiga seotud kontaktteabest. Kliendikirje **Aadressid** kiirkaart sisaldab **Eesmärk** välja, mida müügiesindajad saavad redigeerida. Kui kliendi tüüp on **Isik**, on vaikeväärtus **Avaleht**. Kui kliendi tüüp on **Organisatsioon**, on vaikeväärtus **Äri**. Muud väärtused, mida see väli toetab, sisaldavad **Avaleht** **Äri** ja **Postkast**. Välja **Riik** väärtus pärineb esmasest aadressist, mis on määratud **Juhtseade** Commerce headquarters`i äriüksuse lehel **Organisatsiioni haldus \> Organisatsioonid \> Juhtseade**.



## <a name="additional-resources"></a>Lisaressursid

[Asünkroonne kliendi loomise režiim](async-customer-mode.md)

[Asünkroonsed kliendid teisendamine sünkroonsed kliendid](convert-async-to-sync.md)

[Kliendi atribuudid](dev-itpro/customer-attributes.md)

[Võrguühenduseta andmete välistamine](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
