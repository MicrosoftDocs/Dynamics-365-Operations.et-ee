---
title: E-kaubanduse digitaalsed kinkekaardid
description: See teema kirjeldab, kuidas digitaalsed kinkekaardid e-kaubanduses Microsofti teenuse Dynamics 365 Commerce juurutamisel töötavad. Samuti antakse ülevaade olulistest konfigureerimisetappidest.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982662"
---
# <a name="e-commerce-digital-gift-cards"></a>E-kaubanduse digitaalsed kinkekaardid

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema kirjeldab, kuidas digitaalsed kinkekaardid e-kaubanduses Microsofti teenuse Dynamics 365 Commerce juurutamisel töötavad. Samuti antakse ülevaade olulistest konfigureerimisetappidest.

Teenuses Dynamics 365 Commerce järgib digitaalsete kinkekaartide ostmine sama voogu mis muude süsteemi toodete ostmine. Mingeid lisamooduleid ei ole vaja konfigureerida. Kui ostukorvi lisatakse mitu kinkekaarti, ei koondata kinkekaardikaubad ühele müügireale. Selline käitumine on vajalik, kuna iga müügirea arveldamiseks kasutatakse eraldi kinkekaardi numbrit.

Digitaalsete kinkekaartide ostmine on toetatud teenuse Dynamics 365 Commerce versioonis 10.0.16 ja uuemas versioonis.

Järgmisel joonisel on toodud näide toote üksikasjade lehest (PDP) digitaalse kinkekaardi puhul Fabrikami e-kaubanduse saidil.

![Digitaalse kinkekaardi PDP näide Fabrikami e-kaubanduse saidil](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Lülitage Commerce'i peakontoris digitaalse kinkekaardi funktsioon sisse

Selleks et digitaalsete kinkekaartide ostuvoog teenuses Dynamics 365 Commerce töötaks, tuleb Commerce'i peakontoris lülitada sisse funktsioon **E-kaubanduse funktsiooni kaudu kinkekaardi ostmine**. Funktsioon asub Commerce'i peakontori tööruumis **Funktsionihaldus**, nagu järgmisel joonisel näidatud.

![Funktsioonihalduse tööruum Commerce'i peakontoris](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Commerce'i peakontoris digitaalse kinkekaardi konfigureerimine

Digitaalsete kinkekaartide tooteid tuleb konfigureerida Commerce'i peakontoris. Protsess sarnaneb muude toodete protsessiga. Järgmised olulised etapid käsitlevad konkreetselt ostmiseks kasutatavate kinkekaartide konfiguratsiooni. Lisateavet toodete loomise ja konfigureerimise kohta vt teemast [Commerce'is uue toote loomine](create-new-product-commerce.md).

- Kui konfigureerite dialoogiboksis **Uus toode** digitaalsete kinkekaartide tooteid, määrake välja **Toote tüüp** väärtuseks **Teenus**. (Dialoogiboksi avamiseks minge lehele **Jaemüügi ja kaubandus \> Tooted ja kategooriad \> Tooted kategooriate alusel** ja valige **Uus**.) Tüübi **Teenus** tooteid ei kontrollita enne tellimuse esitamist saadaolevate varude suhtes. Lisateavet vt teemast [Uue toote loomine](create-new-product-commerce.md#create-a-new-product).
- Lehe **Kaubanduse parameetrid** vahekaardil **Sisestamine** peab väli **Kinkekaarditoode** olema seatud väärtusele **Digitaalne kinkekaart**, nagu järgmisel joonisel näidatud. Kui toode on väline kinkekaart, vaadake lisateavet teemast [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).

    ![Kinkekaarditoote väli Commerce'i peakontoris](./media/PostGiftcard.png)

- Kui kinkekaart peab toetama mitmeid eelmääratletud summasid (nt 25, 50 ja 100 $), tuleks nende eelmääratletud summade seadistamiseks kasutada dimensiooni **Suurus**. Iga eelmääratletud summa on variant. Lisateavet vt teemast [Toote dimensioonid](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).
- Kui kliendid peavad saama kinkekaardile kohandatud summat määrata, seadistage esmalt variant, mis lubab kasutada kohandatud summat. Seejärel avage toode lehel **Väljastatud tooted kategooriatena** ja määrake kiirkaardil **Kaubandus** välja **Hinna sisestamine** väärtuseks **Uue hinna sisestamine on kohustuslik**, nagu järgmisel joonisel näidatud. See seadistus tagab, et kliendid saavad PDP-s toote sirvimisel hinna sisestada.

    ![Hinna sisestamise väli Commerce'i peakontoris](./media/KeyInPrice.png)

- Digitaalse kinkekaardi tarneviisi väärtuseks peab olema määratud **Elektrooniline**. Valige lehe **Tarneviisid** (**Jaemüük ja kaubandus \> Kanali seadistus \> Tarneviisid**) loendipaanil tarneviis **Elektrooniline** ja seejärel lisage digitaalse kinkekaardi toode kiirkaardi **Tooted** ruudustikku, nagu järgmisel joonisel näidatud. Lisateavet vt teemast [Tarneviiside seadistamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Digitaalsete kinkekaartide tooted Commerce'i peakontori lehel Tarneviisid](./media/ElectronicMode.PNG)

- Veenduge, et Commerce'i peakontoris oleks loodud veebipõhine funktsiooniprofiil ja see oleks teie võrgupoega seostatud. Määrake funktsiooniprofiilil suvandi **Liida tooted** väärtuseks **Jah**. See seadistus tagab, et kõik kaubad peale kinkekaartide liidetakse. Lisateavet vt teemast [Veebipõhise funktsiooniprofiili loomine](online-functionality-profile.md).
- Kui soovite tagada, et kliendid saaksid pärast kinkekaardi arveldamist meili, looge lehel **Meiliteatiste profiilid** uus meiliteatise tüüp ja määrake välja **Meiliteatise tüüp** väärtuseks **Väljasta kinkekaart**. Lisateavet vt teemast [Meiliteatise profiili seadistamine](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Commerce'i saidiehitaja meediateeki tootepiltide lisamine

Commerce'i saidiehitaja meediateeki tuleb lisada digitaalsete kinkekaartide toodete jaoks tootepildid. Veenduge, et kinkekaartide pildifailide failinimed järgiks teie saidi tootepiltide nimemääramisreegleid. Lisateavet vt teemast [Piltide üleslaadimine](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Commerce'i saidiehitajas digitaalse kinkekaardi jaoks kohandatud summa konfigureerimine

Kui digitaalne kinkekaart on konfigureeritud lubama kohandatud summat, peab see käitumine olema lubatud ka [ostukasti moodulis](add-buy-box.md), mida kasutatakse teie saidi PDP-del. Ostukasti moodul toetab mooduli konfiguratsiooni kohandatud summade lubamiseks. Saate määrata ka kohandatud summade puhul lubatud miinimum- ja maksimumsummad.

Commerce'i saidiehitajas digitaalse kinkekaardi jaoks kohandatud summa konfigureerimiseks toimige järgmiselt.

1. Avage teie saidi PDP-del kasutatav ostukasti moodul. See ostuboksi moodul võib olla kasutusel fragmendis, mallis või lehel.
1. Valige suvand **Redigeeri**.
1. Valige parempoolsel atribuutide paanil märkeruut **Luba kohandatud hind**.
1. Valikuline: kohandatud summade miinimum- ja maksimumsummade määratlemiseks sisestage summad väljale **Miinimumhind** ja **Maksimumhind**.
1. Valige käsk **Lõpeta redigeerimine** ja seejärel käsk **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Ostukastimoodul](add-buy-box.md)

[Maksmismoodul](add-checkout-module.md)

[Ostukorvimoodul](add-cart-module.md)

[Uue toote loomine Commerce'is](create-new-product-commerce.md)

[Tarneviiside häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Tootedimensioonid](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[Meiliteatise profiili seadistamine](email-notification-profiles.md)

[Funktsiooniprofiili loomine võrgus](online-functionality-profile.md)

[Väliste kinkekaartide tugi](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]