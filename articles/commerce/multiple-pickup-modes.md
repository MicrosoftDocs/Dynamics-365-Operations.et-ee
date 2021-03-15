---
title: Klienditellimuste korral mitme järeletulemisega tarneviisi lubamine
description: Selles teemas selgitatakse Microsoft Dynamics 365 Commerce'i funktsioone, mis võimaldavad teil luua klienditellimusi, mille korral saab kaubale poodi järele tulla.
author: hhainesms
manager: annbe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c0879343f100fa1fe6e0a4b4fbf085574225e898
ms.sourcegitcommit: bea695707d1e7b4e2713b62405ad0e7a7a893420
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/22/2021
ms.locfileid: "5053409"
---
# <a name="enable-multiple-pickup-delivery-modes-for-customer-orders"></a>Klienditellimuste korral mitme järeletulemisega tarneviisi lubamine

[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce'i versioonis 10.0.16 ja uuemates versioonides saavad organisatsioonid määratleda mitu tarneviisi, mille vahel ostjad või müügipartnerid saavad valida, kui nad loovad tellimuse, millele poodi järele tullakse. Sel viisil saavad organisatsioonid pakkuda oma ostjatele mitut järeletulemisvõimalust. Näiteks pakuvad paljud jaemüüjad ostjatele nüüd võimalust tulla oma tellimusele järele poodi või see peale võtta. Commerce toetab nende erinevate järeletulemisega tarneviiside konfigureerimist. Kasutajad saavad neid siis ära kasutada, kui nad loovad klienditellimusi mis tahes toetatud Commerce'i kanalis (e-kaubandus, kõnekeskus või pood).

## <a name="enable-and-configure-pickup-delivery-modes"></a>Järeletulemisega tarneviiside lubamine ja konfigureerimine

Selle funktsiooni kasutamiseks lülitage Commerce'i peakontoris tööruumis **Funktsioonihaldus** sisse funktsioon **Mitme järeletulemisega tarneviisi tugi**. Pärast funktsiooni sisselülitamist on vajalik täiendav konfiguratsioon.

Commerce'i versioonis 10.0.15 ja varasemates versioonides saavad organisatsioonid määratud järeletulemisega tarneviisiks määrata ainult ühe tarneviisi. Seda määratakse lehel **Kaubandusparameetrid**. Versioonis 10.0.16 ja uuemates versioonides, kui lülitate sisse funktsiooni **Mitme järeletulemisega tarneviisi tugi**, kopeeritakse tarneviis, mis oli eelnevalt määratletud järeletulemisega tarneviisina lehel **Kaubandusparameetrid**, automaatselt järeletulemisega tarneviiside uude konfiguratsiooni.

![Järeletulemisega tarneviisid lehel Kaubandusparameetrid](media/multiplepickupparameter.png)

Pärast funktsiooni **Mitme järeletulemisega tarneviisi tugi** sisselülitamist saate lehe **Kaubandusparameetrid** vahekaardil **Klienditellimused** kiirkaardi **Tarneviisid** ruudustikus **Järeletulemisega tarneviis** määrata mitu tarneviisi.

Sellele kiirkaardile on ümber paigutatud väli **Järeletulemisega tarneviis** ja **Elektrooniline tarneviis** ning suvand **Kuva tellimuste lähetamiseks ainult vedajarežiimi valikud**.

Enne täiendavate järeletulemisega tarneviiside konfigureerimist peate tarneviisid määratlema. Lisage Commerce'i peakontoris lehel **Tarneviisid** need tarneviisid, mida tuleks pidada järeletulemisega tarneviisiks. Veenduge, et kogu konfigureerimine on lõpule viidud. Näiteks veenduge, et tarneviis oleks lingitud sobivate kanalite ja üksustega. Kui olete lõpetanud, käivitage töö **Tarneviiside töötlus**, et luua tarneviisi, kanalite ja üksuste vahelised seosed. Kui töö lõpule viidud, avage Commerce'i peakontoris leht **Jaotusgraafik** ja käivitage jaotustöö **1120**, et tagada vastavate Commerce'i kanali andmebaaside värskendamine vastavalt uue tarneviisi konfiguratsioonile.

![Näide pealevõtmisega tarneviisi konfigureerimisest](media/pickupmodes.png)

Pärast täiendavate järeletulemisega tarneviiside määratlemist saate need lisada lehel **Kaubandusparameetrid** ruudustikus **Järeletulemisega tarneviis**. Seejärel käivitage asjakohased jaotustööd, et värskendada vastavaid Commerce'i kanali andmebaase konfiguratsioonimuudatusega.

> [!NOTE]
> Peale olemasoleva järeletulemisega tarneviisi, mis kopeeritakse ruudustikku **Järeletulemisega tarneviis**, kui lülitate sisse funktsiooni **Mitme järeletulemisega tarneviisi tugi**, peaksite iga loodava järeletulemisega tarneviisi konfiguratsiooni korral konfigureerima uued tarneviisid. Tarneviiside lisamisel ruudustikku **Järeletulemisega tarneviis** kinnitab Commerce, kas neid juba kasutatakse mõnel aktiivsel avatud müügireal. Kui leitakse avatud müügiridu, kuvatakse tõrketeade. Tarneviise ei loeta järeletulemisega tarneviisideks enne, kui kõik neid kasutavad avatud müügiread on suletud (arveldatud või tühistatud).

> [!IMPORTANT]
> Pärast seda, kui määratlete rohkem kui ühe järeletulemisega tarneviisi lehel **Commerce'i parameetrid** muutub funktsioon **Mitme järeletulemisega tarneviisi tugi** nõutavaks ja seda ei saa enam välja lülitada. Kui peate funktsiooni välja lülitama, eemaldage ruudustikust **Järeletulemisega tarneviisid** kõik peale ühe järeletulemisega tarneviisi. Kui määratletud on ainult üks järeletulemisega tarneviis, ei peeta seda funktsiooni enam nõutavaks ja selle saab välja lülitada.

### <a name="e-commerce-site-configurations"></a>E-kaubanduse saidi konfiguratsioonid

Kui funktsioon **Mitme järeletulemisega tarneviisi tugi** on sisse lülitatud, kuvatakse e-kaubanduse lehtedel järgmistes moodulites uued järeletulemisega tarneviisid konfigureerituna.

- Ostuväli
- Kauplusevalija
- Ostukorv
- Pealevõtmise teave
- Tellimuse kinnitus
- Tellimuse üksikasjad

Järeletulemisega tarneviisi kättesaadavaks tegemiseks ei ole e-kaubanduse lehtedel vaja teha lisatoiminguid.

## <a name="work-with-multiple-pickup-delivery-modes"></a>Mitme järeletulemisega tarneviisiga töötamine

Kui kanali jaoks on saadaval mitu järeletulemisega tarneviisi, pakutakse klientidele täiustatud kasutuskogemust, kui ostetakse tooteid, millele järele tullakse. 

- E-kaubanduse kanalite korral saavad ostjad valida mis tahes kehtiva järeletulemisega tarneviisi, mis on saadaval. Näiteks on jaemüüja määratlenud kaks järeletulemisega tarneviisi (poodi järeletulemine ja pealevõtmine), mõlemad on konfigureeritud ruudustikus **Järeletulemisega tarneviis** ning mõlemad kehtivad tellimuse täitmise kanali ja toote kohta, mida ostja praegu ostab. Sellisel juhul saab ostja valida oma eelistatud järeletulemisega tarneviisi. Valitud järeletulemisega tarneviis muutub siis müügitellimuse reaga lingitud tarneviisiks, kui tellimus luuakse Commerce'i peakontoris.

    ![Järeletulemisega tarneviisi valimine e-kaubanduses](media/pickupecommerce.png)

- Kui kliendi järeletulemisega tellimus koostatakse müügipunkti (kassa) rakenduse kaudu, palutakse müügiesindajal poe kanalite korral valida mõni saadaolev järeletulemisega tarneviis, kui see on konfigureeritud. Kui kanali ja kauba jaoks on saadaval ainult üks kehtiv järeletulemisega tarneviis, ei paluta müügiesindajal seda valida. Selle asemel rakendatakse saadaolev järeletulemisega tarneviis automaatselt tellimuse ridadele.

    ![Järeletulemisega tarneviisi kassarakenduses](media/pickuppos.png)

- Kõnekeskuse kanalites, kui kasutajad loovad järeletulemisega tellimusi, saavad nad käsitsi valida mis tahes määratletud järeletulemisega tarneviisi, mis on seotud kõnekeskuse kanaliga. Seejärel kinnitab süsteem, kas valitud järeletulemisega tarneviisi saab kasutada siis, kui kaup, millega see on seotud, on tellitud. Kui kõnekeskuse kanalites valitakse järeletulemisega tarneviis, peavad müügitellimuse read olema lingitud kehtiva kaupluse laoga. Kui kõnekeskuse müügireal määratleti ladu, mis pole pood, ei saa sellele müügireale määrata järeletulemisega tarneviisi.
- Müügiesindajad saavad tellimuste või järeletulemisega tellimuse ridade hankimiseks kasutada kassarakenduses toimingut **Tellimuse tagasikutsumine** või **Tellimuse täitmine**. Kui müügiesindaja kasutab eelmääratletud filtrit, et kuvada kõik tellimused, millele praegusesse poodi järele tullakse, muudetakse päringuid tagamaks, et otsingutulemused hõlmaksi kõiki järeletulemisega tarneviisi kasutavaid tingimustele vastavaid tellimusi. Kassa kasutajad saavad kasutada ka olemasolevaid filtreid, et lühendada konkreetse järeletulemisega tarneviisi korral tellimuste loendit. Näiteks saavad nad näidata ainult tellimusi, kus tarneviisiks on pealevõtmine.

    ![Tagasikutsutud tellimuste loendile rakendatud järeletulemisega tarneviiside filter](media/pickuprecallorder.png)

## <a name="considerations-for-distributed-order-management"></a>Hajutatud tellimuste haldamisega seotud kaalutlused

Commerce'i [hajutatud tellimuste haldamise (DOM)](https://docs.microsoft.com/dynamics365/commerce/dom) funktsioonidega ignoreeritakse müügiridu, mis on märgitud poodi järeletulemiseks. Neid funktsioone värskendati tagamaks, et konfigureeritud järeletulemisega tarneviisidega lingitud müügiread eiraksid DOM-i loogikat ning et neid ei eraldataks laos uueks täitmiseks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]