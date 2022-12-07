---
title: Store Commerce’i rakendus mobiiliplatvormidele
description: See artikkel kirjeldab, kuidas rakenduse Microsoft Dynamics 365 Commerce Store Commerce ja Android iOS kasutamist alustada.
author: stuharg
ms.date: 11/30/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: dc952698a2a3301aff312e8310c58cbbb9cfe290
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815779"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce’i rakendus mobiiliplatvormidele

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See artikkel kirjeldab, kuidas alustada rakenduse Microsoft Dynamics 365 Commerce Store Commerce rakenduste ja Android iOS-iga.

Mobiilirakendused Dynamics 365 Commerce ja Android iOS-i jaoks muudavad täieliku mobiilsete müügikoha (POS) seadmete kasutamise jaemüügikeskkonnas lihtsaks ja lihtsaks. Store Commerce’i mobiilirakendused [tarnivad kõiki Rakenduse Store Commerce](store-commerce.md) Windowsi võimalusi ja rakendusi ning toimetavad hästi paljude iOS-i Android ja telefonide ning tahvelarvutite puhul. Store Commerce’i mobiilirakendused saab installida otse Developeri ja Developer Play rakenduskauplustest ning ei vaja arendajalt nende juurutamiseks või värskendamiseks uut rakendusepaketti. 

Store Commerce’i mobiilirakendused säilitavad täieliku funktsionaalse paarsuse praeguste jaemüügi rakendustega. Lisaks hõlmab rakendus Store Commerce for iOS sihtotstarbelist riistvarajaama tuge, et iOS-i seadmed saaksid suhelda võrgumakseterminalide, kviitungiprinterite ja sularahasahtlitega ilma, et peaks juurutama ühise riistvarajaama. 

> [!IMPORTANT]
> Windowsi poe ärirakendused ja Android  iOS on järgmise loomise kassarakendused Dynamics 365 Commerce. Store Commerce’i rakendused pakuvad mitmeid parendusi oma eelkäijate ees, säilitades samas täieliku funktsionaalse ja funktsiooni paarsuse. Microsoft amortiseerib MPOS-i Android ja iOS Retail POS-i rakendusi 2023. aasta lõpus ning soovitab kasutada store Commerce’i või Cloud POS-i (CPOS) kõigi uute kassa juurutuste puhul. Olemasolevad kliendid peaksid plaanima jaemüügi rakendustest rakendusse Store Commerce üle kanda. Lisateavet vt jaotisest Modern POS-i [migreerimine poe ärisse](pos-extension/migrate-mpos-store-commerce.md). 

## <a name="app-architecture"></a>Rakenduse arhitektuur

Poe äri mobiilirakendused kasutavad režiimis juurutamisel sama topoloogiat nagu Windowsi poe ärirakendus. Store Commerce’i mobiilirakendused on shellirakendused, mis renderdavad CPOS-i otse Commerce Scale Unitist (CSU) ja ühenduvad Headless Commerce ja Commerce headquartersiga CSU kaudu. Shelli rakenduse mudel võimaldab Store Commerce’i rakendustel toetada sihtotstarbelist riistvarajaama otseseks integreerimiseks makseterminali, printeri, sularahasahtli ja muude seadmetega. Riistvaraseadmete kasutamiseks ei pea te häälestama ühiskasutatava riistvarajaama. 

Store Commerce’i mobiilirakenduse värskendamiseks värskendage lihtsalt CSU-d. Rakendus võtab automaatselt vastu kõik uued müügikoha funktsioonid ja funktsioonid. Lisateavet CSU värskendamise kohta vt Commerce Scale [Uniti (pilve) värskenduste ja laienduste rakendamist](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Shelli rakendusi kasutatakse rakenduse poe värskenduste kaudu. Kui väiksem versioon jõuab üldise saadavuseni (GA), avaldab Microsoft selle rakenduse kauplustes. Microsoft võib avaldada ka väheolulisi versioonivärskendusi paigaid kõrge prioriteediga paranduste vabastamiseks.

## <a name="prerequisites"></a>Eeltingimused

Rakenduse Store Commerce mobiilirakendused nõuavad Dynamics 365 Commerce, eriti Rakenduse Commerce headquarters ja CSU komponente. Järgmises tabelis loetletakse minimaalsed operatsioonisüsteemi (OS) ja CSU versioonid, mida Android nõutavad iOS-i mobiilirakendused. 

| Eeltingimus | Android      | iOS  |
| ------------ | ------------ | ---- |
| OS-i versioon   | 7.0          | 15.0 |
| CSU versioon  | 9.38.22266.8 | Määramata  |

## <a name="install-the-app"></a>Rakenduse installimine

Rakenduse Store Commerce mobiilirakendused saate installida otse kaupluste Commerce Store’ist või Kaupluste rakenduskauplusest. 

- [Rakenduse Store Commerce rakendus<a0/& jaoks Android](https://aka.ms/storecommerceandroid)
- [Rakenduse Store Commerce iOS-i jaoks](https://aka.ms/storecommerceios)

Rakenduse Android (.the) jaRakendusTe (.ipa) pakette saab elutsükli teenustes alla laadida ka ühiskasutuses varateegist Microsoft Dynamics . 

## <a name="device-and-register-setup"></a>Seadme ja registri häälestus

Enne kassaaparaati aktiveerimist poe äri mobiilirakendustes peate häälestama seadme ja registri Commerce Headquartersis. Lisateavet vt seadmetest ja [registritest](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Seadme häälestus

Uue seadme loomiseks ja häälestamiseks järgige neid samme.

1. Minge commerce headquartersi rakenduse Retail ja **Commerce Channel häälestamise \> kassa häälestusseadmetesse \>  \>**. 
1. Looge uus seade ja valige **sõltuvalt juurutatud mobiilirakendusest kas Modern POS Android**  **- või Modern POS - iOS** . 

    > [!NOTE] 
    > Modern **POS-i ja Android**  **Modern POS -iOS-i** rakendusetüüpe kasutatakse ka praeguste windowsi rakenduste juurutamiseks ja Android iOS-i jaoks. Pärast MPOS-i amortiseerimist uuendatakse nende rakendusetüüpide **sildid rakendustüüpidele Store Commerce - Android** and **Modern POS - iOS**. 

### <a name="register-setup"></a>Registri häälestus

Saate luua uue registri ja seostada selle loodud seadmega või seostada olemasoleva registri oma uue seadmega. Lisateavet registrite kohta vt teemast Kassaaparaatide [loomine ja seostamine](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Ekraani paigutuse häälestus

Kui te taasostute ekraani kavandi, mis sisaldub teie litsentsiga antud demoandmetes Dynamics 365 Commerce , valib Store Commerce rakendus automaatselt kaasatud klevandi, kui teie seadme ekraani eraldusvõime on vertikaalsuunas alla 480 &times; 853 pikslit. Kuid kui loote ekraani kavandi nullist või kui teie mobiilses seadmes kasutatakse tihendatud paigutusest suuremat eraldusvõimet, veenduge, et loote lahenduse ja seotud nupupaneelid, mis sobivad telefoni või tahvelarvutiga, mille plaanite juurutada. Lisateavet ekraani paigutuse konfiguratsioonide kohta vaadake kassa [kasutajaliidese visuaalsetest konfiguratsioonidest](../pos-screen-layouts.md). 

Kui seadmed ja registrid on commerce headquartersis konfigureeritud, **\> minge jaemüügi ja äri jaemüügi ja äri ID \>** jaotusgraafikutele ja käivitage registrite töö.

## <a name="activate-a-device"></a>Seadme aktiveerimine

Seadme aktiveerimiseks Rakenduse Store Commerce mobiilirakenduses järgige neid samme.

1. Avage rakendus mobiilses seadmes.
1. Sisestage CPOS-i URL, mille leiate elutsükli teenuste keskkonna üksikasjade lehelt, **või rakenduse Commerce headquarters kanali profiilide** lehel (**Jaemüügi- ja ärikanali \> häälestuse \> kanali profiilid**).
1. Logige sisse, kasutades töötaja mandaate, kellel on luba seadmete haldamiseks.
1. Valige kauplus, mis on seotud rakenduse Commerce Headquarters poolt loodud või uuesti kasutatud registriga.
1. Valige register, mille lõite Commerce Headquartersis loodud seadmega.
1. Seade tuleks nüüd aktiveerida. Saate registrisse sisse logida, kasutades valitud kauplusega seotud töötaja operaatori ID ja parooli. 

Lisateavet seadme aktiveerimise kohta vt müügikoha [(POS) seadme aktiveerimisest](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Funktsioonide paarsus Rakendusega Store Commerce for Windows

Järgmises tabelis võrreldakse Store Commerce’i rakenduse võimalusi Windowsis ja Android iOS-i platvorme.

| Funktsioon                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Sihtotstarbeline riistvarajaam                                                            | Jah     | Jah     | Jah |
| Ühiskasutuses riistvarajaam                                                               | Jah     | Jah     | Jah |
| Side võrguseadmetega (makseterminal, printer ja sularahasahtel) | Jah     | Jah     | Jah |
| OLE müügipunkti (OPOS) välisseadmetele kohaliku riistvarajaama kaudu             | Jah     | Nr      | Nr  |
| Ühenduseta režiim                                                                          | Jah     | Nr      | Nr  |

## <a name="additional-resources"></a>Lisaressursid

[Store Commerce’i rakendus](store-commerce.md)

[Store Commerce’i ja Cloud POS-i vahel valimine](../mpos-or-cpos.md)

[Rakenduse Store Commerce häälestus- ja installiprobleemide tõrkeotsing](../troubleshoot/store-commerce-setup-installation.md)
