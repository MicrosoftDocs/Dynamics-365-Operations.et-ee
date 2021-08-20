---
title: Laovarude manuaalse liigutamise edasilükatud töötlemine
description: See teema kirjeldab, kuidas kasutada laovarude manuaalse liigutamise edasilükatud töötlemist Dynamics 365 Supply Chain Management Microsoftis.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a15c913c876e961c6824c1e8812ab2be2d6ffa4333cd0d4e6f80cae8bac79394
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746743"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Laovarude manuaalse liigutamise edasilükatud töötlemine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas kasutada laovarude manuaalse liigutamise edasilükatud töötlemist Dynamics 365 Supply Chain Management Microsoftis.

Edasilükatud töötlemine võimaldab laotöötajatel jätkata muude töödega, kui asetamistoiminguid taustal töödeldakse. Edasilükatud töötlemine on kasulik ka siis, kui serveris võib esineda töötlusaja kohatisi või plaanivälist suurenemist ja suurenenud töötlusaeg võib mõjutada kasutaja tootlikkust. Varude *liikumise* töötüüp on nüüd lisatud töötüüpide komplekti, mida see funktsioon toetab.

Taustatöötlus on saavutatud lao rakenduse [Process app sündmuste funktsiooni](warehouse-app-events.md) abil.

## <a name="turn-on-this-feature-for-your-system"></a>Selle funktsiooni sisselülitamine teie süsteemi jaoks

Selle funktsiooni sisselülitamiseks lubage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) järgmiseid funktsioone. Need tuleb sisse lülitada selles järjekorras:

1. Organisatsiooniülene töö blokeerimine
1. Laorakenduse sündmuste töötlemine
1. Edasilükatud asetamistoimingud
1. Varude käsitsi paigutamise toimingu edasilükatud töötlemine

## <a name="configure-the-work-processing-policies"></a>Töö töötluspoliitikate konfigureerimine

Edasilükatud töötlemise kasutamiseks peate seadistama ja kasutama töö töötlemise poliitikat. Edasilükatud panemise töötlemiseks toetab lao töö edasilükatud töötlemine järgmisi töötüüpe: [müügitellimus](deferred-put.md), *üleviimistellimuse väljaminek* ja *varude* *ülekandmine*. Käsitsi *liikumise toimingu funktsioonide edasi lükatud* töötlus lisab uue töö tüübi: *lao liikumised*.

Töö töötluspoliitika häälestamiseks tehke järgmist.

1. Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Töö töötluspoliitikad**.
1. Valige loendist olemasolev poliitika või looge uus poliitika, valides tegevuspaanil suvandi **Uus**. Iga poliitika päisel on järgmised väljad:

    - **Töö töötluspoliitika nimi** – töö töötluspoliitikale antud nimi.
    - **Kirjeldus:** – töö töötluspoliitika kirjeldus.

1. **Kiirkaardil Töötlusreeglid** seadistage reeglite kogum, mida poliitika rakendab. Kasutage järgmisi nuppe tööriistaribal, et lisada ja eemaldada reegleid vastavalt teie vajadustele. Määrake igale reeglile järgmised väljad.

    - **Töö tellimuse tüüp** – valige töö tüüp, mille suhtes poliitika kehtib.
    - **Toiming** – valige toiming, mida poliitikaga töötlemiseks kasutatakse. Kui valisite lao liikumise väljal *Töötellimuse tüüp*, ei pea te seda välja seadistama, kuna nii noppimis- kui panemistoiminguid töödeldakse ühe **sündmusena**.
    - **Töö töötlemismeetod** – valige töörea töötlemiseks kasutatav meetod. Kui valitakse suvand *Viivitamatu*, meenutab käitumine käitumist, kui töö töötlemise poliitikaid kasutatakse rea töötlemiseks. Kui valite *edasi lükatud*, rakendab süsteem edasilükatud töötlust, mis kasutab pakktöötluse raamistikku.
    - **Edasilükatud töötlemislävi** – kui seate selle välja väärtuseks *0* (null), lävend puudub. Sel juhul kasutatakse *edasilükatud* töötlemist, kui seda saab kasutada. Kui konkreetne lävearvutus jääb allapoole läve, kasutatakse meetodit *Viivitamatu*. Muul juhul kasutatakse meetodit *edasilükatud*, kui seda saab kasutada. Müügi ja ülekandega seotud töö puhul arvutatakse lävi seotud allika koormusridade arvuga, mida töö jaoks töödeldakse. Täiendustöö puhul arvutatakse lävi tööridade arvuga, mida töö abil täiendatakse. Kui määrate müügi läveks näiteks *5*, on tagatud, et vähemate kui viie allika koormusreaga väiksemate tööde puhul ei kasutata edasilükatud töötlemist, kuid suuremad tööd kasutavad seda. Lävi toimib ainult siis, kui **töö töötlemise meetodiks** on määratud *Edasilükatud*.
    - **Edasilükatud pakktöötluse grupp** – määrake töötlemiseks kasutatav partiigrupp. Kui valisite lao liikumise väljal *Töötellimuse tüüp*, ei pea te seda välja seadistama, kuna **pakktöötluse grupp** on valitud dialoogiaknas **Lao töötlemiserakenduse sündmused**.

## <a name="assign-the-work-creation-policy"></a>Töö loomise poliitika määramine

Üksikasju töö loomispoliitika määramise kohta vt jaotisest [laotöö edasilükatud töötlemine](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Pakett-töö seadistamine laorakenduse sündmuste töötlemiseks

Lao liikumise *käsitsi toimingu protsessi edasilükkumise kasutamiseks* seadistage plaanitud pakett-töö.

1. Avage **Laohaldus \> Perioodilised ülesanded \> Laorakenduse sündmuste töötlemine**.
1. Valige dialoogiboksis **Lao rakenduse sündmuste töötlemine** kiirkaardil **Käivita taustal** suvandi **Pakktöötlus** väärtuseks *Jah*.
1. Valige **Kordumine** ja seadistage äritegevuse nõuetele vastavad käitusgraafikud.
1. Valige igas dialoogiboksis **OK**.

## <a name="inquire-about-the-warehouse-app-events"></a>Laorakenduse sündmuste päring

Saate vaadata sündmuste järjekorda ja laorakenduse loodud sündmuseteateid, avades **Laohaldus \> Päringud ja aruanded \> Mobiilse seadme logid \> Laorakenduse sündmused**.

*Varude liikumissündmuse* teadete olekuks on pärast *esmaloomist* järjekorras. See staatus näitab, et pakett-töö **Laorakenduse töötlemine sündmused** võtab sündmuseteated ette ja töötleb neid. Kui olekuks määratakse *Lõpetatud*, kustutatakse kõik seotud sündmused järjekorrast.

Kõik  *lao liikumissündmused* akumuleerutakse ühe kogumi alusel sündmuse tüübi ja lao kohta.

Pakett-töö töötleb laorakenduse sündmusi vastavalt kordumisele, mis on seadistatud dialoogiaknas **Lao rakenduse sündmuste töötlemine**. Seega, kuni teadet töödeldakse, leiate lao ID väljalt **Identifikaator**.

Sõnumi üksikasjad sisaldavad liikumise üksikasju (nt asukohad Alates ja Kuni).

Lisateavet leiate teemast [Laorakenduse sündmuse töötlemine](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobiilse seadme menüü konfigureerimine viivitatud töötlemise poliitika vahelejätmiseks

Üksikasju mobiilse seadme menüü konfigureerimiseks, et edasilükatud töötlemispoliitika vahele jätta, vt [laotöö edasilükatud töötlemine](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Mõju suletud töö kuupäevadele

Lisateavet suletud töökuupäevade mõju kohta vt jaotist [laotöö edasilükatud töötlemine](deferred-put.md).

## <a name="additional-resources"></a>Lisaressursid

- [Laotöö töötlemise edasilükkamine](deferred-put.md)
- [Laorakenduse sündmusetöötlus](warehouse-app-events.md)
- [Mobiilsete seadmete häälestus laotöö jaoks](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
