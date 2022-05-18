---
title: Soodustuse halduse tööruum
description: Selles teemas kirjeldatakse soodustuste halduse tööruumi rakenduses Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e7f606ae3c5c0a66764cc3235837380725241f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690023"
---
# <a name="benefits-management-workspace"></a>Soodustuse halduse tööruum


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Selles teemas kirjeldatakse **soodustuste halduse** tööruumi rakenduses Dynamics 365 Human Resources.

> [!NOTE]
> **Soodustuste halduse** tööruumi vaatamiseks peate esmalt funktsioonihalduse kaudu lubama funktsiooni **(Eelversioon) Soodustuste halduse tööruum**. Lisateavet funktsioonide eelversioonide lubamise kohta vt [Funktsioonide haldamine](hr-admin-manage-features.md).<br><br>![Soodustuste halduse tööruumi lubamine.](./media/hr-benefits-management-workspace-enable.png)

**Soodustuste halduse** tööruum annab teile kiiresti ülevaate soodustustest, mis nõuavad teie tähelepanu. Sellel lehel näete järgmist teavet:

- sekkumist ootavate üksuste kogusummad
- kinnitamata valikutega töötajad
- hiljuti soodustuste saamiseks registreerunud töötajad
- ees ootavate elusündmustega töötajad
- uued töötajad, kes pole registreeritud
- aktiivsete elusündmustega töötajad
- avatud registreerimistega töötajad, kes pole ühtegi lepingut valinud

![Soodustuse halduse tööruum.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Tegevusüksuste kuvamine

Tegevusüksuste kuvamiseks võite valida paani või vahekaardi. Vahekaardi valimise korral saate töötajaid vaadata ja valida tööruumi lehelt.

![Tegevusüksused.](./media/hr-benefits-management-workspace-action-items.png)

Kui valite paani, viiakse teid vastava ala lehele. Kui näiteks valite ühe neist paanidest, kuvatakse leht **Töötaja soodustuste plaanid**, kus on filtri abil esile tõstetud töötajad, kellega peate midagi tegema.

- **Kinnitamata valikud**
- **Ava välja registreeritud plaanideta registreerimised**
- **Soodustuste jaoks registreeritud**
- **Uus töötaja pole registreeritud**

![Töötaja soodustusplaanid.](./media/hr-benefits-management-workspace-plans.png)

Valides **Aktiivsed elusündmused** või **Tulevased elusündmused**, viiakse teid aktiivsete või tulevaste elusündmuste loendisse.

![Elusündmused.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Töötlemine

Registreerimiseks sobivuse, elusündmuste või tariifimuutuste uuenduste töötlemiseks valige navigeerimisribal asjakohane üksus.

![Töötlemisel.](./media/hr-benefits-management-workspace-processing.png)

Töötlemistulemuste kuvamiseks valige lehel **Protsessi tulemused**.

![Protsessi tulemused.](./media/hr-benefits-management-workspace-process-results.png)

Lisateavet soodustuste töötlemise kohta leiate siit:

- [Registreerimise sobivuse töötlemine](hr-benefits-process-enrollment-eligibility.md)
- [Elusündmuste muudatuste töötlemine](hr-benefits-process-life-event-changes.md)
- [Elusündmuste sobivuse töötlemine](hr-benefits-process-life-event-eligibility.md)
- [Elusündmuste töötlemine](hr-benefits-process-life-events.md)
- [Määra muudatuste töötlemine](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Vaheta perioodi

Muu soodustuste perioodi vaatamiseks valige see ripploendist **Periood**.

![Vaheta perioodi.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>Registreerimise vahekaardi avamine

Tegevusüksuste kuvamiseks võite valida kas paani või vahekaardi. Vahekaardi valimise korral saate töötajaid vaadata ja valida tööruumi lehel.
Vahekaardil **Avatud registreerimine** antakse avatud registreerimisprotsessi võtmemõõdud. 

Avatud registreerimisega seotud teave kuvatakse 30 päeva enne **Registreerimise alguskuupäeva**. See määratletakse **Perioodide** seadistuses **Soodustuste haldus** > **Lingid** > **Perioodid** väljal **Registreerimise alguskuupäev**.  Selle sätte muutmiseks minge inimressursside jagatud **parameetritesseBenefits** > **managementOpeni** > **registreerimisvalikud** ja värskendage **välja arv**.  

Järgmine teave on saadaval vahekaardil **Avatud registreerimine**:
 - Töötajad, kes ei ole avatud registreerimisprotsessi alustanud
 - Töötajad, kellel on valimised toimumas
 - Töötajad, kellel on valimiste protsess lõpule viidud
 - Kinnitamata valikud

**Kokkuvõttepaanid**

- **Alustamata** – **Alustamata** paan kuvab töötajate arvu, kes pole registreerimisprotsessi alustanud. **Alustamata** paanil on filtreeritud loend, milles kuvatakse ainult need töötajad, kelle plaanid ei ole valitud, loobutud või avatud registreerimisplaani perioodi kohta välja registreeritud. Kohustuslikke plaane ignoreeritakse ja neid ei kaasata, kuna need on töötaja jaoks vaikimisi valitud.  Saate minna tagasi sellele paanile, et vaadata töötajate loendit, kes ei ole **Töötaja soodustuste plaani** lehel avatud registreerimisprotsessi alustanud.

  > [!NOTE]
  > Kui te ei soovi jälgida **Plaani tüübi** avatud registreerimise edenemist, saate selle välistada, kui kasutate **Soodustuste haldus** > **Lingid** > **Töötaja iseteeninduse parameetrid** > **Soodustuse plaani paani häälestus** ja värskendades välja **Jälgi avatud registreerimise edenemist**.  Näiteks võib olla loodud plaane, millel **Plaani tüüp** = **Muu**. Need plaanid võivad olla valikulised plaanid, mille puhul te ei soovi jälgida registreerimise edenemist. Kui te seda plaanitüüpi ei vali, eiratakse seda tüüpi plaane registreerimiste jälgimisel või lõpetamisel vahekaardil **Avatud registreerimine**. See säte rakendub plaani tüübile, mis valitakse kõigi perioodide ja juriidiliste isikute puhul.

- **Pooleli** – **Pooleli** paanil on töötajate arv, kellel on valimised pooleli. Paanil **Pooleli** on filtreeritud loend, mis näitab ainult töötajaid, kes omavad vähemalt ühte loobutud või valitud plaani. Kohustuslikke plaane ignoreeritakse ja neid ei kaasata, kuna need on töötaja jaoks vaikimisi valitud. Sellest paanist saate tagasi minna, et näha töötaja soodustusplaanide hulgivärskenduse lehel valitud **ja loobutud plaane**.

- **Registreeritud soodustusteks** – **Registreeritud soodustusteks** paanil on kaasatud töötajate arv, kes on registreeritud soodustusteks. **Registreeritud soodustusteks** paanil on filtreeritud loend, mis näitab kõiki plaanidest valitud või sellest loobunud töötajaid. Päring välistab plaanid, mida ei jälgita avatud registreerimise jaoks lehel **Töötaja iseteeninduse parameetrid**. Sellelt paanilt saate tagasi minna, et vaadata töötajate loendit **Töötaja soodustuse plaanide** lehel.

- **Kinnitamata valikud** – **Kinnitamata valikute** paanil kuvatakse töötajate arv, kes on valitud või loobunud plaanidest, mis tuleb kinnitada. Sellest paanist saate tagasi minna, et kuvada töötaja **soodustusplaanide hulgivärskenduse** leht.

**Tegevus**

- **Alustamata** - **Alustamata** vahekaart kuvab töötajate nimekirja, kes pole registreerimisprotsessi alustanud. **Alustamata** paanil on filtreeritud loend, milles kuvatakse need töötajad, kelle plaanid ei ole valitud, loobutud või avatud registreerimisplaani perioodi kohta välja registreeritud. Kohustuslikke plaane ignoreeritakse ja neid ei kaasata, kuna need on töötaja jaoks vaikimisi valitud. **Töötaja soodustusplaanide üksikasjade** lehe kuvamiseks saate töötajal süvitsi minna.

- **Valimised pooleli** – **Valimised pooleli** vahekaardil on töötajate nimekiri, kellel on valimised pooleli. Paanil **Valimised pooleli** on filtreeritud loend, mis näitab töötajaid, kes omavad vähemalt ühte loobutud või valitud plaani. Kohustuslikke plaane ignoreeritakse ja neid ei kaasata, kuna need on töötaja jaoks vaikimisi valitud. **Töötaja soodustusplaanide üksikasjade** lehe kuvamiseks saate töötajal süvitsi minna.

## <a name="view-more-options"></a>Kuva rohkem variante

Lisateabe ja muude toimingute vaatamiseks valige **Lingid**.

![Lingid.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Vt ka

[Soodustuste halduse ülevaade](hr-benefits-management-overview.md)
