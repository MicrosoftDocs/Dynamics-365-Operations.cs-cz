---
title: Přehled tisku dokumentu
description: Dokumenty můžete tisknout buď pomocí lokální tiskárny nebo zařízení připojeného k síti. Tento článek poskytuje přehled způsobu tisku dokumentů.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d41e299f0076e1016e8ddae8584bfec338a73a9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749386"
---
# <a name="document-printing-overview"></a><span data-ttu-id="1d7e5-104">Přehled tisku dokumentu</span><span class="sxs-lookup"><span data-stu-id="1d7e5-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d7e5-105">Dokumenty můžete tisknout buď pomocí lokální tiskárny nebo zařízení připojeného k síti.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="1d7e5-106">Tento článek poskytuje přehled způsobu tisku dokumentů.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="1d7e5-107">Přehled tisku</span><span class="sxs-lookup"><span data-stu-id="1d7e5-107">Printing overview</span></span>

<span data-ttu-id="1d7e5-108">Aplikace poskytuje integrované služby a klientské aplikace, které usnadňují generování, ukládání a distribuci dokumentů, které podporují podnikatelské aktivity.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="1d7e5-109">Dokumenty můžete tisknout buď pomocí lokální tiskárny nebo zařízení připojeného k síti.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="1d7e5-110">Kromě toho můžete exportovat stránky a sestavy aplikace přímo z klienta jako soubory PDF nebo dokumenty Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="1d7e5-111">V neposlední řadě vám distribuované pracovní vytížení umožňuje tisknout obchodní dokumenty přímo z mobilní zařízení pomocí síťových prostředků.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="1d7e5-112">Přestože se požadavky na tisk mohou lišit, všechna odvětví obvykle musí vytvářet tištěné kopie obchodních dokumentů pomocí aplikace.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="1d7e5-113">Tisk dokumentů na síťových zařízeních z hostovaných aplikací představuje ojedinělou řadu výzev.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="1d7e5-114">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="1d7e5-114">Here are some examples:</span></span>

- <span data-ttu-id="1d7e5-115">Tiskové ovladače nemusí být k dispozici na zařízeních uživatele.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="1d7e5-116">Zařízení uživatele nemusí být připojeno k firemní síti.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="1d7e5-117">Pomocí vyhrazeného hostitele a několika jednoduchých kroků mohou správci systému nakonfigurovat nasazení tak, aby uživatelé mohli tisknout přímo z podnikových aplikací na síťových zařízeních.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="1d7e5-118">Scénáře tisku aplikací</span><span class="sxs-lookup"><span data-stu-id="1d7e5-118">Application printing scenarios</span></span> 

<span data-ttu-id="1d7e5-119">V následující tabulce jsou popsány tři hlavní scénáře tisku.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="1d7e5-120">Scénář</span><span class="sxs-lookup"><span data-stu-id="1d7e5-120">Scenario</span></span>                        | <span data-ttu-id="1d7e5-121">Cíl</span><span class="sxs-lookup"><span data-stu-id="1d7e5-121">Goal</span></span>                                                      | <span data-ttu-id="1d7e5-122">Řešení</span><span class="sxs-lookup"><span data-stu-id="1d7e5-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="1d7e5-123">1. Tisk toho, co vidíte</span><span class="sxs-lookup"><span data-stu-id="1d7e5-123">1. Printing what you see</span></span>        | <span data-ttu-id="1d7e5-124">Tiskněte to, co je momentálně zobrazeno v prohlížeči.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="1d7e5-125">Pro prohlížeč se vygeneruje pro tisk vhodná verze webové stránky.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="1d7e5-126">2. Interaktivní tisk</span><span class="sxs-lookup"><span data-stu-id="1d7e5-126">2. Interactive printing</span></span>         | <span data-ttu-id="1d7e5-127">Tiskněte přesný dokument na místně připojeném zařízení.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="1d7e5-128">Můžete exportovat PDF verzi sestavy a stáhnout ji do prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="1d7e5-129">3. Tisk na síťovém zařízení</span><span class="sxs-lookup"><span data-stu-id="1d7e5-129">3. Printing on a network device</span></span> | <span data-ttu-id="1d7e5-130">Odešlete přesný dokument do domény tiskárny.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="1d7e5-131">Přesný dokument je odeslán do klientské aplikace spuštěné na serveru, který je hostován v doméně zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="1d7e5-132">Protože se řešení liší, v závislosti na scénáři poskytují aplikace vestavěné služby a nástroje, které uživatelům pomáhají dosáhnout svých cílů:</span><span class="sxs-lookup"><span data-stu-id="1d7e5-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="1d7e5-133">**Scénář 1** je podporován vykreslováním prohlížeče HTML5 klienta.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="1d7e5-134">**Scénář 2** používá aplikace klienta a služeb Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="1d7e5-135">**Scénář 3** vyžaduje podporu od aplikací klienta a služeb, které jsou hostovány v Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="1d7e5-136">Kromě platformy, která je nasazena do předplatného Azure, aplikace Finance and Operations poskytuje zákazníkům integrovanou aplikaci Azure první strany, která jim pomáhá snadněji využívat zařízení hostovaná na doméně pro tisk dokumentů.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="1d7e5-137">Přehled služby</span><span class="sxs-lookup"><span data-stu-id="1d7e5-137">Service overview</span></span>
<span data-ttu-id="1d7e5-138">Zatímco dokumenty vytvořené hostovanými aplikacemi čekají na tisk na zařízení připojeném k síti, jsou uloženy v úložišti objektu blob Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="1d7e5-139">[Instalace agenta směrování dokumentu pro aktivaci síťového tisku](install-document-routing-agent.md) používá ověřování Azure k vytvoření zabezpečeného kanálu do služeb Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="1d7e5-140">**Pořadí spouštění**</span><span class="sxs-lookup"><span data-stu-id="1d7e5-140">**Execution sequence**</span></span>

1. <span data-ttu-id="1d7e5-141">Sestava je generovaná pomocí aplikace Microsoft SQL Server Reporting Services (SSRS) a uložena do úložiště objektů blob Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="1d7e5-142">Nastavení připojené tiskárny jsou uložena spolu s dokumenty.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="1d7e5-143">Agent pro směrování dokumentů se dotáže fronty sběrnice služby Azure na aktivní úlohy.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="1d7e5-144">Dokument je stažen agentem pro směrování dokumentů a zařazen na síťovou tiskárnu.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="1d7e5-145">Řešení založené na klientovi umožňuje zákazníkům spravovat rozsah jejich tiskových potřeb.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="1d7e5-146">Zákazníci, kteří pracují s velkým objemem tisku, mohou nainstalovat mnoho agentů pro směrování dokumentů, aby se zvýšil počet souběžných tiskových operací.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="1d7e5-147">Někteří zákazníci oproti tomu vyžadují velmi málo instalací agentů pro směrování dokumentů, aby zvládli své očekávané potřeby tisku.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="1d7e5-148">Servisní komponenty pro síťový tisk</span><span class="sxs-lookup"><span data-stu-id="1d7e5-148">Service components for network printing</span></span>

<span data-ttu-id="1d7e5-149">Následující diagram znázorňuje základní komponenty, které pomáhají s podporou operací síťového tisku.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="1d7e5-150">[![servisní-komponenty-pro-síťový-tisk\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="1d7e5-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="1d7e5-151">Všimněte si, že jednu tiskárnu lze registrovat s více agenty pro směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="1d7e5-152">Chcete-li vyřešit předvolby tiskárny, hostovaná služba používá síťovou cestu, která jednoznačně identifikuje každou síťovou tiskárnu.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="1d7e5-153">Výsledkem je, že i když je tiskárna registrována více klienty, zobrazí se jako jedna volba v seznamu tiskáren dostupných v aplikacích.</span><span class="sxs-lookup"><span data-stu-id="1d7e5-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]