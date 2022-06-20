---
title: Isikuandmete redigeerimise piiramine
description: Siin saate töötajate jaoks piirata kontaktteabe redigeerimist rakenduses Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877681"
---
# <a name="restrict-editing-of-personal-information"></a>Isikuandmete redigeerimise piiramine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

See artikkel kirjeldab, kuidas piirata töötajatel redigeerida kontakti üksikasju Dynamics 365 Human Resources. Vahel tekib vajadus takistada töötajatel redigeerida kindlaid kontaktandmeid, nt nende töökoha asukohta või meiliaadressi.

> [!NOTE]
> Selle funktsiooni kasutamiseks peate esmalt funktsioonihalduses lubama funktsiooni **(Eelversioon) Piirake töötajatel aadressi- ja kontaktteabe lisamist või redigeerimist kindlal otstarbel**. Lisateavet funktsioonide eelversioonide lubamise kohta vt [Funktsioonide haldamine](hr-admin-manage-features.md).<br><br>![Luba eelvaatefunktsioon.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Valige teave, mida töötaja saab lisada või redigeerida

1. Valige Human Resourcesis **Personalihaldus**, valige **Lingid** ja seejärel valige **Human Resourcesi parameetrid**.

   ![Avage inimressursside parameetrid.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Valige lehel **Inimressursside parameetrid** vahekaart **Töötaja iseteenindus**.

   ![Valige Töövõtja iseteenindus.](./media/hr-employee-self-service-tab.png)

3. Tühjendage vahekaardil **Töötaja iseteenindus** kõik jaotises **Aadress ja kontaktandmed** olevad andmed, mida töötaja ei peaks ise lisama ega redigeerima. Selles näites oleme tühjendanud kontaktandmete valiku **Ettevõte**.

   ![Ettevõtte kontaktteabe redigeerimise piiramine.](./media/hr-employee-self-service-restrict-business.png)

4. Valige käsk **Salvesta**.

   ![Salvesta muudatused.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Töötaja vaade

Pärast seda, kui olete töötajatel keelanud kontaktandmeid lisada või redigeerida, saavad nad seda teavet vaadata, kuid mitte muuta.

Selles näites on töötajatel keelatud redigeerida **ettevõtte** kontaktteavet, kuid töötaja **iseteeninduses** saavad nad seda teavet siiski vaadata:

![Kuva ettevõtte kontaktteave.](./media/hr-employee-self-service-restrict-view.png)

Kui töötaja valib ettevõtte kontaktteabe, kuvatakse paan **Aadressi redigeerimine** kirjutuskaitstuna ja ta ei saa ühegi välja teavet muuta.

![Ettevõtte kontaktteave kuvatakse kirjutuskaitstuna.](./media/hr-employee-self-service-restrict-read-only.png)

Kui töötaja valib uue aadressi lisamiseks **Lisa**, ei saa ta ripploendist **Eesmärk** valida väärtust **Ettevõte**.

![Töötaja ei saa ettevõtte aadressi lisada.](./media/hr-employee-self-service-restrict-add.png)

Sama olukord avaneb töötajale ka siis, kui ta valib lehel **Isikuandmed** käsu **Kontakti üksikasjad** ja lisab uue aadressi. Ripploendis **Eesmärk** kuvatakse ainult seda tüüpi teave, mida töötajal on õigus lisada. 

![Töötaja ei saa valida eesmärgi ripploendist ettevõtet.](./media/hr-employee-self-service-restrict-purpose.png)

Vaate **Kontakti üksikasjad** ruudustikus on nüüd kuvatud **Eesmärk**.

![Kontakti üksikasjade ruudustikus on kuvatud eesmärk.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Vt ka

[Töövõtja ja juhataja iseteeninduskeskuse ülevaade](hr-employee-manager-self-service-overview.md)<br>
[Human Resourcesi parameetrite konfigureerimine](hr-setup-parameters.md)<br>
[Isiklike andmete muutmine](hr-employee-manager-self-service-edit-personal-information.md)
