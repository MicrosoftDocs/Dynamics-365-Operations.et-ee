---
title: PayPali kiirmaksete konfigureerimine
description: See teema kirjeldab, kuidas konfigureerida PayPali kiirmakseid, et lubada kiiremaid väljaregistreerimise võimalusi Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5fff17959e7ed9299df169c68b2ed07f6b7c7d2c
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743597"
---
# <a name="configure-express-payments-for-paypal"></a>PayPali kiirmaksete konfigureerimine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas konfigureerida PayPali kiirmakseid, et lubada kiiremaid väljaregistreerimise võimalusi Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Põhimõisted

| Mõiste | Kirjeldus |
|---|---|
| PayPali väljaminek | Kliendikogemus ja integratsioon, mida PayPal Connector toetab. Seda nimetatakse ka PayPali nupuks. |
| Rahakott | Maksetüüp, mis ei sisalda traditsioonilisi makse omadusi nt panga ID-koodi (BIN) vahemikku ja aegumiskuupäeva, mida kasutatakse krediit- ja deebetkaardi tüüpide eristamiseks. |
| Kiirmakse | Commerce'i moodul, mis toetab toetatud makseviiside kasutamisel kiiremat väljaregistreerimise käitumist. See teema käsitleb PayPaliga kiirmakse kiirmooduli kasutamist. |

Dynamics 365 Commerce Rakendus <a0/& pakub väljaminekuvälist integratsiooni PayPal Karbi jaoks. Kui Dynamics 365 Payment Connector PayPali jaoks on konfigureeritud, kuvatakse PayPali nupp valitava makseviisina võrgutellimuse väljaregistreerimise ajal. Kui kasutajad valite PayPali, suunatakse nad oma makse otse PayPali kaudu lõpule viima ja seejärel tagastatakse e-poodi tellimuse lõpetamiseks. PayPali ostukorvi väljaregistreerimine, et kliendid saaksid kasutada oma maksekonto teavet väljaregistreerimise vormi eeltäitmiseks, et nad saaksid väljaregistreerimise protsessi kiiremini lõpule viia.

Commerce on kiirregistreerimise hõlbustamiseks lisanud kiirmakse kiirmooduli. Makse väljendamise moodulit saab kasutada killuss, mida saab kaasata väljaregistreerimise või ostukorvi lehele. Kui PayPal on konfigureeritud, kasutatakse sama Dynamics 365 Payment Connectorit PayPali konnektori viite jaoks nii kiirmakse valikus kui ka tavalises väljaregistreerimise suvandis.

## <a name="paypal-checkout-in-commerce"></a>PayPali väljaregistreerimine Commerce'i puhul

### <a name="prerequisites"></a>Eeltingimused

Seadistage PayPalPuhvri teie keskkonnas nii, nagu on kirjeldatud [Dynamics 365 Payment Connectoris PayPali jaoks](../paypal.md).

Kui kasutate PayPali tavalises väljaregistreerimise voos suvandina (kus kasutajad sisestavad käsitsi oma kontoteabe ilma makse väljendamise eeltäitmise tegevusi kasutamata), [järgige maksemooduli seadistusjuhiseid](../payment-module.md).

### <a name="payment-express-module-with-paypal"></a>Maksete kiirmoodul PayPaliga

Kiirmakse moodul töötab toetavate makseviisitega, et pakkuda saidi klientidele võimalust väljaregistreerida kiiremini, kui nad väljaregistreerimise protsessi käigus eeltäitvad oma makseteenuse konto teavet. Makse väljendamise moodul kasutab konfigureeritud makseühendust väljaregistreerimise vormi eeltäitmiseks kasutajakonto üksikasjadega, nagu aadress, kontaktteave ja valitud makseviis.

Kui kasutatakse PayPali kiirregistreerimist ja kasutaja valib väljaregistreerimise lehe makse kiir jaotises payPali, avaneb PayPali makseaken iFrame. Kasutaja allkirjastab siis oma PayPali kontole, et kasutada kande eest maksmiseks oma konto lähetusaadressi, arveaadressi, meiliaadressi ja PayPali makseviisi.

Kui kasutaja on tegevuse PayPali aknas lõpule jõudnud, suunatakse ta tagasi Commerce'i saidi väljaregistreerimise lehele, kus väljaregistreerimise vorm täidetakse eelnevalt valitud üksikasjadega. Makse kiirvoos täidetakse esimene tagastatud lähetusaadressil saadav tarnevalik kasutajale eeltäitmiseks. Kasutajal on seejärel võimalus tellimus üle vaadata ja muuta väljaregistreerimise tellimuse üksikasju enne **, kui nad valivad** Tellimuse lõplikuks muutmiseks koha.

### <a name="add-the-payment-express-module-with-paypal-to-a-fragment"></a>PayPaliga makse väljendamise mooduli lisamine killusta

Maksete väljendamise mooduli lisamiseks PayPaliga Commerce'i saidilooja killus, järgige neid samme.

1. Liikuge oma saidile.
1. Valige vasakpoolsel navigeerimispaanil tükid **ja** seejärel väärtus **Uus**.
1. Dialoogiboksis Uus **tükk** leidke **·** **ja** valige makse väljendamismoodul ning seejärel sisestage killu jaoks nimi (**nt Kiirväljaregistreerimine).**
1. **Tüki loomiseks valige OK**.
1. Valige liigendusvaates loodud makse kiirmooduli pesa.
1. Valige atribuutide paanil **Pealkiri**.
1. **Sisestage** dialoogiboksi Pealkiri tekstiväljale **pealkirja** tekst, mida soovite oma saidi kiirväljaregistreerimise jaotises kuvada (nt **Kiirväljaregistreerimine**).
1. Valige **jaotises Pealkiri** taseme tase (nt **H2**).
1. Valige nupp **OK**.
1. Sisestage või korrigeerige **elemendi kõrgust iFrame** iFrame atribuutide paanil välja kõrgus (nt **60**).
1. Väljal Toetatud **maksevahendi** tüübid sisestage **PayPal**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Makse väljendamise killu lisamine väljaregistreerimise lehele

Makse väljendamise killu lisamiseks väljaregistreerimise leheküljele saidi koostajas, järgige neid samme.

1. Liikuge oma saidile.
1. Valige vasakul navigeerimispaanil **Lehed** ja seejärel valige oma saidi väljaregistreerimise lehekülg.
1. Lehe **redigeerimiseks** klõpsake nuppu Redigeeri.
1. Valige põhipesas **kolmikpunkt** (**...**) ja seejärel valige käsk **Lisa moodul**.
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.

    > [!NOTE]
    > Kui konteinerimoodul, mis sisaldab väljaregistreerimise killust, on juba olemas, teisaldage maksete väljendamise sektsioon nii, **et see ilmub olemasolevast väljaregistreerimise konteinerist põhipesas**. Seejärel renderdatakse maksete väljendamise sektsioon tavalisest väljaregistreerimise konteinerist ülalpool. Konteinerimooduli liigutamiseks üles või alla valige kolmikpunkt (**...**) ja seejärel valige Nihuta **üles või** Nihuta **alla**.

1. Konteineri **atribuutide** paanil on soovitatav konfigureerida atribuudi sätted järgmisel viisil:

    - **Konteineri** paigutus – valige **virnastatud**.
    - **Laius**: valige **täitekonteiner**.
    - **Kuvatud last** – valige **kolm**.

1. **Valige konteineri** pesast kolmikpunkt (**...**) ja seejärel valige käsk Lisa **kill.**
1. **Dialoogiboksis Tükimakse valimine** leidke ja valige loodud kiirmakse killus ning seejärel valige **OK**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Makse väljendamise killu lisamine ostukorvi lehele

Makse väljendamise killu lisamiseks saidi koostaja ostukorvi lehele, järgige neid samme.

1. Liikuge oma saidile.
1. Valige vasakul navigeerimispaanil **Lehed** ja seejärel valige oma saidi ostukorvi lehekülg.
1. Lehe **redigeerimiseks** klõpsake nuppu Redigeeri.
1. Leidke põhipesast **ostukorvi** moodulit sisaldav **konteiner**. Ostukorvi **moodul** sisaldab makse väljendamise **pesa**.
1. **Valige Payment Expressi** pesa, valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige makse kiirmoodul **ja** seejärel valige **OK**.
1. Sisestage atribuutide paani väljale Toetatud **maksevahendi** tüübid väärtus **Paypal**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="modes-of-delivery"></a>Tarneviisid

Kui makse väljendamise moodul on konfigureeritud Kasutama PayPali, eeltäittakse esimene tarnevõimalus, mis tagastatakse PayPal-konto jaoks valitud lähetusaadressi puhul. Kasutajad saavad soovi korral tarneaadressi muuta.

Tarneviisi järjestus on konfigureeritud **Commerce headquartersi** kanali jaotises Tarneviisid. Lisateavet vt teemast [Tarneviiside seadistamine](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Väljaregistreerimise moodul kasutab ka tarnesuvandite moodulit, kui tarneviisid renderdatakse väljaregistreerimise ajal. Lisateavet vt tarnesuvandite [moodulist](../delivery-options-module.md).

Tarneviisid lisatakse commerce headquartersi e-poe loendisse. Minge jaemüügi **ja ärikanalite \> võrgupoodidesse \>** ja valige oma kaupluse kanali ID. Seejärel valige **seadistuse \> tarneviisid**. Konfiguratsioonis näidatud tarnemooduli režiimid ilmuvad saidil sarnasel viisil. Jaemüügikanali või toote tarneviiside lisamiseks või eemaldamiseks valige **tegevuspaanil suvand** Tarneviiside haldamine.

## <a name="additional-resources"></a>Lisaressursid

[Maksete KKK](payments-retail.md)

[Maksmismoodul](../add-checkout-module.md)

[Maksemoodul](../payment-module.md)

[Tarneviiside häälestamine](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Tarnesuvandite moodul](../delivery-options-module.md)
