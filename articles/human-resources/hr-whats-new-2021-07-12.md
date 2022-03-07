---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (12. juuli 2021)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 12. juuli 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ebe5a6ae19d00b94247381c700ff21d31910fcac1968ab4f8a673f89ddd2f0f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782631"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (12. juuli 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4353.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
|  Teenuse aastate kuvamise lüliti | |See funktsioon võimaldab kasutada erinevaid kuupäevi, et arvutada teenuseaastaid, mis on kuvatud **Sujuvama töötajakirje** lehel ja **Inimesed** lehhel.  See on saadaval [Human Resources parameetrites](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 595871 | Human Resources paanil Teave on vale Dataverse terminoloogia | Common Data Service rebrandimisel Dataverse-ks on terminoloogiat Microsoft Dynamics 365 Human Resources-i teabepaanil uuendatud (**Spikker & tugi > Teave**). |
| 598676 | Ühtlustatud töötaja sisestusvorm ülekirjutamise ülesanne võib salvestatud vaatega kasutamisel tekitada tõrke| Kui lehel **Töötaja** on funktsioon 'Voogu salvestatud töötaja kirje' sisse lülitatud, võib rakendus nurjuda, kui salvestatud vaates on seadistatud kui **Alati redigeerimiseks avatud**. |
| 592344 |Töötajate hüvitiste jaotist positsiooni kohta tuleks lugeda ainult siis, kui hüvitiste haldamine on lubatud | Töötajate hüvitise teavet luuakse soodustuste pärandfunktsiooni kasutades.  Kui soodustuste haldus on lubatud, on väljad kirjutuskaitstud. Kui soodustuste haldus on sisse lülitatud ja **Peida soodustuste pärandvormid** väärtuseks on HR jagatud parameetrites seatud väärtusele **Jah**, on vahekaart **Töötajate hüvitis** peidetud. |
| 598617 | **HcmDiscussion** vormi aktiveerimise vahekaart põhjustab isikupärastamise rakendatud piiramatu silmuse. | Kui nii ruudustiku kui ka üksikasjade vaate valik **Alati avatud redigeerimiseks** on sisse lülitatu, on kood, mis aktiveerib vahekaardi ülekirjutatud ülesandemeetodis, on vastuolus isikupärastamisega selle kohta, millele juhtelement peaks keskenduma, ja loob lõpmatu ahela. |
| 593553 | Töölehe kuupäeva väli jõudluse töölehel kuvab UTC-s | Jõudluse töölehtede **töölehe kuupäeva** väli kuvatakse UTC ajavööndis, mitte süsteemi kuupäeva seadistuses määratletud ajavööndis, põhjustades mõnedes ajatsoonides vale kuupäeva. |
| 586930 | Jõudluseesmärkide tegevuste avamine avab täiesti erineva kirje | Kui funktsioon „Jõudlutöölehtede laiendatud aruannete vaade” on funktsioonide halduses lubatud, avab laiendatud aruannete jõudluseesmärkide vahekaardil **Minu meeskond** jaotises **Töötaja iseteenindus** valimine eesmärgid töötajale valitud töötaja asemel. |
| 569959 |  HcmPositionWorkerAssignmentV2 olem ei määra töötajat ametikohale | Kasutajad said vea ametikoha määramise kirje lisamisel olemi kaudu ja avaldamine ebaõnnestus. |
| 582259 | VETS 4212 aruanne kasutab 2017 vormi asemel 2020 vormi | Värskendatud 2020 vormingusse.  Uue vormingu laadimiseks minge **Aruande konfiguratsioonid** ja kustutage VETS-4212 aruanne vasakust veerust. Avage **Elektrooniline aruandlus – Hoidlad – HR ressurssid** ja valige **Ava**.  Valige **VETS-4212 PDF-väljaprint** ja seejärel valige käsk **Impordi**.|


## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|
|  Luba puudumiste halduril puhkusi hallata | [Luba puudumiste halduril puhkusi hallata](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Puudumiste halduri rolli konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Manustamisnõuete seadistamine puhkuse tüübi kohta | [Manustamisnõuete seadistamine puhkuse tüübi kohta](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Puhkuseühikute konfigureerimine puhkusetüübi järgi | [Puhkuseühikute konfigureerimine puhkusetüübi järgi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Lubage töötajate märkimine kui valmis maksmiseks | [Lubage töötajate märkimine kui valmis maksmiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Maksmiseks valmis](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Platvormi värskendus 10.0.20 (44) | Platvormi värskendus 10.0.20 peaks tuleb välja teenuseväljalaske raames 26. juuli 2021. Lisateavet leiate teemast [Finance and Operationsi rakenduste versiooni 10.0.20 platvormivärskendused (august 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
