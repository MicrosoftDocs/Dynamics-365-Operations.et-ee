---
title: Halda äripartneri kasutajaid B2B e-commerce'i veebisaitidel, kasutades Dynamics 365-müüki
description: See teema kirjeldab Microsoft Dynamics, kuidas kasutada 365 Dynamics 365 Commerce Müüki äripartneri kinnituste haldamiseks ettevõtete vahel (B2B) veebisaitidel.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c6ac5409de5101c91b9348de800e3eaea9895c23
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312124"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Halda äripartneri kasutajaid B2B e-commerce'i veebisaitidel, kasutades Dynamics 365-müüki

[!include [banner](../../includes/banner.md)]

See teema kirjeldab Microsoft Dynamics, kuidas kasutada 365 Dynamics 365 Commerce Müüki äripartneri kinnituste haldamiseks ettevõtete vahel (B2B) veebisaitidel. Organisatsioonid, mis on Dynamics 365 müügilahenduses juba olemas, saavad kasutada oma müügivihjete ja -võimaluste mõisteid B2B e-äripartneri kinnitusprotsessis.

Lisateavet B2B äripartneri kinnitusprotsessi kohta vt [B2B e-kaubanduse veebisaitidel äripartneri kasutajate haldamine](manage-b2b-users.md).

Potentsiaalsed äripartnerid saavad käivitada sisseseadmisprotsessi B2B e-äri veebisaidile, esitades sisseostmistaotluse B2B veebisaidi lingi kaudu. Kui taotlus on **esitatud ja asjakohased tööd (** nt P-0001 **ja** **Sünkrooni tellimused ja kanali taotlused) käitatakse Commerce Headquartersis, salvestatakse sisseostmise taotlus Commerce Headquartersi lehel Kõik potentsiaalsed** kliendid. Äripartneri potentsiaalse kliendi kinnitusprotsessi saab seejärel müügis lõpetada.

Kui müügi ja ärisuhte vaheline integratsioon on lubatud, põhjustab äripartneri *äripotentsiaali loomine Ärirakenduses müügis müügivihje* loomise.

Järgmine näide näitab näiteid müügis äripartneri potentsiaalse kliendi müügivihjete loomise lehe kohta.

![Dynamics 365 müügi juhtlõnga loomise leht.](../media/LeadInSales.png)

Illustratsioonis näitab **kontakt** jaotises isikuid, kes on esitanudboardingu taotluse, ning **jaotises Ettevõte** kuvatakse organisatsioon. Märkus jaotises Ajajoon **näitab**, et müügivihje on loonud topeltkirjutuse infrastruktuuri. Kuna selle lõi topeltkirjutuse infrastruktuur, ei kuvata **seda müügivihjet ripploendis Minu avatud** müügivihjed. Selle asemel kuvatakse see uue vaate all nimega Kõik **äri B2B-müügivihjed**.

Müügi standardse müügivihje kvalifikatsiooniprotsessi kohta, kui kasutaja "täpi annab" müügivihje, *võimaluse* kirje, *·* *kontaktikirje ja kontokirje*. Topeltkirjutuse infrastruktuuri kasutatakse kontakti ja konto kirjete commerce'i kirjutamiseks. Kontakt luuakse seda tüüpi kliendina *ja* ettevõte luuakse organisatsiooni tüübi *kliendina*. Kui kasutaja valib võimaluse jaoks **valiku Sule** valikuks Võidetud, kinnitatakse potentsiaalne klient äris. Potentsiaalse kliendi kinnitamine põhjustab kliendi hierarhia loomise.

Kõik ülejäänud äriprotsessid esinevad Commerce's. Need protsessid hõlmavad e-kirja saatmist äripartnerile, krediidilimiidi halduse määratlemist kasutajatele ja B2B-saidile kasutajate lisamist. Kui kasutaja märgib müügivihje diskvalifitsendiks või märgib võimaluse müügivihje kvalifitseerimise asemel kaotatuks, märgitakse äripotentsiaalne klient tagasi lükatud ja tagasi lükkav meil saadetakse nõudeandjale.

## <a name="enable-integration-between-sales-and-commerce"></a>Luba müükide ja äride integreerimine

Müügi ja äri integratsioon põhineb topeltkirjutuse infrastruktuuril. Seetõttu tuleks topeltkirjutus lubada ja töötada nii, et ühes süsteemis loodud kliendid kirjutatakse teise süsteemi. Lisateavet topeltkirjutuse infrastruktuuri kohta vt topeltkirjutuse [ülevaatest](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Kui topeltkirjutuse häälestus on lõpule viidud, [Microsoft AppSource](https://appsource.microsoft.com/)[saab rakenduspartner minna ja otsida lahendust nimega Topeltkirjutuse ärilahendused](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Installige pakett standardse installiviisardi abil ja seejärel testige seda, luues potentsiaalse kliendi B2B saidil. Pärast potentsiaalse kliendi loomist veenduge, et taotlus kuvataks kõigil potentsiaalsete klientidel äris, ja seejärel veenduge, et potentsiaalne klient kuvatakse **müügis** müügivihjena.

## <a name="additional-resources"></a>Lisaressursid

[Äripartnerist kasutajate haldamine B2B e-kaubanduse veebisaitidel](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
