---
title: Potentsiaalne klient sularahaks andmete migreerimine andmeintegraator topeltkirjutusse
description: See artikkel kirjeldab, kuidas potentsiaalset klienti andmeintegraatorist topeltkirjutusse üle siirdada.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 91cc0e59405bc085e09f01f05ef02e4a0260481e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111890"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Potentsiaalne klient sularahaks andmete migreerimine andmeintegraator topeltkirjutusse

[!include [banner](../../includes/banner.md)]

Andmeintegraator jaoks saadaoleva potentsiaalse kliendi kassalahendus ei ühildu topeltkirjutusega. Selle põhjuseks on msdynce_AccountNumber kontotabeli indeks, mis tuli lahenduse otsimiseks potentsiaalse kliendi osana. Kui see indeks on olemas, ei saa te luua sama kliendi kontonumbrit kahes erinevas juriidilises isikus. Võite valida uue topeltkirjutusega alguse, kui migreerite potentsiaalse kliendi andmeintegraatorist andmeintegraatorist topeltkirjutusse või saate installida potentsiaalse kliendi viimase domaniversiooni kassalahendusse. See artikkel käsitleb mõlemat lähenemist.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Installige andmeintegraatorpotentsiaali viimane doman-versioon kassalahendusse

**P2C versiooni 15.0.0.2** peetakse andmeintegraatori potentsiaalse kliendi viimaseks domaniversiooniks sularahalahenduse jaoks. Selle saate alla laadida asukohast [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Peate selle käsitsi installima. Pärast installimist jääb kõik täpselt samaks, v.a msdynce_AccountNumber indeks eemaldatakse.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Sammud potentsiaalse kliendi migreerimiseks andmeintegraatorist topeltkirjutusse

Teie potentsiaalne klient sularahaks andmete migreerimiseks andmeintegraatorist topeltkirjutusse tehke järgmist.

1. Käivitage potentsiaalne klient sularahaks andmeintegraatori tööd, et teha üks lõplik täielik sünkroonimine. Sel viisil tagate, et mõlemas süsteemis (finantside ja toimingute rakendused ning kliendi kaasamise rakendused) on kõik andmed.
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
5. Looge topeltkirjutusega ühendus ühe või mitme juriidilise isiku finantside ja operatsioonide rakenduse ja kliendi kaasamise rakenduse vahel.
6. Lubage topeltkirjutustabeli kaardid ja käivitage nõutud viiteandmete esialgne sünkroonimine. (Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).) Nõutavate andmete näidete hulka kuuluvad kliendigrupid, maksetingimused ja maksegraafikud. Ärge lubage topeltkirjutuse kaarte tabelitele, mis nõuavad lähtestamist, nt konto, pakkumise, pakkumise rea, tellimuse ja tellimuse rea tabelid.
7. Avage kliendi kaasamise rakenduses **Täpsemad sätted \> Süsteemi sätted \> Andmehaldus \> Duplikaadi tuvastamise reeglid** ja keelake kõik reeglid.
8. Lähtestage 2. etapis loetletud tabelid. Juhiseid vt selle artikli ülejäänud jaotistest.
9. Avage finantside ja toimingute rakendus ning lubage tabelikaardid, nt konto, pakkumise, pakkumise rea, tellimuse ja tellimuserea tabeli vastekaardid. Seejärel käivitage algne sünkroonimine. (Lisateavet vt teemast [Esmase sünkroonimise kaalutlused](initial-sync-guidance.md).) See protsess sünkroonib lisateabe finantside ja toimingute rakendusest, nagu töötlemise olek, saatmise ja arveaadressid, saidid ja laod.

## <a name="account-table"></a>Konto tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Veerus **Suhte tüüp** sisestage staatilise väärtusena **klient**. Te ei pruugi soovida iga kontokirjet oma äriloogikas kliendina klassifitseerida.
3. Veerus Kliendigrupi **ID** sisestage kliendigrupi number finantside ja toimingute rakendusest. Potentsiaalse kliendi sularahaks lahenduse vaikeväärtus on **10**.
4. Kui kasutate valikut potentsiaalne klient sularahaks ilma **kontonumbrit** kohandamata, sisestage **kontonumbri** väärtus veergu **Osapoole number**. Kui kohandused on olemas ja te ei tea osapoole numbrit, tõmbage see teave finantside ja toimingute rakendusest.

## <a name="contact-table"></a>Kontakti tabel

1. Sisestage veergu **Ettevõte** ettevõtte nimi, nt **USMF**.
2. Määrake järgmised veerud, mis põhinevad CSV-faili **IsActiveCustomer** väärtusel.

    - Kui **IsActiveCustomer** on määratud CSV-failis väärtusele **Jah**, määrake veeru **Müüdav** väärtuseks **Jah**. Veerus Kliendigrupi **ID** sisestage kliendigrupi number finantside ja toimingute rakendusest. Potentsiaalse kliendi sularahaks lahenduse vaikeväärtus on **10**.
    - Kui **IsActiveCustomer** on CSV-failis seatud väärtusele **Ei**, määrake veeru **Müüdav** väärtuseks **Ei** ja määrake veeru **Kontakt** väärtuseks **Klient**.

3. Kui kasutate lahendust potentsiaalne klient sularahaks ilma **kontaktinumbrit** kohandamata, määrake järgmised veerud.

    - Migreerige kontakti number CSV-failist (**msdynce\_contactnumber**) kontaktinumbrisse tabelis **Kontakt** (**msd\_contactnumber**).
    - Kasutage tabeli **Kontakti number** väärtusi veerus **Osapoole number**.
    - Kasutage tabeli **Kontakti number** väärtusi veerus **Kontonumber / kontaktisiku ID**.

## <a name="invoice-table"></a>Arve tabel

Kuna arve tabeli andmed **on** mõeldud ühe viisi voogu voogu, alates finantside ja toimingute rakendusest kuni kliendi kaasamise rakenduseni, pole lähtestamine vajalik. Käivitage esialgne sünkroonimine, et migreerida kõik nõutavad andmed finantside ja toimingute rakendusest kliendikogemuse rakendusse. Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).

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

Kuna andmed tabelist **Tooted** on mõeldud ühe viisi voogu, alates finantside ja toimingute rakendusest kuni kliendikogemuse rakenduseni, pole lähtestamine vajalik. Käivitage esialgne sünkroonimine, et migreerida kõik nõutavad andmed finantside ja toimingute rakendusest kliendikogemuse rakendusse. Lisateavet vt teemast [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Hinnapakkumise ja hinnapakkumise toodete tabel

Tabeli Pakkumine **puhul** järgige selle artikli varasemas [jaotises Tellimuse](#order-table) tabel toodud juhiseid. Tabeli **Hinnapakkumise toode** puhul järgige juhiseid jaotises [Tellimuse toodete tabel](#order-products-table).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

