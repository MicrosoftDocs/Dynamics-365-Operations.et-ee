---
title: Maksufunktsiooni tugi üleviimistellimuste jaoks
description: See artikkel selgitab uut maksufunktsiooni toetust üleviimistellimustele, kasutades maksu arvutamise teenust.
author: Kai-Cloud
ms.date: 10/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b611abb2d68d93178d0c26ba40b22f1b8d26b191
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203105"
---
# <a name="tax-feature-support-for-transfer-orders"></a>Maksufunktsiooni tugi üleviimistellimuste jaoks

[!include [banner](../../includes/banner.md)]

See artikkel annab teavet maksu arvutamise ja üleviimistellimuste sisestamise kohta. Selle funktsiooniga saate seadistada laoülekannete maksuarvestust ja üleviimistellimuste sisestamist. Euroopa Liidu (EL) käibemaksu määruste kohaselt peetakse laoülekandeid EL-i siseseks tarneks ja EL-siseseks soetamiseks.

Selle funktsiooni konfigureerimiseks ja kasutamiseks tuleb läbida kolm peamist sammu.

1. **RCS-i seadistus:** seadistage regulatiivses konfiguratsiooniteenuses maksufunktsioon, maksukoodid ja maksukoodide kohaldatavus maksukoodi määramise jaoks üleviimistellimustes.
2. **Dynamics 365 finantside seadistus:** finantsides lubage **üleviimistellimusel** maks, seadistage varudele maksu arvutamise teenuse parameetrid ja seadistage tuummaksu parameetrid.
3. **Lao seadistus:** seadistage üleviimistellimuse kannete laokonfiguratsioon.

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a>Maksu- ja üleviimistellimuse kannete RCS-i loomine

Järgige neid samme üleviimistellimusse lisatava maksu seadistamiseks. Siin kuvatud näites on üleviimistellimus Hollandist Belgiasse.

1. **Maksufunktsioonide** lehe vahekaardil **Versioonid** valige mustandi funktsiooni versioon ja seejärel valige käsk **Redigeeri**.

2. Uute maksukoodide loomiseks valige **Maksufunktsiooni seadistamise** lehel vahekaardil **Maksukoodid** suvand **Lisa**. Selles näites luuakse kolm maksukoodi: **NL-maksuvaba**, **BE-RC-21** ja **BE-RC+21**.

    - Kui üleviimistellimus lähetatakse Hollandi laost, rakendatakse Hollandi käibemaksuvabastuse maksukoodi (**NL-maksuvaba**).
      
        Looge maksukood **NL-maksuvabastus**.
        1. Valige suvand **Lisa**, sisestage **NL-maksuvabastus** väljale **Maksukood**.
        2. Valige käsk **Netosumma järgi** väljal **Maksukomponent**.
        3. Valige käsk **Salvesta**.
        4. Valige tabelis **Määr** suvand **Lisa**.
        5. Määrake valikul **On maksuvabastus** **Jah** jaotises **Üldine**.
        6. Sisestage väljas **Maksuvabastuse kood** **EÜ**.

    - Kui üleviimistellimus on vastu võetud Belgia lattu, rakendatakse pöördtasu mehhanism, kasutades maksukoode **BE-RC-21** ja **BE-RC+21**.
        
        Looge maksukood **BE-RC-21**.      
        1. Valige suvand **Lisa**, sisestage **BE-RC-21** väljale **Maksukood**.
        2. Valige käsk **Netosumma järgi** väljal **Maksukomponent**.
        3. Valige käsk **Salvesta**.
        4. Valige tabelis **Määr** suvand **Lisa**.
        5. Sisestage väljale **Maksumäär** väärtus **–21**.
        6. Määrake valikul **On pöördmaks** väärtuseks **Jah** jaotises **Üldine**.
        7. Valige käsk **Salvesta**.
        
        Looge maksukood **BE-RC+21**.
        1. Valige suvand **Lisa**, sisestage **BE-RC-21** väljale **Maksukood**.
        2. Valige käsk **Netosumma järgi** väljal **Maksukomponent**.
        3. Valige käsk **Salvesta**.
        4. Valige tabelis **Määr** suvand **Lisa**.
        5. Sisestage väljale **Maksumäär** väärtus **21**.
        6. Valige käsk **Salvesta**.

3. Määratlege maksurühm.
    1. Valige **Halda veerge** ja seejärel valige reaväli **Maksurühm**.
    2. Valige **->** ja seejärel **OK**.
    3. Maksurühma lisamiseks valige **Lisa**.
    4. Sisestage veergu **Maksurühm** **AR-EU** ja seejärel valige **NL-vabastuse** maksukood.
    5. Maksurühma lisamiseks valige **Lisa**.
    6. Sisestage veergu **Maksurühm** **RC-VAT** ja seejärel valige maksukoodid **BE-RC-21** ja **BE-RC+21**.
4. Määratlege kauba maksurühm.
    1. Valige **Halda veerge** ja seejärel valige reaväli **Kauba maksurühm**.
    2. Valige **->** ja seejärel **OK**.
    3. Kauba maksurühma lisamiseks valige **Lisa**.
    4. Sisestage veergu **Kauba maksurühm** väärtus **FULL**. Valige maksukoodid **BE-RC-21**, **BE-RC+21** ja **NL-vabastus**.
5. Määratlege maksugrupi kohaldatavus.

    1. Valige suvand **Halda veerge** ja seejärel valige veerud, mida tuleks kasutada kohaldatavustabeli koostamiseks.

        > [!NOTE]
        > Lisage kindlasti tabelisse **Äriprotsessi** ja **Maksusuundade** veerud. Mõlemad veerud on olulised üleviimistellimuste maksufunktsioonide jaoks.

    2. Rakendatavuse reeglite lisamine. Ärge jätke välja **Maksurühm** tühjaks.
        
        Saate lisada üleviimistellimuse saadetisele uue reegli.
        1. Valige tabelis **Rakendatavuse reeglid** suvand **Lisa**.
        2. Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.
        3. Väljale **Riigist/regioonist lähetamine** sisestage **NLD**.
        4. Väljale **Riiki/regiooni lähetamine** sisestage **BEL**.
        5. Väljal **Maksusuund** valige **Väljastus**, et muuta reegel üleviimistellimuse saadetisele rakendatavaks.
        6. Valige väljal **Maksugrupp** **AR-EL**.
        
        Saate lisada üleviimistellimuse sissetulekule muu reegli.
        
        1. Valige tabelis **Rakendatavuse reeglid** suvand **Lisa**.
        2. Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.
        3. Väljale **Riigist/regioonist lähetamine** sisestage **NLD**.
        4. Väljale **Riiki/regiooni lähetamine** sisestage **BEL**.
        5. Väljal **Maksusuund** valige **Sisend**, et muuta reegel üleviimistellimuse sissetulekule rakendatavaks.
        6. Valige väljal **Maksugrupp** **RC-VAT**.

6. Määratlege kauba maksugrupi kohaldatavus.

    1. Valige suvand **Halda veerge** ja seejärel valige veerud, mida tuleks kasutada kohaldatavustabeli koostamiseks.
    2. Rakendatavuse reeglite lisamine.
        
       > [!NOTE]
       > Kui teie maksustatava dokumendi ridadel vaikimisi määratud kauba käibemaksugrupp on juba õige, jätke see maatriks tühjaks. 
        
        Saate lisada üleviimistellimuse saadetisele ja kviitungile uue reegli.
        1. Lehel **Rakendatavuse reeglid** valige **Lisa**.
        2. Väljal **Äriprotsess** valige **Ladu**, et muuta reegel üleviimistellimusel rakendatavaks.
        3. Valige väljal **Kauba maksugrupp** **FULL**.
7. Viige uus maksufunktsiooni versioon lõpule ja avaldage see.


## <a name="set-up-finance-for-transfer-order-transactions"></a>Finantsülevaadete seadistamine kannete üleviimiseks

Üleviimistellimuste lubamiseks ja maksude seadistamiseks järgige neid samme.

1. Jaotises Finantsid avage **Tööruumid** > **Funktsioonihaldus**.
2. Leidke ja valige loendist funktsioon **Üleviimistellimuse maks** ning seejärel valige **Luba kohe**, et see sisse lülitada.

    > [!IMPORTANT]
    > Funktsioon **Üleviimistellimuse maks** sõltub täielikult maksuarvestuse teenusest. Seetõttu saab seda sisse lülitada alles pärast maksuarvestuse teenuse installimist.

    ![Maks funktsioonis üleviimistellimus.](../media/image7.png)

3. Lubage maksuarvestuse teenus ja valige äriprotsess **Ladu**.

    > [!IMPORTANT]
    > Peate selle etapi jaotises Finants lõpule viima iga juriidilise isiku puhul, kus soovite, et maksuarvestuse teenus ja üleviimistellimuste maksufunktsioonid oleks saadaval.

    1. Minge **Maks** > **Seadistamine** > **Maksukonfiguratsioon** > **Maksuarvutuse parameetrid**.
    2. Väljal **Äriprotsess** valige **Ladu**.

4. Kontrollige, kas pöördmaksu mehhanism on seadistatud. Avage menüü **Pearaamat** \> **Seadistus** \> **Parameetrid** ja seejärel veenduge, et vahekaardil **Pöördmaks** on valik **Luba pöördmaks** seatud väärtuseks **Jah**.

    ![Pöördmaksu valiku lubamine.](../media/image9.png)

5. Kontrollige, et seotud maksukoodid, maksugrupid, kauba maksugrupid ja KM-i registreerimisnumbrid on jaotises Finants seadistatud vastavalt maksuarvestuse teenuste juhistele.
6. Seadistage vahetransiidi konto. See samm on nõutav ainult juhul, kui üleviimistellimusele rakendatav maks ei ole rakendatav maksuvabastuse või pöördmaksumehhanismi puhul.

    1. Avage **Maksud** > **Seadistus** > **Käibemaks** > **Pearaamatu sisestusgrupid**.
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
