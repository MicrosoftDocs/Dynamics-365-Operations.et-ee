---
title: Potentsiaalne klient sularahaks andmete migreerimine andmeintegraator topeltkirjutusse
description: See teema kirjeldab, kuidas migreerida potentsiaalne kliendi sularahaks andmeid andmeintegraator topeltkirjutusse.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 82bfb768b0ecac04184f4b806527346d39584d64
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087264"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Potentsiaalne klient sularahaks andmete migreerimine andmeintegraator topeltkirjutusse

[!include [banner](../../includes/banner.md)]

Data Integratori jaoks saadaval olev potentsiaal sularahalahendusele ei ühildu topeltkirjutusega. Selle põhjuseks on kontotabeli msdynce_AccountNumber indeks, mis tuli osana lahendusest Väljavaade sularahale. Kui see indeks on olemas, ei saa te luua sama kliendikonto numbrit kahes erinevas juriidilises üksuses. Võite alustada värskelt topeltkirjutamisega, migreerides prospecti andmete sularahaandmetele data integraatorist topeltkirjutamisele või installida prospecti viimase "seisva" versiooni sularahalahendusele. See teema hõlmab mõlemat lähenemist.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Installige andmeintegraatori prospekti viimane "uinuv" versioon sularahalahendusele

**P2C versiooni 15.0.0.2** peetakse andmeintegraatori Prospecti viimaseks "seisvaks" versiooniks sularahalahendusele. Saate selle alla laadida [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Peate selle käsitsi installima. Pärast paigaldamist jääb kõik täpselt samaks, välja arvatud msdynce_AccountNumber indeks eemaldatakse.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Juhised Prospecti migreerimiseks andmete rahaks andmeintegraatorilt topeltkirjutajale

Teie potentsiaalne klient sularahaks andmete migreerimiseks andmeintegraatorist topeltkirjutusse tehke järgmist.

1. Käivitage potentsiaalne klient sularahaks andmeintegraatori tööd, et teha üks lõplik täielik sünkroonimine. Sel viisil tagate, et nii süsteemidel (Finance and Operationsi rakendused kui ka klientide kaasamise rakendused) on kõik andmed.
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
5. Looge rakenduse Finance and Operations ja kliendi kaasamise rakenduse vahel ühe või mitme juriidilise inimese jaoks topeltkirjutusühendus.
6. Lubage topeltkirjutustabeli kaardid ja käivitage nõutud viiteandmete esialgne sünkroonimine. (Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).) Nõutavate andmete näidete hulka kuuluvad kliendigrupid, maksetingimused ja maksegraafikud. Ärge lubage topeltkirjutuse kaarte tabelitele, mis nõuavad lähtestamist, nt konto, pakkumise, pakkumise rea, tellimuse ja tellimuse rea tabelid.
7. Avage kliendi kaasamise rakenduses **Täpsemad sätted \> Süsteemi sätted \> Andmehaldus \> Duplikaadi tuvastamise reeglid** ja keelake kõik reeglid.
8. Lähtestage 2. etapis loetletud tabelid. Juhiseid vaadake selle teema ülejäänud jaotistest.
9. Avage rakendus Rahandus ja Toimingud ning lubage tabelikaardid (nt konto, pakkumine, hinnapakkumise rida, tellimus ja tellimuse rea tabelikaardid). Seejärel käivitage algne sünkroonimine. (Lisateavet vt teemast [Esialgse sünkroonimise](initial-sync-guidance.md) kaalutlused.) See protsess sünkroonib rakenduse Finance and Operations lisateavet, näiteks töötlemise olekut, lähetus- ja arveldusaadresse, saite ja ladusid.

## <a name="account-table"></a>Konto tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Veerus **Suhte tüüp** sisestage staatilise väärtusena **klient**. Te ei pruugi soovida iga kontokirjet oma äriloogikas kliendina klassifitseerida.
3. Sisestage veerus **Kliendirühma ID** kliendirühma number rakendusest Finance and Operations. Potentsiaalse kliendi sularahaks lahenduse vaikeväärtus on **10**.
4. Kui kasutate valikut potentsiaalne klient sularahaks ilma **kontonumbrit** kohandamata, sisestage **kontonumbri** väärtus veergu **Osapoole number**. Kui kohandusi on ja te ei tea osapoole numbrit, tõmmake see teave rakendusest Finance and Operations.

## <a name="contact-table"></a>Kontakti tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Määrake järgmised veerud, mis põhinevad CSV-faili **IsActiveCustomer** väärtusel.

    - Kui **IsActiveCustomer** on määratud CSV-failis väärtusele **Jah**, määrake veeru **Müüdav** väärtuseks **Jah**. Sisestage veerus **Kliendirühma ID** kliendirühma number rakendusest Finance and Operations. Potentsiaalse kliendi sularahaks lahenduse vaikeväärtus on **10**.
    - Kui **IsActiveCustomer** on CSV-failis seatud väärtusele **Ei**, määrake veeru **Müüdav** väärtuseks **Ei** ja määrake veeru **Kontakt** väärtuseks **Klient**.

3. Kui kasutate lahendust potentsiaalne klient sularahaks ilma **kontaktinumbrit** kohandamata, määrake järgmised veerud.

    - Migreerige kontakti number CSV-failist (**msdynce\_contactnumber**) kontaktinumbrisse tabelis **Kontakt** (**msd\_contactnumber**).
    - Kasutage tabeli **Kontakti number** väärtusi veerus **Osapoole number**.
    - Kasutage tabeli **Kontakti number** väärtusi veerus **Kontonumber / kontaktisiku ID**.

## <a name="invoice-table"></a>Arve tabel

Kuna tabeli Arve **andmed** on loodud voolama ühel viisil, rakendusest Finance and Operations kuni kliendi kaasamise rakenduseni, pole lähtestamine vajalik. Käivitage algne sünkroonimine, et migreerida kõik vajalikud andmed rakendusest Finance and Operations kliendi kaasamise rakendusse. Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).

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

Kuna tabeli Tooted **andmed** on loodud liikuma ühel viisil, rakendusest Finance and Operations kuni kliendi kaasamise rakenduseni, pole lähtestamine vajalik. Käivitage algne sünkroonimine, et migreerida kõik vajalikud andmed rakendusest Finance and Operations kliendi kaasamise rakendusse. Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Hinnapakkumise ja hinnapakkumise toodete tabel

Tabeli **Hinnapakkumine** puhul järgige juhiseid selle teema varasemas jaotises [Tellimuse tabel](#order-table). Tabeli **Hinnapakkumise toode** puhul järgige juhiseid jaotises [Tellimuse toodete tabel](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
