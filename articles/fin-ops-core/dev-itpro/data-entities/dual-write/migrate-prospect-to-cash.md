---
title: Potentsiaalne klient sularahaks andmete migreerimine andmeintegraator topeltkirjutusse
description: See teema kirjeldab, kuidas migreerida potentsiaalne kliendi sularahaks andmeid andmeintegraator topeltkirjutusse.
author: RamaKrishnamoorthy
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: 46f869265e589ad8e0c94a839df70e54fe781c5a4e7f992e6534e883b21801ae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733119"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Potentsiaalne klient sularahaks andmete migreerimine andmeintegraator topeltkirjutusse

[!include [banner](../../includes/banner.md)]

Teie potentsiaalne klient sularahaks andmete migreerimiseks andmeintegraatorist topeltkirjutusse tehke järgmist.

1. Käivitage potentsiaalne klient sularahaks andmeintegraatori tööd, et teha üks lõplik täielik sünkroonimine. Sel viisil tagate, et mõlemas süsteemis (Finance and Operationsi rakendustes ja kliendi kaasamise rakendustes) on kõik andmed.
2. Potentsiaalse andmekao vältimiseks eksportige potentsiaalne klient sularahaks andmed rakendusest Microsoft Dynamics 365 Sales Exceli faili või komaga eraldatud väärtustega (CSV) faili. Eksportige andmed järgmistest üksustest.

    - [Konto](#account-table)
    - [Kontakt](#contact-table)
    - [Arve](#invoice-table)
    - Arve tooted
    - [Tellimus](#order-table)
    - [Toodete tellimine](#order-products-table)
    - [Tooted](#products-table)
    - [Pakkumine](#quote-and-quote-product-tables)
    - [Hinnapakkumise tooted](#quote-and-quote-product-tables)

3. Potentsiaalse kliendi sularahaks lahenduse desinstallimine rakenduse Sales keskkonnast. See etapp eemaldab veerud ja vastavad andmed, mille potentsiaalne klient sularahaks lahenduse jaoks juurutas.
4. Installige topeltkirjutuse lahendus.
5. Looge topeltkirjutusega seos rakenduse Finance and Operations ja kliendi kaasamise rakenduse vahel ühe või mitme juriidilise isiku jaoks.
6. Lubage topeltkirjutustabeli kaardid ja käivitage nõutud viiteandmete esialgne sünkroonimine. (Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).) Nõutavate andmete näidete hulka kuuluvad kliendigrupid, maksetingimused ja maksegraafikud. Ärge lubage topeltkirjutuse kaarte tabelitele, mis nõuavad lähtestamist, nt konto, pakkumise, pakkumise rea, tellimuse ja tellimuse rea tabelid.
7. Avage kliendi kaasamise rakenduses **Täpsemad sätted \> Süsteemi sätted \> Andmehaldus \> Duplikaadi tuvastamise reeglid** ja keelake kõik reeglid.
8. Lähtestage 2. etapis loetletud tabelid. Juhiseid vaadake selle teema ülejäänud jaotistest.
9. Avage rakendus Finance and Operations ja lubage tabelikaardid, nt konto, hinnapakkumise, pakkumise rea, tellimuse ja tellimuse rea tabeli kaardid. Seejärel käivitage algne sünkroonimine. (Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md)sünkroonimist.) See protsess sünkroonib rakendusest Finance and Operations lisateavet, nagu töötlemise olek, saatmine ja arveldusaadressid, saidid ja laod.

## <a name="account-table"></a>Konto tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Veerus **Suhte tüüp** sisestage staatilise väärtusena **klient**. Te ei pruugi soovida iga kontokirjet oma äriloogikas kliendina klassifitseerida.
3. Sisestage veergu **Kliendigrupi ID** rakenduse Finance and Operations kliendigrupi number. Potentsiaalse kliendi sularahaks lahenduse vaikeväärtus on **10**.
4. Kui kasutate valikut potentsiaalne klient sularahaks ilma **kontonumbrit** kohandamata, sisestage **kontonumbri** väärtus veergu **Osapoole number**. Kui on kohandusi ja te ei tea osapoole numbrit, tõmmake see teave rakendusest Finance and Operations.

## <a name="contact-table"></a>Kontakti tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Määrake järgmised veerud, mis põhinevad CSV-faili **IsActiveCustomer** väärtusel.

    - Kui **IsActiveCustomer** on määratud CSV-failis väärtusele **Jah**, määrake veeru **Müüdav** väärtuseks **Jah**. Sisestage veergu **Kliendigrupi ID** rakenduse Finance and Operations kliendigrupi number. Potentsiaalse kliendi sularahaks lahenduse vaikeväärtus on **10**.
    - Kui **IsActiveCustomer** on CSV-failis seatud väärtusele **Ei**, määrake veeru **Müüdav** väärtuseks **Ei** ja määrake veeru **Kontakt** väärtuseks **Klient**.

3. Kui kasutate lahendust potentsiaalne klient sularahaks ilma **kontaktinumbrit** kohandamata, määrake järgmised veerud.

    - Migreerige kontakti number CSV-failist (**msdynce\_contactnumber**) kontaktinumbrisse tabelis **Kontakt** (**msd\_contactnumber**).
    - Kasutage tabeli **Kontakti number** väärtusi veerus **Osapoole number**.
    - Kasutage tabeli **Kontakti number** väärtusi veerus **Kontonumber / kontaktisiku ID**.

## <a name="invoice-table"></a>Arve tabel

Kuna tabeli **Arve** andmed on mõeldud liikuma ühes suunas, rakenduses Finance and Operations klientide kaasamise rakendusse, pole lähtestamine vajalik. Käivitage esialgne sünkroonimine, et migreerida kõik nõutavad andmed rakendusest Finance and Operations klientide kaasamise rakendusse. Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).

## <a name="order-table"></a>Tellimuse tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Kopeerige veeru **Tellimuse ID** väärtus CSV-failis veergu **Müügitellimuse number**.
3. Kopeerige veeru **Kliendi** väärtus CSV-failis veergu **Arve kliendinumber**.
4. Kopeerige veeru **Tarni riiki/piirkonda** väärtus CSV-faili veergu **Tarni riiki/piirkonda**. Selle väärtuse näidete hulka kuuluvad **USA** ja **Ameerika Ühendriigid**.
5. Seadistage veerg **Nõutav sissetulekukuupäev**. Kui te ei kasuta vastuvõtukuupäeva, kasutage CSV-failis veerge **Taotletud tarnekuupäev**, **Täidetud kuupäev** ja **Esitamise kuupäev**. Selle väärtuse näide on **2020-03-27T00:00:00Z**.
6. Määrake veerg **Keel**. Selle väärtuse näide on **en-us**.
7. Määrake veerg **Tellimuse tüüp**, kasutades veergu **Kaubapõhine**.

## <a name="order-products-table"></a>Toodete tellimise tabel

- Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.

## <a name="products-table"></a>Toodete tabel

Kuna tabeli **Tooted** andmed on mõeldud liikuma ühes suunas, rakenduses Finance and Operations klientide kaasamise rakendusse, pole lähtestamine vajalik. Käivitage esialgne sünkroonimine, et migreerida kõik nõutavad andmed rakendusest Finance and Operations klientide kaasamise rakendusse. Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Hinnapakkumise ja hinnapakkumise toodete tabel

Tabeli **Hinnapakkumine** puhul järgige juhiseid selle teema varasemas jaotises [Tellimuse tabel](#order-table). Tabeli **Hinnapakkumise toode** puhul järgige juhiseid jaotises [Tellimuse toodete tabel](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]