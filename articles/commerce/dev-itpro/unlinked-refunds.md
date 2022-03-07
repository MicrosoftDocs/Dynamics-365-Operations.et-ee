---
title: Töötle linkimata tagasimakseid Adyeni Dynamics 365 Commerce Payment Connectoriga
description: See teema kirjeldab, kuidas linkimata tagasimaksed töötavad Aydeni Microsoft Dynamics 365 Payment Connectoriga.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c137dcf7d35031a293c88d8c4f5dc1e5f3d9e2f9
ms.sourcegitcommit: a21a664cd35b95c8600c5af0aac588a64e892902
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/11/2021
ms.locfileid: "7623917"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Töötle linkimata tagasimakseid Adyeni Dynamics 365 Commerce Payment Connectoriga

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas linkimata tagasimaksed töötavad Aydeni [Microsoft Dynamics 365 Payment Connector](adyen-connector.md)iga. Lisaks vaadatakse üle võimalus töödelda tagasimakset uue makseviisi alusel kassas (POS) või kõnekeskuses.

Adyeni Dynamics 365 Payment Connector toetab tagasimaksete töötlemise võimalust, kasutades muud makseviisi, kui kasutati algses kandes. Kuigi me soovitame kasutada [lingitud tagasimakseid](linked-refunds.md), et töödelda tagasimakset antud algse makseviisi suhtes, on mõne stsenaariumi puhul vaja tagasimakseid teise meetodiga. Näiteks võib algse makse jaoks kasutatud kaart olla aegunud või kaotatud või on kasutaja selle võib olla tühistanud.

## <a name="prerequisites"></a>Eeltingimused

Enne kui Adyeni Dynamics 365 Payment Connectori saab linkimata tagasimakseid töödelda, peavad olema täidetud järgmised eeltingimused:

- Seadistada [maksemeetodid](../payment-methods.md).
- Seadista [omnikanali maksed](../omni-channel-payments.md).

## <a name="additional-configuration"></a>Täiendav konfiguratsioon

Dynamics 365 maksekonnektor Adyeni jaoks annab valmis juurutuse iga järgmises jaotises kirjeldatud toetatud tagasimakse stsenaariumi kohta. Kliendid, kes ei kasuta Adyenile mõeldud Dynamics 365 Payment Connectori välist rakendust, peavad seadistama konnektori, mis toetab krediitkaartide tokeniseerimist.

## <a name="supported-refund-scenarios"></a>Toetatud tagasimakse stsenaariumid

Dynamics 365 Commerce toetab varem kinnitatud ja kinnitatud tehingute tagasimakset. Tagasimaksed võivad koosneda kande kas täielikust tagasimaksest või osalisest tagasimaksest. Tagasimaksed ei tohi ületada algse makse autoriseerimise kogusummat. Linkimata tagasimakseid toetatakse ainult kassas ja kõnekeskuses.

## <a name="enable-unlinked-refunds-functionality"></a>Linkimata tagasimaksete funktsiooni lubamine

Lingimata tagasimaksefunktsiooni lubamiseks Commerce'i peakorteris toimige järgmiselt.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**.
1. Seadistage vahekaardil **Omnikanali maksed** suvand **Kasuta omnikanali makseid** valikule **Jah**.

### <a name="supported-payment-method-variants"></a>Toetatud makseviisi variandid

Järgmised makseviisi variandid toetavad linkimata tagasimakseid boksist välja:

- Kaardid
- Rahakott

Kõik makseviisi variandid ei toeta linkimata tagasimakseid. Järgmine tabel annab ühiste makseviiside loendi ja näitab iga meetodi tugivõimalusi lingitud ja linkimata tagasimaksete puhul.

| Makseviis        | Lingitud tagasimakse | Linkimata tagasimakse |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Jah           | Jah             |
| amexconsumer          | Jah           | Jah             |
| amexcorporate         | Jah           | Jah             |
| amexdebit             | Jah           | Jah             |
| amexprepaid           | Jah           | Jah             |
| amexprepaidreloadable | Jah           | Jah             |
| amexsmallbusiness     | Jah           | Jah             |
| avasta              | Jah           | Jah             |
| maestro               | Jah           | Jah             |
| maestrouk             | Jah           | Jah             |
| mc                    | Jah           | Jah             |
| mcalphabankbonus      | Jah           | Jah             |
| mcprepaidanonymous    | Jah           | Jah             |
| viisa                  | Jah           | Jah             |
| visaalphabankbonus    | Jah           | Jah             |
| visacheckout          | Jah           | Jah             |
| visadankort           | Jah           | Jah             |
| visahipotecario       | Jah           | Jah             |
| visasaraivacard       | Jah           | Jah             |
| vpay                  | Jah           | Jah             |
| givex                 | **Ei**        | Jah             |
| svs                   | **Ei**        | Jah             |
| cup                   | Jah           | Jah             |
| diners                | Jah           | Jah             |
| interac               | **Ei**        | Jah             |
| Jcb                   | Jah           | Jah             |
| jcb_applepay          | Jah           | Jah             |
| unionpay              | Jah           | Jah             |

### <a name="process-an-unlinked-refund-in-pos"></a>Linkimata tagasimakse protsess kassas

Klient tagastab kauba kassapidajale tagastuste lubatud perioodi jooksul ja omab kehtivat tšekki tehingust. Tagastuse töötlemisel sisaldub dialoogiaknas **Tagastusmakse** suvand **Vali makseviis**. Kassapidaja saab seejärel valida makseviisi toetatud tagasimaksete makseviiside hulgast (kaart ja sularaha).

### <a name="process-an-unlinked-refund-in-call-center"></a>Linkimata tagasimakse protsess kõnekeskuses

Kui kõnekeskuse tellimuse suhtes töödeldakse linkimata tagasimakset, valib kõnekeskuse töötaja maksemeetodi, mis erineb algsest meetodist. Seejärel palutakse töötajal hankida administraatori õigustega isikukoodi (PIN) ülekirjutamise. PIN on nõutav enne erinevate makseviiside töötlemist tagasimakse jaoks.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Seadistage kõnekeskuse PIN-kood, mida saab administraatorina üle kirjutada

Kui soovite Commerce'i peakorteri kõnekeskuse jaoks seadistada PIN-koodi, mida saab administraatorina üle kirjutada, järgige järgmisi samme.

1. Minge **Retail ja Commerce \> Kanali häälestus \> Kõnekeskuse seadistamine** või otsige sõna "Lubade ülekirjutamine".
1. Valige roll, mis lubaks linkimata tagasimakse töötlemise õigusi.
1. Kiirkaardil **Tagastused** määrake suvand **Luba alternatiivne makse** valikule **Jah**.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Payment Connector Adyeni jaoks](adyen-connector.md)

[Eelnevalt kinnitatud ja kinnitatud kannete lingitud tagasimaksed](linked-refunds.md)
