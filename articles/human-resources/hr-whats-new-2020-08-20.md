---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (20. august 2020)?
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 20. augusti 2020 jaoks.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c71a742022afba36c417092d5a9b75c78600357
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902165"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (20. august 2020)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3478. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Eelseisvate ja ootel puhkuste teabe kuvamine tööruumi Inimesed kaartidel

Ootel ja eelseisva puhkusetaotluse suvandid on nüüd saadaval tööruumi **Inimesed** kaartidel Puhkus ja puudumine.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Isiklik väli pole töövõtja rolli jaoks töövõtja iseteeninduses (477106) vaikimisi Jah

Välja **Privaatne** vaikeväärtus on nüüd **Jah**, kui töövõtjad lisavad uue aadressikirje töövõtja iseteeninduse lehe **Isikuandmed** lehe kaudu. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Personalihalduse palgatavate kandidaatide kiirkaardil kuvatakse kandidaatide vale arv (470110)

Lehel **Personalihaldus** kuvatakse nüüd palgatavate kandidaatide õige arv. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Lõpetatud lepinguga töövõtja haigust ei saa sisestada, kui viitvõlgade väärtuseks on seatud null (446195)

Puhkusekanded on nüüd lubatud töötajate jaoks, kelle tööleping lõpeb tulevikus ja viitvõlgade väärtuseks on seatud null. Puhkusekandeid saab sisestada kuni töövõtjaga lepingu lõpetamise kuupäevani. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Kohandatud väljade lisamine uuele töövõtjavormile keelab puhkuse haldamise toimingupaani väljad (473314)

Toimingupaani suvandid lehe **Puhkuste haldus** uuel vormil **Töövõtja** pole enam keelatud, kui vormile **Töövõtja** on lisatud kohandatud väljad.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Puhkuse kommentaarivälja kohustuslikuks muutmine võimaldab puhkusetaotlust edastada kommentaari lisamata (473543)

Kommentaarväljad saavad olla nüüd kohustuslikud ja puhkusetaotlused saavad seda sätet kasutada. Kohustuslik väli on eelversioonifunktsioon.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-üksus on saadaval lisandumise peatamiseks

Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.

## <a name="in-preview"></a>Eelvaates

### <a name="mandatory-fields"></a>Kohustuslikud väljad

Saate muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil. See funktsioon nõuab **Salvestatud vaateid**. Lisateavet salvestatud vaadete kohta leiate siit.

- [Salvestatud vaated – üldine kättesaadavus](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
- [Koostage vorme, mis täielikult kasutavad salvestatud vaateid](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateabe saamiseks vt:

- [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis
- [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Peagi tulekul

### <a name="human-resources-app-in-teams-preview-features"></a>Rakendus Human Resources Teamsis eelversioonifunktsioonid
 
-  **Teatised**: vaba aja taotluste esitajaid ja kinnitajaid teavitatakse Teamsi rakenduses Human Resources. Kinnitajad saavad vaba aja taotlusi kinnitada või tagasi lükata ja esitajaid teavitatakse sellest, kas taotlus kinnitati või lükati tagasi.
 
- **Juhi vaba aja kalender**: juhid saavad vaadata oma otseste alluvate kinnitatud ja ootel vabu aegu kalendrivaates. Selle vaate abil näeb hõlpsalt, millal nende meeskonnaliikmed töölt puuduvad.

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse'is kaasatud kontroll-loendi üksused

Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.

## <a name="known-issues"></a>Teadaolevad probleemid

Tööruumis **Funktsioonihaldus** võidakse kuvada funktsioone, mis on eelvaatefunktsioonidena keelatud, kuigi need on üldiselt kättesaadavad. Allpool on loend üldiselt kättesaadavatest funktsioonidest, mille olek on vale. 

- Soodustuste haldus
- Juhtumihaldus
- Andmebaasi logimine (auditeerimine)
- Puhkuse lisandumine ühe ettevõtte või ühe plaani kohta
- Puhkuste ja puudumiste lisandumise peatamine
- Saldo korrigeerimise põhjusekood ja kommentaar
- Puhkuse ostmine ja müümine
- Puhkuste ja puudumiste kalender
- Puhkuse edasikandmise reeglid
- Puhkuse lisandumise auditeerimine
- Puhkuse lisandumise kustutamine
- Puhkuse lisandumise ümardamine
- Ühel puhkuseplaanil mitme puhkusetüübi konfigureerimine
- Eemalolekuaja täiustuste värskendamine
- Lisandumiste jaoks töövõtja täistööaja vaste kasutamine
- Ettevõtteülene hüvitusevaade
- Jõudluse ülevaadete printimine
- Puhkuse viitvõla parandused

### <a name="benefit-plan-employee-entity"></a>Soodustusplaani töövõtjaüksus 

Oleme hiljuti avastanud kaks probleemi seoses üksusega **BenefitsPlanEmployee**. Töötaja registreerimiste importimisel on suvandid **Planeerimise kood** ja **Plaani tüübi kood** valesti määratud. Selle probleemi tõttu kuvatakse vormil **Töövõtja soodustuste plaan** ja vormil **Registreerimise avamine** töövõtjate soodustuste plaanid valesti. See probleem võib mõjutada ka töövõtja võimalust valida plaane töövõtja iseteeninduses. Praegu ei ole lahendust. Käsitleme seda kui kõrge prioriteediga parandust ja laseme paranduse välja meie järgmise väljalaskega.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]