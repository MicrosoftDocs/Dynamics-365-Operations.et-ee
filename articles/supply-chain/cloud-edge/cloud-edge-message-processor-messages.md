---
title: Sõnumi töötleja sõnumid
description: See teema annab teavet sõnumite protsessori teadete funktsiooni kohta kaalu ühiku töökoormuste puhul.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 76a3cc316da322c7997072c00780f2fc133bfd2a02274b1e53f5cd06cfb1277e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748855"
---
# <a name="message-processor-messages"></a>Sõnumi töötleja sõnumid

[!include [banner](../includes/banner.md)]

Sõnumitöötluse sõnumeid kasutatakse pilve ja servaskaala üksuste käitamisel [tootmise töökoormuste](cloud-edge-workload-manufacturing.md) ja [laohalduse töökoormuste](cloud-edge-workload-warehousing.md) jaoks.

Keskuse ja kaalu ühiku juurutuskeskkonnad vahetavad nende sünkroonimisel suurt hulka andmeid, kuid *teateprotsessor* töötleb ainult mõnda neist andmevahetustest. Te saate vaadata teateprotsessori töödeldud teateid, kui teateid **Süsteemihaldus > Sõnumiprotsessor > Teateprotsessori teated**.

## <a name="message-grid-columns-and-filters"></a>Teatepaneeli veerud ja filtrid

Võite kasutada väljasid **sõnumiprotsessori teadete** lehe ülaosas, et aidata leida mis tahes konkreetsed sõnumid, mida otsite. Enamik neist filtritest sobivad veeru pealkirjadega teatepaneelis. Saadaval on järgmised filtrid ja veeru pealkirjad:

- **Teate tüüp** – määrab teate tüübi.
- **Teatejärjekord** – määrab järjekorra nime, milles teadet töödeldakse. Saadaval on järgmised järjekorrad:
  - *Skaalaüksus keskusesse*
  - *Lao käivitamise skaalaüksuse keskus*
  - *Tootmise käivitamise skaalaüksuse keskus*
- **Teate olek** – määrab teate oleku. Leidub järgmisi olekuid:
  - *Järjekorras* – sõnum on teateprotsessori töötlemiseks valmis.
  - *Töödeldud* – sõnum on teateprotsessori poolt edukalt töödeldud.
  - *Tühistatud* – teade on töödeldud, kuid töötlemine nurjus.
- **Sõnumi sisu** – selle filtriga tehakse sõnumisisu täistekstotsing. (Sõnumit ei kuvata ruudustikus.) Filter käsitleb enamikke erisümboleid (nt „-”) tühikuna ja käsitleb kõiki tühikuid kahendmuutuja VÕI tehtemärkidena. T=Nt kui otsite konkreetset väärtust `journalid`, mis oleks "USMF-123456", otsib süsteem kõik teated, mis sisaldavad "USMF" või "123456", mis on tõenäoliselt pikk loend. Seetõttu oleks parem sisestada ainult "123456", sest see annab paremad tulemused.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Teate näidistüüp: varude korrigeerimise finantsvärskenduse taotlemine

Näiteks **sõnumi tüüpi** *Varude korrigeerimise finantsvärskendus* kasutatakse inventuuritöölehe loomiseks ja sisestamiseks keskusesse, kui töötaja kasutab lao rakendust [varude korrigeerimise registreerimiseks](cloud-edge-warehouse-inventory-adjustment.md) kaaluühiku laohalduse töökoormuses. Kuna see konkreetne protsess pärineb kaaluühikust, kuvatakse **teatejärjekorra** väljal väärtuse *ühik keskusesse*.

Selle teatetüübi puhul salvestab kaaluühik sõnumi laorakenduse varude korrigeerimistoimingu osana. Sõnumiandmed kantakse seejärel keskusesse üle osana samast protsessist, mida kasutatakse [Commerce data exchange architecture](../../commerce/commerce-architecture.md). Teade uuendatakse, et kuvada **teate olek** olekuna *järjekorras*. Teateprotsessor püüab siis sõnumit töödelda ja uuendab **sõnumi olekut** edukalt *töödeldud* olekule või nurjumisel *tühistatuks*.

## <a name="view-the-message-log-message-content-and-details"></a>Saate kuvada teatelogi, sõnumi sisu ja üksikasju

Teate kohta üksikasjaliku teabe leiate, kui valite selle ruudustikust ja avate seejärel **logi** või **teate sisu** vahekaardid teateruudustikus, kus kuvatakse iga töötlussündmus.

**Sõnumi sisu** sõltub **sõnumitüübist** ja selle teksti pikkus on seega erinev. Tavaline sõnumisisu tekst algab väärtusega **{** ja lõpeb väärtusega **}** ja nende vahel on sellised väljanimed, nagu näiteks `journalId`, millele järgneb **:** ja selline väärtus, nagu *USMF-123456*.

Vahekaardi **Logi** tööriistaribal on järgmised nupud:

- **Logi** – kuvatakse töötlemistulemused. Sellest on abi eelkõige töötlemise nurjumise põhjuste mõistmisel nende teadete puhul, mille **töötlemise tulemus** on *Nurjunud*.
- **Kogum** – mitu teatetöötlustoimingut saab käitada ühe ja sama pakktöötluse osana. Selle nupu abil saate vaadata üksikasjalikke andmeid. Näiteks saate vaadata, kas on olemas sõltuvusi, mis nõuavad süsteemilt kindlas järjekorras teatud teadete töötlemiseks.

## <a name="message-processor-batch-job"></a>Teateprotsessori pakett-töö

Pilve ja serva juurutuse käitamisel käivitatakse sõnumiprotsessori pakett-töö automaatselt uue teate loomisel töötlemiseks, seega ei pea te seda tööd käsitsi *plaanima*.

Vajadusel pääsete pakett-tööle, kui valides **Süsteemihaldus > Sõnumiprotsessor > Teateprotsessor**.

## <a name="manually-process-or-cancel-a-message"></a>Sõnumi käsitsi saatmine või tühistamine

Sõltuvalt selle praegusest olekust, saate sõnumit käsitsi töödelda või tühistada. Selleks valige ruudustikus teade ja valige siis tegevuspaanil suvand **Protsess** või **Tühista**

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Saate häälestada ärisündmusi teatiste esitamiseks nurjunud töötlemise tulemuste kohta

Lisaks **sõnumi oleku** filtreerimiseks *Tühistatud* teadete järgi, et leida ebaõnnestunud teateid, saate seadistada keskuse [ärisündmused](../../fin-ops-core/dev-itpro/business-events/home-page.md), mis teavitavad teid töötluse nurjunud tulemustest. Selleks aktiveerige ärisündmus nimega *Teateprotsessori teade*, mis on töödeldud **ärisündmuste kataloogi** lehel (**Süsteemihaldus > Häälestus > Ärisündmused > Ärisündmuste kataloog**).

Osana aktiveerimisprotsessist juhendatakse teid määramaks, kas sündmus on omane ühele või kõigile juriidilistele isikutele ja andma **lõpp-punkti nime**, mis tuleb esimesena määratleda.

>[!NOTE]
> Kui seade **Kui ärisündmus toimub** on näiteks seatud väärtusele *Microsoft Power Automate* (mitte *HTTPS*), luuakse **lõpp-punkti** nimi seadistuse *Microsoft Power Automate* põhjal automaatselt Supply Chain Managementis.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate näide

Selles näites kasutage seadet **Kui ärisündmus toimub**, kui *Microsoft Power Automate* edastab meile, mis sisaldavad InfoLogi sõnumeid ja hüperlinke, et avada lehe **Sõnumi töötleja sõnumid** spetsiifilise nurjunud sõnumi kohta keskmuse rakendamise puhul. Vajadusel saate lisada lisaloogika, et saata teatised paralleelselt, kasutades erinevaid kanaleid ja juhtida adressaate sündmuse andmete põhjal.

1. Looge [Power Automate](https://preview.flow.microsoft.com)-s voo käivitamiseks uus automatiseeritud pilvevoog **Ärisündmuse toimumisel – Fin & Ops App (Dynamics 365** ), millele järgnevad **Parse JSON** ja **saatke meilisõnumid**, nagu näidatud järgmises illustratsioonis.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate automaatne pilvevoog.":::

1. Sammus **Kui ärisündmus toimus** saate kas üles otsida või sisestada keskuse **instants** pärast **Kategooriat** ja seejärel **Ärisündmus** *Sõnumiprotsessori sõnum on töödeldud*, nagu näidatud järgmises illustratsioonis.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Kui ärisündmuse toimumine on etapp.":::

1. Sammu **Parse JSON** puhul sisestage **skeem**, mis määratleb laiendatud väljad. Saate kasutada suvandit *Laadi skeem* alla ärisündmuste kataloogi lehel **Supply Chain Management** is või alustada, kleepides näidisskeemi teksti. See näitetekst antakse pärast järgmist illustratsiooni.

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Sõelu JSON etappi.":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. **E-kirja saatmise sammus** saate valida üksikud väljad või alustada, kasutades meili kehanäidet **kehaväljale**. See näide antakse pärast järgmist illustratsiooni.

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate meilisõnumi saatmise etapp.":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. Ärisündmuse salvestamisel aktiveeritakse see automaatselt ja on valmis kasutama Supply Chain Managementi osana.
