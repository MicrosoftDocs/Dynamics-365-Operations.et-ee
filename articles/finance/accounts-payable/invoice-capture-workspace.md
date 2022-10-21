---
title: Arvehõive lahenduse tööruum
description: See artikkel annab teavet arve hõivamise lahenduse tööruumi kohta.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4f3af7abf94542437be6132344d6bb7ffaf33d07
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690976"
---
# <a name="invoice-capture-solution-workspace"></a>Arvehõive lahenduse tööruum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="side-by-side-viewer-for-the-invoice-capture-solution"></a>Arve hõivamise lahenduse poolne vaatur

Arvete süsteemi sisestamine on tavaliselt olnud aeganõudev protsess, mis võib ilmneda tõrgetest, kuna ametnikud peavad õige teabe kogumiseks navigeerima mitme manuse failide ja akende vahel. Poolne dokumendivaatur aitab teil arvetega töötades oma kogemust parandada, muutes protsessi lihtsamaks, tõhusamaks ja täpsemaks.

Kõrvuti dokumendivaatur võimaldab kasutajatel kasutada originaaldokumenti ja arvet samas aknas korraga avatud. Arve lehekülg täidetakse teabega, mis pärineb algsest arvedokumendist. Vaatur loob ühenduse arvelehe väljade ja algse arvedokumendi vahel. Vaatur aitab ka kasutajatel leida tõrkeid, mis arvelehel olemas on.

### <a name="open-the-side-by-side-viewer"></a>Ava poolne vaatur

Microsoft Dynamics 365 Finance’s saate avada poolne vaatur loendi kokkuvõtte leheküljelt või arve loendilehelt. Samuti saate seda avada kirje topelt-(või topeltklõpsake) või valides arve numbri.

### <a name="using-the-side-by-side-viewer"></a>Kõrvutivaaturi kasutamine

#### <a name="manually-review-an-invoice"></a>Arve käsitsi ülevaatamine

Imporditud arvedokument võib tõrgete või hoiatuste tõttu nõuda käsitsi ülevaatamist. Kõrvutivaaturis kuvatakse dokumendi päises **olek** Imporditud ja praeguseks versiooniks on **algversioon**.

Arve läbivaatamise alustamiseks valige suvand Käivita **ülevaatus**. Kõik väljad muutuvad redigeeritavaks. Välja **Olek** väärtuseks värskendatakse **Ülevaatusl** ja välja **Praegune versioon** väärtuseks **Muudetud**.

#### <a name="view-and-work-with-messages"></a>Kuvage teateid ja töötage sellega

Kasutajad peaksid ülevaatusprotsessi teatepaanilt käivitama. Tõrketeateid tähistab punane X, hoiatusteateid tähistab kolmnurk ning teadetele tähistab ring. Usalduse skooriga seotud teated saab klassifitseerida kas hoiatuste või vigadena, sõltuvalt konfiguratsioonigrupi seatud lävest. Lisateavet vt arve hõivamise [lahenduse konfiguratsioonigruppidest](invoice-capture-config-group.md).

Hoiatusi ja tõrketeateid saab ignoreerida teatepaanilt, arve päiselt või arve ridadelt. Pärast teate ignoreerimist ei ilmu see enam tõrke või hoiatusena ning arve kinnitamine nurjub.

- Teatepaanilt sõnumite ignoreerimiseks valige suvand **Eira**. Ignoreeritud sõnumi lähtestamiseks valige uuesti **ignoreerimine**. Seejärel muudetakse selle tüüp tõrkest või hoiatusest teabeks.
- Arve päise või arverea teadete ignoreerimiseks valige väljal **Eira**. Teate sümbol kaob. Kui teade lähtestatakse teatepaanilt, ilmub see uuesti.

Arve päiseväljadega seotud teadete korral, kui valite teatepaanil, teisaldatakse kursor päise jaotise vastavale väljale.

#### <a name="proofread-and-edit-fields"></a>Korrektuuri ja redigeerimise väljad

Kui välja väärtust loetakse algsest arvest optilise märgituvastuse (OCR) kaudu, kuvatakse väljal sümbol. Kui valite sümboli, siis dokumendivaatur suumib ja tõstab esile koha, kus välja väärtus on loetud, mis aitab arve andmeid kontrollida.

Dokumendivaaturi lähtestamiseks esialgsele suurendusele järgige ühte järgmistest sammudest:

- Valige sama sümbol, mille eelnevalt valisite.
- Valige dokumendivaaturi ülemises parempoolses nurgas nupp.

Redigeerige välju vastavalt vajadusele. Redigeerimised salvestatakse automaatselt, kui kursor väljalt lahkub. Väljast paremal asuvat sümbol näitab, et väli on käsitsi uuendatud. Lehekülje värskendamisel sümbol eemaldatakse.

#### <a name="check-an-invoice-to-get-up-to-date-messages"></a>Arve kontrollimine ajani teadete toomiseks

Välja redigeerimisl välja väärtust uuendatakse, kuid uusi kinnitamisteateid ei looda. Uuendatud valideerimisteadete toomiseks valige käsk **Kontrolli**. Uuendatakse teatepaanil, arve päisel ja arve ridadel olevad teated.

#### <a name="complete-the-review"></a>Ülevaatuse lõpule viimine

Ülevaatuse lõpetamiseks valige lõpeta **ülevaatus**. Arved kinnitatakse. Vigade ilmnemisel jääb dokumendi olek ülevaatuseks **ja** kuvatakse teateriba. Nurjunud valideerimise põhjuste kohta teabe andmiseks uuendatakse automaatselt kõik teated teatepaanil ja arve päisel ning ridadel.

Pärast kõikide blokeerimistvigade lahendamist saab ülevaatuse lõpule viia. Dokumendi olekuks saab määrata Ülevaadatud **ja** välju ei saa enam redigeerida. Ülevaatuse saate taaskäivitada, kui valite **uuesti suvandi Alusta läbivaatust**.

#### <a name="generate-a-pending-vendor-invoice-in-finance"></a>Ootel hankija arve loomine finantsis

Arvedokumendi saatmiseks ühendatud finantskeskkonda valige käsk **Loo**. Kui arve loomine nurjub, kuvatakse teateribal veateade.

#### <a name="void-an-invoice"></a>Arve tühistamine

Arve tühistamiseks valige käsk **Tühista**. Tühistatud arveid ei saa üle vaadata ja neid ei kuvata arvete **vajaduse käsitsi ülevaateloendis**.

### <a name="validation-logic"></a>Kinnitamise loogika

Mõned võtmeväljad kõrvutivaaturis ei eksisteeri arvete ajastamisandmetes, vaid need on nõutavad finantsis ootel arvete loomiseks. Need väljad tuletatakse finantside praeguste arveplaanimise andmete ja koondandmete kombinatsioonist.

Tuletatud väljad on juriidiline **isik**, **hankija konto** ja **kaubakood**. Need tuleb tuletada järgmises järjestuses. Kui välja tuletus nurjub, protsess katkeb.

1. **Juriidiline isik** – juriidiline isik tuletatakse esimesena. Kui juriidilisele isikule leitakse aktiivne vastendamisreegel, siis tuletatakse juriidiline isik ettevõtte nime ja ettevõtte aadressi alusel.
2. **Hankija konto** – järgmisena tuletatakse hankijakonto aktiivse vastendamisreegli ning tuletatud juriidilise isiku ning hankija nime ja hankija aadressi kombinatsiooni põhjal.
3. **Kauba kood** – lõpuks tuletatakse kauba nimi kauba põhistest andmetest, mis põhinevad kolmel järgneval teabetüübil:

    - Konfigureeritud vastendamisreegel
    - Tuletatud juriidiline isik
    - Tuletatud hankija konto

Kinnituse käivitamiseks valige suvand **Kontrolli** kõrvuti vaaturis. Praegu tehakse kinnitamisel järgmised kontrollid:

- **Kohustuslik kontroll** – see kontroll kinnitab kohustuslikud väljad kõrvutivaaturi jaoks. Kasutajad saavad valida, millised väljad peavad olema konfiguratsiooni seadistamise **lehel** kohustuslikud.
- **Usalduse skoor** – kasutajad saavad seada hoiatusläve ja tõrkeläve enesestuse skoori jaoks. See kontroll keskendub OCR-i usaldusskoorile, mis jääb alla nende lävede. Kinnitamistulemuse alusel kuvatakse tõrkeid või hoiatusteateid.
- **Juriidiline** isik – see kontroll kontrollib, kas juriidiline isik on finantsis. Kui finantskeskkonnas ei ole juriidilist isikut, nurjub kinnitamine.

Kui korraga kasutatakse korraga vaaturit ja kasutaja valib kontrolli, **käivitatakse** tuletus- ja kinnitamisprotsessid. Kui arved on täpsed, käivitatakse kinnitamisprotsess, kui kasutaja valib täieliku **ülevaate**. See käivitatakse ka siis, kui kasutaja valib hankija **arve loomise**.

Tuletusprotsess toimub enne kinnitamisprotsessi ja kõik hoiatused või tõrked tulevad kinnitamisprotsessist. Hoiatused ja tõrked logitakse finantsidesse.
