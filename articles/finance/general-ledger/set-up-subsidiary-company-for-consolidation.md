---
title: Allettevõtte juriidilise isiku seadistamine konsolideerimiseks
description: Selles teemas kirjeldatakse, kuidas töötada konsolideerimisettevõtete kontoplaanidega.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 15050310f355ece683b00a00be9552d32aded17b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832846"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Allettevõtte juriidilise isiku seadistamine konsolideerimiseks

[!include [banner](../includes/banner.md)]

Meetod, mida te kasutate allettevõtte kontode ettevalmistamisel konsolideerimiseks, sõltub osaliselt ulatusest, kui palju allettevõtte juriidilise isiku kontoplaani struktuur kajastab konsolideeritud juriidilise isiku kontoplaani.

Enne, kui perioodilõpu sulgemise osana konsolideerimist alustate, sooritage suletava perioodilõpu jaoks ettevalmistavad toimingud, kuid ärge sulgege allkontosid enne, kui konsolideerimine on lõpetatud. Lisateabe saamiseks pearioodi lõpus sulgemise kohta vt [Pearaamatu sulgemine perioodi lõpus](close-general-ledger-at-period-end.md) ja [Rahandusaasta sulgemine](tasks/close-fiscal-year.md).

> [!NOTE]
>  Soovitame teil kasutada rakenduse Microsoft Dynamics 365 Finance Management Reporterit, et kombineerida finantstulemused mitme juriidilise isiku jaoks konsolideeritud vormingus. Management Reporter võimaldab luua konsolideeritud finantsaruandeid juriidiliste isikute lõikes, kasutada Excelit konsolideerimise andmete importimiseks teistest allikatest ja teisendada summad mis tahes arvuks aruandlusvaluutadeks ilma, et konsolideerimisprotsessi oleks vaja rakenduses Dynamics 365 Finance käivitada.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Allettevõtte põhikontode vastendamine konsolideeritud põhikontodega

Kui allettevõtte juriidilise isiku kontoplaan ei järgi konsolideeritud juriidilise isiku kontoplaani, saate allettevõtte põhikontod vastendada konsolideeritud juriidilise isiku põhikontodega.

1. Avage jaotises *allettevõtte juriidiline isik* jaotis **Pearaamat \> Seadistus** \> **Kontoplaan \> Kontoplaan**.
2. Valige kontoplaan. Valige kiirkaardil **Põhikontod** põhikonto ja seejärel käsk **Redigeeri**.
3. Valige iga allettevõtte põhikonto, mis tuleb konsolideeritud põhikontoga vastendada. Sisestage kiirkaadi **Üldine** väljale **Konsolideerimiskonto** konsolideeritud juriidilise isiku konto, millele valitud alletevõte põhikonto saldo või tehingud tuleb üle kanda. Saate sisestada sama konsolideeritud põhikonto mitme tütarettevõtte konto jaoks.

    > [!NOTE]
    > Kui tütarettevõtte vastendatud kontode põhikontotüübid erinevad konsolideeritud juriidilise isiku kontode põhikontotüüpidest, kirjutatakse väärtused kontodel põhikontotüübiga **Kokku** konsolideerimise käigus üle.

4. Valmistage finantsdimensioonidel põhineva konsolideeritud juriidilise isiku jaoks ette aruanded ja finantsaruanded. Allkontodel kasutatavate finantsdimensioonide vastendamiseks konsolideeritud juriidilise isiku finantsdimensioonidega järgige neid samme.

    1. Avage jaotises *allettevõtte juriidline isik* jaotis **Pearaamat \> Seadistus \> Finantsdimensioonid \> Finantsdimensioonid**, valige finantsdimensioon ja seejärel valige **Finantsdimensiooni väärtused**.
    2. Valige finantsdimensiooni väärtus vastendamiseks erineva finantsdimensiooni väärtusega konsolideeritud juriidilises isikus.
    3. Kiirkaardil **Üldine** väljale **Grupi dimensioon** sisestage konsolideeritud juriidilise isiku finantsdimensioon. Konsolideerimisel määratakse see finantsdimensioon kannetele ja saldodele, mis kasutavad valitud finantsdimensiooni allettevõtte juriidilises isikus. Siin sisestatud finantsdimensioone tuleb kasutada konsolideeritud juriidilises isikus. Saate määrata finantsdimensiooni, mida kasutatakse grupi finantsdimensioonina, mitme tütarettevõtte finantsdimensioonidele.

5. Kui teete konsolideerimist võrgus, järgige neid samme, et tagada tehingute toimimine teie soovi järgi..

    1. Avage jaotises *konsolideeritud juriidiline isik* jaotis **Pearaamat \> Perioodiline \> Konsolideeri \> Konsolideeri \[Ekspordi asukohta\]**, et avada leht **Konsolideeri \[Võrgus\]**.
    2. Valige vahekaardil **Kriteeriumid** märkeruut **KAsuta konsolideerimiskontot**.
    3. Valige vahekaardil **Finantsdimensioonid** sobivad finantsdimensioonid.
    4. Iga valitava finantsdimensiooni jaoks sisestage number väljale **Segmendi järjerstus**, näitamaks dimensioonide kuvamise järjestust.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Sama kontoplaani säilitamine nii tütarettevõtte kui ka konsolideeritud juriidilistes isikutes

Allettevõtte juriidilise isiku põhikontodel võivad olla samad kontonumbrid ja sama kontoplaani struktuur nagu konsolideeritud juriidilise isiku põhikontodel. Sel juhul ei pea allettevõtte põhikontosid käsitsi vastendama konsolideeritud juriidilise isiku põhikontodega.

Enne konsolideerimise käivitamist järgige neid samme.

1. Avage jaotises *konsolideeritud juriidiline isik* jaotis **Pearaamat \> Perioodiline \> Konsolideeri \> Konsolideeri \[Ekspordi asukohta\]**, et avada leht **Konsolideeri \[Võrgus\]**.
2. Märkige ruut **Kasuta konsolideerimiskontot**. Kannete ja saldode ülekanne õigele kontole toimub konsolideerimise käigus automaatselt.

> [!NOTE]
> Kui kontod ei ole vastavuses, siis konsolideerimine seiskub ja te saate sõnumi.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Konsolideeritud juriidilise isiku kontoplaani loomine olemasoleva kontoplaani alusel

Konsolideerimist võite teha isegi siis, kui konsolideeritud juriidilises isikus pole kontoplaani veel loodud.

- Kui teil on kavandatud kontostruktuur kasutamiseks konsolideeritud juriidilises isikus, saate vastendada tütarettevõtte kontod selle struktuuriga.
- Kui te ühtegi allettevõtte kontot ei vastenda, luuakse konsolideeritud juriidilise isiku kontod allettevõtte andmete konsolideeritud juriidilisse isikusse üle kandmisel automaatselt. Need kontod põhinevad põhikontol. Järgnevad andmed kogutakse konsolideeritud juriidilise isiku kontodele, millel on tütarettevõtte kontodega sama kontonumber.

Olenemata sellest, kas kontod on vastendatud, tühjendage konsolideeritud juriidilises isikus ruut **Kasuta konsolideerimiskontot** lehel **Konsolideeri** enne kui käitate sellise konsolideerimise.

> [!NOTE]
> Seda meetodit saate kasutada konsolideeritud juriidilises isikus kontoplaani loomiseks ühe allettevõtte juriidiliste isikute kontoplaanist. (Lisateavet vt teemast [Konsolideerimiskonto grupid ja täiendavad konsolideerimiskontod](../budgeting/consolidation-account-groups-consolidation-accounts.md)). Seejärel määrake igale konsolideeritud põhikontole vastav konsolideerimisteisenduse põhimõte ja käitage konsolideerimine kõigi allettevõtete juriidiliste isikute jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]