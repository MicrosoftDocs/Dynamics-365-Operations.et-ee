---
title: Elektroonilise arvelduse administratsioonikomponendid
description: See artikkel annab teavet komponentide kohta, mis on seotud elektroonilise arvelduse haldamisega.
author: gionoder
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: cdd4d6705730bca967bb1bbff528df6d83a2390d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875996"
---
# <a name="electronic-invoicing-administration-components"></a>Elektroonilise arvelduse administratsioonikomponendid

[!include [banner](../includes/banner.md)]


See artikkel annab teavet komponentide kohta, mis on seotud elektroonilise arvelduse haldamisega. Samuti pakub see teavet selle kohta, kuidas elektroonilise arvelduse teenust konfigureerida.

## <a name="azure"></a>Azure

Kasutage teenust Microsoft Azure võtmehoidla ja salvestuskonto salasõnade loomiseks. Seejärel kasutage elektroonilise arveldamise konfiguratsioonis võtmehoidla saladusi ja salvestuskonto SAS-i luba.

## <a name="lifecycle-services"></a>Lifecycle Services

Kasutage Microsoft Dynamics Lifecycle Services (LCS), et lubada oma LCS-i juurutusprojekti jaoks elektroonilise arvelduse lisandmoodul.

> [!NOTE]
> Lisandmooduli LCS-i install nõuab vähemalt **2. taseme keskkonda**. Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) on liides, mida kasutatakse Elektroonilise arvelduse konfigureerimiseks. Selliseid ressursse nagu keskkonnad ja elektroonilise arvelduse funktsioonid luuakse, hallatakse ja majutatakse RCS-is. Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse teenuses.

RCS-i registreerimiseks vaata [Regulatory services](https://marketing.configure.global.dynamics.com/).

Lisateavet RCS-i kohta vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).

### <a name="integration-with-electronic-invoicing"></a>Elektroonilise arvelduse integratsioon 

Enne kui saate elektrooniliste arvete konfigureerimiseks RCS-i kasutada, peate konfigureerima RCS-i, et lubada andmevahetus elektroonilise arveldusega. See konfiguratsioon lõpetatakse lehe **Elektroonilise arvelduse parameetrid** vahekaardil lehel **Elektroonilise aruandluse lisandmoodul**.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Teenuse lõpp-punkt

Elektrooniline arveldus on saadaval mitmetes Azure'i geograafilistes andmekeskustes. Järgmises tabelis on toodud saadavus piirkonniti.


| Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URI                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Ameerika Ühendriigid              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Euroopa                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Ühendkuningriik             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Aasia                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Teenusekeskkonnad

Teenusekeskkonnad on loogilised sektsioonid, mis luuakse elektroonilise arvelduse funktsioonides elektroonilise arvelduse käivitamise toetamiseks. Turvasaladused ja digitaalserdid ning juhtimine (st juurdepääsuload) peavad olema konfigureeritud teenusekeskkonna tasemel.

Kliendid saavad luua nii palju teenusekeskkondi, kui nad soovivad. Kõik teenusekeskkonnad, mille klient loob, on üksteisest sõltumatud.

Teenusekeskkonnad saab luua ja neid saab hooldada RCS-is. Kui teenusekeskkonnad on valmis, tuleb need elektroonilise arvelduses avaldada.

#### <a name="service-environment-status"></a>Teenusekeskkonna olek

Teenusekeskkondi saab hallata oleku kaudu. Saadaval on järgmised valikud.

- **Pole avaldatud** – keskkond on loodud, kuid seda pole veel avaldatud.
- **Avaldatud** – Keskkond on elektroonilise arvelduses avaldatud .
- **Muudetud** – avaldatud keskkonna atribuute on muudetud, kuid muudatusi pole veel avaldatud.

#### <a name="customer-secrets"></a>Klientide saladused

Elektroonilise arvelduse teenus vastutab kõigi teie äriandmete talletamise eest Azure'i ressurssides, mis kuuluvad teie ettevõttele. Kindlustamaks seda, et teenus korrektselt töötab ja et kõik äriandmed on nõutud ja loodud Elektroonilise arvelduse jaoks sobivalt saadaval,peate looma kaks peamist Azure-i ressurssi:

- Azure'i salvestuskonto (Bloobi talletus), mis talletada elektroonilisi dokumente, sh elektroonilisi arveid, dokumenditeisenduste tulemusi ja väliste veebiteenuste vastuseid.
- Azure'i võtmehoidla salvestab sertide ja salvestuskonto ühtset ressursi-indikaatorit (URI) (SAS juurdepääs).


Spetsiaalne võtmehoidla ja kliendi salvestuskonto peab olema spetsiaalselt elektroonilise arvelduse jaoks määratud. Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).

Oma võtmehoidla seisundi jälgimiseks ja teatiste saamiseks konfigureerige Azure Monitor võtmehoidla jaoks. Võtmehoidla logimise lubamisega saate jälgida, kuidas, millal ja kellel on teie võtmehoidlatele juurdepääs. Lisateavet vt jaotisi [Azure'i võtmehoidla jälgimine ja häirete saatmine](/azure/key-vault/general/alert) ja [Kuidas lubada võtmehoidla logimist](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Hea tava on salasõnasid aegajalt vahetada. Lisateabe saamiseks vt [Salasõnade dokumentatsiooni](/azure/key-vault/secrets/).

#### <a name="users"></a>Kasutajad

Iga teenusekeskkond peab loetlema kasutajad, kes saavad dynamics 365 Finantsid ja Elektroonilises Dynamics 365 Supply Chain Management arveldamises ühendust luua.

#### <a name="publication"></a>Avaldamine

Enne teenusekeskkondade kasutamist tuleb need elektroonilises arvelduses avaldada. Teenuste Finance ja Supply Chain Management kaudu pääseb juurde ainult avaldatud keskkondadele. Peale selle tuleb teenusekeskkond avaldada, enne kui selle atribuutide värskendused elektroonilise arvelduse teenuses jõustuvad.

### <a name="connected-applications"></a>Ühendatud avaldused

Ühendatud rakendused on teenuste Finance and Supply Chain Management eksemplarid, millega võite soovida RCS-i kaudu ühendust saada. Peale rakenduse URL-i ja selle rentniku hõlmab ühendatud rakendus mandaate, mis võimaldavad RCS-il keskkonnaga ühenduse luua.

Ühendatud rakenduste abil saate konfigureerida osa elektroonilise arvelduse funktsioonist teenustes Finance ja Supply Chain Management, et kogu elektroonilise arvelduse funktsioon tööle saada.

## <a name="finance-and-supply-chain-management"></a>Finance ja Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Elektroonilise arvelduse integratsioon

Enne kui saate teenuseid Finance ja Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektrooniliste arvete väljastamiseks kasutada, tuleb lisandmoodul konfigureerida nii, et see lubaks teenusega suhtlemist.

#### <a name="electronic-invoicing-integration-feature"></a>Elektroonilise arvelduse integratsiooni funktsioon

Teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahelise suhtluse lubamiseks peate tööruumis **Funktsioonihaldus** funktsiooni **Elektroonilise arvelduse lisandmooduli integreerimine** sisse lülitama.

#### <a name="service-endpoint"></a>Teenuse lõpp-punkt

Teenuse lõpp-punkt on elektroonilise arvelduse asukoha URL. Enne kui saab väljastada elektroonilisi arveid, tuleb teenuse lõpp-punkt konfigureerida teenustes Finance ja Supply Chain Management nii, et see lubaks teenusega suhtlemist.

Teenuse lõpp-punkti konfigureerimiseks minge organisatsiooni halduse elektroonilise dokumendi parameetritesse ja seejärel sisestage elektroonilise arveldamise vahekaardi lõpp-punkti URL väljale tabelist vastav URL **\>\> selles artiklis eespool olevas** **·** **teenuse lõpp-punkti jaotises.**[...](#svc-endpoint-uris)

#### <a name="environments"></a>Keskkonnad

Keskkonna nimi, mis on sisestatud Finants ja Supply Chain Management -i viitab keskkonna nimele, mis on loodud RCS-is ja avaldatud Elektroonilises arvelduses.

Keskkond peab olema konfigureeritud **elektroonilis arve** vahekaardil **elektroonilise dokumendi parameetrite** lehel. Nii sisaldab iga elektrooniliste arvete väljastamise taotlus keskkonda, kus elektrooniline arveldamine saab määrata, milline elektroonilise arveldamise funktsioon peab taotluse töötlema.

## <a name="additional-resources"></a>Lisaressursid

- [Elektrooniliste arvete konfigureerimine RCS-is](e-invoicing-configuration-rcs.md)
- [Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
