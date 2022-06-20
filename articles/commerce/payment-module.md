---
title: Maksemoodul
description: See artikkel katab maksemooduli ja selgitab selle konfigureerimist moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89ca5dd4f46611e75faccd3213028750fa48d35
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850271"
---
# <a name="payment-module"></a>Maksemoodul

[!include [banner](includes/banner.md)]

See artikkel katab maksemooduli ja selgitab selle konfigureerimist moodulis Microsoft Dynamics 365 Commerce.

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

![Kinkekaardi, boonuspunktide ja Adyen`i maksemoodulite näide maksmise lehel.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector PayPali jaoks

Alates Commerce'i versioonist 10.0.14 integreeriti maksemoodul ka Dynamics 365 PayPali maksekonnektoriga. Lisateavet selle maksekonnektori häälestamise ja konfigureerimise kohta leiate teemast [Dynamics 365 maksekonnektor PayPali jaoks](paypal.md).
 
Maksmise lehel võivad olla konfigureeritud nii Adyeni kui ka PayPali konnektorid. Maksemoodulit on täiustatud lisaatribuutidega, et teha kindlaks, millise konnektoriga see peaks töötama. Üksikasju vaadake järgmises tabelis toetatud **maksevahendi** **tüüpidest ja** mooduli On esmane maksemoodul atribuutidest.
  
Kui maksemoodul on konfigureeritud kasutama PayPali maksekonnektorit, kuvatakse maksmise lehel PayPali nupp. Maksemoodul renderdab PayPali teabega IFrame'i, kui klient selle käivitab. Klient saab oma tehingu lõpuleviimiseks sisse logida ja esitada selle IFrame'i kaudu oma PayPali teabe. Kui klient otsustab tasuda PayPali abil, võetakse tellimuse jääksumma PayPali kaudu.

PayPali maksekonnektor ei nõua arveldusaadressi moodulit, kuna kogu arveldusega seotud teavet käsitletakse PayPali oma IFrame'is. Siiski on vaja saatmisaadressi ja tarnevalikute mooduleid.

Järgmisel joonisel on kujutatud näide kahest maksemoodulist maksmise lehel, millest üks on konfigureeritud Adyeni maksekonnektoriga ja teine PayPali maksekonnektoriga.
![Adyen`i makse ja PayPali maksemoodulite näide maksmise lehel.](./media/ecommerce-paypal.png)

Järgmisel joonisel on toodud näide PayPal IFrame'ist, mida käivitatakse PayPali nupu abil. 
![Näide Paypali IFrame'ist maksmise lehel.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Maksemooduli atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pealkiri | Pealkirja tekst | Maksemooduli valikuline pealkiri. |
| IFrame'i kõrgus | Pikslid | IFrame'i kõrgus pikslites. Kõrgust saab vajaduse järgi reguleerida. |
| Kuva arveaadress | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, näitab Adyen arveaadressi maksemooduli iFrame'i sees. Kui selle väärtuseks on määratus **Väär**, ei näita Adyen arveaadressi ja Commerce'i kasutaja peab konfigureerima mooduli, et näidata maksmise lehel arveaadressi. PayPali maksekonnektorit see väli ei mõjuta, kuna arveldusaadressi käsitletakse täielikult PayPali kaudu. |
| Makse stiili tühistamine | Kaskaadlaadistiku (CSS) kood | Kuna maksemoodulit majutatakse iFrame'is, on laadi muutmine piiratud. Selle atribuudi abil saate laadi veidi muuta. Saidi laadide alistamiseks peate kleepima CSS-koodi selle atribuudi väärtusena. Selle mooduli puhul ei rakendu saidiehitaja CSS-i alistused ja laadid. |
|Toetatud maksevahendi tüübid| String| Kui on konfigureeritud mitu makseühendust, peate andma toetatud maksevahendi tüübi stringi, nagu on määratletud Commerce headquartersi maksekonnektori konfiguratsioonis (vt järgmist pilti). Kui see on tühi, määratakse vaikimisi Adyeni maksekonnektor. Lisatud Commerce'i väljalaskesse 10.0.14.|
|On esmane makse|  **Tõene** või **Väär** | Kui see on **Tõene**, koostatakse tõrketeated maksmise lehel esmase maksekonnektori põhjal. Kui Aydeni ja PayPali maksekonnektorid on konfigureeritud, määrake Adyeni väärtuseks **Tõene**, mis lisati Commerce'i versioonis 10.0.14.|
|Kasuta konnektori ID-d| **Tõene** või **Väär** | Kasutage seda atribuuti, kui saidile on konfigureeritud mitu makseühendust. Kui **see** on tõene, peavad konnektorid kasutama maksete korrelatsiooniks konnektori ID-d.|
|Kasuta brauserikomplekti keelekoodi <a0/& jaoks iFrame|  **Tõene** või **Väär** | (Ainult Omaen) Kui **see** on tõene, renderdab Portaal iFrame keele saidi kasutaja brauserikonteksti alusel, selle asemel et kasutada saidi jaoks konfigureeritud Ärikanali keelekoodi. Lisatud Commerce'i väljalaskesse 10.0.27.|

Järgmisel joonisel on kujutatud näide, kus atribuudi **Toetatud maksevahenditüübid** jaoks on määratud väärtus „PayPal“ Commerce'i peakontori maksekonnektori konfiguratsioonis.
![Commerce'i peakontori toetatud maksevahenditüüpide näide.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Arveldusaadress

Arveldusaadressi moodulit saab kasutada maksmise lehel, kui Adyeni maksekonnektori arveldusaadressi read ei vasta piisavalt ülejäänud saidi välimusele. 

Arveldusaadressi mooduli kasutamiseks maksmise lehel, kui maksemoodul on integreeritud Adyeni maksekonnektoriga, määrake atribuudi **Kuva arveldusaadress** väärtuseks **Väär**, et Adyeni vaike-arveldusaadressi asemel saaks kasutada spetsiaalset arveldusaadressi moodulit. Sel juhul peaks saidi autor kaasama arveldusaadressi mooduli maksmise lehel. Adyeni maksekonnektor võimaldab ka saatmisaadressi arveldusaadressina kasutada, et vähendada saidi kasutaja tehtavate toimingute arvu.

Sarnaselt maksemoodulitele lisati Commerce'i versioonis 10.0.14 arveldusaadressi moodulile atribuut **Toetatud maksevahenditüübid**. Selle atribuudi väärtus peaks olema identne maksemoodulis esitatud väärtusega, et tagada nende koostoimimine. Adyeni maksekonnektori, maksemooduli ja arveldusaadressi mooduli korral peaks selle väärtuse tühjaks jätma (vaikimisi olek). PayPali konnektori jaoks pole vaja spetsiaalset arveldusaadressi moodulit. Muud tüüpi maksekonnektorite korral tuleks string Commerce'i peakontoris konfigureerituna esitada.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Maksmise lehele maksemooduli lisamine ja vajalike atribuutide seadistamine

Maksemoodulit saab lisada ainult maksmise moodulisse. Lisateavet maksmise lehe jaoks maksemooduli konfigureerimise kohta leiate teemast [Maksmise moodul](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Konfigureerige Puhvri ja PayPali makseühendused, kui mõlemat kasutatakse

Kui teie saidi jaoks kasutatakse nii Puhvri kui ka PayPali makseühendusi, järgige commerce'i saidikonstruktoris neid samme iga konnektori maksemoodulite lisamiseks väljaregistreerimise moodulile ja seejärel konfigureerige atribuudid iga mooduli jaoks.

1. PayPal maksemooduli atribuutide paanil järgige neid samme.

    1. Sisestage toetatud maksevahendi **tüüpide atribuudi** väljale **PayPal**.
    1. Tühjendage ruut peamise makse **atribuudi** jaoks.
    1. Märkige ruut atribuudi Kasuta konnektori **ID jaoks**.

1. Maksemooduli Korrake atribuutide paanil järgmisi samme.

    1. Jätke toetatud maksevahendi **tüüpide atribuudi väli** tühjaks.
    1. Märkige ruut peamise makse **atribuudi** jaoks.
    1. Märkige ruut atribuudi Kasuta konnektori **ID jaoks**.

> [!NOTE]
> Kui konfigureerite Puhvri ja PayPali konnektorid nii, et neid koos kasutatakse, **peab Dynamics 365 Payment Connector Puhvri konfiguratsioonile** **olema** võrgukanali Maksekontode konnektori konfiguratsioonis Commerce headquartersis esimene positsioon. Konnektori tellimuse kinnitamiseks või muutmiseks minge võrgupoodidesse **ja** valige oma saidi kanal. **Seejärel** veenduge konnektori all maksekontode kiirkaardi vahekaardil Seadistamine, **·** **et Dynamics 365 Maksekonnektor Omakonfiguratsioon** on **esimeses** positsioonis (st ülemisel real) **ja Et Dynamics 365 Payment Connector PayPali** konfiguratsiooni jaoks on teisel real. Lisage konnektorid ümberjärjesaamiseks vastavalt vajadusele või eemaldage need.

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
