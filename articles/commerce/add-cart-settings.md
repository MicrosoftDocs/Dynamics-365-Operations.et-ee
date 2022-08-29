---
title: Toote ostukorvi lisamise rakendamine
description: See artikkel hõlmab sätteid "Lisa toode korvi" ja kirjeldab nende rakendumist Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16644e6746d182cd86a40861c4e30a85a9d3d478
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277023"
---
# <a name="apply-add-product-to-cart-settings"></a>Toote ostukorvi lisamise rakendamine

[!include [banner](includes/banner.md)]

See artikkel hõlmab **toote ostukorvi lisamise sätteid** ja kirjeldab nende rakendumist ostukorvis Microsoft Dynamics 365 Commerce.

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
