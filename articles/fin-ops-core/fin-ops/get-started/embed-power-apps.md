---
title: Power Appsi lõuendirakenduste manustamine
description: Selles teemas seletatakse, kuidas manustada kliendis Microsoft Power Appsi lõuendirakendusi, et suurendada toote funktsionaalsust.
author: jasongre
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 7b20d24f79bd84f516e005b9d4a0ecdf6ef848fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752886"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Power Appsi lõuendirakenduste manustamine

[!include [banner](../includes/banner.md)]

Microsoft Power Apps on teenus, mis võimaldab arendajatel ja mittetehnilistel kasutajatel luua kohandatud ärirakendusi mobiilsete seadmete, tahvelarvutite ja veebi jaoks ilma koodi kirjutamata. Finance and Operationsi rakenduste puhul toetatakse integratsiooni Power Appsiga. Teie, teie organisatsiooni või laiema ettevõtete „ökosüsteemi” arendatud lõuendirakendusi saab manustada Finance and Operationsi rakendustes, et suurendada toote funktsionaalsust. Näiteks saate luua Power Appsis lõuendirakenduse, mis täiendab Finance and Operationsi rakendust teisest süsteemist toodud teabega.

Lisateavet Power Appsi manustamise kohta vaadake lühivideost [Kuidas manustada Power Appsi rakendusse](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Manustatud lõuendirakenduse lisamine Power Appsist lehele

### <a name="overview"></a>Ülevaade

Enne Power Appsi rakenduse manustamist klienti peate leidma või looma soovitud visuaalide või funktsioonidega rakenduse. Selles teemas ei kirjeldata rakenduste loomise protsessi üksikasjalikult. Kui hakkasite Power Appsi alles kasutama, lugege [Power Appsi dokumentatsiooni](https://docs.microsoft.com/powerapps/).

Kui olete valmis rakendust manustama, on lehel kindlale lõuendirakendusele juurde pääsemiseks kaks võimalust. Saate valida, kumb meetod sobib teie olukorraga paremini. Esimene meetod kasutab standardsele toimingupaanile lisatud nuppu **Power Apps**. Selle meetodi abil lisatavad rakendused kuvatakse menüünupu **Power Apps** elementidena. Kui valite ühe nendest elementidest, kuvatakse külgpaan, mis sisaldab manustatud rakendust. Teise võimalusena saate rakenduse manustada otse lehel uue vahekaardi, kiirkaardi või labana või tööruumis uue jaotisena.

Manustatud lõuendirakenduse konfigureerimisel saate valida ühe välja, mida kontekstina rakendusse saata. Selle sammu tõttu saab rakendus reageerida praegu vaadatavate andmete põhjal.

> [!NOTE]
> Praegu ei saa seda mehhanismi kasutada mudelipõhiste rakenduste manustamiseks.  

### <a name="details"></a>Details

Järgmises protsessis näidatakse, kuidas manustada Power Appsi lõuendirakendust veebikliendis.

1. Avage leht, kus soovite lõuendirakenduse manustada. See on leht, mis sisaldab andmeid, mis tuleb rakendusse sisendina edastada.
2. Avage paan **Lisa rakendus Power Appsist**.

    - Klõpsake valikut **Suvandid** ja seejärel valige **Isikupärasta see leht**. Valige menüüst **Lisa** suvand **Power Apps**. Lõpuks valige piirkond, kuhu soovite rakendust lisada. Kui soovite rakendust menüünupu Power Apps alt manustada, valige toimingupaan. Kui soovite rakendust otse lehele manustada, valige asjakohane vahekaart, kiirkaart, laba või jaotis (kui kasutate tööruumi).
    - Kui rakenduse avamiseks kasutatakse menüünuppu Power Apps, võite teise võimalusena klõpsata standardse toimingupaani menüünuppu **Power Apps** ja valida seejärel suvandi  **Lisa rakendus**.

3. Manustatud rakenduse konfigureerimine.

    - Väljal **Nimi** on näidatud tekst, mis kuvatakse manustatud rakendust sisaldava nupu või vahekaardi jaoks. Sageli korratakse sellel väljal rakenduse nime.
    - Väljal **Rakenduse ID** on toodud manustatava lõuendirakenduse globaalne ainuidentifikaator (GUID). Selle väärtuse toomiseks leidke rakendus aadressilt [make.powerapps.com](https://make.powerapps.com) ja seejärel heitke pilk väljale **Rakenduse ID** jaotises **Üksikasjad**.
    - Välja **Rakenduse sisendkontekst** jaoks võite valida ka välja, mis sisaldab andmeid, mida soovite rakenduse sisendina edastada. Üksikasju, kuidas rakendus saab juurdepääsu rakendusekomplektist Finance and Operations saadetud andmetele, vaadake selle jaotise allpool olevast teemast [Finance and Operationsi rakendustest saadetud andmeid kasutava rakenduse loomine](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps).
    - Valige **Rakenduse suurus**, mis on kooskõlas manustatava rakenduse tüübiga. Valige **Peenike** mobiilsetele seadmetele loodud rakenduste jaoks ja **Lai** tahvelarvutitele loodud rakenduste jaoks. See tagab, et manustatud rakenduse jaoks eraldatakse piisavalt ruumi.
    - Kiirkaardil **Juriidilised isikud** saate määrata, milliste juriidiliste isikute jaoks see rakendus saadaval on. Vaikimisi tehakse rakendus juurdepääsetavaks kõigile juriidilistele isikutele. See suvand on saadaval ainult siis, funktsioon [Salvestatud vaated](saved-views.md) on keelatud. 

4. Kui olete veendunud, et Power Appi konfiguratsioon on õige, klõpsake Power Appi lehele manustamiseks suvandit **Lisa**. Manustatud rakenduse nägemiseks palutakse teil brauserit värskendada.

## <a name="sharing-an-embedded-app"></a>Manustatud rakenduse ühiskasutusse andmine

Kui olete lõuendirakenduse lehel manustanud ja veendunud, et see töötab korrektselt mis tahes lehelt edastatud andmekonteksti puhul, võite rakendust teiste süsteemis olevate kasutajatega jagada. Manustatud lõuendirakenduse jagamiseks toimige järgmiselt.

1. [Jagage lõuendirakendust](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) sobivate kasutajatega, et nad pääseksid rakendusele Power Appsis juurde. 

2. Veenduge, et sihtkasutajatel oleksid sobivad isikupärastamised, et lehekülge vaadates kuvataks neile manustatud rakendus. Saate kasutada üht järgmistest meetoditest.

    - Soovitatav: kasutage funktsiooni [Salvestatud vaated](saved-views.md), et luua ja avaldada vaade, mis sisaldab manustatud rakendust. Selle meetodi puhul on tagatud, et kõik kasutajad, kellel on avaldatud vaatega seotud turberollid, näevad rakendust Finance and Operationsi rakendustes. 
    - Kui salvestatud vaadete funktsioon pole sisse lülitatud, võite paluda süsteemiadministraatoril rakendada isikupärastamist, mis teeb manustatud rakenduse kättesaadavaks kõigile kasutajatele või kasutajate alamhulgale. Teise võimalusena saate eksportida oma lehe isikupärastamised ja saata need ühele või mitmele kasutajale. Need kasutajad saavad seejärel isikupärastamisi importida. Isikupärastamise tööriistaribal on tegevused, mis võimaldavad teil isikupärastamisi eksportida ja importida. 
    
> [!NOTE]
> Kui lõuendirakendust on jagatud väliskasutajatega, ei saa nad kasutada manustatud rakendust Finance and Operationsi rakendustes. Siiski pääsevad nad rakendusele juurde otse Power Appsis. Väliskasutajad hõlmavad külalisi ja kasutajaid, kes ei kuulu Microsoft 365 Azure Directorysse, kus on juurutatud Finance and Operationsi rakendus.

Toote isikupärastamise võimaluste ja nende kasutamise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Finance and Operationsi rakendustest saadetud andmeid kasutava lõuendirakenduse loomine

Kui loote lõuendirakenduse, mis manustatakse Finance and Operationsi rakenduses, on sellest Finance and Operationsi rakendusest pärit sisendandmete kasutamine oluline protsessi osa. Power Appsi arendamiskogemuse põhjal on võimalik pääseda Finance and Operationsi rakendusest edastatavatele andmetele juurde muutuja **Param("EntityId")** abil.

Näiteks saate Finance and Operationsi rakenduste sisendandmed rakenduse funktsioonis OnStart seadistada järgmiseks muutujaks.

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Lõuendirakenduse kuvamine

Manustatud lõuendirakenduse kuvamiseks Finance and Operationsi rakenduste lehel avage lihtsalt manustatud rakendust sisaldav leht. Pidage meeles, et rakendustele on võimalik juurde pääseda standardsel toimingupaanil asuva nupu **Power Apps** kaudu. Teise võimalusena võidakse need kuvada otse lehel uue vahekaardi, kiirkaardi või labana või tööruumis uue jaotisena. Kui kasutajad püüavad rakendust esimest korda lehel laadida, palutakse neil sisse logida. Selle abil tagatakse, et kasutajatel oleksid rakenduse kasutamiseks sobivad load.

## <a name="editing-an-embedded-app"></a>Manustatud rakenduse redigeerimine

Kui rakendus on lehele manustatud, võib tekkida vajadus muuta rakenduse konfiguratsiooni. Näiteks võite soovida muuta manustatud rakendusega seotud silti või on loodud rakenduse uus versioon ja teil on vaja värskendada rakenduse ID-d, et viidata uusimale PowerAppile.

Manustatud rakenduse konfiguratsiooni redigeerimiseks tehke järgmist.

1. Avage paan **Redigeeri rakendust**.

    - Kui kasutate manustatud rakenduse avamiseks menüünuppu Power Apps, paremklõpsake menüünuppu Power Apps ja valige suvand **Isikupärasta**. Valige rippmenüüst **Valige rakendus** see rakendus, mida soovite konfigureerida.
    - Kui manustatud rakendus kuvatakse otse lehel, valige **Suvandid** ja seejärel **Isikupärasta see leht**. Klõpsake **valimistööriista** kasutades manustatud rakendust.

2. Tehke vajalikud muudatused rakenduse konfiguratsioonis ja klõpsake **Salvesta**.

## <a name="removing-an-app"></a>Rakenduse eemaldamine

Kui lehele on manustatud rakendus, on vajaduse korral võimalik seda eemaldada kahel viisil.

- Avage paan **Redigeeri rakendust**, selleks leiate juhtnöörid selle teema varasemast jaotisest [Manustatud rakenduse redigeerimine](#editing-an-embedded-app). Veenduge, et see paan kuvab teavet eemaldada soovitud rakenduse kohta, ja seejärel klõpsake nuppu **Kustuta**.
- Kuna manustatud rakendus salvestatakse isikupärastamisandmetena, eemaldatakse lehe isikupärastamiste kustutamisel ka lehele manustatud rakendused. Pange tähele, et lehe isikupärastamised kustutatakse jäädavalt ja seda ei saa tagasi võtta. Lehe isikupärastamiste eemaldamiseks valige **Suvandid** ja seejärel klõpsake **Isikupärasta see leht** ja lõpuks nuppu **Tühjenda**. Pärast brauseri värskendamist on kõik lehe varasemad isikupärastamised eemaldatud. Isikupärastamist kasutavate lehtede optimeerimise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="appendix"></a>Lisa

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Arendajale] Rakenduse manustamise asukoha täpsustamine

Vaikimisi saavad kasutajad rakendusi manustada mis tahes lehele kas Power Appsi menüünuppu kasutades või otse lehele vahekaardina, kiirkaardina, labana või tööruumi puhul jaotisena lisades. Ent kui see on vajalik, saavad arendajad järgmiste meetodite abil seda funktsiooni konfigureerida selliselt, et rakendusi saab manustada ainult teatud lehtedele.

- **isPowerAppPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei kuvata Power Appsi menüünuppu ja kasutajad ei saa rakendusi kusagile lehele manustada, sh vahekaardina.
- **isPowerAppTabPersonalizationEnabled** – kui see meetod annab teatud lehe puhul väärtuseks vale, ei saa kasutajad rakendusi otse vahekaardina, kiirkaardina või panoraamjaotisena lehele manustada. Kasutajatel on siiski võimalus manustada rakendusi Power Appsi menüünupu abil, kui lehel on manustamine lubatud.

Järgmises näites on toodud uus klass kahe konfigureerimist vajava meetodiga, kuhu rakendusi saab manustada.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]