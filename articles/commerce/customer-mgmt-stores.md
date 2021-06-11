---
title: Kaupluste kliendihaldus
description: See teema kirjeldab, kuidas jaemüüjad saavad müügikohas (POS) lubada Microsoft Dynamics 365 Commerce kliendihaldust.
author: josaw1
ms.date: 05/25/2021
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
ms.openlocfilehash: dd17593d84a8bf262712a84b11829f8ec6c49049
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097204"
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

## <a name="sync-customers-and-async-customers"></a>Klientide ja asünkroonsete klientide sünkroonimine

Äris on kliendi loomiseks kaks režiimi: sünkroonne (või Sync) ja asünkroonne (või Async). Vaikimisi luuakse kliendid sünkroonselt. See tähendab, et need luuakse Commerce Headquarters`is reaalajas. Kliendi loomise režiim Sync on kohe tellitav, kuna uued kliendid on kanalites kohe otsitavad. Ent sellel on ka puudusi. Kuna see loob [Commerce Data Exchange: Real-time Service'i](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) kutsed Commerce Headquarters`isse, võib see mõjutada jõudlust, kui tehakse mitu samaaegset kliendi loomise kutset.

Kui **Loo klient asünkroonses režiimis** suvand on häälestatud **jah** funktsiooniprofiilis (**jaemüügi ja ärikanali \> kanali häälestus \> võrgupoe häälestuse \> funktsiooniprofiilid**), reaalajas teenuse kõnesid ei kasutata kliendikirjete loomiseks kanali andmebaasis. Asünkroonnis kliendi loomise režiim ei mõjuta Commerce Headquarters`i jõudlust. Ajutine globaalselt kordumatu identifikaator (GUID) määratakse igale uuele Async Customeri kirjele ja seda kasutatakse kliendi konto ID-na. Seda GUID-i ei kuvata kassa kasutajatele. Selle asemel näevad need kasutajad **Ootel sünkroonimist** kliendikonto ID-na. Kuigi see konfiguratsioon sunnib kliente asünkroonselt tekitama, pidage meeles, et kliendikirjete muudatusi tehakse alati sünkroonselt.

### <a name="convert-async-customers-to-sync-customers"></a>Klientide ja asünkroonsete klientide sünkroonimine

Async Klientide teisendamiseks teenusesse Sync tuleb teil kõigepealt käitada P-töö, et saata Asynci kliendid Commerce Headquarters`i. Seejärel käivitage **Async Mode tööst klientide ja äripartnerite sünkroonimine** kliendi konto ID-de loomiseks. Lõpuks käivitage **1010** töö, et sünkroonida uue kliendi konto ID-d kanalitega.

### <a name="async-customer-limitations"></a>Asünkroonse kliendi piirangud

Asünkroonse kliendi funktsioonil on praegu järgmised piirangud:

- Asünkroonse kliendi kirjeid ei saa redigeerida, kui klient ei ole loodud Commerce Headquarters`is ja uus kliendi konto ID on kanalisse tagasi sünkroonitud.
- Asünkroonsete klientidega ei saa seostada kuuluvusi. Seetõttu ei päri uued asünkroonsed kliendid vaikekliendilt kuuluvusi.
- Kliendikaarte ei saa asünkroonsetele klientidele väljastada enne, kui uus kliendi konto ID on kanalisse sünkroonitud.
- Asünkroonsete klientide teiseseid meiliaadresse ja telefoninumbreid ei saa hõivata.

### <a name="customer-creation-in-pos-offline-mode"></a>Kliendi loomine ühenduseta režiimis

Kui kassa ei tööta, kui asünkroonse kliendi loomisrežiim on lubatud, luuakse uued kliendikirjed asünkroonselt. Kui kassa ei tööta, kui asünkroonse kliendi loomisrežiim on keelatud, lülitub süsteem automaatselt Asynci kliendi loomisrežiimile. Teisisõnnu, kui kassa ei tööta, luuakse uued kliendikirjed asünkroonselt, isegi kui asünkroonse kliendi loomisrežiim on keelatud. Seetõttu peavad Commerce Headquarters`i administraatorid looma ja planeerima P-töö jaoks **Sünkroniseerige kliendid ja äripartnerid asünkroonsest reziimist** töö ja **1010** korduva töö nii, et kõik asünkroonsed kliendid teisendatakse sünkroonimise klientideks Commerce headquarters`is.

> [!NOTE]
> Kui suvand **Kliendi ühisandmete tabelite filtreerimise** on seatud **jah** väärtusele **Commerce Channeli skeemi** lehel (**Jaemüük ja ärikanal \> Headquarters`i häälestus \> Jaemüügi häälestus \> Kanali andmebaasigrupp**), ei looda kliendikirjeid kassa võrguühenduseta režiimis. Lisateavet leiate artiklist [Andmeüksused](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Lisaressursid

[Kliendi atribuudid](dev-itpro/customer-attributes.md)

[Võrguühenduseta andmete välistamine](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
