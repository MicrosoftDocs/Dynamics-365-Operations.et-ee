---
title: Varahalduse mobiilse tööruumi häälestamine
description: Selles teemas kirjeldatakse, kuidas häälestada rakendus Microsoft Dynamics 365 Supply Chain Management ja mobiilirakendus Finance and Operations (Dynamics 365) käitama varahalduse mobiilset tööruumi, mida töötajad saavad kasutada varahalduse ülesannete täitmiseks.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bc170df2fc58ae6b42fbc8834caad0bb7cd16f69
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837773"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Varahalduse mobiilse tööruumi häälestamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas häälestada rakendus Microsoft Dynamics 365 Supply Chain Management ja mobiilirakendus Finance and Operations (Dynamics 365) käitama mobiilset tööruumi **Varahaldus**, mida töötajad saavad kasutada varahalduse ülesannete täitmiseks.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Hooldustöötajate häälestamine teenuses Supply Chain Management

Iga kasutaja kes vajab juurdepääsu **varahalduse** mobiilsele tööruumile, järgib järgmisi juhiseid.

1. Avage teenuses Supply Chain Management suvand **Inimressursid \> Töötajad** ja veenduge, et kasutaja jaoks, kellele soovite selle häälestada, oleks töötaja kirje olemas. Looge vajaduse korral uus töötaja kirje.
1. Avage **Varahaldus \> Seadistus \> Töötajad \> Töötajad** ja veenduge, et töötaja kirje, mille te eelmises etapid tuvastasite (või lõite), oleks vastendatud hooldustöötaja kirjega. Looge vajaduse korral uus hooldustöötaja kirje ja määrake väli **Töötaja** eelmise etapi töötaja kirjele.
1. Avage **Varahaldus \> Seadistus \> Töötajad \> Hooldustöötajate grupid** ja veenduge, et hooldustöötaja kirje, mille te eelmises etapid tuvastasite (või lõite), kuuluks hooldustöötajate gruppi.
1. Avage **Süsteemihaldus \> Kasutajad**.
1. Valige ruudustikust asjakohane kasutaja.
1. Määrake kiirkaardil **Kasutaja üksikasjad** väli **Isik** töötaja kontole, kelle soovite praeguse kasutajakontoga seostada. See töötaja konto peaks olema töötaja kirje, mille 1. etapis tuvastasite (või lõite) ja vastendasite hooldustöötaja kirjega 2. etapis.

> [!NOTE]
> Kasutajaõigused ja turberollid rakenduvad mobiilse tööruumi **Varahaldus** funktsioonidele samamoodi nagu need rakenduvad teenuse Supply Chain Management kasutajaliidese funktsioonidele. Seetõttu peavad igal kasutajal, kelle jaoks mobiilse tööruumi **Varahaldus** juurdepääsu häälestate, omama turberolle, mis on vajalikud sarnaste toimingute tegemiseks otse teenuses Supply Chain Management.

## <a name="publish-the-asset-management-mobile-workspace"></a>Varahalduse mobiilse tööruumi avaldamine

Varahalduse funktsioonide mobiilirakenduses Finance and Operations (Dynamics 365) kättesaadavaks tegemiseks peate avaldama mobiilse tööruumi **Varahaldus**.

1. Valige teenuses Supply Chain Management nupp **Sätted** (ülemises parempoolses nurgas olev hammasratta sümbol) ja valige seejärel menüüst suvand **Mobiilirakendus**.
1. Leidke dialoogiboksis **Mobiilirakenduse haldamine** paan **Varahaldus**. Kui see sisaldab teksti „Metaandmetes – pole avaldatud”, ei ole tööruumi veel avaldatud. Kui see sisaldab teksti „Metaandmetes - avaldatud”, on tööruum juba avaldatud ja saate selle protseduuri ülejäänud osa vahele jätta.

    ![Dialoogiboks Mobiilirakenduse haldamine](media/mobile-workspaces.png "Dialoogiboks Mobiilirakenduse haldamine")

1. Valige paan **Varahaldus** ja valige seejärel tööriistaribal käsk **Avalda**. Mõne sekundi pärast peaksite saama teatise, mis ütleb, et tööruum on avaldatud. Lisaks peaks paanil olev tekst muutuma variandile „Metaandmetes – avaldatud”.

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Mobiilirakenduse Finance and Operations (Dynamics 365) installimine ja häälestamine

1. Avage üks järgmistest rakendusepoodidest, et installida rakendus **Microsoft Finance and Operations (Dynamics 365)** oma mobiilseadmesse.

    - [Google’i Androidi seadmed](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Apple’i iOS-i seadmed](https://go.microsoft.com/fwlink/?linkid=850663)

1. Avage rakendus Finance and Operations (Dynamics 365). Ilmuma peaks sisselogimisleht. Sisestage **sisselogimise** väljale oma Supply Chain Managementi URL või valige loendist **Hiljutised keskkonnad** hiljutine URL ja puudutage seejärel valikut **Ühenda**.

    ![Sisselogimise leht](media/mobile-app-sign-in.png "Sisselogimise leht")

1. Kui teil palutakse ühendus kinnitada, märkige ruut **Ma mõistan** ja puudutage suvandit **Ühenda**.
1. Kasutage lehel **Konto valimine** oma Microsofti kontot mobiilirakendusse sisselogimiseks.

    Kuvatakse leht **Tööruumid**. See loetleb kõik mobiilsed tööruumid, mille teie Supply Chain Managementi eksemplar on avaldanud.

    ![Tööruumide loend](media/mobile-app-workspaces.png "Tööruumide loend")

1. Kui peate juriidilist isikut (ettevõtet) muutma, puudutage ülemises vasakpoolses nurgas nuppu Menüü (vahel viidatakse sellele kui hamburger või hamburgeri nupp) ja puudutage seejärel nuppu **Muuda ettevõtet**.

    ![Juriidilise isiku muutmine](media/mobile-app-change-comp.png "Juriidilise isiku muutmine")

1. Lehel **Tööruumid** valige avamiseks tööruum, millega soovite töötada.

    ![Varahalduse mobiilne tööruum](media/mobile-app-asset-workspace.png "Varahalduse mobiilne tööruum")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Varahalduse mobiilse tööruumiga töötamine

Lisateavet selle kohta, kuidas mobiilse tööruumiga **Varahaldus** töötada, vt teemat [Varahalduse mobiilse tööruumi kasutamine](asset-management-mobile-workspace.md).

Lisateavet mobiilirakenduse Finance and Operations (Dynamics 365) kohta vt [mobiilirakenduse kodulehelt](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]