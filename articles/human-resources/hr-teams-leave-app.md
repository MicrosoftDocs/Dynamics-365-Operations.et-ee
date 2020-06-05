---
title: Puhkusetaotluste haldamine Teamsis
description: Selles teemas kirjeldatakse, kuidas esitada puhkusetaotlust Microsoft Teamsi rakenduses Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393004"
---
# <a name="manage-leave-requests-in-teams"></a>Puhkusetaotluste haldamine Teamsis

[!include [banner](includes/preview-feature.md)]

Microsoft Teamsi rakendus Microsoft Dynamics 365 Human Resources võimaldab teil kiirelt esitada vaba aja taotlust ja kuvada vaba aja saldo teavet otse Microsoft Teamsis. Teabe taotlemiseks saate suhelda robotiga. Vahekaart **Vaba aeg** annab üksikasjalikumat teavet.

## <a name="install-the-app"></a>Rakenduse installimine

Rakenduse Human Resources leiate Teamsi poest.

1. Valige kolmikpunktid Microsoft Teamsis.

   ![Human Resources Teamsi puhkuse rakenduse kolmikpunktid](./media/hr-teams-leave-app-ellipses.png)
 
2. Otsige üles Dynamics 365 Human Resources ja seejärel valige paan **Human Resources**.

   ![Human Resources Teamsi puhkuse rakenduse paan HR](./media/hr-teams-leave-app-human-resources-tile.png)

3. Rakenduse installimiseks valige nupp **Lisa**.

   ![Human Resources Teamsi puhkuse rakenduse installimine](./media/hr-teams-leave-app-in-store.png)

Kui rakendus ei logi teid automaatselt sisse, valige sisselogimiseks vahekaart **Sätted**.

![Human Resources Teamsi puhkuse rakenduse vahekaart Sätted](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Kui sisselogimise dialoogiboksi ei kuvata, kontrollige oma brauseri sätteid hüpikakende lisamiseks. 

Kui teil on juurdepääs rohkem kui ühele Human Resourcesi eksemplarile, saate valida vahekaardil **Sätted** keskkonna, millega soovite ühenduse luua.

> [!WARNING]
> Rakendus ei toeta praegu süsteemiadministraatori turberolli ja kuvab tõrketeate, kui logite sisse süsteemiadministraatori kontoga. Muu kontoga sisselogimiseks valige vahekaardil **Sätted** nupp **Vaheta kontosid** ja logige sisse kasutajakontoga, millel ei ole süsteemiadministraatori privileege.
 
## <a name="use-the-bot"></a>Roboti kasutamine

Pärast rakenduse installimist kuvatakse tervitussõnum, mis teavitab teid tegevuste tüüpidest, mida robot saab teie eest teha.

![Human Resources Teamsi puhkuse rakenduse roboti tervitussõnum](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Esmakordsel suhtlemisel robotiga peate tõenäoliselt sisse logima. Kui sisselogimise dialoogiboksi ei kuvata, kontrollige oma brauseri sätteid hüpikakende lisamiseks.

Võite paluda robotil teha järgnevat.

- Vaba aja saldo teabe kuvamine iga registreeritud puhkuse tüübi kohta.

   ![Human Resources Teamsi puhkuse rakenduse saldode kuvamine](./media/hr-teams-leave-app-bot-balances.png)
 
- Konkreetse puhkuse tüübi täpsemate üksikasjade kuvamine.

   ![Human Resources Teamsi puhkuse rakenduse üksikasjade kuvamine](./media/hr-teams-leave-app-bot-details.png)

- Puhkusetaotluse alustamine teie eest.

   ![Human Resources Teamsi puhkuse rakenduse puhkusetaotlus](./media/hr-teams-leave-app-bot-request.png)
 
Pärast puhkusetaotluse käivitamist, saate kohandada päevi kaardil või valida taotlusele täiendava teabe lisamiseks **Üksikasjade redigeerimine**.

![Human Resources Teamsi puhkuse rakenduse taotluse redigeerimine](./media/hr-teams-leave-app-bot-edit.png)
 
Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks. Saate tippida ka **Salvesta mustandina**, et hiljem jätkata.

![Human Resources Teamsi puhkuse rakenduse taotluse esitamine](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Puhkuse haldamine Teamsis

Vahekaardil **Vaba aeg** saate kuvada järgnevat.

- Saldo teabe iga registreeritud puhkuse tüübi kohta

- Tulevased puhkusetaotlused

- Vaba aja taotlused

- Puhkusetaotluste mustandid

![Human Resources Teamsi puhkuse rakenduse vahekaart Vaba aeg](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Uue taotluse loomine

1. Valige uue puhkusetaotluse loomiseks **Uus taotlus**.

   ![Human Resources Teamsi puhkuse rakenduse uus taotlus](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Sisestage päev või päevad, mida soovite vabaks võtta ja seejärel valige **Lisa**.

   ![Human Resources Teamsi puhkuse rakenduse vaba aja lisamine](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Vajadusel sisestage põhjusekood. Sisestage ka vajalikud kommentaarid ja lisage manused.

4. Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks. Saate tippida ka **Salvesta mustandina**, et hiljem jätkata.

### <a name="manage-draft-requests"></a>Taotluste mustandite haldamine

1. Valige vahekaart **Mustandid**.

   ![Human Resources Teamsi puhkuse rakenduse vahekaart Mustandid](./media/hr-teams-leave-app-drafts-tab.png)

2. Taotluse redigeerimiseks valige pliiats või selle kustutamiseks prügikast.

3. Tehke vajalikud muudatused. Kui olete lõpetanud teabe sisestamise, tippige **Esita**, et esitada see heakskiitmiseks. Saate valida ka **Salvesta mustandina**, et hiljem jätkata.

   ![Human Resources Teamsi puhkuse rakenduse mustandi redigeerimine](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a>Privaatsusavaldus

Kui Dynamics 365 Human Resourcesi robot on kasutusel Microsoft Teamsis, analüüsitakse kasutaja tekstisisestusi, et mõista aluseks olevat päringut/eesmärki. Kasutaja sisestus (nt „otsing konto Contoso”) suunatakse Microsofti kognitiivsesse teenusesse nimega Language Understanding Intelligent Service (LUIS). Lugege lisateavet LUIS-i kohta  [siin](https://www.luis.ai/). Teenus LUIS eristab või mõistab kasutaja sisestuse kavatsust (antud juhul on eesmärgiks teabe leidmine) ja sihtüksust (antud juhul on soovitud üksuseks konto nimega Contoso). Seejärel edastatakse see teave Microsofti [Azure'i roboti raamistikule](https://azure.microsoft.com/services/bot-service/) , mis suhtleb Dynamics 365 Human Resourcesi andmetega ja toob kasutaja päringu vastuseks soovitud teabe. 

Kui installite ja lubate juurdepääsu roboti kasutamiseks, annate teenusele LUIS ja Azure'i roboti raamistikule nõusoleku töödelda sisestuse kavatsust, mille tulemuseks on täiustatud vestlusvaatega kasutuskogemus. Teenusel LUIS ja Azure'i roboti raamistikul võib olla võrreldes Dynamics 365 Human Resourcesiga erinev vastavuse tase. Kui teenusel LUIS on juurdepääs ainult kasutaja päringutele ja ei ole mõeldud ühendamiseks kasutaja Dynamics 365 Human Resourcesi andmete või kontoga, siis Dynamics 365 Human Resourcesi roboti kasutaja saab vabatahtlikult sisestada kliendiandmeid, isikuandmeid või muid andmeid sisaldavaid päringuid ja selle päringu sisu võidakse saata teenusesse LUIS ja Azure'i roboti raamistikku. 

Kasutaja päringute ja sõnumite sisu säilitatakse süsteemis LUIS maksimaalselt 30 päeva, krüptitakse passiivsena ja seda ei kasutata koolituse või teenuse täiustamiseks. Lisateavet kognitiivsete teenuste kohta leiate [siit](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsi rakenduste administraatori sätete haldamiseks minge [Microsoft Teamsi halduskeskusesse](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Vt ka

[Microsoft Teamsi allalaadimine ja installimine](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teams spikrikeskus](https://support.office.com/teams)</br>
[Rakendus Human Resources Teamsis](hr-admin-teams-leave-app.md)
