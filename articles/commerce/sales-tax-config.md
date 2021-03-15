---
title: Käibemaksu konfigureerimine veebitellimuste jaoks
description: Selles teemas antakse ülevaade käibemaksugrupi valikust erinevate veebitellimuse tüüpide puhul rakenduses Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 56621bb9658b71551c7312aa47812903914bc888
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031785"
---
# <a name="configure-sales-tax-for-online-orders"></a>Käibemaksu konfigureerimine veebitellimuste jaoks

[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade käibemaksugrupi valikust erinevate veebitellimuse tüüpide puhul. 

Teie e-kaubanduse kanal võib soovida toetada selliseid võimalusi nagu veebitellimuste kohaletoimetamine või peale võtmine. Käibemaksu kohaldatavus põhineb teie võrgukasutajate poolt valitud suvandil. Kui saidi klient otsustab osta kauba veebis ja lähetab selle aadressile, määratakse käibemaks kliendi lähetusaadressi maksugrupi sätte põhjal. Kui klient otsustab ostetud kauba poest peale võtta, määratakse käibemaks peale võtmise poe maksugrupi sätte alusel. 

## <a name="orders-shipped-to-a-customer-address"></a>Kliendi aadressile lähetatud tellimused 

Üldiselt määratleb kliendi aadressidele lähetatavate veebitellimuste maksud sihtkoht. Igal käibemaksugrupil on jaemüügi sihtkohapõhine maksukonfiguratsioon, kus teie ettevõte saab hierarhilisel kujul määratleda sihtkoha üksikasjad (nt maakond/regioon, maakond, maakond ja linn). Kui veebitellimus on sisestatud, kasutab kaubanduse maksumootor tellimuse iga reakauba tarneaadressi ja leiab käibemaksugrupid vastavate sihtkohapõhiste maksukriteeriumidega. Näiteks online-tellimuse puhul, mille rea kauba tarneaadress on San Francisco, California, leiab maksumootor California käibemaksugrupi ja käibemaksukoodi ning arvutab seejärel vastavalt iga reakauba maksu.  

## <a name="customer-based-tax-groups"></a>Kliendipõhised maksugrupid

Kaubanduse peakorteris on kaks kohta, kus kliendi maksugrupid on konfigureeritud.

- **Kliendi profiil**
- **Kliendi tarneaadress**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Kui kliendi profiilil on maksugrupp konfigureeritud

Kliendi profiilikirjel võib peakorteris olla konfigureeritud käibemaksugrupp, kuid internetitellimuste puhul ei kasuta maksumootor kliendi profiilis konfigureeritud käibemaksugruppi. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Kui kliendi tarneaadressil on maksugrupp konfigureeritud

Kui kliendi tarneaadressi kirjel on konfigureeritud maksugrupp ja internetitellimus (või reakaup) saadetakse kliendi tarneaadressile, kasutab maksumootor maksu arvutamisel kliendi aadressikirjes konfigureeritud maksugruppi.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Konfigureeri kliendi tarneaadressi kirjele maksugrupp

Kliendi tarneaadressi kirje maksugrupi konfigureerimiseks kaubanduse peakorteris toimige järgmiselt.

1. Avage **Kõik kliendid** ja valige soovitud klient. 
1. Valige **Aadressid** FastTab-is soovitud aadress ja seejärel valige **Veel suvandeid \> Täpsem**. 
1. Määrake **Üldine** vahekaardil **Halda aadresse** lehel käibemaksu väärtus vastavalt vajadusele.

> [!NOTE]
> Maksugrupp määratletakse tellimuserea tarneaadressi abil ja sihtkohapõhised maksud konfigureeritakse maksugrupis. Lisateavet vt teemast [Seadista maksud veebipoodidele vastavalt asukohale](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Tellimusele järgi tulemine kauplusesse

Kauplusesse järgi tulemise või tellimuse peale võtmise tellimuseridade puhul rakendatakse valitud peale võtmise kaupluse maksugrupp. Lisateavet antud kaupluse maksugrupi konfigureerimise kohta leiate teemast [Kaupluste muude maksusuvandite määramine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Kui tellimusele tullakse kauplusesse järgi, ignoreerib maksumootor kliendi aadressi maksusätteid (kui see on seadistatud) ja rakendatakse peale võtmise kaupluse maksu konfiguratsioon. 

## <a name="additional-resources"></a>Lisaressursid

[Käibemaksu ülevaade](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Käibemaksuarvutusmeetodid väljal Päritolu](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[Käibemaksu määramine ja tühistamised](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Maksuvabastuse arvutamine](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]