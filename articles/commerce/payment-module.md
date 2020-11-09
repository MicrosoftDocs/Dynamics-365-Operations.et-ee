---
title: Maksemoodul
description: See teema hõlmab maksemoodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055377"
---
# <a name="payment-module"></a>Maksemoodul

[!include [banner](includes/banner.md)]

See teema hõlmab maksemoodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

## <a name="overview"></a>Ülevaade

Maksemoodul võimaldab klientidel tellimuste eest tasuda krediit-või deebetkaardiga. Selle mooduli puhul võimaldab makseintegratsiooni Dynamics 365 maksekonnektor Adyeni jaoks. Lisateavet maksekonnektori seadistamise ja konfigureerimise kohta leiate teemast [Dynamics 365 maksekonnektor Adyeni jaoks](dev-itpro/adyen-connector.md).

Maksemoodul majutab makseteavet, mida edastab Adyen HTML-i tekstisisese raami kaudu (iFrame). Maksemoodul suhtleb Adyeni makseteabe toomiseks Commerce Scale Unitiga. Commerce Scale Unitiga suhtlemise tõttu lubab maksemoodul esitada arveaadressi teavet nii iFrame'is kui ka eraldi moodulis. Fabrikami kujunduses kuvatakse arveaadress eraldi moodulis. Sellise meetodi puhul on vormindamine paindlikum, sest aadressiridu saab renderdada nii, et need sarnaneksid tarneaadressi ridadega.

Maksemoodul võimaldab ka sisselogitud klientidel oma makseteavet salvestada. Makseteavet ja arveaadressi salvestatakse ning hallatakse Adyeni maksekonnektori kaudu.

Maksemoodul hõlmab kõiki tellimuse tasusid, mis jäävad pärast boonuspunktide või kinkekaardi kasutamist alles. Kui tellimuse kogusumma eest saab tasuda täielikult boonuspunktide või kinkekaardi abil, siis on maksemoodul peidetud ja klient saab teha tellimuse ilma selleta.

Adyeni maksekonnektor toetab ka tugevat kliendi autentimist (SCA). Euroopa Liidu (EL) teise makseteenuste direktiivi (PSD2.0) järgi tuleb veebipoe külastajaid elektroonilise makseviisi kasutamise korral autentida väljaspool veebipoe keskkonda. Maksmisvoo ajal suunatakse kliendid nende pangasaidile. Seejärel suunatakse nad pärast autentimist tagasi Commerce'i maksmisvoogu. Tagasisuunamise ajal näidatakse teavet, mille klient maksmisvoos sisestas (nt tarneaadress, tarnevalikud, kinkekaardi- ja püsiklienditeave). Enne selle funktsiooni sisselülitamist peab maksekonnektor Commerce'i peakontoris SCA jaoks olema konfigureeritud. Lisateavet leiate teemast [Tugev kliendi autentimine Adyeni kaudu](adyen_redirect.md).

> [!NOTE]
> Adyeni maksekonnektori puhul saab maksemoodulis olevat moodulit iFrame renderdada ainult juhul, kui lisate Adyeni oma saidi lubatud URL-ide loendisse. Selle etapi lõpule viimiseks lisage **\*.adyen.com** oma saidi sisu turbepoliitika direktiividele **child-src** , **connect-src** , **img-src** , **script-src** ja **style-src**. Lisateavet leiate teemast [Sisu turbepoliitika haldamine](manage-csp.md). 

Järgmisel illustratsioonil on näide kinkekaardi, boonuspunktide ja maksemoodulitest maksmise lehel.

![Kinkekaardi, boonuspunktide ja maksemoodulite näide maksmise lehel](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Maksemooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri | Pealkirja tekst | Maksemooduli valikuline pealkiri. |
| IFrame'i kõrgus | Pikslid | IFrame'i kõrgus pikslites. Kõrgust saab vajaduse järgi reguleerida. |
| Kuva arveaadress | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene** , näitab Adyen arveaadressi maksemooduli iFrame'i sees. Kui selle väärtuseks on seatud **Väär** , ei näita Adyen arveaadressi ja Commerce'i kasutaja peab konfigureerima mooduli, et näidata maksmise lehel arveaadressi. |
| Makse stiili tühistamine | Kaskaadlaadistiku (CSS) kood | Kuna maksemoodulit majutatakse iFrame'is, on laadi muutmine piiratud. Selle atribuudi abil saate laadi veidi muuta. Saidi laadide alistamiseks peate kleepima CSS-koodi selle atribuudi väärtusena. Selle mooduli puhul ei rakendu saidiehitaja CSS-i alistused ja laadid. |

## <a name="billing-address"></a>Arveaadress

Maksemoodul võimaldab klientidel sisestada oma makseteabes arveaadressi. Samuti võimaldab see neil kasutada arveaadressina oma tarneaadressi, et muuta maksmisvoog lihtsamaks ja kiiremaks. Kui atribuudi **Näita arveaadressi** väärtuseks on seatud **Väär** , tuleb maksemoodul konfigureerida maksmise lehel.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksmise lehele maksemooduli lisamine ja vajalike atribuutide seadistamine

Maksemoodulit saab lisada ainult maksmise moodulisse. Lisateavet maksmise lehe jaoks maksemooduli konfigureerimise kohta leiate teemast [Maksmise moodul](add-checkout-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmise moodul](add-checkout-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnevalikute moodul](delivery-options-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardimoodul](add-giftcard.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](dev-itpro/adyen-connector.md)

[Tugev kliendi autentimine Adyeni kaudu](adyen_redirect.md)
