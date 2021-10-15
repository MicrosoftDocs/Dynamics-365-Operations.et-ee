---
title: Kvaliteedijuhtimise testgrupid
description: See teema kirjeldab, kuidas luua testgruppe, nii et kvaliteettellimustega saab Microsoft Dynamics 365 Supply Chain Management kasutada mitut testi.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 230e402c322509f3ea89d4f1dccb5555828377ff
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578388"
---
# <a name="quality-management-test-groups"></a>Kvaliteedijuhtimise testgrupid

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua testgruppe, nii et kvaliteettellimustega saab Microsoft Dynamics 365 Supply Chain Management kasutada mitut testi.

Testgruppide ja neile määratud üksikute testide seadistamiseks, muutmiseks ja vaatamiseks kasutage lehte **Testgrupid**. Ülemine paan kuvab testgruppe ja alumine paan kuvab valitud testgruppi määratud katseid.

Määrate testgrupile mitmed põhimõtted, sealhulgas valimiplaan, vastuvõetav kvaliteeditase (AQL) ja nõuded hävitavale testimisele. Kui määrate testgrupile eraldi katse, määratlete lisateabe, näiteks sageduse, dokumendid ja kehtivuse kuupäevad. Kvantitatiivse katse puhul sisaldab teie määratletud teave ka vastuvõetavaid mõõtmisväärtusi. Kvalitatiivse katse puhul sisaldab teave katsemuutujat ja vaiketulemust.

Kvaliteettellimusele määratud katsegrupp määratleb katsete vaikekogumi, mis tuleb määratud kaubaga sooritada. Te saate kvaliteettellimuse katseid lisada, kustutada või muuta. Iga katse tulemused kinnitatakse kvaliteettellimuses.

Kui määratlete testgrupi, saate valikuliselt määrata kauba valimi. Kauba valimit kasutatakse testitava toote koguse määratlemiseks. Lisateavet vt [Kvaliteedijuhtimise kauba valim](quality-item-sampling.md). Võite ka näidata, kas testgrupi katsed on hävitavad. Hävitava testi korral on kauba valim rikutud ja kogus eemaldatakse vabast laoseisust.

## <a name="example-of-a-test-group"></a>Testgrupi näide

Tootmisettevõte määrab iga kvaliteetjuhise variandi puhul katsegrupi. Erinevad katsegrupid näitavad erinevusi valimiplaanides, katsehulkasid, mida peab koos läbi viima, vastuvõetavat kvaliteeditaset ja muid tegureid. Kvantitatiivsete katsete puhul on erinevused ka vastuvõetavates mõõteväärtustes. Kvaliteedijuhiste jõustamiseks määrab ettevõte igale reeglile testgrupi, mida kasutatakse kvaliteettellimuste automaatseks genereerimiseks **Kvaliteediseosed** lehel. Samuti määrab see testgrupi käsitsi loodud kvaliteettellimustele.

## <a name="create-a-test-group"></a>Katsegrupi loomine

Testgrupi loomiseks tehke järgmist.

1. Avage **Varud \> Seaded \> Kvaliteedijuhtimine \> Testgrupid**.
1. Ruudustiku rea lisamiseks lehe ülaossa valige tegevuspaanil suvand **Uus**. Seejärel määrake uuel real järgmised väljad.

    - **Testgrupp** – Sisestage testgrupi kordumatu ID või nimi.
    - **Kirjeldus** – Sisestage testgrupi detailne kirjeldus.
    - **Vastuvõetav kvaliteeditase** – Sisestage testitulemuste kogu protsent, mille peab läbima, et testide grupp lugeda läbituks.
    - **Kauba valim** – Valige kauba valim. Lisateavet vt [Kvaliteedijuhtimise kauba valim](quality-item-sampling.md).
    - **Hävitav** – Märkige see ruut näitamaks, et testgrupp hävitab testitavad kaubad.

1. Kui uus rida on endiselt valitud, valige lehekülje ülaosas vahekaart **Üldine**. Mõnda vahekaardil **Ülevaade** valitud testgrupi sätteid korratakse siin. Lisaks saate seada grupile järgmised väljad:

    - **Uuenda varude partii atribuuti** – Kui seadistate selle suvandi siin väärtusele *Jah*, seatakse see automaatselt olekusse *Jah* iga uue testi puhul, mis lisatakse testigrupile lehe alumises osas.
    - **Uuendage partii paigutust** – Kui seadistate selle suvandi valikule *Jah*, kui testitava kauba partiid kontrollitakse, uuendatakse partii paigutust automaatselt väärtusega, mis on valitud **Kvaliteettellimuse nurjunud partii paigutus** või **Testi läbinud kvaliteettellimuse partii paigutus** väljal.
    - **Nurjunud kvaliteettellimuse partii paigutus** – Valige partii paigutuskood, mis tuleks määrata, kui seda testgruppi kaasav kvaliteettellimus nurjub, sest see ei vasta AQL-ile.
    - **Testi läbinud kvaliteettellimuse partii paigutus** – Valige partii paigutuskood, mis tuleks määrata, kui seda testgruppi kaasav kvaliteettellimus läbib testi, sest see vastan AQL-ile.
    - **Uuenda varude olekut** – Kui seadistate selle suvandi olekule *Jah*, kui **Varude olek** on testitava üksuse salvestusmõõdurühmas testitaval kaubal lubatud, uuendatakse olekut automaatselt olekuga, mis on valitud väljal **Nurjunud kvaliteettellimuse olek** või **Testi läbinud kvaliteettellimuse olek**.
    - **Nurjunud kvaliteettellimuse olek** – Valige varude oleks, mis tuleks kaubale määrata, kui seda testgruppi kaasav kvaliteettellimus nurjub, sest see ei vasta AQL-ile.
    - **Testi läbinud kvaliteettellimuse olek** – Valige varude oleks, mis tuleks kaubale määrata, kui seda testgruppi kaasav kvaliteettellimus läbib testi, sest see vastab AQL-ile.

## <a name="add-a-qualitative-test-to-a-test-group"></a>Kvaliteeditesti lisamine testigrupile

Kvalitatiivse testi lisamiseks testgruppi toimige järgmiselt.

1. Avage **Varud \> Seaded \> Kvaliteedijuhtimine \> Testgrupid**.
1. Lehe ülemise osa vahekaardil **Ülevaade** valige testgrupp, millele soovite testi lisada.
1. Lehekülje alumises osas vahekaardil **Ülevaade** valige tööriistaribal suvand **Lisa**, et lisada rida ruudustikku. Seejärel määrake uuel real järgmised väljad.

    - **Järjekorranumber** – Sisestage täisarv, et määrata testide järjekord. Testid, millel on väiksemad järjekorranumbrid, viiakse läbi enne suuremate järjekorranumbritega teste.

        > [!NOTE]
        > Soovitatav on jätta järjekorranumbrite vahel vahe. Näiteks seadke esimese katse puhul **Järjekorranumber** välja väärtuseks *10* ja seejärel suurendage iga lisatesti puhul väärtust 10 võrra. Sel viisil saate hiljem lisada uusi teste, ilma et peaksite ridu kustutama ja uuesti looma, et need soovitud järjekorda panna.

    - **Test** – Valige test, mida soovite läbi viia. Kvalitatiivse testi jaoks valige test, kus välja **Tüüp** väärtuseks on määratud *Suvand*.
    - **Kehtiv** – Valige testi kehtivuse esimene kuupäev. Kui jätate selle välja tühjaks, pole piirangut.
    - **Aegumine** – Valige testi kehtivuse viimane kuupäev. Kui jätate selle välja tühjaks või määrate selle väärtuseks *Mitte kunagi*, siis piirang puudub.
    - **Testväärtuse määratlemine** – Valige, kuidas AQL tuleks määrata, kui sama testi jaoks registreeritakse mitu tulemust. Kvalitatiivse katse puhul saab valida ainult *Manuaalne*. Kui valite ühe muu väärtuse (*Keskmine*, *Miinimum* või *Maksimum*), saate testgrupi salvestamisel tõrketeate.
    - **Atribuut** – kui soovite salvestada testitulemused partii atribuudile, valige siin atribuut ja märkige ruut **Uuenda varude partii atribuuti**.
    - **Uuenda varude partii atribuuti** – Märkige see märkeruut väljal **Atribuut** valitud partii atribuudi testitulemuste salvestamiseks.

1. Lehe alumises osas valige vahekaart **Üldine**. Mõnda vahekaardil **Ülevaade** valitud testisätetest korratakse siin. Lisaks saate seada testile järgmised väljad:

    - **Analüüsitunnistuse aruanne** – Seadke see suvand valikule *Jah*, näitamaks, et testitulemused tuleks printida analüüsitunnistusele (CoA). Selle aruande saab luua kvaliteettellimusest.
    - **Toiming tõrke korral** – Valige suvand *Aktsepteeri* või *Nurju*, et näidata, kas testi peaks läbima või mitte, kui selle AQL ei ole täidetud.
    - **Vastuvõetav kvaliteeditase** – Sisestage testitulemuste kogu protsent, mille peab läbima, et test lugeda läbituks.

1. Seadke lehe alumises osas vahekaardil **Test** järgmised väljad:

    - **Muutuv** – Valige testmuutuja, mille jaoks kvalitatiivsed testitulemused registreeritakse.
    - **Vaiketulemus** – valige vaiketulemus, mis tuleks testitulemuste jaoks salvestada.
    - **Katsevahend** – valige testi jaoks kasutatav seade. Kui katsevahend on määratletud, sisestatakse see automaatselt testgrupi testi jaoks.

1. Sulgege leht.

## <a name="add-a-quantitative-test-to-a-test-group"></a>Lisage testrühmale kvantitatiivne test

Kvantitatiivse testi lisamiseks testgruppi toimige järgmiselt.

1. Avage **Varud \> Seaded \> Kvaliteedijuhtimine \> Testgrupid**.
1. Lehe ülemise osa vahekaardil **Ülevaade** valige testgrupp, millele soovite testi lisada.
1. Lehekülje alumises osas vahekaardil **Ülevaade** valige tööriistaribal suvand **Lisa**, et lisada rida ruudustikku. Seejärel määrake uuel real järgmised väljad.

    - **Järjekorranumber** – Sisestage täisarv, et määrata testide järjekord. Testid, millel on väiksemad järjekorranumbrid, viiakse läbi enne suuremate järjekorranumbritega teste.

        > [!NOTE]
        > Soovitatav on jätta järjekorranumbrite vahel vahe. Näiteks seadke esimese katse puhul **Järjekorranumber** välja väärtuseks *10* ja seejärel suurendage iga lisatesti puhul väärtust 10 võrra. Sel viisil saate hiljem lisada uusi teste, ilma et peaksite ridu kustutama ja uuesti looma, et need soovitud järjekorda panna.

    - **Test** – Valige test, mida soovite läbi viia. Kvantitatiivse testi jaoks valige test, kus välja **Tüüp** väärtuseks on määratud *Murd* või *Täisarv*.
    - **Kehtiv** – Valige testi kehtivuse esimene kuupäev. Kui jätate selle välja tühjaks, pole piirangut.
    - **Aegumine** – Valige testi kehtivuse viimane kuupäev. Kui jätate selle välja tühjaks või määrate selle väärtuseks *Mitte kunagi*, siis piirang puudub.
    - **Testväärtuse määratlemine** – Valige, kuidas AQL tuleks määrata, kui sama testi jaoks registreeritakse mitu tulemust. Saadaolevad valikud on *Keskmine*, *Miinimum*, *Maksimum* ja *Manuaalne*.
    - **Atribuut** – kui soovite salvestada testitulemused partii atribuudile, valige siin atribuut ja märkige ruut **Uuenda varude partii atribuuti**.
    - **Uuenda varude partii atribuuti** – Märkige see märkeruut väljal **Atribuut** valitud partii atribuudi testitulemuste salvestamiseks.

1. Lehe alumises osas valige vahekaart **Üldine**. Mõnda vahekaardil **Ülevaade** valitud testisätetest korratakse siin. Lisaks saate seada testile järgmised väljad:

    - **Analüüsitunnistuse aruanne** – Seadke see suvand valikule *Jah*, näitamaks, et testitulemused tuleks printida analüüsitunnistusele (CoA). Selle aruande saab luua kvaliteettellimusest.
    - **Toiming tõrke korral** – Valige suvand *Aktsepteeri* või *Nurju*, et näidata, kas testi peaks läbima või mitte, kui selle AQL ei ole täidetud.
    - **Vastuvõetav kvaliteeditase** – Sisestage testitulemuste kogu protsent, mille peab läbima, et test lugeda läbituks.

1. Seadke lehe alumises osas vahekaardil **Test** järgmised väljad:

    - **Standard** – Sisestage kogus (täisarv või murruline), mida testi tulemuselt eeldatakse. Teie sisestatud väärtus sisestatakse vaikimisi testitulemustesse. Lisaks sisestatakse see automaatselt vaikeväärtuseks väljadele **Min** ja **Max**.
    - **Min** – Sisestage testitulemuste minimaalne lubatud väärtus. Sisestatav väärtus peab olema väiksem kui väljal **Standard** määratud summa. Kui uuendate välja **Min**, uuendatakse automaatselt **Miinimumkõikumine (%)** väli. Kui uuendate välja **Miinimumkõikumine (%)**, uuendatakse automaatselt **Min** väli.
    - **Max** – Sisestage testitulemuste maksimaalne lubatud väärtus. Sisestatav väärtus peab olema suurem kui väljal **Standard** määratud summa. Kui uuendate välja **Max**, uuendatakse automaatselt **Maksimumkõikumine (%)** väli. Kui uuendate välja **Maksimumkõikumine (%)**, uuendatakse automaatselt **Max** väli.
    - **Katsevahend** – valige testi jaoks kasutatav seade. Kui katsevahend on määratletud, sisestatakse see automaatselt testgrupi testi jaoks.

1. Sulgege leht.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise testvahendid](quality-management-processes.md)
- [Kvaliteedijuhtimise testid](quality-management-processes.md)
- [Kvaliteedijuhtimise testi muutujad](quality-management-processes.md)
- [Kvaliteediseosed](quality-management-processes.md)
- [Partii atribuudid](/supply-chain/production-control/batch-attributes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
