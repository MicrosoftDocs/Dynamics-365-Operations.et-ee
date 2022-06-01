---
title: KliendiAndmete integreerimine e-kaubanduse saidi lehtedele
description: See teema kirjeldab, kuidas integreerida Microsoft Dynamics 365 Customer Voice Dynamics 365 Commerce e-äri saitide lehtedele.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 272ec1a59ed45b2d2336dcfea16051d27011360f
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767920"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>KliendiAndmete integreerimine e-kaubanduse saidi lehtedele

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas integreerida Microsoft Dynamics 365 Customer Voice Dynamics 365 Commerce e-äri saitide lehtedele.

Saate integreerida [CustomerKlienditeeninduse](https://dynamics.microsoft.com/customer-voice/overview/) oma e-äri saidile, et koguda, analüüsida ja jälgida reaalajas kliendi tagasisidet. Integratsiooniga alustamiseks peate kogutava tagasiside tüübi jaoks looma konto ja valima kliendi projektimalli.

## <a name="integrate-the-customer-voice-service"></a>Kliendi klienditeeninduse integreerimine

Kliendi Konto loomiseks minge Kliendi Saatele [ja](https://dynamics.microsoft.com/customer-voice/overview/) järgige viipasid.

Kui olete kliendikonto salvestatud ja sisse loginud, peate kogutava tagasiside tüübi jaoks valima projektimalli.

Kliendi projektimalli valimiseks järgige neid samme.

1. Minge kliendi [Projektimalli lehele](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Valige **suvand Alusta**.
1. Valige kogutava tagasiside tüübi projektimall ja seejärel valige **Edasi**.
1. Valige **manustamisvorming** **vahekaardi Saada jaotises Vali** manustamisvorming. Väljal **Manustatud** kood kuvatakse Kood, mis peab olema Commerce'i saidiloojale manustatud.

Selles teemas toodud näited kasutavad perioodilist **kliendi** uuringuprojekti malli ja **nupu** manustatud vormingut.

Järgmine näite näide näitab **perioodilist** kliendi uuringuprojekti mallilehte, **kus** on valitud suvand Nupu manustamisvorming ja **selle** suvandi manustamiskood kuvatakse väljal Manustatud kood. Antud koodi oma saidi lehtedele kaasamiseks on vaja kolm eraldi tegevust, nagu kirjeldatud järgmistes jaotistes.

![Kliendi Perioodiline kliendi uuringuleht koos valitud nupu suvandiga.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Manusta välise skripti URL

Kõigil saidilehtedel, kus peaks olema kliendi Saateuuring, peate manustama välise skripti URL-i, mille Customer Antud kood sisaldab Customer Antud koodis. Parim viis skripti kaasamiseks mitmele saidilehele on luua killus saidikonstruktoris, mis sisaldab välise skripti URL-i, ja seejärel lisada killus sobivale lehekülje mallile. Pärast värskendatud malli avaldamist sarnaneb manustatud väline skriptikood mõjutatud saidi lehtedel järgmise näitega.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Teavet killust kohta vt teemast [Killustega töö](work-with-fragments.md).

> [!NOTE]
> Tükile tuleb lisada ainult URL. Väline skriptimoodul lisab teise skriptikoodi.

Välise skripti URL-i killustamiseks järgige neid samme.

1. Looge saidikonstruktoris välisel skriptimoodulil [põhinev killust](script-module.md).
1. Uuel tükil valige vaikimisi **väline skriptipesa**.
1. Välise skripti **atribuutide vaikepaanil** väljale **Skripti allikas** sisestage väline skripti URL, nagu näidatud järgmises näite näites.

    ![Uue tüki välise skripti URL skripti lähteväljal.](media/customer-voice-integration-2.png)

1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. **Tüki avaldamiseks** valige käsk Avalda.

Manustatud välise skripti blokki sisaldav uus killus on nüüd valmis lisama sobivale leheküljemallile.

### <a name="embed-the-external-style-sheet-code"></a>Kaasa väline laadilehe kood

Seejärel peate kõigil saidilehtedel, kus peaks olema Customer Exceli uuring, manustama välise laadilehe koodi, mille CustomerMeetri manustas manustamiskoodile. Nagu eelmises jaotises, on parim viis mitme saidi lehe välise laadilehe koodi kinnistada, luua tüki saidikonstruktoris, mis sisaldab laadilehe koodi, ja seejärel lisada tüki sobivale leheküljemallile. Manustatud väline laadilehe kood sarnaneb järgmise näite koodiga.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Välise laadilehe koodi killustamiseks järgige neid samme.

1. Looge saidikonstruktoris metasildade [moodulil põhinev killus](metatags-module.md).
1. Tükis valige vaikimisi **metamärgipesa**.
1. Sisestage **metasiltide atribuutide** vaikepaani **väljale Meta sildid** laadilehe kood, nagu näha järgmises näite näites.

    ![Välise laadilehe kood väljal Meta sildid uue tüki jaoks.](media/customer-voice-integration-3.png)

1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. **Tüki avaldamiseks** valige käsk Avalda.

Manustatud välise laadilehe koodi sisaldav uus killus on nüüd valmis lisama sobivale lehemallile.

### <a name="embed-the-inline-script-code"></a>Manusta tekstisisese skripti kood 

Seejärel peate kõigil saidilehtedel, kus peaks olema Customer Exceli uuring, manustama tekstisisese skripti koodi, mille CustomerMeetri manustas manustamiskoodile. Nagu eelmistes jaotistes, on parim viis mitme saidi lehekülje tekstisisese skripti koodi kinnistada, et luua saidikonstruktoris killus, mis sisaldab tekstisisese skripti koodi, ja seejärel lisada killust asjakohastele leheküljemallidele.

Järgmises tekstisisese skripti koodi näites on uuringuvõti **\_** kohatäitja. UURINGUVÕTME väärtus **peab\_ vastama** rel tegelikule uuringuvõtmele, mille CustomerMeetri manustamiskoodis esitas. Viimane rida helistab koodile, et renderdada uuringunuppu ühe sekundi pärast, tagamaks, et skriptidele on laadimiseks piisavalt aega. Sõltuvalt valitud uuringust, peate võib-olla lisama või uuendama ka teisi metaandmeid, nt ettevõtte nime.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Tekstisisese skripti koodi killustamiseks järgige neid samme.

1. Saidikonstruktoris looge tükihind, mis põhineb [tekstisisesel skriptimoodulil](script-module.md).
1. Tükis valige vaikimisi **tekstisisese skripti pesa**.
1. Sisestage **tekstisisese** **skripti** atribuutide paanile Vaikimisi tekstisisese skripti atribuudid tekstisisese skripti kood, nagu näha järgmises näite näites.

    ![Tekstisisese skripti kood tekstisisese skripti väljal uue tüki jaoks.](media/customer-voice-integration-4.png)

1. Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.
1. **Tüki avaldamiseks** valige käsk Avalda.

Manustatud tekstisisese skripti koodi sisaldav uus killus on nüüd valmis lisama sobivale leheküljemallile.

## <a name="add-fragments-to-a-template"></a>Killude lisamine mallile

Kui olete lõpetanud killustide loomise, mis sisaldavad Kliendi manuskoodi, peate need lisama nende saidilehtedega seotud mallidele, kus soovite neid kasutada. Järgmises näites on toote üksikasjade lehele (PDP) lisatud kolm näidet.

![PDP mallile lisatud näite fragmendid.](media/customer-voice-integration-5.png)

Pärast värskendatud malli avaldamist kuvatakse Kliendi Saateuuring kõigil malliga kontrollitud lehtedel.

Lisateavet mallide kohta vt "Töötamine [mallidega"](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Sisu turbepoliitika konfigureerimine

Vaikimisi ei luba sisu turbepoliitika (CSP) kõnesid muudele teenustele, kui muud konfiguratsiooni pole tehtud. Seetõttu on pärast värskendatud mallide avaldamist tõenäoline, et uuringu laadimist asjakohastele saidilehtedele ei õnnestu. CSP-ga seotud tõrgete vaatamiseks avage veebibrauseri arendaja tööriistad (F12) ja minge uuringuga lehele. CSP-ga seotud tõrked ilmuvad konsooli väljundis.

CsP konfigureerimiseks saidikonstruktoris tõrgete parandamiseks järgige neid samme.

1. Avage **Saidi sätted \> Laiendused**.
1. **Lisage sisu turbepoliitika** vahekaardil alam-src `https://customervoice.microsoft.com/`**direktiivile**.
1. Lisa `https://customervoice.microsoft.com/` raam-src **direktiivile**.
1. Saate `https://mfpembedcdnmsit.azureedge.net` lisada **azureedge.net** **·** .rc.

Lisateavet leiate teemast [Sisu turbepoliitika](manage-csp.md).

## <a name="additional-resources"></a>Lisaressursid

[Väline skriptimoodul](script-module.md)

[Metasiltide moodul](metatags-module.md)

[Tekstisisese skripti moodul](script-module.md)

[Sisu turbepoliitika](manage-csp.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Mallidega töötamine](work-with-templates.md)
