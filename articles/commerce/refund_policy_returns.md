---
title: Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine
description: See teema selgitab, kuidas seadistada kanali tagastuste ja tagasimaksete poliitikat.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 89e8fe78414e73053317ebe19e3afcc89231d440
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979699"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Ülevaade

Kanali tagastuspoliitika rakenduses Dynamics 365 Commerce võimaldab jaemüüjatel määrata rakendamisi, mille alusel saab lubada maksevahendeid kassaseadmes tagastuse töötlemiseks.  

See teema kirjeldab etappe, kuidas seadistada kanali tagastuste ja tagasimaksete poliitikat.

Poliitika ulatus piirdub hetkel maksevahendi määramisega, mida saab kanali jaoks lubada. Lubatute loend põhineb ostu sooritamiseks kasutatavatel makseviisidel. Näide:

- Kui ost tehti kinkekaardi abil, on kaupluse poliitika töödelda tagasimakseid ainult uuele kinkekaardile või anda kaupluse krediiti. 
- Kui tehing on tehtud sularaha kasutades, on tagasimakse lubatud valikud sularaha, kinkekaart ja kliendikonto, kuid mitte krediitkaart. 


## <a name="enable-return-policy"></a>Tagastuspoliitika lubamine

Kanali tagastuspoliitika funktsiooni lubamiseks tehke järgmist.

1. Avage tööruum **Funktsioonihaldus** rakenduses Dynamics 365 Commerce.
2. Otsige funktsiooni nimede loendist funktsiooni **Luba kanali tagastuspoliitikad**.
3. Valige **Luba kohe**. 

## <a name="configure-return-policy"></a>Tagastuspoliitika konfigureerimine

Jaekaupluse või jaemüügi võrgukanali tagastuspoliitika konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Tagastused** \> **Kanali tagastuspoliitika**.

2. Valige **Uus**, et luua uus tagastuspoliitika mall. Olemasoleva malli kasutamiseks valige vasakul paneelil mall. Uute mallide jaoks lisage nimi ja kirjeldus, mis aitab teil tuvastada poliitika, kui seda kanalile rakendatakse.

   ![Uue tagastuspoliitika lisamine](media/Return-policy-page1.png "Uue tagastuspoliitika lisamine")
     
   
3. Jaotises **Lubatud tagasimakse viisid** määratlege **lubatud** tagastamise maksevahendid, mis on igale makseviisile omased.
   ![Makseviiside lisamine](media/Return-policy-page2.PNG "Lubatud makseviiside määramine makse tüübi kohta")
   
    > [!IMPORTANT]
    > - Makseviisid tuletatakse organisatsiooni jaoks määratud makseviisidest.
    > - Iga loetletud makseviisi jaoks lubatud tagastuse maksevahendi tüübi lisamine tagab, et tagastuse saab teha lubatud tagastuse maksevahendi tüübile.
    
4. Seostage tagastuspoliitika mall kauplustega, kus seda kasutatakse. Valige suvand **Lisa** vahekaardil **Jaemüügikanalid** ja seostage saadaolevad kanalid. 

    - Valige dialoogikastis **Vali organisatsiooni sõlmed** kauplused, regioonid ja organisatsioonid, millega mall peaks seotud olema.
    - Iga kauplusega saab seostada ainult ühe tagastuspoliitika malli.
    - Kasutage noolenuppe, et valida kauplusi, regioone või organisatsioone.
    - Poliitika jõustumiskuupäev on kuupäev, mil poliitikad rakendatakse kanalitele ja kanali töid käitatakse. 

    ![Organisatsioonisõlmede dialoogiakna valimine](media/Return-policy-page3.PNG "Organisatsioonisõlmede dialoogiakna valimine")

5. Lehel **Jaotusgraafik** käitage tööd **1070**, et muuta kanali tagastuspoliitika kassa jaoks kättesaadavaks.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Kanali tagastuspoliitika eelvaate vaatamine kassas

Järgige etappe ühes järgmistest näidetest, et vaadata kassas lubatud tagastuse maksevahendi tüüpe.

1. Logige kassasse kassapidaja või juhina sisse.
2. Jaotises **Vahetus ja sahtel** valige käsk **Näita töölehte**.
3. Valige tagastuse osaks olev kanne. 
4. Valige tagastuseks kaubad ja valige makseviis.  
- Kui valitud maksevahendi tüüp on tagastuse maksevahendi tüüpide lubatud loendis, saab kassapidaja kande lõpule viia.
- Kui valitud maksevahend pole lubatud, kuvatakse veateade.
- Valige suvand **Võlgnevus**, et kuvada kõikide lubatud tagastuse maksevahendi tüüpide loend.

- või -

1. Logige kassasse kassapidaja või juhina sisse.
2. Valige **Tagastuskanne** ja sisestage kviitungi ID vöötkoodi skannimise või käsitsi sisestamisega. 
3. Valige tagastuse osaks olev kanne. 
4. Valige tagastuseks kaubad ja valige makseviis.  
- Kui valitud maksevahendi tüüp on tagastuse maksevahendi tüüpide lubatud loendis, saab kassapidaja kande lõpule viia.
- Kui valitud maksevahend pole lubatud, kuvatakse veateade.
- Valige suvand **Võlgnevus**, et kuvada kõikide lubatud tagastuse maksevahendi tüüpide loend.

![Tagasimakse pole lubatud](media/Return-policy-page6.png "Tagasimakse tüüp ei ole lubatud")



![Makseviiside loend](media/Return-policy-page5.PNG "Tagasimakse tüübid on lubatud")


[!INCLUDE[footer-include](../includes/footer-banner.md)]