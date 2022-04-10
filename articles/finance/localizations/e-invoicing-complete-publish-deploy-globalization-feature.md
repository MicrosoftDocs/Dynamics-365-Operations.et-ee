---
title: Globaliseerimisfunktsiooni lõpule viimine, avaldamine ja juurutamine
description: See teema annab teavet globaliseerimisfunktsiooni elutsükli kohta.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a842a3ba31c0a8e0d80ad1856d9d6d861a8514ea
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371889"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Globaliseerimisfunktsiooni lõpule viimine, avaldamine ja juurutamine

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Elektroonilise arveldamise funktsiooniversioonid

Elektroonilise arveldamise funktsioonid on versioonitud. Uue versiooni loomisel lisatakse automaatselt suurem versiooninumber.

Elektroonilise arvelduse funktsioonide versioonid järgivad elutsüklit, mis hõlmab kuni kolme olekut.

- **Mustand** : kui funktsiooni versioonil on see olek, saate redigeerida selle konfiguratsiooni atribuute ja selle artefaktide (nt failivormingu konfiguratsioonid).
- **Lõpetatud** – see olek näitab, et olete funktsiooniversiooni redigeerimise lõpetanud ja te ei kavatse seda rohkem uuendada. Kui funktsiooni versiooni olek on selline, ei saa te seda ega selle komponente enam redigeerida.
- **Avaldatud** : see olek näitab, et funktsiooni versioon on avaldatud teie organisatsiooniga seotud globaalses hoidlas. Kui funktsiooni versiooni olek on selline, ei saa te seda ega selle komponente enam redigeerida.

Saate elektroonilise arveldamise **funktsiooni** uuele versioonile määrata kehtivuse alguskuupäeva. Sel viisil saate määrata vaikeversiooni, mida saab kasutada või üle kirjutada, kui funktsioon juurutatakse teenuse keskkonda.

Elektroonilise arveldamise funktsiooniversiooni oleku muutmiseks järgige neid samme.

1. Logige oma teenuse Regulatory Configuration Service (RCS) kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
3. Elektroonilise arveldamise funktsioonide **lehe vasakul poolel** valige elektroonilise arveldamise funktsioon.
4. **Valige versioon** vahekaardil Versioonid lehe paremal küljel.
5. Valige **muuda olekut** ja seejärel valige Vii **lõpule** (kui praegune **olek on Mustand**) **või Avaldatud** (kui praegune olek on **Lõpetatud**).
6. Teateaknas valige taotluse **kinnitamiseks** jah.

Käsitsi muutmine olekust Lõpetatud **olekusse** **Avaldatud** on valikuline. Elektroonilise arveldamise funktsiooniversioonid uuendatakse automaatselt **olekusse** Avaldatud, kui need juurutatakse teenusekeskkonda.

Olekut saate jälgida vahekaardi **Versioonid veerus** Funktsiooni **versiooni** olek.

## <a name="deploy-feature-versions"></a>Funktsiooniversioonide juurutamine

RCS-i puhul kasutate käsku **Deploy**, et avaldada elektrooniline arveldamise funktsiooni versioon sihtteenuse keskkonnas või ühendatud rakenduses.

1. Elektroonilise arveldamise funktsioonide **lehe vasakul poolel** valige elektroonilise arveldamise funktsioon.
2. **Lehe paremal** küljel oleval vahekaardil Versioonid valige elektroonilise arveldamise funktsiooni versioon, mida soovite juurutada teenuse keskkonda või ühendatud rakendusele. Valitud versiooni olek peab olema Lõpetatud **või** Avaldatud **·**.
3. Valige **juurutamine** ja seejärel valige üks või mõlemad järgmistest suvanditest juurutamise sihtmärgi määratlemiseks:

    - **Seotud rakendus** – rakenduse seadistusega antud konfiguratsioon kirjutatakse Microsofti Dynamics 365 Finance eksemplari või on Dynamics 365 Supply Chain Management sellega eelnevalt seostatud.
    - **Teenuse keskkond** – elektroonilise arveldamise funktsiooni versioon juurutatakse teenuse keskkonda. Elektrooniline arveldamine on seejärel valmis vastu saama ja töötlema finants- või tarneahela haldus saadavad elektroonilisi dokumente.

> [!NOTE]
> Tavaliselt muudate te elektroonilise aruandluse (ER) funktsiooni parameetreid, mis tuleb juurutada teenuse keskkonda. Seotud rakenduse muudatused on harvased. Uued versioonid tuleks ühendatud rakendusse juurutada ainult siis, kui muudate oma rakenduse vastavaid parameetreid.

Määramaks, kas konkreetne elektroonilise arveldamise funktsiooni versioon juurutatakse konkreetsesse keskkonda, **vaadake teavet vahekaardil Keskkonnad**.

## <a name="remove-feature-versions"></a>Funktsiooniversioonide eemaldamine

RCS-s saate valida **tühistamisfunktsiooni** konkreetse elektroonilise arveldamise funktsiooniversiooni eemaldamiseks teenusekeskkonnast, kui see seal juurutati.

> [!IMPORTANT]
> Nupp **Tühista** töötab ainult teenuse keskkondades. See ei eemalda ühendatud rakendusest midagi praeguse elektroonilise arveldamise funktsiooni jaoks.

## <a name="rebase-electronic-invoicing-features"></a>Elektroonilise arveldamise funktsioonide uuesti põhinemine

Kui ühest elektroonilise arveldamise funktsioonist tuletatakse teine, **saate valida Rebase'i** tuletatud funktsiooni uuendamiseks algses (ema-) funktsioonis tehtud muudatustega.

Loodud funktsiooni tuletatud versiooni taasbaasi loomiseks järgige neid samme.

1. Hankige funktsiooni uusim versioon, importides selle globaalsest hoidlast. Lisateavet vt impordi funktsioon globaalsest [hoidlast](e-invoicing-import-feature-global-repository.md).
2. Valige funktsioonide loetelust funktsioon, mille alust soovite muuta.
3. Valige vahekaardil **Versioonid** suvand Uus **,** et luua mustandversioon.
4. Valige **Aluse muutmine**.
5. Valige dialoogiboksis **Rebase'i** versioon funktsioonist, mida soovite uuesti kasutada.
6. Valige nupp **OK**.
7. Vaadake üle funktsiooni komponendid ja tehke vajalikud muudatused.
8. Valige funktsiooni, mille alus on muudetud, lõpule viimiseks suvand **Muuda olekut**. Kui aluse muutmine on lõpule viidud, saate teostada täiendavaid toiminguid.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Hankige konkreetne elektroonilise arveldamise funktsioonide versioon

Kui loote elektroonilise arveldamise funktsioonist uue versiooni, loob süsteem koopia uusimast funktsiooniversioonist. Funktsiooni varasema versiooni kasutamiseks uue versiooni alusena valige versioon ja seejärel valige käsk **Hangi see versioon**. Luuakse funktsiooni uus mustandversioon, mis on valitud versiooni koopia.
