---
title: Töökandidaatide värbamine
description: See teema kirjeldab, kuidas värvata kandidaate Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef2f2c82708fd48055faa7546e7e0c4da51e7b6c
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733981"
---
# <a name="recruit-job-candidates"></a>Töökandidaatide värbamine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources aitab teil värbamistaotlusi hallata. Samuti aitab see teil sujuvalt kandidaadid töövõtjateks üle viia. Kui teie organisatsioon kasutab eraldi värbamisrakendust, võib teie värbamisprotsess hõlmata järgmisi etappe.<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- Sisestate värbamistaotluse rakendusse Human Resources.
- Saate värbamisrakenduse kaudu kandidaatide soovitused kätte rakenduses Human Resources.
- Viite kandidaadi kinnitamise lõpule rakenduses Human Resources.

Kui te ei kasuta eraldi värbamisrakendust, saate rakenduses Human Resources kandidaate ka käsitsi hallata.

> [!NOTE]
> Kui olete administraator või arendaja ja soovite integreerida Inimressursid kolmanda osapoole värbamisrakendusega, [Dataverse](hr-admin-integration-common-data-service.md) minge valikute Konfigureeri integratsioon ja Virtuaaltabelite konfigureerimine [Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)
>
> Lisaks saate otsida värbamisrakendusi siit: [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Värbamistaotluste lubamine ühendatud infrastruktuuris

Kui soovite värbamistaotlusi esitada inimressursside värbamises, peate esmalt lubama inimressursside **kasutajakogemuse** **ja värbamisprotsessi haldusfunktsioonid**.

Kui funktsioonid on sisse lülitatud, valige järgmiste sammudega funktsioon: 
1. Avage **inimressurssidesetupHuman** > **·** > **ressursside parameetrid**.
2. Seadke väljal  **Recruitmentment**  väli Värbamine **keelatud valikule** **Ei**.
3. Valige värbamiskogemuse **ripploendist** inimressursside **värbamine**.   

> [!Note] 
> Kui **inimressursside värbamine** on valitud, **siis on** värbamisprojektid (pärand) kirjutuskaitstud. 


## <a name="add-a-recruiting-request-location"></a>Värbamistaotluse asukoha lisamine

Kui teie organisatsioonil on mitu asukohta, saate need lisada, et taotluse esitajad saaksid valida asukoha, kus uus töövõtja tööle hakkab. Asukoht lisatakse töökuulutusele.

1. Otsinguribal sisestage värbamistaotluse **asukoht**.
2. Valige suvand **Uus**.
3. Sisestage asukoha nimi väljale **Värbamistaotluse asukoht**.

    ![Värbamistaotluse asukoha lisamine.](./media/hr-recruit-0a-add-location.png)

4. **Kirjelduse** jaoks sisestage asukoha kirjeldus.
5. Valige jaotises **Asukoht** nupp **Lisa**. Kui kuvatakse **dialoogiboks** Uus aadress, sisestage asukoha aadress.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Sisestage aadress.](./media/hr-recruit-0b-address.png)

6. Jaotises **Kontaktteave** sisestage asukoha kontaktisiku teave.
7. Valige käsk **Salvesta**.

## <a name="add-a-recruiting-request"></a>Värbamistaotluse lisamine

Rakenduse Human Resources saavad juhid värbamistaotlusi esitada. Kui kasutate eraldi värbamisrakendust ja viite need toimingud lõpule, saadetakse värbamisrakendus ja vastavas rakenduses alustatakse värbamisprotsessi. Muul juhul viige see protseduur lõpule, et alustada töövoogu ettevõttesisese värbamisprotsessiga.

1. Valige **Töövõtja iseteenindus**.
2. Valige vahekaart **Minu töörühm**.
3. Valige **värbamistaotlus**.

    ![Värbamistaotluse alustamine.](./media/hr-recruit-1-request-to-recruit.png)

4. Täitke väli **Kirjeldus**, **Töö** ja **Eeldatav alguskuupäev**.

    ![Värbamistaotluse lõpuleviimine.](./media/hr-recruit-2-request-to-recruit.png)

5. Valige nupp **Jätka**. Kuvatakse teie ametikoha värbamistaotlus.
6. Valige **jaotises** Üldine värbamistaja ripploendist **värbaja** **ja seejärel valige asukoht värbamise nõude asukoha** ripploendist.
7. Jaotises **Töö** muutke teavet vastavalt vajadusele ja seejärel valige käsk **Loo töö põhjal üksikasjad**.

    ![Loo töö põhjal üksikasjad.](./media/hr-recruit-3-create-details-from-job.png)

    Ülejäänud värbamistaotlus täidetakse vaiketeabega teie sisestatud töö kohta.

8. Sisestage jaotises **Väline kirjeldus** ettevõtteväline töökirjeldus.
9. Jaotises **Ametikohad** valige nupp **Lisa** ja seejärel selle värbamistaotluse ametikoht.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Ametikoha lisamine.](./media/hr-recruit-4-select-position.png)

10. Jaotises **Oskused** valige nupp **Lisa** ja seejärel valige oskus.
11. Valige **jaotises Haridusnõuded** **suvand** Lisa ja seejärel valige väärtused **haridus-** **ja haridustaseme** rippmenüüdest.

    ![Haridusnõuete lisamine.](./media/hr-recruit-5-select-educational-requirements.png)

12. Jaotises **Kommenteerimine** lisage vajaduse korral kommentaarid.
13. Valige **suvandi** Hüvitus all tase ripploendist **Tase** **ja** seejärel korrigeerige vastavalt vajadusele madal lävi, **kontrollpunkt** **ja kõrge** lävi.
14. Kui teie värbamistaotlus on lõpule viidud ja olete valmis alustama värbamisprotsessi, valige menüüribalt käsk **Aktiveeri**.

    ![Värbamistaotluse aktiveerimine.](./media/hr-recruit-6-activate-recruit-request.png)

15. Valige käsk **Salvesta**.

## <a name="view-and-edit-your-recruiting-requests"></a>Värbamistaotluste kuvamine ja muutmine

Kui olete juht ja soovite oma taotlusi vaadata, tehke järgmist.

1. Valige **Töövõtja iseteenindus**.
2. Valige vahekaart **Minu töörühm**.
3. Jaotises **Minu töörühma teave** valige vahekaart **Värbamistaotlused**.

    ![Värbamistaotluste vahekaardi valimine.](./media/hr-recruit-7-recruiting-requests.png)

4. Värbamistaotluse vaatamiseks või muutmiseks valige see ruudustikus.

Kui olete personalispetsialist ja soovite vaadata kõiki värbamistaotlusi, tehke järgmist.

1. Valige **Personalihaldus**.
2. valige **Värbamistaotlused**.

    ![Personalihalduse kaudu värbamistaotluste kuvamine.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. Värbamistaotluse vaatamiseks või muutmiseks valige see ruudustikus.

## <a name="add-or-edit-a-candidate-profile"></a>Kandidaadi profiili lisamine või muutmine

Kui teie organisatsioon on integreeritud mõne muu rakendusega, et hallata värbamisaotlusi, edastatakse värbamistaotlused sellele rakendusele. Värbamisrakendus saadab seejärel kandidaadi teabe tagasi rakendusele Human Resources. Muidu saate jälgida ettevõttesiseseid värbamisprotsesse ja kandidaaditeavet sisestada käsitsi.

1. Valige **Personalihaldus**.
2. Valige **Lingid**.
3. Jaotises **Värbamine** valige **Kandidaadid**.

    ![Kandidaatide kuvamine.](./media/hr-recruit-9-candidates.png)

4. Kandidaadi lisamiseks valige nupp **Uus**. Olemasoleva kandidaadi redigeerimiseks valige loendist aadress ja seejärel valige **Redigeeri**. Kuvatakse kandidaadi profiil.
5. Jaotises **Kandidaadi ülevaade** saate kandidaadi teavet vajaduse korral sisestada või redigeerida.
6. Jaotises **Värbamistaotlus** valige kandidaadi linkimiseks värbamistaotlus. Seejärel täitke väljad **Hinnanguline alguskuupäev**, **Palkamise juht**,**Ametikoht** **ja** Kirjeldus vastavalt vajadusele.

    ![Värbamistaotluse link.](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Lisage kõik andmed järgmistes valdkondades, mida soovite kandidaadi kirjele lisada.

    - **Kommentaarid**
    - **Töökogemus**
    - **Kontaktandmed**
    - **Haridus**
    - **Oskused**
    - **Serdid**
    - **Skriiningud**

8. Valige käsk **Salvesta**.

## <a name="hire-a-candidate"></a>Kandidaadi palkamine

Kui olete kandidaadi palkamiseks valmis, järgige seda protseduuri, et muuta kandidaat töövõtjaks.

1. Valige leheküljel **Kandidaat** suvand **Palka**.

    ![Kandidaadi palkamine.](./media/hr-recruit-11-hire.png)

2. Täitke kõik **väljad** lehel Uue töötaja **palkamine** jaotises Üksikasjad.

    ![Palgatud töövõtja üksikasjade sisestamine.](./media/hr-recruit-12-hire-new-worker.png)

3. Jaotises **Ametikoha üksikasjad** kontrollige ja muutke vajaduse korral teavet.
4. Valige jaotisest **Palkamise kontroll-loendid** selle töövõtja jaoks asjakohased kontroll-loendid.
5. Valige **Jätka**, et luua töötaja kirje.

    > [!NOTE]
    > Sõltuvalt teie organisatsiooni töövoogudest võib kandidaadi kirje enne töötajakirjeks muutumist läbida lisa kinnitustoiminguid.

## <a name="decide-not-to-hire-a-candidate"></a>Otsus kandidaati mitte palgata

Kui otsustate kandidaati mitte palgata, järgige seda protseduuri, et eemaldada ta taustakontrollist. 

1. Valige leheküljel **Kandidaat** suvand **Ära palka**.

    ![Kandidaadi mittepalkamine.](./media/hr-recruit-13-do-not-hire.png)

2. Saate valida **Põhjuse koodi** ja kommentaare lisada.
3. Valige nupp **OK**.

## <a name="dismiss-a-candidate"></a>Kandidaadist loobumine

Vajaduse korral saate kandidaadist pärast tema palkamist loobuda. Näiteks võib kandidaat teie pakkumise tagasi lükata või ei ilmu esimesel päeval kohale.

- Valige kandidaadi **leheküljelt** vallandamise **kandidaat**.

    ![Loobu kandidaadist.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Vt ka

[Dataverse'i virtuaalsete tabelite konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Tööjõu korraldamine](hr-personnel-departments-jobs-positions.md)<br>
[Töö komponentide häälestus](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
