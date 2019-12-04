---
title: Hankija portaali kasutajate turvalisus
description: See artikkel selgitab, kuidas seadistada hankija portaali kasutavate väliste hankijate turvet. See teave kehtib ainult Dynamics AX-i 2016. aasta veebruari ja 2016. aasta mai versioonide puhul.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 944b27754e87d80584b7fdfffa46d8af112227e3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813565"
---
# <a name="vendor-portal-user-security"></a>Hankija portaali kasutaja turvalisus

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada hankija portaali kasutavate väliste hankijate turvet. See teave kehtib ainult Dynamics AX-i 2016. aasta veebruari ja 2016. aasta mai versioonide puhul.

Hankija portaali funktsionaalsus on rakenduse Dynamics 365 for Operations versioonis 1611 asendatud hankija koostöö laiendatud funktsionaalsusega. Lisateavet hankija koostöö turvalisuse seadistamise kohta vt teemast [Hankija koostöö seadistamine ja haldamine](set-up-maintain-vendor-collaboration.md). Hankija portaal näitab välishankijatele piiratud koguses teavet ostutellimuste (OT-d) kohta. Oluline on seadistada Microsoft Dynamics AX-i hankija portaali kasutajaõigused õigesti, nii et hankijatel ei oleks lubamatut juurdepääsu teie Dynamics AX-i installi lisateabele. **Oluline.** Erinevalt teistest kasutajatest ei peaks välishankijatel olema rolli **SystemUser**. Roll **SystemUser** annab juurdepääsu privileegide kogumile, mis ei ole väliskasutajatele sobivad.

## <a name="setting-up-a-vendor-portal-user"></a>Hankija portaali kasutaja seadistamine
Enne kui loote kasutajakonto kellelegi, kes kasutab hankija portaali, peate seadistama hankija, et lubada hankija portaali koostöö. Kasutage välja **Ostutellimuse koostöö** lehe **Hankijad** vahekaardil **Üldine**. Välishankijatel, kes kasutavad hankija portaali, peab olema järgmine seaditus.

-   Microsoft Azure Active Directory (AAD) rakenduse kasutajakonto peab olema hankijale registreeritud Dynamics AX-i lehel **Kasutajad**.
-   Hankijal peab olema turberoll **(Välis)hankija**, mitte roll **SystemUser**. **Märkus.** Roll **SystemUser** antakse automaatselt, kui loote Dynamics AX-is uue kasutajakonto. Seega peate selle rolli eemaldama ja kinnitama hoiatusteate, mille saate.
-   Hankija-kasutajale ei tohiks anda luba lisada täiendavaid välju ostutellimuse tabelitest oma ostutellimuse vaatesse. Määrake vahekaardil **Isikupärastamine**, vahekaardil **Kasutajad** kasutaja suvand **Üksikasjalik isikupärastamine on lubatud** olekusse **Ei**.
-   Kasutajakonto peab olema seostatud registreeritud kontaktisikuga. Valige kontaktisik lehe **Kasutajad** väljal **Nimi**. Valitud isikul peab olema asjakohase hankija jaoks olema roll **Kontakt**.

Kui sama isik taotleb mitme hankijakonto juurdepääsu hankija portaalile (võib-olla erinevatele juriidilistele isikutele), tuleb selle isiku iga kasutajakonto seostada sama registreeritud kontaktisikuga. Roll **(Välis)hankija** hõlmab kõiki põhilisi võimalusi, mis on nõutavad hankija portaalis saadaolevate funktsioonide kasutamiseks. See seadistus aitab tagada, et kasutajaliides, mida väliskasutaja näeb, keskendub ainult ettenähtud stsenaariumile.

<a name="additional-resources"></a>Lisaressursid
--------

[Hankijatega koostöö tegemine Hankija portaali kasutades](collaborate-vendors-vendor-portal.md)



