---
title: Maksufunktsiooni tugi üleviimistellimuste jaoks
description: See teema selgitab uut maksufunktsiooni tuge üleviimistellimustele, kasutades maksuarvutuse teenust.
author: Kai-Cloud
ms.date: 09/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 01bf7c251fe57072f042c9187b9f5b6b6687ab0f
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500072"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Maksufunktsiooni tugi üleviimistellimuste jaoks

[!include [banner](../../includes/banner.md)]

Selles teemas antakse teavet maksuarvutuse ja üleviimistellimuste sisestuse kohta. Selle funktsiooniga saate seadistada laoülekannete maksuarvestust ja üleviimistellimuste sisestamist. Euroopa Liidu (EL) käibemaksu määruste kohaselt peetakse laoülekandeid EL-i siseseks tarneks ja EL-siseseks soetamiseks.

Selle funktsiooni konfigureerimiseks ja kasutamiseks tuleb läbida kolm peamist sammu.

1. **RCS-i seadistus:** seadistage regulatiivses konfiguratsiooniteenuses maksufunktsioon, maksukoodid ja maksukoodide kohaldatavus maksukoodi määramise jaoks üleviimistellimustes.
2. **Finantside häälestamine:** lülitage rakenduses Microsoft Dynamics 365 Finance sisse **Üleviimistellimuse maksu** funktsioon, seadistage lao maksuteenuse parameetrid ja tuummaksu parameetrid.
3. **Lao seadistus:** seadistage üleviimistellimuse kannete laokonfiguratsioon.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Maksu- ja üleviimistellimuse kannete RCS-i loomine

Järgige neid samme üleviimistellimusse lisatava maksu seadistamiseks. Siin kuvatud näites on üleviimistellimus Hollandist Belgiasse.

1. **Maksufunktsioonide** lehe vahekaardil **Versioonid** valige mustandi funktsiooni versioon ja seejärel valige käsk **Redigeeri**.

    ![Redigeerimise valimine.](../media/tax-feature-support-01.png)

2. Uute maksukoodide loomiseks valige **Maksufunktsiooni seadistamise** lehel vahekaardil **Maksukoodid** suvand **Lisa**. Selles näites luuakse kolm maksukoodi: **NL-maksuvaba**, **BE-RC-21** ja **BE-RC+21**.

    - Kui üleviimistellimus lähetatakse Hollandi laost, rakendatakse Hollandi käibemaksuvabastuse maksukoodi (**NL-maksuvaba**).
      
        Looge maksukood **NL-maksuvabastus**.
        1. Valige suvand **Lisa**, sisestage **NL-maksuvabastus** väljale **Maksukood**.
        2. Valige käsk **Netosumma järgi** väljal **Maksukomponent**.
        3. Valige käsk **Salvesta**.
        4. Valige tabelis **Määr** suvand **Lisa**.
        5. Lülitage valikul **On maksuvabastus** sisse nupp **Jah** jaotises **Üldine**.

           ![NL-maksuvabastuse maksukood.](../media/tax-feature-support-02.png)

    - Kui üleviimistellimus on vastu võetud Belgia lattu, rakendatakse pöördtasu mehhanism, kasutades maksukoode **BE-RC-21** ja **BE-RC+21**.
        
        Looge maksukood **BE-RC-21**.      
        1. Valige suvand **Lisa**, sisestage **BE-RC-21** väljale **Maksukood**.
        2. Valige käsk **Netosumma järgi** väljal **Maksukomponent**.
        3. Valige käsk **Salvesta**.
        4. Valige tabelis **Määr** suvand **Lisa**.
        5. Sisestage väljale **Maksumäär** väärtus **–21**.
        6. Lülitage valikul **On pöördmaks** sisse nupp **Jah** jaotises **Üldine**.
        7. Valige käsk **Salvesta**.

           ![BE-RC-21 maksukood pöördmaksude jaoks.](../media/tax-feature-support-03.png)
        
        Looge maksukood **BE-RC+21**.
        1. Valige suvand **Lisa**, sisestage **BE-RC-21** väljale **Maksukood**.
        2. Valige käsk **Netosumma järgi** väljal **Maksukomponent**.
        3. Valige käsk **Salvesta**.
        4. Valige tabelis **Määr** suvand **Lisa**.
        5. Sisestage väljale **Maksumäär** väärtus **21**.
        6. Valige käsk **Salvesta**.

           ![BE-RC+21 maksukood pöördmaksude jaoks.](../media/tax-feature-support-04.png)

3. Määratlege maksukoodide kohaldatavus.

    1. Valige suvand **Halda veerge** ja seejärel valige veerud, mida tuleks kasutada kohaldatavustabeli koostamiseks.

        > [!NOTE]
        > Lisage kindlasti tabelisse **Äriprotsessi** ja **Maksusuundade** veerud. Mõlemad veerud on olulised üleviimistellimuste maksufunktsioonide jaoks.

    2. Rakendatavuse reeglite lisamine. Ärge jätke välju **Maksukoodid**, **Maksugrupp** ja **Kauba maksugrupp** tühjaks.
        
        Saate lisada üleviimistellimuse saadetisele uue reegli.
        1. Valige tabelis **Rakendatavuse reeglid** suvand **Lisa**.
        2. Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.
        3. Väljale **Riigist/regioonist lähetamine** sisestage **NLD**.
        4. Väljale **Riiki/regiooni lähetamine** sisestage **BEL**.
        5. Väljal **Maksusuund** valige **Väljastus**, et muuta reegel üleviimistellimuse saadetisele rakendatavaks.
        6. Valige väljal **Maksukoodid** suvand **NL-maksuvabastus**.
        7. Sisestage väljadele **Maksugrupp** ja **Kauba maksugrupp** seotud käibemaksugrupp ja kauba käibemaksugrupp, mis on määratletud teie finantssüsteemis.
        
        Saate lisada üleviimistellimuse sissetulekule muu reegli.
        
        1. Valige tabelis **Rakendatavuse reeglid** suvand **Lisa**.
        2. Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.
        3. Väljale **Riigist/regioonist lähetamine** sisestage **NLD**.
        4. Väljale **Riiki/regiooni lähetamine** sisestage **BEL**.
        5. Väljal **Maksusuund** valige **Sisend**, et muuta reegel üleviimistellimuse sissetulekule rakendatavaks.
        6. Valige väljal **Maksukoodid** suvandid **BE-RC+21** ja **BE-RC-21**.
        7. Sisestage väljadele **Maksugrupp** ja **Kauba maksugrupp** seotud käibemaksugrupp ja kauba käibemaksugrupp, mis on määratletud teie finantssüsteemis.

           ![Kohaldatavusreeglid.](../media/image5.png)

4. Viige uus maksufunktsiooni versioon lõpule ja avaldage see.

    [![Uue versiooni oleku muutmine.](../media/image6.png)](../media/image6.png)

## <a name="set-up-finance-for-transfer-order-transactions"></a>Finantsülevaadete seadistamine kannete üleviimiseks

Üleviimistellimuste lubamiseks ja maksude seadistamiseks järgige neid samme.

1. Jaotises Finantsid avage **Tööruumid** > **Funktsioonihaldus**.
2. Leidke ja valige loendist funktsioon **Üleviimistellimuse maks** ning seejärel valige **Luba kohe**, et see sisse lülitada.

    > [!IMPORTANT]
    > Funktsioon **Üleviimistellimuse maks** sõltub täielikult maksuteenusest. Seetõttu saab seda sisse lülitada alles pärast maksuteenuse installimist.

    ![Maks funktsioonis üleviimistellimus.](../media/image7.png)

3. Lubage maksuteenus ja valige äriprotsess **Ladu**.

    > [!IMPORTANT]
    > Peate selle etapi jaotises Finants lõpule viima iga juriidilise isiku puhul, kus soovite, et maksuteenus ja üleviimistellimuste maksufunktsioonid oleks saadaval.

    1. Avage menüü **Maksud** > **Seadistamine** > **Maksu konfiguratsioon** > **Maksuteenuse häälestus**.
    2. Väljal **Äriprotsess** valige **Ladu**.

      ![Äriprotsessi välja seadistamine.](../media/image8.png)

4. Kontrollige, kas pöördmaksu mehhanism on seadistatud. Avage menüü **Pearaamat** \> **Seadistus** \> **Parameetrid** ja seejärel veenduge, et vahekaardil **Pöördmaks** on valik **Luba pöördmaks** seatud väärtuseks **Jah**.

    ![Pöördmaksu valiku lubamine.](../media/image9.png)

5. Kontrollige, et seotud maksukoodid, maksugrupid, kauba maksugrupid ja KM-i registreerimisnumbrid on jaotises Finants seadistatud vastavalt maksuteenuste juhistele.
6. Seadistage vahetransiidi konto. See samm on nõutav ainult juhul, kui üleviimistellimusele rakendatav maks ei ole rakendatav maksuvabastuse või pöördmaksumehhanismi puhul.

    1. Avage **Maksud** > **Seadistus** > **Käibemaks** \ **Pearaamatu sisestusgrupid**.
    2. Valige väljal **Vahetransiidid** pearaamatu konto.

       ![Vahetransiidi konto valimine.](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a>Peamiste varude seadistamine kannete üleviimiseks

Järgige neid samme, et seadistada peamised varud, et lubada üleviimistellimuse kanded.

1. Looge erinevates riikides või regioonides oma ladude jaoks saatmis- ja lähetuskohad ning lisage iga asukoha esmane aadress.

    1. Avage jaotis **Warehouse management** > **Seadistus** > **Ladu** > **Saidid**.
    2. Valige suvand **Uus** asukoha loomiseks, mille hiljem määrate laole.
    3. Korrake 2. sammu kõigi teiste asukohta puhul, mille peate looma.

    > [!NOTE]
    > Ühe teie valitud asukoha nimi peab olema **Transiit**. Selle protseduuri hilisemates sammudes määrate selle asukoha transiitlaole, nii et maksudega seotud laokandeid saab sisestada üleviimistellimuste "läheta" ja "vastuvõtu" kannetesse. Transiidikoha aadress pole maksuarvestuses oluline. Seetõttu saate selle tühjaks jätta.

    ![Saitide seadistamine.](../media/image11.png)

2. Looge lähetamis-, transiit- ja sihtlaod. Kogu laos säilitatav aadressiteave alistab maksuarvestuse ajal asukoha aadressi.

    1. Avage **Laohaldus** > **Seadistus** > **Ladu** > **Laod**.
    2. Valige suvand **Uus** lao loomiseks ja määrake see vastavale asukohale.
    3. Korrake 2. sammu, et luua ladu igale asukohale vastavalt vajadusele.

       ![Ladude seadistamine.](../media/image12.png)

    > [!NOTE]
    > Lähetamislaost üleviimistellimuse kannete jaoks peab transiitladu olema väljal **Transiitladu** valitud.
    >
    > ![Transiitlao valimine.](../media/image13.png)

3. Veenduge, et üleviimistellimuste kannete varude sisestuste konfiguratsioon on seadistatud.

    1. Avage **Varude haldus** > **Seadistus** > **Sisestus** > **Sisestus**.
    2. Kontrollige vahekaardil **Varud**, et pearaamatukontol on seadistatud nii **Lao väljamineku** kui ka **Lao sissetuleku** sisestamine.

        ![Lao väljamineku ja lao sissetuleku sisestamise seadistamine.](../media/image14.png)

    3. Kontrollige, kas pearaamatukonto on seadistatud **Üksusesiseseks ostureskonto** sisestamiseks.

        ![Üksusesisese ostureskonto sisestuse seadistamine.](../media/image15.png)

    4. Kontrollige, kas pearaamatukonto on seadistatud **Üksusesiseseks müügireskonto** sisestamiseks.

        ![Üksusesisese müügireskonto sisestuse seadistamine.](../media/image16.png)
        
        
  [!INCLUDE[footer-include](../../../includes/footer-banner.md)]
