---
title: Korduvate andmete ekspordi rakenduse loomine
description: See artikkel kirjeldab, kuidas luua loogikarakendus Microsoft Azure, mis ekspordib Microsoftist Dynamics 365 Human Resources andmeid korduvas graafikus.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c840dbf4f717da3359640ee5c8231ccd129ebb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875825"
---
# <a name="create-a-recurring-data-export-app"></a>Korduvate andmete ekspordi rakenduse loomine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab, kuidas luua loogikarakendus Microsoft Azure, mis ekspordib Microsoftist Dynamics 365 Human Resources andmeid korduvas graafikus. Õpetus kasutab andmete eksportimiseks rakenduse Human Resources DMF-i paketi REST rakenduse programmeerimisliidest (API). Pärast andmete eksportimist salvestab loogikarakendus eksporditud andmed Microsoft OneDrive for Businessi kausta.

## <a name="business-scenario"></a>Äristsenaarium

Ühes tüüpilises Microsoft Dynamics 365 integreerimise äristsenaariumis tuleb andmeid eksportida allsüsteemi korduva graafiku alusel. See õpetus näitab, kuidas eksportida kõik töötajate kirjed rakendusest Microsoft Dynamics 365 Human Resources ja salvestada töötajate loend OneDrive for Businessi kausta.

> [!TIP]
> Selles õpetus eksporditavad konkreetsed andmed ja eksporditud andmete sihtkoht on ainult näited. Saate neid oma ettevõtte vajadustele vastavalt hõlpalt muuta.

## <a name="technologies-used"></a>Kasutatud tehnoloogiad

See õpetus kasutab järgmisi tehnoloogiaid.

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**– eksporditavatele töötajatele mõeldud koondandmete allikas.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – tehnoloogia, mis võimaldab korduva eksportimise korraldamist ja planeerimist.

    - **[Konnektorid](/azure/connectors/apis-list)** – tehnoloogia, mida kasutatakse loogikarakenduse ühendamiseks vajalike lõpp-punktidega.

        - Konnektor [HTTP koos Azure AD-ga](/connectors/webcontents/)
        - Konnektor [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness)

- **[DMF-i pakett REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – tehnoloogia, mida kasutatakse eksportimise käivitamiseks ja selle edenemise jälgimiseks.
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** – eksporditud töötajate sihtkoht.

## <a name="prerequisites"></a>Eeltingimused

Enne selle õpetuse harjutusega alustamist peavad teil olema järgmised üksused.

- Inimressursside keskkond, millel on keskkonnas administraatori taseme load
- [Azure’i tellimus](https://azure.microsoft.com/free/) loogikarakenduse majutamiseks

## <a name="the-exercise"></a>Harjutus

Selle harjutuse lõpus on teil loogikarakendus, mis on ühendatud teie inimressursside keskkonna ja OneDrive for Businessi kontoga. Loogikarakendus ekspordib rakendusest Human Resources andmepaketi, ootab eksportimise lõpule jõudmist, laadib eksporditud andmepaketi alla ja salvestab andmepaketi määratud OneDrive for Businessi kausta.

Lõpetatud loogikarakendus sarnaneb järgmisele joonisele.

![Loogikarakenduse ülevaade.](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>1. etapp: andmete eksportimise projekti loomine rakenduses Human Resources

Looge rakenduses Human Resources andmete eksportimise projekt, mis ekspordib töötajaid. Pange sellele nimi **Töötajate eksportimine** ja veenduge, et suvand **Andmepaketi loomine** oleks seatud valikule **Jah**. Lisage projektile üks üksus (**Töötaja**) ja valige eksportimiseks vorming. (Selles õpetuses on kasutatud Microsoft Exceli vormingut.)

![Töötajate eksportimise andmeprojekt.](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Jätke andmete eksportimise projekti nimi meelde. Seda on vaja, kui loote järgmises etapis loogikarakenduse.

### <a name="step-2-create-the-logic-app"></a>2. etapp: loogikarakenduse loomine

Suur osa harjutusest hõlmab loogikarakenduse loomist.

1. Looge Azure’i portaalis loogikarakendus.

    ![Loogikarakenduse loomise leht.](media/integration-logic-app-creation-1.png)

2. Alustage Logic Apps Designeris tühja loogikarakendusega.
3. Lisage [kordumise graafiku päästik](/azure/connectors/connectors-native-recurrence), et käivitada loogikarakendus iga 24 tunni järel (või vastavalt teie valitud graafikule).

    ![Kordumise dialoogiaken.](media/integration-logic-app-recurrence-step.png)

4. Kutsuge DMF-i REST API [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage), et ajastada teie andmepaketi eksportimine.

    1. Kasutage tegevust **HTTP-päringu kutsumine** konnektorist HTTP koos Azure AD-ga.

        - **Põhiressursi URL:** teie inimressursside keskkonna URL (ärge lisage tee/nimeruumi teavet.)
        - **Azure AD ressursi URI:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > Teenus Human Resources ei paku veel konnektorit, mis näitab kõiki API-sid, millest DMF-i paketi REST API koosneb, näiteks **ExportToPackage**. Selle asemel peate kutsuma API-d, kasutades HTTPS-i toortaotlusi läbi konnektori HTTP koos Azure AD-ga. See konnektor kasutab autentimiseks ja autoriseerimiseks rakendusele Human Resources Azure Active Directoryt (Azure AD).

        ![Konnektor HTTP koos Azure AD-ga.](media/integration-logic-app-http-aad-connector-step.png)

    2. Logige oma inimressursside keskkonda läbi konnektori HTTP koos Azure AD-ga sisse.
    3. Seadistage HTTP **POST-i** taotlus kutsuma DMF-i REST API **ExportToPackage**.

        - **Meetod:** POST
        - **Taotluse URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **Taotluse keha:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Tegevuse HTTP-päringu käivitamine.](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Võite soovida iga sammu ümber nimetada, et see oleks tähendusrikkam kui vaikenimi **HTTP-päringu käivitamine**. Näiteks võite panna sellele etapile nimeks **ExportToPackage**.

5. [Lähtestage muutuja](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) salvestama taotluse **ExportToPackage** käivitamisoleku.

    ![Muutuja tegevuse lähtestamine.](media/integration-logic-app-initialize-variable-step.png)

6. Oodake, kuni andmete ekspordi käivitamisolek on **Õnnestunud**.

    1. Lisage [silmus Kuni](/azure/logic-apps/logic-apps-control-flow-loops#until-loop), mis kordub, kuni muutuja **ExecutionStatus** väärtus on **Õnnestunud**.
    2. Lisage tegevus **Viivitus**, mis ootab viis sekundit enne kui pollib eksportimise praegust käivitamisolekut.

        ![Silmuse Kuni konteiner.](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Määrake limiidi arvuks **15**, et oodata ekspordi lõpetamiseks maksimaalselt 75 sekundit (15 iteratsiooni × 5 sekundit). Kui teie eksportimisele kulub rohkem aega, reguleerige limiidi arvu vastavalt vajadusele.        

    3. Lisage tegevus **Käivita HTTP-päring**, er kutsuda DMF-i REST API [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) ja määrata muutuja **ExecutionStatus** vastuse **GetExecutionSummaryStatus** tulemusele.

        > See näide ei tee veakontrolli. API **GetExecutionSummaryStatus** võib tagastada ebaõnnestunud lõplikke olekuid (s.t muud olekud kui **Õnnestunud**). Lisateabe saamiseks vt [API-i dokumentatsiooni](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **Meetod:** POST
        - **Taotluse URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **Taotluse keha:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > Võimalik, et peate sisestama väärtuse **Taotluse keha** kas koodi vaates või kujundaja funktsioonide redaktoris.

        ![Tegevuse HTTP-päring 2 käivitamine.](media/integration-logic-app-get-execution-status-step.png)

        ![Muutuva tegevuse määramine.](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > Tegevuse **Muutuja määramine** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) väärtus erineb keha **HTTP-päringu 2 käivitamine** väärtusest, isegi kui kujundaja näitab väärtuseid samamoodi.

7. Hankige eksporditud paketi allalaadimise URL.

    - Lisake tegevus **HTTP-päringu käivitamine** DMF-i REST API [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) kutsumiseks.

        - **Meetod:** POST
        - **Taotluse URL:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **Taotluse keha:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![Tegevus GetExportedPackageURL.](media/integration-logic-app-get-exported-package-step.png)

8. Laadige eksporditud pakett alla.

    - Lisage HTTP taotlus **GET** (sisseehitatud [HTTP konnektori tegevus](/azure/connectors/connectors-native-http)), et laadida pakett alla URL-ilt, mis eelmises etapis tagastati.

        - **Meetod:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > Võimalik, et peate sisestama väärtuse **URI** kas koodi vaates või kujundaja funktsioonide redaktoris.

        ![HTTP GET tegevus.](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > See taotlus ei nõua ühtegi täiendavat autentimist, kuna API **GetExportedPackageUrl** tagastatav URL sisaldab ühiskasutusega juurdepääsu allkirja luba, mis annab juurdepääsu faili allalaadimisele.

9. Salvestage allalaaditud pakett, kasutades konnektorit [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness).

    - Lisage OneDrive for Businessi tegevus [Loo fail](/connectors/onedriveforbusinessconnector/#create-file).
    - Ühendage vastavalt vajadusele oma OneDrive for Businessi konto.

        - **Kausta tee:** teie valitud kaust
        - **Failinimi:** worker\_package.zip
        - **Faili sisu:** keha eelmisest etapist (dünaamiline sisu)

        ![Faili loomise tegevus.](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>3. etapp: loogikarakenduse testimine

Oma loogikarakenduse testimiseks valige kujundajas nupp **Käivita**. Näete, et loogikarakenduse etapid algavad. Pärast 30 kuni 40 sekundit peaks loogikarakendus lõpetama töötamise ja teie OneDrive for Businessi kaust peaks sisaldama uut pakettfali, mis sisaldab eksporditud töötajaid.

Kui mõnes etapis esitatakse tõrge, valige kujundajas nurjunud etapp ja kontrollige selle väljasid **Sisendid** ja **Väljundid**. Siluge ja reguleerige etappi tõrgete kõrvaldamiseks vastavalt vajadusele.

Järgmisel joonisel on näha, kuidas Logic Apps Designer välja näeb, kui kõik loogikarakenduse etapid töötavad edukalt.

![Edukas loogikarakenduse käitamine.](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Kokkuvõte

Selles õpetuses saite teada, kuidas kasutada loogikarakendusi, et eksportida andmeid rakendusest Human Resources, ja salvestada eksporditud andmed OneDrive for Businessi kausta. Saate selle õpetuse etappe vastavalt vajadusele muuta, et need vastaksid teie ettevõtte vajadustele.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
