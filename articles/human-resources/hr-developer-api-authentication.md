---
title: Autentimine
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008800"
---
# <a name="authentication"></a><span data-ttu-id="32993-102">Autentimine</span><span class="sxs-lookup"><span data-stu-id="32993-102">Authentication</span></span>

<span data-ttu-id="32993-103">See artikkel annab ülevaate teabest, kuidas autentida rakenduse Microsoft Dynamics 365 Human Resources andmete rakenduse programmeerimisliidese (API) abil.</span><span class="sxs-lookup"><span data-stu-id="32993-103">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="32993-104">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="32993-104">Overview</span></span>

<span data-ttu-id="32993-105">Rakenduse Human Resources andmete API on OData juurutus.</span><span class="sxs-lookup"><span data-stu-id="32993-105">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="32993-106">Lisateavet vaadake teemast [Avatud andmeprotokoll (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="32993-106">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="32993-107">Teie rakendus peab autentima autoriseeritud kutsujana, enne kui API teenindab teie rakendusest taotlusi.</span><span class="sxs-lookup"><span data-stu-id="32993-107">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="32993-108">Põhisätted</span><span class="sxs-lookup"><span data-stu-id="32993-108">Fundamentals</span></span>

<span data-ttu-id="32993-109">Andmete API kutsumiseks peab teie rakendus hankima Microsofti identiteedi platvormilt juurdepääsuloa.</span><span class="sxs-lookup"><span data-stu-id="32993-109">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="32993-110">Juurdepääsuluba sisaldab teavet teie rakenduse kohta ja luba, et see peab rakenduses Human Resources ressursse kutsuma.</span><span class="sxs-lookup"><span data-stu-id="32993-110">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="32993-111">Juurdepääsuluba</span><span class="sxs-lookup"><span data-stu-id="32993-111">Access token</span></span>

<span data-ttu-id="32993-112">Microsofti identiteedi platvormi väljastatud juurdepääsuluba on Base64-kodeeringuga JavaScript Object Notationi (JSON) veebiload (JWTs).</span><span class="sxs-lookup"><span data-stu-id="32993-112">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="32993-113">Need sisaldavad teavet (nõudeid), et andmete API (ja muud veebi API-d, mis on turvatud Microsofti identiteedi platvormiga) kasutavad kutsuja kinnitamist ja tagavad, et kutsujal on taotletud toimingu teostamiseks vajalikud load.</span><span class="sxs-lookup"><span data-stu-id="32993-113">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="32993-114">Kutsumiste ajal saate käsitleda juurdepääsulubasid läbipaistmatutena.</span><span class="sxs-lookup"><span data-stu-id="32993-114">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="32993-115">Peaksite alati edastama juurdepääsulubasid üle turvalise kanali, nt Transport Layer Security (TLS) ja Hypertext Transfer Protocol Secure (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="32993-115">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="32993-116">Siin on juurdepääsuloa näide, mille on väljastanud Microsofti identiteedi platvorm.</span><span class="sxs-lookup"><span data-stu-id="32993-116">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="32993-117">Andmete API kutsumiseks lisate juurdepääsuloa oma HTTP-taotluse autoriseerimise päisesse vastutaja loana.</span><span class="sxs-lookup"><span data-stu-id="32993-117">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="32993-118">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="32993-118">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="32993-119">Uue rakenduse registreerimine Azure’i portaali kasutades</span><span class="sxs-lookup"><span data-stu-id="32993-119">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="32993-120">Logige [Microsoft Azure’i portaali](https://portal.azure.com) töö- või koolikontoga või isikliku Microsofti kontoga sisse.</span><span class="sxs-lookup"><span data-stu-id="32993-120">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="32993-121">Kui teie konto annab teile juurdepääsu rohkem kui ühele rentnikule, valige ülemises parempoolses nurgas oma konto ja seadke oma portaali seanss Azure Active Directory (Azure AD) soovitud rentnikule.</span><span class="sxs-lookup"><span data-stu-id="32993-121">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="32993-122">Vasakpoolsel paanil valige teenus **Azure Active Directory** ja seejärel valige **Rakenduse registreerimised \> Uus registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="32993-122">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="32993-123">Kui ilmub leht**Rakenduse registreerimine**, sisestage oma rakenduse registreerimisteave.</span><span class="sxs-lookup"><span data-stu-id="32993-123">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="32993-124">**Nimi**: sisestage tähendusega rakenduse nimi, mis kuvatakse rakenduse kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="32993-124">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="32993-125">**Toetatud kontotüübid**: valige kontode tüübid, mida teie rakendus peaks toetama.</span><span class="sxs-lookup"><span data-stu-id="32993-125">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="32993-126">Toetatud kontotüübid</span><span class="sxs-lookup"><span data-stu-id="32993-126">Supported account types</span></span> | <span data-ttu-id="32993-127">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="32993-127">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="32993-128">Ainult selle organisatsioonikataloogi kontod</span><span class="sxs-lookup"><span data-stu-id="32993-128">Accounts in this organizational directory only</span></span> | <span data-ttu-id="32993-129">Valige see suvand, kui ehitate tegevusalapõhist rakendust.</span><span class="sxs-lookup"><span data-stu-id="32993-129">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="32993-130">See suvand ei ole saadaval, kui te ei registreeri rakendust kataloogis.</span><span class="sxs-lookup"><span data-stu-id="32993-130">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="32993-131">See suvand on vastendatud suvandiga **Azure AD ainult üks rentnik**.</span><span class="sxs-lookup"><span data-stu-id="32993-131">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="32993-132">See suvand on vaikimisi suvand, kui te ei registreeri rakendust väljaspool kataloogi.</span><span class="sxs-lookup"><span data-stu-id="32993-132">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="32993-133">Sellisel juhul on vaikimisi suvand **Azure AD mitu rentnikku ja isiklikud Microsofti kontod**.</span><span class="sxs-lookup"><span data-stu-id="32993-133">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="32993-134">Mis tahes organisatsioonikataloogi kontod</span><span class="sxs-lookup"><span data-stu-id="32993-134">Accounts in any organizational directory</span></span> | <span data-ttu-id="32993-135">Valige see suvand kõikidele äri- ja haridusklientidele suunamiseks.</span><span class="sxs-lookup"><span data-stu-id="32993-135">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="32993-136">See suvand on vastendatud suvandiga **Azure AD ainult mitu rentnikku**.</span><span class="sxs-lookup"><span data-stu-id="32993-136">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="32993-137">Kui olete rakenduse registreerinud kui **Azure AD ainult üks rentnik**, saate kasutada laba **Autentimine**, et uuendada see valikule **Azure AD ainult mitu rentnikku** ja seejärel tagasi valikule **Azure AD ainult üks rentnik**.</span><span class="sxs-lookup"><span data-stu-id="32993-137">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="32993-138">Kontod mis tahes organisatsioonikataloogides ja isiklikes Microsofti kontodes</span><span class="sxs-lookup"><span data-stu-id="32993-138">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="32993-139">Valige see suvand kõige laiemale klientide kogumile suunamiseks.</span><span class="sxs-lookup"><span data-stu-id="32993-139">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="32993-140">See valik on vastendatud suvandiga **Azure AD mitu rentnikku ja isiklikud Microsofti kontod**.</span><span class="sxs-lookup"><span data-stu-id="32993-140">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="32993-141">Kui olete rakenduse registreerinud kui **Azure AD mitu rentnikku ja isiklikud Microsofti kontod**, ei saa te seda sätet kasutajaliideses (UI) muuta.</span><span class="sxs-lookup"><span data-stu-id="32993-141">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="32993-142">Selle asemel peate toetatud kontotüüpide muutmiseks kasutama rakenduse manifesti redaktorit.</span><span class="sxs-lookup"><span data-stu-id="32993-142">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="32993-143">**Ümbersuunamis-URI (valikuline)** – valige loodava rakenduse tüüp: **veebisait** või **avalik klient (mobiili- ja töölauaga seade)**.</span><span class="sxs-lookup"><span data-stu-id="32993-143">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="32993-144">Seejärel sisestage rakenduse ümbersuunamis-URI (või vastuse URL).</span><span class="sxs-lookup"><span data-stu-id="32993-144">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="32993-145">Veebirakenduste jaoks sisestage rakenduse baas-URL.</span><span class="sxs-lookup"><span data-stu-id="32993-145">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="32993-146">Näiteks võib `http://localhost:31544` olla veebirakenduse URL, mis töötab teie kohalikus masinas.</span><span class="sxs-lookup"><span data-stu-id="32993-146">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="32993-147">Kasutajad kasutavad seejärel seda URL-i, et logida sisse veebikliendi rakendusse.</span><span class="sxs-lookup"><span data-stu-id="32993-147">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="32993-148">Avalike kliendirakenduste jaoks sisestage URI, mida Azure AD kasutab loa vastuste tagastamiseks.</span><span class="sxs-lookup"><span data-stu-id="32993-148">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="32993-149">Sisestage teie rakendusele omane väärtus, nt `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="32993-149">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="32993-150">Veebirakenduste või kohalike rakenduste kohta konkreetsete näidete nägemiseks vaadake lühijuhendeid [Microsofti identiteedi platvormil (varem arendajatele suunatud Azure Active Directory)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="32993-150">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="32993-151">Jaotises **API load** valige suvand **Lisa luba**.</span><span class="sxs-lookup"><span data-stu-id="32993-151">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="32993-152">Seejärel otsige vahekaardil **Minu organisatsiooni kasutatavad API-d** rakendust **Dynamics 365 Human Resources** ja lisage rakendusele luba **kasutaja\_matkimine**.</span><span class="sxs-lookup"><span data-stu-id="32993-152">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="32993-153">Rakenduse Human Resources ID on f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="32993-153">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="32993-154">Kasutage seda ID-d, et tagada õige rakenduse valimine.</span><span class="sxs-lookup"><span data-stu-id="32993-154">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="32993-155">Valige suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="32993-155">Select **Register**.</span></span>

   <span data-ttu-id="32993-156">[![Azure’i portaalis uue rakenduse registreerimine](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="32993-156">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="32993-157">Azure AD määrab rakendusele kordumatu rakenduse ID (kliendi ID) ja viib teid rakenduse lehele **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="32993-157">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="32993-158">Rakendusele täiendavate võimaluste lisamiseks saate valida teisi konfiguratsiooni suvandeid, nagu tootjakohasuse ja sertifikaatide ning saladuste suvandid.</span><span class="sxs-lookup"><span data-stu-id="32993-158">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="32993-159">Juurdepääsuloa toomine</span><span class="sxs-lookup"><span data-stu-id="32993-159">Retrieving an access token</span></span>

<span data-ttu-id="32993-160">Rakenduse Human Resources andmete API juurdepääsuloa hankimise üksikasjad sõltuvad tehnoloogiatest, mida kliendi rakenduse arendamiseks kasutate.</span><span class="sxs-lookup"><span data-stu-id="32993-160">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="32993-161">Näiteks võite [testida kolmanda poole utiliidiga](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (nt Postman), arendades C# konsooli rakendust või veebiteenust või luues Javascripti/TypeScripti kliendi.</span><span class="sxs-lookup"><span data-stu-id="32993-161">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="32993-162">C# kliendi rakenduse näide.</span><span class="sxs-lookup"><span data-stu-id="32993-162">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="32993-163">Kui olete juurdepääsuloa juba hankinud, edastate loa autoriseerimise päises vastutaja loana koos iga taotlusega, mille saadate andmete API-le, nagu eespool kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="32993-163">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
