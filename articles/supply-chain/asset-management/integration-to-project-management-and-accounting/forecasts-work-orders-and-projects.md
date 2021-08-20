---
title: Ennustused, töökäsud ja projektid
description: Selles teemas kirjeldatakse ennustuste ja töökäsu integratsiooni projekti halduse ja varahalduse raamatupidamismooduliga.
author: johanhoffmann
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b53dcf4e8796f808283b7bd5ea92b869ee0e59aac5359d74bcdc5de37ea7352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770332"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognoosid, töökäsud ja projektid

[!include [banner](../../includes/banner.md)]

 

Varade halduses aitab integreerimine mooduliga **Projekti haldus ja raamatupidamine** optimeerida kulu, et kasutajad saaksid jälgida hooldustöö tüübi ennustuste ja töökäsu tööde kulusid.

Hooldustöö tüübi ennustuste jälgimiseks peab seadistama kahte seadet:

1. Valige projekt **Varade haldus** > **Seadistus** > **Varade halduse parameetrid** ja seejärel vahekaardil **Varad** > **Projekti** vahelehel, väljal **Hooldusprognoosi projekt** valige projekt.

2. Hooldustöö tüübi tavarea loomisel luuakse automaatselt **Hooldustöö tavatüübid** lehel olevale reale tegevuse number (**Varahaldus** > **Seadistus** > **Tööd** > **Hooldustöö tavatüübid**).

Hooldustöö tüübi prognoosidel on kaks eesmärki: 

- Hooldustöö tüübi prognooside kulusid saate jälgida moodulis **Projektihaldus ja -arvestus**. 
- Prognoosid edastatakse automaatselt töökäsu töö projekti, kui valite töökäsu töö hooldustöö tüübi.

Töökäsu tööde kulud jälgimiseks peate esmalt seadistama töökäsu projektid. Lisateavet leiate jaotisest [Töökäsu projekti seadistamine](../setup-for-work-orders/work-order-project-setup.md).

## <a name="work-order-job-projects"></a>Töökäsu töö projektid

Kui loote töökäsu töö, määratakse töökäsu projekt töökäskude ülemprojekti seadistamisega lehel **Töökäsu projekti seadistamine** (**Varade haldus** > **Seadistamine** > **Töökäsud** > **Projekti seadistamine**).

Töökäsu töö projekte luuakse järgmise töökäsu teabe kombinatsiooni alusel:

- Töökäsus valitud tüüp 
- töökäsu varaga seotud töö asukoht;
- Vara tüüp, mis on seotud töökäsu varaga  
- Töökäsule seatud eeldatavad algus- ja lõpuajad  

Osa sellest teabest ei pruugi töökäsul leida. Seega otsitakse töökäsu ülemprojekti saadaval andmete kombinatsiooni alusel ja valides projekti ID, mis vastab töökäsu andmetele.

Näiteks järgmisel joonisel on varatüübi **Veoki mootor** seadistamise viisi tõttu iga töökäsu töö, mis luuakse varatüübiga **Veoki mootor** projekti ID 000186 alamprojekt.

![Joonis 1.](media/01-integration-to-pma.png)

Projekti ID eesmärk töökäsu tööl ja sellega seotud tegevuse numbri eesmärk on jälgida töökäsu tööga seotud kulusid ja sellel valitud vara moodulis **Projektihaldus ja -arvestus**. (Projekti ID ja tegevuse numbri vaatamiseks **Varade haldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** ja valige töökäsk. Vahekaardil **Rea üksikasjad** kuvatakse väljal **Projekti ID** projekti ID ja väljal **Tegevuse number** kuvatakse tegevuse number.) Lisateavet varade haldamise kulukontrolli kohta vt [Kulude ja kuupäeva kontroll](../controlling-and-reporting/cost-and-date-control.md).

Järgmisel joonisel on kujutatud graafiline ülevaade töökäsu projektidest ja sellega seotud projektitegevustest.

![Joonis 2.](media/02-integration-to-pma.png)

Kui töökäsus luuakse uus töö, luuakse selle jaoks automaatselt projekt. Töökäsu tööga seotud vara finantsdimensioonid edastatakse automaatselt töökäsu projekti.

Töökäsu töö jaoks loodud projektitegevusel on sellega seotud teave. See teave on hooldustöö tüübi, hooldustöö tüübi variandi ja kaubanduse kohta. Sellest on kasu näiteks töökäsu ostutellimuse loomisel (vt [Hankimine](../work-orders/procurement.md)) või mooduli **Projekti haldus ja raamatupidamine** kasutamisel aja registreerimiseks.

Kui vara paigaldati funktsionaalsesse asukohta, kuid hiljem paigaldati teisele funktsionaalsele asukohale, värskendatakse selle varaga automaatselt uue funktsionaalse asukohaga seotud finantsilisi dimensioone. Seejärel, kui loote vara töökäsu töö, saab töökäsu töö projekt automaatselt nüüd varaga seotud finantsilised dimensioonid. Seega kui kasutate töö asukohti, saab alati jälgida töö asukohtade, kuhu vara paigaldati mistahes ajal, kulusid. Finantsiliste dimensioonide automaatne värskendamine aitab tagada projekti kontrolli ja aruandluse kulude täieliku jälgitavuse.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Töökäsu projektid, töökäsu tsükli olekud, projekti etapid ja projekti tüübid

Et tagada töökäsu tsükli olekute ja nendega seotud projekti etappide õiget kasutamist, kaaluge mooduliga **Projektihaldus ja -arvestus** seotud sõltuvusi:

- Mooduli **Projekti haldus ja -arvestus** projekti etapid on seadistatud projekti tüüpidega lehel **Projektihalduse ja -arvestuse parameetrid**.  
- Valige lehel **Projektihalduse ja -arvestuse parameetrid** märkeruudud, et valida kõigi kasutatavate projektitüüpide jaoks asjakohased projektietapid. Järgmistel joonistel on valitud viis etappi projektitüüpide **Aeg ja materjal** ja **Sisemine** jaoks (**Loodud**, **Hinnatud**, **Ajastatud**, **Pooleli** ja **Valmis**) . Need viis etappi on vajalikud nii sisemiste hooldustööde kui ka teenuse hoolduse töödele.
- Moodulis **Varade haldus** määratletakse projektitüübid projektigruppidega, mille seadistate **Töökäsu projekti seadistuse** lehel > vahekaardil **Projektigrupp** (**Varade haldus** > **Seadistus** > **Töökäsud** > **Projekti seadistus**).  
- Valiku **Töökäsu projekti seadistus** lehel olevat projekti rühmade seadistust kasutatakse uute töökäskude loomisel. Kui luuakse töökäsk, koostatakse selle jaoks automaatselt projekt.  
- Iga töökäsu tsükli olek peab olema seotud projekti etapiga.  
- Projekti etapp, mis on seotud töökäsu elutsükli olekuga, tuleb määratleda töökäsu projektis määratletud projektigrupi aktiivse etapina. Töökäsu projekt koostatakse automaatselt.
- Uue töökäsu loomisel põhineb töökäsu projekti automaatne eraldamine lehel **Töökäsu projekti seadistamine** oleval seadistusel.  

Järgmised joonised näitavad seoseid töökäsu projekti gruppide, seotud projektitüüpide, projekti etappide ja töökäsu tsükli olekute vahel.

![Joonis 3.](media/03-integration-to-pma.png)

![Joonis 4.](media/04-integration-to-pma.png)

![Joonis 5.](media/05-integration-to-pma.png)

Lisateavet töökäsu projektide seadistamise kohta vt [Töökäsu projektide seadistus](../setup-for-work-orders/work-order-project-setup.md). Lisateavet töökäsu elutsükli olekute loomise kohta vt [Töökäsu elutsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).

Järgmisel joonisel on kujutatud erinevate projektide graafiline ülevaade, mis on loodud moodulis **Varade haldus**, et võimaldada integreerimist mooduliga **Projektihaldus ja -arvestus**. See näitab ka tööprotsesse, millega projektid on seotud.

![Joonis 6.](media/06-integration-to-pma.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]