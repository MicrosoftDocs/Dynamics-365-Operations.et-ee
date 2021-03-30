---
title: Hoolduskavade plaanimine
description: Selles teemas selgitatakse hoolduskavade plaanimist varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c84711412d799f9d3cce02e0740ec065ef42d8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223550"
---
# <a name="schedule-maintenance-plans"></a>Hoolduskavade plaanimine

[!include [banner](../../includes/banner.md)]

 

Ennetav hoolduskavade plaanimine loob kalendri varade kohta seadistatud hooldusplaanide põhjal kanded varade kohta. Saate plaanida kalendri kandeid valitud hoolduskavade, vara tüüpide ja varade põhjal.

1. Klõpsake suvandil **Varahaldus** > **Perioodiline** > **Ennetav hooldus** > **Hoolduskavade plaanimine**.

2. Intervalli saate valida väljadel **Periood** ja **Perioodi sagedus**.

>[!NOTE]
>Väljad **Periood** ja **Perioodi sagedus** näitavad kui palju aega ette soovite hooldusgraafiku ridu luua tuginedes loodud hoolduskavadele (ajapõhised või loenduripõhised). Alloleval joonisel olevad hooldusgraafiku read (= töökäsu ettepanekud) on loodud alates praegusest kuupäevast ja kolm kuud pärast seda.

3. Valige tumblernupu **Loo automaatselt, kui real on täpsustatud** väärtuseks "Jah", kui hoolduskava rea põhjal tuleks automaatselt luua töökäsud.

>[!NOTE]
>Kui tumblernupp on seatud väärtusele "Jah" *ja* märkeruut **Loo automaatselt** on hoolduskavade ridadel valitud vormil **Hoolduskavad**, luuakse töökäsud hoolduskava ridade põhjal ja samuti luuakse hooldusgraafiku read olekuga "Töökäsu loodud". Kui ainult üks suvand on valitud (selles dialoogis tumblernupp **Loo automaatselt, kui real on täpsustatud** või märkeruut **Loo automaatselt** vormil **Hoolduskavad**), luuakse ainult hooldusgraafiku read olekuga "Loodud". Sellisel juhul töökäske ei looda.

4. Kalendri kandeid on võimalik luua hoolduskavade (aja- ja loenduripõhiseid), varade, vara tüüpida, töö asukohtade ja töö asukohatüüpide põhjal. Klõpsake nuppu **Filter** ja tehke oma valikud, kui seda nõutakse.

- Töö asukohtade põhjal hoolduskavade plaanimisest: kui värskendate vara tüüpide, tootjate ja mudelite seadistust hoolduskavadel kiirkaardil **Kõik töö asukohad** > **Hoolduskavad**, pärast seda, kui olete plaaninud hoolduskavad, kustutatakse automaatselt selle töö asukohaga seotud olemasolevad hooldusgraafiku kanded. Selleks, et luua uusi kalendri kandeid, mis on vastavuses värskendatud hoolduskava seadistusega töö asukoha jaoks, peate selle töö asukoha jaoks käivitama uue hoolduskava plaanimise. Vara tüüpida, tootjate ja mudelite seadistuse kohta lugege täpsemalt teemast [Töö asukohtade loomine](../functional-locations/create-functional-locations.md).

>*Näide*: soovite luua hoolduskava konkreetse töö asukoha jaoks, mis tähendab, et kui plaanite hoolduskava, kaasatakse kõik mis tahes ajal selle töö asukoha jaoks seadistatud varad. Sellisel juhul loote hoolduskava ja valite konkreetse funktsionaalse asukoha, kuid te EI lisa hoolduskavasse ühtegi vara. Tulemuseks on see, et kui te plaanite seda hoolduskava, luuakse hooldusgraafiku read kõigi töö asukohaga seotud varade kohta mis tahes ajal.

- Kui teete muudatusi vara tüüpide, tootjate ja mudelite kohta vormil **Vara tüübid**, mõjutavad need muudatused ainult uusi varasid, mis kasutavad värskendatud vara tüüpi. Vara tüüpide seadistuse kohta lugege täpsemalt teemast [Vara tüübid](../setup-for-objects/object-types.md).  

5. Klõpsake **OK**, et alustada hooldusgraafiku kannete loomist varade kohta. Loodud kandeid näidatakse loendilehel **Kõik hooldusgraafikud**. Järgnev illustratsioon näitab dialoogi **Plaani hoolduskavad** näidet.

![Joonis 1](media/09-preventive-maintenance.png)

- Dialoogis **Plaani hoolduskavad** saate seadistada pakett-tööd kiirkaardil **Käivita taustal**, et kalendri kannete loomine toimuks automaatselt regulaarsete intervallidega.  
- Kui plaanite ennetava hoolduse, ei looda hooldusgraafiku ridu, mille oodatav alguskuupäev ja kellaaeg on varasemad kui süsteemi kuupäev ja kellaaeg.  

Alloleval joonisel on kujutatud graafiline illustratsioon ajapõhisest hoolduskava arvutusest.  

![Joonis 2](media/10-preventive-maintenance.jpg)

Loenduripõhistest hoolduskavadest: allolevatel joonistel kuvatakse kahte erinevat loenduri registreerimise tsüklit. Need põhinevad hoolduskaval, mis on seadistatud vara "V0001" jaoks ja eeldatakse, et vara (auto) sõidab iga kuu ligikaudu 2000 km.

Esimeses näites ei läbita iga kuu eeldatavat 2000 km. Vastavalt loenduripõhisele hoolduskavale on lävi 2000 km, mis tähendab, et kui käivitate hoolduskava plaanimise, peaks hooldusgraafiku rida olema loodud iga kord, kui jõutakse 2000 km läveni. Näites 1 on 4 registreerimise rida, kuid 2000 km läveni on jõutud ainult ühel korral. See tähendab, et kui käivitate selle vara jaoks hoolduskavade plaanimise, näiteks kolmekuulise perioodi jaoks, luuakse ainult üks hooldusgraafiku rida.

Järgmisel joonisel registreeritakse igal kuul 2000 või enam km. Seetõttu luuakse selle vara kohta kolmekuulise perioodiga hoolduskavade plaanimise käigus kolm hoolduse rida. 

Siin kirjeldatud näidete põhjal on näha, et kõik vara kohta tehtud loenduri registreeringud näitavad tendentsi, mis kirjeldab vara kulumist. Seda tendentsi kasutatakse arvutuse aluseks hoolduskava plaanimise ajal.

![Joonis 3](media/11-preventive-maintenance.png)

![Joonis 4](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]