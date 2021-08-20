---
title: Käibemaksu konfigureerimine veebitellimuste jaoks
description: Selles teemas antakse ülevaade käibemaksugrupi valikust erinevate veebitellimuse tüüpide puhul rakenduses Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 5801bbfb5b5850cb4c9ae06140bff5adca9b368febdc06d69c538fc49f9ee40a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772957"
---
# <a name="configure-sales-tax-for-online-orders"></a>Käibemaksu konfigureerimine veebitellimuste jaoks

[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade käibemaksugrupi valikust erinevate võrgutellimuse tüüpide jaoks, kasutades sihtkoha- või kliendikontopõhiseid maksusätteid. 

Võite soovida, et teie e-kaubanduse kanal toetaks selliseid valikuid nagu kohaletoimetamine või veebitellimuste kättesaamine. Käibemaksu kohaldatavus põhineb teie võrguklientide poolt valitud suvandil. 

## <a name="destination-based-taxes-for-online-orders"></a>Võrgutellimuste sihtkohapõhised maksud

Üldiselt määratleb kliendi aadressidele lähetatavate veebitellimuste maksud sihtkoht. Igal käibemaksugrupil on jaemüügi sihtkohapõhine maksukonfiguratsioon, kus teie ettevõte saab hierarhilisel kujul määratleda sihtkoha üksikasjad (nt maakond või regioon, maakond, maakond ja linn).

### <a name="orders-delivered-to-customer-address"></a>Kliendi aadressile saadetud tellimused

Kui veebitellimus on sisestatud, kasutab kaubanduse maksumootor tellimuse iga reakauba tarneaadressi ja leiab käibemaksugrupid vastavate sihtkohapõhiste maksukriteeriumidega. Näiteks online-tellimuse puhul, mille rea kauba tarneaadress on San Francisco, California, leiab maksumootor California käibemaksugrupi ja käibemaksukoodi ning arvutab seejärel vastavalt iga reakauba maksu.

### <a name="order-pick-up-in-store"></a>Tellimusele järgi tulemine kauplusesse

Kauplusesse järgi tulemise või tellimuse peale võtmise tellimuseridade puhul rakendatakse valitud peale võtmise kaupluse maksugrupp. Lisateavet antud kaupluse müügimaksude seadistamise kohta leiate teemast [Kaupluste muude maksusuvandite määramine](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Võrgutellimuste kliendi kontopõhised maksud

Võib esineda äristsenaarium, kus soovite konfigureerida müügimaksugrupi konkreetsel kliendikontol Commerce peakorteris. Peakontoris on kaks kohta, kus saate kliendikontol käibemaksu konfigureerida. Neile juurdepääsuks peate esmalt pääsema kliendi üksikasjade lehele, minnes lehele **Retail ja Commerce \> Kliendid \> Kõik kliendid** ja valides seejärel klient.

Kaks kohta, kus konfigureerite kliendikonto müügimaksu, on järgmised.

- **Käibemaksugrupp** kliendi üksikasjade lehe kiirkaardil **Arve ja tarne**. 
- **Käibemaks** **aadresside haldamise** lehe kiirkaardil **Üldine**. Kliendi üksikasjade lehelt sinna jõudmiseks valige kiirkaardil **Aadressid** kindel aadress ja seejärel valige **Täpsemalt**.

> [!TIP]
> Kui soovite võrgukliendi tellimuste puhul rakendada ainult sihtkohapõhiseid makse ja vältida kliendikontol põhinevaid makse, veenduge, et väli **Käibemaksugrupp** oleks kliendi üksikasjade lehe kiirkaardil **Arve ja tarne** tühi. Tagamaks, et võrgukanali kaudu registreeruvad uued kliendid ei päriks käibemaksugrupi sätteid kliendi või kliendigrupi vaikesätetest, veenduge, et väli **Käibemaksugrupp** oleks tühi ka võrgukanali kliendi vaikesätete ja kliendigrupi sätete korral ( **Retail ja Commercea \>Kliendid \> Kliendigrupid**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Sihtpõhise maksu või kliendikontol põhineva maksu kohaldatavuse määratlemine 

Järgmises tabelis selgitatakse, kas veebipõhiste tellimuste puhul rakendatakse sihtkohapõhiseid või kliendikontopõhiseid makse. 

| Kliendi tüüp | Tarneaadress                   | Klient > Arve ja tarne > Käibemaksugrupp? | Aadress peakontori kliendikontol? | Kliendi aadress > Täpsemalt > Üldine > Käibemaksugrupp?                                              | Rakendatud käibemaksugrupp      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Külaline         | Manhattan, NY                      | Ei (tühi)                                                | Ei (tühi)                              | Ei (tühi)                                                                                                   | NY (sihtkohapõhised maksud) |
| Sisse logitud     | Austin, TX                          | Ei (tühi)                                             | Jah                               | None<br/><br/>Võrgukanali kaudu lisatud uus aadress.                                                            | TX (sihtkohapõhised maksud) |
| Sisse logitud     | San Francisco, CA (Kättesaamine poest) | Jah (NY)                                            | Pole kohaldatav                              | Pole kohaldatav                                                                                                    | CA (sihtkohapõhised maksud) |
| Sisse logitud     | Houston, TX                         | Jah (NY)                                            | Jah                               | Jah (NY)<br/><br/>Võrgukanali ja käibemaksugrupi kaudu lisatud uus aadress, mis on päritud kliendikontolt. | NY (kliendikontol põhinevad maksud)  |
| Sisse logitud     | Austin, TX                          | Jah (NY)                                            | Jah                               | Jah (NY)<br/><br/>Võrgukanali ja käibemaksugrupi kaudu lisatud uus aadress, mis on päritud kliendikontolt. | NY (kliendikontol põhinevad maksud)  |
| Sisse logitud     | Sarasota, FL                       | Jah (NY)                                            | Jah                               | Jah (WA)<br/><br/>Käsitsi seatud WA-le.                                                                          | WA (kliendikontol põhinevad maksud)  |
| Sisse logitud     | Sarasota, FL                       | Ei (tühi)                                                | Jah                               | Jah (WA)<br/><br/>Käsitsi seatud WA-le.                                                                          | WA (kliendikontol põhinevad maksud)  |

## <a name="additional-resources"></a>Lisaressursid

[Saate seadistada maksud võrgupoodide jaoks asukoha alusel](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Käibemaksu ülevaade](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Käibemaksuarvutusmeetodid väljal Päritolu](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Käibemaksu määramine ja tühistamised](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Maksuvabastuse arvutamine](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]