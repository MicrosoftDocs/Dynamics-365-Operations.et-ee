---
title: Hinnanguprofiilid
description: Selles teemas kirjeldatakse, kuidas seadistada andmeid hinnangu gruppidele.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828438"
---
# <a name="rating-profiles"></a>Hinnanguprofiilid

Hinnangu profiil sarnaneb logistika lepingule (kuid mitte juriidilisele lepingule). Seda kasutatakse koormate transpordi tariifide määramiseks. 

Iga hinnanguprofiil on vedaja puhul kordumatu. Hinnanguprofiilis seostatakse vedaja määra koondüksusega. Määra koondüksus defineerib määra aluse määrangu ja määra aluse. Määra alus määrab vedaja hinna.

Saate seadistada hinnanguprofiili, kasutades üldist lehte, mis annab ülevaade kõigist olemasolevatest hinnanguprofiilidest. Alternatiivina saate seadistada hinnanguprofiili ka otse vedaja alt. Mõlemal juhul on hinnangu profiili jaoks seadistatud teave sama.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Hinnangu profiili loomine või redigeerimine hinnangute profiilide lehel

Lehel **Hinnanguprofiilid** saate vaadata kõiki saadaolevaid hinnangu reegleid. Saate redigeerida ka olemasolevaid reegleid ja luua uusi profiile.

1. Avage **Transpordihaldus \> Seadistus \> Hinnang \> Hinnanguprofiil**.
1. Uue hinnanguprofiili lisamiseks ruudustikku valige tegumiribal nupp **Uus** või valige nupp **Redigeeri**, et redigeerida olemasolevat profiili.
1. Määrake uue või olemasoleva hinnangu profiili real järgmised väljad.

    - **Hinnanguprofiil** – Sisestage kordumatu identifikaator (ID) hinnanguprofiilile.
    - **Nimi** – Sisestage hinnanguprofiili kirjeldav nimi.
    - **Saadetise vedaja** – Valige saadetise vedaja. Teie seadistatav hinnanguprofiil kuvatakse valitud vedaja kohta ka **Saadetise vedaja** lehel.
    - **Sait** ja **Ladu** – Valige sait ja ladu.
    - **Määra mootor** – Valige hinnanguprofiili määra mootor.
    - **Määra koondüksus** – Valige hinnanguprofiili määra koondüksus. Määra koondüksuse abil saate määratleda määra aluse tüübi ja määra aluse. Lisateavet leiate teemast [Määra koondüksuse seadistamine](set-up-rate-masters.md).
    - **Transiidi aja mootor** – Valige hinnanguprofiili jaoks transiidi aja mootor.
    - **Vedaja kütuseindeks** – Valige hinnanguprofiili jaoks vedaja kütuseindeks.
    - **Teostamise alguskuupäev ja kellaaeg** ning **Teostamise lõppkuupäev ja-kellaaeg** – Määratlege periood, millal hinnanguprofiil peaks olema aktiivne.

1. Valige toimingupaanil nupp **Salvesta**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Hinnangu profiili loomine otse vedajate lehel

1. Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Kättetoimetajad**.
1. Valige nimekirjast vedaja.
1. Hinnanguprofiili loomiseks valige **Hinnanguprofiilide** FastTab-is **Uus**.
1. Seadistage uue hinnangu profiili väljad. Need väljad vastavad lehe **Hinnangu profiilid** väljadele, nagu on kirjeldatud selle teema eelmises jaotises.

> [!NOTE]
> Lehel **Saadetise vedajad** loodud profiilid kuvatakse ka lehel **Hinnanguprofiilid**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]