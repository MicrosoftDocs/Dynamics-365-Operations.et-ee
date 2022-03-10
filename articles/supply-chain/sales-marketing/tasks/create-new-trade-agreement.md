---
title: Uue kaubandusleppe loomine
description: See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a16a39d95605900be0fa1e339b8cd0755ba85189
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573413"
---
# <a name="create-a-new-trade-agreement"></a>Uue kaubandusleppe loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Kui kasutate oma andmeid, peate enne selle juhendi käivitamist veenduma, et oleks olemas kaubandusleppe tööleht, kus suvandi Vaikeseos sätteks on valitud „Hind (müük)”.

## <a name="create-and-post-a-new-trade-agreement-journal"></a>Uue kaubandusleppe töölehe loomine ja sisestamine

1. Avage **Navigatsioonipaan > Moodulid > Müük ja turundus > Hinnad ja allahindlused > Kaubandusleppe töölehed**.
2. Klõpsake valikut **Uus**.
3. Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake paanil **Toimingupaan** suvandit **Read**.
6. Valige väljal **Konto kood** suvand "Tabel".
    
    Selles näites värskendate hinda teatud kliendi puhul, mis tähendab, et peate valima suvandi Tabel. Kui värskendasite toote hinnakirja, siis valige suvand "Kõik", et uus hind kehtiks kõikide klientide jaoks. Kui määrasite erinevatele kliendisektoritele erinevad hinnad, siis valige suvand Grupp. Suvandi Grupp valimiseks peate seadistama kliendi hinnagrupid.  

7. Klõpsake väljal **Konto valik** otsingu avamiseks ripploendi nuppu.
8. Otsige loendist ja valige soovitud kirje.
9. Valige väljal **Kaubakood** suvand "Tabel".
    
    Kui sisestate kaubandusleppe, mille tüüp on Hind (müük), peate valima väljal **Kaubakood** ainult suvandi "Tabel". Põhjuseks on see, et hind on absoluutväärtus ning ei saa olla kõigi toodete või tootegrupi puhul olla sama.
    
10. Klõpsake väljal **Kauba seos** otsingu avamiseks ripploendi nuppu.
11. Valige loendist toode, mille soovite leppesse kaasata. Märkige üles, millise toote valisite.  
12. Sisestage miinimumkogus väljale **Alates**.
    - Kui klient peab tellima miinimumkoguse, enne kui kvalifitseerub uue hinna saamiseks, peate määrama selle koguse siin.  
    - Sisestage väärtus väljale **Kuni**, et määrata maksimaalne kogus, üle mille leppe hind ei kehti. Kui pakute hindu ja allahindlusi mitme kogusekatkestuse põhjal, määrake iga koguserühm miinimum- ja maksimumkoguse paarina vastavalt väljadel **Alates** ja **Kuni**.
13. Sisestage hind väljale **Summa valuutas**.
14. Sisestage jaotise **Üksikasjad** väljale **Alguskuupäev** kuupäev, millest alates see lepe kehtib.
15. Klõpsake valikut **Salvesta**.
16. Klõpsake valikut **Kinnita**.
17. Klõpsake **Kinnita valitud read**.
18. Klõpsake valikut **OK**.
19. Klõpsake käsku **Sisesta**.
20. Klõpsake valikut **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Toote kaubanduslepete kuvamine

1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.
2. Leidke ja valige loendist toode, mille hinda äsja värskendasite.
3. Klõpsake paanil **Tegevuspaan** nuppu **Müük**.
4. Klõpsake **Kuva kaubanduslepped**.
    
    Vaadake üle äsjaloodud hinna kaubandusleppe üksikasjad.

5. Sulgege leht.

## <a name="additional-resources"></a>Lisaressursid

### <a name="whitepaper"></a>Tehniline ülevaade

Lisateabe saamiseks laadige alla järgmine tehniline ülevaade (kirjutatud versiooni AX2012 toetamiseks, kuid kehtib ka rakendusele Dynamics 365 Supply Chain Management)

- [Kaubanduslepped](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>Kogukonna ajaveebid

- [Müügihinnad rakenduses Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]