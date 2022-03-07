---
title: Soodustuste aruanne
description: Väljavõtte aruandes selgitatakse soodustusi, kuhu töötaja on hetkel registreeritud.
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 46f7358684502a4bf05854fbcb5cca9a1eb2c87c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548051"
---
# <a name="benefit-statement"></a>Soodustuste aruanne

**Soodustuste väljavõte** annab väljavõtte soodustustest, kuhu töötaja on hetkel registreeritud. Aruandele pääseb otse juurde töötaja või soodustuse administraator. **Soodustuste väljavõte** annab töötaja registreeritud soodustuste, valikute, kulude ja registreeritud ülalpeetavate või kasusaajate loendi. Väljavõtte saab printida ühe või mitme töötaja kohta.

> [!NOTE]
**Soodustuste väljavõtte** funktsioon peab olema lubatud tööruumis **Funktsioonide haldus**. Selleks peab **Soodustuste halduse** funktsioon olema funktsioonide halduses sisse lülitatud. 


## <a name="importing-the-benefit-statement"></a>Soodustuste väljavõtte importimine 

Enne **Soodustuste väljavõtte** saadaval olemist peate **Soodustuste väljavõtte** importima aruandekonfiguratsiooni abil. Selleks läbige järgmised sammud:

1.  Avage **Süsteemi haldus** tööruum.

2.  Valige **Elektroonilise aruandluse** paan.

3.  Minge **Konfiguratsiooniteenuste pakkujad** ja valige **Hoidlad**.

  ![Hoidlate valik.](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  Valige loendist **Inimressursid** ja seejärel käsk **Ava**.

    ![Konfiguratsioonide hoidlad.](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  Valige vasakul paanil **Soodustuste väljavõtte mudel** ja laiendage seda nii, et kuvaks **Soodustuste väljavõtte vorming**.

6.  Valige vasakult paanilt **Soodustuste väljavõtte vorming**.

7.  Ekraani paremal küljel on **Versioonid** kiirkaart. Valige **Impordi**.

    ![Versioonide kiirkaart.](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>Soodustuste väljavõtte loomine PDF-failina

Vaikimisi prinditakse **Soodustuste väljavõte** Microsoft Word dokumendina. PDF-vormingus printimiseks peate **Elektroonilise aruandluse sihtkohas** konfigureerima PDF-suvandi. 

1. Selleks minge **Süsteemihalduse tööruum** > **Elektrooniline aruandlus** > **Seotud lingid** > **Elektroonilise aruandluse sihtkoht**.

1.  Valige suvand **Uus**.

2.  Väljal **Viide** valige **Soodustuste väljavõtte vorming**.

3.  Valige **Faili sihtkoht** kiirkaardil **Uus**.

4.  Väljale **Nimi** sisestage **Soodustuste väljavõte PDF**.

5.  Väljal **Faili komponendi nimi** valige suvand **Soodustuste väljavõte**.

6.  Märkige ruut **Teisenda PDF-vormingusse**.

7.  Valige menüükäsust **Sätted**. 

    ![Faili sihtkoht.](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  Valige kiirkaart **Fail** ja seejärel valige **Lubage**.

9.  Valige nupp **OK**.
   
> [!NOTE]
> Soodustuste haldamise funktsioon on eelversiooni olekus. **Elektroonilise aruandluse sihtkoha** aruandes meili sihtkoha sätte kasutamisel on teada probleem. Võite saada tõrketeate ja e-kirja saatmine ebaõnnestub.

**Soodustuste väljavõtet** saab luua järgmistel lehtedel:

-   **Soodustuste halduse tööruumi** > **Lingid** > **Aruanded** > **Soodustuste väljavõte**

-   **Töötajad (pärandvorm)** > **Isikuandmete vahekaart** > **Soodustuste väljavõte**

-   **Sujuv töötajate sisenemine** > **Soodustuste aruanne** > **Soodustuste väljavõte**

-   **Töötaja iseteenindus** > **Soodustused** > **Kuva Soodustuste väljavõte**

> [!NOTE]
>  Juurdepääs **Soodustuste väljavõtetele** **Töötaja iseteeninduses** on kontrollitud privileegiga **Vaata soodustuste väljavõtet**. See on **Töötaja iseteeninduse soodustuste** kohustuse all. See privileeg on töötajatele vaikimisi antud.

## <a name="report-contents"></a>Aruande sisu

**Soodustuste väljavõte** prindib töötaja kinnitatud plaanivalikud, sh kõik loobutud plaanid. Järgmine pilt näitab selle aruande näidet. 

![Soodustuste väljavõtte aruanne.](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

Aruandes kuvatakse **Plaan**, **Katvuse võimalused**, **Töötaja kulu** ja **Tööandja kulu**. Aruandes loetletakse ka kõik kaetud ülalpeetavad. Kui plaaniga on seotud kasusaajad, kuvatakse kasusaajad ning nende jaotuse prioriteet ja protsent.

**Soodustuste väljavõtte** aruande saab printida korraga mitmele töötajale, kasutades **Lisatavad kirjed** kiirkaarti **Soodustuste väljavõtted** lehel.
