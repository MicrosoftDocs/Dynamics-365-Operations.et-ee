---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (14. märts 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38641d6a84340112ce15335533795ed7faf91123
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517829"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-14-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (14. märts 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis
See versioon sisaldab väikesi veaparandusi.

## <a name="changes-in-onboarding"></a>Muutused kasutuselevõtus
See versioon sisaldab väikesi veaparandusi.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused
**Järk 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Jõudlushaldus ei tööta kõigi stsenaariumite kohasele, kui kasutatakse topelt turberolle
Selles väljaandes tehtud muudatused võimaldavad jõudlushalduse stsenaariume, kasutades valmiskujul rolle või duplikaat-rolle.

### <a name="mass-assign-checklists-to-workers"></a>Töötajatele kontroll-loendite massiline määramine
Selle muudatusega saate nüüd valida mitu töötajat ja määrata neile töötajatele ühe või mitu kontroll-loendit korraga. 

### <a name="platform-update-24"></a>Platvormivärskendus update 24
Lisateavet platvormivärskenduse 24 kohta vt jaotisest [Mis on rakenduse Finance and Operations platvormivärskenduses 24 uut või mida on muudetud (märts 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Olulised muudatused platvormil 24 sisaldavad: 

- Talendis on lubatud teavitused.
- Uuendatud navigeerimisriba joondub nüüd Office'i päisega.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Office'i asukoha värskendus lülitab konteksti töötajate loendi algusesse
Praeguse väljaandega ei muutu enam kontori asukohta määrates selle töötaja, keda vaatate, kontekst kontori asukoha muutmisel.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Ametikoha määramise lõppkuupäeva ei kuvata töötaja värbamise ja üleviimise tegevuste juures õigesti
Ametikoha määramise lõppkuupäev kuvatakse nüüd tegevuste kasutamisel õigesti, vastavalt kasutaja eelistatud ajavööndile.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service töö üksus ei luba töö tüübi ja tööfunktsiooni väljade uuendamist
Common Data Service üksused sünkroonivad nüüd õigesti, kui neid Common Data Service'i abil värskendatakse.

## <a name="coming-soon"></a>Peagi tulekul

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Täpsem hüvitusturve (fikseeritud ja muutuv)
Paljudes ettevõtetes on hüvitise ja eeliste halduritel juurdepääs ainult teatud hüvituskirjetele. Need võivad olla juhtkonna või piirkonna töövõtjate omad. Selle muudatusega saab personaliosakond ettevõttesiseselt hüvitusplaane hallata ja säilitada erinevate töövõtjate gruppide jaoks. Saate fikseeritud ja muutuvatele plaanidele määrata turberolle, mis määravad plaanide juurdepääsu ja plaanidega seotud töövõtja andmed, näiteks palga või lisakulumikirjed. Ainult juurdepääsu saanud rollid saavad töödelda nende töötajate hüvitisi.

###  <a name="email-support-for-alerts"></a>E-posti tugi teatistele
Platvormi värskendusega 24 saavad kasutajad luua teavituse reegleid, mis saadavad kontaktidele automaatselt sündmuse käivitatud meiliteateid.

### <a name="duplicate-employee-check-interface-changes"></a>Topelt töötajate kontroll: kasutajaliidese muudatused
Selle muudatusega tuvastatakse nimeväljade sisestamisel duplikaadid ja olek näitab leitud duplikaatide arvu. Võite uue lehe avamiseks valida antud lingi, et hinnata, kas kasutada tuvastatud vastet. Andmesisestuse katkestamise vältimiseks ei avane duplikaatide vorm automaatselt.
