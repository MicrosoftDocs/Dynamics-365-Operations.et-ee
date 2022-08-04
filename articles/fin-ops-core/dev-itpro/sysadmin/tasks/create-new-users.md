---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00da7c69ff18abd02ca0cd7984e9b2de5e453a0c
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103321"
---
# <a name="create-new-users"></a>Uute kasutajate loomine

[!include [banner](../../includes/banner.md)]

Enne kui pääsete juurde finantside ja toimingute rakendustele, tuleb teid kõigepealt lisada lehele **Kasutajad** (**Süsteemihalduse kasutajad \>\>**). Kasutajad hõlmavad teie organisatsioonisiseseid töötajaid või väliseid kliente ja hankijaid. Kasutajaid saab importida või lisada käsitsi. Kõik kasutajad peavad ühilduvaks kasutuseks olema õigesti litsentsitud.

Lisateavet finantside ja toimingute rakenduste ostmise ja litsentsimise kohta vt teemast [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Kasutajale litsentsi määramine
Süsteemi administraatorid saavad [määrata litsentsid kasutajatele](/office365/admin/subscriptions-and-billing/assign-licenses-to-users) halduskeskuses [Microsoft 365](/office365/admin/admin-overview/about-the-admin-center).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Azure AD-s välise kasutaja lisamine ja litsentsi määramine 
Litsentside määramiseks peavad välised kasutajad olema teie rentniku teegis esindatud (Azure Active Directory (Azure AD)). Need välised kasutajad tuleb lisada Azure AD's rentnikku külaliskasutajatena ja seejärel määrata vastavad litsentsid. Finantside ja toimingute rakenduste vajadus on see, et külaliskasutaja ettevõtte peab seda kasutama Azure AD. Lisateavet vt teemast [Azure portaalis Azure Active Directory B2B koostöö kasutajate lisamine](/azure/active-directory/b2b/add-users-administrator).

## <a name="import-new-users-from-azure-ad"></a>Uute kasutajate importimine teenusest Azure AD 
1. Avage **Süsteemihaldud** \> **Kasutaja** \> **Kasutajad**.
2. Toimingupaanil valige **Impordi kasutajad**.
3. Valige imporditavad failid. Loend hõlmab Azure AD kasutajaid, kes pole praegu selles keskkonnas kasutajad.
4. Valige **Impordi kasutajad**.
5. Valige suvand **Sule**.

> [!NOTE]
> Välja **Ettevõte** väärtus määratakse administraatori praeguse seansi ettevõtte põhjal. Pärast importimist peate määrama vastavalt vajadusele rollid ja organisatsioonid. Lisainfo saamiseks vt [Kasutajatele turberollide määramine](assign-users-security-roles.md). Tingimuslikult võib olla nõutav ka kasutaja seostamine **isikuga** ja kasutaja valikute uuendamine, nt keel.

## <a name="manually-add-a-new-user"></a>Uue kasutaja käsitsi lisamine
1. Avage **Süsteemihaldus** \> **Kasutajad** \> **Kasutajad**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljale **Kasutaja ID** saate sisestada küsimustiku kordumatu koodi.   
4. Sisestage väljale **Kasutajanimi** kasutaja nimi.  
5. Väljal **Pakkuja** tehke järgmist.
 - Sisemiste kasutajate puhul kasutage vaikeväärtust. Näiteks teie Azure AD rentnik koos eesliitega https://sts.windows.net/.  
 - Mitte-Azure AD kasutajate jaoks, näiteks teenustevahelised kontod, sisestage põhiteksti väärtus. Näiteks, NA. See väärtus aitab vältida valesid autentimiskutseid, mis võivad põhjustada tõrkeid, kui kasutatakse kehtivat identiteedipakkuja väärtust.  
 - Väliste või külaliskasutajate jaoks lisage nende Azure AD rentniku nimi aadressi https://sts.windows.net/ järel.
6. Sisestage väljale **Meil** kasutaja täispikk meil / kasutaja üldnimi.  
7. Valige väljal **Ettevõte** kasutaja vaikimisi avatav ettevõte. 
8. Valige käsk **Salvesta**.

Identiteedipakkuja ja telemeetria ID väärtusi värskendatakse [Microsofti graafiku](/graph/overview) kutse põhjal, kui kasutajakirje salvestatakse. Telemeetria ID põhineb kasutaja objekti ID-l / turbeidentifikaatoril (SID) Azure AD-s.

> [!NOTE]
> Pärast kasutaja lisamist peate määrama vastavalt vajadusele rollid ja organisatsioonid. Lisainfo saamiseks vt [Kasutajatele turberollide määramine](assign-users-security-roles.md). Tingimuslikult võib olla nõutav ka kasutaja seostamine **isikuga** ja **kasutaja valikute** uuendamine, nt keel.

## <a name="change-a-user-id"></a>Kasutaja ID muutmine
Kasutaja ID muutmiseks peate võtme andmebaasis ümber nimetama. Kui muudate seda protseduuri kasutades kasutaja ID, muudetakse kõiki seotud kasutajasätteid, et kasutada uut kasutaja ID-d. Näiteks tabeli **SysLastValue** kasutusteavet värskendatakse, et see viitaks uuele kasutaja ID-le.

> [!NOTE]
> Kasutaja ID on kasutajateabe tabeli primaarvõti. Primaarvõtme ümbernimetamine võib olemasoleva kasutaja puhul võtta aega, kuna kõiki võtme viiteid värskendatakse ka andmebaasis. 

1. Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.
2. Valige loendist kasutaja ja valige **Suvandid\> Kirje teave**.
3. Valige nupp **Nimeta ümber**.
4. Sisestage kasutaja ID uus ja ainulaadne väärtus ning valige seejärel **OK**. 
5. Kinnitamiseks valige **Jah**.

## <a name="additional-resources"></a>Lisaressursid

Lisateavet B2B kasutajate juurutamiseks vt [B2B kasutajate eksportimine Azure AD-sse](../implement-b2b.md).

Lisateavet eelkonfigureeritud süsteemikontode kohta vt [Eelkonfigureeritud süsteemikontod](../pre-configured-system-accounts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
