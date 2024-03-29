---
title: Uue e-kaubanduse rentniku juurutamine
description: See artikkel kirjeldab, kuidas juurutada uut Dynamics 365 Commerce e-äri saiti, kasutades elutsükli Microsoft Dynamics teenuseid (LCS).
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: c2dadbebea04b59680df5a5bbbd71e83eab41175
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267551"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Uue e-kaubanduse rentniku juurutamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas juurutada uut Dynamics 365 Commerce e-äri saiti, kasutades elutsükli Microsoft Dynamics teenuseid (LCS).

Microsoft Dynamicsi teenus Lifecycle Services (LCS) on pilvepõhine koostöö tööruum, mida partnerid ja kliendid saavad kasutada oma projektide ja keskkondade haldamiseks, Microsoft Dynamicsi toodete ja funktsioonide kohta uusima teabe vaatamiseks ning teenindusjuhtumite loomiseks, jälgimiseks ja sirvimiseks. E-kaubanduse haldusefunktsioonid on LCS-i integreeritud.

Lisateavet LCS-i kohta vaadake teemast [Teenuse Lifecycle Services kasutusjuhend](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Alustage

Enne e-kaubanduse lähtestamist tuleb teil lähtestada projekt, keskkond ja Retail Cloud Scale Unit (RCSU). LCS-i lähtestamiseks peab teil olema kas projekti omaniku või keskkonnahalduri rolli õigused. Tootmise ja liivakasti keskkonna topoloogiad on toetatud.

Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Lisateavet RCSU kohta leiate teemast [Lähtesta Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>E-kaubanduse lähtestamine

Kasutage seda protseduuri, et lähtestada e-kaubanduse funktsioon olemasolevas keskkonnas.

Enne alustamist veenduge, et teil on järgmine vajalik teave.

- Kasutatav RCSU.
- Microsoft Azure Active Directory turbegrupp, mida kasutatakse e-kaubanduse süsteemiadministraatorite jaoks.
- Microsoft Azure Active Directory turvagrupp, mida kasutatakse hinnangute ja arvustuste moderaatorite jaoks.
- Keskkonnaga seostatavad domeenid.

Lisaks saate koguda järgmist valikulist teavet.

- Azure AD ettevõtja ja tarbija vaheline (B2C) teave.

    - Rentniku nimi.
    - Kliendi ID.
    - Kohandatud sisselogimisdomeen.
    - Vastuse URL.
    - Registreerumis- ja sisselogimispoliitika ID.
    - Paroolilähtestuspoliitika ID.
    - Profiilipoliitika ID redigeerimine.

> [!NOTE]
> Seda teavet saab hiljem teenuse taotluse alusel lisada.

Pärast nõutava teabe kogumist tehke e-kaubanduse lähtestamiseks järgmist.

1. Logige teenusesse [LCS](https://lcs.dynamics.com) sisse.
1. Avage projekt, mis sisaldab keskkonda, kus soovite e-kaubandust lähtestada.
1. Jaotises **Keskkond** valige keskkond.
1. Jaotises **Keskkonna funktsioonid** valige link **Jaemüügi haldus**.
1. Vahekaardil **E-kaubandus** valige **Seadistus**. Kuvatakse dialoogiaken, kus peate sisestama ettevalmistamiseks vajaliku teabe.
1. Täitke nõutud teave ja seejärel minge järgmisele lehele.
1. Järgmisel lehel täitke nõutud teave ja seejärel esitage vorm. Olete naasnud vahekaardile **E-kaubandus**, kus peaksite nägema, et lähtestamine on alanud.
1. Lähtestamise oleku vaatamiseks kas vajutage **Lähtesta** või naaske hiljem vahekaardile **E-kaubandus**.
    
Kui e-kaubandus on LCS-ist lähtestatud, valmistab süsteem ette mitu komponenti, mis on e-kaubandusele vajalikud, ja seostab need keskkonnaga. Pärast ettevalmistuse lõpuleviimist uuendatakse vahekaarti **E-kaubandus** lehel **Jaemüügi haldus**, et kajastada ettevalmistamist. Lehel kuvatakse uusimad kohanduste juurutused ja kõikide teiste käimasolevate juurutuste olekud. See sisaldab ka linke e-kaubanduse saidile ja Commerce'i saidiehitajat, kus saidid on tehtud.

## <a name="access-commerce-site-builder"></a>Juurdepääs Commerce'i saidiehitajale

Commerce'i saidiehitajale juurdepääsuks avage vahekaart **E-kaubandus** LCS-i lehel **Jaemüügi haldus** ja valige link **E-kaubanduse saidihalduse tööriist**. Saidiehitaja sihtleht kuvab rentniku tasemel vaadet. Sellelt lehelt saate teha järgmist.

- Rentniku taseme sätete muutmine.
- Navigeerige mistahes loodud saidile ja omage vaatamiseks õigusi. 
- Juurdepääs ülevaadete funktsioonidele, nagu modereerimine ja aruandlus.
- Uue saidi loomine. Lisateavet uue saidi loomise kohta vt jaotisest [E-kaubanduse saidi loomine](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas](configure-multi-B2C-tenants.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
