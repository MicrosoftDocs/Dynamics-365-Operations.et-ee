---
title: Kataloogi valija moodul
description: See artikkel katab kataloogi valijamoodulid ja Microsoft Dynamics 365 Commerce kirjeldab, kuidas lisada neid ettevõtetele (B2B) e-kaubanduse saitidele.
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-04-21
ms.openlocfilehash: 642319eea7e40415fd32898f6ec07bfc86f3b1b1
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136927"
---
# <a name="catalog-picker-module"></a>Kataloogi valija moodul

[!include [banner](includes/banner.md)]

See artikkel katab kataloogi valijamoodulid ja Microsoft Dynamics 365 Commerce kirjeldab, kuidas lisada neid ettevõtetele (B2B) e-kaubanduse saitidele.

Kataloogi valijamoodul on erikonteiner, mida kasutatakse kõikide B2B saidi kasutajatele ostuks saadaval tootekataloogide loetlemiseks. Mitut kataloogi toetatakse praegu ainult B2B-saitide puhul.

Järgmine näide näitab kataloogi valijamooduli näidet.

![Näide kataloogi valijamoodulist, kus on loetletud kolm tootekataloogi.](./media/Catalog-picker-sample.png)

## <a name="add-a-catalog-picker-module-to-your-site"></a>Kataloogi valijamooduli lisamine saidile

Kataloogi valijamooduli lisamiseks ärisaidi koostaja saidile järgige neid samme.

### <a name="create-a-catalog-picker-page"></a>Kataloogi valija lehe loomine

Kõigepealt looge kataloogi valija lehekülg.

1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Sisestage **dialoogiboksi Uue lehe** loomine jaotises Lehe nimi **kataloogi** **valija**.
1. Sisestage **lehekülje URL** jaotises Lehe URL ja seejärel valige **edasi**.

    ![Saate luua uue lehekülje dialoogiboksi.](./media/Create-catalog-picker-page.png)

1. Valige **valiku Vali mall** all **Üldine sisu** ja seejärel **edasi**.
1. Valige **valiku Vali paigutus** all Paindlik **paigutus** ja seejärel **edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui peate lehekülje teavet redigeerima, valige suvand **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**.
1. Valige **valiku Kataloogi valija** all **Põhipesa**, valige ellips (**...**) ja seejärel valige **lisamoodul**.

    ![Mooduli lisamine kataloogi valija aknas põhipesasse.](./media/Author-web-page-catalog-picker-1.png)

1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri **pesa, valige kolmikpunkt (**...**) ja seejärel valige lisamoodul** **.**
1. Dialoogiaknas **Vali** moodulid valige kataloogi **valija** moodul ja seejärel valige **OK**.
1. Valige kataloogi **valija** atribuutide paanil **pealkirjas** **kataloogid** ja seejärel sisestage kataloogi valijalehele pealkiri.
1. Valige **jaotises Pealkiri** taseme tase ja seejärel valige **OK**.
1. Sisestage **RTF-teksti** all tekst, mis ilmub kataloogi valija lehe ülaosas.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="add-a-link-on-your-account-page"></a>Oma kontolehele lingi lisamine

Järgmisena lisage oma kataloogi valijalehele viide oma minu **konto** lehel.

1. Minge **lehekülgedele**, otsige ja valige oma saidi minu **konto** leht ning seejärel valige käsk **Redigeeri**.
1. Valige lehe **põhipesast** konto üldine **paanipesa**. 
1. Valige konto **üldise paani** atribuutide paani jaotises **Lingid** suvand **Lisa tegevuse link** ja seejärel valige link **Tegevus**.
1. Sisestage **dialoogiakna** Tegevuslingi jaotises **Lingi tekst** kataloogi valija lehele lingi tekst.
1. Lingi **sihtmärgi all** valige **lisa link**.
1. Dialoogiaknas **Lingi lisamine** valige leht **Kohandatud ja** seejärel valige **edasi**.
1. Valige **jaotises** Nimi oma kataloogi valija lehekülg, valige Rakenda **ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Järgmine näide näitab kontolehe näidet viitega kataloogilehele.

![Minu kontode leht kataloogilingiga.](./media/my-accounts.png)

### <a name="add-a-link-from-the-header"></a>Lingi lisamine päisest

Lõpuks lisage link oma saidi päisest kataloogi.

1. **Minge fragmentidesse**, otsige ja valige oma saidi päise tükk ning seejärel valige käsk **Redigeeri**.
1. Valige pesa **Päis**. 
1. Valige paani **Päise atribuudid jaotises Minu** konto lingid suvand **Lisa** tegevuslink **ja seejärel valige tegevuslink** **·**.
1. Sisestage **dialoogiakna** Tegevuslingi jaotises **Lingi tekst** kataloogi valija lehele lingi tekst.
1. Lingi **sihtmärgi all** valige **lisa link**.
1. Dialoogiaknas **Lingi lisamine** valige leht **Kohandatud ja** seejärel valige **edasi**.
1. Valige **jaotises** Nimi oma kataloogi valija lehekülg, valige Rakenda **ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige päise fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Järgmine näide näitab näidet e-poodide veebisaidi päise kohta lingiga B2B-kataloogile.

![Poodide veebisaidi päis koos kataloogi ripplingiga.](./media/catalog-in-header.png)


## <a name="additional-resources"></a>Lisaressursid 

[B2B-saitide Commerce'i kataloogide loomine](catalogs-b2b-sites.md)

[B2B-kohanduste Commerce'i kataloogide laiendatavus](catalogs-b2b-sites-dev.md)

[B2B-saitide Commerce'i kataloogide KKK](catalogs-b2b-sites-FAQ.md)

[Kontohalduse lehed ja moodulid](account-management.md)

[Päisemoodul](author-header-module.md)
