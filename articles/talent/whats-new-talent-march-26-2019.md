---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (26. märts 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
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
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4b59183116784f44f45fddacdfa4aa954383ecd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023880"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (26. märts 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="enhancements-to-interview-scheduling"></a>Vestluse plaanimise täiustused
Vestluse plaanimiseks on saadaval järgmised täiustused.

- Värbajad või personalijuhid saavad müüd käsitsi käivitada intervjueeritavale tagasiside jätmise meeldetuletuse. Seotud meeldetuletuse e-kirja mall on samuti konfigureeritav.
- Intervjuu kokkuvõte jagamisel kandidaadiga saab intervjuu planeerija valida intervjueeritavate nimede peitmise ja ka teatud ridade peitmise intervjuu kokkuvõtte vaatest.

## <a name="changes-in-onboard"></a>Muutused Onboardis

### <a name="embedded-images-in-activities"></a>Manustatud pildid tegevustes
Nüüd saate pildid otse tegevustesse manustada. Lisaks võimalusele kopeerida ja kleepida pilte veebist, saate üles laadida pilte oma kohalikust failisüsteemist. Tegevuse mahu piiranguks on 1 MB. Kui pilt on liiga suur, muutke suurust ja proovige uuesti üles laadida.

[![Vastendamine](./media/embedimages.png)](./media/embedimages.png)

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused
**Järk 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>Kohandatud väljade tugi on valitud üksustele saadaval teenuse Common Data Service all 

Järgmised Common Data Service’i üksused toetavad nüüd rakenduses Talent loodud kliendiväljasid.

- Töötaja
- Etniline päritolu
- Veterani staatus
- Keelekood
- Amet
- Töö tüüp
- Tööfunktsioon
- Ametikoht
- Positsiooni tüüp
 
### <a name="employment-history-not-displayed-chronologically"></a>Tööhõive ajalugu ei kuvata kronoloogilises järjestuses
Selle muudatusega näitab tööhõive ajaloo leht nüüd tööhõive kirjeid kronoloogilises järjekorras, sõltumata ettevõttest. Saate ettevõtte järgi sorteerimiseks kasutada sorteerimisvalikuid.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>Fikseeritud kompensatsiooniplaane ei kuvata, kui kasutaja on turvalisuse all piiratud ettevõtte järgi.
Selles väljalaskes kuvatakse fikseeritud kompensatsiooniplaane, kui kasutajaid piiratakse turvalisuse all ettevõtte järgi. Kõigist turvasätetest peatakse kinni ja fikseeritud plaanid kuvatakse nendele ettevõtetele, millele kasutajal on ligipääsuõigus. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>Ei saa kustutada töö kirjeid kasutades Talentis Excelis avamise valikut
Selles väljalaskes saate nüüd töö kirjeid eemaldada, kasutades valikut **Ava Excelis** rakenduses Talent.

### <a name="upgrade-to-common-data-service"></a>Common Data Service'i värskendus
Tähtajad Common Data Service'i värskendamiseks lähenevad kiiresti. Logige sisse PowerAppsi halduskeskusesse, et teha kindlaks, kas teie andmebaas vajab värskendamist. Lisateavet tähtaegade ja täiendamiseks nõutavate etappide kohta vt jaotisest [Täiendamine teenusele Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>Eelvaates

Eelvaate funktsioonide lubamise infot leiate jaotisest [Juurdepääs eelvaatefunktsioonidele rakenduses Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Puhkuse tüüpidele põhjusekoodide määramise lubamine
Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Selle info saamiseks peavad töötajad oma puhkuseavaldusele lisama põhjusekoodi. Selles väljaandes saate nüüd määrata antud puhkuse tüübiga seotud põhjusekoodid ja lubada töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>Teatud puhkusetüüpide puhkuseavaldustel nõutavate põhjusekoodide konfigureerimine
Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkuseavaldustele põhjusekoodide määramist. See võib olla nõutud vastavalt riigi/regiooni regulatiivsetele nõuetele või ettevõtte poliitikale. See väljaanne annab personaliosakonnale võimaluse määrata, millised puhkusetüübid vajavad põhjusekoodi. See rakendatakse siis, kui töötaja esitab puhkuseavalduse juhul, kui puhkus vajab põhjusekoodi.

## <a name="coming-soon"></a>Peagi tulekul

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Täpsem hüvitusturve (fikseeritud ja muutuv)
Paljudes ettevõtetes on hüvitise ja eeliste halduritel juurdepääs ainult teatud hüvituskirjetele. Need võivad olla juhtkonna või piirkonna töövõtjate omad. Selle muudatusega saab personaliosakond ettevõttesiseselt hüvitusplaane hallata ja säilitada erinevate töövõtjate gruppide jaoks. Saate fikseeritud ja muutuvatele plaanidele määrata turberolle, mis määravad plaanide juurdepääsu ja plaanidega seotud töövõtja andmed, näiteks palga või lisakulumikirjed. Ainult juurdepääsu saanud rollid saavad töödelda nende töötajate hüvitisi.

###  <a name="email-support-for-alerts"></a>E-posti tugi teatistele
Finance and Operationsi platvormi 25. uuendusega saavad kasutajad luua alarmide reegleid, mis saadavad sündmuse poolt käivitades automaatselt kontaktidele meiliteavitusi. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>Topelt töötajate kontrollid: kasutajaliidese muudatused
Selle muudatusega tuvastatakse nimeväljade sisestamisel duplikaadid ja olek näitab leitud duplikaatide arvu. Võite uue lehe avamiseks valida antud lingi, et hinnata, kas kasutada tuvastatud vastet. Andmesisestuse katkestamise vältimiseks ei avane duplikaatide vorm automaatselt.
