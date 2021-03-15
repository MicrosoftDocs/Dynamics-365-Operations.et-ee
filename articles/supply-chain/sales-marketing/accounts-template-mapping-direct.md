---
title: Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks rakendusest Dynamics 365 Sales rakendusse Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0499f604049240a226b4002710817034598b1e66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977709"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Enne kui saate kasutada lahendust Potentsiaalne klient sularahaks, tutvuge [andmete integreerimisega teenusesse Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse kontode sünkroonimiseks otse rakendusest Dynamics 365 Sales rakendusse Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Andmevoog lahenduses Potentsiaalne klient sularahaks

Lahendus Potentsiaalne klient sularahaks kasutab andmete integreerimise funktsiooni andmete sünkroonimiseks rakenduste Supply Chain Management ja Sales vahel.  Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Supply Chain Management ja Sales. Järgmine illustratsioon näitab, kuidas sünkroonitakse andmeid rakenduste Supply Chain Management ja Sales vahel.

[![Andmevoog lahenduses Potentsiaalne klient sularahaks](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Saadaolevatele mallidele juurdepääsemiseks avage [Power Apps administreerimiskeskus](https://preview.admin.powerapps.com/dataintegration). Valige **Projektid** ja seejärel paremas ülanurgas **Uus projekt**, et valida avalikud mallid.

Kontode sünkroonimiseks rakendusest Sales rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

- **Andmete integratsioon malli nimi:** Kontod (rakendusest Sales rakendusse Fin and Ops) – otse
- **Ülesande nimi projektis:** Kontod – Kliendid

Enne konto/kliendi sünkroonimist ei ole vaja teha ühtki sünkroonimisülesannet.

## <a name="entity-set"></a>Üksuste komplekt

| Müük    | Supply Chain Management |
|----------|------------------------|
| Kontod | Kliendid V2           |

## <a name="entity-flow"></a>Üksuse voog

Kontosid hallatakse rakenduses Sales ja need sünkroonitakse rakendusega Supply Chain Management klientidena. Nende klientide atribuudi **On väliselt hallatav** sätteks on määratud **Jah**, et jälgida rakendusest Sales pärit kliente. Arveldamise ajal kasutatakse seda teavet rakendusega Sales sünkroonitud arvete filtreerimiseks.

## <a name="prospect-to-cash-solution-for-sales"></a>Lahendus Potentsiaalne klient sularahaks rakendusele Sales

Veerg **Konto number** on saadaval lehel **Konto**. See on loomulik ja kordumatu võti, et toetada integratsiooni. Kliendisuhete halduse (CRM) lahenduse loomuliku võtme funktsioon võib mõjutada kliente, kes juba kasutavad veergu **Konto number**, kuid ei kasuta iga konto puhul atribuudi **Konto number** kordumatuid väärtusi. Praegu ei toeta integratsioonilahendus seda juhtumit.

Kui uue konto loomisel ei ole atribuudi **Konto number** väärtust veel olemas, luuakse see automaatselt numbriseeriat kasutades. Väärtus sisaldab sõnet **ACC**, millele järgneb suurenev numbriseeria ja seejärel kuuest tähemärgist koosnev järelliide. Näide: **ACC-01000-BVRCPS**

Kui rakendatakse integratsioonilahendust rakendusele Sales, seab täiendusskript veeru **Konto number** olemasolevatele kontodele rakenduses Sales. Kui ühtki atribuudi **Konto number** väärtust ei ole, kasutatakse varem mainitud numbriseeriat.

## <a name="preconditions-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

- Atribuudi **CustomerGroupId** vastendust tuleb värskendada rakenduses Supply Chain Management kehtivale väärtusele. Saate määrata vaikeväärtuse või määrata väärtuse väärtuskaardi abil.

    Malli vaikeväärtus on **10**.

- Kui lisate järgmised vastendused, saate vähendada rakenduses Supply Chain Management nõutavate käsitsi värskenduste arvu. Saate kasutada vaikeväärtust või väärtuskaarti näiteks valikust **Riik/piirkond** või **Linn**.

    - **SiteId** – sait on vajalik pakkumiste ja müügitellimuse ridade loomiseks rakenduses Supply Chain Management. Vaikesaidi võib võtta kas tootelt või kliendilt tellimuse päises.

        Malli vaikeväärtus on **1**.

    - **WarehouseId** – ladu on vajalik pakkumiste ja müügitellimuse ridade töötlemiseks rakenduses Supply Chain Management. Vaikelao võib võtta kas tootelt või kliendilt tellimuse päises rakenduses Supply Chain Management.

        Malli vaikeväärtus on **13**.

    - **LanguageId** – keel on vajalik pakkumiste ja müügitellimuste loomiseks rakenduses Supply Chain Management. Vaikimisi kasutatakse kliendilt saadud tellimuse päises olevat keelt.

        Malli vaikeväärtus on **en-us**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

> [!NOTE]
> Veerud **Maksetingimused**, **Veosetingimused**, **Tarnetingimused**, **Saatmisviis** ja **Tarneviis** ei ole vaikevastenduste osa. Nende veergude vastendamiseks peate seadistama väärtuskaardi, mis on kohane neis organisatsioonides olevatele andmetele, mille vahel tabelit sünkroonitakse.

Järgmisel joonisel on toodud näide malli vastendusest andmete integratsioonis. 

> [!NOTE]
> Vastendamine näitab, millise veeru teave sünkroonitakse rakendusest Sales rakendusse Supply Chain Management.

![Malli vastendamine andmete integratsioonis](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Seotud dokumendid


[Potentsiaalne klient sularahaks](prospect-to-cash.md)

[Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega](accounts-template-mapping-direct.md)

[Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega](contacts-template-mapping-direct.md)

[Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel](sales-order-template-mapping-direct-two-ways.md)

[Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]