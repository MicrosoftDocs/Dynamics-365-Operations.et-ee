---
title: Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine
description: See teema selgitab, kuidas seadistada kanali tagastuste ja tagasimaksete poliitikat.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: 4346f9eefa04688c80ce2512a7972bfd4627942c
ms.sourcegitcommit: 53fad4d4b5fb67aa75550956ec205f456a5be01d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/17/2021
ms.locfileid: "7388929"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine

[!include [banner](includes/banner.md)]

Kanali tagastuspoliitika rakenduses Dynamics 365 Commerce võimaldab jaemüüjatel määrata rakendamisi, mille alusel saab lubada maksevahendeid kassaseadmes tagastuse töötlemiseks.  

See teema kirjeldab etappe, kuidas seadistada kanali tagastuste ja tagasimaksete poliitikat.

Poliitika ulatus piirdub hetkel maksevahendi määramisega, mida saab kanali jaoks lubada. Lubatute loend põhineb ostu sooritamiseks kasutatavatel makseviisidel. Näide:

- Kui ost tehti kinkekaardi abil, on kaupluse poliitika töödelda tagasimakseid ainult uuele kinkekaardile või anda kaupluse krediiti. 
- Kui tehing on tehtud sularaha kasutades, on tagasimakse lubatud valikud sularaha, kinkekaart ja kliendikonto, kuid mitte krediitkaart. 

## <a name="enable-return-policy"></a>Tagastuspoliitika lubamine

Kanali tagastuspoliitika funktsionaalsuse lubamiseks Commerce peakorteris toimige järgmiselt.

1. Avage tööruum **Funktsioonihaldus** rakenduses Dynamics 365 Commerce.
1. Otsige funktsiooni nimede loendist funktsiooni **Luba kanali tagastuspoliitikad**.
1. Valige **Luba kohe**.
1. **Jaotusgraafiku** lehel käitage **1110** (globaalne konfiguratsioon) funktsioonimuutuse tööks.

## <a name="configure-return-policy"></a>Tagastuspoliitika konfigureerimine

Jaekaupluse või jaemüügi võrgukanali tagastuspoliitika konfigureerimiseks tehke järgmist.

1. Avage **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Tagastused** \> **Kanali tagastuspoliitika**.

1. Valige **Uus**, et luua uus tagastuspoliitika mall. Olemasoleva malli kasutamiseks valige vasakul paneelil mall. Uute mallide jaoks lisage nimi ja kirjeldus, mis aitab teil tuvastada poliitika, kui seda kanalile rakendatakse.

   ![Uue tagastuspoliitika lisamine.](media/Return-policy-page1.png)
     
   
1. Jaotises **Lubatud tagasimakse viisid** määratlege **lubatud** tagastamise maksevahendid, mis on igale makseviisile omased.
   ![Lubatud makseviiside määramine makse tüübi kohta.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Makseviisid tuletatakse organisatsiooni jaoks määratud makseviisidest.
    > - Iga loetletud makseviisi jaoks lubatud tagastuse maksevahendi tüübi lisamine tagab, et tagastuse saab teha lubatud tagastuse maksevahendi tüübile.
    
1. Seostage tagastuspoliitika mall kauplustega, kus seda kasutatakse. Valige suvand **Lisa** vahekaardil **Jaemüügikanalid** ja seostage saadaolevad kanalid. 

    - Valige dialoogikastis **Vali organisatsiooni sõlmed** kauplused, regioonid ja organisatsioonid, millega mall peaks seotud olema.
    - Iga kauplusega saab seostada ainult ühe tagastuspoliitika malli.
    - Kasutage noolenuppe, et valida kauplusi, regioone või organisatsioone.
    - Poliitika jõustumiskuupäev on kuupäev, mil poliitikad rakendatakse kanalitele ja kanali töid käitatakse. 

    ![Organisatsioonisõlmede dialoogiakna valimine.](media/Return-policy-page3.png)

1. Lehel **Jaotusgraafik** käitage tööd **1070**, et muuta kanali tagastuspoliitika kassa jaoks kättesaadavaks.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Kanali tagastuspoliitika eelvaate vaatamine kassas

Järgige etappe ühes järgmistest näidetest, et vaadata kassas lubatud tagastuse maksevahendi tüüpe.

1. Logige kassasse kassapidaja või juhina sisse.
1. Jaotises **Vahetus ja sahtel** valige käsk **Näita töölehte**.
1. Valige tagastuse osaks olev kanne. 
1. Valige tagastuseks kaubad ja valige makseviis.  
    - Kui valitud maksevahendi tüüp on tagastuse maksevahendi tüüpide lubatud loendis, saab kassapidaja kande lõpule viia.
    - Kui valitud maksevahend pole lubatud, kuvatakse veateade.
    - Valige suvand **Võlgnevus**, et kuvada kõikide lubatud tagastuse maksevahendi tüüpide loend.

- või -

1. Logige kassasse kassapidaja või juhina sisse.
1. Valige **Tagastuskanne** ja sisestage kviitungi ID vöötkoodi skannimise või käsitsi sisestamisega. 
1. Valige tagastuse osaks olev kanne. 
1. Valige tagastuseks kaubad ja valige makseviis.  
    - Kui valitud maksevahendi tüüp on tagastuse maksevahendi tüüpide lubatud loendis, saab kassapidaja kande lõpule viia.
    - Kui valitud maksevahend pole lubatud, kuvatakse veateade.
    - Valige suvand **Võlgnevus**, et kuvada kõikide lubatud tagastuse maksevahendi tüüpide loend.

![Tagasimakse tüüp ei ole lubatud.](media/Return-policy-page6.png)



![Tagasimakse tüübid on lubatud.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
