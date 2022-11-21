---
title: B2C-avalduse loomine
description: See artikkel kirjeldab, kuidas portaalis luua ettevõtte tarbimist (B2C) Microsoft Azure rakendust.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785801"
---
# <a name="create-a-b2c-application"></a>B2C-avalduse loomine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas portaalis luua ettevõtte tarbimist (B2C) Microsoft Azure rakendust.

Kui teie B2C rentnik on loodud, loote ärisuhtega suhtlemiseks uue () rentniku Azure Active Directory piires B2C-rakenduse Azure AD.

B2C rakenduse loomiseks toimige järgmiselt.

1. Avage Azure’i portaalis suvand **Rakenduse registreerimised** ja valige **Uus registreerimine**.
1. Sisestage selle Azure AD B2C-rakenduse jaoks nimi väljas **Nimi**.
1. **Toetatud kontotüüpide** all valige **kontod mis tahes identiteedipakkujas või organisatsioonikaustas (kasutajavoogudega kasutajate autentimiseks)**.
1. **Ümbersuunamise URI** puhul sisestage oma sihtotstarbeline vastuse URL-id tüübina **Veeb**. Lisateavet vastuse URL-ide ja nende vormindamise kohta leiate allpool jaotisest [Vastuse URL-id](#reply-urls). Kasutaja autendimisel ümbersuunamiste lubamiseks B2C-st tagasisuunas peate sisestama ümbersuunamise URI/vastuse URL-i Azure AD. Vastuse URL-i saab lisada registreerimisprotsessi ajal või hiljem lisada, **valides B2C** rakenduse ülevaate jaotisest Ülevaade **lingi Lisa ümbersuunamise URI** **link**.
1. **Õiguste** puhul valige suvand **Hüvitise administraatori nõustumine openID-offline_access õigustega**.
1. Valige suvand **Registreeri**.
1. Valige vastloodud rakendus ja liikuge autentimise **menüüsse**. 
1. Vastuse URL-i **·** **·** **sisestamisel valige valiku Vaikimisi hüvitise ja rahavoo all nii juurdepääsu lubade kui ka ID-lubade** suvandid nende lubamiseks rakenduses ja seejärel valige **salvesta.** Kui registreerimise ajal ei sisestatud vastuse URL-i, saab **selle** lisada ka sellele lehele, valides suvandi Lisa platvorm, valides veebi ja **sisestades** seejärel rakenduse ümbersuunamise URI. Siis **on vaikimisi hüvitise ja rahavoo** jaotis saadaval **, et valida nii juurdepääsulubasid kui** **ka ID-pääsu suvandeid**.
1. Minge Azure'i portaali menüüsse **Ülevaade** ja kopeerige **Rakenduse (kliendi) ID**. Pange see ID hilisemate seadistusetappide jaoks üles (mida hiljem viidatakse kui **Kliendi GUID**).

Täiendavat viidet rakenduse registreerimiste kohta Azure AD B2C-s vt [Uue rakenduse registreerimiste kogemust Azure Active Directory B2C-ga](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Vastuse URL-id

Vastuse URL-id on olulised, kuna need tagavad tagastusdomeenide lubatud üksuste loendi, kui teie sait küsib Azure AD B2C kasutaja autentimist. See lubab autenditud kasutajal pöörduda tagasi domeeni, kuhu ta sisse logib (teie saidi domeen). 

Akna **Azure AD B2C - Rakendused \> Uus rakendus** kastis **Vastuse URL** tuleb lisada eraldi read nii saidi domeenile kui ka (kui teie keskkond on ette valmistatud) Commerce'i loodud URL-ile. Need URL-id peavad alati kasutama kehtivat URL-vormingut ja need peavad olema ainult alus-URL-id (neile ei järgne kaldkriipse ega teid). Seejärel tuleb lisada string ``/_msdyn365/authresp`` alus-URL-idele, nagu järgnevates näidetes illustreeritud.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domeen peab vastama täielikult e-kaubanduse domeenile. Kui teil on mitu domeeni, peate selle URL-i lisama igale domeenile.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Järgmised sammud

Ärisuhte (B2C) rentniku seadistamise jätkamiseks jätkake kasutajavoo [poliitikate loomisega](create-user-flow-policies.md).

## <a name="additional-resources"></a>Lisaressursid

[Jaekaubandusrentniku häälestamine Commerce'is](set-up-b2c-tenant.md)

[Looge või linkige olemasoleva B2C Azure AD rentnikuga Azure’i portaalis.](create-link-aad-b2c-tenant.md)

[Kasutajavoo poliitikate loomine](create-user-flow-policies.md)

[Sotsiaalstete identiteedipakkujate lisamine (valikuline)](add-social-identity-providers.md)

[Commerce headquartersi värskendamine uue Azure AD B2C-teabega](update-hq-aad-b2c-info.md)

[B2C rentniku konfigureerimine kaubanduse saidiehitajas](config-b2c-tenant-site-builder.md)

[Lisateave B2C kohta](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
