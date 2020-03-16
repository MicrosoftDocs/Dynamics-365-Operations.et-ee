---
title: Power Appsi manustamine
description: Selles teemas kirjeldatakse, kuidas manustada Power Appsi klienti, et tõsta toote funktsionaalsust.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042938"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Appsi manustamine

[!include [banner](../includes/banner.md)]

Finance and Operations toetab integratsiooni Microsoft Power Appsiga, mis on mõeldud arendajatele ja mittetehnilistele kasutajatele kohandatud ärirakenduste ehitamiseks mobiilsideseadmete, tahvelarvutite ning veebi jaoks ilma koodi kirjutamata.  Teie, teie organisatsiooni või laiema ettevõtete „ökosüsteemi” arendatud Power Appsi saab lisada Finance and Operationsi rakendustesse, et võimendada toote funktsionaalsust. Näiteks võite luua rakenduse Power Appsist, mis täiendab rakendust Finance and Operations teisest süsteemist toodud teabega.

Lisateavet Power Appsi manustamise kohta vaadake lühivideost [Kuidas manustada Power Appsi rakendusse](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Manustatud rakenduse lisamine Power Appsist lehele

### <a name="overview"></a>Ülevaade

Enne Power Appsist rakenduse klienti manustamist peate esmalt leidma või looma soovitud visuaalide ja/või funktsionaalsusega rakenduse. Siin ei kirjeldata rakenduste üksikasjalikku loomisprotsessi. Kui olete alles uus Power Appsi kasutaja, siis teema  [Power Appsi sissejuhatus](https://docs.microsoft.com/powerapps/getting-started) on heaks algukspunktiks.

Kui olete valmis konkreetset rakendust manustama, on teil valida kahe võimaluse vahel, kuidas rakendust lehel avada, olenevalt sellest, milline viis teile paremini sobib. Esimene võimalus on kasutada standardselt toimingupaanile lisatud nuppu Power Apps. Sedasi lisatud rakendused  kuvatakse Power Appsi menüünupus menüü üksusena. Valimisel avab iga menüü-üksus külgpaani, mis sisaldab manustatud rakendust. Teise võimalusena saate rakenduse manustada otse lehel uue vahekaardina, kiirkaardina, labana või uue jaotisena tööruumis.

Manustatud rakenduse konfigureerimisel saate valida ühe välja, mida kontekstina rakendusse saata. See võimaldab rakendusel reageerida praegu vaadatavate andmete põhjal.

### <a name="details"></a>Üksikasjad

Järgmised juhised näitavad, kuidas manustada rakendust Power Appsist veebiklienti.

1. Minge lehele, kuhu soovite rakendust manustada. See on sama leht, mis sisaldab mis tahes andmeid, mis tuleb rakendusse sisendina edastada.
2. Avage paan **Lisa rakendus Power Appsist**.

    - Klõpsake valikut **Suvandid** ja seejärel valige **Isikupärasta see leht**. Valige menüüst **Lisa** suvand **Power Apps**. Lõpuks valige piirkond, kuhu soovite rakendust lisada. Kui soovite rakendust menüünupu Power Apps alt manustada, valige toimingupaan. Kui soovite rakendust otse lehele manustada, valige asjakohane vahekaart, kiirkaart, laba või jaotis (kui kasutate tööruumi).
    - Kui rakenduse avamiseks kasutatakse menüünuppu Power Apps, võite teise võimalusena klõpsata standardse toimingupaani menüünuppu **Power Apps** ja valida seejärel suvandi  **Lisa rakendus**.

3. Manustatud rakenduse konfigureerimine.

    - Väljal **Nimi** on näidatud tekst, mis kuvatakse manustatud rakendust sisaldava nupu või vahekaardi jaoks. Sageli korratakse sellel väljal rakenduse nime.
    - **Rakenduse ID** on manustatava rakenduse GUID. Selle väärtuse toomiseks leidke rakendus aadressilt [web.powerapps.com](https://web.powerapps.com) ja seejärel väli **Rakenduse ID** jaotisest **Üksikasjad**.
    - Välja **Rakenduse sisendkontekst** jaoks võite valida ka välja, mis sisaldab andmeid, mida soovite rakenduse sisendina edastada. Üksikasju, kuidas rakendus saab juurdepääsu rakendusekomplektist Finance and Operations saadetud andmetele, vaadake selle jaotise allpool olevast teemast [Finance and Operationsi rakendustest saadetud andmeid kasutava rakenduse loomine](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps).
    - Valige **Rakenduse suurus**, mis on kooskõlas manustatava rakenduse tüübiga. Valige **Peenike** mobiilsetele seadmetele loodud rakenduste jaoks ja **Lai** tahvelarvutitele loodud rakenduste jaoks. See tagab, et manustatud rakenduse jaoks eraldatakse piisavalt ruumi.
    - Kiirkaardil **Juriidilised isikud** saate määrata, milliste juriidiliste isikute jaoks see rakendus saadaval on. Vaikimisi tehakse rakendus juurdepääsetavaks kõigile juriidilistele isikutele. See suvand on saadaval ainult siis, funktsioon [Salvestatud vaated](saved-views.md) on keelatud. 

4. Kui olete veendunud, et Power Appi konfiguratsioon on õige, klõpsake Power Appi lehele manustamiseks suvandit **Lisa**. Manustatud rakenduse nägemiseks palutakse teil brauserit värskendada.

## <a name="sharing-an-embedded-app"></a>Manustatud rakenduse ühiskasutusse andmine

Kui olete rakenduse lehele manustanud ja veendunud, et see töötab korrektselt mis tahes lehelt edastatud andmete konteksti puhul, võite seda manustatud PowerAppi teistele süsteemis olevatele kasutajatele ühiskasutusse anda. Seda saab toote isikupärastamisvõimalusi kasutades teha kahel viisil.

- Soovitatav on seda teha süsteemi administraatori kaudu, kes saab isikupärastamise avaldada kõigile kasutajatele või kasutajate alamkogumile.
- Teise võimalusena saate lehe isikupärastamised eksportida, saata need ühele või mitmele kasutajale ja igaüks neist saab muudatused importida. Isikupärastamise tööriistaribal on toiminguid, mis võimaldavad teil isikupärastamisi eksportida ja importida.

Toote isikupärastamise võimaluste ja nende kasutamise kohta vaadake lisateavet teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Rakenduse ehitamine, mis võimendab rakendustekomplektist Finance and Operations saadetud andmeid

Oluline osa Power Appsist rakenduse loomisest, mis manustatakse rakendusse Finance and Operations on selle rakenduse sisendandmete kasutamine. Power Appsi arenduse kogemuse põhjal pääseb Finance and Operationsi rakendusest edastatavate andmed juurde, kasutades muutujat Param("EntityId").

Näiteks saate Finance and Operationsi rakenduste sisendandmed rakenduse funktsioonis OnStart seadistada järgmiseks muutujaks.

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Rakenduse kuvamine

Manustatud rakenduse kuvamiseks Finance and Operationsi rakenduste lehel avage lihtsalt manustatud rakendusega leht. Meenutuseks, et rakendusi saab avada standardse toimingupaani nupuga Power Apps või see võib olla kuvatud otse lehel vahekaardina, kiirkaardina, labana või tööruumi puhul uue jaotisena. Kui kasutaja püüab esimest korda rakendust lehele laadida, palutakse tal i sisse logida, tagamaks, et kasutajal on olemas vajalikud load rakenduse kasutamiseks.

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

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Arendaja kontroll rakenduse manustamise asukohtade üle

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
