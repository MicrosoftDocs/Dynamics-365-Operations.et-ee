---
title: Elektroonilise arvelduse lisandmooduli halduse komponendid
description: Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse lisandmooduli haldusega.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104370"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Elektroonilise arvelduse lisandmooduli halduse komponendid

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse lisandmooduli haldusega. Samuti kirjeldab see, kuidas elektroonilise arvelduse lisandmooduli teenust konfigureerida.

## <a name="azure"></a>Azure

Kasutage teenust Microsoft Azure võtmehoidla ja salvestuskonto saladuste loomiseks. Seejärel kasutage saladusi elektroonilise arvelduse lisandmooduli konfigureerimisel.

## <a name="lifecycle-services"></a>Lifecycle Services

Kasutage LCS-i juurutusprojekti mikroteenuste jaoks lisandmooduli lubamiseks Microsoft Dynamicsi teenust Lifecycle Services (LCS).

Valige LCS-is paan **Eelvaate funktsiooni haldamine** ja lülitage funktsioon **E-arvelduse teenus** sisse.

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) on elektroonilise arvelduse lisandmooduli konfigureerimiseks kasutatav liides. Selliseid ressursse nagu keskkonnad ja elektroonilise arvelduse funktsioonid luuakse, hallatakse ja majutatakse RCS-is. Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse lisandmooduli teenuses.

Lisateavet RCS-i kohta vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Elektroonilise arvelduse lisandmooduliga integreerimine

Enne kui saate elektrooniliste arvete konfigureerimiseks RCS-i kasutada, peate konfigureerima RCS-i, et lubada andmevahetus elektroonilise arvelduse lisandmooduliga. See konfiguratsioon lõpetatakse lehe **Elektroonilise aruandluse parameetrid** vahekaardil **Elektroonilise aruandluse lisandmoodul**.

#### <a name="service-endpoint"></a>Teenuse lõpp-punkt

Elektroonilise arvelduse lisandmooduli lõpp-punkt võib olenevalt Azure'i andmekeskuse geograafilisest piirkonnast erineda. Järgmises tabelis on toodud saadavus piirkonniti.

| Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URL                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Ida-USA                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| Lääne-USA                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| Põhja-EL                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| Lääne-EL                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>Rakenduse ID

Rakenduse ID on elektroonilise arvelduse lisandmooduli rakenduse ID. Selles näites on see väärtus fikseeritud: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

#### <a name="lcs-environment-id"></a>LCS-i keskkonna ID

LCS-i keskkonna ID on teie organisatsiooni LCS-i tellimuse ID.

### <a name="service-environments"></a>Teenusekeskkonnad

Teenusekeskkonnad on loogilised sektsioonid, mis luuakse elektroonilise arvelduse lisandmoodulis elektroonilise arvelduse funktsioonide käivitamise toetamiseks. Turvasaladused ja digitaalserdid ning juhtimine (st juurdepääsuload) peavad olema konfigureeritud teenusekeskkonna tasemel.

Kliendid saavad luua nii palju teenusekeskkondi, kui nad soovivad. Kõik teenusekeskkonnad, mille klient loob, on üksteisest sõltumatud.

Teenusekeskkonnad saab luua ja neid saab hooldada RCS-is. Kui teenusekeskkonnad on valmis, tuleb need elektroonilise arvelduse lisandmooduli teenuses avaldada.

#### <a name="service-environment-status"></a>Teenusekeskkonna olek

Teenusekeskkondi saab hallata oleku kaudu. Saadaval on järgmised valikud.

- **Pole avaldatud** – keskkond on loodud, kuid seda pole veel avaldatud.
- **Avaldatud** – keskkond on elektroonilise arvelduse lisandmoodulis avaldatud.
- **Muudetud** – avaldatud keskkonna atribuute on muudetud, kuid muudatusi pole veel avaldatud.

#### <a name="customer-secrets"></a>Klientide saladused

Elektroonilise arvelduse lisandmooduli teenus vastutab kõigi teie äriandmete talletamise eest Azure'i ressurssides, mis kuuluvad teie ettevõttele. Et teenus töötaks korrektselt ning kõikidele äriandmetele, mida elektroonilise arvelduse lisandmoodul vajab ja kasutab, pääseks juurde vaid see lisandmoodul, peate looma kaks peamist Azure'i ressurssi.

- Azure'i salvestuskonto (bloobimälu) elektrooniliste arvete talletamiseks
- Azure'i võtmehoidla sertide ja salvestuskonto ühtse ressursi-indikaatori (URI) talletamiseks

> [!NOTE]
> Elektroonilise arvelduse lisandmooduli jaoks tuleb määrata spetsiaalne võtmehoidla ja kliendi salvestuskonto.

Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Kasutajad

Iga teenusekeskkond peab loetlema kasutajad, kes saavad elektroonilise arvelduse lisandmoodulis teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management kaudu ühenduse luua.

#### <a name="publication"></a>Avaldamine

Enne teenusekeskkondade kasutamist tuleb need elektroonilise arvelduse lisandmoodulis avaldada. Teenuste Finance ja Supply Chain Management kaudu pääseb juurde ainult avaldatud keskkondadele. Peale selle tuleb teenusekeskkond avaldada, enne kui selle atribuutide värskendused elektroonilise arvelduse teenuses jõustuvad.

### <a name="connected-applications"></a>Ühendatud avaldused

Ühendatud rakendused on teenuste Finance and Supply Chain Management eksemplarid, millega võite soovida RCS-i kaudu ühendust saada. Peale rakenduse URL-i ja selle rentniku hõlmab ühendatud rakendus mandaate, mis võimaldavad RCS-il keskkonnaga ühenduse luua.

Ühendatud rakenduste abil saate konfigureerida osa elektroonilise arvelduse funktsioonist teenustes Finance ja Supply Chain Management, et kogu elektroonilise arvelduse funktsioon tööle saada.

## <a name="finance-and-supply-chain-management"></a>Finance ja Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Elektroonilise arvelduse lisandmooduliga integreerimine

Enne kui saate teenuseid Finance ja Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektrooniliste arvete väljastamiseks kasutada, tuleb lisandmoodul konfigureerida nii, et see lubaks teenusega suhtlemist.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Elektroonilise arvelduse lisandmooduli integreerimisfunktsioon

Teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahelise suhtluse lubamiseks peate tööruumis **Funktsioonihaldus** funktsiooni **Elektroonilise arvelduse lisandmooduli integreerimine** sisse lülitama.

#### <a name="service-endpoint"></a>Teenuse lõpp-punkt

Teenuse lõpp-punkt on elektroonilise arvelduse lisandmooduli asukoha URL. Enne kui saab väljastada elektroonilisi arveid, tuleb teenuse lõpp-punkt konfigureerida teenustes Finance ja Supply Chain Management nii, et see lubaks teenusega suhtlemist.

Teenuse lõpp-punkti konfigureerimiseks avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid** ja seejärel sisestage vahekaardi **Edastusteenused** väljale **Elektroonilise arvelduse lisandmooduli URL** URL, nagu on kirjeldatud jaotises **Teenuse lõpp-punkt** näidatud tabelis.

#### <a name="environments"></a>Keskkonnad

Teenuses Finance ja Supply Chain Management sisestatud keskkonna nimi viitab selle keskkonna nimele, mis luuakse RCS-is ja avaldatakse elektroonilise arvelduse lisandmoodulis.

Keskkond tuleb konfigureerida lehe **Elektroonilise dokumendi parameetrid** vahekaardil **Edastusteenused**, nii et kõik elektrooniliste arvete väljastamistaotlused hõlmavad keskkonda, kus elektroonilise arvelduse lisandmoodul saab määrata, milline elektroonilise arvelduse funktsioon peab taotlust töötlema.

## <a name="additional-resources"></a>Lisaressursid

- [Elektrooniliste arvete konfigureerimine RCS-is](e-invoicing-configuration-rcs.md)
- [Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
