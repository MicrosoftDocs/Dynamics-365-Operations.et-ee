---
title: Maksemoodul
description: See teema hõlmab maksemoodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 85b5d8306eb4e9f2a4b9df13d95ab88020c3591e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000661"
---
# <a name="payment-module"></a>Maksemoodul

[!include [banner](includes/banner.md)]

See teema hõlmab maksemoodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.

Maksemoodul võimaldab klientidel tellimuste eest tasuda krediit-või deebetkaardiga. Selle mooduli puhul võimaldab makseintegratsiooni Dynamics 365 maksekonnektor Adyeni jaoks. Lisateavet maksekonnektori seadistamise ja konfigureerimise kohta leiate teemast [Dynamics 365 maksekonnektor Adyeni jaoks](dev-itpro/adyen-connector.md).  

Alates Commerce'i versioonist 10.0.14 integreeriti maksemoodul ka Dynamics 365 PayPali maksekonnektoriga, et võimaldada klientidel maksta tellimuste eest PayPali kasutades. Lisateavet Dynamics 365 PayPali maksekonnektori häälestamise ja konfigureerimise kohta leiate teemast [Dynamics 365 maksekonnektor PayPali jaoks](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365 maksekonnektor Adyeni jaoks 

Maksemoodul majutab makseteavet, mida edastab Adyen HTML-i tekstisisese raami kaudu (iFrame). Maksemoodul suhtleb Adyeni makseteabe toomiseks Commerce Scale Unitiga. Commerce Scale Unitiga suhtlemise tõttu lubab maksemoodul esitada arveaadressi teavet nii Aydeni kaudu iFrame'is kui ka eraldi moodulis. Fabrikami kujunduses lubatakse arveaadress eraldi moodulis. Sellise meetodi puhul on vormindamine paindlikum, sest aadressiridu saab renderdada nii, et need sarnaneksid tarneaadressi ridadega.

Maksemoodul võimaldab ka sisselogitud klientidel oma makseteavet salvestada. Makseteavet ja arveaadressi salvestatakse ning hallatakse Adyeni maksekonnektori kaudu.

Maksemoodul hõlmab kõiki tellimuse tasusid, mis jäävad pärast boonuspunktide või kinkekaardi kasutamist alles. Kui tellimuse kogusumma eest saab tasuda täielikult boonuspunktide või kinkekaardi abil, siis on maksemoodul peidetud ja klient saab teha tellimuse ilma selleta.

Adyeni maksekonnektor toetab ka tugevat kliendi autentimist (SCA). Euroopa Liidu (EL) muudetud makseteenuste direktiivi (PSD2) järgi tuleb veebipoe külastajaid elektroonilise makseviisi kasutamise korral autentida väljaspool veebipoe keskkonda. Maksmisvoo ajal suunatakse kliendid nende pangasaidile ja seejärel pärast autentimist suunatakse nad tagasi Commerce'i maksmisvoole. Tagasisuunamise ajal näidatakse teavet, mille klient maksmisvoos sisestas (nt tarneaadress, tarnevalikud, kinkekaardi- ja püsiklienditeave). Enne Aydeni maksekonnektori funktsiooni sisselülitamist peab maksekonnektor Commerce'i peakontoris SCA jaoks olema konfigureeritud. Lisateavet leiate teemast [Tugev kliendi autentimine Adyeni kaudu](adyen_redirect.md). See funktsioon lubati Commerce'i versioonis 10.0.12.

> [!NOTE]
> Adyeni maksekonnektori puhul saab maksemoodulis olevat moodulit iFrame renderdada ainult juhul, kui lisate Adyeni oma saidi lubatud URL-ide loendisse. Selle etapi lõpule viimiseks lisage **\*.adyen.com** oma saidi sisu turbepoliitika direktiividele **child-src**, **connect-src**, **img-src**, **script-src** ja **style-src**. Lisateavet leiate teemast [Sisu turbepoliitika haldamine](manage-csp.md). 

Järgmisel illustratsioonil on näide kinkekaardi, boonuspunktide ja Aydeni maksemoodulitest maksmise lehel.

![Kinkekaardi, boonuspunktide ja Adyeni maksemoodulite näide maksmise lehel](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 maksekonnektor PayPali jaoks

Alates Commerce'i versioonist 10.0.14 integreeriti maksemoodul ka Dynamics 365 PayPali maksekonnektoriga. Lisateavet selle maksekonnektori häälestamise ja konfigureerimise kohta leiate teemast [Dynamics 365 maksekonnektor PayPali jaoks](paypal.md).
 
Maksmise lehel võivad olla konfigureeritud nii Adyeni kui ka PayPali konnektorid. Maksemoodulit on täiustatud lisaatribuutidega, et teha kindlaks, millise konnektoriga see peaks töötama. Lisateavet leiate järgmisest tabelitest atribuutide **Toetatud maksevahenditüübid** ja **On peamine makseviis** alt.
  
Kui maksemoodul on konfigureeritud kasutama PayPali maksekonnektorit, kuvatakse maksmise lehel PayPali nupp. Maksemoodul renderdab PayPali teabega IFrame'i, kui klient selle käivitab. Klient saab oma tehingu lõpuleviimiseks sisse logida ja esitada selle IFrame'i kaudu oma PayPali teabe. Kui klient otsustab tasuda PayPali abil, võetakse tellimuse jääksumma PayPali kaudu.

PayPali maksekonnektor ei nõua arveldusaadressi moodulit, kuna kogu arveldusega seotud teavet käsitletakse PayPali oma IFrame'is. Siiski on vaja saatmisaadressi ja tarnevalikute mooduleid.

Järgmisel joonisel on kujutatud näide kahest maksemoodulist maksmise lehel, millest üks on konfigureeritud Adyeni maksekonnektoriga ja teine PayPali maksekonnektoriga.
![Kinkekaardi, boonuspunktide ja PayPali maksemoodulite näide maksmise lehel](./media/ecommerce-paypal.png)

Järgmisel joonisel on toodud näide PayPal IFrame'ist, mida käivitatakse PayPali nupu abil. 
![Näide Paypali IFrame'ist maksmise lehel](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Maksemooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri | Pealkirja tekst | Maksemooduli valikuline pealkiri. |
| IFrame'i kõrgus | Pikslid | IFrame'i kõrgus pikslites. Kõrgust saab vajaduse järgi reguleerida. |
| Kuva arveaadress | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, näitab Adyen arveaadressi maksemooduli iFrame'i sees. Kui selle väärtuseks on määratus **Väär**, ei näita Adyen arveaadressi ja Commerce'i kasutaja peab konfigureerima mooduli, et näidata maksmise lehel arveaadressi. PayPali maksekonnektorit see väli ei mõjuta, kuna arveldusaadressi käsitletakse täielikult PayPali kaudu. |
| Makse stiili tühistamine | Kaskaadlaadistiku (CSS) kood | Kuna maksemoodulit majutatakse iFrame'is, on laadi muutmine piiratud. Selle atribuudi abil saate laadi veidi muuta. Saidi laadide alistamiseks peate kleepima CSS-koodi selle atribuudi väärtusena. Selle mooduli puhul ei rakendu saidiehitaja CSS-i alistused ja laadid. |
|Toetatud maksevahendi tüübid| String| Mitme maksekonnektori konfigureerimise korral peaksite sisestama toetatud maksevahendi tüübi stringi, nagu on määratletud Commerce'i peakontori maksekonnektor konfiguratsioonis (vt järgmist pilti). Kui see on tühi, määratakse vaikimisi Adyeni maksekonnektor. Lisatud Commerce'i väljalaskesse 10.0.14.|
|On esmane makse|  **Tõene** või **Väär** | Kui see on **Tõene**, koostatakse tõrketeated maksmise lehel esmase maksekonnektori põhjal. Kui Aydeni ja PayPali maksekonnektorid on konfigureeritud, määrake Adyeni väärtuseks **Tõene**, mis lisati Commerce'i versioonis 10.0.14.|

Järgmisel joonisel on kujutatud näide, kus atribuudi **Toetatud maksevahenditüübid** jaoks on määratud väärtus „PayPal“ Commerce'i peakontori maksekonnektori konfiguratsioonis.
![Commerce'i peakontori toetatud maksevahenditüüpide näide](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Arveldusaadress

Arveldusaadressi moodulit saab kasutada maksmise lehel, kui Adyeni maksekonnektori arveldusaadressi read ei vasta piisavalt ülejäänud saidi välimusele. 

Arveldusaadressi mooduli kasutamiseks maksmise lehel, kui maksemoodul on integreeritud Adyeni maksekonnektoriga, määrake atribuudi **Kuva arveldusaadress** väärtuseks **Väär**, et Adyeni vaike-arveldusaadressi asemel saaks kasutada spetsiaalset arveldusaadressi moodulit. Sel juhul peaks saidi autor kaasama arveldusaadressi mooduli maksmise lehel. Adyeni maksekonnektor võimaldab ka saatmisaadressi arveldusaadressina kasutada, et vähendada saidi kasutaja tehtavate toimingute arvu.

Sarnaselt maksemoodulitele lisati Commerce'i versioonis 10.0.14 arveldusaadressi moodulile atribuut **Toetatud maksevahenditüübid**. Selle atribuudi väärtus peaks olema identne maksemoodulis esitatud väärtusega, et tagada nende koostoimimine. Adyeni maksekonnektori, maksemooduli ja arveldusaadressi mooduli korral peaks selle väärtuse tühjaks jätma (vaikimisi olek). PayPali konnektori jaoks pole vaja spetsiaalset arveldusaadressi moodulit. Muud tüüpi maksekonnektorite korral tuleks string Commerce'i peakontoris konfigureerituna esitada.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksmise lehele maksemooduli lisamine ja vajalike atribuutide seadistamine

Maksemoodulit saab lisada ainult maksmise moodulisse. Lisateavet maksmise lehe jaoks maksemooduli konfigureerimise kohta leiate teemast [Maksmise moodul](add-checkout-module.md).

Kui on vaja nii Adyeni kui ka PayPali maksekonnektoreid, lisage maksejaotisse mõlemad moodulid. Veenduge, et atribuudi **Toetatud maksevahenditüübid** on PayPali jaoks konfigureeritud ja jätke see Adyeni jaoks tühjaks. Lisaks määrake Aydeni korral atribuudi **On peamine makseviis** väärtuseks **Tõene**.

## <a name="additional-resources"></a>Lisaressursid

[Ostukorvimoodul](add-cart-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Maksmismoodul](add-checkout-module.md)

[Tarneaadressi moodul](ship-address-module.md)

[Tarnesuvandite moodul](delivery-options-module.md)

[Järeletulemise teabe moodul](pickup-info-module.md)

[Tellimuse üksikasjade moodul](order-confirmation-module.md)

[Kinkekaardi moodul](add-giftcard.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](dev-itpro/adyen-connector.md)

[Dynamics 365 maksekonnektor PayPali jaoks](paypal.md)

[Tugev kliendi autentimine Adyeni kaudu](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]