---
title: Aruande parameetrite määramiseks kasutage kasutaja sisendparameetri andmeallikaid
description: See artikkel selgitab, kuidas kasutada kasutaja sisendparameetri andmeallikaid, et määrata parameetrid teie genereeritud aruannetele.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 62b7a8173416a1d36a2985823d186a7a0e6a7e60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872968"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Aruande parameetrite määramiseks kasutage kasutaja sisendparameetri andmeallikaid

[!include[banner](../includes/banner.md)]

Kui kujundate [elektroonilise](general-electronic-reporting.md) aruandluse (ER) [mudeli](er-overview-components.md#model-mapping-component) vastendamise ja ER-vormingu [komponente](er-overview-components.md#format-component), saate kasutada andmeallikaid tüübiga USER INPUT PARAMETER *, et saada nõutud väärtused,* mida saab määrata käitusajal dialoogiboksi andmesisestusväljadele, enne kui algab ER-vormingu käivitamine. See artikkel kirjeldab praegu *toetatud andmeallikaid USER INPUT PARAMETER*.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a> Kohustuslikud atribuudid

Iga KASUTAJA SISENDPARAMEETRi tüübi andmeallikatele tuleb määrata *järgmised* atribuudid:

- **Sisestage** väljale Nimi andmeallika sisemine nimi. Seda nime saate kasutada konfigureeritud mudelivastenduse [või](er-formula-language.md) -komponendi teistes avaldistes ja sidumistes.

## <a name="optional-properties"></a><a name="optional-properties"></a> Valikulised atribuudid

Kasutaja sisendparameetri tüüpi andmeallikate jaoks saate valikuliselt *määrata järgmised* atribuudid:

- **Määrake väljal** Silt silt, mida kasutatakse käitusajal seostuva andmesisestusvälja jaoks. Erinevatele keelekoodidele saate lisada erineva silditeksti, aktiveerides sildivälja **ja** valides seejärel suvandi **Tõlki**.
- Määrake spikriväljal spikritekst, mis kuvatakse kujundusaja ajal vormingukujundaja või mudeli vastendamise kujundaja lehe allosas, **·** **·** **kui on valitud kasutaja sisestusparameetri tüübi** redigeeritav andmeallikas.*·* See tekst võib anda andmeallika kohta täiendavaid üksikasju, mis aitavad kasutajaid redigeeritava vormingu või mudeli vastendamise komponendi konfigureerimisel. Teise keelekoodi jaoks saate lisada erineva spikriteksti, valides suvandi **Tõlkimine**.

    > [!NOTE]
    > Nupp **Tõlkimine**, [mida](er-design-multilingual-reports.md#format-component) saate kasutada keele kindlate siltide ja teksti lisamiseks, muutub kättesaadavaks alles pärast andmeallika lisamise, muudatuste salvestamist ja seejärel andmeallika redigeerimise jaoks uuesti avamist.

- Konfigureerige **väljal Kirjutuskaitstud** avaldis, mis tagastab Kahendmuutuja *[...](er-formula-supported-data-types-primitive.md#boolean)* väärtuse.

    - Kui konfigureeritud avaldis **annab** käitusajal tulemuseks väärtuse Tõene, siis kuvatakse seotud andmesisestusväli dialoogiboksis tuhmina ja te ei saa selle väärtust muuta.
    - Kui konfigureeritud avaldis **annab** tulemuseks väärtuse Väär käitusajal või kui ühtegi avaldist pole konfigureeritud, on seotud andmesisestusväli dialoogiboksis saadaval ja te saate selle väärtust muuta.

- Vaikeväärtuse **väljal konfigureerige** avaldis, mis tagastab viidatud parameetritüübi väärtuse. Seda väärtust saab kasutada dialoogiboksi seostuva andmesisestusvälja vaikeväärtuse täitmiseks käitusajal.

    ER-vormingu käivitamisel salvestatakse käitusajal dialoogiboksi seotud andmesisestusväljale sisestatud väärtus mälus varem kasutatud väärtusena. Varem kasutatud väärtused salvestatakse eraldi iga välja puhul, käitades ER-vormingut, praegust kasutajat ja praegust organisatsiooni (ettevõte).

    - Seadistage **suvand Lähtesta** **·** **vaikeväärtusele** Alati, kui vaikeväärtuse avaldisega tagastatud väärtust tuleks alati kasutada vaikeväärtusena, olenemata eelnevalt kasutatud väärtusest.
    - Määrake valik **Lähtesta vaikeväärtusele** **·** **Alati**, kui vaikeväärtuse avaldise väärtusega tagastatud väärtust tuleks vaikeväärtusena kasutada ainult juhul, kui eelnevalt kasutatud väärtus puudub.

    > [!NOTE]
    > Kui seate suvandi **Lähtesta vaikeväärtusele** alati väärtuseks **Jah**, peab avaldis olema konfigureeritud **väljal** Vaikeväärtus.

- Kui määrate suvandi **Luba mitme valik** valikuks **Jah**, saate käitusajal konfigureeritud parameetrile valida mitu väärtust. Kui seate väärtuseks **Ei**, saate valida ainult ühe väärtuse.

    > [!NOTE]
    > See valik ei kehti kõigi KASUTAJA SISESTUSPARAMEETRite *tüüpide* puhul. Konstruktsiooni ajal ilmneb erand, mis teavitab kasutajat, et konfigureeritud kasutaja sisestusparameeter ei toeta mitme valikut ning et valida või sisestada saab ainult ühe väärtuse.
    >
    > Kui määrasite suvandi **Luba mitme valiku** **puhul väärtuseks Jah** ja **määrasite** avaldise väljal Vaikeväärtus, saab seda avaldist kasutada ainult ühe vaikeväärtuse miseks.

- Valige suvand **Muuda nähtavust**, et määrata, kas konfigureeritud parameetrit tuleks käitusajal dialoogiboksis kuvada.

    > [!NOTE]
    > KASUTAJA SISENDPARAMEETRi tüübi andmeallikate vaikimisi *nähtavus sõltub* neid hoiab ER-komponendist.
    >
    > - Kui andmeallikas on konfigureeritud vormingu komponendis, on see vaikimisi nähtav.
    > - Kui andmeallikas on mudeli vastendamise komponendis konfigureeritud, on see nähtav ainult siis, kui andmeallika väärtus mõjutab väljundväärtust ER-komponendi käivitamisel. Näiteks lisate andmeallika, kuid ei kasutanud seda praeguse mudeli vastendamise komponendi avaldistes ja sidumistes. Kui see on nii, siis ei kuvata dialoogiaknas käitusajal vaikimisi asjakohast andmesisestusvälja. 

    Valemikoosturi **lehel** valemi väljal konfigureerige **avaldis**, mis tagastab Kahendmuutuja *väärtuse*.

    - Kui konfigureeritud avaldis **annab** tulemuseks väärtuse Tõene käitusajal või kui ühtegi avaldist pole konfigureeritud, siis on seotud andmesisestusväli käitusajal dialoogiboksis nähtav.
    - Kui konfigureeritud avaldis annab tulemuseks väärtuse **Väär**, on seotud andmesisestusväli käitusajal dialoogiaknas peidetud. Kui seda kutsuvad käitusajal teised avaldised, tagastab see vaikeväärtuse, varem kasutatud väärtuse või praeguse andmetüübi väärtuse vaikeväärtuse, sõltuvalt teistest sätetest.

## <a name="type-specific-properties"></a>Tüübipõhised atribuudid

### <a name="application-dependent-user-input-parameter"></a>Rakendusest sõltuv kasutaja sisendparameeter

Kasutage kasutaja **sisestusparameetri** \> **·** Microsoft Dynamics tüübi andmeallikat, et hankida andmetüübi nõutud väärtus või väärtused, mis on määratletud rakenduse 365 Finantsid praeguse eksemplari jaoks. Seda tüüpi andmeallika lisamisel ER-komponendile määrake järgmised atribuudid:

- Valige väljal **Toimingute andmetüübi nimi (EDT, loetelu)**[rakenduse laiendatud andmetüüp (EDT)](../extensibility/extensible-edts.md) või rakenduse loetelu.

> [!NOTE]
> Soovitame teil vaadata üle avaldised, mis on konfigureeritud kirjutuskaitstud ja vaikeväärtuse **väljadel** **·** **, kui muudate toimingute andmetüübi nime (EDT, enum)** *viidet selle KASUTAJA SISESTUSPARAMEETRi tüübi redigeeritavas andmeallikas.*

Järgmine näide näitab Instat XML-i `$TaxRegNum` (DE) **ER-vormingu konfiguratsioonis konfigureeritud** andmeallika atribuute. See andmeallikas on konfigureeritud kasutama *kirjeldus*-EDT-d **·**, et pakkuda käibemaksu registreerimisnumbri andmesisestusvälja dialoogiaknas käitusajal.

![KASUTAJA SISENDPARAMEETRi tüüpi andmeallika atribuudid, mis on vormingukujundaja lehe dialoogiboks.](./media/er-user-input-parameter-data-sources-01.png)

Järgmine näide näitab dialoogiakent, **mis kuvatakse käitusajal, kui Intrastat-deklaratsiooni loomiseks käivitatakse Instat XML-i (DE)** ER-vormingu [konfiguratsioon](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md). Pange tähele, et konfigureeritud **maksu registreerimisnumbri** väli on andmesisestuses saadaval.

![Intrastati aruande dialoogiboks jooksva ER-vormingu jaoks Intrastati lehel.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Andmemudeli loetelu kasutaja sisendparameeter

Kasutage andmemudeli **loetelu** \> **kasutaja sisendparameetri**[tüübi andmeallikat, et saada ühe andmemudeli loetelu nõutud väärtus või väärtused.](er-formula-supported-data-types-primitive.md#enumeration) Seda tüüpi andmeallika lisamisel ER-komponendile määrake järgmised atribuudid:

- **Määrake väljal** Mudel viide põhiandmete mudelile.
- **Määrake väljal Mudeli** loetelu viide viidatud andmemudeli loetelule.
- Valige väljal **Versioon** viidatud mudeli loetelu sisaldava ER-andmemudeli komponendi revisjoni number.

    > [!TIP]
    > Konstruktsiooni ajal võite jätta välja Versioon tühjaks, et pääseda juurde loendile viidatud andmemudeli komponendi loetelude kohta, **mis** asub vastava ER-i andmemudeli konfiguratsiooni mustandversioonis. Sel viisil saate samaaegselt redigeerida oma mudeli vastenduse või vormingu komponendi mustandversiooni ja põhiandmemudeli komponendi mustandversiooni.
    >
    > Pange siiski tähele, et välja **Versioon** saab tühjaks jätta ainult mudeli vastenduse või vormingu komponendi mustandversioonis. Kui muudate ER-mudeli **·** **vastendamise** oleku või vormingu konfiguratsiooni mustand olekuks Lõpetatud, täidetakse see väli automaatselt kõrgeima mudeli revisjoni numbriga, mis on praeguses finantseksemplaris saadaval. Kui tutvustate oma põhiandmete mudeli mustandversioonis uut loetelu või uut loeteluväärtust ja viitate sellele redigeeritavas mudelivastenduses või vormingu komponendis, lõpetage põhiandmete mudeli konfiguratsiooni mustandversioon enne ER-mudeli vastendamise või vormingu konfiguratsiooni mustandversiooni lõpetamist. Vastasel juhul ilmneb "Tee ei leita" erand, kui muudate mudeli vastendamise või vormingu konfiguratsiooni oleku mustandist **olekusse** Lõpetatud **·**. Teade teavitab teid, et viidatud loetelu või loetelu väärtus puudub põhiandmete mudelis.

Järgmine näide näitab `$ReportDirection` Instat XML-i (DE) Contoso **ER-i vormingu konfiguratsioonis konfigureeritud** andmeallika atribuute. **Instat XML-i (DE) Contoso** konfiguratsioon on [tuletatud](general-electronic-reporting.md#Configuration)**Instat XML-i (DE) konfiguratsioonist.** See andmeallikas on konfigureeritud kasutama *mudeli ReportDirection* loetelu sobiva otsinguvälja pakkumiseks dialoogiaknas käitusajal.

![Kasutaja sisestusparameetri andmeallika atribuudid.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Vormingu loetelu kasutaja sisendparameeter

Kasutage vormingu loetelu loetelu **kasutaja** \> **sisendparameetri** tüübi andmeallikat, et hankida ühe vormingu loetelu soovitud väärtus või väärtused. Seda tüüpi andmeallika lisamisel ER-komponendile määrake järgmised atribuudid:

- **Määrake väljal Vorminda** loetelud redigeeritava vormingu nummerdamine.

> [!NOTE]
> Seda tüüpi andmeallikaid saab konfigureerida ainult redigeeritava vormingu komponendi ulatuses.

## <a name="additional-resources"></a>Lisaressursid

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Tüübi USER INPUT PARAMETER andmeallika väärtuste käivitamine lähtekoodist](er-initiate-uip-data-source-value-from-source-code.md)
