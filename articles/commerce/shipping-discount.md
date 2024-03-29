---
title: Saatmise allahindlus
description: See artikkel kirjeldab lähetuse allahindluse võimalusi moodulis Microsoft Dynamics 365 Commerce ja seadistust, mida on nende kasutamiseks vaja.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: 74cfe5246ad72cbdedd0ed4e3b3394bf7277919e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473846"
---
# <a name="shipping-discount"></a>Saatmise allahindlus

[!include [banner](includes/banner.md)]

See artikkel kirjeldab lähetuse allahindluse võimalusi moodulis Microsoft Dynamics 365 Commerce ja seadistust, mida on nende kasutamiseks vaja.

Vaba või allahinnatud saatmine on üks tegur, mis mõjutab klientide võrguostu langetamist. Oma tulu suurendamiseks kande kohta kasutavad paljud jaemüüjad tasuta lähetuse soodustust, et motiveerida kliente ostukorvi suuruste suurendamiseks.

Commerce toetab saadetise allahindluse võimalust, mis võimaldab jaemüüjatel konfigureerida allahindlusprotsendi saatekuludes konkreetse lähetusviisi puhul, kui kvalifitseeritud kaupade müügi kogusumma kandes vastab kindlatele kriteeriumitele. Näide stsenaariumist, mis kasutab saadetise allahindluse võimalust, on "Kulutamine $50 rohkem, et saada tasuta öösel saatmine."

## <a name="prerequisites"></a>Eeltingimused

Lähetuse allahindluse võimalust toetavad Commerce’i kanali täpsemad [automaatsete kulude](/dynamics365/unified-operations/retail/omni-auto-charges) funktsioonid. Lähetuse allahindluse võimaluse **tööks peate lubama Commerce Headquartersi Commerce’i parameetrite lehe klienditellimuste vahekaardil Kasuta täpsemate automaatsete** **·** **tasude** konfiguratsiooni. Jaemüüjad saavad kasutada täpsemate automaatsete kulude funktsiooni erinevat tüüpi tasude (nt käsitsemine, installimine ja likvideerimine) häälestamiseks.

Saadetise allahindlust rakendatakse ainult saatekuludele. Seetõttu peab jaemüüja täpsustama, millised tasud on saatekulud. Saatekulude määramiseks minge rakendusse Commerce Headquarters **\>\>** **·** **kanali** häälestuse kulude kood ja seadke soovitud kulude jaoks saatmistasu suvandiks Jah.

![Saate määrata tasu saatekuludena.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Konfiguratsioon

Saadetise allahindluse võimalus on mitmetasandiline ja toetab ainult arvutamistüübi **Protsent maha** arvutamist. Lähetusallahindluse seadistamist minge Commerce Headquartersi lähetusläve **allahindlusele hinnakujunduse ja \> allahindluste korral**. Seejärel saate määrata tarneviisi, mille suhtes allahindlus rakendub, määratleda ühe või mitu summaläve ja seadistada igale lävele allahindluse protsendi. Saate kategooriate või toodete loendit konfigureerida kvalifitseeritud kaupadena. Sel viisil arvestatakse ainult kandes olevate kaupade müügisummat, kui hinnakujundusmootor hindab, kas kande kogusumma vastab lävele.

> [!NOTE]
> Erinevalt teistest allahindlustüüpidest ei loo saadetise allahindlus allahindluse ridu. Selle asemel redigeerib see otse lähetustasu ja lisab kulu kirjeldusele allahindluse nime.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
