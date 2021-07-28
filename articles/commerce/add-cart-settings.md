---
title: Toote ostukorvi lisamise rakendamine
description: See teema hõlmab "ostukasti moodulite lisamist" ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce rakendada.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 55b81e7c644f884b052853206f312ac796031600
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479440"
---
# <a name="apply-add-product-to-cart-settings"></a>Toote ostukorvi lisamise rakendamine

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab **ostukasti moodulite lisamist** ja kirjeldab, kuidas neid Microsoft Dynamics 365 Commerce rakenduses rakendada.

Erinevaid töövooge toetatakse, kui toode lisatakse Dynamics 365 Commerce ostukorvi e-commerce saidil. Näiteks võidakse saidi kasutaja ostukorvi lehele võtta. Teise võimalusena võib kasutaja püsida praegusel lehel, kuid saab teatise, mis kinnitab, et toode lisati ostukorvi.

Erinevate töövoogude toetamiseks on väli **Lisa toode ostukorvi** saadaval **Seaded \> Laiendid** Commerce saidi ehitajas. Valige vastava töövoo rakendamiseks üks järgmistest sättevalikutest:

- **Navigeeri ostukorvi lehele** - Kasutajad suunatakse pärast kauba lisamist ostukorvi lehele.
- **Kuva teatised** - kuvatakse kasutajatele kinnitusteatis pärast kauba lisamist ostukorvi ja nad võivad jätkata toote üksikasjade lehe sirvimist (PDP).
- **Näita minikorvi** – kui kasutajad lisavad kauba ostukorvi, kuvatakse minikorvi sisu. Kasutajad saavad läbi vaadata kõik ostukorvis olevad kaubad ja nad saavad jätkata väljaregistreerimist, kui nad on valmis.
- **Näita teatisi, kasutades teatiste moodulit** – kui kasutajad lisavad kauba korvi, kasutatakse teatiste moodulit kinnitusteatise näitamiseks. Selle sätte valiku tööks tuleb teatiste moodul lisada lehekülje päisesse.
- **Ärge suunake ostukorvi lehele** - Kasutajad jäävad olemasolevale lehele pärast kauba lisamist ostukorvi.

Järgmine näide näitab saidikonstruktoris **toote ostukorvi lisamise** sättevalikuid.

![Näide toote ostukorvi lisamise sättevalikute kohta saidikonstruktoris](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - **Lisa toode ostukorvi** saidi sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11. Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama. Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Säte **Minikorvi näitamine** on saadaval alates versiooni Dynamics 365 Commerce 10.0.20 väljalaskest. Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama. Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Järgmisel pildil on näide kinnitusteatisest „lisati ostukorvi” Fabrikami saidil.

![Järgmisel pildil on näide kinnitusteatisest „lisati ostukorvi” Fabrikami saidil](./media/ecommerce-addtocart-notifications.PNG)

Järgmisel pildil on näide kinnitusteatisest „lisati ostukorvi” Adventure Works saidil.

![Järgmisel pildil on näide kinnitusteatisest „lisati ostukorvi” Adventure Works saidil](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Kaupluse valimise moodul](store-selector.md)
